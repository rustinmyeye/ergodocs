## (CPU) Mining your own chain


### Generating genesisStateDigestHex

You will need to generate your `genesisStateDigestHex`, this is a Base16 representation of the *genesis state* roothash and generated configuring your chains values in [src/main/resources/testnet.conf](https://github.com/ergoplatform/ergo/blob/master/src/main/resources/testnet.conf) and then compiling the node. 


### Pre-requisites

You will need to have sbt installed, a build tool for Scala. 

[SDKMAN](https://sdkman.io/) is the easiest way to get setup with sbt. 

```
curl -s "https://get.sdkman.io" | bash 
sdk install sbt
```

### Compiling the node


```
sbt assembly
```

This will create an ergo.jar at `/target/scala*/ergo-*.jar`


### Configuring your .conf file

Your `testnet.conf` should look like this at this stage; 

```
ergo {
  networkType = "testnet"

  node {
    mining = true
    offlineGeneration = true
    useExternalMiner = false
  }
  
  #chain {
  #     genesisStateDigestHex = "Still to be generated at this stage"
  #}
}

scorex {

 network {
    bindAddress = "0.0.0.0:9020"
    nodeName = "ergo-testnet-5"
    #knownPeers = []
  }

 restApi {
    # Hex-encoded Blake2b256 hash of an API key. Should be 64-chars long Base16 string.
    # Below is hash corresponding to API_KEY = "hello" (with no quotes)
    apiKeyHash = "324dcf027dd4a30a932c441f365a25e86b173defa4b8e58948253471b81b72cf"
  }
}
```

### Running the node

```
java -jar -Xmx4G ergo-*.jar --testnet -c testnet.conf
```

The console should return a new `genesisStateDigestHex` value, place that inbetween the quotation marks and uncomment the lines above.

Restart your node and it will now CPU-mine its own chain! 