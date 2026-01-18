
# tactiq.io free youtube transcript
# #01 - Relational Model & Algebra (CMU Intro to Database Systems)
# https://www.youtube.com/watch/APqWIjtzNGE

00:00:05.799 official members bounce bust off the
00:00:08.119 Chrome realize it's real hell what we
00:00:10.639 call Home official members bounce bust
00:00:13.400 off the Chrome realize it's real hell
00:00:16.000 where we from the inside one I Vision
00:00:19.000 fat licks and M Clips the Chrome will
00:00:20.720 make the average imitator do back flips
00:00:23.119 you like a pistol to put the best around
00:00:25.279 the issue never miss coming that's
00:00:28.960 official before we get started I have to
00:00:30.960 read this out
00:00:33.040 um so I do not have child protection
00:00:36.559 clearance for ACT 153 uh this the state
00:00:39.040 law in Pennsylvania so if anybody here
00:00:41.160 is under the age 18 uh you cannot be in
00:00:44.239 this
00:00:45.640 classroom no it's not a joke
00:00:48.160 seriously I don't think they would have
00:00:49.920 notified me just make sure that anybody
00:00:51.160 here who's who's not uh 18 or older um
00:00:54.480 it's a pen state law criminal history
00:00:56.359 patch um I I don't have I I don't have
00:01:00.440 the crial background history or crial
00:01:02.039 history background to pass this so uh
00:01:04.159 again if you're everybody coming in if
00:01:05.400 you're under 18 please leave the room um
00:01:08.159 with that aside I want to give a quick
00:01:09.479 shout out to people who's helped us get
00:01:11.080 here where we are today so this is e in
00:01:13.360 crookland uh JL in Seattle uh and then
00:01:16.560 DJ drop tables unfortunately passed away
00:01:18.240 the summer so rip to him and then DJ
00:01:20.840 Mushu is in lockdown which is a whole
00:01:23.040 another issue uh so we send our respect
00:01:25.840 for him okay all right so with that out
00:01:28.320 of the way uh let's get into to
00:01:30.040 databases so I sort of mentioned this in
00:01:32.640 lecture zero which I did record
00:01:34.000 re-record today I apologize for uh the
00:01:36.840 mic but it should be better now um so as
00:01:40.040 we go along throughout the semester you
00:01:41.119 will see I get very very excited about
00:01:42.600 databases and this is for sort of a a
00:01:45.880 very important reason I only care about
00:01:48.280 two things in my life right the first
00:01:50.799 thing is my wife and my biological
00:01:52.680 daughter and then the second thing is
00:01:54.560 databases I don't care about anything
00:01:56.479 else I don't talk to my family they're
00:01:57.840 all Trump supporters the antiac I don't
00:02:00.119 care about them I don't have any hobbies
00:02:01.680 it's just databases I live what is what
00:02:03.719 you call a database Centric lifestyle
00:02:06.159 and hopefully I hope impart to you guys
00:02:08.160 what that means what that entails and
00:02:09.758 you can continue down the path Beyond
00:02:11.640 this course now earlier last week
00:02:14.720 someone posted this on the seam you
00:02:16.800 Reddit
00:02:18.680 right they want to know whether taking
00:02:20.599 440 or 445 is harder uh because they
00:02:23.599 want to spend their time doing other
00:02:24.920 things in their life right so I chime in
00:02:27.640 and say whoever this person is should
00:02:29.400 not be the course because I don't care
00:02:32.000 whether they think it's hard or easy
00:02:33.640 right you will see throughout the
00:02:35.319 semester that if you take a Viewpoint of
00:02:37.560 everything is pretty much a database
00:02:38.720 problem and then all your time should be
00:02:40.400 spending working on databases uh then
00:02:43.040 you you'll be happier in your life uh so
00:02:45.560 again if I don't know if someone's in
00:02:47.360 the class here that post this uh you
00:02:48.879 don't
00:02:50.120 belong uh again quickly to reminder
00:02:52.400 about the course Logistics I everything
00:02:54.159 is on the course web page all the
00:02:55.720 announcements and discussion for
00:02:57.000 projects homeworks Logistics and other
00:02:58.519 things we've done through Piaza all the
00:03:00.560 homeworks and projects will be submitted
00:03:01.920 through grade scope and autograd your
00:03:03.599 final grades for the actually the
00:03:05.159 mid-semester grades and the final grades
00:03:06.879 for all your projects and homeworks will
00:03:08.280 be in final exams will be posted on
00:03:09.879 canvas um if you're on the wait list I
00:03:13.000 think our Max Capacity is 140 before the
00:03:14.959 Fire Marshall shows up uh and as of uh
00:03:17.599 an hour or so ago we have six open seats
00:03:20.159 and the administrators will fill off
00:03:21.720 people uh from the weight list into that
00:03:23.599 uh so if you're still on the weight list
00:03:24.640 you may have a chance to get in but I I
00:03:26.159 can't guarantee it okay and then if
00:03:28.879 you're not at CMU
00:03:30.480 uh we make everything available for the
00:03:32.720 projects through this grade scope use
00:03:34.239 this code make sure you put yourself as
00:03:36.400 uh as as University of Carnegie melon
00:03:39.080 everybody in this room right now do not
00:03:40.280 do this because then then you won't get
00:03:41.439 a grade and we ask everyone else who's
00:03:43.480 not at CMU who's watching the videos
00:03:45.560 don't post your Solutions on GitHub
00:03:47.239 don't do the stupid thing of spitting
00:03:48.519 the pr with with your code because we're
00:03:50.480 going to put a Wall of Shame up for that
00:03:52.360 and then don't email myself or the Tas
00:03:54.040 if you're not a senior student everybody
00:03:55.439 else here in the class please post on
00:03:56.680 piao and we will respond any questions
00:03:59.079 or comments about any these
00:04:01.120 things again if you're coming in if
00:04:03.040 you're not 18 or older you have to leave
00:04:05.159 the room because of the ACT 153 okay all
00:04:08.879 right so today's agenda we're going to
00:04:11.519 talk about quick background what
00:04:12.720 database systems are that sort of sets
00:04:14.400 us up for what the course will be about
00:04:17.040 uh we'll spend most of our time talking
00:04:18.160 about the relational model and
00:04:19.079 relational algebra this is going to be
00:04:20.639 the Bedrock for how most database
00:04:22.320 systems that you're going to care about
00:04:23.919 uh not all but but most systems uh will
00:04:26.919 be predicated on this we'll talk a
00:04:29.080 little bit about alternative data models
00:04:30.759 that are out there like aod DBS document
00:04:33.479 stuff Json stuff um and Vector databases
00:04:36.520 U but these will sort of be anary to
00:04:38.080 what we talk about this course the core
00:04:40.919 ideas beyond the relational model of how
00:04:43.880 we're going to build these these datab
00:04:45.639 system will be applicable to these other
00:04:47.639 alternative data models it's just I care
00:04:50.520 less about them right because I I care
00:04:52.240 about SQL I care about the relation data
00:04:53.600 model and as I said on Piaza yesterday
00:04:56.880 uh we'll have since this comes up every
00:04:58.440 year people always sort of high level
00:05:00.479 questions about databases throughout the
00:05:02.199 semester I want to try to cover as much
00:05:03.680 as I can at the very beginning uh so if
00:05:05.800 you have any Q&A if you have any
00:05:06.759 questions you want to ask me at the end
00:05:08.039 we can we can take those
00:05:09.800 okay and again as I said on in lecture
00:05:12.759 zero uh I get very excited about
00:05:14.759 databases I talk very fast please tell
00:05:16.440 me to stop and slow down and if you have
00:05:17.960 any questions please interrupt me uh and
00:05:19.960 ask me to repeat myself and and I'm not
00:05:21.800 going to I refuse to answer any
00:05:22.960 questions about the lecture uh at the
00:05:24.800 end of class so don't line up and say
00:05:26.160 you know what did you say on lecture you
00:05:27.280 know Slide Five said this what do you
00:05:28.479 mean right interrupt me as a go along
00:05:30.120 because if you have a question somebody
00:05:31.560 else also probably has the same question
00:05:33.479 uh and so we want to cover these things
00:05:35.919 okay all right databases the second most
00:05:38.919 important thing in my life um can
00:05:41.000 anybody give me an example of a
00:05:47.720 database yes click house he says click
00:05:50.440 house anybody
00:05:52.919 else aary you said a dictionary yeah
00:05:56.600 yeah that's pretty good what else
00:06:02.680 nobody can can nobody can my database
00:06:04.319 the contact manager on your phone
00:06:05.919 contact manager phone good excellent one
00:06:08.199 more IM say what IMDb IMDb good
00:06:11.800 excellent all right so he said click
00:06:13.560 house he said dictionary said he said
00:06:14.880 contct manager he said I'm DB so click
00:06:17.680 housee is a database management system
00:06:20.039 the other examples are all databases and
00:06:22.319 and so what's tricky in in well the
00:06:26.000 common semantics of how people describe
00:06:27.440 databases is usually they meant the
00:06:28.759 database systems
00:06:30.160 which we'll focus on this class but I
00:06:31.759 want to First s discover discuss what a
00:06:33.720 database is and then how we're going to
00:06:35.400 build a databas man system to manage it
00:06:39.319 okay so database is going to be an
00:06:41.440 organized collection of data no surprise
00:06:44.720 there that are related to way in in in
00:06:47.840 some some Manner and it's meant to model
00:06:50.000 some aspect of the real world so he said
00:06:52.479 dictionary and what is the dictionary a
00:06:54.280 bunch of words and then their
00:06:55.919 definitions and maybe like the part of
00:06:57.720 speech or whatever right so that's
00:06:59.840 modeling sort of this you know the
00:07:01.440 vocabulary you said a contact manager
00:07:03.520 that's modeling someone keeping track of
00:07:05.240 of pencil on paper here's all my
00:07:06.720 contacts and their phone numbers and
00:07:07.759 email addresses right you're modeling
00:07:10.039 some aspect of the real world and you're
00:07:11.879 trying to capture all the constraints
00:07:13.599 and and aspects of that real word
00:07:16.440 concept in in your
00:07:18.879 database and again I'm highly biased
00:07:21.319 because all I care about is databases uh
00:07:23.520 but the database is going to be the core
00:07:25.199 concept among all Computer Applications
00:07:27.520 and almost all of computer science the
00:07:29.840 end day what is a computer doing some
00:07:31.720 input comes in you do something on data
00:07:33.759 you produce some output that's a
00:07:36.120 database that middle part most almost
00:07:38.360 always as a database what is a file
00:07:40.199 system file system is a database if you
00:07:42.240 use a website what are you doing you're
00:07:43.520 interacting some form that talks to a
00:07:45.440 database right what is an llm it's a
00:07:48.560 database more or
00:07:49.960 less right so this is be the most
00:07:52.400 important thing in in in computer
00:07:54.360 science again I'm biased but you're
00:07:56.120 going to encounter databases all
00:07:57.759 throughout your life and what this class
00:08:00.240 is going to teach you is to understand
00:08:02.960 what a database management system is
00:08:04.400 trying to do for you right why are
00:08:06.840 things going slow why is my query coming
00:08:08.599 back with with garbage right so if you
00:08:11.039 understand what the how the components
00:08:12.280 are implemented what they're doing
00:08:14.000 you're in a better position to to use a
00:08:16.599 database system to to to manage a
00:08:19.000 database so no matter where you go off
00:08:21.000 and become a you know database systems
00:08:22.400 internal developer like all the
00:08:23.919 companies that are coming in a few weeks
00:08:25.520 to talk to us or you go off and do
00:08:27.280 something else the end of the day you're
00:08:28.840 going to interact with databases because
00:08:30.159 that's what really life is all about
00:08:32.640 everyone's got a smartphone here right
00:08:35.159 all those applications are running SQL
00:08:36.799 light SQL light is a database management
00:08:38.240 system it's the most widely deployed one
00:08:39.919 right so we'll understand how sqlite is
00:08:41.399 actually implemented and in homework one
00:08:42.799 you you'll use
00:08:44.760 sqlite so let's use it let's discuss a
00:08:46.920 toy example and we can use that as to
00:08:48.760 explain you know the various parts of
00:08:50.160 the oral model and and database man
00:08:51.560 systems as we go along so assume we're
00:08:53.720 trying to build a a Spotify clone right
00:08:56.680 it's some kind a digital music store and
00:08:58.560 we want to keep track of the artists
00:09:00.519 that are putting out music and then the
00:09:02.640 albums that those artists release right
00:09:04.200 we want to know what you know for given
00:09:05.640 album what artist appears on those
00:09:08.640 albums so a really simple implementation
00:09:11.519 of the database could just be a bunch of
00:09:13.880 files on
00:09:15.440 disk right my example here I'm showing
00:09:17.839 them as csvs or comma separative values
00:09:20.240 but it could be Json the kids love yaml
00:09:22.519 you could do yaml it doesn't matter
00:09:24.399 right but we're going to have a separate
00:09:26.160 file per per per entity so I a file for
00:09:28.640 the artists and artists have a name the
00:09:30.920 year that they came out and maybe the
00:09:33.040 country that they're located in and then
00:09:35.040 we'll have albums with the name of the
00:09:36.519 the the the album the artist that
00:09:38.920 appears on the album and then the year
00:09:40.760 the album is
00:09:41.920 released right this is a database I
00:09:44.680 don't recommend doing it this way but
00:09:45.920 you could do it this way a bunch of
00:09:47.440 files on
00:09:48.440 disk so now anytime you want to update
00:09:51.680 or insert a new record we just could go
00:09:54.200 open the file you know pen to the end of
00:09:56.040 it or if you need to answer a query we
00:09:58.120 just scan through it untilt we find the
00:09:59.480 answer that we
00:10:00.519 want right so say want answer query like
00:10:02.760 what year did the jiz go go solo well I
00:10:05.720 could write some python code that just
00:10:07.480 opens the file up reads every line
00:10:09.920 parses the parses it as a CSV to get
00:10:13.079 back an array or or list of values I
00:10:16.320 know that I'm trying to look up the the
00:10:18.279 name jiza well the name is the first
00:10:20.680 field in my file so I just jump to the
00:10:22.920 the first element of the array check to
00:10:24.920 see whether that value equals jiza if it
00:10:27.320 does then I print it out
00:10:31.320 right this is the database system more
00:10:33.360 or less well this is interacting with
00:10:35.240 the database uh that I'm basically
00:10:38.399 embedding The Logical datas system
00:10:39.839 inside my application to do
00:10:41.639 this is this a good idea or a bad
00:10:46.600 idea I guess it says strawman at the top
00:10:48.760 so you know it's a bad idea so why is it
00:10:50.000 a bad
00:10:52.959 idea yes so we kind of need to look over
00:10:56.000 every entry so he says you kind of need
00:10:57.720 need to look over every entry yes
00:11:00.079 so my example here my file has three
00:11:02.160 lines okay who cares like that that'll
00:11:04.200 sit in L1 cache it'll be super fast but
00:11:07.120 always when you think about in computer
00:11:09.160 science especially in databases think
00:11:10.800 about what happens if you scale up to
00:11:12.079 really large numbers so what if my line
00:11:14.720 what if my file had a billion records do
00:11:17.240 I want to be scanning through and
00:11:18.360 parsing every single uh line just to
00:11:20.399 find the element I'm looking for one
00:11:21.600 entry
00:11:23.279 no what are some other
00:11:26.040 problems yes you have to rewrite the
00:11:28.920 code every time you want to change your
00:11:30.320 query excellent so he says you have to
00:11:31.600 rewrite the code every time you want to
00:11:32.760 change your
00:11:33.920 query worse than that what if I want to
00:11:36.120 add a new new field right now I gotta
00:11:39.440 change much of my code as well is
00:11:40.880 updating the file that
00:11:43.040 sucks maybe one more in the back
00:11:49.959 yes yes so he says what if you come
00:11:52.839 across a line that's reordered in a
00:11:54.079 different way right maybe like they SWA
00:11:56.560 the some someone some stupid somebody
00:11:58.680 stupid again these are just files on
00:12:00.399 disc they open up a text editor and flip
00:12:01.920 the order of these things and now my
00:12:03.440 python code is going to choke on it
00:12:05.839 right or even like what if I put instead
00:12:08.040 of the you know the year 1990 I put a
00:12:10.440 phone number in what happens
00:12:13.240 then right so there's a bunch of
00:12:15.000 problems doing this approach but this is
00:12:16.760 this is what the datab system is going
00:12:18.920 to prevent you from from encountering
00:12:20.760 these these issues because it'll manage
00:12:22.720 all these things for
00:12:24.120 you so there's some other issues we have
00:12:26.120 to deal with right so in my in my file I
00:12:30.120 just if if if a if an artist put puts
00:12:32.760 out multiple albums then in my my album
00:12:35.120 file I'm just repeating their name over
00:12:36.680 and over again wuen Clan wuang Clan wuen
00:12:38.760 Clan but how do I make sure that someone
00:12:40.360 doesn't like drop an n in the you know
00:12:43.519 the name of the wuen clan and now it's
00:12:45.000 Wang claw right well I know that they
00:12:48.160 should be the same thing but the data
00:12:49.440 says that they're
00:12:51.000 different we brought this up before what
00:12:53.000 have someone comes along and overwrites
00:12:54.680 the the album name with a weird string
00:12:57.160 puts email address in or puts in number
00:12:59.560 that shouldn't be
00:13:01.440 there and then we didn't talk about this
00:13:03.880 but in my toy example I assume that
00:13:06.560 there was one artist per
00:13:09.399 album but you know if it's if it's a
00:13:11.320 mixtape there's a lot of artists on that
00:13:13.560 and in my my simple example I couldn't
00:13:16.079 couldn't handle
00:13:18.199 that then what happens is what if I
00:13:20.279 delete an artist by accident or by
00:13:22.320 choice from the artist file but now I
00:13:24.720 got a bunch of albums that rep that are
00:13:27.839 you know that mention an artist that
00:13:29.519 doesn't exist in my my table or my my
00:13:31.760 file so I basically have a dangling
00:13:33.880 pointer
00:13:35.360 now we've talked about how on the
00:13:37.680 implementation side how do we find a
00:13:39.320 particular record well just iterating
00:13:41.880 over single file and parsing it one by
00:13:43.760 one that's terrible that's
00:13:45.839 slow what if you have another
00:13:47.519 application that wants to use the same
00:13:48.639 database well now I got to basically
00:13:50.720 copy and paste the code that I wrote to
00:13:52.600 parse that file and and get records out
00:13:54.759 and put it to my other application but
00:13:56.519 what if I wrote the first version of the
00:13:57.680 application in Python then I rewrote it
00:13:59.759 in Rust now I got to translate all the
00:14:02.000 python code to rust code that sucks but
00:14:05.639 then what also what if the file sorry
00:14:07.160 what if the the the other application is
00:14:08.480 running on a different machine or bunch
00:14:09.959 of cell phones now I got to make sure
00:14:11.839 that they all the application
00:14:13.560 implementations can access that file
00:14:15.160 some way to like a distribut a file
00:14:16.839 system which is the database by the
00:14:19.160 way and then what happens if we have two
00:14:21.199 threads try to write to the same file at
00:14:22.560 the same
00:14:23.360 time well we can do something really
00:14:25.600 really stupid and just let the OS lock
00:14:27.040 stuff for us lock the file and then
00:14:29.320 prevent only one only allow one thread
00:14:31.040 to write into it at a time but a
00:14:33.199 reoccurring theme you're going to see
00:14:34.279 throughout the semester is in the world
00:14:36.440 of databases the OS is our Frenemy we
00:14:39.399 never want to let it do anything for us
00:14:41.399 so letting the OS lock files for us is a
00:14:43.199 bad idea because we're database people
00:14:44.720 we can always do it better than they can
00:14:46.720 so only allowing one thread to write it
00:14:48.560 to the file at a time that is actually
00:14:50.759 what SQL light does but SQL light's
00:14:52.519 meant to run on cellphones you know
00:14:54.440 you're running a machine with you know
00:14:55.759 thousand cores you don't want to do that
00:14:58.399 and the OS
00:14:59.600 is always going to be more inefficient
00:15:01.959 anyway then lastly what happens if we're
00:15:04.279 modifying the the the
00:15:07.040 file and we going to write a new record
00:15:09.839 we write half of it and then it crashes
00:15:12.800 the the the machine crashes someone chps
00:15:14.399 over the power cord lightning strikes
00:15:15.600 the Transformer whatever now we come
00:15:17.920 back online what should be in our
00:15:20.560 file well if we just write to the file
00:15:22.720 we'll just see whatever we wrote before
00:15:24.000 to the crash but that's invalid right
00:15:26.040 now we have a record that's missing half
00:15:27.320 of it
00:15:29.959 and then what if we want to allow
00:15:30.839 multiple shees to access the the the
00:15:33.000 file or the database uh and we want to
00:15:35.720 make sure that and if any one of those
00:15:37.399 machines goes down we can keep running
00:15:38.800 and still you know serve queries serve
00:15:41.000 requests well now I got to basically
00:15:43.279 Implement a bunch of load balancing
00:15:44.480 stuff to to handle accessing the file
00:15:46.839 that
00:15:47.759 sucks so this is just a quick smattering
00:15:50.519 of the problems that we're going to have
00:15:52.240 to solve throughout the entire semester
00:15:53.720 to make it so people don't have to do
00:15:55.120 stupid things like relying on the
00:15:56.839 operating system or managing a stuff in
00:15:59.440 application
00:16:00.920 code right and this is what a database
00:16:02.959 management system is going to do for you
00:16:04.720 right it's going to be the software that
00:16:06.040 that allows applications to store
00:16:08.360 analyze query data uh in a database and
00:16:13.040 a general purpose database system will
00:16:14.600 be one that can support the any
00:16:16.440 arbitrary schema within reason of course
00:16:19.480 uh it can allow any arbitrary queries
00:16:21.319 meaning it's not hardcoded just to do
00:16:23.199 that one look up on the jiza you can
00:16:25.040 change the query to do any look up on
00:16:26.600 any artist or or any field or do any
00:16:29.040 kind of
00:16:30.560 transformation and it's going to do this
00:16:32.360 according to what we'll call a data
00:16:34.040 model it's a way a high level
00:16:35.440 representation of what is in a
00:16:39.079 database right and again just to push
00:16:42.759 this uh this this point home further
00:16:45.319 database systems are some of the most
00:16:46.720 widely deployed and widely tested and
00:16:48.560 vetted pieces of software in the world
00:16:50.680 that maybe Rivals you know maybe
00:16:52.440 operating system is the only one I could
00:16:53.839 think of maybe some ineda systems right
00:16:56.680 there's you know multi-billion dollar
00:16:58.240 corporations that are running off of
00:16:59.440 database systems that are tested and
00:17:01.040 sold by Major Enterprises there's a lot
00:17:02.759 of money involved in database both you
00:17:04.359 know building them and selling them 's a
00:17:06.280 lot of money riding on a datab system
00:17:08.520 operating
00:17:09.640 correctly and so at no point say again
00:17:13.079 if you go off in the real world and
00:17:14.480 you're do a startup or whatever at no
00:17:16.720 point you should you say to yourself oh
00:17:18.640 I'm just going to build my own you know
00:17:19.760 databas system in my application that's
00:17:21.880 a bad idea you're going to have problems
00:17:24.119 we going to rely on these existing uh
00:17:27.119 existing tools that are out there and
00:17:29.120 again this class is going to teach you
00:17:30.200 how to how to do
00:17:31.960 it all right so a data model is going to
00:17:34.360 be this high level abstraction that is
00:17:37.640 going to represent data in a database
00:17:40.240 again According to some to some scheme
00:17:42.840 we we'll see in a second and within for
00:17:47.280 most database systems support only one
00:17:49.559 data model like a relational database or
00:17:51.919 a document database the lines start to
00:17:54.080 get blurred more recently because in
00:17:56.280 relational databases you can store
00:17:57.480 documents you can store Json now and if
00:17:58.960 field and now the document databases all
00:18:01.720 support SQL and like relational like
00:18:03.400 things on top of Json so in some cases
00:18:06.520 it's clear that there there's a
00:18:07.480 distinction between the data models uh
00:18:09.840 but in the more more widely played
00:18:11.080 systems again the lines get
00:18:12.880 blurry and so given a data model your
00:18:16.200 database will be defined according to a
00:18:18.200 schema that just specifies I have these
00:18:21.159 tables or these collections of data they
00:18:23.159 have these attributes with this name and
00:18:25.159 this data type again we'll see this
00:18:26.880 throughout the entire semester but it's
00:18:28.360 a way to to specify the structure of the
00:18:31.400 things you want to store in your
00:18:32.919 database because without a schema it's
00:18:34.960 just a bunch of random bits and it
00:18:36.240 doesn't mean anything right the schema
00:18:38.880 is going allow you to to provide a
00:18:41.720 structure to to the data so that you can
00:18:44.559 write queries against it another way I
00:18:47.120 think about this save a bunch of log
00:18:48.240 files for my application server it's a
00:18:49.520 bunch of text lines right you know with
00:18:51.240 time stamps and so forth if I don't have
00:18:54.600 any structure on top of that I then
00:18:56.480 there's no way to sort of find the data
00:18:57.960 I'm looking for but if I say oh a log
00:19:00.159 file entry is going to have a timestamp
00:19:01.760 followed by maybe an event code followed
00:19:03.640 by a string that with the event well
00:19:05.600 that's a schema that's a structure that
00:19:07.200 I can then run queries on top of it
00:19:09.799 because otherwise again if it's just a
00:19:10.760 random bunch of blob random bunch of
00:19:13.200 bits the data is useless the data is
00:19:15.720 meaningless yes how this the data model
00:19:20.559 model also the data model is we'll see
00:19:23.120 this second a data model is the the
00:19:25.440 abstraction for how you
00:19:27.720 define collections of data and then and
00:19:30.960 then their relationships between other
00:19:33.640 collections the schema says okay within
00:19:36.400 that data model I have these collections
00:19:38.400 that have these attributes with these
00:19:39.840 these
00:19:40.720 types think of it like a it's almost
00:19:43.039 like a uh like a class versus object in
00:19:46.240 like Java world the class is the
00:19:47.799 definition of of the of like the the the
00:19:51.720 data model and then the instantiation
00:19:53.640 would be actually that's a bad
00:19:55.360 example um it would be like a I in the
00:19:59.799 programming language you specify like in
00:20:02.200 Java the Java you has a has a way to
00:20:05.080 define how you represent data and then
00:20:07.799 you you would create instances of it in
00:20:10.240 classes let's go further along I think
00:20:12.280 it's a b ex able to but
00:20:14.480 it I think it makes sense when you start
00:20:16.360 see uh when you start seeing
00:20:17.880 differentiations between it okay other
00:20:23.440 questions okay so I'm going to be highly
00:20:27.000 highly biased the entire semester I love
00:20:28.880 the relational data model I think it's
00:20:30.440 how every datab system should be
00:20:31.600 implemented because relational model can
00:20:33.280 be contorted at least in the modern
00:20:35.720 version of it into any possible data
00:20:37.520 model you would care about except for
00:20:38.600 one I'll talk about in a second so most
00:20:41.640 database systems we're to talk about
00:20:42.760 this semester and most database systems
00:20:44.559 that are in the real world that you've
00:20:45.679 heard of are very likely going to be
00:20:47.880 relational databases um but it's not to
00:20:50.600 say that's it's the only one out there
00:20:53.159 right there's these key value stores
00:20:54.360 that are out there things like rock DB
00:20:56.120 level DB um reddis sort of like this
00:20:59.799 where you sort of have a key and then a
00:21:01.200 value and that's it and there's no
00:21:02.440 meaning to the actual value except for
00:21:04.360 what the application puts upon it so
00:21:06.320 this is typically used for simple
00:21:07.640 applications or caching like you know
00:21:10.400 cookie ID to some
00:21:11.840 payload then you have this whole sort of
00:21:13.919 category what falls under the moniker no
00:21:15.760 SQL which is ironic now because now they
00:21:18.159 now they really mean at the beginning
00:21:20.000 when no SQL came out they were like oh
00:21:21.240 guys you know SQL sucks we're not doing
00:21:23.080 any SQL no SQL now they really mean now
00:21:25.320 they say oh no SQL really means not only
00:21:27.200 SQL right because they've seen the light
00:21:29.400 and basically become relational
00:21:31.240 databases um so the the document stuff
00:21:34.720 the Json databases probably the ones
00:21:36.360 that are you've heard about the most
00:21:37.840 like mongodb would would be a document
00:21:41.080 database uh wide column or column family
00:21:43.919 is a subset of of document Json
00:21:46.360 databases it's like uh uh Google big
00:21:50.080 table was this uh Cassandra was
00:21:52.720 this then you have these uh array
00:21:56.080 databases so vectors matrices and
00:21:59.080 tensors uh tensors are probably the
00:22:02.400 thing you don't want to store in inter
00:22:03.679 relational database because it's since
00:22:05.919 it's like a multi-dimensional array it's
00:22:07.520 it's kind of weird to do that in a
00:22:08.600 relational model um even though the SQL
00:22:10.679 standard last year just added it
00:22:12.120 multidimensional
00:22:13.840 arrays and then there's these hod podge
00:22:16.120 of these ones at the end uh hierle
00:22:18.840 Network semantic ntid relationship I'll
00:22:20.840 talk about Network one a little bit from
00:22:22.360 kodil but these are like stuff from the
00:22:24.279 70s and 80s they were doing cocaine back
00:22:27.080 then they were experimenting but it
00:22:28.559 basically the world has come back to
00:22:30.000 realize that the relational model is the
00:22:31.159 right way to go every 10 years though
00:22:33.360 there's always this repeat where someone
00:22:34.679 says oh relational model stupid SQL
00:22:36.200 stupid we're GNA have a new data model
00:22:38.600 and then everyone gets all excited about
00:22:39.840 that on Hacker News and then they
00:22:40.960 eventually come around say oh yeah
00:22:41.880 relational model is is the right idea so
00:22:44.679 we're right now we're in the phase where
00:22:46.480 all these guys have said oh yeah SQL is
00:22:48.320 actually a good idea and then the next
00:22:50.080 step is going to be the vector databases
00:22:51.640 come back and say SQL is a good idea uh
00:22:53.640 but we'll get there all right so again
00:22:56.159 this course is going to be about
00:22:57.320 relational databases but it's not to say
00:22:58.799 that the things we're talking about
00:22:59.840 can't be applied to the other data
00:23:01.520 models it's just you know most of the
00:23:04.720 systems you encounter are going to be
00:23:07.240 relational all right so why is
00:23:08.960 relational model matter matter and why
00:23:10.559 do I why am I so keen on it well if you
00:23:12.960 go back to like the 60s and early early
00:23:15.559 70s the there wasn't this sort of
00:23:18.360 plethora of database systems that we
00:23:19.640 have now uh there was a small number of
00:23:21.840 them and it was very difficult to build
00:23:24.440 database applications like think of like
00:23:26.279 Mainframe days um and so in the early
00:23:29.480 days the one the first dat systems that
00:23:30.919 was built thing called IDs for
00:23:33.080 integrated data store uh that was
00:23:35.080 actually built by GE in
00:23:37.799 1965 or 66 IMS was a hierle database
00:23:41.799 built by IBM to manage the Apollo moon
00:23:43.760 mission the keeping track of all the
00:23:45.120 parts to build the the the the rocket
00:23:47.200 going up and then part of this IDs work
00:23:50.279 there was this thing called kodil which
00:23:51.960 came out of the cball world I was
00:23:53.880 basically trying to Define what the API
00:23:55.640 is how you would interact with with the
00:23:57.240 database and and so back in the day in
00:24:00.360 the 60s and 70s computers were very very
00:24:02.799 expensive and humans were relatively
00:24:04.919 cheap the labor of humans were
00:24:07.159 relatively cheap to uh computers so it
00:24:10.480 wasn't that big of a deal that people
00:24:11.679 had to spend a lot of time rewriting
00:24:12.960 their code as he brought up every time
00:24:14.400 you to change make a change to your
00:24:15.440 database right if you use these other uh
00:24:18.159 other data models and that's because
00:24:20.279 there was a tight coupling between at
00:24:22.159 The Logical level how you're defining
00:24:23.679 your database and then how the data
00:24:25.360 system actually physically represented
00:24:26.799 it so now in your application code you
00:24:28.640 had to be aware of how the D was laid
00:24:31.320 out in the bits on disk and how things
00:24:33.919 were connected with pointers and you had
00:24:35.640 to basically Traverse those those data
00:24:37.279 structures manually in your code right
00:24:40.360 so that meant that anytime there was a
00:24:41.679 change in your database schema you have
00:24:43.640 to go back and rewrite all your
00:24:44.720 application code to account for that so
00:24:47.080 an example would be in IMS least the
00:24:50.039 early days you would you would Define a
00:24:52.000 table and then you would tell the they I
00:24:53.720 want to start it either either as a hash
00:24:55.159 table or a B tree and then say if you
00:24:57.720 made a mistake said oh I really want to
00:24:59.000 store you know I decided to do a hash
00:25:00.880 table but I really need to do range
00:25:02.559 scans and you can't do range scans on a
00:25:03.919 hash table and I want to switch it to a
00:25:05.360 b tree well I got to dump the data out
00:25:07.840 then load it back in as a b tree then
00:25:10.120 rewrite all my application code because
00:25:11.799 now the API to that table has changed
00:25:13.480 because it went from a hash table to a b
00:25:14.679 Tre so there was this guy at IBM uh who
00:25:18.799 basically saw all these programmers
00:25:20.679 doing the same thing over again making
00:25:22.120 all these these mundane changes to their
00:25:24.720 Davis applications every single time
00:25:26.520 there was a change and there's always
00:25:28.360 going to be changes in databases right
00:25:29.679 because as the world evolves or the the
00:25:31.840 data you're capturing evolves you want
00:25:33.600 to you know evolve your
00:25:36.520 database so there's this guy named Ted
00:25:38.640 Cod who was originally a mathematician
00:25:40.880 he did his PhD in mathematics um he
00:25:43.240 joins IBM research in in New York and as
00:25:46.240 I said he was seeing all these
00:25:47.480 programmers doing the same thing over
00:25:48.919 and over again is rewriting their
00:25:50.159 applications every single time the the
00:25:53.120 the layout or schema changed and he
00:25:55.440 obviously thought that there has to be a
00:25:56.480 better way to do this and so he devised
00:25:59.120 the relational model in 1969 as a sort
00:26:02.600 of abstraction uh to a database based on
00:26:06.640 sets or sorry based on relations which
00:26:09.240 I'll explain that in a second and that
00:26:11.440 there would be this logical connection
00:26:12.880 between data through values rather than
00:26:15.360 physical connections like pointers and
00:26:17.240 offsets and things on disk as you would
00:26:19.000 have to do in in the other data
00:26:21.640 models so the first paper that defined
00:26:24.039 the relational model came out in 1969 I
00:26:26.520 think this was an internal tech report
00:26:27.960 at uh at IBM but the one that's really
00:26:31.200 really famous that everyone refers to is
00:26:33.120 is this one here that came out in the
00:26:34.679 cacm in uh in 1970 so if you say what's
00:26:38.279 the first paper relational model people
00:26:39.960 typically point to this other one here
00:26:42.320 and so when this came out all the
00:26:44.120 academics thought this was the greatest
00:26:45.399 thing ever this is clearly how we should
00:26:46.720 be building database systems but IBM poo
00:26:50.600 pooed it or ignored it right because
00:26:53.240 they were making so much money on IMS
00:26:55.200 which is the high Echo database system
00:26:56.840 and then one of their own employees
00:26:58.039 comes along and say hey the thing you're
00:26:59.559 making a lot of money on is actually
00:27:01.240 stupid you don't want to do this way you
00:27:02.240 want to do this other way for this
00:27:03.279 system that I I don't hasn't actually
00:27:04.840 been implemented but here's the better
00:27:06.600 way to to represent databases again he
00:27:09.120 was a mathematician he didn't he he
00:27:11.080 wasn't building a system at the time and
00:27:12.720 actually in this first paper here it's
00:27:13.880 all mathematics there is no there is no
00:27:16.200 SQL at this time he didn't find a
00:27:17.880 programming language it's all through
00:27:19.559 relational algebra and how you
00:27:21.240 manipulate databases so from IBM's
00:27:23.960 perspective they were like well we can't
00:27:25.200 do anything with this it's just a paper
00:27:27.399 right
00:27:29.240 so but eventually IBM did do this did
00:27:31.480 take the paper uh but not in New York
00:27:33.679 act AC San Jose they got a team together
00:27:36.000 which will cover throughout the semester
00:27:37.640 and actually build one of the first
00:27:38.520 relational
00:27:39.399 databases as a prototype based on Ted
00:27:41.559 cod's
00:27:43.399 paper
00:27:45.159 so I mentioned kodil Kil was a highle
00:27:48.240 database that was that was spearheaded
00:27:50.080 by this the the guy that building IDs or
00:27:52.720 I'm um a GE um and so there's a sort of
00:27:56.360 back and forth between the relational
00:27:57.640 guys
00:27:58.760 uh the people that like in Academia like
00:28:00.720 relational datas is the right way to go
00:28:02.240 and then all the cell people all the
00:28:03.440 Cobalt people said no no no cell is the
00:28:04.919 way the right way to go and so actually
00:28:07.519 who has ever heard of cotol
00:28:09.799 ktool no one right because it's dead
00:28:12.240 right uh so codale was based on these
00:28:15.399 like sets so you would have you would
00:28:17.039 Define like these collections as if
00:28:18.279 tables and you would Define the
00:28:19.799 relationships between them through these
00:28:21.919 sets and you would and you would
00:28:23.159 basically iterate over every element
00:28:25.600 each set and follow pointers to go find
00:28:27.360 the data that that you're looking for
00:28:29.480 and so there was this uh famous Workshop
00:28:31.960 in 1974 at at in Michigan where they got
00:28:35.600 all the people from the codale camp and
00:28:37.360 all people from relational database Camp
00:28:38.760 put them in a single room and they they
00:28:40.640 fought over it so this is a very very
00:28:42.720 famous meeting uh obviously Ted cob was
00:28:45.240 there but there's been four four touring
00:28:47.679 Awards in databases and all four of
00:28:50.120 those people were there so we're going
00:28:51.840 to cover a bunch of these guys uh
00:28:53.000 throughout the semester uh Bachman was
00:28:55.000 the the kotto sale guy He's dead Jim
00:28:57.519 Gray and Ed two- phase locking we'll
00:28:58.960 have a whole lecture on that he's dead
00:29:01.080 and then Stonebreaker uh invented
00:29:02.840 Ingress and postgress and a bunch of
00:29:04.279 other stuff uh that you may have heard
00:29:05.840 of before uh he's still alive um he's 80
00:29:10.320 turns 81 this year so he was my pH
00:29:12.799 adviser he's brilliant um but basically
00:29:16.039 the the all the Koto guys were saying
00:29:18.039 hey this relational model stuff you
00:29:19.600 can't actually build a real system doing
00:29:21.080 this right uh people aren't going to
00:29:23.600 understand what it means to have
00:29:24.399 relations and tables and then
00:29:26.360 furthermore you if you're going to be
00:29:28.080 programming at a high level language
00:29:29.720 again SQL uh the guys that been to SQL
00:29:32.519 were were actually at this conference
00:29:33.559 too um but at the time SEL was you know
00:29:36.440 very early like you're never going be
00:29:38.080 able to to take SQL and compile it to a
00:29:40.320 program that can run efficiently right
00:29:43.080 so they all complained the cot cell guy
00:29:44.799 said that that relational database is a
00:29:46.600 bad idea but then the relational guy
00:29:48.679 says they all say that this this cotell
00:29:51.080 thing these these sets and you have to
00:29:52.480 walk through these records and deal with
00:29:54.120 the physical data structure that's all a
00:29:55.720 bad idea too like it's makes the makes
00:29:58.120 the application brittle makes the
00:29:59.480 application more likely to break when
00:30:01.000 one part of your you know your of the
00:30:03.120 database breaks it breaks all the other
00:30:04.480 stuff because it relies on the physical
00:30:05.919 Integrity of of data right and as I said
00:30:09.000 nobody here has ever heard of Cil the
00:30:10.840 relational Camp one but again as I was
00:30:13.679 saying every 10 years people forget all
00:30:15.480 the things we've learned before and now
00:30:17.159 the graph database guys are basically
00:30:18.399 making the same claims now as the Coto
00:30:20.080 people did in the
00:30:22.279 70s all right so what is the relational
00:30:25.320 model so it's a data model that that's
00:30:27.640 going to find a abstraction for a
00:30:30.640 database based on relations to avoid the
00:30:33.960 cost of having to maintain the the the
00:30:37.559 implicit knowledge of what the data
00:30:38.919 looks like physically in your
00:30:40.360 application code so there's three key
00:30:43.039 ideas in the the relational model first
00:30:45.720 is that we're going to store our
00:30:47.159 database in as simple data structures
00:30:50.240 I.E relations or tables and that we
00:30:52.600 don't expose that information to the
00:30:54.880 application code right you get this
00:30:57.080 abstraction just I tables and I can
00:30:58.679 interact with
00:30:59.639 them the physical storage the way
00:31:02.320 actually datab system is going to going
00:31:03.440 to actually write down the bits of your
00:31:06.200 of your tables is left up to the
00:31:08.679 implementation so the idea here is that
00:31:11.279 say I have a database I use a datab
00:31:13.120 system I have my database I store A
00:31:14.320 datab system that stores things on disk
00:31:16.279 but may maybe I want to store things in
00:31:18.559 you know uh in memory in in memory
00:31:20.159 database well if I just Define things
00:31:22.440 through through relations and interact
00:31:23.960 it through SQL in theory I could take my
00:31:26.639 database out of the disc database and
00:31:28.440 put it into the in memory database where
00:31:30.399 some new some new storage device comes
00:31:32.080 along I just plop it in that one and now
00:31:34.399 I don't have to change any of my
00:31:35.279 application code even though the
00:31:36.480 physical layout of the bits has changed
00:31:39.159 now I say in in theory this should work
00:31:41.559 as we see next class the there is a SQL
00:31:44.360 standard nobody follows it exactly uh
00:31:47.919 the only sort of defacto SQL standard we
00:31:49.519 have now would be postgress because
00:31:51.159 everyone can take the post parser and
00:31:52.519 reuse that but we'll see many cases
00:31:55.840 where if just because I have you know
00:31:57.880 two relational databases doesn't mean
00:31:59.120 they're always going to be compatible so
00:32:01.159 again I say in theory you should be able
00:32:02.480 to do this but not
00:32:04.159 always and then at the last one again is
00:32:06.639 that instead of writing procedural code
00:32:08.880 like a lowlevel for Loops to iterator
00:32:11.480 single uh you know one record at a time
00:32:13.320 as I showed my toy example before we're
00:32:15.720 going to write queries in some kind of
00:32:17.919 high level
00:32:19.080 language uh and the spoiler is going to
00:32:21.360 be SQL but we have to do relation
00:32:22.600 algebra first before we get there and
00:32:24.440 then that way we just say here's the
00:32:25.840 answer that I want and it's up to
00:32:27.960 databas system to figure out what's the
00:32:29.639 most efficient way to to implement it to
00:32:31.720 execute
00:32:32.720 it right so my example before where I
00:32:34.960 said I was parsing that file to try to
00:32:36.440 find one record and in said what if I
00:32:38.039 have a billion records uh then that
00:32:40.679 would really be slow but if I wrote it
00:32:41.919 as a SQL query and say I had a billion
00:32:44.279 records and things went slow well then I
00:32:45.840 can go back and add an index so I can
00:32:48.039 jump to the exact record that I want
00:32:50.159 think of like a glossery in a text book
00:32:52.000 I can jump to the page I want for for
00:32:53.320 some keyword and then now I don't again
00:32:55.760 I don't to rewrite my application code
00:32:57.159 because I have an index index because
00:32:59.200 I've extracted away the the actual the
00:33:01.840 implementation of both the data and the
00:33:04.000 query
00:33:07.039 plan so we'll see as we go throughout
00:33:09.480 the semester again in back in the 70s
00:33:11.080 people were making the same arguments uh
00:33:13.519 when C came along the C programming
00:33:15.159 language that oh you know there's never
00:33:16.760 going to be a compiler that can generate
00:33:18.360 assembly uh for C code as well as a
00:33:20.840 human can write of course now we know
00:33:22.760 that's crazy right compilers are very
00:33:24.000 very efficient same thing was said about
00:33:25.919 SQL back in the day from the codell guys
00:33:28.440 that no no computer program is going to
00:33:30.159 be able to generate a query plan for a
00:33:32.399 SQL query that's as efficient as what a
00:33:34.559 human could write
00:33:36.279 themselves uh and of course again nobody
00:33:38.639 writes SQL by hand anymore or at least
00:33:40.320 sorry nobody writes the query Plans by
00:33:41.519 hand let let the D system do it for
00:33:43.960 you all right so there's going to be
00:33:46.159 sort of three comp three components of
00:33:47.720 the relational model there's going to be
00:33:49.320 the structure of of the database again
00:33:51.480 that's going to the definition of of the
00:33:53.000 tables we have you can use the term
00:33:55.639 tables and relations interchangeably but
00:33:57.799 to be pedantic you would say relations
00:33:59.159 not tables right you define the what's
00:34:01.880 going to be in your relations and then
00:34:04.080 their contents and you define this
00:34:06.080 independent of their physical
00:34:07.359 representation and we we'll cover that a
00:34:09.399 bit further next slide and then you can
00:34:11.520 also Define what we'll call sort of
00:34:12.918 Integrity constraints and these are
00:34:14.520 going to be definitions of what the data
00:34:16.520 is allowed to look like in accordance to
00:34:19.280 whatever you're trying to model in the
00:34:20.440 real
00:34:21.359 world right so if you store someone's
00:34:24.320 age in a database we know no one no no
00:34:26.399 one can be negative right there's nobody
00:34:28.480 that's negative 10 years old so we can
00:34:30.119 put a constraint in our in our table say
00:34:32.560 this value of this age can never be less
00:34:34.599 than
00:34:35.960 zero and the last one is going to be the
00:34:37.918 manipulation mechanism and this is
00:34:39.280 basically the the API the programming
00:34:41.000 interface that that is exposed to us to
00:34:43.560 allow us to access and modify the
00:34:45.639 contents in our in in our database and
00:34:47.800 this is what relational algebra will
00:34:49.839 this is what relational algebra will be
00:34:51.399 that we'll see in a second but I'm going
00:34:53.800 to cover this Independence thing first a
00:34:55.000 little bit more because this is it seems
00:34:57.000 obvious now but again in the 1970s this
00:34:58.800 was considered you know
00:35:01.079 groundbreaking but the idea of data
00:35:02.839 independ is that again we don't want
00:35:05.320 to uh have to expose necessarily the
00:35:08.800 physical layout of data on whatever
00:35:12.400 storage device we're storing it on uh to
00:35:14.920 the application so they can program
00:35:16.680 against it using a high level
00:35:18.760 extraction right so at the lowest level
00:35:20.760 there's database storage I'm not
00:35:22.520 defining what that is because it could
00:35:23.839 be in memory it could be an SSD it could
00:35:25.640 be an object store like S3 again for our
00:35:28.320 purposes here it doesn't matter and then
00:35:30.800 you define a physical schema of of
00:35:34.960 basically how to represent the the
00:35:37.160 database you're trying to store in that
00:35:39.359 that database storage device so this
00:35:41.680 would be defining the pages the layouts
00:35:43.480 of the pages like where how the bits are
00:35:45.000 actually laid out in a single page where
00:35:46.640 the files are how the files are
00:35:48.079 organized is your database one file
00:35:50.079 multiple file multiple directories all
00:35:52.319 right what do your extents look like are
00:35:53.520 you packing multiple you know files in a
00:35:55.000 single or sorry multiple pages in a
00:35:56.200 single St or is a single St for part
00:35:57.680 table all that is is handled at the
00:36:00.079 physical schema level and then above
00:36:02.560 that you have the logical schema which
00:36:04.280 is how the application is going to
00:36:05.520 Define what's in my my database I have
00:36:08.800 these tables I have these columns I have
00:36:10.880 these constraints on them typically you
00:36:12.640 would do this through through sqle like
00:36:14.000 a a crate crate table
00:36:16.920 command then I have a further
00:36:18.680 abstraction on top of that called an
00:36:19.960 external schema and this is where I can
00:36:22.839 Define sort of virtual tables on top of
00:36:25.119 my existing tables these are called
00:36:27.079 views
00:36:28.280 again we'll cover this uh throughout the
00:36:29.640 semester but the idea here is that say I
00:36:31.680 have some table of student records and I
00:36:35.400 want to expose to different applications
00:36:37.960 uh portions of what's in that table so
00:36:40.040 say like ACC accounting needs to know
00:36:41.680 your social security number but they
00:36:43.560 don't need to know your your grades say
00:36:45.839 it's all on a single table so I can
00:36:47.520 create a view that says this application
00:36:49.720 can see the table with with these
00:36:51.040 columns and this application can see the
00:36:52.680 table of these other columns even though
00:36:54.440 physically it's the same table it's just
00:36:56.319 exposed to you in a different uh
00:36:58.079 different
00:36:59.000 way and above that very top this is the
00:37:01.440 application code right this is the
00:37:02.800 python code JavaScript whatever doesn't
00:37:04.599 matter that's going to interact with
00:37:06.680 with our our
00:37:08.280 database So Physical Independence would
00:37:10.520 be this part here where I could Define
00:37:12.839 my tables uh and and their contents but
00:37:16.079 I don't care about how they're actually
00:37:17.680 being physically stored and I have a
00:37:20.160 further level of logical Independence
00:37:22.240 where I could say I have these logical
00:37:23.920 tables but then I could sort of
00:37:26.319 recompose them in different ways
00:37:28.040 for different applications or different
00:37:29.599 users and they don't need to know how
00:37:31.920 things are actually being stored at The
00:37:33.640 Logical level right below
00:37:35.520 it so this physical data Independence
00:37:38.680 this was this was a big deal because Cod
00:37:40.440 of sale couldn't do this in your
00:37:42.000 application code you had to know how to
00:37:43.240 follow the pointers of the data
00:37:44.880 structures that the data system was
00:37:46.920 storing for you relational model says
00:37:49.200 there is no notional pointers right even
00:37:51.560 though we're going to use pointers to
00:37:52.960 implement our system but we don't expose
00:37:55.079 that to to the application code
00:37:58.160 again it's one of those things where it
00:37:59.119 seems obvious now when you hear it but
00:38:01.319 back in the day back in the day this was
00:38:02.680 this was
00:38:04.920 groundbreaking all right so let's go a
00:38:06.560 bit more now what you know what
00:38:08.520 relations look like so as I said I'm
00:38:11.680 going to could use the term relation
00:38:13.280 interchangeably with table but to be uh
00:38:15.880 sort of again pedantic to the relational
00:38:17.560 model we'll call them relations so a
00:38:19.960 relation going to be an unordered set of
00:38:21.960 of data that contains a relationship of
00:38:24.480 attributes uh that represent some in the
00:38:28.160 world right so again going back to the
00:38:30.280 artist table a one record or one entity
00:38:33.839 would be an artist that exists like the
00:38:35.800 wuang clan and we would have all the
00:38:38.200 attributes that represent the
00:38:39.359 information or the metadata or sorry not
00:38:41.560 the metadata the attributes of the of
00:38:44.000 that entity together within within a
00:38:48.079 record and a record we're going to call
00:38:50.079 Tuple again think of I want use the term
00:38:52.640 row because a row mean applies to a row
00:38:54.160 store we'll see column stores later on
00:38:56.240 but a tuple is is going to represent
00:38:57.839 some entity or instance of an entity
00:38:59.920 within my
00:39:01.079 relation and so the original relational
00:39:03.280 model had to Define that the all the the
00:39:05.520 attributes you would have in your uh in
00:39:08.480 in in in your relation had to be Atomic
00:39:10.800 or scalar you couldn't have lists you
00:39:13.280 couldn't have like nested documents like
00:39:14.599 Json that has s OB since obviously been
00:39:17.079 relaxed in the SQL standard and most
00:39:19.000 Data Systems Support these things but
00:39:20.599 back in the 70s you couldn't do
00:39:22.960 this we'll also have a special value of
00:39:25.599 null uh if it's because we can Define
00:39:28.319 that things can't be null in in our in
00:39:30.160 our relations but this is just a way to
00:39:32.119 say that the value of something uh is
00:39:34.880 unknown for a given
00:39:37.160 attribute so you would say
00:39:39.760 a again to be sort of be pedantically
00:39:42.480 correct you would say a Nary relation
00:39:44.280 meaning a relation with n attributes
00:39:46.240 that's more or less equivalent to a
00:39:47.359 table with n columns right and similar
00:39:51.359 to if you say oh I'm using what database
00:39:53.240 are using I'm using my SQL or postgress
00:39:54.960 people know what you mean so if you say
00:39:56.160 table with these columns know what you
00:39:59.520 mean so a core concept of of relation
00:40:02.280 model is this is this idea of having a
00:40:04.319 primary key and a primary key is going
00:40:07.160 to be some some set of
00:40:09.680 attributes that uniquely represent one
00:40:13.280 entity within our within our
00:40:17.040 relation right so say you know for
00:40:19.960 Simplicity we' have like we could say
00:40:21.760 that there's no no artist can have the
00:40:23.920 same name so we could say that's our
00:40:25.280 primary key of course we know that
00:40:26.960 doesn't you know that's not correct in
00:40:28.440 the real world but for our purposes here
00:40:30.319 we can say oh yeah there's there's the
00:40:31.880 primary key is a name for for an artist
00:40:34.240 so given for a given name like a string
00:40:36.960 I can jump to one tubal that has that
00:40:39.760 information so you don't always have to
00:40:41.720 define a primary key uh most relational
00:40:44.480 dat will let you define tables without
00:40:45.880 it what we'll see later on is underneath
00:40:48.040 the covers if you don't Define a primary
00:40:49.520 key some SES will actually create one
00:40:51.119 for you and then even though you may
00:40:53.960 Define a primary key some systems May
00:40:56.440 ignore that
00:40:57.760 treat that as still like a unique
00:40:59.520 constraint like the value of the primary
00:41:01.200 key is still unique but underneath the
00:41:02.880 covers it maintains its own primary key
00:41:05.319 so sqlite does this sqlite has its own
00:41:07.480 incrementing incrementing value as the
00:41:09.000 primary key even though and treats
00:41:11.760 whatever you define as primary key as a
00:41:13.040 unique
00:41:14.480 attribute so going back here as I said
00:41:17.880 before we could use the name as the
00:41:19.400 primary key but that's that's bad
00:41:20.880 because obviously artists could have the
00:41:22.000 same name so to get around this we could
00:41:24.760 rely on like a a synthetic ID
00:41:28.520 uh like like a number that could
00:41:30.839 represent you know that that given
00:41:32.760 attribute or sorry given tupal right and
00:41:35.400 they could just be incremented
00:41:36.720 monotonically 101 102 103 so the Seagle
00:41:39.520 standard allows you to Def find what are
00:41:40.560 called identity columns again think of
00:41:42.720 these like synthetic values that don't
00:41:44.440 really map to things in the real world
00:41:46.200 but it's going to allow us in our
00:41:47.119 application code to uniquely Define
00:41:49.200 where where that data is
00:41:50.560 located SQL standard calls it identity
00:41:53.240 post Oracle called these sequences and
00:41:55.599 as we'll see throughout the semester my
00:41:57.359 SQL for whatever reason does things
00:41:59.000 differently they call it an auto
00:42:00.359 increment
00:42:01.640 key right so it's it would be this
00:42:03.680 column
00:42:04.920 here so in addition of the primary Keys
00:42:07.240 we also have foreign keys and the
00:42:09.480 foreign keys are going to allow us to
00:42:10.680 map some some set of attributes from one
00:42:13.680 relation to another relation to Define
00:42:15.720 that those things are linked together
00:42:17.960 and again this is different what from
00:42:19.200 what codell did cotell would actually
00:42:20.760 have pointers from one one record to
00:42:23.680 another record that you would literally
00:42:25.119 follow either through through memory or
00:42:26.839 through dis dis access to go find the
00:42:29.200 things that it was connected
00:42:30.760 to but in the relational model instead
00:42:33.240 we're going to use
00:42:34.359 values to to represent those those
00:42:37.440 relationships so say before remember we
00:42:39.760 wanted to be able to keep track of all
00:42:41.800 the artists in our album but if the
00:42:45.480 album only has one artist well that's
00:42:47.119 fine because we just stored the single
00:42:48.880 value uh but what if I have a mixtape
00:42:51.240 again with multiple multiple artists on
00:42:52.960 it now again I said you can store arrays
00:42:56.000 uh in as attributes
00:42:57.680 ignore that for now and in in the sort
00:43:01.520 of in the true relational model form you
00:43:04.480 would actually have to store this as a
00:43:05.760 separate cross reference table that
00:43:08.040 keeps track of for given artist ID what
00:43:11.319 album do they appear on and so these
00:43:13.920 would be called the foreign Keys you
00:43:15.359 would have a foreign key from the artist
00:43:16.720 table the artist ID that points to the
00:43:18.920 record on the artist table and you have
00:43:20.520 an Alum ID that's a far key pointing to
00:43:22.839 uh the album
00:43:24.200 table and again it's up to the data
00:43:26.280 system to decide how to make this work
00:43:28.440 efficiently typically there's going to
00:43:30.200 be an index that says for a for this
00:43:33.079 record here given a look up on if I have
00:43:35.359 an album ID I have to have an index on
00:43:37.839 the on that ID in the other table so
00:43:40.520 when I go insert something into this
00:43:41.920 table and I need to quickly check does
00:43:43.440 this album ID actually exist I can do
00:43:46.040 quickly do that
00:43:47.200 lookup and these foreign keys are allow
00:43:49.359 us to handle constraints or other issues
00:43:50.800 where like if now I delete a artist and
00:43:53.880 I want to Cascade and remove all it all
00:43:56.119 their albums well I can follow this
00:43:58.119 table to go find all the albums that
00:43:59.559 they belong to and then go make sure I
00:44:01.240 delete things here or in some cases you
00:44:03.079 can prevent you from deleting things you
00:44:04.480 say I can't delete a record if I know I
00:44:06.200 have a forign key reference over
00:44:09.280 here basically the data system is is
00:44:11.480 preventing you from shooting yourself in
00:44:12.559 the foot and you may think oh I'm a c
00:44:15.119 student I'm not GNA make mistakes
00:44:16.480 everybody makes mistakes right and so
00:44:18.680 the DAT systm can prevent you from
00:44:20.240 causing a lot of
00:44:22.480 problems so I sort of mentioned this
00:44:24.400 with the foreign keys but the idea of
00:44:25.720 constraints these are way to define what
00:44:29.280 data is allowed to look like uh and that
00:44:32.160 could be either within a single
00:44:33.559 attribute uh or multiple attribute
00:44:35.680 within a uh within a tupal or what
00:44:39.280 values are allowed to look like across
00:44:40.839 multiple tupal within the with within a
00:44:44.040 table within a relation so we said oh
00:44:46.760 the the the artist ID has to be unique
00:44:48.599 because that's the primary key that's a
00:44:50.040 constraint right that's saying that
00:44:51.680 there's only one tool can have a given
00:44:53.319 artist ID and across the entire table
00:44:57.440 so the most common ones are going to be
00:44:59.160 unique keys and then the foreign key
00:45:00.880 references uh the SQL standard from 1992
00:45:04.440 has this idea of basically Global
00:45:06.319 asserts but I think maybe some systems
00:45:09.599 implement this but they're really used
00:45:10.880 because they're really slow because
00:45:12.119 think of like every single time I insert
00:45:13.839 into the table I got to run this other
00:45:15.400 query to see whether my my constraint
00:45:16.920 has been violated or
00:45:18.400 not so the most common you'll see them
00:45:20.839 is defined in the table itself right so
00:45:23.200 if I could say I have a name it's going
00:45:25.040 to be a barart that's a string string
00:45:26.640 type and then not null that not null
00:45:29.000 part is the constraint that says you
00:45:31.319 can't insert a record with it with a
00:45:32.720 null
00:45:33.760 name another one could be explicit check
00:45:36.599 down here you could say that the year
00:45:38.760 has to be greater than 1900 because you
00:45:41.280 know nobody can be born in 1800 it's not
00:45:43.359 correct but you know in the real world
00:45:45.160 but like that's the idea of how you
00:45:46.760 could apply different constraints like
00:45:48.760 that and I said you have you have these
00:45:50.839 Global asserts is a create assertion uh
00:45:53.000 command you basically put a SQL
00:45:54.720 statement in every single time you you
00:45:56.079 modify the table this thing runs but
00:45:58.680 again they're super slow again always
00:46:01.200 think big I have a billion records and I
00:46:03.520 got to scan to make sure some
00:46:04.640 constraints not violate across those
00:46:05.839 billion records every single update
00:46:07.800 update that table I got to run that
00:46:09.280 across a billion tub and that's
00:46:13.119 bad all right so then next thing is the
00:46:15.240 DML and this basically the way we're
00:46:17.400 going to manipulate interact with the
00:46:19.720 the database through the relational
00:46:21.000 model and there's sort of two categories
00:46:23.440 of uh of you know the DML you could have
00:46:26.440 a programing language which you could
00:46:27.280 have for in a database the first is
00:46:29.520 going to be procedural but this is
00:46:31.359 basically defining the exact steps you
00:46:33.319 want the data system to execute in order
00:46:35.280 to run your query and the other one
00:46:37.359 would be non-procedural or declarative
00:46:39.280 where this is you're specifying the
00:46:40.720 answer you want that the data to compute
00:46:43.280 for you you don't Define how you should
00:46:45.839 you want to compute it uh you say but
00:46:48.040 this is just what I
00:46:49.359 want so for this class here this today's
00:46:52.040 lecture we're going to focus on this one
00:46:53.640 because this is be relational algebra
00:46:55.440 and as I said no datab expose a
00:46:57.440 relational algebra interface to you
00:46:59.040 because it's just it's too cumbersome to
00:47:00.800 write it uh and again you're basically
00:47:03.640 defining what the the query plan should
00:47:05.880 be most systems will will support this a
00:47:09.079 declarative language and this will be
00:47:10.680 based on what we call relational
00:47:12.640 calculus uh for this class you don't
00:47:14.520 need to know relational calculus but
00:47:16.079 it's a higher higher level form of
00:47:17.960 defining uh you know operations over the
00:47:20.680 relational model so if you take the
00:47:23.000 advanced class or we might do the
00:47:24.200 special topics class in the in the
00:47:25.640 spring semester on query optimizers the
00:47:28.240 relational calculus will come up
00:47:30.359 sparingly uh but for for our purposes
00:47:32.839 here today in this semester we only need
00:47:34.400 to care about relational
00:47:35.680 algebra earlier inversions of this
00:47:37.800 course used to teach relational calculus
00:47:39.160 but
00:47:39.839 it's nobody uses that in the real world
00:47:42.000 unless you're burning query
00:47:44.880 Optimizer all right so relational
00:47:46.680 algebra is going to be Bas or it's going
00:47:48.359 to Define so the raal model is going to
00:47:49.760 Define uh seven Primitives and the idea
00:47:53.599 here is that we can use these to
00:47:55.440 construct any possible query you would
00:47:57.680 want to have on a relational database
00:47:59.960 now not entirely true right Ted CA Ral
00:48:02.839 paper in the 70s to find these these uh
00:48:05.640 these seven seven Primitives it's since
00:48:07.640 been expanded because you this doesn't
00:48:09.160 handle things like sorting or
00:48:10.680 aggregations or group eyes uh but I want
00:48:13.760 to cover the core uh the core Primitives
00:48:16.200 and then it's sort of trival to see how
00:48:17.839 you could extend that to do other things
00:48:19.319 that you you want to do in a real
00:48:21.599 system so we're going to be able to
00:48:23.599 chain these things together to compute
00:48:25.240 more complex queries but I'm going to go
00:48:26.920 them each each of them one by
00:48:29.000 one so the most basic operation you can
00:48:31.280 do is is a
00:48:33.000 select um and this is basically the
00:48:35.760 first order predicate logic to say
00:48:37.960 here's how to identify the tobs that I
00:48:39.520 want for a given relation and it could
00:48:42.319 be what I'll call the base relation like
00:48:44.079 whatever I defined in my my database I'm
00:48:46.280 going directly at at at those tables or
00:48:48.800 could be from the output of another
00:48:51.040 relational operator and that's feeding
00:48:53.160 into my to my select
00:48:54.920 operator and so basically you're going
00:48:56.920 to find predicates that uh be based on
00:49:00.319 Boolean logic to Define what tupes are
00:49:02.240 allowed to sat or what tupal satisfy the
00:49:05.520 the constraints you want on the data and
00:49:08.200 then any T that that does satisfy is
00:49:10.200 then emitted as output so say I have a
00:49:12.880 really simple table or relation with two
00:49:14.440 attributes a ID and B ID I can define a
00:49:18.480 uh do a select where the predicate is
00:49:20.480 where a ID equals A2 against the
00:49:23.000 relation R and that just matches any any
00:49:25.880 record where a a a ID equals
00:49:28.920 A2 right it's like the wear clause in a
00:49:32.000 select statement if you remember that
00:49:34.319 and you can combine these things
00:49:35.280 together conjunctions and disjunctions
00:49:36.799 so I can say find me all the the the two
00:49:39.359 BS from R where a ID equals 2 and b d is
00:49:43.000 greater than 102 and it produces that
00:49:45.520 relation as the
00:49:47.160 output right so for me the way I always
00:49:50.040 remember this is like the it's the the
00:49:52.480 lowercase Sigma symbol S for Sigma s for
00:49:56.160 select
00:49:58.319 easy nemonic to remember
00:50:00.520 that so in SQL which most going to be
00:50:03.319 writing it's just the wear Clause right
00:50:05.760 so select start from R and then my wear
00:50:07.920 Clause be the predicate for how I'm
00:50:09.040 filtering
00:50:10.359 tubes and that's equivalent to defining
00:50:12.599 the the select operator
00:50:15.160 here all right the next thing we do is
00:50:17.680 projection and this is where we're
00:50:19.680 defining what the output should look
00:50:21.760 like in terms of what attributes we care
00:50:24.440 about from our input that that we want
00:50:26.079 to produce as the output as well as how
00:50:28.480 to manipulate that those attributes in
00:50:30.960 any given way so again same same
00:50:34.160 relation on r with Aid and B ID I could
00:50:37.319 have a projection where I take whatever
00:50:40.799 the the input is from the from this
00:50:42.200 inter relation sorry in operator here so
00:50:44.680 here I'm doing a select or uh on Aid
00:50:48.119 equals A2 and then I take the output of
00:50:50.559 this inter select and now project it
00:50:52.520 where I take the bid value or B
00:50:54.920 attribute subtract 100 to it and then
00:50:57.440 also produce Aid as the output so not
00:51:00.200 only am I selecting what attributes I
00:51:02.000 want I can change the order of them I
00:51:03.760 can manipulate them I can do arithmetic
00:51:06.400 operations string functions whatever you
00:51:07.920 want right and you're just defining what
00:51:10.040 you want the output to look like from
00:51:11.599 any given input and that's equivalent to
00:51:14.640 the like the select operator the
00:51:16.440 projection Clause of a select operator
00:51:18.520 in in
00:51:20.200 SQL so far so
00:51:24.000 good so then now we we going to be able
00:51:26.119 to start com Bing relations together
00:51:28.880 because again the idea is that instead
00:51:30.480 of having this one giant relation with
00:51:32.079 everything possible attribute I could
00:51:33.599 have for whatever whatever is it
00:51:35.400 whatever it is I'm trying to model my
00:51:36.520 database I'm want to break it up into
00:51:38.440 relations and then combine them together
00:51:41.040 to to reconstruct the the original
00:51:43.119 form so I have the union operator which
00:51:45.839 basically just takes all the attributes
00:51:48.319 uh from one side and all the on the
00:51:50.760 other side and uh just s of mashes them
00:51:54.480 together into a single single relation
00:51:57.359 in this case here this this operator
00:51:58.960 only works if the uh if the the both
00:52:02.079 relations you're trying to Union have
00:52:03.920 the same the same attributes with the
00:52:06.400 same
00:52:08.119 types right because you're literally
00:52:09.960 taking concatenating you know taking R
00:52:12.720 putting S at the bottom of it and that's
00:52:14.040 the output so in SLE you can do this
00:52:16.640 with there's there is a unit operator uh
00:52:19.119 where you basically combine the the
00:52:20.760 values of two select statements and
00:52:22.119 again they have to have the same
00:52:22.920 attributes because you're just
00:52:23.599 concatenating the two bols combining
00:52:25.160 them into a single output
00:52:28.000 of course there's a union there's an
00:52:29.799 intersection right an intersection is
00:52:32.119 just taking the uh finding the where
00:52:36.280 sorry back
00:52:41.760 yes this question is if there's in for
00:52:45.280 Union if there's a two that exist in
00:52:47.200 both tables will will it reuse
00:52:50.880 them uh let me about this in the
00:52:53.640 original relational model no because
00:52:55.720 it's based on
00:52:57.400 in SQL the answer is
00:53:00.240 yes I other way around in in the Rel
00:53:04.640 model it'll remove duplicates in SQL it
00:53:07.799 will keep them so in SQL if you do a
00:53:10.520 union it keeps them you put Union all
00:53:13.599 then uh it removes them because by
00:53:16.599 default they want to be efficient
00:53:18.040 because it's extra work to find the
00:53:21.839 duplicates I'll say too the this is
00:53:24.040 unordered so even though I'm showing R
00:53:25.839 followed by S
00:53:27.079 this is going be a key thing we see
00:53:28.160 throughout uh throughout the semester is
00:53:31.400 the order of of of the relational model
00:53:33.799 and SQL is
00:53:35.079 undefined so it's okay for things to end
00:53:37.839 up being you maybe inserted into your
00:53:39.839 table and then when you read them back
00:53:41.400 they come back in a different order and
00:53:43.200 this is going to open up a lot of
00:53:44.240 opportunities for us to optimize things
00:53:45.480 in different ways because we don't have
00:53:46.720 to maintain that order now in some cases
00:53:49.040 we do want that order uh we have to put
00:53:51.119 constraints on top of that to do that
00:53:52.520 and some systems would always store data
00:53:54.400 in sorted order uh in some manner but
00:53:57.640 we'll see examples when we see you know
00:54:00.079 manipulating or updating the the the
00:54:02.400 database uh through transactions that if
00:54:05.160 we maybe running a background garbage
00:54:06.359 collector it could reorder things in any
00:54:08.359 way we want and we get back things in a
00:54:09.599 different order so if you care about
00:54:11.799 getting back things in the right order
00:54:13.119 you you define an order by clause in in
00:54:15.400 in SQL but again the original version of
00:54:17.400 relational model does not have
00:54:20.040 that so intersection is again finding
00:54:22.799 things that are that are in both in this
00:54:25.040 this case here I have to have again I
00:54:26.599 have to have the same attributes there's
00:54:28.200 only one uh Tuple that matches to both
00:54:30.319 them A3 and 103 and that produces the
00:54:33.160 output uh
00:54:37.359 below difference is finding all the
00:54:40.480 tupal that appear in the first relation
00:54:43.079 uh but not in the second relation right
00:54:46.000 again this is just sort of set theory
00:54:47.680 stuff here nothing nothing exotic right
00:54:50.040 so I can do this again in SQL using the
00:54:52.799 accept operator again here I have a my
00:54:56.359 prod my output A1 100 101 A2 102 because
00:54:59.400 those things don't exist in s but
00:55:01.640 because I have A3 103 also in s that
00:55:04.200 thing it's excluded as from my
00:55:09.160 output all right so this is again this
00:55:11.440 is basic set the uh but it still doesn't
00:55:15.640 it's not allowing us to to identify the
00:55:18.839 the relations that we would or the
00:55:20.040 relationship or the connections between
00:55:21.720 different relations that we would want
00:55:23.720 so to do that we want to do what are
00:55:25.480 called joins but before we get joins we
00:55:27.680 have to do a cartisian product because
00:55:28.880 that's the basis of how we're going to
00:55:30.079 do joins later on so cartisian product
00:55:33.400 yes the operations covered do the colums
00:55:37.039 have to be the same this question is for
00:55:39.000 these operations here do the columns
00:55:40.119 have to be the same yes joins we'll see
00:55:42.480 in a second they don't for Union
00:55:44.640 intersection and difference they have to
00:55:49.960 yes all right so the the I'm say the
00:55:54.680 easiest the the
00:55:56.760 a naive join would be the cartisian
00:55:58.640 product you're just taking all the tupal
00:56:00.480 that are one relation and all the tup in
00:56:02.720 the other relation and just finding all
00:56:04.039 combinations of them and producing the
00:56:05.440 output right so in this case here if I
00:56:07.640 do the cartisian product on RNs I get
00:56:10.440 all of these for every Aid sorry where
00:56:13.000 AID is is A1 and 101 I then generate all
00:56:16.480 of
00:56:17.440 the
00:56:19.200 sorry I generate all of the these guys
00:56:21.720 here just match them together and that's
00:56:23.240 these and then I go into the next tup on
00:56:24.559 this side and and get all the 18 102s
00:56:26.920 and then match them together that right
00:56:30.359 so you may think why is this a good idea
00:56:32.280 why would you ever actually want to do
00:56:33.359 this because you're generating a bunch
00:56:34.480 of data that actually doesn't actually
00:56:36.079 match with with with with what's in the
00:56:37.960 real world um this shows up when you do
00:56:40.720 experiments and experiment analysis and
00:56:42.440 as in testing because you want to get
00:56:43.440 all possible combinations of your inputs
00:56:45.640 you would do the cartisian product for
00:56:48.000 that but more importantly from a
00:56:49.839 theoretical perspective this is going to
00:56:51.119 be the the basis of how we're going to
00:56:52.720 do joins in the next operator because
00:56:55.440 what we're going to want to do is find
00:56:56.960 all the you know where the AIDS in R
00:57:00.039 matches the AIDS in s's because we know
00:57:01.960 they're going to be connected in some
00:57:03.280 way based on how we Define them in our
00:57:06.799 schema so you can do this in SQL there
00:57:08.920 is a explicit crossjoin operator or
00:57:11.760 keyword right so I can say select star
00:57:13.760 from R cross join with s and that gives
00:57:15.319 you the cartisian product or it's not
00:57:17.359 recommended in the standard but you can
00:57:19.079 just put you know the comma separated
00:57:22.039 list of the tables and this will produce
00:57:23.880 the cartisian product for you right
00:57:28.119 but joins the important thing that we
00:57:29.440 care about this is basically a getting
00:57:32.400 all finding all the matches from one
00:57:34.640 relation quing some value with the with
00:57:38.079 the given attributes in s and so unlike
00:57:42.160 in the intersection operator where the
00:57:43.680 the the schemas of the two relations
00:57:45.079 have to be the same joined doesn't have
00:57:47.520 to be so implicitly it's going to look
00:57:49.760 for the name of the column and find the
00:57:52.240 corresponding matching name in in the
00:57:53.640 yellow column when I do a joint so for
00:57:56.240 RNs
00:57:57.280 here when I do a join on RNs with a
00:57:59.799 joint operator I'll find where the
00:58:01.680 values of Aid and B ID are the
00:58:04.440 same and then value just sort of comes
00:58:06.760 along for the ride too because it was
00:58:08.240 part of the matching tupal right so you
00:58:12.160 again you sort of think of this as like
00:58:15.160 uh you sort of sort of mashing the the
00:58:17.760 two tupal
00:58:19.160 together then checking to see where
00:58:21.119 things match like r r a ID for R has to
00:58:24.200 match a aid for S and the the B ID for R
00:58:26.920 has to match the B ID for S and then you
00:58:29.119 just you throw away the duplicate
00:58:32.039 attributes right and then that's your
00:58:35.319 output joins are going to see this we
00:58:37.480 have spend a whole lecture on this joins
00:58:39.440 going to be where where Data Systems are
00:58:40.920 going to spend most of their time in in
00:58:43.119 running queries so this is the thing
00:58:45.039 we're going to try to optimize the most
00:58:46.079 to make them run the
00:58:47.680 fastest there's a lot of different ways
00:58:49.599 to Define joints a lot of different
00:58:50.920 types of joins we we'll see more in next
00:58:52.839 class um and so my example here where
00:58:55.599 I'm sort of
00:58:56.760 implicitly joining based on the the
00:58:58.359 having the values be the same or sorry
00:59:00.039 the names of the attributes be the same
00:59:01.960 that's called a natural join so there's
00:59:03.760 a natural join keyword that's basically
00:59:05.200 going to look up the names and see of
00:59:06.920 columns see whether they match and then
00:59:08.079 do a join against them I don't recommend
00:59:10.440 doing this because again it's plicitly
00:59:12.319 storing the uh implicitly figuring out
00:59:15.119 what the joint should be based on um and
00:59:17.520 you actually want to actually Define how
00:59:18.839 you want to do your join so you can
00:59:20.640 either do this with a join clause for
00:59:22.599 RNs and there's a using uh keyword you
00:59:24.880 say what what you're doing look your
00:59:26.240 look up on or you can do the on Clause
00:59:28.760 where explicit to say like Aid has to
00:59:30.960 for R has to equal to aid for S and the
00:59:33.280 bid for R has to equal to B ID for
00:59:35.760 S right so the bottom one is probably if
00:59:39.000 you're writing by hand is probably what
00:59:40.160 you're going to be doing um this has a
00:59:42.400 little bit more information because
00:59:43.119 you're actually specifying what columns
00:59:44.319 you want to to do the join on and then
00:59:46.440 natural join again is not something I
00:59:49.799 recommend again the anti SQL standard
00:59:51.880 prefers want to to explicitly Define as
00:59:54.200 much as possible uh so that way if the
00:59:56.680 schema changes or things evolve it
00:59:58.599 doesn't break your application
01:00:01.680 code all right so there's a bunch of
01:00:03.799 other stuff in that came along later in
01:00:06.000 the 70s for uh the rational model how to
01:00:09.160 rename columns uh how to assign colums
01:00:12.240 to to variables removing duplicates de
01:00:15.079 aggregations and sorting and division uh
01:00:17.960 again these all came after Ted CS
01:00:19.799 original paper and most Data Systems are
01:00:22.680 going to
01:00:23.440 support maybe not division but
01:00:25.400 everything
01:00:28.520 above
01:00:30.079 okay so that's the crash course what you
01:00:32.079 need to know for relational algebra but
01:00:33.240 we'll see how this you know as we go
01:00:35.319 along I should build the the query
01:00:36.599 engine of a system that's be predicated
01:00:38.799 on on these
01:00:41.520 ideas all right
01:00:43.599 so as I said before relational algebra
01:00:46.599 is considered a procedural language like
01:00:48.520 even though it's mathematical notation
01:00:50.559 but you can kind of easily see how you
01:00:51.559 can Implement a system to implement it
01:00:53.799 right one of the complaints about Ted
01:00:54.960 cod's paper in the 70s was they thought
01:00:56.680 it was too
01:00:58.280 mathematical I'm not saying that I'm I'm
01:01:00.319 I'm brilliant and I could easily
01:01:01.480 decipher it but I was surprised when
01:01:03.039 when they said that because it it's not
01:01:04.319 that it's not that esoteric it's not
01:01:06.119 that hard right any I think any uh you
01:01:09.319 know CS undergrad people should be able
01:01:10.760 to understand it but it's still defining
01:01:13.760 the steps you want the data system to
01:01:15.480 perform in order to compute your query
01:01:18.000 right so I have to say if I'm going to
01:01:20.480 join
01:01:21.359 RNs uh I have to Define how in what
01:01:24.319 order I want that to happen so I would
01:01:26.200 say all right first my choices are first
01:01:27.920 join R and then s then do the select on
01:01:31.359 it uh to to filter out the tupal that I
01:01:35.039 want or I could do the filter on s first
01:01:37.760 based on the B ID then take whatever the
01:01:39.799 output of that uh select operator then
01:01:42.119 do the join against
01:01:44.079 that and again there would be pretty
01:01:46.440 dramatically different performance uh uh
01:01:48.920 of these two queries based on what the
01:01:51.359 database actually looks like again if if
01:01:54.720 if RNs only have 10 tup then it's not
01:01:57.559 that big of a deal but if RNs have
01:02:00.000 billions of tup then I definitely want
01:02:02.240 to filter as much as I can out from s
01:02:04.079 before I join it with with r but in raal
01:02:07.279 algebra there is no concept of of allow
01:02:09.440 things to be reorder I'm defining
01:02:10.880 exactly what I want to
01:02:12.880 happen so this is going to lead us to
01:02:15.000 next class talking about SQL but a
01:02:16.480 better solution is going to be say again
01:02:18.000 the high level definition or Declaration
01:02:20.520 of the answer that I want in my query
01:02:23.440 and let the data system figure out
01:02:24.640 what's the best way to to perform that
01:02:27.000 and again now if I change the physical
01:02:28.760 layout or data structures that are in my
01:02:31.520 database uh I don't have to change my
01:02:33.880 query plan uh or don't to change my
01:02:36.760 query if it's def find a SQL I let the
01:02:38.400 data system figure that out for
01:02:41.000 me so that that's why SQL matters and we
01:02:43.839 again we'll see this more next
01:02:46.079 class all right so
01:02:48.960 the as I said the relational model
01:02:51.160 defined by Ted cod in the 1970s didn't
01:02:53.160 come with a programming language SQL was
01:02:55.079 amended by IBM a few years later Ted cot
01:02:58.000 eventually proposed his own query
01:02:59.279 language called Alpha but nobody
01:03:01.160 actually implemented that um and there
01:03:03.200 was actually an early version of SQL
01:03:04.480 called Square which we'll see next time
01:03:06.480 which required a keyboard that didn't
01:03:07.839 exist because you had to write things
01:03:08.839 vertically right it was a bizarre thing
01:03:10.960 um but SQL basically became the defao
01:03:13.279 standard that it is now it wasn't the
01:03:14.599 first one there was another language
01:03:15.559 called quell invented by Stonebreaker uh
01:03:18.440 from Ingress which later became
01:03:19.880 postgress um but there was there's a
01:03:23.079 bunch of there was other variations of
01:03:25.039 of Rel query languages SQL end up being
01:03:27.520 the dominant one there is a SQL standard
01:03:30.079 but again nobody actually implements
01:03:31.680 that uh exactly in every system so the
01:03:35.200 idea is that instead of writing
01:03:36.160 procedural code like this like doing my
01:03:37.640 lookup in in in Python code I'm better
01:03:40.480 off writing SQL because now I don't care
01:03:43.480 about how stuff's physically stored I
01:03:45.039 don't care how how the query plan is
01:03:46.920 actually going to execute I let the data
01:03:49.520 system handle all that for
01:03:52.359 me so any questions about the relational
01:03:54.440 model
01:03:57.200 yes when we talked about relational
01:03:58.880 algebra there was no concept of a key
01:04:01.119 like a primary key in that situation
01:04:03.200 because when we did unions I didn't
01:04:04.680 understand like what if we had two
01:04:05.920 values the same key so this question is
01:04:07.920 we didn't when we talk about relational
01:04:09.079 algebra we didn't mention primary Keys
01:04:12.440 uh and that's because the you would
01:04:13.920 Define that in the schema of like here's
01:04:16.440 what My Relations look like the DAT syst
01:04:18.920 can then enforce that the constraint
01:04:20.480 that the primary key has to be unique
01:04:22.480 but then when it came time to actually
01:04:23.720 run queries uh you don't care like what
01:04:27.400 the primary key actually is so I can do
01:04:29.880 joins I can do intersections all that
01:04:31.520 without worrying about what the primary
01:04:32.799 key
01:04:36.359 is likewise I didn't have toine what the
01:04:38.279 far key was right it's it's there it's
01:04:40.960 it's a it's Integrity
01:04:45.720 constraint all right so I want to
01:04:47.520 briefly talk about uh in the last five
01:04:49.799 minutes uh the leading alternative is
01:04:52.000 going to be the the document Json model
01:04:54.240 and then the the vector database stuff
01:04:56.000 is the hot thing now uh I just want to
01:04:57.960 expose you to this real quickly what
01:04:59.680 what these ideas are and then we'll we
01:05:02.279 can mostly ignore them throughout the
01:05:03.359 rest of the
01:05:04.640 semester all right the docine data model
01:05:07.359 is just think Json right or XML or or
01:05:12.079 object Orient uh you know uh data right
01:05:16.640 but the idea is that you're going to
01:05:17.720 have some kind of pical collection of of
01:05:19.920 data where there's going to be these
01:05:22.000 name key value pairs but then within a
01:05:25.119 given doc
01:05:26.279 you can have a nesting of arrays nesting
01:05:28.359 of other documents and so forth right
01:05:32.079 Json is how you would implement this
01:05:33.520 today there's older systems from XML and
01:05:35.760 then even earlier than that in the early
01:05:37.039 90s late 80s when object oriented
01:05:39.000 programming was a big thing there was
01:05:40.119 these object oriented databases that
01:05:41.839 you've never heard of uh that basically
01:05:43.920 try to map like C++ objects into objects
01:05:46.119 in a database so instead of operating on
01:05:48.200 relations you would operate on on
01:05:49.920 objects so we'll see this more next
01:05:52.599 class but the problem that they're
01:05:54.160 trying to solve is the idea of the Rel
01:05:55.640 ational object impedance mismatch
01:05:57.160 meaning I'm writing code in my
01:05:59.599 application based on objects uh that
01:06:02.200 have this High structure but then when I
01:06:04.160 have to store it in my database the DAT
01:06:06.079 requires me to store it as relations and
01:06:08.480 then now I need a way to map that back
01:06:09.760 and forth between relations and objects
01:06:11.200 which can be
01:06:12.119 cumbersome there's a bunch of systems
01:06:14.200 out there uh that implement this the
01:06:16.520 document model manga to be is probably
01:06:18.119 the most famous one uh CB or cou Bas is
01:06:20.720 probably the second one but again this
01:06:23.359 idea goes back to the 1980s
01:06:26.680 so going back to my example of the of
01:06:29.559 our music store I would have a relation
01:06:32.119 for artists I would have a relation for
01:06:33.559 album and then I have this this cross
01:06:34.880 reference table cross reference relation
01:06:36.960 that Maps artists to albums right so now
01:06:39.680 if I want to get for a given artist all
01:06:41.559 the albums that they appear on I have to
01:06:43.599 do a join to go from the artist table to
01:06:46.839 then the artist album table and then to
01:06:48.599 the the the album table so the document
01:06:52.119 model people say this is stupid joins
01:06:54.279 are slow you want get rid of this thing
01:06:57.039 and instead what you want to do is just
01:06:58.640 embed for a given artist all the albums
01:07:01.599 that they appear on or the reverse of
01:07:03.599 that for given album all the artists
01:07:05.480 that appear on
01:07:06.599 it so the idea is like if you're writing
01:07:08.760 much uh python code or Java code
01:07:11.000 whatever you define these classes and
01:07:13.440 then when now you actually want to store
01:07:14.559 it in your database uh in this case here
01:07:16.960 for given an artist we're now going to
01:07:18.240 embed the the list of of albums that
01:07:21.599 they appear on so now for again when I
01:07:24.240 want to do that lookup for a given AR
01:07:25.520 artist go give me all their albums it's
01:07:27.279 one query to go fetch that artist record
01:07:29.599 and then it pulls on all their
01:07:31.720 albums so this a good idea or a bad
01:07:35.920 idea again I'm it's obvious what my
01:07:38.559 answer is GNA be uh why is it a bad
01:07:41.680 idea yes you can direct quy onbs he says
01:07:46.079 you can't query directly on albums you
01:07:47.680 could you can do like you you can do
01:07:49.599 nesting inside get things yes
01:07:55.920 prict
01:07:59.279 what she said yes she said and she's
01:08:01.760 correct this is you have to predict what
01:08:03.920 the query is are going to want to look
01:08:04.920 up on and then model that in your in
01:08:07.200 your database absolutely yes and then
01:08:09.279 likewise I I'm going to be end up
01:08:11.799 duplicating a bunch of information if if
01:08:14.240 if a artist appears on sorry if multiple
01:08:17.158 artists appear on one album I got to
01:08:19.040 re-record that over and over again so
01:08:21.479 some cases this nesting makes sense in
01:08:23.040 many cases it doesn't yes and also you
01:08:25.080 want Del an
01:08:26.839 album you said if you got to delete an
01:08:28.600 album you got to find all the artists
01:08:29.759 that where the album appears on yes you
01:08:31.799 can do an index an index could help find
01:08:34.158 that but still it's it's implicitly in
01:08:36.359 in your application what the layout
01:08:38.399 is so in some cases you do want to store
01:08:41.000 things as as Json in your database uh
01:08:44.399 but often times you do
01:08:47.920 not all right so the last one to talk
01:08:49.759 about is the vector databases so this is
01:08:52.880 the hot thing now there's a bunch of
01:08:54.198 companies that have gotten a lot of
01:08:55.158 money
01:08:56.158 uh that are Building Systems in the
01:08:57.479 space we is coming to talk with us on
01:09:00.000 campus uh in a few weeks uh I like those
01:09:03.719 guys they're good people um but no they
01:09:08.279 fun I was I was on their podcast they're
01:09:09.759 fun
01:09:11.198 uh
01:09:12.759 so a a vector database at its core when
01:09:16.399 when you say a vector database they
01:09:17.960 really mean a document database that
01:09:19.920 also has this extra data type called a
01:09:21.759 vector an embedding and and think of
01:09:23.799 that as a it's a larger array of
01:09:25.679 floating Point numbers and what they're
01:09:28.719 trying to provide is the ability to do
01:09:31.279 approximate nearest neighbor search
01:09:32.920 searches based on these vectors because
01:09:35.600 these vectors are going to be generated
01:09:36.960 from some kind of Transformer embedding
01:09:39.238 that's trying to represent what's
01:09:40.640 actually in the data you're storing
01:09:43.080 right the end of the day there's just a
01:09:44.960 fast index to do approximate nearest
01:09:46.799 neighbor search so what does that look
01:09:49.359 like so again say I have my album
01:09:51.719 table and then somehow I'm going to get
01:09:53.960 out all the lyrics from these albums
01:09:56.239 from from you know from Rap Genius or
01:09:58.520 whatever right and I'm going to feed
01:10:00.400 that into some kind of Transformer uh
01:10:02.560 either I'm using obing eye or or or
01:10:04.800 something from hugging face and then
01:10:06.600 that's going to generate me a bunch of
01:10:07.880 these embeddings which is just floating
01:10:09.360 Point arrays of floating Point numbers
01:10:11.360 and that somehow they the the magic of
01:10:14.040 the Transformer is that somehow
01:10:15.239 implicitly the information or the
01:10:16.800 semantics of the data that I fed into
01:10:19.520 the Transformer is is is in those uh
01:10:22.360 floating Point numbers so then I'm going
01:10:24.560 to show that in my vector vector
01:10:25.880 database it's going to have a vector
01:10:27.080 index uh the most common one is hnsw
01:10:30.280 highle near or highle navigable small
01:10:33.400 worlds ivv IVF flat it's another one but
01:10:37.159 there's a bunch of libraries like meta
01:10:38.560 Fest or Spotify noi there can be some
01:10:40.840 data structure we'll cover in a few
01:10:42.040 lectures to to easily do these these
01:10:44.400 these near nebor searches on these uh uh
01:10:47.400 on these embeddings so now my query
01:10:49.679 instead of doing exact lookups like find
01:10:51.280 me jiz albums I can say things like find
01:10:54.280 me albums that are similar to Liquid
01:10:56.360 Swords and somehow assuming I have
01:10:58.600 lyrics to Liquid Swords I can convert
01:11:01.840 that information into uh put that in my
01:11:04.760 Transformer I get out the same kind of
01:11:06.920 embedding that I would get when I first
01:11:08.159 loaded my database and then I do nearest
01:11:10.080 neighbor search on the vector index and
01:11:11.800 that it returns back the A ranked list
01:11:14.320 of of matches right so the vector
01:11:17.760 database is essentially this part here
01:11:20.400 they can also store metadata like they
01:11:22.120 also store this information I over here
01:11:23.600 as Json right so I say find me all the
01:11:26.239 albums that are sound like liquid stores
01:11:27.520 that came out after 2012 or something
01:11:30.000 and I can incorporate that in my lookup
01:11:32.360 but at its core a vector database is
01:11:34.080 this Vector index piece here but in the
01:11:36.520 last year or so pretty much all the
01:11:38.440 relational databases now support Vector
01:11:41.679 indexes right so it's again it's it's I
01:11:45.239 argued I've told the we8 guys this
01:11:46.639 directly like it's
01:11:48.600 not the idea of vector search near
01:11:50.800 neighbor search does not mean you have
01:11:51.920 to build a whole new system that throws
01:11:53.120 away everything we talk about the entire
01:11:54.280 semester it's just an extra thing we can
01:11:56.400 add and the relational model can
01:11:58.120 accommodate it so the the SQL standard
01:12:00.560 does not support doesn't have a notion
01:12:02.600 of this nearest neighbor searches uh
01:12:05.880 postgress through PG Vector has their
01:12:07.760 own API Oracle has copied that I think
01:12:10.360 that's going to end up in the SQ
01:12:11.280 standard in a few years uh and the the
01:12:15.560 vector guys will have to figure out how
01:12:16.760 to how to overcome
01:12:18.000 that
01:12:19.719 okay this is like crash course in vector
01:12:22.080 vector databases in in in two minutes
01:12:24.239 but the we8 guys come talk about it more
01:12:26.480 uh later in the semester all right
01:12:28.960 soever it is databases are ubiquitous
01:12:31.239 databases are important databases are
01:12:32.560 the second level in my life um the
01:12:34.440 relational algebra is going to be the
01:12:35.800 foundation for how we're going to build
01:12:37.360 our systems to support them uh and then
01:12:39.600 we're going to see this over and over
01:12:40.480 again we talk about crit optimization
01:12:41.480 career execution uh and certainly we'll
01:12:43.600 see this next class when we talk about
01:12:44.880 SQL okay so next class will be not done
01:12:48.400 yet Q&A next class we're going to do
01:12:50.679 modern SQL so by modern SQL I mean like
01:12:52.719 I'm not going to te you what a select
01:12:53.639 star is it's 2024 you guys are see me
01:12:56.840 students I'm assuming most of you have
01:12:57.920 seen seable 4 in some form the basic
01:13:00.159 form of it so I'll try to teach you the
01:13:01.639 more advanced things and where things
01:13:03.320 break in the SQL standard okay so least
01:13:05.320 make sure you understand basic SQL for
01:13:07.120 showing up next class
01:13:08.840 okay all right we have eight minutes
01:13:12.040 left any questions about
01:13:16.360 databases yes so you talked about a
01:13:19.280 little bit earlier we talked about the
01:13:20.639 blurry line between relational and do
01:13:25.679 a little bit yes and it feels like
01:13:28.400 relational database support SE now right
01:13:33.520 so you explain little that me so his
01:13:38.120 question is he's used dyb dynb is one of
01:13:40.600 the uh from Amazon one of the first no
01:13:42.400 SQL databases it originally started off
01:13:44.600 as I think a as a key value store then
01:13:47.440 they added for Json and then more
01:13:49.560 recently they've added basically looks
01:13:51.199 like tables and I don't think it's
01:13:52.880 directly SQL I think it's the it's part
01:13:54.320 of ql it's it's it's no not graph there
01:13:57.800 part of ql is Amazon's dialect of SQL
01:14:00.960 and it looks like SQL so why is this why
01:14:03.400 is this uh convergence between the the
01:14:05.440 no seal guys and the and the um and in
01:14:09.239 the relational World well because all
01:14:11.000 the things we talked about today why
01:14:12.679 having a relational model and and making
01:14:14.239 sure you can't shoot yourself in the
01:14:15.520 foot in your database is a good idea
01:14:18.199 they they've come realize oh customers
01:14:20.000 actually want these things and they've
01:14:21.600 added added it added it on top of it
01:14:24.120 right so that's why I think there's a
01:14:25.320 convergence because like in the same way
01:14:27.840 that no one's going to vent a new
01:14:29.040 mathematics where like CU cuz 1 plus 1
01:14:31.080 equals 2 is just true I think like the
01:14:33.520 relational model is just the true way
01:14:35.400 the correct way to implement to
01:14:37.080 represent data and you can add
01:14:38.880 accoutrements like the vector indexes on
01:14:40.760 top of that or the various things
01:14:42.679 dealing with Json but everyone's
01:14:44.719 basically coming back around like the
01:14:45.920 relational model is the right way to go
01:14:47.800 katab is a genius yes so I have a
01:14:51.679 question about the uh V database yes you
01:14:55.120 know there a very famous
01:14:57.199 St
01:14:59.400 Rock by yes I wonder like with this kind
01:15:03.639 of real time Vector search database what
01:15:06.719 kind of realistic um you know
01:15:09.000 applications you can imagine like for
01:15:11.440 Vector index for dates
01:15:14.000 uh dat all right so his first question
01:15:16.560 you start off with uh open ey made a
01:15:19.000 major acquisition the summer they bought
01:15:20.679 rocket rocket was a database startup a
01:15:23.320 relational database startup uh based on
01:15:25.480 the guys that that created frb out of
01:15:27.520 Facebook an opening eye uh he paid a lot
01:15:30.880 of money for it um so the question is
01:15:33.639 what first of all what is open ey going
01:15:34.840 to do with rocket I can't tell you uh
01:15:38.080 but what are some uses for a vector
01:15:40.280 database so going back to my example
01:15:42.719 here
01:15:46.239 um right this idea of this semantic
01:15:49.120 search like find me the albums that are
01:15:50.960 similar to Liquid Swords I'm not
01:15:53.199 defining what it means to be similar
01:15:55.120 right or find me the albums where they
01:15:56.800 talk about slinging rocks well you could
01:15:59.880 have your Transformer know that slinging
01:16:01.280 rocks means dealing drugs and even
01:16:03.400 though you ask for something in rocks it
01:16:04.679 knows somehow magically knows because
01:16:06.239 the training data based on can how to
01:16:08.840 match that to to different things so
01:16:11.679 it's a way to do better searching based
01:16:14.000 on the semantics rather than find exact
01:16:17.000 matches that's that's where these things
01:16:18.880 are being used for yes are we not able
01:16:21.760 to do like these kind of semantic or
01:16:23.480 like fuzzy search through Rel database
01:16:26.080 the question is are we not able to do
01:16:27.480 the semantic searches Rel no I said
01:16:29.239 absolutely yes you can assuming you can
01:16:31.440 store this an embedding and then have a
01:16:33.800 vector a vector index do the fast
01:16:35.719 approximate nearest neighbor search you
01:16:37.960 could write SQL queries against this
01:16:39.360 postest does this PG Vector all all
01:16:42.199 relational databases have now some form
01:16:43.800 of a vector index you can do this prior
01:16:46.520 to this though the way you would do
01:16:47.560 lookups would be like fuzzy matching
01:16:49.400 like find me all the albums that you
01:16:51.440 know have the word swords in it right
01:16:53.600 you couldn't do this this the semantic
01:16:55.920 meaning is that's that's part that's new
01:16:58.440 in the back
01:17:04.520 yes his question is if every record
01:17:06.520 needs to go through a Transformer
01:17:07.400 wouldn't that be slow
01:17:12.960 yes I mean milliseconds it takes
01:17:15.400 milliseconds yeah it's not it's not
01:17:17.400 seconds yeah it's
01:17:21.679 Rel again be very clear here like you
01:17:24.360 can put the you can put this in a
01:17:25.560 relational database right the question
01:17:29.360 would be is the is running through the
01:17:32.080 Transformer to get back the the
01:17:33.360 embedding they didn't do the lookup is
01:17:35.239 that going to be slower than doing an
01:17:36.880 inverted index which we'll cover later
01:17:38.600 on
01:17:40.400 maybe depends on what this is depends on
01:17:42.800 what's the memory there's so many
01:17:43.960 different factors involved it's hard to
01:17:45.360 say and that's and then that that
01:17:47.440 assumes that you're you're going to get
01:17:48.960 the data you'd want using a fuzzy fuzzy
01:17:50.639 search anyway again for some things like
01:17:53.760 it's not going to work CU there's no no
01:17:55.400 understanding of what actually is in the
01:17:57.320 in the in the data what it means that's
01:17:59.520 what the Transformer does for
01:18:03.040 you yes when we are taking interview
01:18:05.880 sometimes the interviewer ask us to uh
01:18:08.400 design a system and they want us to
01:18:10.400 choose which kind of database like C no
01:18:13.560 sometimes they are more satisfied with
01:18:15.120 you when you choosing Nole but as you
01:18:17.520 said that right
01:18:19.800 so his question is sometimes in the job
01:18:22.400 interview the interviewer ask you pick a
01:18:24.280 database for whatever like prototype
01:18:25.920 system you're building the answer is
01:18:27.639 postgress always pick postgress right
01:18:30.440 I'm dead
01:18:31.719 serious right and you can't say oh
01:18:34.040 because Andy said so but like postgress
01:18:36.679 is a rock solid database system that has
01:18:38.719 a lot of the features you would see in a
01:18:41.040 you know sort of enterprise system um
01:18:44.000 and actually just not just for
01:18:45.320 interviews for anybody doing a startup
01:18:46.760 anything your first choice would be
01:18:48.080 postgress right because because you want
01:18:50.920 to be spending your time like building
01:18:52.639 your application not worrying about what
01:18:53.800 datab system you want to build so you
01:18:55.159 just say postgress because I want to
01:18:56.600 spend my time building the application
01:18:57.719 because that's what matters like no
01:18:58.960 one's going to know or care that your
01:19:00.159 application is running on postgress
01:19:01.360 versus mongod DB because they don't
01:19:02.760 interact with the data at that level
01:19:04.480 postest is almost always the right
01:19:05.800 choice now you may get to the point
01:19:07.120 where postest can't scale handle your
01:19:08.800 data and at which point you pay not me
01:19:11.480 but paid somebody else a lot of money to
01:19:12.639 help figure out what dat is you know how
01:19:14.040 to make post
01:19:15.280 scale in the back
01:19:19.480 yes can you speak up sorry yeah so as as
01:19:22.480 a career wise like what do you think
01:19:24.280 like good compies can work you know it's
01:19:27.040 a good place to work and you we should
01:19:30.440 run his question is uh what are some
01:19:32.719 good database companies to work at what
01:19:33.800 are some bad database companies to work
01:19:36.159 at all right so good database companies
01:19:38.800 this is the great thing about databases
01:19:39.960 there's a lot of money and there's a lot
01:19:42.000 of lot of lot of people building
01:19:43.760 database systems so like say you you're
01:19:45.480 in operating systems where can you go to
01:19:47.199 build an oper system IBM Red Hat maybe
01:19:50.199 right the Linux guys are all doing their
01:19:51.760 various things but like there isn't
01:19:53.400 there there aren't a lot of competing
01:19:54.719 operating systems there's a ton of
01:19:56.199 databases and if you want to go to a big
01:19:57.880 company the Microsoft the Amazon the
01:19:59.400 Googles even the Facebooks right all of
01:20:02.040 them are building database systems and
01:20:03.639 then there's a bunch of startups that
01:20:04.960 are all in the space as well now some of
01:20:06.679 them have questionable uh Financial
01:20:09.120 footings um but I say this that because
01:20:11.239 my database start up failed this summer
01:20:13.120 but um the so there's a lot of choices
01:20:16.320 in the database and there's a lot of
01:20:17.400 money in it right even now even though
01:20:19.520 you know the relational model relation
01:20:20.840 dees are 50 years old there's still
01:20:23.280 trying people trying to build new
01:20:24.199 systems all time now in terms of bad
01:20:26.480 companies uh I mean I'll to say off the
01:20:28.880 bat Enterprise DB
01:20:34.719 uh them so avoid Enterprise DB
01:20:38.520 uh in terms of other ones I mean for
01:20:41.480 startups obviously you want to talk to
01:20:42.760 people and see what their the finances
01:20:44.960 look like uh you can maybe get a sense
01:20:47.600 of how much they're chasing bads like if
01:20:51.000 they're a uh if if all a sudden they
01:20:54.040 they start off being you know some kind
01:20:55.400 of database and now they're a vector
01:20:56.400 database because it's the hot thing or
01:20:57.360 the AI database looks a little dicey
01:20:59.840 right another interesting Avenue is also
01:21:02.840 I mentioned like Google Google and
01:21:04.040 Amazon they'll sell you you know they
01:21:05.159 sell datab Services then there's
01:21:06.560 companies like uh I can't say well I'll
01:21:09.600 bleep it out like they're building a
01:21:11.840 database system and like the great thing
01:21:14.120 about it is they're building it in house
01:21:15.760 they they don't have to worry about
01:21:16.560 getting customers because they're
01:21:17.440 they're their own customer but they're
01:21:18.400 actually building a whole system from
01:21:19.480 scrap from and doing some interesting
01:21:21.159 things so there's so many different
01:21:22.400 options to do this in databases and
01:21:24.239 that's why I think this class is super
01:21:25.520 important because you're you're
01:21:26.719 encounter this throughout your life and
01:21:28.679 the companies don't want to hire a bunch
01:21:29.920 of random JavaScript programmers because
01:21:31.280 those people are going to break your
01:21:32.040 database system you don't want them to
01:21:33.000 touch the internals they want CMU
01:21:34.719 students who know how to you know handle
01:21:36.800 these things uh and are dying to hire
01:21:39.040 you guys uh yes quick do you think this
01:21:41.360 class is a good preparation for database
01:21:43.199 career his question is is this class
01:21:44.360 good preparation for databased career I
01:21:46.040 am biased because it's my class um I've
01:21:49.320 been told by certain davus companies
01:21:50.920 this class is the uh onboarding process
01:21:53.600 for davus companies
01:21:55.159 uh I've also been told that the the
01:21:57.440 interviews for some D companies are
01:21:59.040 basically entire lectures from this
01:22:00.800 class uh so take that to mean what it
01:22:04.040 what it means right um there's always
01:22:07.320 money in databases how about that okay
01:22:10.560 last question what's the best way to
01:22:12.719 incorporate blockchain into
01:22:18.760 my all right do do you have a real
01:22:21.320 question uh what happened to the DJ in
01:22:23.639 this course uh all right um yeah so
01:22:26.520 unfortunately we cannot have a DJ this
01:22:27.719 year because of legal problems dealing
01:22:29.159 with uh War Hall so I apologize uh they
01:22:33.600 I there is the moral T I have tenure but
01:22:36.080 there is the moral T Clause that seeu
01:22:37.600 where I can still get fired uh so I'm
01:22:39.320 trying to lay low this year so I
01:22:41.280 apologize okay all right all right guys
01:22:45.199 uh that's it see you on tues or
01:22:48.239 Wednesday I need something refreshing
01:22:50.480 when I get finished manifesting too cold
01:22:52.600 a whole B like Smith and Wesson one
01:22:54.800 court and my th's hip hop related write
01:22:57.360 a rhyme in my pants intoxicated lyrics
01:23:00.199 are quicker with a simple Mo licker
01:23:02.239 since on a city slicker play waves are
01:23:04.520 picker rhes I create rotate at a r too
01:23:07.760 quick to duplicate feel a breze as a
01:23:09.960 skate mik at fah when I hold it real
01:23:12.679 tight then I'm in flight then we ignite
01:23:16.159 starts to boil you I heat up the party
01:23:18.199 for you let a girl R me and my mic down
01:23:20.600 with oil Rec still turn with third
01:23:22.800 degree burn for one man I heat up your
01:23:25.320 brain give it a suntan to just cool let
01:23:28.040 the temperature rise to cool it off with
01:23:31.280 s eyes
01:23:34.210 [Music]
