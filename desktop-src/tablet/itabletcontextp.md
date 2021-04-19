---
description: Représente le contexte de tablette.
ms.assetid: d518c42d-c2f6-4776-bea5-fecdfe48e260
title: Interface ITabletContextP
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletContextP
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 5b3b6a69deeaa30c3fa0e16b1b36094dceaff304
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106532303"
---
# <a name="itabletcontextp-interface"></a><span data-ttu-id="3a91b-103">Interface ITabletContextP</span><span class="sxs-lookup"><span data-stu-id="3a91b-103">ITabletContextP interface</span></span>

<span data-ttu-id="3a91b-104">Représente le contexte de tablette.</span><span class="sxs-lookup"><span data-stu-id="3a91b-104">Represents the tablet context.</span></span>

## <a name="members"></a><span data-ttu-id="3a91b-105">Membres</span><span class="sxs-lookup"><span data-stu-id="3a91b-105">Members</span></span>

<span data-ttu-id="3a91b-106">L’interface **ITabletContextP** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="3a91b-106">The **ITabletContextP** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="3a91b-107">**ITabletContextP** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="3a91b-107">**ITabletContextP** also has these types of members:</span></span>

-   [<span data-ttu-id="3a91b-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="3a91b-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="3a91b-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="3a91b-109">Methods</span></span>

<span data-ttu-id="3a91b-110">L’interface **ITabletContextP** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="3a91b-110">The **ITabletContextP** interface has these methods.</span></span>



| <span data-ttu-id="3a91b-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="3a91b-111">Method</span></span>                                                                                           | <span data-ttu-id="3a91b-112">Description</span><span class="sxs-lookup"><span data-stu-id="3a91b-112">Description</span></span>                                                                     |
|:-------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------|
| [<span data-ttu-id="3a91b-113">**IsTopMostHook**</span><span class="sxs-lookup"><span data-stu-id="3a91b-113">**IsTopMostHook**</span></span>](itabletcontextp-istopmosthook.md)                                           | <span data-ttu-id="3a91b-114">Indique si le contexte de tablette se trouve dans le hook le plus élevé.</span><span class="sxs-lookup"><span data-stu-id="3a91b-114">Indicates if the tablet context is in the top most hook.</span></span><br/>             |
| [<span data-ttu-id="3a91b-115">**Éviter**</span><span class="sxs-lookup"><span data-stu-id="3a91b-115">**Overlap**</span></span>](itabletcontextp-overlap.md)                                                       | <span data-ttu-id="3a91b-116">Déplace un contexte de tablette vers l’avant ou l’arrière de la file d’attente d’entrée.</span><span class="sxs-lookup"><span data-stu-id="3a91b-116">Moves a tablet context to the front or back of the input queue.</span></span><br/>      |
| [<span data-ttu-id="3a91b-117">**TrackInputRect**</span><span class="sxs-lookup"><span data-stu-id="3a91b-117">**TrackInputRect**</span></span>](itabletcontextp-trackinputrect.md)                                         | <span data-ttu-id="3a91b-118">Met à jour les coordonnées du mappage de l’emplacement des fenêtres dans le digitaliseur de tablette.</span><span class="sxs-lookup"><span data-stu-id="3a91b-118">Updates the tablet digitizer to window location mapping coordinates.</span></span><br/> |
| [<span data-ttu-id="3a91b-119">**UseNamedSharedMemoryCommunications**</span><span class="sxs-lookup"><span data-stu-id="3a91b-119">**UseNamedSharedMemoryCommunications**</span></span>](itabletcontextp-usenamedsharedmemorycommunications.md) | <span data-ttu-id="3a91b-120">Fournit l’accès à la mémoire partagée entre les Tablet threads.</span><span class="sxs-lookup"><span data-stu-id="3a91b-120">Provides access to memory shared between tablet threads.</span></span><br/>             |
| [<span data-ttu-id="3a91b-121">**UseSharedMemoryCommunications**</span><span class="sxs-lookup"><span data-stu-id="3a91b-121">**UseSharedMemoryCommunications**</span></span>](itabletcontextp-usesharedmemorycommunications.md)           | <span data-ttu-id="3a91b-122">Fournit l’accès à la mémoire partagée entre les Tablet threads.</span><span class="sxs-lookup"><span data-stu-id="3a91b-122">Provides access to memory shared between tablet threads.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="3a91b-123">Notes</span><span class="sxs-lookup"><span data-stu-id="3a91b-123">Remarks</span></span>

<span data-ttu-id="3a91b-124">Les développeurs ne doivent pas utiliser cette interface.</span><span class="sxs-lookup"><span data-stu-id="3a91b-124">Developers should not use this interface.</span></span>

<span data-ttu-id="3a91b-125">[**UseNamedSharedMemoryCommunications**](itabletcontextp-usenamedsharedmemorycommunications.md) est disponible uniquement sur Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="3a91b-125">[**UseNamedSharedMemoryCommunications**](itabletcontextp-usenamedsharedmemorycommunications.md) is only available on Windows Vista and later.</span></span>

<span data-ttu-id="3a91b-126">Le code suivant décrit comment l’interface **ITabletContextP** est définie.</span><span class="sxs-lookup"><span data-stu-id="3a91b-126">The following code describes how the **ITabletContextP** interface is defined.</span></span>

``` syntax
[
    object,
    uuid(22F74D0A-694F-4f47-A5CE-AE08A6409AC8),
    pointer_default(unique)
]
interface ITabletContextP : ITabletContext
{

    HRESULT Overlap([in] BOOL bTop, [out] DWORD *pdwtcid);

    HRESULT GetType([out] CONTEXT_TYPE *pct);

    HRESULT TrackInputRect([out] RECT *prcInput);

    HRESULT IsTopMostHook();

    HRESULT GetEventSink(
        [out] ITabletEventSink **ppSink);

    HRESULT UseSharedMemoryCommunications(
        [in]  DWORD pid,
        [out] DWORD *phEventMoreData,
        [out] DWORD *phEventClientReady,
        [out] DWORD *phMutexAccess,
        [out] DWORD *phFileMapping);

    HRESULT UseNamedSharedMemoryCommunications(
        [in] DWORD pid,
        [in, string] LPCTSTR szSid,
        [in, string] LPCTSTR sdIlSid,
        [out] DWORD *pdwEventMoreDataId,
        [out] DWORD *pdwEventClientReadyId,
        [out] DWORD *pdwMutexAccessId,
        [out] DWORD *pdwFileMappingId);
};
```

## <a name="requirements"></a><span data-ttu-id="3a91b-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3a91b-127">Requirements</span></span>



| <span data-ttu-id="3a91b-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3a91b-128">Requirement</span></span> | <span data-ttu-id="3a91b-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="3a91b-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3a91b-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3a91b-130">Minimum supported client</span></span><br/> | <span data-ttu-id="3a91b-131">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3a91b-131">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="3a91b-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3a91b-132">Minimum supported server</span></span><br/> | <span data-ttu-id="3a91b-133">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="3a91b-133">None supported</span></span><br/>                                                              |
| <span data-ttu-id="3a91b-134">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3a91b-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="3a91b-135"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3a91b-135"><dt>Wisptis.exe</dt></span></span> </dl> |



 

