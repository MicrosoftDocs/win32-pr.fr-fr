---
title: utilisation du contrôle Bureau à distance ActiveX avec des canaux virtuels
description: Si vous avez activé une application de canaux virtuels dans votre déploiement Services Bureau à distance, vous pouvez mettre cette application à la disposition des ordinateurs clients.
ms.assetid: df537ffb-41dd-400e-8a49-9d8a10734eda
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dae33c059a84422788bc49d47f95e0011f78930054ed3884669e8f35763461b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119868729"
---
# <a name="using-the-remote-desktop-activex-control-with-virtual-channels"></a>utilisation du contrôle Bureau à distance ActiveX avec des canaux virtuels

si vous avez activé une application de canaux virtuels dans votre déploiement Services Bureau à distance, vous pouvez mettre cette application à la disposition des ordinateurs clients qui accèdent au serveur de l’hôte de session Bureau à distance (hôte de session bureau à distance) au moyen du contrôle de ActiveX Bureau à distance.

**Pour rendre une application de canal virtuel disponible**

1.  Déployez le module côté serveur de l’application et assurez-vous qu’il s’exécute sur le serveur hôte de session Bureau à distance. Dans la page connexion de l’application Web Services Bureau à distance s’exécutant sur votre serveur Web, accédez à la propriété **PluginDlls** de l’interface [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) pour spécifier le nom de votre dll de canal virtuel. Si vous disposez de plusieurs plug-ins, spécifiez une liste délimitée par des virgules de noms de DLL. Par exemple, si le plug-in de votre canal virtuel est nommé « MyPlugin.dll », utilisez le code suivant :

    ``` syntax
    MsRdpClient.AdvancedSettings.PluginDlls = "myplugin.dll"
    ```

    Utilisez le code suivant si vous avez deux dll de canal virtuel. Dans cet exemple, les noms de fichier DLL sont « MyPlugin.dll » et « Vdriver.dll » :

    ``` syntax
    MsRdpClient.AdvancedSettings.PluginDlls = "myplugin.dll,Vdriver.dll"
    ```

    Pour des raisons de sécurité, la propriété **PluginDlls** accepte uniquement une liste nommée de dll de canal virtuel. Le contrôle retourne une erreur si une forme de système de fichiers ou un chemin d’accès UNC est spécifié. En outre, les noms des dll doivent contenir uniquement des caractères alphanumériques.

2.  Assurez-vous que le module côté client est installé dans le répertoire% windir% \\ system32.

L’API de canal virtuel ne permet pas de charger plusieurs instances de la même DLL de canal virtuel au sein d’un même processus. pour cette raison, s’il existe plusieurs instances du Bureau à distance ActiveX contrôle s’exécutant dans le même processus, seule la première instance du contrôle sera en mesure de charger la DLL du canal virtuel. Si vous concevez une application de canal virtuel qui doit prendre en charge plusieurs instances au sein d’un même processus, vous devez utiliser l’API [canaux virtuels dynamiques](dynamic-virtual-channels.md) pour implémenter votre application de canal virtuel.

> [!Note]  
> par défaut, le contrôle Bureau à distance ActiveX charge les dll du client du canal virtuel à partir du répertoire% windir% \\ system32. Il est possible pour un administrateur de modifier ce répertoire DLL de plug-in client par défaut. Pour ce faire, modifiez la clé de Registre **HKEY \_ local \_ machine** \\ **Software** \\ **Microsoft** \\ **Terminal Server client** \\ **vdllpath** sur l’ordinateur client. Ce chemin d’accès de répertoire ne peut pas être spécifié au format UNC.

 

 

 




