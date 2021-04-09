---
description: Personnaliser la sortie de débogage avec ID3D10InfoQueue (Direct3D 10)
ms.assetid: 082c7783-c53a-4b73-b8f2-3f60e2c2689a
title: Personnaliser la sortie de débogage avec ID3D10InfoQueue (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 843ac7dd34b19cfe1fc7835a2026ae2dd28b9dcd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033718"
---
# <a name="customize-debug-output-with-id3d10infoqueue-direct3d-10"></a><span data-ttu-id="860af-103">Personnaliser la sortie de débogage avec ID3D10InfoQueue (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="860af-103">Customize Debug Output with ID3D10InfoQueue (Direct3D 10)</span></span>

<span data-ttu-id="860af-104">La file d’attente d’informations est gérée par une interface (voir [**interface ID3D10InfoQueue**](/windows/desktop/api/D3D10SDKLayers/nn-d3d10sdklayers-id3d10infoqueue)) qui stocke, récupère et filtre les messages de débogage.</span><span class="sxs-lookup"><span data-stu-id="860af-104">The information queue is managed by an interface (see [**ID3D10InfoQueue Interface**](/windows/desktop/api/D3D10SDKLayers/nn-d3d10sdklayers-id3d10infoqueue)) that stores, retrieves, and filters debug messages.</span></span> <span data-ttu-id="860af-105">La file d’attente comprend : une file d’attente de messages, une pile de filtres de stockage facultative et une pile de filtres de récupération facultative.</span><span class="sxs-lookup"><span data-stu-id="860af-105">The queue consists of: a message queue, an optional storage filter stack, and a optional retrieval filter stack.</span></span> <span data-ttu-id="860af-106">La pile de filtre de stockage peut être utilisée pour filtrer les messages que vous souhaitez stocker. la pile de filtres de récupération peut être utilisée pour filtrer les messages que vous souhaitez stocker.</span><span class="sxs-lookup"><span data-stu-id="860af-106">The storage-filter stack can be used to filter the messages you want stored; the retrieval-filter stack can be used to filter the messages you want stored.</span></span> <span data-ttu-id="860af-107">Une fois que vous avez filtré un message, le message est affiché dans la fenêtre de débogage et stocké dans la pile appropriée.</span><span class="sxs-lookup"><span data-stu-id="860af-107">Once you have filtered a message, the message will be printed out to the debug window and stored in the appropriate stack.</span></span>

<span data-ttu-id="860af-108">En général :</span><span class="sxs-lookup"><span data-stu-id="860af-108">In general:</span></span>

-   <span data-ttu-id="860af-109">Appeler [**ID3D10InfoQueue :: AddApplicationMessage**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-addapplicationmessage) pour générer des messages définis par l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="860af-109">Call [**ID3D10InfoQueue::AddApplicationMessage**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-addapplicationmessage) to generate user-defined messages</span></span>
-   <span data-ttu-id="860af-110">L’appel de [**ID3D10InfoQueue :: GetMessage**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-getmessage) est utilisé pour recevoir des messages (qui passent un filtre de récupération facultatif).</span><span class="sxs-lookup"><span data-stu-id="860af-110">Call [**ID3D10InfoQueue::GetMessage**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-getmessage) is used to get messages (that pass an optional retrieval filter).</span></span>

## <a name="registry-controls"></a><span data-ttu-id="860af-111">Contrôles du Registre</span><span class="sxs-lookup"><span data-stu-id="860af-111">Registry Controls</span></span>

<span data-ttu-id="860af-112">Utilisez les clés de Registre pour ajuster les paramètres de filtre, ajuster les points d’arrêt et désactiver la sortie de débogage.</span><span class="sxs-lookup"><span data-stu-id="860af-112">Use registry keys to adjust filter settings, adjust break points, and to mute the debug output.</span></span> <span data-ttu-id="860af-113">La couche de débogage vérifie ces chemins d’accès pour les clés de Registre ; le premier chemin d’accès trouvé sera utilisé.</span><span class="sxs-lookup"><span data-stu-id="860af-113">The debug layer will check these paths for registry keys; the first path found will be used.</span></span>

1.  <span data-ttu-id="860af-114">\\Logiciel HKCU logiciel \\ Microsoft \\ Direct3D \\<sous-clé définie par l’utilisateur></span><span class="sxs-lookup"><span data-stu-id="860af-114">HKCU\\Software\\Microsoft\\Direct3D\\<user-defined subkey></span></span>
2.  <span data-ttu-id="860af-115">HKLM \\ Software \\ Microsoft \\ Direct3D \\<sous-clé définie par l’utilisateur></span><span class="sxs-lookup"><span data-stu-id="860af-115">HKLM\\Software\\Microsoft\\Direct3D\\<user-defined subkey></span></span>
3.  <span data-ttu-id="860af-116">\\Logiciel HKCU \\ Microsoft \\ Direct3D</span><span class="sxs-lookup"><span data-stu-id="860af-116">HKCU\\Software\\Microsoft\\Direct3D</span></span>

<span data-ttu-id="860af-117">Où :</span><span class="sxs-lookup"><span data-stu-id="860af-117">Where:</span></span>

-   <span data-ttu-id="860af-118">Socle HKCU pour HKEY \_ Current \_ User et HKLM stand pour HKEY \_ local \_ machine.</span><span class="sxs-lookup"><span data-stu-id="860af-118">HKCU stand for HKEY\_CURRENT\_USER, and HKLM stand for HKEY\_LOCAL\_MACHINE.</span></span>
-   <span data-ttu-id="860af-119"><> de sous-clé définie par l’utilisateur est un nom arbitraire pour stocker les paramètres de débogage d’une application</span><span class="sxs-lookup"><span data-stu-id="860af-119"><user-defined subkey> is an arbitrary name to store debug settings for an application</span></span>

### <a name="filtering-debug-messages-using-registry-keys"></a><span data-ttu-id="860af-120">Filtrage des messages de débogage à l’aide de clés de Registre</span><span class="sxs-lookup"><span data-stu-id="860af-120">Filtering Debug Messages using Registry Keys</span></span>

<span data-ttu-id="860af-121">Si le registre contient une clé InfoQueueStorageFilterOverride (et est différent de zéro), les messages (et la sortie de débogage) peuvent être filtrés en ajoutant les contrôles de registre suivants.</span><span class="sxs-lookup"><span data-stu-id="860af-121">If the registry contains an InfoQueueStorageFilterOverride key (and is non-zero), then messages (and debug output) can be filtered by adding the following registry controls.</span></span>

-   <span data-ttu-id="860af-122">DWORD muet \_ catégorie \_ \* -sortie de débogage si cette clé est différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="860af-122">DWORD Mute\_CATEGORY\_\* - Debug output if this key is non-zero.</span></span>
-   <span data-ttu-id="860af-123">\_Gravité de silence DWORD \_ \* -la sortie de débogage est désactivée si cette clé n’est pas nulle.</span><span class="sxs-lookup"><span data-stu-id="860af-123">DWORD Mute\_SEVERITY\_\* - Debug output is disabled if this key is non-zero.</span></span>
-   <span data-ttu-id="860af-124">\_ID de sourdine DWORD \_ \* : le nom ou le numéro du message peut être utilisé pour \* (comme pour l' \_ ID BreakOn \_ \* décrit précédemment).</span><span class="sxs-lookup"><span data-stu-id="860af-124">DWORD Mute\_ID\_\* - Message name or number can be used for \* (just like for BreakOn\_ID\_\* described earlier).</span></span> <span data-ttu-id="860af-125">La sortie de débogage est désactivée si cette clé est différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="860af-125">Debug output is disabled if this key is non-zero.</span></span>
-   <span data-ttu-id="860af-126">\_Info de gravité d' \_ inactivation DWORD-la sortie de débogage est activée si cette clé n’est pas nulle.</span><span class="sxs-lookup"><span data-stu-id="860af-126">DWORD Unmute\_SEVERITY\_INFO - Debug output is ENABLED if this key is non-zero.</span></span> <span data-ttu-id="860af-127">Par défaut, quand InfoQueueStorageFilterOverride est activé, les messages de débogage avec des informations de gravité sont muets. par conséquent, pour cette clé, les informations sont retournées.</span><span class="sxs-lookup"><span data-stu-id="860af-127">By default when InfoQueueStorageFilterOverride is enabled, debug messages with severity INFO are muted - therefore for this key allows INFO to be turned back on.</span></span>

<span data-ttu-id="860af-128">Ces contrôles modifient si un message est enregistré ou affiché ; ils n’affectent pas si une API réussit ou échoue.</span><span class="sxs-lookup"><span data-stu-id="860af-128">These controls change whether a message is recorded or displayed; they do not affect whether an API passes or fails.</span></span>

### <a name="setting-break-conditions-using-registry-keys"></a><span data-ttu-id="860af-129">Définition de conditions d’arrêt à l’aide de clés de Registre</span><span class="sxs-lookup"><span data-stu-id="860af-129">Setting Break Conditions using Registry Keys</span></span>

<span data-ttu-id="860af-130">Les applications peuvent être forcées à s’arrêter sur un message à l’aide des clés de Registre suivantes.</span><span class="sxs-lookup"><span data-stu-id="860af-130">Applications can be forced to break on a message using the following registry keys.</span></span>

<span data-ttu-id="860af-131">**EnableBreakOnMessage** : cette clé permet de rompre les messages (et entraîne l’ignorance des paramètres de SetBreakOnCategory ()/SetBreakOnSeverity ()/SetBreakOnID ()).</span><span class="sxs-lookup"><span data-stu-id="860af-131">**EnableBreakOnMessage** - This key enables breaking on messages (and causes i's SetBreakOnCategory()/SetBreakOnSeverity()/SetBreakOnID() settings to be ignored).</span></span> <span data-ttu-id="860af-132">Les messages réels sur lesquels s’arrêter sont définis à l’aide d’une ou de plusieurs \_ \* valeurs BreakOn définies ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="860af-132">The actual messages to break on are defined using one or more BreakOn\_\* values defined below.</span></span>

-   <span data-ttu-id="860af-133">\**BreakOn \_ \_Catégorie \** _ Break sur un message passant par les filtres de stockage.</span><span class="sxs-lookup"><span data-stu-id="860af-133">\**BreakOn\_CATEGORY\_\** _ - Break on any message passing through the storage filters.</span></span> <span data-ttu-id="860af-134">\_ est l’un des \_ messages de catégorie de message D3D10 \_ .</span><span class="sxs-lookup"><span data-stu-id="860af-134">\_ is one of the D3D10\_MESSAGE\_CATEGORY messages.</span></span>
-   <span data-ttu-id="860af-135">\**BreakOn \_ \_Gravité \**: arrêt sur un message passant par les filtres de stockage.</span><span class="sxs-lookup"><span data-stu-id="860af-135">\**BreakOn\_SEVERITY\_\** _ - Break on any message passing through the storage filters.</span></span> <span data-ttu-id="860af-136">\_ est l’un des \_ messages de gravité du message D3D10 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="860af-136">\_ is one of the D3D10\_MESSAGE\_SEVERITY\_ messages.</span></span>
-   <span data-ttu-id="860af-137">\**BreakOn \_ \_ID \** _ Break sur un message passant par les filtres de stockage.</span><span class="sxs-lookup"><span data-stu-id="860af-137">\**BreakOn\_ID\_\** _ - Break on any message passing through the storage filters.</span></span> <span data-ttu-id="860af-138">\_ est l’un des \_ messages d' \_ ID de message D3D10 \_ ou peut être la valeur numérique de l’énumération d’erreur.</span><span class="sxs-lookup"><span data-stu-id="860af-138">\_ is one of the D3D10\_MESSAGE\_ID\_ messages or can be the numerical value of the error enumeration.</span></span> <span data-ttu-id="860af-139">Par exemple, supposons que le message avec l’ID « D3D10 \_ message \_ ID \_ hypothétique » contenait la valeur 123 dans l' \_ énumération de l’ID de message D3D10 \_ .</span><span class="sxs-lookup"><span data-stu-id="860af-139">For example, Suppose the message with ID "D3D10\_MESSAGE\_ID\_HYPOTHETICAL" had the value 123 in the D3D10\_MESSAGE\_ID enumeration.</span></span> <span data-ttu-id="860af-140">Dans ce cas, la création de la valeur BreakOn \_ ID \_ hypothétique = 1 ou BreakOn \_ ID \_ 123 = 1 permet d’effectuer la même opération-Break lorsqu’un message ayant l’ID de message D3D10 ID \_ \_ \_ hypothétique est rencontré.</span><span class="sxs-lookup"><span data-stu-id="860af-140">In this case, creating the value BreakOn\_ID\_HYPOTHETICAL=1 or BreakOn\_ID\_123=1 would both accomplish the same thing - break when a message having ID D3D10\_MESSAGE\_ID\_HYPOTHETICAL is encountered.</span></span>

### <a name="muting-debug-output-using-registry-keys"></a><span data-ttu-id="860af-141">Désactiver la sortie de débogage à l’aide de clés de Registre</span><span class="sxs-lookup"><span data-stu-id="860af-141">Muting Debug Output using Registry Keys</span></span>

<span data-ttu-id="860af-142">La sortie de débogage peut être muette à l’aide d’une clé MuteDebugOutput.</span><span class="sxs-lookup"><span data-stu-id="860af-142">Debug output can be muted using a MuteDebugOutput key.</span></span> <span data-ttu-id="860af-143">La présence de cette valeur dans le registre force la substitution de la méthode [**ID3D10InfoQueue :: SetMuteDebugOutput**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-setmutedebugoutput) de InfoQueue.</span><span class="sxs-lookup"><span data-stu-id="860af-143">The presence of this value in the registry forces override of the InfoQueue's [**ID3D10InfoQueue::SetMuteDebugOutput**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-setmutedebugoutput) method.</span></span> <span data-ttu-id="860af-144">MuteDebugOutput arrête les messages qui passent le filtre de stockage à être envoyés à la sortie de débogage.</span><span class="sxs-lookup"><span data-stu-id="860af-144">MuteDebugOutput stops messages that pass the storage filter from being sent to debug output.</span></span>

## <a name="disabling-debug-layer-messages"></a><span data-ttu-id="860af-145">Désactivation des messages de la couche de débogage</span><span class="sxs-lookup"><span data-stu-id="860af-145">Disabling Debug Layer Messages</span></span>

<span data-ttu-id="860af-146">Les messages de couche de débogage peuvent être isolés ou en tant que groupe lors de l’exécution en spécifiant des filtres à l’aide de [**ID3D10InfoQueue :: AddStorageFilterEntries**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-addstoragefilterentries).</span><span class="sxs-lookup"><span data-stu-id="860af-146">Debug layer messages can be disabled individualy or as a group at runtime by specifying filters using [**ID3D10InfoQueue::AddStorageFilterEntries**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-addstoragefilterentries).</span></span> <span data-ttu-id="860af-147">L’argument *pFilter* de **ID3D10InfoQueue :: AddStorageFilterEntries** prend une structure de [**\_ \_ \_ filtre de file d’attente d’informations D3D10**](/windows/desktop/api/d3d10sdklayers/ns-d3d10sdklayers-d3d10_info_queue_filter) qui contient une liste verte et une liste d’exclusion.</span><span class="sxs-lookup"><span data-stu-id="860af-147">The *pFilter* argument to **ID3D10InfoQueue::AddStorageFilterEntries** takes a [**D3D10\_INFO\_QUEUE\_FILTER**](/windows/desktop/api/d3d10sdklayers/ns-d3d10sdklayers-d3d10_info_queue_filter) structure that contains an allow list and a deny list.</span></span> <span data-ttu-id="860af-148">Les listes d’autorisation et de refus sont décrites par les structures DESC de filtre de la [**\_ \_ file d’attente \_ \_ D3D10s**](/windows/desktop/api/d3d10sdklayers/ns-d3d10sdklayers-d3d10_info_queue_filter_desc) qui permettent de spécifier le filtrage par catégorie, gravité et ID de message individuel.</span><span class="sxs-lookup"><span data-stu-id="860af-148">The allow and deny lists are described by [**D3D10\_INFO\_QUEUE\_FILTER\_DESC**](/windows/desktop/api/d3d10sdklayers/ns-d3d10sdklayers-d3d10_info_queue_filter_desc) structures that allow filtering to be specified by catergory, severity and individual message ID.</span></span>

<span data-ttu-id="860af-149">Le code suivant est un exemple de configuration de l' [**interface ID3D10InfoQueue**](/windows/desktop/api/D3D10SDKLayers/nn-d3d10sdklayers-id3d10infoqueue) pour refuser l’ID de message D3D10 de la \_ \_ mémoire tampon d’index de dessin de l’appareil un \_ \_ \_ \_ \_ \_ message trop petit.</span><span class="sxs-lookup"><span data-stu-id="860af-149">The following code is an example of setting up the [**ID3D10InfoQueue Interface**](/windows/desktop/api/D3D10SDKLayers/nn-d3d10sdklayers-id3d10infoqueue) to deny the D3D10\_MESSAGE\_ID\_DEVICE\_DRAW\_INDEX\_BUFFER\_TOO\_SMALL message.</span></span>


```
  //retrieve the ID3D10InfoQueue from a Direct3D device created with the D3D10_CREATE_DEVICE_DEBUG flag
  ID3D10InfoQueue * pInfoQueue;
    g_pd3dDevice->QueryInterface( __uuidof(ID3D10InfoQueue),  (void **)&pInfoQueue );
    
  //set up the list of messages to filter
    D3D10_MESSAGE_ID messageIDs [] = { D3D10_MESSAGE_ID_DEVICE_DRAW_INDEX_BUFFER_TOO_SMALL };
    
  //set the DenyList to use the list of messages
    D3D10_INFO_QUEUE_FILTER filter = { 0 };
    filter.DenyList.NumIDs = 1;
    filter.DenyList.pIDList = messageIDs;
    
  //apply the filter to the info queue
    pInfoQueue->AddStorageFilterEntries( &filter );  
```



## <a name="related-topics"></a><span data-ttu-id="860af-150">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="860af-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="860af-151">Couches d’API</span><span class="sxs-lookup"><span data-stu-id="860af-151">API Layers</span></span>](d3d10-graphics-programming-guide-api-features-layers.md)
</dt> <dt>

[<span data-ttu-id="860af-152">Fonctionnalités de l’API (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="860af-152">API Features (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-api-features.md)
</dt> </dl>

 

 



