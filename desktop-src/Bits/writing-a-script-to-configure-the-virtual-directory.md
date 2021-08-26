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
ms.openlocfilehash: b9ea1de5a0b9f7be9598a4011cbb6cd76f49e6d4bcc3d468093be1479ee2b59e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004599"
---
# <a name="writing-a-script-to-configure-the-virtual-directory"></a>Écriture d’un script pour configurer le répertoire virtuel

Vous pouvez utiliser les valeurs de propriété IIS BITS par défaut pour télécharger un fichier sur le serveur. Le fichier de chargement est écrit dans l’URL, tel que spécifié dans le nom de fichier distant du travail. Pour charger le fichier dans une application serveur et recevoir une réponse, modifiez la propriété [BITSServerNotificationType](bits-iis-extension-properties.md) pour envoyer les données par référence (envoie le nom du fichier qui contient les données) ou par valeur (envoie les données dans le corps de la demande).

Pour obtenir une liste et une description des propriétés que vous pouvez modifier, consultez [propriétés d’extension IIS bits](bits-iis-extension-properties.md). Utilisez les méthodes de l’interface [**IBITSExtensionSetup**](/windows/desktop/api/Bitscfg/nn-bitscfg-ibitsextensionsetup) pour activer et désactiver le répertoire virtuel pour les téléchargements.

l’exemple suivant montre comment utiliser Windows Script Host pour créer, configurer et activer un répertoire virtuel IIS pour les téléchargements BITS.


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



Pour modifier l’exemple précédent en vue de télécharger les données vers une application serveur, ajoutez le code suivant avant **setinfo**.


```JScript
VirtualDir.BITSServerNotificationType = 1;
VirtualDir.BITSServerNotificationURL = "https://myserver/mypath/myasp.asp";
```



L’emplacement du fichier de téléchargement est transmis à l’application serveur, myasp. asp, dans l’en-tête BITS-Request-DataFile-Name. Pour recevoir le fichier de téléchargement dans le corps de la demande, affectez à la propriété [BITSServerNotificationType](bits-iis-extension-properties.md) la valeur 2.

Pour plus d’informations sur la réception des données de téléchargement dans votre application serveur, consultez [utilisation des en-têtes de demande de notification bits/réponse](using-bits-notification-request-response-headers.md).

 

 




