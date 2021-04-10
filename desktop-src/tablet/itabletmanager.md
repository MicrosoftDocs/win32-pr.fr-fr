---
description: Permet d’accéder à tous les tablettes attachées à l’ordinateur.
ms.assetid: d0fd9a6f-93fe-43d6-97fd-fee45854dfa1
title: Interface ITabletManager
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletManager
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 3400d98a832819d1edd640cd78586f1cfb06bdee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042782"
---
# <a name="itabletmanager-interface"></a><span data-ttu-id="e435b-103">Interface ITabletManager</span><span class="sxs-lookup"><span data-stu-id="e435b-103">ITabletManager interface</span></span>

<span data-ttu-id="e435b-104">Permet d’accéder à tous les tablettes attachées à l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="e435b-104">Provides access to all of the tablets attached to the computer.</span></span>

## <a name="members"></a><span data-ttu-id="e435b-105">Membres</span><span class="sxs-lookup"><span data-stu-id="e435b-105">Members</span></span>

<span data-ttu-id="e435b-106">L’interface **ITabletManager** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="e435b-106">The **ITabletManager** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="e435b-107">**ITabletManager** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="e435b-107">**ITabletManager** also has these types of members:</span></span>

-   [<span data-ttu-id="e435b-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="e435b-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="e435b-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="e435b-109">Methods</span></span>

<span data-ttu-id="e435b-110">L’interface **ITabletManager** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="e435b-110">The **ITabletManager** interface has these methods.</span></span>



| <span data-ttu-id="e435b-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="e435b-111">Method</span></span>                                                  | <span data-ttu-id="e435b-112">Description</span><span class="sxs-lookup"><span data-stu-id="e435b-112">Description</span></span>                                                        |
|:--------------------------------------------------------|:-------------------------------------------------------------------|
| <span data-ttu-id="e435b-113">[**GetTablet**](/previous-versions/windows/desktop/legacy/aa373683(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e435b-113">[**GetTablet**](/previous-versions/windows/desktop/legacy/aa373683(v=vs.85))</span></span>           | <span data-ttu-id="e435b-114">Récupère l’objet tablette spécifié.</span><span class="sxs-lookup"><span data-stu-id="e435b-114">Retrieves the specified tablet object.</span></span><br/>                  |
| [<span data-ttu-id="e435b-115">**GetTabletCount**</span><span class="sxs-lookup"><span data-stu-id="e435b-115">**GetTabletCount**</span></span>](itabletmanager-gettabletcount.md) | <span data-ttu-id="e435b-116">Récupère le nombre de tablettes attachées au système.</span><span class="sxs-lookup"><span data-stu-id="e435b-116">Retrieves the number of tablets attached to the system.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e435b-117">Notes</span><span class="sxs-lookup"><span data-stu-id="e435b-117">Remarks</span></span>

<span data-ttu-id="e435b-118">Les développeurs ne doivent pas utiliser cette interface.</span><span class="sxs-lookup"><span data-stu-id="e435b-118">Developers should not use this interface.</span></span>

<span data-ttu-id="e435b-119">Le code suivant illustre l’implémentation de l’interface **ITabletManager** .</span><span class="sxs-lookup"><span data-stu-id="e435b-119">The following code shows how the **ITabletManager** interface is implemented.</span></span>

``` syntax
[
    object,
    uuid(764DE8AA-1867-47C1-8F6A-122445ABD89A),
    pointer_default(unique)
]
interface ITabletManager : IUnknown
{
    HRESULT GetDefaultTablet(
        [out] ITablet **ppTablet);

    HRESULT GetTabletCount(
        [out] ULONG *pcTablets);

    HRESULT GetTablet(
        [in] ULONG iTablet,
        [out] ITablet **ppTablet);

    HRESULT GetTabletContextById(
        [in] TABLET_CONTEXT_ID tcid,
        [out] ITabletContext **ppContext);

    HRESULT GetCursorById(
        [in] CURSOR_ID cid,
        [out] ITabletCursor **ppCursor);
};
        
        
```

<span data-ttu-id="e435b-120">Appelez [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) avec l’ID de classe CLSID \_ TabletManagerS, puis appelez [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) pour obtenir un pointeur vers l' **interface ITabletManager**.</span><span class="sxs-lookup"><span data-stu-id="e435b-120">Call [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) with a class ID of CLSID\_TabletManagerS, and then call [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) to get a pointer to the **ITabletManager Interface**.</span></span> <span data-ttu-id="e435b-121">Le \_ GUID TABLETMANAGERS CLSID est défini comme suit :</span><span class="sxs-lookup"><span data-stu-id="e435b-121">The CLSID\_TabletManagerS GUID is defined as follows:</span></span>

``` syntax
#define CLSID_TabletManagerS uuid(A5B020FD-E04B-4e67-B65A-E7DEED25B2CF)
```

## <a name="requirements"></a><span data-ttu-id="e435b-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e435b-122">Requirements</span></span>



| <span data-ttu-id="e435b-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e435b-123">Requirement</span></span> | <span data-ttu-id="e435b-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="e435b-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e435b-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e435b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="e435b-126">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e435b-126">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="e435b-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e435b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="e435b-128">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="e435b-128">None supported</span></span><br/>                                                              |
| <span data-ttu-id="e435b-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e435b-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="e435b-130"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e435b-130"><dt>Wisptis.exe</dt></span></span> </dl> |



 

