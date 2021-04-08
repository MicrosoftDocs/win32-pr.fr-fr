---
description: Contient la réponse à une \_ requête D3DAUTHENTICATEDQUERY RESTRICTEDSHAREDRESOURCEPROCESSCOUNT.
ms.assetid: dd6286d8-dfb5-413a-ba38-8b99dc8fe305
title: Structure D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESSCOUNT_OUTPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESSCOUNT_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 60568e7056ab9df7aafcec1cac7864685c7c6100
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749316"
---
# <a name="d3dauthenticatedchannel_queryrestrictedsharedresourceprocesscount_output-structure"></a><span data-ttu-id="239d1-103">\_Structure de \_ sortie D3DAUTHENTICATEDCHANNEL QUERYRESTRICTEDSHAREDRESOURCEPROCESSCOUNT</span><span class="sxs-lookup"><span data-stu-id="239d1-103">D3DAUTHENTICATEDCHANNEL\_QUERYRESTRICTEDSHAREDRESOURCEPROCESSCOUNT\_OUTPUT structure</span></span>

<span data-ttu-id="239d1-104">Contient la réponse à une requête [**D3DAUTHENTICATEDQUERY \_ RESTRICTEDSHAREDRESOURCEPROCESSCOUNT**](d3dauthenticatedquery-restrictedsharedresourceprocesscount.md) .</span><span class="sxs-lookup"><span data-stu-id="239d1-104">Contains the response to a [**D3DAUTHENTICATEDQUERY\_RESTRICTEDSHAREDRESOURCEPROCESSCOUNT**](d3dauthenticatedquery-restrictedsharedresourceprocesscount.md) query.</span></span>

<span data-ttu-id="239d1-105">Pour envoyer cette requête, appelez [**IDirect3DAuthenticatedChannel9 :: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span><span class="sxs-lookup"><span data-stu-id="239d1-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="239d1-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="239d1-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESSCOUNT_OUTPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT Output;
  UINT                                 NumRestrictedSharedResourceProcesses;
} D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESSCOUNT_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="239d1-107">Membres</span><span class="sxs-lookup"><span data-stu-id="239d1-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="239d1-108">**Sortie**</span><span class="sxs-lookup"><span data-stu-id="239d1-108">**Output**</span></span>
</dt> <dd>

<span data-ttu-id="239d1-109">Une structure de [**\_ \_ sortie de requête D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-output.md) contenant un code d’Authentification de message (Mac) et d’autres données.</span><span class="sxs-lookup"><span data-stu-id="239d1-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_OUTPUT**](d3dauthenticatedchannel-query-output.md) structure that contains a Message Authentication Code (MAC) and other data.</span></span>

</dd> <dt>

<span data-ttu-id="239d1-110">**NumRestrictedSharedResourceProcesses**</span><span class="sxs-lookup"><span data-stu-id="239d1-110">**NumRestrictedSharedResourceProcesses**</span></span>
</dt> <dd>

<span data-ttu-id="239d1-111">Nombre de processus autorisés à ouvrir des ressources partagées qui ont un accès restreint.</span><span class="sxs-lookup"><span data-stu-id="239d1-111">The number of processes allowed to open shared resources that have restricted access.</span></span> <span data-ttu-id="239d1-112">Un processus ne peut pas ouvrir une telle ressource, sauf si l’accès a été accordé au processus.</span><span class="sxs-lookup"><span data-stu-id="239d1-112">A process cannot open such a resource unless the process has been granted access.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="239d1-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="239d1-113">Requirements</span></span>



| <span data-ttu-id="239d1-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="239d1-114">Requirement</span></span> | <span data-ttu-id="239d1-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="239d1-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="239d1-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="239d1-116">Minimum supported client</span></span><br/> | <span data-ttu-id="239d1-117">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="239d1-117">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="239d1-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="239d1-118">Minimum supported server</span></span><br/> | <span data-ttu-id="239d1-119">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="239d1-119">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="239d1-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="239d1-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="239d1-121"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="239d1-121"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="239d1-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="239d1-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="239d1-123">Structures vidéo Direct3D</span><span class="sxs-lookup"><span data-stu-id="239d1-123">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="239d1-124">**IDirect3DAuthenticatedChannel9 :: Query**</span><span class="sxs-lookup"><span data-stu-id="239d1-124">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




