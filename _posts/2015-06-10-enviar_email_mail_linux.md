---
title:  "Enviando e-mail no linux usando o utilitario mail"
date:   2015-06-10 17:20:00
categories: posts
layout: post
---
Simples script para enviar e-mails usando o utilitario mail, que é padrão em diversas distribuições linux.
<!--more-->
{% highlight bash %}

#!/bin/bash
######################################################
#ENVIAR E-MAIL USANDO O UTILITARIO MAIL              #
#CRIADO POR ADRIANO TANAKA adriano.tanakaa@gmail.com #
#VERSAO 1: 10/06/2015                                #
######################################################

#VARIAVEIS
MENSAGEM=${1:-"mensagem"}

EMAIL=${2:-"adriano.tanakaa@gmail.com"}

echo "Enviando e-mail para: $EMAIL" `date`
echo "$MENSAGEM" | mail -s "Teste" $EMAIL

echo "Mensagem: " $MENSAGEM
echo "####"
echo "Destinatario: "
echo $EMAIL
echo "Email enviado para $2  -  `date` "

{% endhighlight %}


Como usar:

{% highlight bash %}

./envia_email_mail.sh "Sua mensagem" email@destinatario.com

{% endhighlight %}
