---
title: Protocole de notification pour les applications serveur
description: BITS utilise la propriété BITSServerNotificationType pour déterminer la façon dont le service BITS envoie le contenu du fichier de téléchargement à l’application serveur.
ms.assetid: d5193d0c-3ab4-47ab-a570-fea2904a4371
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a54e859730acaa1456624e9fa5c2302bc36efd9d085daeecdf234aef8f74729c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004939"
---
# <a name="notification-protocol-for-server-applications"></a>Protocole de notification pour les applications serveur

BITS utilise la propriété [BITSServerNotificationType](bits-iis-extension-properties.md) pour déterminer la façon dont le service bits envoie le contenu du fichier de téléchargement à l’application serveur. Si la propriété BITSServerNotificationType a la valeur 1, [bits passe l’emplacement du fichier de téléchargement dans un en-tête](#sending-the-location-of-the-upload-file-in-a-header). Si la propriété BITSServerNotificationType a la valeur 2, [bits passe le contenu du fichier de téléchargement dans le corps de la demande](#sending-the-upload-file-in-the-body-of-the-request).

Pour plus d’informations sur la façon dont BITS gère les erreurs de l’application serveur, consultez [gestion des erreurs d’application serveur](#handling-server-application-errors).

## <a name="sending-the-location-of-the-upload-file-in-a-header"></a>Envoi de l’emplacement du fichier de téléchargement dans un en-tête

BITS passe l’emplacement des fichiers de chargement et de réponse à l’application serveur dans les en-têtes si la propriété [BITSServerNotificationType](bits-iis-extension-properties.md) a la valeur 1. L’application serveur ouvre le fichier de téléchargement, traite les données, puis génère le fichier de réponse. Par défaut, le service BITS supprime les fichiers de chargement et de réponse du serveur après avoir reçu la réponse de l’application serveur. Pour que le service BITS copie le fichier de téléchargement à l’emplacement spécifié par le nom de fichier distant dans le travail, incluez l’en-tête BITS-Copy-file-to-destination dans votre réponse. Si vous n’incluez pas l’en-tête et que vous souhaitez enregistrer les fichiers de téléchargement et de réponse, vous devez copier les fichiers de chargement et de réponse dans un nouvel emplacement avant de répondre. Le tableau suivant présente les en-têtes de demande.



| En-tête de requête              | Description                                                                                |
|-----------------------------|--------------------------------------------------------------------------------------------|
| BITS-URL de requête d’origine   | Contient le nom distant spécifié dans le travail.                                             |
| BITS-Request-DataFile-nom  | Contient le chemin d’accès complet aux données téléchargées.                                               |
| BIT-Response-DataFile-nom | Contient le chemin d’accès complet à l’emplacement où le service BITS s’attend à ce que l’application serveur écrive la réponse. |



 

Le tableau suivant présente les en-têtes de réponse.



| En-tête de réponse               | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BITS-static-Response-URL      | Facultatif. Contient l’URL absolue (ne spécifiez pas d’URL relative) à un fichier de données statiques à utiliser comme réponse. Le fichier de données statique doit être accessible par le client BITS. Si vous utilisez cet en-tête, ne créez pas le fichier réponse spécifié dans l’en-tête de demande BITS-Response-DataFile-Name. Notez que le service BITS ne supprime pas ce fichier pour vous.<br/>                                                                                                           |
| BITS-copier-fichier vers destination | Facultatif. Par défaut, si la propriété [BITSServerNotificationType](bits-iis-extension-properties.md) a la valeur 1 ou 2, le serveur bits ne copie pas le fichier de téléchargement à l’emplacement spécifié par le nom de fichier distant dans le travail. Pour que le service BITS copie le fichier à l’emplacement spécifié par le nom de fichier distant dans le travail, envoyez cet en-tête de réponse. Vous pouvez spécifier n’importe quelle valeur ; BITS n’utilise pas la valeur. Notez que les dossiers dans le chemin d’accès du fichier distant doivent exister. |



 

La requête suivante montre les BITS envoyant l’emplacement du fichier de téléchargement à l’application serveur.

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

L’exemple suivant montre la réponse de l’application serveur à BITS ; la réponse est placée dans le fichier spécifié par l’en-tête de demande BITS-Response-DataFile-Name.

``` syntax
HTTP/1.1 200 - OK
Content-Length: 0
```

## <a name="sending-the-upload-file-in-the-body-of-the-request"></a>Envoi du fichier de téléchargement dans le corps de la demande

Le service BITS envoie le fichier de téléchargement dans le corps de la demande si la propriété [BITSServerNotificationType](bits-iis-extension-properties.md) a la valeur 2. L’envoi du fichier de téléchargement dans le corps de la demande permet aux scripts et applications existants de fonctionner avec un minimum de modifications. Le fichier de téléchargement et le fichier de réponse sont transmis dans la demande et la réponse, respectivement. Le tableau suivant indique l’en-tête de demande.



| En-tête de requête            | Description                                    |
|---------------------------|------------------------------------------------|
| BITS-URL de requête d’origine | Contient le nom distant spécifié dans le travail. |



 

Le tableau suivant présente les en-têtes de réponse.



| En-tête de réponse               | Description                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BITS-static-Response-URL      | Facultatif. Contient l’URL absolue (ne spécifiez pas d’URL relative) à un fichier de données statiques à utiliser comme réponse. Le fichier de données statique doit être accessible par le client BITS. Si vous utilisez cet en-tête, n’incluez pas la réponse dans le flux. Notez que le service BITS ne supprime pas ce fichier pour vous.<br/>                                                                                                                                      |
| BITS-copier-fichier vers destination | Facultatif. Si la propriété [BITSServerNotificationType](bits-iis-extension-properties.md) a la valeur 1 ou 2, le serveur bits ne copie pas le fichier de téléchargement à l’emplacement spécifié par le nom de fichier distant dans le travail. Pour que le service BITS copie le fichier à l’emplacement spécifié par le nom de fichier distant, envoyez cet en-tête de réponse. Vous pouvez spécifier n’importe quelle valeur ; BITS n’utilise pas la valeur. Notez que les dossiers dans le chemin d’accès du fichier distant doivent exister. |



 

La requête suivante montre les BITS qui passent le fichier téléchargé à l’application serveur dans le corps de la requête.

``` syntax
POST https://myserver/myvdir/handle_upload.asp?ACCOUNT=873112 HTTP/1.1
Host: myserver
BITS-Original-Request-URL: https://front-end-server/vdir
Content-Length: 80000

80000 bytes of upload data goes here
```

La réponse suivante montre l’application serveur qui transmet les données de réponse à BITS dans le corps de la réponse.

``` syntax
HTTP/1.1 200 - OK
Content-Length: 100

100 bytes of reply data goes here
```

## <a name="handling-server-application-errors"></a>Gestion des erreurs d’application serveur

Consultez [gestion des erreurs d’application serveur](handling-server-application-errors.md).

 

 





