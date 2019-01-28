# AWS GraphicsMagick Lambda Layer

### Statically compiled GraphicsMagick binary with serverless file to setup a lambda layer.


## Usage
Clone the repo and unzip the binary in which is located in the ```bin``` folder.

Run ```sls deploy -v``` to deploy layer with Serverless (you need to have Serverless installed and setup for this...).

You can then reference the layer in your main Serverless .yml file like so:

```
functions:
  myLambda:
    handler: handlers/myLambda.run
    layers:
      - Fn::ImportValue: GraphicsmagickLambdaLayer
```
```GraphicsMagickLambdaLayer``` is specified in the layers .yml file, but you can call it what you want.

