
# GitHub Action for generating a contribution graph with a snake eating your contributions.

name: Generate Snake

# Controls when the action will run. This action runs every 6 hours.

on:
  schedule:
      # every 6 hours
    - cron: "0 */6 * * *"

# This command allows us to run the Action automatically from the Actions tab.
  workflow_dispatch:

# The sequence of runs in this workflow:
jobs:
  # This workflow contains a single job called "build"
  build:
    # The type of runner that the job will run on
    runs-on: ubuntu-latest

    # Steps represent a sequence of tasks that will be executed as part of the job
    steps:

    # Checks repo under $GITHUB_WORKSHOP, so your job can access it
      - uses: actions/checkout@v2

    # Generates the snake  
      - uses: Platane/snk@master
        id: snake-gif
        with:
          github_user_name: sprout-seedly-berryfunny
          # these next 2 lines generate the files on a branch called "output". This keeps the main branch from cluttering up.
          gif_out_path: dist/github-contribution-grid-snake.gif
          svg_out_path: dist/github-contribution-grid-snake.svg

     # show the status of the build. Makes it easier for debugging (if there's any issues).
      - run: git status

      # Push the changes
      - name: Push changes
        uses: ad-m/github-push-action@master
        with:
          github_token: ${{ secrets.GITHUB_TOKEN }}
          branch: master
          force: true

      - uses: crazy-max/ghaction-github-pages@v2.1.3
        with:
          # the output branch we mentioned above
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}

# ABOUT ME  !!! (°ロ°)
HELLO!!! MY NAME IS DANIEL/KRATCY, free feel to call me any of those. Nicknames are allowed!

 > ***Don't talk about 	<ins>YinYang</ins> from ii to me or you will get blocked with no hesitation.***

<img width="374" height="227" alt="cosmo-dandys-world-cosmo" src="https://github.com/user-attachments/assets/7e82e1a5-ca88-44bb-9733-a4a1bcb7a8b9" />

# For Pony town: (°ロ°)
> Feel free to C+H with me, always w2i, or I'll never see your message since I'm mainly offline on Pony town. Don't copy my ponies but you can get inspo from them, but not too much where you literally just copied the whole thing and changed just a bit. Doesn't matter if I'm talking to someone, afk, sleeping, etc etc, NO NEED TO ASK TO C+H WITH ME!!! JUST DO IT, DON'T BE AFRAID OF ME GETTING MAD OF YOU!

<img width="291" height="277" alt="image" src="https://github.com/user-attachments/assets/37037c6d-ab03-4d94-bf8f-c455dd10812b" />

# For Discord: (°ロ°)
> DM's & friend request are always on, expect me to accept your friend request unless you're in my DNI list. I block freely so if you don't see my bio/status/activity etc than sorry not sorry, I just blocked you. Not really good at comforting so I might be having a hard time trying to make you feel better. Blah blah blah, I'm too lazy to write more for my discord, you can interact with me there, idc.

<img width="386" height="532" alt="image" src="https://github.com/user-attachments/assets/029ea3fe-afff-47e7-a2ec-0ec89a05ed28" />

my user id is <ins>1401063021752746077</ins> if you can't find my profile


more info about me is here!!

https://berryfunnylol.straw.page
(∩^o^)⊃━☆
https://en.pronouns.page/@Sprout.Seedly_

