---
description: Fournit des données pour un événement d’interruption de l’application.
ms.assetid: 2590AFAA-679C-49F1-804F-D429BB971727
title: Interface ISuspendingEventArgs (Windows. ApplicationModel. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISuspendingEventArgs
api_type:
- COM
api_location:
- Windows.ApplicationModel.h
ms.openlocfilehash: 687ecbb056a057338091b21a862816985ed0186a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514021"
---
# <a name="isuspendingeventargs-interface"></a><span data-ttu-id="f4482-103">Interface ISuspendingEventArgs</span><span class="sxs-lookup"><span data-stu-id="f4482-103">ISuspendingEventArgs interface</span></span>

<span data-ttu-id="f4482-104">Fournit des données pour un événement d’interruption de l’application.</span><span class="sxs-lookup"><span data-stu-id="f4482-104">Provides data for an app suspending event.</span></span>

## <a name="members"></a><span data-ttu-id="f4482-105">Membres</span><span class="sxs-lookup"><span data-stu-id="f4482-105">Members</span></span>

<span data-ttu-id="f4482-106">L’interface **ISuspendingEventArgs** hérite de [**IInspectable**](/windows/win32/api/inspectable/nn-inspectable-iinspectable).</span><span class="sxs-lookup"><span data-stu-id="f4482-106">The **ISuspendingEventArgs** interface inherits from [**IInspectable**](/windows/win32/api/inspectable/nn-inspectable-iinspectable).</span></span> <span data-ttu-id="f4482-107">**ISuspendingEventArgs** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="f4482-107">**ISuspendingEventArgs** also has these types of members:</span></span>

-   [<span data-ttu-id="f4482-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="f4482-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f4482-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="f4482-109">Properties</span></span>

<span data-ttu-id="f4482-110">L’interface **ISuspendingEventArgs** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="f4482-110">The **ISuspendingEventArgs** interface has these properties.</span></span>



| <span data-ttu-id="f4482-111">Propriété</span><span class="sxs-lookup"><span data-stu-id="f4482-111">Property</span></span>                                                                           | <span data-ttu-id="f4482-112">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="f4482-112">Access type</span></span>           | <span data-ttu-id="f4482-113">Description</span><span class="sxs-lookup"><span data-stu-id="f4482-113">Description</span></span>                                   |
|:-----------------------------------------------------------------------------------|:----------------------|:----------------------------------------------|
| [<span data-ttu-id="f4482-114">**SuspendingOperation**</span><span class="sxs-lookup"><span data-stu-id="f4482-114">**SuspendingOperation**</span></span>](isuspendingeventargs-suspendingoperation.md)<br/> | <span data-ttu-id="f4482-115">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f4482-115">Read/write</span></span><br/> | <span data-ttu-id="f4482-116">Obtient l’opération d’interruption de l’application.</span><span class="sxs-lookup"><span data-stu-id="f4482-116">Gets the app suspending operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f4482-117">Notes</span><span class="sxs-lookup"><span data-stu-id="f4482-117">Remarks</span></span>

<span data-ttu-id="f4482-118">Cet objet est accessible quand vous implémentez des gestionnaires d’événements tels que [**SuspendingEventHandler**](/uwp/api/windows.ui.webui.suspendingeventhandler?view=winrt-19041), [**SuspendingEventHandler**](/uwp/api/windows.ui.xaml.suspendingeventhandler?view=winrt-19041)et que vous [**Ajoutez la \_ suspension**](/previous-versions//hh438376(v=vs.85)) pour répondre aux événements d’interruption de l’application.</span><span class="sxs-lookup"><span data-stu-id="f4482-118">This object is accessed when you implement event handlers like [**SuspendingEventHandler**](/uwp/api/windows.ui.webui.suspendingeventhandler?view=winrt-19041), [**SuspendingEventHandler**](/uwp/api/windows.ui.xaml.suspendingeventhandler?view=winrt-19041), and [**add\_Suspending**](/previous-versions//hh438376(v=vs.85)) to respond to app suspending events.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4482-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f4482-119">Requirements</span></span>



| <span data-ttu-id="f4482-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f4482-120">Requirement</span></span> | <span data-ttu-id="f4482-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="f4482-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4482-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f4482-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f4482-123">Windows 8</span><span class="sxs-lookup"><span data-stu-id="f4482-123">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="f4482-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f4482-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f4482-125">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f4482-125">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="f4482-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="f4482-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f4482-127"><dt>Windows. ApplicationModel. h</dt></span><span class="sxs-lookup"><span data-stu-id="f4482-127"><dt>Windows.ApplicationModel.h</dt></span></span> </dl>   |
| <span data-ttu-id="f4482-128">MIDL</span><span class="sxs-lookup"><span data-stu-id="f4482-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f4482-129"><dt>Windows. ApplicationModel. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f4482-129"><dt>Windows.ApplicationModel.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4482-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f4482-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4482-131">**IInspectable**</span><span class="sxs-lookup"><span data-stu-id="f4482-131">**IInspectable**</span></span>](/windows/win32/api/inspectable/nn-inspectable-iinspectable)
</dt> <dt>

[<span data-ttu-id="f4482-132">**ISuspendingOperation**</span><span class="sxs-lookup"><span data-stu-id="f4482-132">**ISuspendingOperation**</span></span>](isuspendingoperation.md)
</dt> <dt>

[<span data-ttu-id="f4482-133">**ISuspendingDeferral**</span><span class="sxs-lookup"><span data-stu-id="f4482-133">**ISuspendingDeferral**</span></span>](isuspendingdeferral.md)
</dt> </dl>

 

 
