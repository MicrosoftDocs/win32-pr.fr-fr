---
description: Décrit les processus d’implémentation de gestionnaires d’événements d’appareil dans le registre.
ms.assetid: 84B12B5C-C179-4124-A1FC-B90D120336BF
title: Comment inscrire un gestionnaire pour un événement d’appareil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34ef15071b349afa3f863e7c57b64c280c2aef8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864918"
---
# <a name="how-to-register-a-handler-for-a-device-event"></a><span data-ttu-id="95fd6-103">Comment inscrire un gestionnaire pour un événement d’appareil</span><span class="sxs-lookup"><span data-stu-id="95fd6-103">How to Register a Handler for a Device Event</span></span>

<span data-ttu-id="95fd6-104">Les gestionnaires définissent la partie logicielle de l’exécution automatique.</span><span class="sxs-lookup"><span data-stu-id="95fd6-104">Handlers define the software portion of AutoPlay.</span></span> <span data-ttu-id="95fd6-105">Ils définissent l’icône et le nom convivial du logiciel, ainsi que le composant COM (Component Object Model) à instancier et comment initialiser le composant en réponse à un événement.</span><span class="sxs-lookup"><span data-stu-id="95fd6-105">They define the software's icon and friendly name, as well as the Component Object Model (COM) component to instantiate and how to initialize the component in response to an event.</span></span> <span data-ttu-id="95fd6-106">Chaque gestionnaire d’un événement spécifique s’inscrit sous la forme d’une valeur sous la clé **EventHandler** appropriée.</span><span class="sxs-lookup"><span data-stu-id="95fd6-106">Each handler for a specific event registers as a value under the appropriate **EventHandler** key.</span></span> <span data-ttu-id="95fd6-107">Lorsque cet événement est détecté, l’utilisateur est invité à choisir un gestionnaire dans la liste de tous les gestionnaires inscrits pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="95fd6-107">When that event is detected, the user is prompted to choose a handler from a list of all the handlers registered for that event.</span></span>

## <a name="instructions"></a><span data-ttu-id="95fd6-108">Instructions</span><span class="sxs-lookup"><span data-stu-id="95fd6-108">Instructions</span></span>


<span data-ttu-id="95fd6-109">Les gestionnaires et leurs valeurs associées sont définis sous la  \\ clé des **gestionnaires** AutoplayHandlers.</span><span class="sxs-lookup"><span data-stu-id="95fd6-109">Handlers and their associated values are defined under the **AutoplayHandlers**\\**Handlers** key.</span></span> <span data-ttu-id="95fd6-110">Les sous-clés diffèrent selon que le système peut lire le contenu de l’appareil directement ou si l’appareil fournit du contenu au système par le biais d’une interface propriétaire.</span><span class="sxs-lookup"><span data-stu-id="95fd6-110">Subkeys differ depending on whether the system can read device contents directly or whether the device provides contents to the system through a proprietary interface.</span></span>

<span data-ttu-id="95fd6-111">L’exemple suivant montre les sous-clés et les valeurs utilisées pour un périphérique, telles qu’une caméra vidéo numérique ou un lecteur. mp3, qui fournit son contenu au système via une interface propriétaire.</span><span class="sxs-lookup"><span data-stu-id="95fd6-111">The following example shows the subkeys and values that are used for a device, such as a digital video camera or .mp3 player, that provides its contents to the system through a proprietary interface.</span></span> <span data-ttu-id="95fd6-112">L’exemple de gestionnaire est appelé **MyHandler**.</span><span class="sxs-lookup"><span data-stu-id="95fd6-112">The example handler is called **MyHandler**.</span></span>

```
HKEY_LOCAL_MACHINE or HKEY_CURRENT_USER
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AutoplayHandlers
                     Handlers
                        MyHandler
                           Action [REG_SZ] = Play music
                           CLSID [REG_SZ] = {a51f2ed3-634e-4a97-9d55-efcf08e7b32f}
                           DefaultIcon [REG_EXPAND_SZ] = %ProgramFiles%\Windows Media Player\wmplayer.exe,0
                           InitCmdLine [REG_SZ] = /Play
                           ProgID [REG_SZ] = WMP.PlayMusicFiles
                           Provider [REG_SZ] = Windows Media Player
```

> [!Note]  
> <span data-ttu-id="95fd6-113">Tandis que l’exemple montre à la fois un ProgID et une valeur d’identificateur de classe (CLSID), dans la pratique, ces valeurs sont mutuellement exclusives afin qu’une seule ou l’autre soit présente.</span><span class="sxs-lookup"><span data-stu-id="95fd6-113">While the example shows both a ProgID and a class identifier (CLSID) value, in practice these values are mutually exclusive so that only one or the other is present.</span></span> <span data-ttu-id="95fd6-114">La valeur ProgID est préférée.</span><span class="sxs-lookup"><span data-stu-id="95fd6-114">The ProgID value is preferred.</span></span> <span data-ttu-id="95fd6-115">Le cas échéant, il doit pointer vers un composant COM qui implémente l’interface [**IHWEventHandler**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler) .</span><span class="sxs-lookup"><span data-stu-id="95fd6-115">Whichever is used, it should point to a COM component that implements the [**IHWEventHandler**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler) interface.</span></span>

 

