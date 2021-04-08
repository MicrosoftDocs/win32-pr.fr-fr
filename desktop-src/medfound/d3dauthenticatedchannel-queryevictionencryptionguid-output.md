---
description: Contient la réponse à une \_ requête D3DAUTHENTICATEDQUERY ENCRYPTIONWHENACCESSIBLEGUID.
ms.assetid: afe73f8e-3304-470c-a37a-17b6c767b2c0
title: Structure D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUID_OUTPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUID_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 8fa46095c5075b0a36ed691978b73de1e7b8cade
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861805"
---
# <a name="d3dauthenticatedchannel_queryevictionencryptionguid_output-structure"></a><span data-ttu-id="0e90b-103">\_Structure de \_ sortie D3DAUTHENTICATEDCHANNEL QUERYEVICTIONENCRYPTIONGUID</span><span class="sxs-lookup"><span data-stu-id="0e90b-103">D3DAUTHENTICATEDCHANNEL\_QUERYEVICTIONENCRYPTIONGUID\_OUTPUT structure</span></span>

<span data-ttu-id="0e90b-104">Contient la réponse à une requête [**D3DAUTHENTICATEDQUERY \_ ENCRYPTIONWHENACCESSIBLEGUID**](d3dauthenticatedquery-encryptionwhenaccessibleguid.md) .</span><span class="sxs-lookup"><span data-stu-id="0e90b-104">Contains the response to a [**D3DAUTHENTICATEDQUERY\_ENCRYPTIONWHENACCESSIBLEGUID**](d3dauthenticatedquery-encryptionwhenaccessibleguid.md) query.</span></span>

<span data-ttu-id="0e90b-105">Pour envoyer cette requête, appelez [**IDirect3DAuthenticatedChannel9 :: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span><span class="sxs-lookup"><span data-stu-id="0e90b-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="0e90b-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0e90b-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUID_OUTPUT {
  Output D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT;
  UINT   EncryptionGuidIndex;
  GUID   EncryptionGuid;
} D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUID_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="0e90b-107">Membres</span><span class="sxs-lookup"><span data-stu-id="0e90b-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="0e90b-108">**Sortie de la \_ requête D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="0e90b-108">**D3DAUTHENTICATEDCHANNEL\_QUERY\_OUTPUT**</span></span>
</dt> <dd>

<span data-ttu-id="0e90b-109">Une structure de [**\_ \_ sortie de requête D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-output.md) contenant un code d’Authentification de message (Mac) et d’autres données.</span><span class="sxs-lookup"><span data-stu-id="0e90b-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_OUTPUT**](d3dauthenticatedchannel-query-output.md) structure that contains a Message Authentication Code (MAC) and other data.</span></span>

</dd> <dt>

<span data-ttu-id="0e90b-110">**EncryptionGuidIndex**</span><span class="sxs-lookup"><span data-stu-id="0e90b-110">**EncryptionGuidIndex**</span></span>
</dt> <dd>

<span data-ttu-id="0e90b-111">Index du GUID de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="0e90b-111">The index of the encryption GUID.</span></span>

</dd> <dt>

<span data-ttu-id="0e90b-112">**EncryptionGuid**</span><span class="sxs-lookup"><span data-stu-id="0e90b-112">**EncryptionGuid**</span></span>
</dt> <dd>

<span data-ttu-id="0e90b-113">GUID qui spécifie un type de chiffrement pris en charge.</span><span class="sxs-lookup"><span data-stu-id="0e90b-113">A GUID that specifies a supported encryption type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0e90b-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0e90b-114">Requirements</span></span>



| <span data-ttu-id="0e90b-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0e90b-115">Requirement</span></span> | <span data-ttu-id="0e90b-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="0e90b-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0e90b-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0e90b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="0e90b-118">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0e90b-118">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="0e90b-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0e90b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="0e90b-120">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0e90b-120">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="0e90b-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="0e90b-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e90b-122"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e90b-122"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e90b-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0e90b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e90b-124">Structures vidéo Direct3D</span><span class="sxs-lookup"><span data-stu-id="0e90b-124">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="0e90b-125">**IDirect3DAuthenticatedChannel9 :: Query**</span><span class="sxs-lookup"><span data-stu-id="0e90b-125">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




