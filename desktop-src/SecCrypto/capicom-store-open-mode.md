---
description: Utilisé avec la méthode Store. Open pour indiquer le mode d’ouverture d’un magasin de certificats.
ms.assetid: 6ec87b8c-9431-4ecc-bd90-943cfe2df1c2
title: Énumération CAPICOM_STORE_OPEN_MODE (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_STORE_OPEN_MODE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 61fe8be0bdf75db5204066563ca07f8225678f7d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526379"
---
# <a name="capicom_store_open_mode-enumeration"></a><span data-ttu-id="aa0b0-103">\_ \_ Énumération du mode d’ouverture d’un magasin CAPICOM \_</span><span class="sxs-lookup"><span data-stu-id="aa0b0-103">CAPICOM\_STORE\_OPEN\_MODE enumeration</span></span>

<span data-ttu-id="aa0b0-104">Le \_ type d’énumération du mode d’ouverture du magasin CAPICOM \_ \_ est utilisé avec la méthode [**Store. Open**](store-open.md) pour indiquer comment un magasin de certificats doit être ouvert.</span><span class="sxs-lookup"><span data-stu-id="aa0b0-104">The CAPICOM\_STORE\_OPEN\_MODE enumeration type is used with the [**Store.Open**](store-open.md) method to indicate how a certificate store is to be opened.</span></span>

## <a name="members"></a><span data-ttu-id="aa0b0-105">Membres</span><span class="sxs-lookup"><span data-stu-id="aa0b0-105">Members</span></span>



| <span data-ttu-id="aa0b0-106">Membre</span><span class="sxs-lookup"><span data-stu-id="aa0b0-106">Member</span></span>                                      | <span data-ttu-id="aa0b0-107">Description</span><span class="sxs-lookup"><span data-stu-id="aa0b0-107">Description</span></span>                                                                                                                                                              | <span data-ttu-id="aa0b0-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="aa0b0-108">Value</span></span> |
|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| <span data-ttu-id="aa0b0-109">**le magasin CAPICOM \_ est \_ ouvert \_ en lecture \_ seule**</span><span class="sxs-lookup"><span data-stu-id="aa0b0-109">**CAPICOM\_STORE\_OPEN\_READ\_ONLY**</span></span>        | <span data-ttu-id="aa0b0-110">Ouvrez le magasin en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="aa0b0-110">Open the store in read-only mode.</span></span><br/>                                                                                                                             | <span data-ttu-id="aa0b0-111">0</span><span class="sxs-lookup"><span data-stu-id="aa0b0-111">0</span></span>     |
| <span data-ttu-id="aa0b0-112">**ouverture de la \_ \_ \_ lecture écriture du \_ magasin CAPICOM**</span><span class="sxs-lookup"><span data-stu-id="aa0b0-112">**CAPICOM\_STORE\_OPEN\_READ\_WRITE**</span></span>       | <span data-ttu-id="aa0b0-113">Ouvrez le magasin en mode lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="aa0b0-113">Open the store in read/write mode.</span></span><br/>                                                                                                                            | <span data-ttu-id="aa0b0-114">1</span><span class="sxs-lookup"><span data-stu-id="aa0b0-114">1</span></span>     |
| <span data-ttu-id="aa0b0-115">**\_ \_ \_ maximum \_ autorisé pour le magasin CAPICOM**</span><span class="sxs-lookup"><span data-stu-id="aa0b0-115">**CAPICOM\_STORE\_OPEN\_MAXIMUM\_ALLOWED**</span></span>  | <span data-ttu-id="aa0b0-116">Ouvre le magasin en mode lecture/écriture si l’utilisateur dispose d’autorisations de lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="aa0b0-116">Open the store in read/write mode if the user has read/write permissions.</span></span> <span data-ttu-id="aa0b0-117">Si l’utilisateur n’a pas d’autorisations de lecture/écriture, ouvrez le magasin en mode lecture seule.</span><span class="sxs-lookup"><span data-stu-id="aa0b0-117">If the user does not have read/write permissions, open the store in read-only mode.</span></span><br/> | <span data-ttu-id="aa0b0-118">2</span><span class="sxs-lookup"><span data-stu-id="aa0b0-118">2</span></span>     |
| <span data-ttu-id="aa0b0-119">**le magasin CAPICOM \_ est \_ ouvert \_ \_ uniquement**</span><span class="sxs-lookup"><span data-stu-id="aa0b0-119">**CAPICOM\_STORE\_OPEN\_EXISTING\_ONLY**</span></span>    | <span data-ttu-id="aa0b0-120">Ouvrir les magasins existants uniquement ; ne créez pas de nouveau magasin.</span><span class="sxs-lookup"><span data-stu-id="aa0b0-120">Open existing stores only; do not create a new store.</span></span> <span data-ttu-id="aa0b0-121">Introduit par CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="aa0b0-121">Introduced by CAPICOM 2.0.</span></span><br/>                                                                              | <span data-ttu-id="aa0b0-122">128</span><span class="sxs-lookup"><span data-stu-id="aa0b0-122">128</span></span>   |
| <span data-ttu-id="aa0b0-123">**l’ouverture du \_ magasin \_ CAPICOM \_ inclut \_ Archived**</span><span class="sxs-lookup"><span data-stu-id="aa0b0-123">**CAPICOM\_STORE\_OPEN\_INCLUDE\_ARCHIVED**</span></span> | <span data-ttu-id="aa0b0-124">Incluez les certificats archivés lors de l’utilisation du magasin.</span><span class="sxs-lookup"><span data-stu-id="aa0b0-124">Include archived certificates when using the store.</span></span> <span data-ttu-id="aa0b0-125">Introduit par CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="aa0b0-125">Introduced by CAPICOM 2.0.</span></span><br/>                                                                                | <span data-ttu-id="aa0b0-126">256</span><span class="sxs-lookup"><span data-stu-id="aa0b0-126">256</span></span>   |



## <a name="remarks"></a><span data-ttu-id="aa0b0-127">Notes</span><span class="sxs-lookup"><span data-stu-id="aa0b0-127">Remarks</span></span>

<span data-ttu-id="aa0b0-128">Lors de l’utilisation de l' \_ \_ énumération du mode d’ouverture d’un magasin CAPICOM \_ , vous pouvez utiliser un seul des paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="aa0b0-128">When using the CAPICOM\_STORE\_OPEN\_MODE enumeration, only one of the following settings can be used.</span></span>

-   <span data-ttu-id="aa0b0-129">le magasin CAPICOM \_ est \_ ouvert \_ en lecture \_ seule</span><span class="sxs-lookup"><span data-stu-id="aa0b0-129">CAPICOM\_STORE\_OPEN\_READ\_ONLY</span></span>
-   <span data-ttu-id="aa0b0-130">ouverture de la \_ \_ \_ lecture écriture du \_ magasin CAPICOM</span><span class="sxs-lookup"><span data-stu-id="aa0b0-130">CAPICOM\_STORE\_OPEN\_READ\_WRITE</span></span>
-   <span data-ttu-id="aa0b0-131">\_ \_ \_ maximum \_ autorisé pour le magasin CAPICOM</span><span class="sxs-lookup"><span data-stu-id="aa0b0-131">CAPICOM\_STORE\_OPEN\_MAXIMUM\_ALLOWED</span></span>

## <a name="requirements"></a><span data-ttu-id="aa0b0-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aa0b0-132">Requirements</span></span>



| <span data-ttu-id="aa0b0-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="aa0b0-133">Requirement</span></span> | <span data-ttu-id="aa0b0-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="aa0b0-134">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="aa0b0-135">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="aa0b0-135">Redistributable</span></span><br/> | <span data-ttu-id="aa0b0-136">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="aa0b0-136">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="aa0b0-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="aa0b0-137">Header</span></span><br/>          | <dl> <span data-ttu-id="aa0b0-138"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa0b0-138"><dt>Capicom.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa0b0-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aa0b0-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa0b0-140">**Store. Open**</span><span class="sxs-lookup"><span data-stu-id="aa0b0-140">**Store.Open**</span></span>](store-open.md)
</dt> </dl>

 

 




