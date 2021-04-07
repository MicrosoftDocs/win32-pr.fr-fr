---
title: Protocole de notification pour les applications serveur
description: BITS utilise la propriété BITSServerNotificationType pour déterminer la façon dont le service BITS envoie le contenu du fichier de téléchargement à l’application serveur.
ms.assetid: d5193d0c-3ab4-47ab-a570-fea2904a4371
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0d35f6f5fec1a1de9ebd5c2c244a55bc1806b06
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939707"
---
# <a name="notification-protocol-for-server-applications"></a><span data-ttu-id="59ec3-103">Protocole de notification pour les applications serveur</span><span class="sxs-lookup"><span data-stu-id="59ec3-103">Notification Protocol for Server Applications</span></span>

<span data-ttu-id="59ec3-104">BITS utilise la propriété [BITSServerNotificationType](bits-iis-extension-properties.md) pour déterminer la façon dont le service bits envoie le contenu du fichier de téléchargement à l’application serveur.</span><span class="sxs-lookup"><span data-stu-id="59ec3-104">BITS uses the [BITSServerNotificationType](bits-iis-extension-properties.md) property to determine how BITS sends the contents of the upload file to the server application.</span></span> <span data-ttu-id="59ec3-105">Si la propriété BITSServerNotificationType a la valeur 1, [bits passe l’emplacement du fichier de téléchargement dans un en-tête](#sending-the-location-of-the-upload-file-in-a-header).</span><span class="sxs-lookup"><span data-stu-id="59ec3-105">If the BITSServerNotificationType property is set to 1, [BITS passes the location of the upload file in a header](#sending-the-location-of-the-upload-file-in-a-header).</span></span> <span data-ttu-id="59ec3-106">Si la propriété BITSServerNotificationType a la valeur 2, [bits passe le contenu du fichier de téléchargement dans le corps de la demande](#sending-the-upload-file-in-the-body-of-the-request).</span><span class="sxs-lookup"><span data-stu-id="59ec3-106">If the BITSServerNotificationType property is set to 2, [BITS passes the contents of the upload file in the body of the request](#sending-the-upload-file-in-the-body-of-the-request).</span></span>

<span data-ttu-id="59ec3-107">Pour plus d’informations sur la façon dont BITS gère les erreurs de l’application serveur, consultez [gestion des erreurs d’application serveur](#handling-server-application-errors).</span><span class="sxs-lookup"><span data-stu-id="59ec3-107">For details on how BITS handles errors from the server application, see [Handling server application errors](#handling-server-application-errors).</span></span>

## <a name="sending-the-location-of-the-upload-file-in-a-header"></a><span data-ttu-id="59ec3-108">Envoi de l’emplacement du fichier de téléchargement dans un en-tête</span><span class="sxs-lookup"><span data-stu-id="59ec3-108">Sending the location of the upload file in a header</span></span>

<span data-ttu-id="59ec3-109">BITS passe l’emplacement des fichiers de chargement et de réponse à l’application serveur dans les en-têtes si la propriété [BITSServerNotificationType](bits-iis-extension-properties.md) a la valeur 1.</span><span class="sxs-lookup"><span data-stu-id="59ec3-109">BITS passes the location of the upload and reply files to the server application in the headers if the [BITSServerNotificationType](bits-iis-extension-properties.md) property is set to 1.</span></span> <span data-ttu-id="59ec3-110">L’application serveur ouvre le fichier de téléchargement, traite les données, puis génère le fichier de réponse.</span><span class="sxs-lookup"><span data-stu-id="59ec3-110">The server application opens the upload file, processes the data, and then generates the reply file.</span></span> <span data-ttu-id="59ec3-111">Par défaut, le service BITS supprime les fichiers de chargement et de réponse du serveur après avoir reçu la réponse de l’application serveur.</span><span class="sxs-lookup"><span data-stu-id="59ec3-111">By default, BITS removes the upload and reply files from the server after it receives the response from the server application.</span></span> <span data-ttu-id="59ec3-112">Pour que le service BITS copie le fichier de téléchargement à l’emplacement spécifié par le nom de fichier distant dans le travail, incluez l’en-tête BITS-Copy-file-to-destination dans votre réponse.</span><span class="sxs-lookup"><span data-stu-id="59ec3-112">To have BITS copy the upload file to the location specified by the remote file name in the job, include the BITS-Copy-File-To-Destination header in your response.</span></span> <span data-ttu-id="59ec3-113">Si vous n’incluez pas l’en-tête et que vous souhaitez enregistrer les fichiers de téléchargement et de réponse, vous devez copier les fichiers de chargement et de réponse dans un nouvel emplacement avant de répondre.</span><span class="sxs-lookup"><span data-stu-id="59ec3-113">If you do not include the header and you want to save the upload and reply files, you must copy the upload and reply files to a new location before responding.</span></span> <span data-ttu-id="59ec3-114">Le tableau suivant présente les en-têtes de demande.</span><span class="sxs-lookup"><span data-stu-id="59ec3-114">The following table shows the request headers.</span></span>



| <span data-ttu-id="59ec3-115">En-tête de requête</span><span class="sxs-lookup"><span data-stu-id="59ec3-115">Request header</span></span>              | <span data-ttu-id="59ec3-116">Description</span><span class="sxs-lookup"><span data-stu-id="59ec3-116">Description</span></span>                                                                                |
|-----------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="59ec3-117">BITS-URL de requête d’origine</span><span class="sxs-lookup"><span data-stu-id="59ec3-117">BITS-Original-Request-URL</span></span>   | <span data-ttu-id="59ec3-118">Contient le nom distant spécifié dans le travail.</span><span class="sxs-lookup"><span data-stu-id="59ec3-118">Contains the remote name specified in the job.</span></span>                                             |
| <span data-ttu-id="59ec3-119">BITS-Request-DataFile-nom</span><span class="sxs-lookup"><span data-stu-id="59ec3-119">BITS-Request-DataFile-Name</span></span>  | <span data-ttu-id="59ec3-120">Contient le chemin d’accès complet aux données téléchargées.</span><span class="sxs-lookup"><span data-stu-id="59ec3-120">Contains the full path to the uploaded data.</span></span>                                               |
| <span data-ttu-id="59ec3-121">BIT-Response-DataFile-nom</span><span class="sxs-lookup"><span data-stu-id="59ec3-121">BITS-Response-DataFile-Name</span></span> | <span data-ttu-id="59ec3-122">Contient le chemin d’accès complet à l’emplacement où le service BITS s’attend à ce que l’application serveur écrive la réponse.</span><span class="sxs-lookup"><span data-stu-id="59ec3-122">Contains the full path to where BITS expects the server application to write the response.</span></span> |



 

<span data-ttu-id="59ec3-123">Le tableau suivant présente les en-têtes de réponse.</span><span class="sxs-lookup"><span data-stu-id="59ec3-123">The following table shows the response headers.</span></span>



| <span data-ttu-id="59ec3-124">En-tête de réponse</span><span class="sxs-lookup"><span data-stu-id="59ec3-124">Response header</span></span>               | <span data-ttu-id="59ec3-125">Description</span><span class="sxs-lookup"><span data-stu-id="59ec3-125">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59ec3-126">BITS-static-Response-URL</span><span class="sxs-lookup"><span data-stu-id="59ec3-126">BITS-Static-Response-URL</span></span>      | <span data-ttu-id="59ec3-127">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="59ec3-127">Optional.</span></span> <span data-ttu-id="59ec3-128">Contient l’URL absolue (ne spécifiez pas d’URL relative) à un fichier de données statiques à utiliser comme réponse.</span><span class="sxs-lookup"><span data-stu-id="59ec3-128">Contains the absolute URL (do not specify a relative URL) to a static data file to use as the response.</span></span> <span data-ttu-id="59ec3-129">Le fichier de données statique doit être accessible par le client BITS.</span><span class="sxs-lookup"><span data-stu-id="59ec3-129">The static data file must be accessible by the BITS client.</span></span> <span data-ttu-id="59ec3-130">Si vous utilisez cet en-tête, ne créez pas le fichier réponse spécifié dans l’en-tête de demande BITS-Response-DataFile-Name.</span><span class="sxs-lookup"><span data-stu-id="59ec3-130">If you use this header, do not create the response file specified in the BITS-Response-DataFile-Name request header.</span></span> <span data-ttu-id="59ec3-131">Notez que le service BITS ne supprime pas ce fichier pour vous.</span><span class="sxs-lookup"><span data-stu-id="59ec3-131">Note that BITS does not delete this file for you.</span></span><br/>                                                                                                           |
| <span data-ttu-id="59ec3-132">BITS-copier-fichier vers destination</span><span class="sxs-lookup"><span data-stu-id="59ec3-132">BITS-Copy-File-To-Destination</span></span> | <span data-ttu-id="59ec3-133">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="59ec3-133">Optional.</span></span> <span data-ttu-id="59ec3-134">Par défaut, si la propriété [BITSServerNotificationType](bits-iis-extension-properties.md) a la valeur 1 ou 2, le serveur bits ne copie pas le fichier de téléchargement à l’emplacement spécifié par le nom de fichier distant dans le travail.</span><span class="sxs-lookup"><span data-stu-id="59ec3-134">By default, if the [BITSServerNotificationType](bits-iis-extension-properties.md) property is set to 1 or 2, the BITS server does not copy the upload file to the location specified by the remote file name in the job.</span></span> <span data-ttu-id="59ec3-135">Pour que le service BITS copie le fichier à l’emplacement spécifié par le nom de fichier distant dans le travail, envoyez cet en-tête de réponse.</span><span class="sxs-lookup"><span data-stu-id="59ec3-135">To have BITS copy the file to the location specified by the remote file name in the job, send this response header.</span></span> <span data-ttu-id="59ec3-136">Vous pouvez spécifier n’importe quelle valeur ; BITS n’utilise pas la valeur.</span><span class="sxs-lookup"><span data-stu-id="59ec3-136">You can specify any value; BITS does not use the value.</span></span> <span data-ttu-id="59ec3-137">Notez que les dossiers dans le chemin d’accès du fichier distant doivent exister.</span><span class="sxs-lookup"><span data-stu-id="59ec3-137">Note that the folders in the remote file path must exist.</span></span> |



 

<span data-ttu-id="59ec3-138">La requête suivante montre les BITS envoyant l’emplacement du fichier de téléchargement à l’application serveur.</span><span class="sxs-lookup"><span data-stu-id="59ec3-138">The following request shows BITS sending the location of the upload file to the server application.</span></span>

``` syntax
POST https://myserver/myvdir/handle_upload.asp?ACCOUNT=873112 HTTP/1.1
Host: myserver
BITS-Original-Request-URL: https://front-end-server/vdir
BITS-Request-DataFile-Name: c:\physical-path\BITS-Sessions\{5e53c221-f2d6-4bf2-
b994-1dc43ceaca8d}\request
BITS-Response-DataFile-Name: c:\physical-path\BITS-Sessions\{5e53c221-f2d6-4bf2-
b994-1dc43ceaca8d}\response
Content-Length: 0
```

<span data-ttu-id="59ec3-139">L’exemple suivant montre la réponse de l’application serveur à BITS ; la réponse est placée dans le fichier spécifié par l’en-tête de demande BITS-Response-DataFile-Name.</span><span class="sxs-lookup"><span data-stu-id="59ec3-139">The following shows the server application's reply to BITS; the reply is placed in the file specified by the BITS-Response-DataFile-Name request header.</span></span>

``` syntax
HTTP/1.1 200 - OK
Content-Length: 0
```

## <a name="sending-the-upload-file-in-the-body-of-the-request"></a><span data-ttu-id="59ec3-140">Envoi du fichier de téléchargement dans le corps de la demande</span><span class="sxs-lookup"><span data-stu-id="59ec3-140">Sending the upload file in the body of the request</span></span>

<span data-ttu-id="59ec3-141">Le service BITS envoie le fichier de téléchargement dans le corps de la demande si la propriété [BITSServerNotificationType](bits-iis-extension-properties.md) a la valeur 2.</span><span class="sxs-lookup"><span data-stu-id="59ec3-141">BITS sends the upload file in the body of the request if the [BITSServerNotificationType](bits-iis-extension-properties.md) property is set to 2.</span></span> <span data-ttu-id="59ec3-142">L’envoi du fichier de téléchargement dans le corps de la demande permet aux scripts et applications existants de fonctionner avec un minimum de modifications.</span><span class="sxs-lookup"><span data-stu-id="59ec3-142">Sending the upload file in the body of the request lets existing scripts and applications work with minimal modifications.</span></span> <span data-ttu-id="59ec3-143">Le fichier de téléchargement et le fichier de réponse sont transmis dans la demande et la réponse, respectivement.</span><span class="sxs-lookup"><span data-stu-id="59ec3-143">The upload file and reply file are passed in the request and response, respectively.</span></span> <span data-ttu-id="59ec3-144">Le tableau suivant indique l’en-tête de demande.</span><span class="sxs-lookup"><span data-stu-id="59ec3-144">The following table shows the request header.</span></span>



| <span data-ttu-id="59ec3-145">En-tête de requête</span><span class="sxs-lookup"><span data-stu-id="59ec3-145">Request header</span></span>            | <span data-ttu-id="59ec3-146">Description</span><span class="sxs-lookup"><span data-stu-id="59ec3-146">Description</span></span>                                    |
|---------------------------|------------------------------------------------|
| <span data-ttu-id="59ec3-147">BITS-URL de requête d’origine</span><span class="sxs-lookup"><span data-stu-id="59ec3-147">BITS-Original-Request-URL</span></span> | <span data-ttu-id="59ec3-148">Contient le nom distant spécifié dans le travail.</span><span class="sxs-lookup"><span data-stu-id="59ec3-148">Contains the remote name specified in the job.</span></span> |



 

<span data-ttu-id="59ec3-149">Le tableau suivant présente les en-têtes de réponse.</span><span class="sxs-lookup"><span data-stu-id="59ec3-149">The following table shows the response headers.</span></span>



| <span data-ttu-id="59ec3-150">En-tête de réponse</span><span class="sxs-lookup"><span data-stu-id="59ec3-150">Response header</span></span>               | <span data-ttu-id="59ec3-151">Description</span><span class="sxs-lookup"><span data-stu-id="59ec3-151">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59ec3-152">BITS-static-Response-URL</span><span class="sxs-lookup"><span data-stu-id="59ec3-152">BITS-Static-Response-URL</span></span>      | <span data-ttu-id="59ec3-153">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="59ec3-153">Optional.</span></span> <span data-ttu-id="59ec3-154">Contient l’URL absolue (ne spécifiez pas d’URL relative) à un fichier de données statiques à utiliser comme réponse.</span><span class="sxs-lookup"><span data-stu-id="59ec3-154">Contains the absolute URL (do not specify a relative URL) to a static data file to use as the response.</span></span> <span data-ttu-id="59ec3-155">Le fichier de données statique doit être accessible par le client BITS.</span><span class="sxs-lookup"><span data-stu-id="59ec3-155">The static data file must be accessible by the BITS client.</span></span> <span data-ttu-id="59ec3-156">Si vous utilisez cet en-tête, n’incluez pas la réponse dans le flux.</span><span class="sxs-lookup"><span data-stu-id="59ec3-156">If you use this header, do not include the response in the stream.</span></span> <span data-ttu-id="59ec3-157">Notez que le service BITS ne supprime pas ce fichier pour vous.</span><span class="sxs-lookup"><span data-stu-id="59ec3-157">Note that BITS does not delete this file for you.</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="59ec3-158">BITS-copier-fichier vers destination</span><span class="sxs-lookup"><span data-stu-id="59ec3-158">BITS-Copy-File-To-Destination</span></span> | <span data-ttu-id="59ec3-159">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="59ec3-159">Optional.</span></span> <span data-ttu-id="59ec3-160">Si la propriété [BITSServerNotificationType](bits-iis-extension-properties.md) a la valeur 1 ou 2, le serveur bits ne copie pas le fichier de téléchargement à l’emplacement spécifié par le nom de fichier distant dans le travail.</span><span class="sxs-lookup"><span data-stu-id="59ec3-160">If the [BITSServerNotificationType](bits-iis-extension-properties.md) property is set to 1 or 2, the BITS server does not copy the upload file to the location specified by the remote file name in the job.</span></span> <span data-ttu-id="59ec3-161">Pour que le service BITS copie le fichier à l’emplacement spécifié par le nom de fichier distant, envoyez cet en-tête de réponse.</span><span class="sxs-lookup"><span data-stu-id="59ec3-161">To have BITS copy the file to the location specified by the remote file name, send this response header.</span></span> <span data-ttu-id="59ec3-162">Vous pouvez spécifier n’importe quelle valeur ; BITS n’utilise pas la valeur.</span><span class="sxs-lookup"><span data-stu-id="59ec3-162">You can specify any value; BITS does not use the value.</span></span> <span data-ttu-id="59ec3-163">Notez que les dossiers dans le chemin d’accès du fichier distant doivent exister.</span><span class="sxs-lookup"><span data-stu-id="59ec3-163">Note that the folders in the remote file path must exist.</span></span> |



 

<span data-ttu-id="59ec3-164">La requête suivante montre les BITS qui passent le fichier téléchargé à l’application serveur dans le corps de la requête.</span><span class="sxs-lookup"><span data-stu-id="59ec3-164">The following request shows BITS passing the uploaded file to the server application in the body of the request.</span></span>

``` syntax
POST https://myserver/myvdir/handle_upload.asp?ACCOUNT=873112 HTTP/1.1
Host: myserver
BITS-Original-Request-URL: https://front-end-server/vdir
Content-Length: 80000

80000 bytes of upload data goes here
```

<span data-ttu-id="59ec3-165">La réponse suivante montre l’application serveur qui transmet les données de réponse à BITS dans le corps de la réponse.</span><span class="sxs-lookup"><span data-stu-id="59ec3-165">The following reply shows the server application passing the reply data to BITS in the body of the response.</span></span>

``` syntax
HTTP/1.1 200 - OK
Content-Length: 100

100 bytes of reply data goes here
```

## <a name="handling-server-application-errors"></a><span data-ttu-id="59ec3-166">Gestion des erreurs d’application serveur</span><span class="sxs-lookup"><span data-stu-id="59ec3-166">Handling server application errors</span></span>

<span data-ttu-id="59ec3-167">Consultez [gestion des erreurs d’application serveur](handling-server-application-errors.md).</span><span class="sxs-lookup"><span data-stu-id="59ec3-167">See [Handling Server Application Errors](handling-server-application-errors.md).</span></span>

 

 





