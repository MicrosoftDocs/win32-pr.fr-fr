---
description: Fournit les fonctionnalités permettant d’obtenir le IMFDXGIDeviceManager à partir du récepteur de rendu vidéo Microsoft Media Foundation.
ms.assetid: 80078ed6-61cc-4fb9-8fd5-eda78cd5be30
title: Interface IMFDXGIDeviceManagerSource
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFDXGIDeviceManagerSource
api_type:
- COM
api_location:
- mfidl.h
ms.openlocfilehash: 669ec840a3122172147840052bd1dbf5c940569d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753189"
---
# <a name="imfdxgidevicemanagersource-interface"></a><span data-ttu-id="6cf05-103">Interface IMFDXGIDeviceManagerSource</span><span class="sxs-lookup"><span data-stu-id="6cf05-103">IMFDXGIDeviceManagerSource interface</span></span>

<span data-ttu-id="6cf05-104">Fournit les fonctionnalités permettant d’obtenir le [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) à partir du récepteur de rendu vidéo Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="6cf05-104">Provides functionality for getting the [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) from the Microsoft Media Foundation video rendering sink.</span></span>

## <a name="members"></a><span data-ttu-id="6cf05-105">Membres</span><span class="sxs-lookup"><span data-stu-id="6cf05-105">Members</span></span>

<span data-ttu-id="6cf05-106">L’interface **IMFDXGIDeviceManagerSource** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="6cf05-106">The **IMFDXGIDeviceManagerSource** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="6cf05-107">**IMFDXGIDeviceManagerSource** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="6cf05-107">**IMFDXGIDeviceManagerSource** also has these types of members:</span></span>

-   [<span data-ttu-id="6cf05-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="6cf05-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="6cf05-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="6cf05-109">Methods</span></span>

<span data-ttu-id="6cf05-110">L’interface **IMFDXGIDeviceManagerSource** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="6cf05-110">The **IMFDXGIDeviceManagerSource** interface has these methods.</span></span>



| <span data-ttu-id="6cf05-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="6cf05-111">Method</span></span>                                                      | <span data-ttu-id="6cf05-112">Description</span><span class="sxs-lookup"><span data-stu-id="6cf05-112">Description</span></span>                                                                                                              |
|:------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6cf05-113">**GetManager**</span><span class="sxs-lookup"><span data-stu-id="6cf05-113">**GetManager**</span></span>](imfdxgidevicemanagersource-getmanager.md) | <span data-ttu-id="6cf05-114">Obtient le [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) à partir du récepteur de rendu vidéo Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="6cf05-114">Gets the [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) from the Media Foundation video rendering sink.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="6cf05-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6cf05-115">Requirements</span></span>



| <span data-ttu-id="6cf05-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6cf05-116">Requirement</span></span> | <span data-ttu-id="6cf05-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="6cf05-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="6cf05-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6cf05-118">Minimum supported client</span></span><br/> | <span data-ttu-id="6cf05-119">\[Applications Windows 8.1 Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="6cf05-119">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="6cf05-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6cf05-120">Minimum supported server</span></span><br/> | <span data-ttu-id="6cf05-121">Applications Windows Server 2012 R2 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="6cf05-121">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                       |
| <span data-ttu-id="6cf05-122">MIDL</span><span class="sxs-lookup"><span data-stu-id="6cf05-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6cf05-123"><dt>Mfidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6cf05-123"><dt>Mfidl.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6cf05-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6cf05-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6cf05-125">Interfaces Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6cf05-125">Media Foundation Interfaces</span></span>](media-foundation-interfaces.md)
</dt> </dl>

 

 
