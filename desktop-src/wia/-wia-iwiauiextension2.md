---
description: L’interface IWiaUIExtension2 fournit des méthodes qui remplacent la valeur par défaut, l’interface utilisateur fournie par le système par une interface utilisateur personnalisée, et qui fournissent une icône d’appareil personnalisée.
ms.assetid: 1a747ea3-2476-438b-baf0-903b86cbbb16
title: Interface IWiaUIExtension2 (Wiadevd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaUIExtension2
api_type:
- COM
api_location:
- Wiadevd.h
ms.openlocfilehash: 4bfac82f90938a89b0d0ed76d9649e8e1a7cf19c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951217"
---
# <a name="iwiauiextension2-interface"></a><span data-ttu-id="b8ecc-103">Interface IWiaUIExtension2</span><span class="sxs-lookup"><span data-stu-id="b8ecc-103">IWiaUIExtension2 interface</span></span>

<span data-ttu-id="b8ecc-104">L’interface IWiaUIExtension2 fournit des méthodes qui remplacent la valeur par défaut, l’interface utilisateur fournie par le système par une interface utilisateur personnalisée, et qui fournissent une icône d’appareil personnalisée.</span><span class="sxs-lookup"><span data-stu-id="b8ecc-104">The IWiaUIExtension2 interface provides methods that replace the default, system-supplied user interface with a custom user interface, and that provide a custom device icon.</span></span> <span data-ttu-id="b8ecc-105">Les fournisseurs d’appareils peuvent implémenter cette interface pour fournir des interfaces utilisateur personnalisées pour leurs appareils.</span><span class="sxs-lookup"><span data-stu-id="b8ecc-105">Device vendors can implement this interface to provide custom user interfaces for their devices.</span></span>

## <a name="members"></a><span data-ttu-id="b8ecc-106">Membres</span><span class="sxs-lookup"><span data-stu-id="b8ecc-106">Members</span></span>

<span data-ttu-id="b8ecc-107">L’interface **IWiaUIExtension2** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="b8ecc-107">The **IWiaUIExtension2** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="b8ecc-108">**IWiaUIExtension2** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="b8ecc-108">**IWiaUIExtension2** also has these types of members:</span></span>

-   [<span data-ttu-id="b8ecc-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="b8ecc-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="b8ecc-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="b8ecc-110">Methods</span></span>

<span data-ttu-id="b8ecc-111">L’interface **IWiaUIExtension2** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="b8ecc-111">The **IWiaUIExtension2** interface has these methods.</span></span>



| <span data-ttu-id="b8ecc-112">Méthode</span><span class="sxs-lookup"><span data-stu-id="b8ecc-112">Method</span></span>                                                       | <span data-ttu-id="b8ecc-113">Description</span><span class="sxs-lookup"><span data-stu-id="b8ecc-113">Description</span></span>                                                                                  |
|:-------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b8ecc-114">**DeviceDialog**</span><span class="sxs-lookup"><span data-stu-id="b8ecc-114">**DeviceDialog**</span></span>](-wia-iwiauiextension2-devicedialog.md)   | <span data-ttu-id="b8ecc-115">Fournit une interface utilisateur personnalisée qui remplace l’interface utilisateur système par défaut.</span><span class="sxs-lookup"><span data-stu-id="b8ecc-115">Provides a custom user interface that replaces the default system user interface.</span></span><br/> |
| [<span data-ttu-id="b8ecc-116">**GetDeviceIcon**</span><span class="sxs-lookup"><span data-stu-id="b8ecc-116">**GetDeviceIcon**</span></span>](-wia-iwiauiextension2-getdeviceicon.md) | <span data-ttu-id="b8ecc-117">Obtient une icône d’appareil personnalisé.</span><span class="sxs-lookup"><span data-stu-id="b8ecc-117">Gets a custom device icon.</span></span><br/>                                                        |



 

## <a name="remarks"></a><span data-ttu-id="b8ecc-118">Notes</span><span class="sxs-lookup"><span data-stu-id="b8ecc-118">Remarks</span></span>



| <span data-ttu-id="b8ecc-119">Méthodes IUnknown</span><span class="sxs-lookup"><span data-stu-id="b8ecc-119">IUnknown Methods</span></span>                                        | <span data-ttu-id="b8ecc-120">Description</span><span class="sxs-lookup"><span data-stu-id="b8ecc-120">Description</span></span>                               |
|---------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="b8ecc-121">[IUnknown :: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span><span class="sxs-lookup"><span data-stu-id="b8ecc-121">[IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span></span> | <span data-ttu-id="b8ecc-122">Retourne des pointeurs aux interfaces prises en charge.</span><span class="sxs-lookup"><span data-stu-id="b8ecc-122">Returns pointers to supported interfaces.</span></span> |
| [<span data-ttu-id="b8ecc-123">IUnknown :: AddRef</span><span class="sxs-lookup"><span data-stu-id="b8ecc-123">IUnknown::AddRef</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | <span data-ttu-id="b8ecc-124">Incrémente le décompte de références.</span><span class="sxs-lookup"><span data-stu-id="b8ecc-124">Increments reference count.</span></span>               |
| [<span data-ttu-id="b8ecc-125">IUnknown :: Release</span><span class="sxs-lookup"><span data-stu-id="b8ecc-125">IUnknown::Release</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | <span data-ttu-id="b8ecc-126">Décrémente le décompte de références.</span><span class="sxs-lookup"><span data-stu-id="b8ecc-126">Decrements reference count.</span></span>               |



 

## <a name="requirements"></a><span data-ttu-id="b8ecc-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b8ecc-127">Requirements</span></span>



| <span data-ttu-id="b8ecc-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b8ecc-128">Requirement</span></span> | <span data-ttu-id="b8ecc-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="b8ecc-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b8ecc-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b8ecc-130">Minimum supported client</span></span><br/> | <span data-ttu-id="b8ecc-131">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b8ecc-131">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="b8ecc-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b8ecc-132">Minimum supported server</span></span><br/> | <span data-ttu-id="b8ecc-133">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b8ecc-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="b8ecc-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="b8ecc-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8ecc-135"><dt>Wiadevd. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8ecc-135"><dt>Wiadevd.h</dt></span></span> </dl> |



 

 
