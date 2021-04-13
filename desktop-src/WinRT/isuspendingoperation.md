---
description: Fournit des informations sur une opération d’interruption de l’application.
ms.assetid: B380AEA2-6486-46CC-AD0A-CF25C144DC01
title: Interface ISuspendingOperation (Windows. ApplicationModel. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISuspendingOperation
api_type:
- COM
api_location:
- Windows.ApplicationModel.h
ms.openlocfilehash: 09a3c37216298fa672cdd676e835454b4e0f4bd2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526223"
---
# <a name="isuspendingoperation-interface"></a><span data-ttu-id="bc26b-103">Interface ISuspendingOperation</span><span class="sxs-lookup"><span data-stu-id="bc26b-103">ISuspendingOperation interface</span></span>

<span data-ttu-id="bc26b-104">Fournit des informations sur une opération d’interruption de l’application.</span><span class="sxs-lookup"><span data-stu-id="bc26b-104">Provides information about an app suspending operation.</span></span>

## <a name="members"></a><span data-ttu-id="bc26b-105">Membres</span><span class="sxs-lookup"><span data-stu-id="bc26b-105">Members</span></span>

<span data-ttu-id="bc26b-106">L’interface **ISuspendingOperation** hérite de [**IInspectable**](/windows/win32/api/inspectable/nn-inspectable-iinspectable).</span><span class="sxs-lookup"><span data-stu-id="bc26b-106">The **ISuspendingOperation** interface inherits from [**IInspectable**](/windows/win32/api/inspectable/nn-inspectable-iinspectable).</span></span> <span data-ttu-id="bc26b-107">**ISuspendingOperation** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="bc26b-107">**ISuspendingOperation** also has these types of members:</span></span>

-   [<span data-ttu-id="bc26b-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="bc26b-108">Methods</span></span>](#methods)
-   [<span data-ttu-id="bc26b-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="bc26b-109">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="bc26b-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="bc26b-110">Methods</span></span>

<span data-ttu-id="bc26b-111">L’interface **ISuspendingOperation** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="bc26b-111">The **ISuspendingOperation** interface has these methods.</span></span>



| <span data-ttu-id="bc26b-112">Méthode</span><span class="sxs-lookup"><span data-stu-id="bc26b-112">Method</span></span>                                                  | <span data-ttu-id="bc26b-113">Description</span><span class="sxs-lookup"><span data-stu-id="bc26b-113">Description</span></span>                                                       |
|:--------------------------------------------------------|:------------------------------------------------------------------|
| [<span data-ttu-id="bc26b-114">**GetDeferral**</span><span class="sxs-lookup"><span data-stu-id="bc26b-114">**GetDeferral**</span></span>](isuspendingoperation-getdeferral.md) | <span data-ttu-id="bc26b-115">Demande que l’opération d’interruption de l’application soit retardée.</span><span class="sxs-lookup"><span data-stu-id="bc26b-115">Requests that the app suspending operation be delayed.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="bc26b-116">Propriétés</span><span class="sxs-lookup"><span data-stu-id="bc26b-116">Properties</span></span>

<span data-ttu-id="bc26b-117">L’interface **ISuspendingOperation** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="bc26b-117">The **ISuspendingOperation** interface has these properties.</span></span>



| <span data-ttu-id="bc26b-118">Propriété</span><span class="sxs-lookup"><span data-stu-id="bc26b-118">Property</span></span>                                                     | <span data-ttu-id="bc26b-119">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="bc26b-119">Access type</span></span>           | <span data-ttu-id="bc26b-120">Description</span><span class="sxs-lookup"><span data-stu-id="bc26b-120">Description</span></span>                                                                             |
|:-------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------|
| [<span data-ttu-id="bc26b-121">**Échéance**</span><span class="sxs-lookup"><span data-stu-id="bc26b-121">**Deadline**</span></span>](isuspendingoperation-deadline.md)<br/> | <span data-ttu-id="bc26b-122">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="bc26b-122">Read/write</span></span><br/> | <span data-ttu-id="bc26b-123">Obtient le temps restant avant qu’une opération d’interruption de l’application retardée se poursuive.</span><span class="sxs-lookup"><span data-stu-id="bc26b-123">Gets the time remaining before a delayed app suspending operation continues.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="bc26b-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bc26b-124">Requirements</span></span>



| <span data-ttu-id="bc26b-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bc26b-125">Requirement</span></span> | <span data-ttu-id="bc26b-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="bc26b-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc26b-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bc26b-127">Minimum supported client</span></span><br/> | <span data-ttu-id="bc26b-128">Windows 8</span><span class="sxs-lookup"><span data-stu-id="bc26b-128">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="bc26b-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bc26b-129">Minimum supported server</span></span><br/> | <span data-ttu-id="bc26b-130">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="bc26b-130">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="bc26b-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="bc26b-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc26b-132"><dt>Windows. ApplicationModel. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc26b-132"><dt>Windows.ApplicationModel.h</dt></span></span> </dl>   |
| <span data-ttu-id="bc26b-133">MIDL</span><span class="sxs-lookup"><span data-stu-id="bc26b-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="bc26b-134"><dt>Windows. ApplicationModel. idl</dt></span><span class="sxs-lookup"><span data-stu-id="bc26b-134"><dt>Windows.ApplicationModel.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc26b-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bc26b-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc26b-136">**IInspectable**</span><span class="sxs-lookup"><span data-stu-id="bc26b-136">**IInspectable**</span></span>](/windows/win32/api/inspectable/nn-inspectable-iinspectable)
</dt> <dt>

[<span data-ttu-id="bc26b-137">**ISuspendingDeferral**</span><span class="sxs-lookup"><span data-stu-id="bc26b-137">**ISuspendingDeferral**</span></span>](isuspendingdeferral.md)
</dt> <dt>

[<span data-ttu-id="bc26b-138">**ISuspendingEventArgs**</span><span class="sxs-lookup"><span data-stu-id="bc26b-138">**ISuspendingEventArgs**</span></span>](isuspendingeventargs.md)
</dt> </dl>

 

 
