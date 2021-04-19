---
description: Représente une tablette attachée à l’ordinateur.
ms.assetid: 31e11f7d-5610-4c49-9203-2dc322fbef95
title: Interface ITablet
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 76fa7baea2713e5a2e5eaae562b6dac29e002fff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106528229"
---
# <a name="itablet-interface"></a><span data-ttu-id="2746b-103">Interface ITablet</span><span class="sxs-lookup"><span data-stu-id="2746b-103">ITablet interface</span></span>

<span data-ttu-id="2746b-104">Représente une tablette attachée à l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="2746b-104">Represents a tablet attached to the computer.</span></span>

## <a name="members"></a><span data-ttu-id="2746b-105">Membres</span><span class="sxs-lookup"><span data-stu-id="2746b-105">Members</span></span>

<span data-ttu-id="2746b-106">L’interface **ITablet** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="2746b-106">The **ITablet** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="2746b-107">**ITablet** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="2746b-107">**ITablet** also has these types of members:</span></span>

-   [<span data-ttu-id="2746b-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="2746b-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="2746b-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="2746b-109">Methods</span></span>

<span data-ttu-id="2746b-110">L’interface **ITablet** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="2746b-110">The **ITablet** interface has these methods.</span></span>



| <span data-ttu-id="2746b-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="2746b-111">Method</span></span>                                                                 | <span data-ttu-id="2746b-112">Description</span><span class="sxs-lookup"><span data-stu-id="2746b-112">Description</span></span>                                                                           |
|:-----------------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [<span data-ttu-id="2746b-113">**CreateContext**</span><span class="sxs-lookup"><span data-stu-id="2746b-113">**CreateContext**</span></span>](itablet-createcontext.md)                         | <span data-ttu-id="2746b-114">Crée un objet de contexte qui décrit le périphérique tablette spécifié.</span><span class="sxs-lookup"><span data-stu-id="2746b-114">Creates a context object that describes the specified tablet device.</span></span><br/>       |
| <span data-ttu-id="2746b-115">[**GetCursor**](/previous-versions/windows/desktop/legacy/aa373535(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2746b-115">[**GetCursor**](/previous-versions/windows/desktop/legacy/aa373535(v=vs.85))</span></span>                                 | <span data-ttu-id="2746b-116">Récupère l’objet [**ITabletCursor**](itabletcursor.md) spécifié.</span><span class="sxs-lookup"><span data-stu-id="2746b-116">Retrieves the specified [**ITabletCursor**](itabletcursor.md) object.</span></span><br/>     |
| [<span data-ttu-id="2746b-117">**GetCursorCount**</span><span class="sxs-lookup"><span data-stu-id="2746b-117">**GetCursorCount**</span></span>](itablet-getcursorcount.md)                       | <span data-ttu-id="2746b-118">Récupère le nombre d’objets Cursor associés à la tablette.</span><span class="sxs-lookup"><span data-stu-id="2746b-118">Retrieves the number of cursor objects associated with the tablet.</span></span><br/>         |
| [<span data-ttu-id="2746b-119">**GetDefaultContextSettings**</span><span class="sxs-lookup"><span data-stu-id="2746b-119">**GetDefaultContextSettings**</span></span>](itablet-getdefaultcontextsettings.md) | <span data-ttu-id="2746b-120">Récupère les paramètres de contexte par défaut pour la tablette.</span><span class="sxs-lookup"><span data-stu-id="2746b-120">Retrieves the default context settings for the tablet.</span></span><br/>                     |
| [<span data-ttu-id="2746b-121">**GetHardwareCaps**</span><span class="sxs-lookup"><span data-stu-id="2746b-121">**GetHardwareCaps**</span></span>](itablet-gethardwarecaps.md)                     | <span data-ttu-id="2746b-122">Récupère une valeur qui représente les fonctionnalités du matériel de tablette.</span><span class="sxs-lookup"><span data-stu-id="2746b-122">Retrieves a value that represents the capabilities of the tablet hardware.</span></span><br/> |
| [<span data-ttu-id="2746b-123">**GetMaxInputRect**</span><span class="sxs-lookup"><span data-stu-id="2746b-123">**GetMaxInputRect**</span></span>](itablet-getmaxinputrect.md)                     | <span data-ttu-id="2746b-124">Récupère un rectangle qui représente la zone d’entrée maximale de la tablette.</span><span class="sxs-lookup"><span data-stu-id="2746b-124">Retrieves a rectangle that represents maximum input area of the tablet.</span></span><br/>    |
| [<span data-ttu-id="2746b-125">**GetName**</span><span class="sxs-lookup"><span data-stu-id="2746b-125">**GetName**</span></span>](itablet-getname.md)                                     | <span data-ttu-id="2746b-126">Récupère une chaîne contenant le nom du périphérique tablette.</span><span class="sxs-lookup"><span data-stu-id="2746b-126">Retrieves a string containing the name of the tablet device.</span></span><br/>               |
| [<span data-ttu-id="2746b-127">**GetPlugAndPlayId**</span><span class="sxs-lookup"><span data-stu-id="2746b-127">**GetPlugAndPlayId**</span></span>](itablet-getplugandplayid.md)                   | <span data-ttu-id="2746b-128">Récupère une chaîne contenant l’ID de Plug-and-Play pour le périphérique tablette.</span><span class="sxs-lookup"><span data-stu-id="2746b-128">Retrieves a string containing the Plug and Play ID for the tablet device.</span></span><br/>  |
| <span data-ttu-id="2746b-129">[**GetPropertyMetrics**](/previous-versions/windows/desktop/legacy/aa367722(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2746b-129">[**GetPropertyMetrics**](/previous-versions/windows/desktop/legacy/aa367722(v=vs.85))</span></span>               | <span data-ttu-id="2746b-130">Récupère les données de métriques pour une propriété spécifiée.</span><span class="sxs-lookup"><span data-stu-id="2746b-130">Retrieves the metrics data for a specified property.</span></span><br/>                       |



 

## <a name="remarks"></a><span data-ttu-id="2746b-131">Notes</span><span class="sxs-lookup"><span data-stu-id="2746b-131">Remarks</span></span>

<span data-ttu-id="2746b-132">Les développeurs ne doivent pas utiliser cette interface.</span><span class="sxs-lookup"><span data-stu-id="2746b-132">Developers should not use this interface.</span></span>

<span data-ttu-id="2746b-133">Le code suivant décrit comment l’interface **ITablet** est définie.</span><span class="sxs-lookup"><span data-stu-id="2746b-133">The following code describes how the **ITablet** interface is defined.</span></span>

``` syntax
[
    object,
   uuid(1CB2EFC3-ABC7-4172-8FCB-3BC9CB93E29F),
    pointer_default(unique)
]
interface ITablet : IUnknown
{
    HRESULT GetDefaultContextSettings(
        [out] TABLET_CONTEXT_SETTINGS **ppTCS);

    HRESULT CreateContext(
        [in] HWND hWnd,
        [in, unique] RECT *prcInput,
        [in] DWORD dwOptions,
        [in, unique] TABLET_CONTEXT_SETTINGS *pTCS,
        [in] CONTEXT_ENABLE_TYPE cet,
        [out] ITabletContext **ppCtx,
        [in, out, unique] TABLET_CONTEXT_ID *pTcid,
        [in, out, unique] PACKET_DESCRIPTION **ppPD,
        [in, unique] ITabletEventSink *pSink);

    HRESULT GetName(
        [out] LPWSTR *ppwszName);

    HRESULT GetMaxInputRect(
        [out] RECT *prcInput);

    HRESULT GetHardwareCaps(
        [out] DWORD *pdwCaps);

    HRESULT GetPropertyMetrics(
        [in] REFGUID rguid,
        [out] PROPERTY_METRICS *pPM);

    HRESULT GetPlugAndPlayId(
        [out] LPWSTR *ppwszPPId);

    HRESULT GetCursorCount(
        [out] ULONG *pcCurs);

    HRESULT GetCursor(
        [in] ULONG iCur,
        [out] ITabletCursor **ppCur);
};   
```

## <a name="requirements"></a><span data-ttu-id="2746b-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2746b-134">Requirements</span></span>



| <span data-ttu-id="2746b-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2746b-135">Requirement</span></span> | <span data-ttu-id="2746b-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="2746b-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2746b-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2746b-137">Minimum supported client</span></span><br/> | <span data-ttu-id="2746b-138">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2746b-138">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="2746b-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2746b-139">Minimum supported server</span></span><br/> | <span data-ttu-id="2746b-140">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="2746b-140">None supported</span></span><br/>                                                              |
| <span data-ttu-id="2746b-141">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2746b-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="2746b-142"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2746b-142"><dt>Wisptis.exe</dt></span></span> </dl> |



 

