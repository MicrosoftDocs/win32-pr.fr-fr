---
description: Représente un accélérateur matériel pour DirectX Video Acceleration (DXVA) 1,0.
ms.assetid: 63f77cf9-4c04-4ddb-9582-cfcf86f66a2a
title: Interface IDirect3DDXVADevice9 (DXVA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DDXVADevice9
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: 192f47b8161893f9517bc976452eb8836da4bb53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533847"
---
# <a name="idirect3ddxvadevice9-interface"></a><span data-ttu-id="c0ff9-103">Interface IDirect3DDXVADevice9</span><span class="sxs-lookup"><span data-stu-id="c0ff9-103">IDirect3DDXVADevice9 interface</span></span>

<span data-ttu-id="c0ff9-104">Représente un accélérateur matériel pour DirectX Video Acceleration (DXVA) 1,0.</span><span class="sxs-lookup"><span data-stu-id="c0ff9-104">Represents a hardware accelerator for DirectX Video Acceleration (DXVA) 1.0.</span></span>

## <a name="members"></a><span data-ttu-id="c0ff9-105">Membres</span><span class="sxs-lookup"><span data-stu-id="c0ff9-105">Members</span></span>

<span data-ttu-id="c0ff9-106">L’interface **IDirect3DDXVADevice9** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="c0ff9-106">The **IDirect3DDXVADevice9** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="c0ff9-107">**IDirect3DDXVADevice9** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="c0ff9-107">**IDirect3DDXVADevice9** also has these types of members:</span></span>

-   [<span data-ttu-id="c0ff9-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="c0ff9-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="c0ff9-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="c0ff9-109">Methods</span></span>

<span data-ttu-id="c0ff9-110">L’interface **IDirect3DDXVADevice9** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="c0ff9-110">The **IDirect3DDXVADevice9** interface has these methods.</span></span>



| <span data-ttu-id="c0ff9-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="c0ff9-111">Method</span></span>                                                  | <span data-ttu-id="c0ff9-112">Description</span><span class="sxs-lookup"><span data-stu-id="c0ff9-112">Description</span></span>                                                           |
|:--------------------------------------------------------|:----------------------------------------------------------------------|
| [<span data-ttu-id="c0ff9-113">**BeginFrame**</span><span class="sxs-lookup"><span data-stu-id="c0ff9-113">**BeginFrame**</span></span>](idirect3ddxvadevice9-beginframe.md)   | <span data-ttu-id="c0ff9-114">Commence le traitement pour créer une image décodée.</span><span class="sxs-lookup"><span data-stu-id="c0ff9-114">Begins the processing to create a decoded picture.</span></span><br/>         |
| [<span data-ttu-id="c0ff9-115">**EndFrame**</span><span class="sxs-lookup"><span data-stu-id="c0ff9-115">**EndFrame**</span></span>](idirect3ddxvadevice9-endframe.md)       | <span data-ttu-id="c0ff9-116">Termine le traitement pour créer une image décodée.</span><span class="sxs-lookup"><span data-stu-id="c0ff9-116">Ends the processing to create a decoded picture.</span></span><br/>           |
| [<span data-ttu-id="c0ff9-117">**Execute**</span><span class="sxs-lookup"><span data-stu-id="c0ff9-117">**Execute**</span></span>](idirect3ddxvadevice9-execute.md)         | <span data-ttu-id="c0ff9-118">Effectue une opération de décodage DXVA.</span><span class="sxs-lookup"><span data-stu-id="c0ff9-118">Performs a DXVA decoding operation.</span></span> <br/>                       |
| [<span data-ttu-id="c0ff9-119">**QueryStatus**</span><span class="sxs-lookup"><span data-stu-id="c0ff9-119">**QueryStatus**</span></span>](idirect3ddxvadevice9-querystatus.md) | <span data-ttu-id="c0ff9-120">Interroge l’État lecture/écriture d’une surface de décodage DXVA.</span><span class="sxs-lookup"><span data-stu-id="c0ff9-120">Queries the read/write status of a DXVA decoding surface.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="c0ff9-121">Notes</span><span class="sxs-lookup"><span data-stu-id="c0ff9-121">Remarks</span></span>

<span data-ttu-id="c0ff9-122">Pour obtenir un pointeur vers cette interface, appelez [**IDirect3DVideoDevice9 :: CreateDXVADevice**](idirect3dvideodevice9-createdxvadevice.md).</span><span class="sxs-lookup"><span data-stu-id="c0ff9-122">To get a pointer to this interface, call [**IDirect3DVideoDevice9::CreateDXVADevice**](idirect3dvideodevice9-createdxvadevice.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c0ff9-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c0ff9-123">Requirements</span></span>



| <span data-ttu-id="c0ff9-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c0ff9-124">Requirement</span></span> | <span data-ttu-id="c0ff9-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="c0ff9-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="c0ff9-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c0ff9-126">Minimum supported client</span></span><br/> | <span data-ttu-id="c0ff9-127">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c0ff9-127">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c0ff9-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c0ff9-128">Minimum supported server</span></span><br/> | <span data-ttu-id="c0ff9-129">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c0ff9-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="c0ff9-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="c0ff9-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0ff9-131"><dt>DXVA. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0ff9-131"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0ff9-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c0ff9-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0ff9-133">Interfaces vidéo Direct3D</span><span class="sxs-lookup"><span data-stu-id="c0ff9-133">Direct3D Video Interfaces</span></span>](direct3d-video-interfaces.md)
</dt> </dl>

 

 