<span data-ttu-id="95fd6-116">Vous pouvez entrer la valeur de l’action en tant que valeur littérale, par exemple « lire la musique » comme illustré dans cet exemple, ou en tant que nom de fichier avec une chaîne de ressource.</span><span class="sxs-lookup"><span data-stu-id="95fd6-116">You can enter the Action value as a literal value, for example "Play music" as shown in this example, or as a file name with a resource string.</span></span> <span data-ttu-id="95fd6-117">Vous pouvez également entrer la valeur du fournisseur sous la forme d’une valeur littérale ou d’un nom de fichier avec une chaîne de ressource.</span><span class="sxs-lookup"><span data-stu-id="95fd6-117">You can also enter the Provider value as a literal value or as a file name with a resource string.</span></span> <span data-ttu-id="95fd6-118">L’exécution automatique combine la valeur d’action et la valeur de fournisseur avec le mot « using » pour créer une légende conviviale qui s’affiche dans l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="95fd6-118">AutoPlay combines the Action value and the Provider value with the word "using" to create a friendly caption that displays in the UI.</span></span> <span data-ttu-id="95fd6-119">Dans l’exemple, la légende obtenue est « lire la musique à l’aide du lecteur Windows Media ».</span><span class="sxs-lookup"><span data-stu-id="95fd6-119">In the example, the resulting caption is "Play music using Windows Media Player."</span></span>

<span data-ttu-id="95fd6-120">La valeur DefaultIcon pointe vers un fichier. ico ou une ressource dans un fichier binaire.</span><span class="sxs-lookup"><span data-stu-id="95fd6-120">The DefaultIcon value points to either an .ico file or a resource in a binary file.</span></span> <span data-ttu-id="95fd6-121">Si la valeur numérique qui suit le nom de fichier binaire est égale ou supérieure à zéro, alors il s’agit de la valeur d’index de l’icône dans ce fichier binaire.</span><span class="sxs-lookup"><span data-stu-id="95fd6-121">If the numeric value that follows the binary file name is zero or greater, then it is the index value of the icon in that binary file.</span></span> <span data-ttu-id="95fd6-122">S’il s’agit d’une valeur négative, il s’agit de l’ID de ressource icône.</span><span class="sxs-lookup"><span data-stu-id="95fd6-122">If it is a negative value, then it is the icon resource ID.</span></span> <span data-ttu-id="95fd6-123">Les valeurs d’index négatives sont recommandées.</span><span class="sxs-lookup"><span data-stu-id="95fd6-123">Negative index values are recommended.</span></span> <span data-ttu-id="95fd6-124">Aucune valeur n’est nécessaire dans le cas d’un fichier. ico.</span><span class="sxs-lookup"><span data-stu-id="95fd6-124">No value is necessary in the case of an .ico file.</span></span> <span data-ttu-id="95fd6-125">Il est recommandé d’utiliser des variables d’environnement dans le chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="95fd6-125">It is recommended that you use environment variables in the path.</span></span>

<span data-ttu-id="95fd6-126">La valeur InitCmdLine passe l’état non modifié à l’aide de la méthode [**IHWEventHandler :: Initialize**](/windows/desktop/api/Shobjidl/nf-shobjidl-ihweventhandler-initialize) avant que toutes les autres méthodes ne soient appelées.</span><span class="sxs-lookup"><span data-stu-id="95fd6-126">The InitCmdLine value passes unaltered through the [**IHWEventHandler::Initialize**](/windows/desktop/api/Shobjidl/nf-shobjidl-ihweventhandler-initialize) method before any other methods are called.</span></span>

<span data-ttu-id="95fd6-127">L’exemple suivant montre les sous-clés et les valeurs utilisées pour un appareil qui peut être lu directement, par exemple un lecteur de CD-ROM ou un autre disque amovible.</span><span class="sxs-lookup"><span data-stu-id="95fd6-127">The following example shows the subkeys and values that are used for a device that can be read directly, such as a CD-ROM drive or other removable disk.</span></span> <span data-ttu-id="95fd6-128">Là encore, l’exemple de gestionnaire est appelé **MyHandler**.</span><span class="sxs-lookup"><span data-stu-id="95fd6-128">Again, the example handler is called **MyHandler**.</span></span>

