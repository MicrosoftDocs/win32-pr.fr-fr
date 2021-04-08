---
description: 'Contient la réponse de la méthode IDirect3DAuthenticatedChannel9 :: Query.'
ms.assetid: b2783b8e-0436-419a-a93e-93dc1b87024d
title: Structure D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 79fe02a483ade1ff60107287799624017496887b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111819"
---
# <a name="d3dauthenticatedchannel_query_output-structure"></a><span data-ttu-id="78d27-103">Structure de sortie de la \_ requête D3DAUTHENTICATEDCHANNEL \_</span><span class="sxs-lookup"><span data-stu-id="78d27-103">D3DAUTHENTICATEDCHANNEL\_QUERY\_OUTPUT structure</span></span>

<span data-ttu-id="78d27-104">Contient la réponse de la méthode [**IDirect3DAuthenticatedChannel9 :: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query) .</span><span class="sxs-lookup"><span data-stu-id="78d27-104">Contains the response from the [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="78d27-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="78d27-105">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT {
  D3D_OMAC       omac;
  GUID           QueryType;
  hChannel       HANDLE;
  SequenceNumber UINT;
  HRESULT        ReturnCode;
} D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="78d27-106">Membres</span><span class="sxs-lookup"><span data-stu-id="78d27-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="78d27-107">**omac**</span><span class="sxs-lookup"><span data-stu-id="78d27-107">**omac**</span></span>
</dt> <dd>

<span data-ttu-id="78d27-108">Structure [**D3D \_ OMAC**](d3d-omac.md) qui contient un code d’Authentification de message (Mac) des données.</span><span class="sxs-lookup"><span data-stu-id="78d27-108">A [**D3D\_OMAC**](d3d-omac.md) structure that contains a Message Authentication Code (MAC) of the data.</span></span> <span data-ttu-id="78d27-109">Le pilote utilise l’algorithme CBC MAC (OMAC) basé sur AES pour calculer cette valeur pour le bloc de données qui s’affiche après ce membre de la structure.</span><span class="sxs-lookup"><span data-stu-id="78d27-109">The driver uses AES-based one-key CBC MAC (OMAC) to calculate this value for the block of data that appears after this structure member.</span></span>

</dd> <dt>

<span data-ttu-id="78d27-110">**Affectée**</span><span class="sxs-lookup"><span data-stu-id="78d27-110">**QueryType**</span></span>
</dt> <dd>

<span data-ttu-id="78d27-111">GUID qui spécifie la requête.</span><span class="sxs-lookup"><span data-stu-id="78d27-111">A GUID that specifies the query.</span></span> <span data-ttu-id="78d27-112">Pour obtenir la liste des valeurs, consultez [protection du contenu des requêtes](content-protection-queries.md).</span><span class="sxs-lookup"><span data-stu-id="78d27-112">For a list of values, see [Content Protection Queries](content-protection-queries.md).</span></span>

</dd> <dt>

<span data-ttu-id="78d27-113">**TRAITÉE**</span><span class="sxs-lookup"><span data-stu-id="78d27-113">**HANDLE**</span></span>
</dt> <dd>

<span data-ttu-id="78d27-114">Handle vers le canal authentifié.</span><span class="sxs-lookup"><span data-stu-id="78d27-114">A handle to the authenticated channel.</span></span>

</dd> <dt>

<span data-ttu-id="78d27-115">**UINT**</span><span class="sxs-lookup"><span data-stu-id="78d27-115">**UINT**</span></span>
</dt> <dd>

<span data-ttu-id="78d27-116">Numéro de séquence de la requête.</span><span class="sxs-lookup"><span data-stu-id="78d27-116">The query sequence number.</span></span>

</dd> <dt>

<span data-ttu-id="78d27-117">**ReturnCode**</span><span class="sxs-lookup"><span data-stu-id="78d27-117">**ReturnCode**</span></span>
</dt> <dd>

<span data-ttu-id="78d27-118">Code de résultat de la requête.</span><span class="sxs-lookup"><span data-stu-id="78d27-118">The result code for the query.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="78d27-119">Notes</span><span class="sxs-lookup"><span data-stu-id="78d27-119">Remarks</span></span>

<span data-ttu-id="78d27-120">Pour **les membres** **QueryType**, **hChannel** et de l’application, le pilote utilise les mêmes valeurs que celles fournies par l’application dans la structure [**\_ \_ d’entrée de requête D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-input.md) .</span><span class="sxs-lookup"><span data-stu-id="78d27-120">For the **QueryType**, **hChannel**, and **SequenceNumber** members, the driver uses in the same values that the application provided in the [**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**](d3dauthenticatedchannel-query-input.md) structure.</span></span> <span data-ttu-id="78d27-121">L’application doit vérifier que ces valeurs correspondent.</span><span class="sxs-lookup"><span data-stu-id="78d27-121">The application should verify that these values match.</span></span>

## <a name="requirements"></a><span data-ttu-id="78d27-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="78d27-122">Requirements</span></span>



| <span data-ttu-id="78d27-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="78d27-123">Requirement</span></span> | <span data-ttu-id="78d27-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="78d27-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="78d27-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="78d27-125">Minimum supported client</span></span><br/> | <span data-ttu-id="78d27-126">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="78d27-126">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="78d27-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="78d27-127">Minimum supported server</span></span><br/> | <span data-ttu-id="78d27-128">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="78d27-128">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="78d27-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="78d27-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="78d27-130"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="78d27-130"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78d27-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="78d27-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78d27-132">Structures vidéo Direct3D</span><span class="sxs-lookup"><span data-stu-id="78d27-132">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="78d27-133">**IDirect3DAuthenticatedChannel9 :: Query**</span><span class="sxs-lookup"><span data-stu-id="78d27-133">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




