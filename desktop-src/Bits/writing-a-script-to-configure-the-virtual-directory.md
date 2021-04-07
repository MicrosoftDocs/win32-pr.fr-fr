---
title: Écriture d’un script pour configurer le répertoire virtuel
description: Écriture d’un script pour configurer le répertoire virtuel
ms.assetid: 0324fbc8-1d64-454c-b021-4e010edcac8d
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ae23a33c2c91dc0a141c6f377daf89708499aae7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939661"
---
# <a name="writing-a-script-to-configure-the-virtual-directory"></a><span data-ttu-id="1e5ac-103">Écriture d’un script pour configurer le répertoire virtuel</span><span class="sxs-lookup"><span data-stu-id="1e5ac-103">Writing a Script to Configure the Virtual Directory</span></span>

<span data-ttu-id="1e5ac-104">Vous pouvez utiliser les valeurs de propriété IIS BITS par défaut pour télécharger un fichier sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="1e5ac-104">You can use the default BITS IIS property values to upload a file to the server.</span></span> <span data-ttu-id="1e5ac-105">Le fichier de chargement est écrit dans l’URL, tel que spécifié dans le nom de fichier distant du travail.</span><span class="sxs-lookup"><span data-stu-id="1e5ac-105">The upload file is written to the URL as specified in the remote file name of the job.</span></span> <span data-ttu-id="1e5ac-106">Pour charger le fichier dans une application serveur et recevoir une réponse, modifiez la propriété [BITSServerNotificationType](bits-iis-extension-properties.md) pour envoyer les données par référence (envoie le nom du fichier qui contient les données) ou par valeur (envoie les données dans le corps de la demande).</span><span class="sxs-lookup"><span data-stu-id="1e5ac-106">To upload the file to a server application and receive a reply, change the [BITSServerNotificationType](bits-iis-extension-properties.md) property to send the data by reference (sends the name of the file that contains the data) or by value (sends the data in the body of the request).</span></span>

<span data-ttu-id="1e5ac-107">Pour obtenir une liste et une description des propriétés que vous pouvez modifier, consultez [propriétés d’extension IIS bits](bits-iis-extension-properties.md).</span><span class="sxs-lookup"><span data-stu-id="1e5ac-107">For a list and description of the properties that you can modify, see [BITS IIS Extension Properties](bits-iis-extension-properties.md).</span></span> <span data-ttu-id="1e5ac-108">Utilisez les méthodes de l’interface [**IBITSExtensionSetup**](/windows/desktop/api/Bitscfg/nn-bitscfg-ibitsextensionsetup) pour activer et désactiver le répertoire virtuel pour les téléchargements.</span><span class="sxs-lookup"><span data-stu-id="1e5ac-108">Use the methods of the [**IBITSExtensionSetup**](/windows/desktop/api/Bitscfg/nn-bitscfg-ibitsextensionsetup) interface to enable and disable the virtual directory for uploads.</span></span>

<span data-ttu-id="1e5ac-109">L’exemple suivant montre comment utiliser Windows Script Host pour créer, configurer et activer un répertoire virtuel IIS pour les téléchargements BITS.</span><span class="sxs-lookup"><span data-stu-id="1e5ac-109">The following example shows how to use Windows Script Host to create, configure, and enable an IIS virtual directory for BITS uploads.</span></span>


```JScript
if (WScript.Arguments.length < 2)
{
    WScript.Echo("Usage: bitsvdir virtual_directory local_directory");
    WScript.Quit(1);
}

VirtualDirectoryName = WScript.Arguments(0);
LocalDirectoryName = WScript.Arguments(1);

ServerObj = GetObject("IIS://LocalHost/W3SVC/1/ROOT");
VirtualDir = ServerObj.Create("IIsWebVirtualDir", VirtualDirectoryName );

VirtualDir.Path = LocalDirectoryName;
VirtualDir.AppIsolated = 0;
VirtualDir.AccessScript = true;
VirtualDir.AccessRead = false;
VirtualDir.AccessWrite = false;
VirtualDir.SetInfo();

//Set BITS specific IIS configuration settings
VirtualDir.EnableBITSUploads();
VirtualDir.BITSMaximumUploadSize = "4294967296";
VirtualDir.SetInfo();

WScript.Echo( "Created virtual directory " + VirtualDirectoryName + 
              " with a local directory of " + LocalDirectoryName );
WScript.Quit( 0 );
```



<span data-ttu-id="1e5ac-110">Pour modifier l’exemple précédent en vue de télécharger les données vers une application serveur, ajoutez le code suivant avant **setinfo**.</span><span class="sxs-lookup"><span data-stu-id="1e5ac-110">To change the previous example to upload the data to a server application, add the following code before **SetInfo**.</span></span>


```JScript
VirtualDir.BITSServerNotificationType = 1;
VirtualDir.BITSServerNotificationURL = "https://myserver/mypath/myasp.asp";
```



<span data-ttu-id="1e5ac-111">L’emplacement du fichier de téléchargement est transmis à l’application serveur, myasp. asp, dans l’en-tête BITS-Request-DataFile-Name.</span><span class="sxs-lookup"><span data-stu-id="1e5ac-111">The location of the upload file is passed to the server application, myasp.asp, in the BITS-Request-DataFile-Name header.</span></span> <span data-ttu-id="1e5ac-112">Pour recevoir le fichier de téléchargement dans le corps de la demande, affectez à la propriété [BITSServerNotificationType](bits-iis-extension-properties.md) la valeur 2.</span><span class="sxs-lookup"><span data-stu-id="1e5ac-112">To receive the upload file in the body of the request, set the [BITSServerNotificationType](bits-iis-extension-properties.md) property to 2.</span></span>

<span data-ttu-id="1e5ac-113">Pour plus d’informations sur la réception des données de téléchargement dans votre application serveur, consultez [utilisation des en-têtes de demande de notification bits/réponse](using-bits-notification-request-response-headers.md).</span><span class="sxs-lookup"><span data-stu-id="1e5ac-113">For information on receiving the upload data in your server application, see [Using BITS Notification Request/Response Headers](using-bits-notification-request-response-headers.md).</span></span>

 

 




