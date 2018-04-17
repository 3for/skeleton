# Skeleton dapp.

clone our conveniently prepared skeleton repository:

```
git clone https://github.com/paritytech/skeleton mydapp
```

This will make your a new repo mydapp with everything set up and ready to go. We will cd in to it and remove the origin repository lest it confuse Git:

```
cd mydapp
git remote rm origin
```

It’s liberally licensed (Apache 2.0) so you don’t have to worry about open sourcing your own code (though obviously you’ll be enlightened and want to do that anyway :-)). You’re now free to push it out to your own Git repo, if you decide to create one on Github.

The next stage is to get all the dependencies installed. NPM makes this rather easy, but the bundled script makes it even easier! Just run:

```
./init.sh
```

This should grab and install all that is required. The next thing to do is to build the final web-ready version of the fledgling dapp. We use webpack for this; it’ll smash everything together and provide you with a single bundle.js for you in the dist path, which our index.html (already there) brings in.

```
npm install -g webpack@3.11.0
webpack
```

You now have a basic dapp built. Well done!

Files will be built into `dist/`. Just symlink that dir into your dapps path.

