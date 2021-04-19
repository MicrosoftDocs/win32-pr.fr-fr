---
description: L' \_ énumération de l’indicateur de stockage de clé CAPICOM définit des indicateurs de stockage de \_ \_ clé.
ms.assetid: 326cef75-24a5-4dc9-a7e9-a63dd3d8de54
title: Énumération CAPICOM_KEY_STORAGE_FLAG (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_KEY_STORAGE_FLAG
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 9edbc3a5ac3396e528ebbb5390c4b07c24770e58
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520906"
---
# <a name="capicom_key_storage_flag-enumeration"></a><span data-ttu-id="fad2e-103">\_Énumération de l' \_ indicateur de stockage de clé CAPICOM \_</span><span class="sxs-lookup"><span data-stu-id="fad2e-103">CAPICOM\_KEY\_STORAGE\_FLAG enumeration</span></span>

<span data-ttu-id="fad2e-104">L’énumération de l' **\_ indicateur de \_ stockage \_ de clé CAPICOM** définit des indicateurs de stockage de clé.</span><span class="sxs-lookup"><span data-stu-id="fad2e-104">The **CAPICOM\_KEY\_STORAGE\_FLAG** enumeration defines key storage flags.</span></span>

## <a name="members"></a><span data-ttu-id="fad2e-105">Membres</span><span class="sxs-lookup"><span data-stu-id="fad2e-105">Members</span></span>



| <span data-ttu-id="fad2e-106">Membre</span><span class="sxs-lookup"><span data-stu-id="fad2e-106">Member</span></span>                                     | <span data-ttu-id="fad2e-107">Description</span><span class="sxs-lookup"><span data-stu-id="fad2e-107">Description</span></span>                           | <span data-ttu-id="fad2e-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="fad2e-108">Value</span></span> |
|--------------------------------------------|---------------------------------------|-------|
| <span data-ttu-id="fad2e-109">**\_ \_ \_ valeur par défaut du stockage de la clé CAPICOM**</span><span class="sxs-lookup"><span data-stu-id="fad2e-109">**CAPICOM\_KEY\_STORAGE\_DEFAULT**</span></span>         | <span data-ttu-id="fad2e-110">Stockage de clé par défaut.</span><span class="sxs-lookup"><span data-stu-id="fad2e-110">Default key storage.</span></span><br/>       | <span data-ttu-id="fad2e-111">0</span><span class="sxs-lookup"><span data-stu-id="fad2e-111">0</span></span>     |
| <span data-ttu-id="fad2e-112">**\_espace de stockage de clé CAPICOM \_ \_ exportable**</span><span class="sxs-lookup"><span data-stu-id="fad2e-112">**CAPICOM\_KEY\_STORAGE\_EXPORTABLE**</span></span>      | <span data-ttu-id="fad2e-113">La clé peut être exportée.</span><span class="sxs-lookup"><span data-stu-id="fad2e-113">The key is exportable.</span></span><br/>     | <span data-ttu-id="fad2e-114">1</span><span class="sxs-lookup"><span data-stu-id="fad2e-114">1</span></span>     |
| <span data-ttu-id="fad2e-115">**\_clé CAPICOM \_ \_ protégée par l’utilisateur \_**</span><span class="sxs-lookup"><span data-stu-id="fad2e-115">**CAPICOM\_KEY\_STORAGE\_USER\_PROTECTED**</span></span> | <span data-ttu-id="fad2e-116">La clé est protégée par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="fad2e-116">The key is user protected.</span></span><br/> | <span data-ttu-id="fad2e-117">2</span><span class="sxs-lookup"><span data-stu-id="fad2e-117">2</span></span>     |



## <a name="remarks"></a><span data-ttu-id="fad2e-118">Notes</span><span class="sxs-lookup"><span data-stu-id="fad2e-118">Remarks</span></span>

<span data-ttu-id="fad2e-119">Cette énumération est utilisée par la méthode suivante :</span><span class="sxs-lookup"><span data-stu-id="fad2e-119">This enumeration is used by the following method:</span></span>

-   [<span data-ttu-id="fad2e-120">**Certificate. Load**</span><span class="sxs-lookup"><span data-stu-id="fad2e-120">**Certificate.Load**</span></span>](certificate-load.md)
-   [<span data-ttu-id="fad2e-121">**Store. Load**</span><span class="sxs-lookup"><span data-stu-id="fad2e-121">**Store.Load**</span></span>](store-load.md)

## <a name="requirements"></a><span data-ttu-id="fad2e-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fad2e-122">Requirements</span></span>



| <span data-ttu-id="fad2e-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fad2e-123">Requirement</span></span> | <span data-ttu-id="fad2e-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="fad2e-124">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="fad2e-125">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="fad2e-125">Redistributable</span></span><br/> | <span data-ttu-id="fad2e-126">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="fad2e-126">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="fad2e-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="fad2e-127">Header</span></span><br/>          | <dl> <span data-ttu-id="fad2e-128"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="fad2e-128"><dt>Capicom.h</dt></span></span> </dl> |



 

 




