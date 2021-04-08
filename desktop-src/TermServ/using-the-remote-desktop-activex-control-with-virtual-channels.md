---
title: Utilisation du contrôle ActiveX Bureau à distance avec des canaux virtuels
description: Si vous avez activé une application de canaux virtuels dans votre déploiement Services Bureau à distance, vous pouvez mettre cette application à la disposition des ordinateurs clients.
ms.assetid: df537ffb-41dd-400e-8a49-9d8a10734eda
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 026c8fa23f1498270bd0d2a29c5f48d50f0b2463
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840173"
---
# <a name="using-the-remote-desktop-activex-control-with-virtual-channels"></a>Utilisation du contrôle ActiveX Bureau à distance avec des canaux virtuels

Si vous avez activé une application de canaux virtuels dans votre déploiement Services Bureau à distance, vous pouvez mettre cette application à la disposition des ordinateurs clients qui accèdent au serveur de l’hôte de session Bureau à distance (hôte de session Bureau à distance) au moyen du contrôle ActiveX Bureau à distance.

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

L’API de canal virtuel ne permet pas de charger plusieurs instances de la même DLL de canal virtuel au sein d’un même processus. Pour cette raison, si plusieurs instances du Bureau à distance contrôle ActiveX s’exécutent dans le même processus, seule la première instance du contrôle sera en mesure de charger la DLL du canal virtuel. Si vous concevez une application de canal virtuel qui doit prendre en charge plusieurs instances au sein d’un même processus, vous devez utiliser l’API [canaux virtuels dynamiques](dynamic-virtual-channels.md) pour implémenter votre application de canal virtuel.

> [!Note]  
> Par défaut, le contrôle ActiveX Bureau à distance charge les dll du client de canal virtuel à partir du répertoire% windir% \\ system32. Il est possible pour un administrateur de modifier ce répertoire DLL de plug-in client par défaut. Pour ce faire, modifiez la clé de Registre **HKEY \_ local \_ machine** \\ **Software** \\ **Microsoft** \\ **Terminal Server client** \\ **vdllpath** sur l’ordinateur client. Ce chemin d’accès de répertoire ne peut pas être spécifié au format UNC.

 

 

 




