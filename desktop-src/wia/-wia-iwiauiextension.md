---
description: L’interface IWiaUIExtension fournit des méthodes qui remplacent l’interface utilisateur système par défaut, fournissent un logo de bitmap d’appareil personnalisé et fournissent une icône d’appareil personnalisé.
ms.assetid: e3c69019-0e07-44ad-b48b-ea7e3daed2b7
title: Interface IWiaUIExtension (Wiadevd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaUIExtension
api_type:
- COM
api_location:
- Wiadevd.h
ms.openlocfilehash: 98318ba3b2b94d334834150b219c5d453c4e0d89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515867"
---
# <a name="iwiauiextension-interface"></a><span data-ttu-id="97870-103">Interface IWiaUIExtension</span><span class="sxs-lookup"><span data-stu-id="97870-103">IWiaUIExtension interface</span></span>

<span data-ttu-id="97870-104">L’interface **IWiaUIExtension** fournit des méthodes qui remplacent l’interface utilisateur système par défaut, fournissent un logo de bitmap d’appareil personnalisé et fournissent une icône d’appareil personnalisé.</span><span class="sxs-lookup"><span data-stu-id="97870-104">The **IWiaUIExtension** interface provides methods that replace the default system user interface, provide a custom device bitmap logo, and provide a custom device icon.</span></span>

## <a name="members"></a><span data-ttu-id="97870-105">Membres</span><span class="sxs-lookup"><span data-stu-id="97870-105">Members</span></span>

<span data-ttu-id="97870-106">L’interface **IWiaUIExtension** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="97870-106">The **IWiaUIExtension** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="97870-107">**IWiaUIExtension** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="97870-107">**IWiaUIExtension** also has these types of members:</span></span>

-   [<span data-ttu-id="97870-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="97870-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="97870-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="97870-109">Methods</span></span>

<span data-ttu-id="97870-110">L’interface **IWiaUIExtension** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="97870-110">The **IWiaUIExtension** interface has these methods.</span></span>



| <span data-ttu-id="97870-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="97870-111">Method</span></span>                                                                  | <span data-ttu-id="97870-112">Description</span><span class="sxs-lookup"><span data-stu-id="97870-112">Description</span></span>                                                                                  |
|:------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="97870-113">**DeviceDialog**</span><span class="sxs-lookup"><span data-stu-id="97870-113">**DeviceDialog**</span></span>](-wia-iwiauiextension-devicedialog.md)               | <span data-ttu-id="97870-114">Fournit une interface utilisateur personnalisée qui remplace l’interface utilisateur système par défaut.</span><span class="sxs-lookup"><span data-stu-id="97870-114">Provides a custom user interface that replaces the default system user interface.</span></span><br/> |
| [<span data-ttu-id="97870-115">**GetDeviceBitmapLogo**</span><span class="sxs-lookup"><span data-stu-id="97870-115">**GetDeviceBitmapLogo**</span></span>](-wia-iwiauiextension-getdevicebitmaplogo.md) | <span data-ttu-id="97870-116">Obtient un logo de bitmap personnalisé pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="97870-116">Gets a custom bitmap logo for the device.</span></span><br/>                                         |
| [<span data-ttu-id="97870-117">**GetDeviceIcon**</span><span class="sxs-lookup"><span data-stu-id="97870-117">**GetDeviceIcon**</span></span>](-wia-iwiauiextension-getdeviceicon.md)             | <span data-ttu-id="97870-118">Obtient une icône d’appareil personnalisé.</span><span class="sxs-lookup"><span data-stu-id="97870-118">Gets a custom device icon.</span></span><br/>                                                        |



 

## <a name="remarks"></a><span data-ttu-id="97870-119">Notes</span><span class="sxs-lookup"><span data-stu-id="97870-119">Remarks</span></span>



| <span data-ttu-id="97870-120">Méthodes IUnknown</span><span class="sxs-lookup"><span data-stu-id="97870-120">IUnknown Methods</span></span>                                        | <span data-ttu-id="97870-121">Description</span><span class="sxs-lookup"><span data-stu-id="97870-121">Description</span></span>                               |
|---------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="97870-122">[IUnknown :: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span><span class="sxs-lookup"><span data-stu-id="97870-122">[IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span></span> | <span data-ttu-id="97870-123">Retourne des pointeurs aux interfaces prises en charge.</span><span class="sxs-lookup"><span data-stu-id="97870-123">Returns pointers to supported interfaces.</span></span> |
| [<span data-ttu-id="97870-124">IUnknown :: AddRef</span><span class="sxs-lookup"><span data-stu-id="97870-124">IUnknown::AddRef</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | <span data-ttu-id="97870-125">Incrémente le décompte de références.</span><span class="sxs-lookup"><span data-stu-id="97870-125">Increments reference count.</span></span>               |
| [<span data-ttu-id="97870-126">IUnknown :: Release</span><span class="sxs-lookup"><span data-stu-id="97870-126">IUnknown::Release</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | <span data-ttu-id="97870-127">Décrémente le décompte de références.</span><span class="sxs-lookup"><span data-stu-id="97870-127">Decrements reference count.</span></span>               |



 

## <a name="requirements"></a><span data-ttu-id="97870-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="97870-128">Requirements</span></span>



| <span data-ttu-id="97870-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="97870-129">Requirement</span></span> | <span data-ttu-id="97870-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="97870-130">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="97870-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="97870-131">Minimum supported client</span></span><br/> | <span data-ttu-id="97870-132">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="97870-132">Windows XP \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="97870-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="97870-133">Minimum supported server</span></span><br/> | <span data-ttu-id="97870-134">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="97870-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="97870-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="97870-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="97870-136"><dt>Wiadevd. h</dt></span><span class="sxs-lookup"><span data-stu-id="97870-136"><dt>Wiadevd.h</dt></span></span> </dl> |



 

 
