---
description: Définit des méthodes qui gèrent les événements de l’interface ITablet.
ms.assetid: 9acf32fa-b33f-4b9a-be73-804b7d5434e8
title: Interface ITabletEventSink
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: fc42bfe8a6e69504c35d7926c4c5a8b688404897
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210615"
---
# <a name="itableteventsink-interface"></a><span data-ttu-id="0aeeb-103">Interface ITabletEventSink</span><span class="sxs-lookup"><span data-stu-id="0aeeb-103">ITabletEventSink interface</span></span>

<span data-ttu-id="0aeeb-104">Définit des méthodes qui gèrent les événements de l' [**interface ITablet**](itablet.md) .</span><span class="sxs-lookup"><span data-stu-id="0aeeb-104">Defines methods that handle the [**ITablet Interface**](itablet.md) events.</span></span>

## <a name="members"></a><span data-ttu-id="0aeeb-105">Membres</span><span class="sxs-lookup"><span data-stu-id="0aeeb-105">Members</span></span>

<span data-ttu-id="0aeeb-106">L’interface **ITabletEventSink** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="0aeeb-106">The **ITabletEventSink** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="0aeeb-107">**ITabletEventSink** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="0aeeb-107">**ITabletEventSink** also has these types of members:</span></span>

-   [<span data-ttu-id="0aeeb-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="0aeeb-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="0aeeb-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="0aeeb-109">Methods</span></span>

<span data-ttu-id="0aeeb-110">L’interface **ITabletEventSink** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="0aeeb-110">The **ITabletEventSink** interface has these methods.</span></span>



| <span data-ttu-id="0aeeb-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="0aeeb-111">Method</span></span>                                                        | <span data-ttu-id="0aeeb-112">Description</span><span class="sxs-lookup"><span data-stu-id="0aeeb-112">Description</span></span>                                                                                      |
|:--------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0aeeb-113">**ContextCreate**</span><span class="sxs-lookup"><span data-stu-id="0aeeb-113">**ContextCreate**</span></span>](itableteventsink-contextcreate.md)       | <span data-ttu-id="0aeeb-114">Se produit lors de la création d’un nouveau contexte de tablette.</span><span class="sxs-lookup"><span data-stu-id="0aeeb-114">Occurs when a new tablet context is created.</span></span><br/>                                          |
| [<span data-ttu-id="0aeeb-115">**ContextDestroy**</span><span class="sxs-lookup"><span data-stu-id="0aeeb-115">**ContextDestroy**</span></span>](itableteventsink-contextdestroy.md)     | <span data-ttu-id="0aeeb-116">Se produit lorsqu’un contexte de tablette est en cours de destruction.</span><span class="sxs-lookup"><span data-stu-id="0aeeb-116">Occurs when a tablet context is being destroyed.</span></span><br/>                                      |
| [<span data-ttu-id="0aeeb-117">**CursorDown**</span><span class="sxs-lookup"><span data-stu-id="0aeeb-117">**CursorDown**</span></span>](itableteventsink-cursordown.md)             | <span data-ttu-id="0aeeb-118">Se produit lorsque l’info-bulle du stylet contacte la surface de tablette numérique.</span><span class="sxs-lookup"><span data-stu-id="0aeeb-118">Occurs when the stylus tip contacts the digitizing tablet surface.</span></span><br/>                    |
| [<span data-ttu-id="0aeeb-119">**CursorInRange**</span><span class="sxs-lookup"><span data-stu-id="0aeeb-119">**CursorInRange**</span></span>](itableteventsink-cursorinrange.md)       | <span data-ttu-id="0aeeb-120">Se produit lorsqu’un stylet est dans la plage de détection du digitaliseur.</span><span class="sxs-lookup"><span data-stu-id="0aeeb-120">Occurs when a stylus comes within the digitizer's range of detection.</span></span><br/>                 |
| [<span data-ttu-id="0aeeb-121">**CursorMove**</span><span class="sxs-lookup"><span data-stu-id="0aeeb-121">**CursorMove**</span></span>](itableteventsink-cursormove.md)             | <span data-ttu-id="0aeeb-122">Se produit lorsque le curseur se déplace sur le digitaliseur de tablette.</span><span class="sxs-lookup"><span data-stu-id="0aeeb-122">Occurs when the cursor moves over the tablet digitizer.</span></span><br/>                               |
| [<span data-ttu-id="0aeeb-123">**CursorNew**</span><span class="sxs-lookup"><span data-stu-id="0aeeb-123">**CursorNew**</span></span>](itableteventsink-cursornew.md)               | <span data-ttu-id="0aeeb-124">Se produit lorsqu’un nouveau stylet est ajouté au système.</span><span class="sxs-lookup"><span data-stu-id="0aeeb-124">Occurs when a new stylus is added to the system.</span></span><br/>                                      |
| [<span data-ttu-id="0aeeb-125">**CursorOutOfRange**</span><span class="sxs-lookup"><span data-stu-id="0aeeb-125">**CursorOutOfRange**</span></span>](itableteventsink-cursoroutofrange.md) | <span data-ttu-id="0aeeb-126">Se produit lorsque le stylet quitte la plage de détection physique (proximité) de la tablette.</span><span class="sxs-lookup"><span data-stu-id="0aeeb-126">Occurs when the stylus leaves the physical detection range (proximity) of the tablet.</span></span><br/> |
| [<span data-ttu-id="0aeeb-127">**CursorUp**</span><span class="sxs-lookup"><span data-stu-id="0aeeb-127">**CursorUp**</span></span>](itableteventsink-cursorup.md)                 | <span data-ttu-id="0aeeb-128">Se produit lorsque l’utilisateur a relâché le stylet à partir de la surface du digitaliseur de tablette.</span><span class="sxs-lookup"><span data-stu-id="0aeeb-128">Occurs when the user has raised the stylus from the tablet digitizer surface.</span></span><br/>         |
| [<span data-ttu-id="0aeeb-129">**Paquets**</span><span class="sxs-lookup"><span data-stu-id="0aeeb-129">**Packets**</span></span>](itableteventsink-packets.md)                   | <span data-ttu-id="0aeeb-130">Se produit lorsque le stylet se déplace sur le digitaliseur.</span><span class="sxs-lookup"><span data-stu-id="0aeeb-130">Occurs when the stylus is moving on the digitizer.</span></span><br/>                                    |
| [<span data-ttu-id="0aeeb-131">**SystemEvent**</span><span class="sxs-lookup"><span data-stu-id="0aeeb-131">**SystemEvent**</span></span>](itableteventsink-systemevent.md)           | <span data-ttu-id="0aeeb-132">Se produit lorsqu’un événement système est disponible.</span><span class="sxs-lookup"><span data-stu-id="0aeeb-132">Occurs when a system event is available.</span></span><br/>                                              |



 

## <a name="remarks"></a><span data-ttu-id="0aeeb-133">Notes</span><span class="sxs-lookup"><span data-stu-id="0aeeb-133">Remarks</span></span>

<span data-ttu-id="0aeeb-134">Les développeurs ne doivent pas utiliser cette interface.</span><span class="sxs-lookup"><span data-stu-id="0aeeb-134">Developers should not use this interface.</span></span>

<span data-ttu-id="0aeeb-135">Le code suivant illustre la définition de l’interface **ITabletEventSink** .</span><span class="sxs-lookup"><span data-stu-id="0aeeb-135">The following code shows how the **ITabletEventSink** interface is defined.</span></span>

``` syntax
[
    object,
    uuid(788459C8-26C8-4666-BF57-04AD3A0A5EB5),
    pointer_default(unique)
]
interface ITabletEventSink: IUnknown
{

    HRESULT ContextCreate(
        [in] TABLET_CONTEXT_ID tcid
    );

    HRESULT ContextDestroy(
        [in] TABLET_CONTEXT_ID tcid
    );

    HRESULT CursorNew(
        [in] TABLET_CONTEXT_ID tcid,
        [in] CURSOR_ID cid
    );

    HRESULT CursorInRange(
        [in] TABLET_CONTEXT_ID tcid,
        [in] CURSOR_ID cid
    );

    HRESULT CursorOutOfRange(
        [in] TABLET_CONTEXT_ID tcid,
        [in] CURSOR_ID cid
    );

    HRESULT CursorDown(
        [in] TABLET_CONTEXT_ID tcid,
        [in] CURSOR_ID cid,
        [in] ULONG nSerialNumber,
        [in] ULONG cbPkt,
        [in, size_is(cbPkt)] BYTE *pbPkt
    );

    HRESULT CursorUp(
        [in] TABLET_CONTEXT_ID tcid,
        [in] CURSOR_ID cid,
        [in] ULONG nSerialNumber,
        [in] ULONG cbPkt,
        [in, size_is(cbPkt)] BYTE *pbPkt
    );

    HRESULT Packets(
        [in] TABLET_CONTEXT_ID tcid,
        [in] ULONG cPkts,
        [in] ULONG cbPkts,
        [in, size_is(cbPkts)] BYTE * pbPkts,
        [in, unique, size_is(cPkts)
#ifndef NT_TARGET_XP
         ,disable_consistency_check
#endif
        ] ULONG *pnSerialNumbers,
        [in] CURSOR_ID cid
    );

    HRESULT SystemEvent(
        [in] TABLET_CONTEXT_ID tcid,
        [in] CURSOR_ID cid,
        [in] SYSTEM_EVENT event,
        [in] SYSTEM_EVENT_DATA eventdata
    );
};

     
```

## <a name="requirements"></a><span data-ttu-id="0aeeb-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0aeeb-136">Requirements</span></span>



| <span data-ttu-id="0aeeb-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0aeeb-137">Requirement</span></span> | <span data-ttu-id="0aeeb-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="0aeeb-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0aeeb-139">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0aeeb-139">Minimum supported client</span></span><br/> | <span data-ttu-id="0aeeb-140">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0aeeb-140">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="0aeeb-141">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0aeeb-141">Minimum supported server</span></span><br/> | <span data-ttu-id="0aeeb-142">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="0aeeb-142">None supported</span></span><br/>                                                              |
| <span data-ttu-id="0aeeb-143">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0aeeb-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="0aeeb-144"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0aeeb-144"><dt>Wisptis.exe</dt></span></span> </dl> |



 

