# How the Internet works

*This chapter is inspired by a talk "How the Internet works" by Jessica McKellar (http://web.mit.edu/jesstess/www/).*

We bet you use the Internet every day. But do you actually know what happens when you type an address like http://djangogirls.org in your browser and press 'Enter'?

First thing you need to understand is that a website is just a bunch of files saved on a computer disk. Just like your movies, music or pictures.
However, there is one part that is unique for websites: they include computer code called HTML.

If you're not familiar with programming, it can be hard to grasp at first, but your web browsers (like Chrome, Safari, Firefox, etc) love HTML. Web browsers are designed to understand this code,
follow the instructions and present all these files that your website is made of exactly the way you want them to be presented.

As every file, we need to store them somewhere on a computer disk. For the Internet, we use special, powerful computers called *servers*. They don't have
a screen, mouse or a keyboard, because their main purpose is to store data and serve it. That's why they're all called *servers* -- because they *serve* you data.

Ok, but you want to know how the Internet looks like, right?

We drew you a picture! It looks like this:

![Figure 1.1](images/internet_1.png)

Looks like a mess, right? In fact it is a network of connected machines (*servers*). Hundreds of thousands of machines! Many, many kilometers of cables around the world! You can visit a Submarine Cable Map website (http://submarinecablemap.com/) to see how complicated the net is. Here is a screenshot from the website:

![Figure 1.2](images/internet_3.png)

It is fascinating, isn't it? But obviously, it is not possible to have a wire between every machine connected to the Internet. So to reach a machine (for example the one where http://djangogirls.org is) we need to pass a request through many, many different machines.

It looks like this:

![Figure 1.3](images/internet_2.png)

Imagine that when you type http://djangogirls.org you send a letter that says: "Dear DjangoGirls, I want to see djangogirls.org website. Send it to me, please!"

Your letter goes to the post office. Then it goes to another that is nearer your addressee, then to another and another till it is delivered to the destination. The only unique thing is that if you send letters (*data packets*) frequently to the same place, each letter could go through totally different post offices (*routers*), depending how they are distributed in each office.

![Figure 1.4](images/internet_4.png)

Yes, it is as simple as that. You send messages and you expect some response. Of course, instead of paper and pen you use bytes of data, but the idea is the same!

Instead of address with street name, city, zipcode and country, we use IP addresses. Your computer asks DNS (Domain Name System) first to translate djangogirls.org into an IP address. It works a little bit like old-fashioned phonebooks where you could look for the name of the person and find their phone number and address.

When you send a letter it needs to have certain features to be delivered correctly: address, postmark etc.. You also use language that the receiver understands, right? The same is with *data packets* you send in order to see a website: you use a protocol called HTTP (HyperText TransferProtocol).

So basically, when you have a website you need to have a *server* (machine) where it lives. The *server* is waiting for any incoming *requests* (letters that ask you to send your website) and it sends back your website (in another letter).

Since it is a Django tutorial, you will ask what Django does? When you send a response you don't always want to send the same thing to everybody. It is so much better if your letters are personalized especially for the person that has just written to you, right? Django helps you with creating these personalized, interesting letters :).

Enough talking, time to create! But first - the boring part - installation!
