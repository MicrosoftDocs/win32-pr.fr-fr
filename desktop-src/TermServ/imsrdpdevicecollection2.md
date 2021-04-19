---
title: Interface IMsRdpDeviceCollection2
description: Représente une collection d’objets périphériques. Il s’agit d’une amélioration de l’interface IMsRdpDeviceCollection.
ms.assetid: df4d704c-e031-4df1-aed1-11aacf8a6992
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de l’interface IMsRdpDeviceCollection2
- Services Bureau à distance de l’interface IMsRdpDeviceCollection2, Description
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ea35c0a66ad8bf5d291062eafb7be3ceae4ac58
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511575"
---
# <a name="imsrdpdevicecollection2-interface"></a><span data-ttu-id="e4e82-106">Interface IMsRdpDeviceCollection2</span><span class="sxs-lookup"><span data-stu-id="e4e82-106">IMsRdpDeviceCollection2 interface</span></span>

<span data-ttu-id="e4e82-107">Représente une collection d’objets périphériques.</span><span class="sxs-lookup"><span data-stu-id="e4e82-107">Represents a collection of device objects.</span></span> <span data-ttu-id="e4e82-108">Il s’agit d’une amélioration de l’interface [**IMsRdpDeviceCollection**](imsrdpdevicecollection.md) .</span><span class="sxs-lookup"><span data-stu-id="e4e82-108">This is an enhancement to the [**IMsRdpDeviceCollection**](imsrdpdevicecollection.md) interface.</span></span>

## <a name="members"></a><span data-ttu-id="e4e82-109">Membres</span><span class="sxs-lookup"><span data-stu-id="e4e82-109">Members</span></span>

<span data-ttu-id="e4e82-110">L’interface **IMsRdpDeviceCollection2** hérite de [**IMsRdpDeviceCollection**](imsrdpdevicecollection.md).</span><span class="sxs-lookup"><span data-stu-id="e4e82-110">The **IMsRdpDeviceCollection2** interface inherits from [**IMsRdpDeviceCollection**](imsrdpdevicecollection.md).</span></span> <span data-ttu-id="e4e82-111">**IMsRdpDeviceCollection2** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="e4e82-111">**IMsRdpDeviceCollection2** also has these types of members:</span></span>

-   [<span data-ttu-id="e4e82-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="e4e82-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="e4e82-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="e4e82-113">Methods</span></span>

<span data-ttu-id="e4e82-114">L’interface **IMsRdpDeviceCollection2** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="e4e82-114">The **IMsRdpDeviceCollection2** interface has these methods.</span></span>



| <span data-ttu-id="e4e82-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="e4e82-115">Method</span></span>                                                                         | <span data-ttu-id="e4e82-116">Description</span><span class="sxs-lookup"><span data-stu-id="e4e82-116">Description</span></span>                                                                                                 |
|:-------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e4e82-117">**AddDeviceByInstanceId**</span><span class="sxs-lookup"><span data-stu-id="e4e82-117">**AddDeviceByInstanceId**</span></span>](imsrdpdevicecollection2-adddevicebyinstanceid.md) | <span data-ttu-id="e4e82-118">Ajoute un appareil non répertorié au regroupement de périphériques.</span><span class="sxs-lookup"><span data-stu-id="e4e82-118">Adds an unlisted device to the device collection.</span></span><br/>                                                |
| [<span data-ttu-id="e4e82-119">**RedirectNow**</span><span class="sxs-lookup"><span data-stu-id="e4e82-119">**RedirectNow**</span></span>](imsrdpdevicecollection2-redirectnow.md)                     | <span data-ttu-id="e4e82-120">Force la redirection ou la suppression des appareils qui ont été sélectionnés ou désélectionnés dans la collection.</span><span class="sxs-lookup"><span data-stu-id="e4e82-120">Forces devices that were selected or unselected from the collection to be redirected or removed.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="e4e82-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e4e82-121">Requirements</span></span>



| <span data-ttu-id="e4e82-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e4e82-122">Requirement</span></span> | <span data-ttu-id="e4e82-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="e4e82-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4e82-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e4e82-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e4e82-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="e4e82-125">Windows 8</span></span><br/>                                                                       |
| <span data-ttu-id="e4e82-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e4e82-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e4e82-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e4e82-127">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="e4e82-128">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="e4e82-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="e4e82-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e4e82-129"><dt>MsTscAx.dll</dt></span></span> </dl>     |
| <span data-ttu-id="e4e82-130">DLL</span><span class="sxs-lookup"><span data-stu-id="e4e82-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e4e82-131"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e4e82-131"><dt>MsTscAx.dll</dt></span></span> </dl>     |
| <span data-ttu-id="e4e82-132">IID</span><span class="sxs-lookup"><span data-stu-id="e4e82-132">IID</span></span><br/>                      | <span data-ttu-id="e4e82-133">IID \_ IMsRdpDeviceCollection2 est défini en tant que e0e5d68a-f2e7-4350-ADFE-ac0e08d74de0</span><span class="sxs-lookup"><span data-stu-id="e4e82-133">IID\_IMsRdpDeviceCollection2 is defined as e0e5d68a-f2e7-4350-adfe-ac0e08d74de0</span></span><br/> |



 

 





