# NLP restaurant finder

This project is a semestral work for an [Internet Applications Development course](https://sites.google.com/a/via.felk.cvut.cz/via/) on a [CTU in Prague](https://www.cvut.cz/en).


## Goal

The main aim is to create a simple conversational chat bot, which will be able to reply to questions regarding the nearby restaurants, their daily menu, and details. For example:

> **What is the nearest restaurant?**  
> U Topolů
>
> **And what is on their daily menu?**  
> Silný vývar z hovězích kostí se zeleninou a vaječným svítkem and Selečí bůček pečený na kmíně, čerstvý listový špenát zahuštěný vejci, bramborový knedlík, for 119 Kč
>
> **Where is it?**  
> Jugoslávských partyzanů 32
>
> **Call there.**  
> +420608630310

The application has to be able to:

- search for restaurants, filter them by a cuisine type and order by distance, price or rating
- get the daily menu of a restaurant
- get the restaurant location, phone number, and website


## Architecture

The application backend will use a Python, namely a [Flask framework](http://flask.pocoo.org/). The backend will handle a communication with two other APIs needed to solve the goal:

- [Wit.ai](https://wit.ai) for NLP
- [Zomato](https://developers.zomato.com/api) for retrieving a restaurant info

The backend will provide its own API, which will be used mainly by the application frontend but can also be used by other developers.

The frontend will be a Javascript web application. The advantage of using Javascript is, that there are many cool browser APIs available for it, (for example, [geolocation](https://developer.mozilla.org/en-US/docs/Web/API/Geolocation) or [microphone](https://developer.mozilla.org/en-US/docs/Web/API/MediaDevices/getUserMedia)), without a need to install anything. These can be used in the future to further improve the application.
