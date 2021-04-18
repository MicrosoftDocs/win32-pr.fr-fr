---
description: L' \_ énumération des spécifications de clé CAPICOM \_ définit les spécifications de clé.
ms.assetid: e4aaaf69-ab28-4e8c-8a8a-6dc662299865
title: Énumération CAPICOM_KEY_SPEC (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_KEY_SPEC
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 153f0431d78ff595b4d568fd7a677abea0d28be7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532851"
---
# <a name="capicom_key_spec-enumeration"></a><span data-ttu-id="13656-103">\_Énumération des spécifications de clé CAPICOM \_</span><span class="sxs-lookup"><span data-stu-id="13656-103">CAPICOM\_KEY\_SPEC enumeration</span></span>

<span data-ttu-id="13656-104">L’énumération des **\_ \_ spécifications de clé CAPICOM** définit les spécifications de clé.</span><span class="sxs-lookup"><span data-stu-id="13656-104">The **CAPICOM\_KEY\_SPEC** enumeration defines key specifications.</span></span>

## <a name="members"></a><span data-ttu-id="13656-105">Membres</span><span class="sxs-lookup"><span data-stu-id="13656-105">Members</span></span>



| <span data-ttu-id="13656-106">Membre</span><span class="sxs-lookup"><span data-stu-id="13656-106">Member</span></span>                              | <span data-ttu-id="13656-107">Description</span><span class="sxs-lookup"><span data-stu-id="13656-107">Description</span></span>                                                | <span data-ttu-id="13656-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="13656-108">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|-------|
| <span data-ttu-id="13656-109">**clé d’échange de la \_ spécification de clé CAPICOM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="13656-109">**CAPICOM\_KEY\_SPEC\_KEYEXCHANGE**</span></span> | <span data-ttu-id="13656-110">La clé peut être utilisée pour le chiffrement et la signature.</span><span class="sxs-lookup"><span data-stu-id="13656-110">The key can be used for encryption and signing.</span></span><br/> | <span data-ttu-id="13656-111">1</span><span class="sxs-lookup"><span data-stu-id="13656-111">1</span></span>     |
| <span data-ttu-id="13656-112">**SIGNATURE de la \_ spécification de clé CAPICOM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="13656-112">**CAPICOM\_KEY\_SPEC\_SIGNATURE**</span></span>   | <span data-ttu-id="13656-113">La clé peut être utilisée uniquement pour la signature.</span><span class="sxs-lookup"><span data-stu-id="13656-113">The key can be used only for signing.</span></span><br/>           | <span data-ttu-id="13656-114">2</span><span class="sxs-lookup"><span data-stu-id="13656-114">2</span></span>     |



## <a name="remarks"></a><span data-ttu-id="13656-115">Notes</span><span class="sxs-lookup"><span data-stu-id="13656-115">Remarks</span></span>

<span data-ttu-id="13656-116">L’énumération des **\_ \_ spécifications de clé CAPICOM** est utilisée par les propriétés et méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="13656-116">The **CAPICOM\_KEY\_SPEC** enumeration is used by the following methods and properties:</span></span>

-   <span data-ttu-id="13656-117">Propriété [**PrivateKey. KeySpec**](privatekey-keyspec.md) .</span><span class="sxs-lookup"><span data-stu-id="13656-117">[**PrivateKey.KeySpec**](privatekey-keyspec.md) property.</span></span>
-   <span data-ttu-id="13656-118">Méthode [**PrivateKey. Open**](privatekey-open.md) .</span><span class="sxs-lookup"><span data-stu-id="13656-118">[**PrivateKey.Open**](privatekey-open.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="13656-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="13656-119">Requirements</span></span>



| <span data-ttu-id="13656-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="13656-120">Requirement</span></span> | <span data-ttu-id="13656-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="13656-121">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="13656-122">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="13656-122">Redistributable</span></span><br/> | <span data-ttu-id="13656-123">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="13656-123">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="13656-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="13656-124">Header</span></span><br/>          | <dl> <span data-ttu-id="13656-125"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="13656-125"><dt>Capicom.h</dt></span></span> </dl> |



 

 




