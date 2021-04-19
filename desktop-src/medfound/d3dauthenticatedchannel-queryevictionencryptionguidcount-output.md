---
description: Contient la réponse à une \_ requête D3DAUTHENTICATEDQUERY ENCRYPTIONWHENACCESSIBLEGUIDCOUNT.
ms.assetid: 168f9455-8dc6-473a-ad2c-e51996b63650
title: Structure D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUIDCOUNT_OUTPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUIDCOUNT_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 51668dccdfa15649ec2a062a1231eb0b16e68ff8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527597"
---
# <a name="d3dauthenticatedchannel_queryevictionencryptionguidcount_output-structure"></a><span data-ttu-id="441e8-103">\_Structure de \_ sortie D3DAUTHENTICATEDCHANNEL QUERYEVICTIONENCRYPTIONGUIDCOUNT</span><span class="sxs-lookup"><span data-stu-id="441e8-103">D3DAUTHENTICATEDCHANNEL\_QUERYEVICTIONENCRYPTIONGUIDCOUNT\_OUTPUT structure</span></span>

<span data-ttu-id="441e8-104">Contient la réponse à une requête [**D3DAUTHENTICATEDQUERY \_ ENCRYPTIONWHENACCESSIBLEGUIDCOUNT**](d3dauthenticatedquery-encryptionwhenaccessibleguidcount.md) .</span><span class="sxs-lookup"><span data-stu-id="441e8-104">Contains the response to a [**D3DAUTHENTICATEDQUERY\_ENCRYPTIONWHENACCESSIBLEGUIDCOUNT**](d3dauthenticatedquery-encryptionwhenaccessibleguidcount.md) query.</span></span>

<span data-ttu-id="441e8-105">Pour envoyer cette requête, appelez [**IDirect3DAuthenticatedChannel9 :: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span><span class="sxs-lookup"><span data-stu-id="441e8-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="441e8-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="441e8-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUIDCOUNT_OUTPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT Output;
  NumEncryptionGuids                   UINT;
} D3DAUTHENTICATEDCHANNEL_QUERYEVICTIONENCRYPTIONGUIDCOUNT_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="441e8-107">Membres</span><span class="sxs-lookup"><span data-stu-id="441e8-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="441e8-108">**Sortie**</span><span class="sxs-lookup"><span data-stu-id="441e8-108">**Output**</span></span>
</dt> <dd>

<span data-ttu-id="441e8-109">Une structure de [**\_ \_ sortie de requête D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-output.md) contenant un code d’Authentification de message (Mac) et d’autres données.</span><span class="sxs-lookup"><span data-stu-id="441e8-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_OUTPUT**](d3dauthenticatedchannel-query-output.md) structure that contains a Message Authentication Code (MAC) and other data.</span></span>

</dd> <dt>

<span data-ttu-id="441e8-110">**UINT**</span><span class="sxs-lookup"><span data-stu-id="441e8-110">**UINT**</span></span>
</dt> <dd>

<span data-ttu-id="441e8-111">Nombre de GUID de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="441e8-111">The number of encryption GUIDs.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="441e8-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="441e8-112">Requirements</span></span>



| <span data-ttu-id="441e8-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="441e8-113">Requirement</span></span> | <span data-ttu-id="441e8-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="441e8-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="441e8-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="441e8-115">Minimum supported client</span></span><br/> | <span data-ttu-id="441e8-116">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="441e8-116">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="441e8-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="441e8-117">Minimum supported server</span></span><br/> | <span data-ttu-id="441e8-118">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="441e8-118">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="441e8-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="441e8-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="441e8-120"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="441e8-120"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="441e8-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="441e8-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="441e8-122">Structures vidéo Direct3D</span><span class="sxs-lookup"><span data-stu-id="441e8-122">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="441e8-123">**IDirect3DAuthenticatedChannel9 :: Query**</span><span class="sxs-lookup"><span data-stu-id="441e8-123">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




