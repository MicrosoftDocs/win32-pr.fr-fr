---
description: Contient la réponse à une \_ requête de protection D3DAUTHENTICATEDQUERY.
ms.assetid: eb99089a-5e8e-4970-9c40-7f6a9662b5ec
title: Structure D3DAUTHENTICATEDCHANNEL_QUERYPROTECTION_OUTPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYPROTECTION_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: d68cafdf545d93a290e90c54be134977e51de4e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524604"
---
# <a name="d3dauthenticatedchannel_queryprotection_output-structure"></a><span data-ttu-id="ca8cc-103">\_Structure de \_ sortie D3DAUTHENTICATEDCHANNEL QUERYPROTECTION</span><span class="sxs-lookup"><span data-stu-id="ca8cc-103">D3DAUTHENTICATEDCHANNEL\_QUERYPROTECTION\_OUTPUT structure</span></span>

<span data-ttu-id="ca8cc-104">Contient la réponse à une requête de [**\_ protection D3DAUTHENTICATEDQUERY**](d3dauthenticatedquery-protection.md) .</span><span class="sxs-lookup"><span data-stu-id="ca8cc-104">Contains the response to a [**D3DAUTHENTICATEDQUERY\_PROTECTION**](d3dauthenticatedquery-protection.md) query.</span></span>

<span data-ttu-id="ca8cc-105">Pour envoyer cette requête, appelez [**IDirect3DAuthenticatedChannel9 :: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span><span class="sxs-lookup"><span data-stu-id="ca8cc-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="ca8cc-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ca8cc-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYPROTECTION_OUTPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT     Output;
  D3DAUTHENTICATEDCHANNEL_PROTECTION_FLAGS ProtectionFlags;
} D3DAUTHENTICATEDCHANNEL_QUERYPROTECTION_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="ca8cc-107">Membres</span><span class="sxs-lookup"><span data-stu-id="ca8cc-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="ca8cc-108">**Sortie**</span><span class="sxs-lookup"><span data-stu-id="ca8cc-108">**Output**</span></span>
</dt> <dd>

<span data-ttu-id="ca8cc-109">Une structure de [**\_ \_ sortie de requête D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-output.md) contenant un code d’Authentification de message (Mac) et d’autres données.</span><span class="sxs-lookup"><span data-stu-id="ca8cc-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_OUTPUT**](d3dauthenticatedchannel-query-output.md) structure that contains a Message Authentication Code (MAC) and other data.</span></span>

</dd> <dt>

<span data-ttu-id="ca8cc-110">**ProtectionFlags**</span><span class="sxs-lookup"><span data-stu-id="ca8cc-110">**ProtectionFlags**</span></span>
</dt> <dd>

<span data-ttu-id="ca8cc-111">Structure [**d' \_ \_ indicateurs de protection D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-protection-flags.md) qui spécifie le niveau de protection.</span><span class="sxs-lookup"><span data-stu-id="ca8cc-111">A [**D3DAUTHENTICATEDCHANNEL\_PROTECTION\_FLAGS**](d3dauthenticatedchannel-protection-flags.md) structure that specifies the protection level.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ca8cc-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ca8cc-112">Requirements</span></span>



| <span data-ttu-id="ca8cc-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ca8cc-113">Requirement</span></span> | <span data-ttu-id="ca8cc-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="ca8cc-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ca8cc-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ca8cc-115">Minimum supported client</span></span><br/> | <span data-ttu-id="ca8cc-116">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ca8cc-116">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="ca8cc-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ca8cc-117">Minimum supported server</span></span><br/> | <span data-ttu-id="ca8cc-118">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ca8cc-118">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="ca8cc-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="ca8cc-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca8cc-120"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca8cc-120"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca8cc-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ca8cc-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca8cc-122">Structures vidéo Direct3D</span><span class="sxs-lookup"><span data-stu-id="ca8cc-122">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="ca8cc-123">**IDirect3DAuthenticatedChannel9 :: Query**</span><span class="sxs-lookup"><span data-stu-id="ca8cc-123">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




