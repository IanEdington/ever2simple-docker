# IanEdington/ever2simple
This is a very simple port of claytron's ever2simple to docker.

## Why would you want to use this?
You have a beautiful laptop with a perfect settings to run all your dev environments.
Every new package you install increases the likelyhood of breaking your beautiful system.
Using this docker image you can install this software,
      run this command,
      and uninstall,
      all without compromizing your current work environment.
Why risk you dev env when you can dockerize.

## Usage:
Once you have docker installed, running this command will put you into a sh prompt with evernote containing your evernote exprots.

    docker run -it -v {path to evernote exports}:/evernote ianedington/ever2simple

You should then be ablet to cd into the folder and run the ever2simple command.

    ever2simple my_evernote.enex --output simplenote_dir --format dir

Checkout claytron's [ usages section ]( https://github.com/claytron/ever2simple#usage ) for detailed command line instructions.

## technical notes:
Unfortunately, ever2simple won't work on alpine because lxml is built using python instead of being sourced from py-lxml. If this changes please let me know and I will update this image.
