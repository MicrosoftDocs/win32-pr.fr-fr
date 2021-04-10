---
title: Utilisation d’en-têtes de demande/réponse de notification BITS
description: BITS peut envoyer l’emplacement du fichier de téléchargement (par référence) à votre application serveur ou il peut envoyer le fichier de téléchargement dans le corps de la demande (par valeur).
ms.assetid: b80f9077-54e7-4d10-909a-dee7d8822627
ms.topic: article
ms.date: 11/29/2018
ms.openlocfilehash: 5dcbee8b82d96a4f13db0ae4de6441e9df40ce83
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104190793"
---
# <a name="using-bits-notification-requestresponse-headers"></a><span data-ttu-id="dd752-103">Utilisation d’en-têtes de demande/réponse de notification BITS</span><span class="sxs-lookup"><span data-stu-id="dd752-103">Using BITS Notification Request/Response Headers</span></span>

<span data-ttu-id="dd752-104">BITS peut envoyer l’emplacement du fichier de téléchargement (par référence) à votre application serveur ou il peut envoyer le fichier de téléchargement dans le corps de la demande (par valeur).</span><span class="sxs-lookup"><span data-stu-id="dd752-104">BITS can send the location of the upload file (by reference) to your server application or it can send the upload file in the body of the request (by value).</span></span> <span data-ttu-id="dd752-105">Pour spécifier la façon dont le service BITS envoie le fichier de téléchargement à votre application serveur, définissez la propriété de la métabase IIS, [**BITSServerNotificationType**](bits-iis-extension-properties.md).</span><span class="sxs-lookup"><span data-stu-id="dd752-105">To specify how BITS sends the upload file to your server application, set the IIS metabase property, [**BITSServerNotificationType**](bits-iis-extension-properties.md).</span></span> <span data-ttu-id="dd752-106">Si vous spécifiez par référence, BITS passe l’emplacement du fichier dans l’en-tête BITS-Request-DataFile-Name.</span><span class="sxs-lookup"><span data-stu-id="dd752-106">If you specify by reference, BITS passes the location of the file in the BITS-Request-DataFile-Name header.</span></span> <span data-ttu-id="dd752-107">Pour envoyer une réponse, créez et écrivez votre réponse dans le fichier spécifié dans l’en-tête BITS-Response-DataFile-Name.</span><span class="sxs-lookup"><span data-stu-id="dd752-107">To send a reply, create and write your response to the file specified in the BITS-Response-DataFile-Name header.</span></span>

<span data-ttu-id="dd752-108">Les applications serveur qui envoient la même réponse à de nombreux clients doivent utiliser par référence, de sorte qu’il n’y a qu’une seule copie de la réponse sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="dd752-108">Server applications that send the same reply to many clients should use by reference, so there is only one copy of the reply on the server.</span></span> <span data-ttu-id="dd752-109">Par exemple, dans une application de mise à jour logicielle, le client télécharge sa configuration logicielle vers l’application serveur.</span><span class="sxs-lookup"><span data-stu-id="dd752-109">For example, in a software update application, the client would upload its software configuration to the server application.</span></span> <span data-ttu-id="dd752-110">L’application serveur détermine le package dont le client a besoin et envoie l’URL du package à BITS.</span><span class="sxs-lookup"><span data-stu-id="dd752-110">The server application determines which package the client needs and sends the URL of the package to BITS.</span></span> <span data-ttu-id="dd752-111">Ensuite, le service BITS télécharge le package en tant que réponse.</span><span class="sxs-lookup"><span data-stu-id="dd752-111">Then, BITS downloads the package as the reply.</span></span>

<span data-ttu-id="dd752-112">Les applications serveur qui génèrent des réponses uniques pour chaque client doivent utiliser par valeur.</span><span class="sxs-lookup"><span data-stu-id="dd752-112">Server applications that generate unique replies for each client should use by value.</span></span> <span data-ttu-id="dd752-113">Par exemple, une application serveur qui prend en charge l’achat de fichiers musicaux doit envoyer un fichier de musique signé au client.</span><span class="sxs-lookup"><span data-stu-id="dd752-113">For example, a server application that supports the purchase of music files would need to send a signed music file to the client.</span></span> <span data-ttu-id="dd752-114">Étant donné que le fichier de musique signé est unique pour le client, l’application serveur ne l’enregistre pas sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="dd752-114">Because the signed music file is unique to the client, the server application would not store it on the server.</span></span> <span data-ttu-id="dd752-115">Par valeur est également utile pour une application déjà écrite pour accepter directement les données du client Web.</span><span class="sxs-lookup"><span data-stu-id="dd752-115">By value is also useful for an application that is already written to accept web client data directly.</span></span>

<span data-ttu-id="dd752-116">Pour plus d’informations sur les en-têtes de demande et de réponse utilisés entre BITS et votre application serveur, consultez [protocole de notification pour les applications serveur](notification-protocol-for-server-applications.md).</span><span class="sxs-lookup"><span data-stu-id="dd752-116">For details on the request and response headers used between BITS and your server application, see [Notification Protocol for Server Applications](notification-protocol-for-server-applications.md).</span></span>

<span data-ttu-id="dd752-117">L’exemple JavaScript suivant montre comment accéder aux fichiers de requête et de réponse dans une application serveur qui utilise la notification par référence (BITS passe l’emplacement des fichiers dans les en-têtes).</span><span class="sxs-lookup"><span data-stu-id="dd752-117">The following JavaScript example shows how to access the request and response files in a server application that uses by reference notification (BITS passes the location of the files in the headers).</span></span>


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



<span data-ttu-id="dd752-118">Si vous souhaitez utiliser un autre fichier réponse que celui spécifié dans BITS-Response-DataFile-Name, appelez la méthode **Response. AddHeader** pour ajouter l’URL bits-static-Response-URL, comme indiqué dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="dd752-118">If you want to use a different response file than the one specified in BITS-Response-DataFile-Name, call the **Response.AddHeader** method to add the BITS-Static-Response-URL as shown in the following example.</span></span> <span data-ttu-id="dd752-119">Si vous spécifiez un autre fichier réponse, ne créez pas le fichier réponse spécifié dans BITS-Response-DataFile-Name.</span><span class="sxs-lookup"><span data-stu-id="dd752-119">If you specify a different response file, do not create the response file specified in BITS-Response-DataFile-Name.</span></span>


```JavaScript
  Response.AddHeader "BITS-Static-Response-URL" "https://myserver/mypath/myfile"
```
 

 




