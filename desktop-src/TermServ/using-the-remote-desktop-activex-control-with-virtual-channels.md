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
# <a name="using-the-remote-desktop-activex-control-with-virtual-channels"></a><span data-ttu-id="00af9-103">Utilisation du contrôle ActiveX Bureau à distance avec des canaux virtuels</span><span class="sxs-lookup"><span data-stu-id="00af9-103">Using the Remote Desktop ActiveX control with virtual channels</span></span>

<span data-ttu-id="00af9-104">Si vous avez activé une application de canaux virtuels dans votre déploiement Services Bureau à distance, vous pouvez mettre cette application à la disposition des ordinateurs clients qui accèdent au serveur de l’hôte de session Bureau à distance (hôte de session Bureau à distance) au moyen du contrôle ActiveX Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="00af9-104">If you have enabled a virtual channels application in your Remote Desktop Services deployment, you can make this application available to client computers that access the Remote Desktop Session Host (RD Session Host) server by means of the Remote Desktop ActiveX control.</span></span>

<span data-ttu-id="00af9-105">**Pour rendre une application de canal virtuel disponible**</span><span class="sxs-lookup"><span data-stu-id="00af9-105">**To make a virtual channel application available**</span></span>

1.  <span data-ttu-id="00af9-106">Déployez le module côté serveur de l’application et assurez-vous qu’il s’exécute sur le serveur hôte de session Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="00af9-106">Deploy the server-side module of the application and make sure it is running on the RD Session Host server.</span></span> <span data-ttu-id="00af9-107">Dans la page connexion de l’application Web Services Bureau à distance s’exécutant sur votre serveur Web, accédez à la propriété **PluginDlls** de l’interface [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) pour spécifier le nom de votre dll de canal virtuel.</span><span class="sxs-lookup"><span data-stu-id="00af9-107">In the connection page of the Remote Desktop Services web application running on your web server, access the **PluginDlls** property of the [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) interface to specify the name of your virtual channel DLL.</span></span> <span data-ttu-id="00af9-108">Si vous disposez de plusieurs plug-ins, spécifiez une liste délimitée par des virgules de noms de DLL.</span><span class="sxs-lookup"><span data-stu-id="00af9-108">If you have more than one plug-in, specify a comma-delimited list of DLL names.</span></span> <span data-ttu-id="00af9-109">Par exemple, si le plug-in de votre canal virtuel est nommé « MyPlugin.dll », utilisez le code suivant :</span><span class="sxs-lookup"><span data-stu-id="00af9-109">For instance, if your virtual channel plug-in is named "MyPlugin.dll", use the following code:</span></span>

    ``` syntax
    MsRdpClient.AdvancedSettings.PluginDlls = "myplugin.dll"
    ```

    <span data-ttu-id="00af9-110">Utilisez le code suivant si vous avez deux dll de canal virtuel.</span><span class="sxs-lookup"><span data-stu-id="00af9-110">Use the following code if you have two virtual channel DLLs.</span></span> <span data-ttu-id="00af9-111">Dans cet exemple, les noms de fichier DLL sont « MyPlugin.dll » et « Vdriver.dll » :</span><span class="sxs-lookup"><span data-stu-id="00af9-111">In this example, the DLL file names are "MyPlugin.dll" and "Vdriver.dll":</span></span>

    ``` syntax
    MsRdpClient.AdvancedSettings.PluginDlls = "myplugin.dll,Vdriver.dll"
    ```

    <span data-ttu-id="00af9-112">Pour des raisons de sécurité, la propriété **PluginDlls** accepte uniquement une liste nommée de dll de canal virtuel.</span><span class="sxs-lookup"><span data-stu-id="00af9-112">For security reasons, the **PluginDlls** property only accepts a named list of virtual channel DLLs.</span></span> <span data-ttu-id="00af9-113">Le contrôle retourne une erreur si une forme de système de fichiers ou un chemin d’accès UNC est spécifié.</span><span class="sxs-lookup"><span data-stu-id="00af9-113">The control returns an error if any form of file system or UNC path is specified.</span></span> <span data-ttu-id="00af9-114">En outre, les noms des dll doivent contenir uniquement des caractères alphanumériques.</span><span class="sxs-lookup"><span data-stu-id="00af9-114">In addition, the names of the DLLs must contain only alphanumeric characters.</span></span>

2.  <span data-ttu-id="00af9-115">Assurez-vous que le module côté client est installé dans le répertoire% windir% \\ system32.</span><span class="sxs-lookup"><span data-stu-id="00af9-115">Ensure that the client-side module is installed in the %windir%\\system32 directory.</span></span>

<span data-ttu-id="00af9-116">L’API de canal virtuel ne permet pas de charger plusieurs instances de la même DLL de canal virtuel au sein d’un même processus.</span><span class="sxs-lookup"><span data-stu-id="00af9-116">The virtual channel API does not allow for multiple instances of the same virtual channel DLL to be loaded within a single process.</span></span> <span data-ttu-id="00af9-117">Pour cette raison, si plusieurs instances du Bureau à distance contrôle ActiveX s’exécutent dans le même processus, seule la première instance du contrôle sera en mesure de charger la DLL du canal virtuel.</span><span class="sxs-lookup"><span data-stu-id="00af9-117">Because of this, if there are multiple instances of the Remote Desktop ActiveX control running within the same process, only the first instance of the control will be able to load the virtual channel DLL.</span></span> <span data-ttu-id="00af9-118">Si vous concevez une application de canal virtuel qui doit prendre en charge plusieurs instances au sein d’un même processus, vous devez utiliser l’API [canaux virtuels dynamiques](dynamic-virtual-channels.md) pour implémenter votre application de canal virtuel.</span><span class="sxs-lookup"><span data-stu-id="00af9-118">If you are designing a virtual channel application that must support multiple instances within a single process, you must use the [Dynamic Virtual Channels](dynamic-virtual-channels.md) API to implement your virtual channel application.</span></span>

> [!Note]  
> <span data-ttu-id="00af9-119">Par défaut, le contrôle ActiveX Bureau à distance charge les dll du client de canal virtuel à partir du répertoire% windir% \\ system32.</span><span class="sxs-lookup"><span data-stu-id="00af9-119">By default, the Remote Desktop ActiveX control loads virtual channel client DLLs from the %windir%\\system32 directory.</span></span> <span data-ttu-id="00af9-120">Il est possible pour un administrateur de modifier ce répertoire DLL de plug-in client par défaut.</span><span class="sxs-lookup"><span data-stu-id="00af9-120">It is possible for an administrator to change this default client plug-in DLL directory.</span></span> <span data-ttu-id="00af9-121">Pour ce faire, modifiez la clé de Registre **HKEY \_ local \_ machine** \\ **Software** \\ **Microsoft** \\ **Terminal Server client** \\ **vdllpath** sur l’ordinateur client.</span><span class="sxs-lookup"><span data-stu-id="00af9-121">To do so, edit the **HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**Terminal Server Client**\\**vdllpath** registry key on the client computer.</span></span> <span data-ttu-id="00af9-122">Ce chemin d’accès de répertoire ne peut pas être spécifié au format UNC.</span><span class="sxs-lookup"><span data-stu-id="00af9-122">This directory path cannot be specified in the UNC format.</span></span>

 

 

 




