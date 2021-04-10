---
description: 'Contient des données d’entrée pour la méthode IDirect3DAuthenticatedChannel9 :: Query.'
ms.assetid: 6a484652-8da2-4074-96b2-6fe49f4d4200
title: Structure D3DAUTHENTICATEDCHANNEL_QUERY_INPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERY_INPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: a0bec356b20569b5638848407eff27e930ef76b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201164"
---
# <a name="d3dauthenticatedchannel_query_input-structure"></a><span data-ttu-id="8606c-103">\_ \_ Structure d’entrée de la requête D3DAUTHENTICATEDCHANNEL</span><span class="sxs-lookup"><span data-stu-id="8606c-103">D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT structure</span></span>

<span data-ttu-id="8606c-104">Contient des données d’entrée pour la méthode [**IDirect3DAuthenticatedChannel9 :: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query) .</span><span class="sxs-lookup"><span data-stu-id="8606c-104">Contains input data for the [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="8606c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8606c-105">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERY_INPUT {
  GUID           QueryType;
  hChannel       HANDLE;
  SequenceNumber UINT;
} D3DAUTHENTICATEDCHANNEL_QUERY_INPUT;
```



## <a name="members"></a><span data-ttu-id="8606c-106">Membres</span><span class="sxs-lookup"><span data-stu-id="8606c-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="8606c-107">**Affectée**</span><span class="sxs-lookup"><span data-stu-id="8606c-107">**QueryType**</span></span>
</dt> <dd>

<span data-ttu-id="8606c-108">GUID qui spécifie la requête.</span><span class="sxs-lookup"><span data-stu-id="8606c-108">A GUID that specifies the query.</span></span> <span data-ttu-id="8606c-109">Pour obtenir la liste des valeurs, consultez [protection du contenu des requêtes](content-protection-queries.md).</span><span class="sxs-lookup"><span data-stu-id="8606c-109">For a list of values, see [Content Protection Queries](content-protection-queries.md).</span></span>

</dd> <dt>

<span data-ttu-id="8606c-110">**TRAITÉE**</span><span class="sxs-lookup"><span data-stu-id="8606c-110">**HANDLE**</span></span>
</dt> <dd>

<span data-ttu-id="8606c-111">Handle vers le canal authentifié.</span><span class="sxs-lookup"><span data-stu-id="8606c-111">A handle to the authenticated channel.</span></span> <span data-ttu-id="8606c-112">Pour récupérer le handle, appelez [**IDirect3DDevice9Video :: CreateAuthenticatedChannel**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel).</span><span class="sxs-lookup"><span data-stu-id="8606c-112">To get the handle, call [**IDirect3DDevice9Video::CreateAuthenticatedChannel**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel).</span></span>

</dd> <dt>

<span data-ttu-id="8606c-113">**UINT**</span><span class="sxs-lookup"><span data-stu-id="8606c-113">**UINT**</span></span>
</dt> <dd>

<span data-ttu-id="8606c-114">Numéro de séquence de la requête.</span><span class="sxs-lookup"><span data-stu-id="8606c-114">The query sequence number.</span></span> <span data-ttu-id="8606c-115">Au début de la session, générez un nombre aléatoire 32 bits sécurisé par chiffrement à utiliser comme numéro de séquence de départ.</span><span class="sxs-lookup"><span data-stu-id="8606c-115">At the start of the session, generate a cryptographically secure 32-bit random number to use as the starting sequence number.</span></span> <span data-ttu-id="8606c-116">Pour chaque requête, incrémentez le numéro de séquence de 1.</span><span class="sxs-lookup"><span data-stu-id="8606c-116">For each query, increment the sequence number by 1.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8606c-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8606c-117">Requirements</span></span>



| <span data-ttu-id="8606c-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8606c-118">Requirement</span></span> | <span data-ttu-id="8606c-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="8606c-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8606c-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8606c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8606c-121">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8606c-121">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="8606c-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8606c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8606c-123">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8606c-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="8606c-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="8606c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="8606c-125"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="8606c-125"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8606c-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8606c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8606c-127">Structures vidéo Direct3D</span><span class="sxs-lookup"><span data-stu-id="8606c-127">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="8606c-128">**IDirect3DAuthenticatedChannel9 :: Query**</span><span class="sxs-lookup"><span data-stu-id="8606c-128">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




