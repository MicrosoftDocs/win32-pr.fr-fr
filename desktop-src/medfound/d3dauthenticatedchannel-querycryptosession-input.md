---
description: Contient des données d’entrée pour une \_ requête D3DAUTHENTICATEDQUERY CRYPTOSESSION.
ms.assetid: 3a4dead8-fe23-41b4-a167-e0430d09248a
title: Structure D3DAUTHENTICATEDCHANNEL_QUERYCRYPTOSESSION_INPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYCRYPTOSESSION_INPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 76b9d09bcb03dbf3742d551c253d3f4982215757
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104317986"
---
# <a name="d3dauthenticatedchannel_querycryptosession_input-structure"></a><span data-ttu-id="bab1e-103">\_ \_ Structure d’entrée D3DAUTHENTICATEDCHANNEL QUERYCRYPTOSESSION</span><span class="sxs-lookup"><span data-stu-id="bab1e-103">D3DAUTHENTICATEDCHANNEL\_QUERYCRYPTOSESSION\_INPUT structure</span></span>

<span data-ttu-id="bab1e-104">Contient des données d’entrée pour une requête [**D3DAUTHENTICATEDQUERY \_ CRYPTOSESSION**](d3dauthenticatedquery-cryptosession.md) .</span><span class="sxs-lookup"><span data-stu-id="bab1e-104">Contains input data for a [**D3DAUTHENTICATEDQUERY\_CRYPTOSESSION**](d3dauthenticatedquery-cryptosession.md) query.</span></span>

<span data-ttu-id="bab1e-105">Pour envoyer cette requête, appelez [**IDirect3DAuthenticatedChannel9 :: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span><span class="sxs-lookup"><span data-stu-id="bab1e-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="bab1e-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bab1e-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYCRYPTOSESSION_INPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_INPUT Input;
  HANDLE                              DXVA2DecodeHandle;
} D3DAUTHENTICATEDCHANNEL_QUERYCRYPTOSESSION_INPUT;
```



## <a name="members"></a><span data-ttu-id="bab1e-107">Membres</span><span class="sxs-lookup"><span data-stu-id="bab1e-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="bab1e-108">**Entrée**</span><span class="sxs-lookup"><span data-stu-id="bab1e-108">**Input**</span></span>
</dt> <dd>

<span data-ttu-id="bab1e-109">Structure [**\_ \_ d’entrée de requête D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-input.md) qui contient le GUID de la requête et d’autres données.</span><span class="sxs-lookup"><span data-stu-id="bab1e-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**](d3dauthenticatedchannel-query-input.md) structure that contains the GUID for the query and other data.</span></span>

</dd> <dt>

<span data-ttu-id="bab1e-110">**DXVA2DecodeHandle**</span><span class="sxs-lookup"><span data-stu-id="bab1e-110">**DXVA2DecodeHandle**</span></span>
</dt> <dd>

<span data-ttu-id="bab1e-111">Handle vers un appareil de décodage DirectX Video Acceleration 2 (DXVA-2).</span><span class="sxs-lookup"><span data-stu-id="bab1e-111">A handle to a DirectX Video Acceleration 2 (DXVA-2) decoder device.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bab1e-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bab1e-112">Requirements</span></span>



| <span data-ttu-id="bab1e-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bab1e-113">Requirement</span></span> | <span data-ttu-id="bab1e-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="bab1e-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bab1e-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bab1e-115">Minimum supported client</span></span><br/> | <span data-ttu-id="bab1e-116">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bab1e-116">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="bab1e-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bab1e-117">Minimum supported server</span></span><br/> | <span data-ttu-id="bab1e-118">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bab1e-118">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="bab1e-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="bab1e-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="bab1e-120"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="bab1e-120"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bab1e-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bab1e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bab1e-122">Structures vidéo Direct3D</span><span class="sxs-lookup"><span data-stu-id="bab1e-122">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="bab1e-123">**IDirect3DAuthenticatedChannel9 :: Query**</span><span class="sxs-lookup"><span data-stu-id="bab1e-123">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