```
HKEY_LOCAL_MACHINE or HKEY_CURRENT_USER
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AutoplayHandlers
                     Handlers
                        MyHandler
                           Action [REG_SZ] = @%systemroot%\System32\wiaacmgr.exe,-276
                           DefaultIcon [REG_EXPAND_SZ] = %systemroot%\System32\wiaacmgr.exe,-2
                           InvokeProgID [REG_SZ] = WIA.AutoPlayDropHandler
                           InvokeVerb [REG_SZ] = open
                           Provider [REG_SZ] = @%systemroot%\System32\wiaacmgr.exe,-101
```

<span data-ttu-id="95fd6-129">Dans cet exemple, les valeurs action et Provider sont affichées sous la forme d’un nom de fichier avec une chaîne de ressource plutôt que des valeurs littérales, mais les chaînes qu’elles référencent sont utilisées de la même manière.</span><span class="sxs-lookup"><span data-stu-id="95fd6-129">In this example, the Action and Provider values are shown as a file name with a resource string rather than literal values, but the strings that they reference are used in the same manner.</span></span> <span data-ttu-id="95fd6-130">Elles sont combinées avec le mot « using » pour former une légende conviviale, comme expliqué précédemment.</span><span class="sxs-lookup"><span data-stu-id="95fd6-130">They are combined with the word "using" to form a friendly caption as explained earlier.</span></span>

<span data-ttu-id="95fd6-131">Les valeurs InvokeProgID et InvokeVerb remplacent CLSID, InitCmdLine et ProgID.</span><span class="sxs-lookup"><span data-stu-id="95fd6-131">InvokeProgID and InvokeVerb values replace CLSID, InitCmdLine, and ProgID.</span></span> <span data-ttu-id="95fd6-132">Les valeurs InvokeProgID et InvokeVerb correspondent aux noms de clés qui se trouvent sous la **\_ \_ racine** de la clé HKEY, comme indiqué dans l’entrée de Registre suivante.</span><span class="sxs-lookup"><span data-stu-id="95fd6-132">The InvokeProgID and InvokeVerb values match key names that are found under **HKEY\_CLASSES\_ROOT**, as shown in the following registry entry.</span></span> <span data-ttu-id="95fd6-133">Cet ensemble d’exemples de clés correspond à l’exemple de gestionnaire spécifique décrit précédemment.</span><span class="sxs-lookup"><span data-stu-id="95fd6-133">This set of example keys corresponds to the specific Handler example described earlier.</span></span>

```
HKEY_CLASSES_ROOT
   WIA.AutoplayDropHandler
      shell
         open
            DropTarget
               Clsid = {F1ABE2B5-C073-4dba-B6EB-FD7A5111DD8F}
```

<span data-ttu-id="95fd6-134">La fonction [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) utilise le CLSID pour implémenter l’application appropriée.</span><span class="sxs-lookup"><span data-stu-id="95fd6-134">The [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function uses the CLSID to implement the appropriate application.</span></span>

<span data-ttu-id="95fd6-135">Une fois que vous avez défini le gestionnaire de l’une des deux manières suivantes, vous devez l’inscrire pour un événement spécifique.</span><span class="sxs-lookup"><span data-stu-id="95fd6-135">After you define the handler in either of these two ways, you need to register it for a specific event.</span></span> <span data-ttu-id="95fd6-136">Pour ce faire, vous devez fournir le nom du gestionnaire en tant que valeur pour la clé de cet événement sous **EventHandlers**.</span><span class="sxs-lookup"><span data-stu-id="95fd6-136">You do this by providing the handler name as a value for that event's key under **EventHandlers**.</span></span> <span data-ttu-id="95fd6-137">L’exemple suivant montre comment inscrire **MyHandler** en tant que gestionnaire pour l’événement GenericVolumeArrival.</span><span class="sxs-lookup"><span data-stu-id="95fd6-137">The following example shows how to register **MyHandler** as a handler for the GenericVolumeArrival event.</span></span> <span data-ttu-id="95fd6-138">Aucune valeur de données n’est assignée.</span><span class="sxs-lookup"><span data-stu-id="95fd6-138">It has no assigned data value.</span></span>

```
HKEY_LOCAL_MACHINE or HKEY_CURRENT_USER
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AutoplayHandlers
                     EventHandlers
                        GenericVolumeArrival
                           MyHandler [REG_SZ]
```

## <a name="related-topics"></a><span data-ttu-id="95fd6-139">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="95fd6-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="95fd6-140">**IHWEventHandler**</span><span class="sxs-lookup"><span data-stu-id="95fd6-140">**IHWEventHandler**</span></span>](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler)
</dt> <dt>

[<span data-ttu-id="95fd6-141">**CoCreateInstance**</span><span class="sxs-lookup"><span data-stu-id="95fd6-141">**CoCreateInstance**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> </dl>

 

 
