---
title: Inscription du plug-in DVC
description: Décrit la syntaxe de l’entrée de plug-in de canal virtuel dynamique (DVC) pour le client Connexion Bureau à distance (RDC).
ms.assetid: cda4f8c9-867a-41ac-894a-4296d5912b2b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 183c73f5f9dda0321640119b2750776d207973cc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106511314"
---
# <a name="dvc-plug-in-registration"></a><span data-ttu-id="ab1cc-103">Inscription du plug-in DVC</span><span class="sxs-lookup"><span data-stu-id="ab1cc-103">DVC plug-in registration</span></span>

<span data-ttu-id="ab1cc-104">Le plug-in de canal virtuel dynamique (DVC) est inscrit pour une utilisation par le client Connexion Bureau à distance (RDC) à l’aide de l’une des méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="ab1cc-104">The dynamic virtual channel (DVC) plug-in is registered for use by the Remote Desktop Connection (RDC) client using one of the following methods:</span></span>

-   <span data-ttu-id="ab1cc-105">Appel de la méthode [**IMsTscAdvancedSettings ::p ut \_ PluginDlls**](imstscadvancedsettings-plugindlls.md) du contrôle ActiveX protocole RDP (Remote Desktop Protocol) (RDP).</span><span class="sxs-lookup"><span data-stu-id="ab1cc-105">Invoking the [**IMsTscAdvancedSettings::put\_PluginDlls**](imstscadvancedsettings-plugindlls.md) method of the Remote Desktop Protocol (RDP) ActiveX control.</span></span> <span data-ttu-id="ab1cc-106">Les entrées multiples doivent être séparées par des virgules.</span><span class="sxs-lookup"><span data-stu-id="ab1cc-106">Multiple entries must be comma separated.</span></span>
-   <span data-ttu-id="ab1cc-107">Écriture de l’entrée de plug-in à l’emplacement suivant dans le registre sur l’ordinateur où est démarré le processus client Connexion Bureau à distance (RDC) :</span><span class="sxs-lookup"><span data-stu-id="ab1cc-107">Writing the plug-in entry to the following location in the registry on the computer where the Remote Desktop Connection (RDC) client process is started:</span></span>

    <span data-ttu-id="ab1cc-108">**HKEY \_ \_** \\  \\  \\  \\  \\  \\ ***Nom du plug-*** in par défaut des compléments Microsoft Terminal Server client du logiciel utilisateur actuel</span><span class="sxs-lookup"><span data-stu-id="ab1cc-108">**HKEY\_CURRENT\_USER**\\**Software**\\**Microsoft**\\**Terminal Server Client**\\**Default**\\**AddIns**\\***unique plug-in name***</span></span>

    > [!Note]  
    > <span data-ttu-id="ab1cc-109">Vous devez créer la sous-clé *de nom de plug-in unique* si elle n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="ab1cc-109">You must create the *unique plug-in name* subkey if it does not exist.</span></span> <span data-ttu-id="ab1cc-110">Le nom de la sous-clé du *nom de plug-in unique* est une chaîne arbitraire qui peut identifier le plug-in.</span><span class="sxs-lookup"><span data-stu-id="ab1cc-110">The *unique plug-in name* subkey name is an arbitrary string that can identify the plug-in.</span></span> <span data-ttu-id="ab1cc-111">La chaîne peut être n’importe quelle combinaison de caractères.</span><span class="sxs-lookup"><span data-stu-id="ab1cc-111">The string can be any combination of characters.</span></span>

     

    <span data-ttu-id="ab1cc-112">Sous *nom de plug-in unique*, vous devez ajouter une entrée qui identifie le plug-in.</span><span class="sxs-lookup"><span data-stu-id="ab1cc-112">Under *unique plug-in name*, you must add an entry that identifies the plug-in.</span></span>

    <span data-ttu-id="ab1cc-113">Nom de l’entrée = **nom**</span><span class="sxs-lookup"><span data-stu-id="ab1cc-113">Entry name = **Name**</span></span>

    <span data-ttu-id="ab1cc-114">Type de données = **reg \_ SZ** ou **reg \_ expand \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="ab1cc-114">Data type = **REG\_SZ** or **REG\_EXPAND\_SZ**</span></span>

<span data-ttu-id="ab1cc-115">Dans les deux cas, la valeur d’entrée doit être conforme à l’un des formats suivants :</span><span class="sxs-lookup"><span data-stu-id="ab1cc-115">In both cases, the entry value must conform to one of the following formats:</span></span>

<dl> <dt>

<span data-ttu-id="ab1cc-116"><span id="Plug-inDLLName__CLSID_"></span><span id="plug-indllname__clsid_"></span><span id="PLUG-INDLLNAME__CLSID_"></span>«*Plug-inDLLName*: {*CLSID*} »</span><span class="sxs-lookup"><span data-stu-id="ab1cc-116"><span id="Plug-inDLLName__CLSID_"></span><span id="plug-indllname__clsid_"></span><span id="PLUG-INDLLNAME__CLSID_"></span>"*Plug-inDLLName*:{*CLSID*}"</span></span>
</dt> <dd>

