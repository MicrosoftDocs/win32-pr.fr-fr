---
description: Spécifie le type de canal authentifié Direct3D.
ms.assetid: 99a7664e-b0c8-4e66-ad3b-c6ad039ef6eb
title: Énumération D3DAUTHENTICATEDCHANNELTYPE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNELTYPE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 5c0cab8a0a208bfb1a005166740dcc64c319c6e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519239"
---
# <a name="d3dauthenticatedchanneltype-enumeration"></a><span data-ttu-id="aef36-103">Énumération D3DAUTHENTICATEDCHANNELTYPE</span><span class="sxs-lookup"><span data-stu-id="aef36-103">D3DAUTHENTICATEDCHANNELTYPE enumeration</span></span>

<span data-ttu-id="aef36-104">Spécifie le type de canal authentifié Direct3D.</span><span class="sxs-lookup"><span data-stu-id="aef36-104">Specifies the type of Direct3D authenticated channel.</span></span>

## <a name="syntax"></a><span data-ttu-id="aef36-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="aef36-105">Syntax</span></span>


```C++
typedef enum  { 
  D3DAUTHENTICATEDCHANNEL_D3D9             = 1,
  D3DAUTHENTICATEDCHANNEL_DRIVER_SOFTWARE  = 2,
  D3DAUTHENTICATEDCHANNEL_DRIVER_HARDWARE  = 3
} D3DAUTHENTICATEDCHANNELTYPE;
```



## <a name="constants"></a><span data-ttu-id="aef36-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="aef36-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="aef36-107"><span id="D3DAUTHENTICATEDCHANNEL_D3D9"></span><span id="d3dauthenticatedchannel_d3d9"></span>**D3DAUTHENTICATEDCHANNEL \_ d3d9**</span><span class="sxs-lookup"><span data-stu-id="aef36-107"><span id="D3DAUTHENTICATEDCHANNEL_D3D9"></span><span id="d3dauthenticatedchannel_d3d9"></span>**D3DAUTHENTICATEDCHANNEL\_D3D9**</span></span>
</dt> <dd>

<span data-ttu-id="aef36-108">Canal Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="aef36-108">Direct3D 9 channel.</span></span> <span data-ttu-id="aef36-109">Ce canal fournit la communication avec le runtime Direct3D.</span><span class="sxs-lookup"><span data-stu-id="aef36-109">This channel provides communication with the Direct3D runtime.</span></span>

</dd> <dt>

<span data-ttu-id="aef36-110"><span id="D3DAUTHENTICATEDCHANNEL_DRIVER_SOFTWARE"></span><span id="d3dauthenticatedchannel_driver_software"></span>**\_Logiciel du pilote D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="aef36-110"><span id="D3DAUTHENTICATEDCHANNEL_DRIVER_SOFTWARE"></span><span id="d3dauthenticatedchannel_driver_software"></span>**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>
</dt> <dd>

<span data-ttu-id="aef36-111">Canal du pilote de logiciel.</span><span class="sxs-lookup"><span data-stu-id="aef36-111">Software driver channel.</span></span> <span data-ttu-id="aef36-112">Ce canal fournit une communication avec un pilote qui implémente des mécanismes de protection de contenu dans le logiciel.</span><span class="sxs-lookup"><span data-stu-id="aef36-112">This channel provides communication with a driver that implements content protection mechanisms in software.</span></span>

</dd> <dt>

<span data-ttu-id="aef36-113"><span id="D3DAUTHENTICATEDCHANNEL_DRIVER_HARDWARE"></span><span id="d3dauthenticatedchannel_driver_hardware"></span>**\_Matériel du pilote D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="aef36-113"><span id="D3DAUTHENTICATEDCHANNEL_DRIVER_HARDWARE"></span><span id="d3dauthenticatedchannel_driver_hardware"></span>**D3DAUTHENTICATEDCHANNEL\_DRIVER\_HARDWARE**</span></span>
</dt> <dd>

<span data-ttu-id="aef36-114">Canal du pilote matériel.</span><span class="sxs-lookup"><span data-stu-id="aef36-114">Hardware driver channel.</span></span> <span data-ttu-id="aef36-115">Ce canal fournit une communication avec un pilote qui implémente des mécanismes de protection du contenu dans le matériel GPU.</span><span class="sxs-lookup"><span data-stu-id="aef36-115">This channel provides communication with a driver that implements content protection mechanisms in the GPU hardware.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="aef36-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aef36-116">Requirements</span></span>



| <span data-ttu-id="aef36-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="aef36-117">Requirement</span></span> | <span data-ttu-id="aef36-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="aef36-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aef36-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aef36-119">Minimum supported client</span></span><br/> | <span data-ttu-id="aef36-120">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="aef36-120">Windows 7 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="aef36-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aef36-121">Minimum supported server</span></span><br/> | <span data-ttu-id="aef36-122">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="aef36-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="aef36-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="aef36-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="aef36-124"><dt>D3d9types. h (inclure d3d9. h)</dt></span><span class="sxs-lookup"><span data-stu-id="aef36-124"><dt>D3d9types.h (include D3d9.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aef36-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aef36-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aef36-126">Énumérations de vidéos Direct3D</span><span class="sxs-lookup"><span data-stu-id="aef36-126">Direct3D Video Enumerations</span></span>](direct3d-video-enumerations.md)
</dt> <dt>

[<span data-ttu-id="aef36-127">**IDirect3DDevice9Video::CreateAuthenticatedChannel**</span><span class="sxs-lookup"><span data-stu-id="aef36-127">**IDirect3DDevice9Video::CreateAuthenticatedChannel**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel)
</dt> </dl>

 

 




