---
title: Interface IVMVirtualPCEvents (VPCCOMInterfaces. h)
description: Définit l’interface d’événements sortants pour l’interface IVMVirtualPC.
ms.assetid: 40ce14d8-43e4-4c72-9729-e5503d882be6
keywords:
- Virtual PC de l’interface IVMVirtualPCEvents
- IVMVirtualPCEvents interface Virtual PC, Description
topic_type:
- apiref
api_name:
- IVMVirtualPCEvents
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c3a6fd22f75027d1424b8605e8e36e373064069
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033101"
---
# <a name="ivmvirtualpcevents-interface"></a><span data-ttu-id="ce29c-105">Interface IVMVirtualPCEvents</span><span class="sxs-lookup"><span data-stu-id="ce29c-105">IVMVirtualPCEvents interface</span></span>

<span data-ttu-id="ce29c-106">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="ce29c-106">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="ce29c-107">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="ce29c-107">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="ce29c-108">Définit l’interface d’événements sortants pour l’interface [**IVMVirtualPC**](ivmvirtualpc.md) .</span><span class="sxs-lookup"><span data-stu-id="ce29c-108">Defines the outgoing event interface for the [**IVMVirtualPC**](ivmvirtualpc.md) interface.</span></span> <span data-ttu-id="ce29c-109">Le client implémente ces méthodes pour recevoir les événements envoyés par [**IVMVirtualPC**](ivmvirtualpc.md).</span><span class="sxs-lookup"><span data-stu-id="ce29c-109">The client implements these methods to receive events sent from [**IVMVirtualPC**](ivmvirtualpc.md).</span></span>

## <a name="members"></a><span data-ttu-id="ce29c-110">Membres</span><span class="sxs-lookup"><span data-stu-id="ce29c-110">Members</span></span>

<span data-ttu-id="ce29c-111">L’interface **IVMVirtualPCEvents** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="ce29c-111">The **IVMVirtualPCEvents** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="ce29c-112">**IVMVirtualPCEvents** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="ce29c-112">**IVMVirtualPCEvents** also has these types of members:</span></span>

-   [<span data-ttu-id="ce29c-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="ce29c-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="ce29c-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="ce29c-114">Methods</span></span>

<span data-ttu-id="ce29c-115">L’interface **IVMVirtualPCEvents** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="ce29c-115">The **IVMVirtualPCEvents** interface has these methods.</span></span>



| <span data-ttu-id="ce29c-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="ce29c-116">Method</span></span>                                                        | <span data-ttu-id="ce29c-117">Description</span><span class="sxs-lookup"><span data-stu-id="ce29c-117">Description</span></span>                                                                  |
|:--------------------------------------------------------------|:-----------------------------------------------------------------------------|
| [<span data-ttu-id="ce29c-118">**OnEventLogged**</span><span class="sxs-lookup"><span data-stu-id="ce29c-118">**OnEventLogged**</span></span>](ivmvirtualpcevents-oneventlogged.md)     | <span data-ttu-id="ce29c-119">Reçoit une notification indiquant que Windows Virtual PC enregistre un événement.</span><span class="sxs-lookup"><span data-stu-id="ce29c-119">Receives notification that Windows Virtual PC logs an event.</span></span><br/>      |
| [<span data-ttu-id="ce29c-120">**OnVMStateChange**</span><span class="sxs-lookup"><span data-stu-id="ce29c-120">**OnVMStateChange**</span></span>](ivmvirtualpcevents-onvmstatechange.md) | <span data-ttu-id="ce29c-121">Reçoit une notification indiquant que l’état d’une machine virtuelle a changé.</span><span class="sxs-lookup"><span data-stu-id="ce29c-121">Receives notification that a virtual machine's state has changed.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ce29c-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ce29c-122">Requirements</span></span>



| <span data-ttu-id="ce29c-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ce29c-123">Requirement</span></span> | <span data-ttu-id="ce29c-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="ce29c-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce29c-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ce29c-125">Minimum supported client</span></span><br/> | <span data-ttu-id="ce29c-126">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ce29c-126">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ce29c-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ce29c-127">Minimum supported server</span></span><br/> | <span data-ttu-id="ce29c-128">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="ce29c-128">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="ce29c-129">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="ce29c-129">End of client support</span></span><br/>    | <span data-ttu-id="ce29c-130">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ce29c-130">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="ce29c-131">Produit</span><span class="sxs-lookup"><span data-stu-id="ce29c-131">Product</span></span><br/>                  | <span data-ttu-id="ce29c-132">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="ce29c-132">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="ce29c-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="ce29c-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce29c-134"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce29c-134"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="ce29c-135">IID</span><span class="sxs-lookup"><span data-stu-id="ce29c-135">IID</span></span><br/>                      | <span data-ttu-id="ce29c-136">DIID \_ IVMVirtualPCEvents est défini comme efed1ef1-3c09-41f7-a9c2-7e29fa286c9d</span><span class="sxs-lookup"><span data-stu-id="ce29c-136">DIID\_IVMVirtualPCEvents is defined as efed1ef1-3c09-41f7-a9c2-7e29fa286c9d</span></span><br/>        |



 