<span data-ttu-id="ab1cc-117">Le plug-in n’est pas nécessairement inscrit dans le Registre Windows en tant qu’objet COM (Component Object Model), mais la DLL est implémentée en tant qu’objet COM in-process.</span><span class="sxs-lookup"><span data-stu-id="ab1cc-117">The plug-in is not necessarily registered in the Windows registry as a Component Object Model (COM) object, but the DLL is implemented as an in-process COM object.</span></span> <span data-ttu-id="ab1cc-118">Le client RDC charge la DLL spécifiée par *Plug-inDLLName* et récupère l’objet com directement à l’aide du *CLSID*.</span><span class="sxs-lookup"><span data-stu-id="ab1cc-118">The RDC client will load the DLL specified by *Plug-inDLLName* and retrieve the COM object directly using *CLSID*.</span></span>

</dd> <dt>

<span data-ttu-id="ab1cc-119"><span id="Plug-inDLLName"></span><span id="plug-indllname"></span><span id="PLUG-INDLLNAME"></span>«*Plug-inDLLName*»</span><span class="sxs-lookup"><span data-stu-id="ab1cc-119"><span id="Plug-inDLLName"></span><span id="plug-indllname"></span><span id="PLUG-INDLLNAME"></span>"*Plug-inDLLName*"</span></span>
</dt> <dd>

<span data-ttu-id="ab1cc-120">La DLL implémente la fonction [**VirtualChannelGetInstance**](virtualchannelgetinstance.md) et l’exporte par nom.</span><span class="sxs-lookup"><span data-stu-id="ab1cc-120">The DLL implements the [**VirtualChannelGetInstance**](virtualchannelgetinstance.md) function and exports it by name.</span></span> <span data-ttu-id="ab1cc-121">Le client RDC utilise la fonction **VirtualChannelGetInstance** pour obtenir les pointeurs d’interface [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) pour tous les plug-ins implémentés par la dll.</span><span class="sxs-lookup"><span data-stu-id="ab1cc-121">The RDC client will use the **VirtualChannelGetInstance** function to obtain [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) interface pointers for all of the plug-ins implemented by the DLL.</span></span>

</dd> <dt>

<span data-ttu-id="ab1cc-122"><span id="_CLSID_"></span><span id="_clsid_"></span>« {*CLSID*} »</span><span class="sxs-lookup"><span data-stu-id="ab1cc-122"><span id="_CLSID_"></span><span id="_clsid_"></span>"{*CLSID*}"</span></span>
</dt> <dd>

<span data-ttu-id="ab1cc-123">Le client RDC instancie le plug-in en tant qu’objet COM normal à l’aide de [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) avec le *CLSID*.</span><span class="sxs-lookup"><span data-stu-id="ab1cc-123">The RDC client will instantiate the plug-in as a regular COM object using [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) with the *CLSID*.</span></span>

</dd> </dl>

> [!Note]  
> <span data-ttu-id="ab1cc-124">*Plug-inDLLName* représente le chemin d’accès complet et le nom du fichier. dll.</span><span class="sxs-lookup"><span data-stu-id="ab1cc-124">*Plug-inDLLName* represents the full path and file name of the .dll file.</span></span> <span data-ttu-id="ab1cc-125">Si le type de données est **reg \_ expand \_ SZ**, le chemin d’accès peut contenir des variables d’environnement non développées qui sont développées au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="ab1cc-125">If the data type is **REG\_EXPAND\_SZ**, the path can contain unexpanded environment variables that are expanded at runtime.</span></span>

 

<span data-ttu-id="ab1cc-126">Lorsque le client Connexion Bureau à distance (RDC) termine son initialisation, il effectue les opérations suivantes pour chaque plug-in inscrit :</span><span class="sxs-lookup"><span data-stu-id="ab1cc-126">When the Remote Desktop Connection (RDC) client finishes its initialization, it will perform the following for every registered plug-in:</span></span>

1.  <span data-ttu-id="ab1cc-127">Obtenez une instance de l’interface [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) pour chaque plug-in à l’aide de l’une des méthodes décrites ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="ab1cc-127">Obtain an instance of the [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) interface for each plug-in using one of the methods described above.</span></span>
2.  <span data-ttu-id="ab1cc-128">Appelez la méthode [**Initialize**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-initialize) de chaque interface [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) .</span><span class="sxs-lookup"><span data-stu-id="ab1cc-128">Call the [**Initialize**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-initialize) method of each [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) interface.</span></span>
3.  <span data-ttu-id="ab1cc-129">Si le client se connecte plusieurs fois au même serveur ou à un autre serveur, il peut y avoir plusieurs appels aux méthodes [**connectées**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-connected) et [**déconnectées**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-disconnected) .</span><span class="sxs-lookup"><span data-stu-id="ab1cc-129">If the client connects multiple times to the same or to a different server, there may be multiple calls to the [**Connected**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-connected) and [**Disconnected**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-disconnected) methods.</span></span>
4.  <span data-ttu-id="ab1cc-130">Le dernier appel que le plug-in doit gérer est [**terminé**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-terminated).</span><span class="sxs-lookup"><span data-stu-id="ab1cc-130">The last call that the plug-in should handle is [**Terminated**](/windows/desktop/api/TsVirtualChannels/nf-tsvirtualchannels-iwtsplugin-terminated).</span></span> <span data-ttu-id="ab1cc-131">Le client Connexion Bureau à distance (RDC) est sur le point de décharger le plug-in.</span><span class="sxs-lookup"><span data-stu-id="ab1cc-131">It is a signal that the Remote Desktop Connection (RDC) client is about to unload the plug-in.</span></span>

 

 