---
title: Utilisation d’en-têtes de demande/réponse de notification BITS
description: BITS peut envoyer l’emplacement du fichier de téléchargement (par référence) à votre application serveur ou il peut envoyer le fichier de téléchargement dans le corps de la demande (par valeur).
ms.assetid: b80f9077-54e7-4d10-909a-dee7d8822627
ms.topic: article
ms.date: 11/29/2018
ms.openlocfilehash: 3db568f483468cbc92474f24f830da5bf1be94a2165cbb69a2d1751cc58965dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119021067"
---
# <a name="using-bits-notification-requestresponse-headers"></a>Utilisation d’en-têtes de demande/réponse de notification BITS

BITS peut envoyer l’emplacement du fichier de téléchargement (par référence) à votre application serveur ou il peut envoyer le fichier de téléchargement dans le corps de la demande (par valeur). Pour spécifier la façon dont le service BITS envoie le fichier de téléchargement à votre application serveur, définissez la propriété de la métabase IIS, [**BITSServerNotificationType**](bits-iis-extension-properties.md). Si vous spécifiez par référence, BITS passe l’emplacement du fichier dans l’en-tête BITS-Request-DataFile-Name. Pour envoyer une réponse, créez et écrivez votre réponse dans le fichier spécifié dans l’en-tête BITS-Response-DataFile-Name.

Les applications serveur qui envoient la même réponse à de nombreux clients doivent utiliser par référence, de sorte qu’il n’y a qu’une seule copie de la réponse sur le serveur. Par exemple, dans une application de mise à jour logicielle, le client télécharge sa configuration logicielle vers l’application serveur. L’application serveur détermine le package dont le client a besoin et envoie l’URL du package à BITS. Ensuite, le service BITS télécharge le package en tant que réponse.

Les applications serveur qui génèrent des réponses uniques pour chaque client doivent utiliser par valeur. Par exemple, une application serveur qui prend en charge l’achat de fichiers musicaux doit envoyer un fichier de musique signé au client. Étant donné que le fichier de musique signé est unique pour le client, l’application serveur ne l’enregistre pas sur le serveur. Par valeur est également utile pour une application déjà écrite pour accepter directement les données du client Web.

Pour plus d’informations sur les en-têtes de demande et de réponse utilisés entre BITS et votre application serveur, consultez [protocole de notification pour les applications serveur](notification-protocol-for-server-applications.md).

L’exemple JavaScript suivant montre comment accéder aux fichiers de requête et de réponse dans une application serveur qui utilise la notification par référence (BITS passe l’emplacement des fichiers dans les en-têtes).


```JavaScript
  var fso = new ActiveXObject ("Scripting.FileSystemObject")
  var requestFileName = Request.ServerVariables ("HTTP_BITS-Request-DataFile-Name")
  var responseFileName = Request.ServerVariables ("HTTP_BITS-Response-DataFile-Name")
  var requestStream
  var responseStream
  var ForReading = 1
  var ForWriting = 2
  var TristateUseDefault = -2

  //Open the upload data file as text stream for reading.
  requestStream = fso.OpenTextFile(requestFileName, ForReading, false, TristateUseDefault);

  //Do something with the uploaded data.

  //Close the upload stream.
  requestStream.Close()

  //Open response data file as text stream for writing.
  responseStream = fso.OpenTextFile(responseFileName, ForWriting, true, TristateUseDefault);

  //Write a response to the response file.

  //Close the response text stream
  responseStream.Close()
```



Si vous souhaitez utiliser un autre fichier réponse que celui spécifié dans BITS-Response-DataFile-Name, appelez la méthode **Response. AddHeader** pour ajouter l’URL bits-static-Response-URL, comme indiqué dans l’exemple suivant. Si vous spécifiez un autre fichier réponse, ne créez pas le fichier réponse spécifié dans BITS-Response-DataFile-Name.


```JavaScript
  Response.AddHeader "BITS-Static-Response-URL" "https://myserver/mypath/myfile"
```
 

 




