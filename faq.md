# FAQ


Where is this playbook executed?

- I assume to execute the playbook locally on the VM.

How many concurrent users are possible on the smallest possible instance from e.g. Hetzner ?

- Honestly, I don't know. I have seen 20 Users on one machine, working fine..

Which Jitsi server do you use?

- Use the Jitsi Server of your least distrust. It could be meet.jit.si, it could be your own.

What should I look after in Jitsi server configs.

- There are plenty of config options in Jitsi. Take your time.
- I have had some problems with using Jitsi-internal Authentication

What WorkAdventure do I want to use?

- I use the docker-compose file from `contrib/docker`
- I would opt for using stability over newness
 
Do I need a STUN Server?

- Not that I know of.

Could one implement Authentication and User Groups?

- Probably, you might wanna get that information from thecodingmachine/workadventure
- Alternatively, you could implement that via "Authelia" or something
 
How do you do updates?

- You could re-run the playbook or reset the whole machine

Do you need any help?

- Well, I think I would need help removing traefik and replace it with nginx
- The Authentication is another cup of tea, where help is very appreciated.
- Monitoring the application on application level would also be an interesting topic.


# Notes:

After the *rC3* a group was esablished to create a federated permanent WorkAdventure-Universe. It goes by the name *Fediventure*.
You can join via Matrix: #fediventure:hackerspace.pl

People found out, that Graphic Files with more than 4096 Pixels in height won't be displayed correctly. They will just be displayed as black tiles. Same happens when the Tile-lenghts, which are no Powers of 2. Chromium doesn't cope well with that aspecially.


