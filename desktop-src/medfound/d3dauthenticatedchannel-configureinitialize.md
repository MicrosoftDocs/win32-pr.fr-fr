---
description: Contient des données d’entrée pour une \_ commande D3DAUTHENTICATEDCONFIGURE Initialize.
ms.assetid: 08677cb3-6f08-49d5-a3b6-c48c88516273
title: Structure D3DAUTHENTICATEDCHANNEL_CONFIGUREINITIALIZE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_CONFIGUREINITIALIZE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 072d7886a024b1c28e8c3b7f0609dc8dd3e6add8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033811"
---
# <a name="d3dauthenticatedchannel_configureinitialize-structure"></a><span data-ttu-id="c4812-103">D3DAUTHENTICATEDCHANNEL \_ CONFIGUREINITIALIZE, structure</span><span class="sxs-lookup"><span data-stu-id="c4812-103">D3DAUTHENTICATEDCHANNEL\_CONFIGUREINITIALIZE structure</span></span>

<span data-ttu-id="c4812-104">Contient des données d’entrée pour une commande [**D3DAUTHENTICATEDCONFIGURE \_ Initialize**](d3dauthenticatedconfigure-initialize.md) .</span><span class="sxs-lookup"><span data-stu-id="c4812-104">Contains input data for a [**D3DAUTHENTICATEDCONFIGURE\_INITIALIZE**](d3dauthenticatedconfigure-initialize.md) command.</span></span>

<span data-ttu-id="c4812-105">Pour envoyer cette requête, appelez [**IDirect3DAuthenticatedChannel9 :: configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure).</span><span class="sxs-lookup"><span data-stu-id="c4812-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure).</span></span>

## <a name="syntax"></a><span data-ttu-id="c4812-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c4812-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_CONFIGUREINITIALIZE {
  D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT Parameters;
  UINT                                    StartSequenceQuery;
  UINT                                    StartSequenceConfigure;
} D3DAUTHENTICATEDCHANNEL_CONFIGUREINITIALIZE;
```



## <a name="members"></a><span data-ttu-id="c4812-107">Membres</span><span class="sxs-lookup"><span data-stu-id="c4812-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="c4812-108">**Paramètres**</span><span class="sxs-lookup"><span data-stu-id="c4812-108">**Parameters**</span></span>
</dt> <dd>

<span data-ttu-id="c4812-109">Un [**D3DAUTHENTICATEDCHANNEL \_ configure une structure \_ d’entrée**](d3dauthenticatedchannel-configure-input.md) qui contient le GUID de la commande et d’autres données.</span><span class="sxs-lookup"><span data-stu-id="c4812-109">A [**D3DAUTHENTICATEDCHANNEL\_CONFIGURE\_INPUT**](d3dauthenticatedchannel-configure-input.md) structure that contains the command GUID and other data.</span></span>

</dd> <dt>

<span data-ttu-id="c4812-110">**StartSequenceQuery**</span><span class="sxs-lookup"><span data-stu-id="c4812-110">**StartSequenceQuery**</span></span>
</dt> <dd>

<span data-ttu-id="c4812-111">Numéro de séquence initial pour les requêtes.</span><span class="sxs-lookup"><span data-stu-id="c4812-111">The initial sequence number for queries.</span></span>

</dd> <dt>

<span data-ttu-id="c4812-112">**StartSequenceConfigure**</span><span class="sxs-lookup"><span data-stu-id="c4812-112">**StartSequenceConfigure**</span></span>
</dt> <dd>

<span data-ttu-id="c4812-113">Numéro de séquence initial pour les commandes.</span><span class="sxs-lookup"><span data-stu-id="c4812-113">The initial sequence number for commands.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c4812-114">Notes</span><span class="sxs-lookup"><span data-stu-id="c4812-114">Remarks</span></span>

<span data-ttu-id="c4812-115">Les membres **StartSequenceQuery** et **StartSequenceConfigure** contiennent chacun un nombre aléatoire 32 bits sécurisé par chiffrement.</span><span class="sxs-lookup"><span data-stu-id="c4812-115">The **StartSequenceQuery** and **StartSequenceConfigure** members each contain a cryptographically secure 32-bit random number.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4812-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c4812-116">Requirements</span></span>



| <span data-ttu-id="c4812-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c4812-117">Requirement</span></span> | <span data-ttu-id="c4812-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="c4812-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c4812-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c4812-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c4812-120">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c4812-120">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="c4812-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c4812-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c4812-122">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c4812-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="c4812-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="c4812-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4812-124"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4812-124"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4812-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c4812-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4812-126">Structures vidéo Direct3D</span><span class="sxs-lookup"><span data-stu-id="c4812-126">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="c4812-127">**IDirect3DAuthenticatedChannel9 :: configure**</span><span class="sxs-lookup"><span data-stu-id="c4812-127">**IDirect3DAuthenticatedChannel9::Configure**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




