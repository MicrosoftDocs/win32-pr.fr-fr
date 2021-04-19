---
description: Indique ce qui est vérifié lorsqu’une signature numérique est vérifiée.
ms.assetid: e6259c3f-caed-42f4-832c-250365caa0d7
title: Énumération CAPICOM_SIGNED_DATA_VERIFY_FLAG (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_SIGNED_DATA_VERIFY_FLAG
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: bc8db48ee067e8d12bffa9dbff433384058013b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542687"
---
# <a name="capicom_signed_data_verify_flag-enumeration"></a><span data-ttu-id="f710a-103">\_Énumération de l' \_ \_ indicateur de vérification des données signées CAPICOM \_</span><span class="sxs-lookup"><span data-stu-id="f710a-103">CAPICOM\_SIGNED\_DATA\_VERIFY\_FLAG enumeration</span></span>

<span data-ttu-id="f710a-104">L’énumération de l' **\_ indicateur de \_ \_ vérification \_ des données signées CAPICOM** indique ce qui est vérifié lorsqu’une [*signature numérique*](../secgloss/d-gly.md) est vérifiée.</span><span class="sxs-lookup"><span data-stu-id="f710a-104">The **CAPICOM\_SIGNED\_DATA\_VERIFY\_FLAG** enumeration indicates what is checked when a [*digital signature*](../secgloss/d-gly.md) is verified.</span></span>

## <a name="members"></a><span data-ttu-id="f710a-105">Membres</span><span class="sxs-lookup"><span data-stu-id="f710a-105">Members</span></span>



| <span data-ttu-id="f710a-106">Membre</span><span class="sxs-lookup"><span data-stu-id="f710a-106">Member</span></span>                                           | <span data-ttu-id="f710a-107">Description</span><span class="sxs-lookup"><span data-stu-id="f710a-107">Description</span></span>                                                                                                 | <span data-ttu-id="f710a-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="f710a-108">Value</span></span> |
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------|-------|
| <span data-ttu-id="f710a-109">**\_signature de vérification CAPICOM \_ \_ uniquement**</span><span class="sxs-lookup"><span data-stu-id="f710a-109">**CAPICOM\_VERIFY\_SIGNATURE\_ONLY**</span></span>             | <span data-ttu-id="f710a-110">Seule la signature est vérifiée.</span><span class="sxs-lookup"><span data-stu-id="f710a-110">Only the signature is checked.</span></span><br/>                                                                   | <span data-ttu-id="f710a-111">0</span><span class="sxs-lookup"><span data-stu-id="f710a-111">0</span></span>     |
| <span data-ttu-id="f710a-112">**\_vérification \_ de la signature et du \_ \_ certificat de CAPICOM**</span><span class="sxs-lookup"><span data-stu-id="f710a-112">**CAPICOM\_VERIFY\_SIGNATURE\_AND\_CERTIFICATE**</span></span> | <span data-ttu-id="f710a-113">La signature et la validité du certificat utilisé pour créer la signature sont vérifiées.</span><span class="sxs-lookup"><span data-stu-id="f710a-113">Both the signature and the validity of the certificate used to create the signature are checked.</span></span><br/> | <span data-ttu-id="f710a-114">1</span><span class="sxs-lookup"><span data-stu-id="f710a-114">1</span></span>     |



## <a name="requirements"></a><span data-ttu-id="f710a-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f710a-115">Requirements</span></span>



| <span data-ttu-id="f710a-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f710a-116">Requirement</span></span> | <span data-ttu-id="f710a-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="f710a-117">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f710a-118">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="f710a-118">Redistributable</span></span><br/> | <span data-ttu-id="f710a-119">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="f710a-119">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="f710a-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="f710a-120">Header</span></span><br/>          | <dl> <span data-ttu-id="f710a-121"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="f710a-121"><dt>Capicom.h</dt></span></span> </dl> |



 

 
