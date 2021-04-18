---
description: Définit le type d’attribut associé à une signature.
ms.assetid: 94f0dce4-0b32-4c39-ab2e-b01795432acd
title: Énumération CAPICOM_ATTRIBUTE (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_ATTRIBUTE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: b03f91d0737b29b98adeb7e6a56bf9eccd35cc8f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533193"
---
# <a name="capicom_attribute-enumeration"></a><span data-ttu-id="45a98-103">CAPICOM ( \_ énumération d’attribut)</span><span class="sxs-lookup"><span data-stu-id="45a98-103">CAPICOM\_ATTRIBUTE enumeration</span></span>

<span data-ttu-id="45a98-104">Le type d’énumération d' **\_ attribut CAPICOM** définit le type d’attribut associé à une [*signature*](../secgloss/d-gly.md).</span><span class="sxs-lookup"><span data-stu-id="45a98-104">The **CAPICOM\_ATTRIBUTE** enumeration type defines the kind of attribute associated with a [*signature*](../secgloss/d-gly.md).</span></span>

## <a name="members"></a><span data-ttu-id="45a98-105">Membres</span><span class="sxs-lookup"><span data-stu-id="45a98-105">Members</span></span>



| <span data-ttu-id="45a98-106">Membre</span><span class="sxs-lookup"><span data-stu-id="45a98-106">Member</span></span>                                                       | <span data-ttu-id="45a98-107">Description</span><span class="sxs-lookup"><span data-stu-id="45a98-107">Description</span></span>                                                                | <span data-ttu-id="45a98-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="45a98-108">Value</span></span> |
|--------------------------------------------------------------|----------------------------------------------------------------------------|-------|
| <span data-ttu-id="45a98-109">**\_heure de signature de l' \_ attribut \_ authentifié \_ CAPICOM**</span><span class="sxs-lookup"><span data-stu-id="45a98-109">**CAPICOM\_AUTHENTICATED\_ATTRIBUTE\_SIGNING\_TIME**</span></span>         | <span data-ttu-id="45a98-110">L’attribut contient l’heure à laquelle la signature a été créée.</span><span class="sxs-lookup"><span data-stu-id="45a98-110">The attribute contains the time that the signature was created.</span></span><br/> | <span data-ttu-id="45a98-111">0</span><span class="sxs-lookup"><span data-stu-id="45a98-111">0</span></span>     |
| <span data-ttu-id="45a98-112">**\_nom du document de l' \_ attribut \_ authentifié \_ CAPICOM**</span><span class="sxs-lookup"><span data-stu-id="45a98-112">**CAPICOM\_AUTHENTICATED\_ATTRIBUTE\_DOCUMENT\_NAME**</span></span>        | <span data-ttu-id="45a98-113">L’attribut contient le nom du document signé.</span><span class="sxs-lookup"><span data-stu-id="45a98-113">The attribute contains the name of the signed document.</span></span><br/>         | <span data-ttu-id="45a98-114">1</span><span class="sxs-lookup"><span data-stu-id="45a98-114">1</span></span>     |
| <span data-ttu-id="45a98-115">**\_Description du document de l' \_ attribut \_ authentifié \_ CAPICOM**</span><span class="sxs-lookup"><span data-stu-id="45a98-115">**CAPICOM\_AUTHENTICATED\_ATTRIBUTE\_DOCUMENT\_DESCRIPTION**</span></span> | <span data-ttu-id="45a98-116">L’attribut contient une description du document signé.</span><span class="sxs-lookup"><span data-stu-id="45a98-116">The attribute contains a description of the signed document.</span></span><br/>    | <span data-ttu-id="45a98-117">2</span><span class="sxs-lookup"><span data-stu-id="45a98-117">2</span></span>     |



## <a name="remarks"></a><span data-ttu-id="45a98-118">Notes</span><span class="sxs-lookup"><span data-stu-id="45a98-118">Remarks</span></span>

<span data-ttu-id="45a98-119">Le type d’énumération d' **\_ attribut CAPICOM** est utilisé par la propriété [**attribute.Name**](attribute-name.md) .</span><span class="sxs-lookup"><span data-stu-id="45a98-119">The **CAPICOM\_ATTRIBUTE** enumeration type is used by the [**Attribute.Name**](attribute-name.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="45a98-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="45a98-120">Requirements</span></span>



| <span data-ttu-id="45a98-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="45a98-121">Requirement</span></span> | <span data-ttu-id="45a98-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="45a98-122">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="45a98-123">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="45a98-123">Redistributable</span></span><br/> | <span data-ttu-id="45a98-124">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="45a98-124">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="45a98-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="45a98-125">Header</span></span><br/>          | <dl> <span data-ttu-id="45a98-126"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="45a98-126"><dt>Capicom.h</dt></span></span> </dl> |



 

 
