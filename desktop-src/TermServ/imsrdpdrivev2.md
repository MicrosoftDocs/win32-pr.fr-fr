---
title: Interface IMsRdpDriveV2
description: Contient des informations sur un objet lecteur. Il s’agit d’une amélioration de l’interface IMsRdpDrive.
ms.assetid: 0d804fcc-960f-48f7-9794-b7be8d7e258e
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de l’interface IMsRdpDriveV2
- Services Bureau à distance de l’interface IMsRdpDriveV2, Description
topic_type:
- apiref
api_name:
- IMsRdpDriveV2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7c397e96d4f3b0dbb172c6e10eba4e09ff96e37
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103085"
---
# <a name="imsrdpdrivev2-interface"></a><span data-ttu-id="17248-106">Interface IMsRdpDriveV2</span><span class="sxs-lookup"><span data-stu-id="17248-106">IMsRdpDriveV2 interface</span></span>

<span data-ttu-id="17248-107">Contient des informations sur un objet lecteur.</span><span class="sxs-lookup"><span data-stu-id="17248-107">Contains information about a drive object.</span></span> <span data-ttu-id="17248-108">Il s’agit d’une amélioration de l’interface [**IMsRdpDrive**](imsrdpdrive.md) .</span><span class="sxs-lookup"><span data-stu-id="17248-108">This is an enhancement of the [**IMsRdpDrive**](imsrdpdrive.md) interface.</span></span>

## <a name="members"></a><span data-ttu-id="17248-109">Membres</span><span class="sxs-lookup"><span data-stu-id="17248-109">Members</span></span>

<span data-ttu-id="17248-110">L’interface **IMsRdpDriveV2** hérite de [**IMsRdpDrive**](imsrdpdrive.md).</span><span class="sxs-lookup"><span data-stu-id="17248-110">The **IMsRdpDriveV2** interface inherits from [**IMsRdpDrive**](imsrdpdrive.md).</span></span> <span data-ttu-id="17248-111">**IMsRdpDriveV2** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="17248-111">**IMsRdpDriveV2** also has these types of members:</span></span>

-   [<span data-ttu-id="17248-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="17248-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="17248-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="17248-113">Properties</span></span>

<span data-ttu-id="17248-114">L’interface **IMsRdpDriveV2** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="17248-114">The **IMsRdpDriveV2** interface has these properties.</span></span>



| <span data-ttu-id="17248-115">Propriété</span><span class="sxs-lookup"><span data-stu-id="17248-115">Property</span></span>                                                              | <span data-ttu-id="17248-116">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="17248-116">Access type</span></span>          | <span data-ttu-id="17248-117">Description</span><span class="sxs-lookup"><span data-stu-id="17248-117">Description</span></span>                                                |
|:----------------------------------------------------------------------|:---------------------|:-----------------------------------------------------------|
| [<span data-ttu-id="17248-118">**DriveLetterIndex**</span><span class="sxs-lookup"><span data-stu-id="17248-118">**DriveLetterIndex**</span></span>](imsrdpdrivev2-driveletterindex.md)<br/> | <span data-ttu-id="17248-119">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="17248-119">Read-only</span></span><br/> | <span data-ttu-id="17248-120">Contient l’index de la lettre du lecteur.</span><span class="sxs-lookup"><span data-stu-id="17248-120">Contains the index of the letter for the drive.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="17248-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="17248-121">Requirements</span></span>



| <span data-ttu-id="17248-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="17248-122">Requirement</span></span> | <span data-ttu-id="17248-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="17248-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="17248-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="17248-124">Minimum supported client</span></span><br/> | <span data-ttu-id="17248-125">Windows 7 avec SP1</span><span class="sxs-lookup"><span data-stu-id="17248-125">Windows 7 with SP1</span></span><br/>                                                          |
| <span data-ttu-id="17248-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="17248-126">Minimum supported server</span></span><br/> | <span data-ttu-id="17248-127">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="17248-127">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="17248-128">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="17248-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="17248-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17248-129"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="17248-130">DLL</span><span class="sxs-lookup"><span data-stu-id="17248-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17248-131"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17248-131"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="17248-132">IID</span><span class="sxs-lookup"><span data-stu-id="17248-132">IID</span></span><br/>                      | <span data-ttu-id="17248-133">IID \_ IMsRdpDriveV2 est défini en tant que 3e05417c-2721-4008-9d80-4edf1539c817</span><span class="sxs-lookup"><span data-stu-id="17248-133">IID\_IMsRdpDriveV2 is defined as 3e05417c-2721-4008-9d80-4edf1539c817</span></span><br/>       |



 

 





