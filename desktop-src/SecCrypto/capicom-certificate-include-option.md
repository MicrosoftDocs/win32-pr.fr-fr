---
description: Définit les certificats d’une chaîne qui sont enregistrés.
ms.assetid: 6f9e28e6-b01f-4803-8259-8ab73abeecf8
title: Énumération CAPICOM_CERTIFICATE_INCLUDE_OPTION (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_CERTIFICATE_INCLUDE_OPTION
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 45ea9ccf7d3a43e325073f04e28bbd392fa34998
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106534766"
---
# <a name="capicom_certificate_include_option-enumeration"></a><span data-ttu-id="773ec-103">Le certificat CAPICOM \_ \_ inclut l' \_ énumération des options</span><span class="sxs-lookup"><span data-stu-id="773ec-103">CAPICOM\_CERTIFICATE\_INCLUDE\_OPTION enumeration</span></span>

<span data-ttu-id="773ec-104">Le type d’énumération d' **\_ \_ \_ option de certificat CAPICOM** définit les certificats d’une chaîne qui sont enregistrés.</span><span class="sxs-lookup"><span data-stu-id="773ec-104">The **CAPICOM\_CERTIFICATE\_INCLUDE\_OPTION** enumeration type defines which certificates in a chain are saved.</span></span> <span data-ttu-id="773ec-105">Ce type d’énumération a été introduit dans CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="773ec-105">This enumeration type was introduced in CAPICOM 2.0.</span></span>

## <a name="members"></a><span data-ttu-id="773ec-106">Membres</span><span class="sxs-lookup"><span data-stu-id="773ec-106">Members</span></span>



| <span data-ttu-id="773ec-107">Membre</span><span class="sxs-lookup"><span data-stu-id="773ec-107">Member</span></span>                                                 | <span data-ttu-id="773ec-108">Description</span><span class="sxs-lookup"><span data-stu-id="773ec-108">Description</span></span>                                                                           | <span data-ttu-id="773ec-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="773ec-109">Value</span></span> |
|--------------------------------------------------------|---------------------------------------------------------------------------------------|-------|
| <span data-ttu-id="773ec-110">**le certificat CAPICOM \_ \_ inclut une \_ chaîne \_ à l’exception \_ de la racine**</span><span class="sxs-lookup"><span data-stu-id="773ec-110">**CAPICOM\_CERTIFICATE\_INCLUDE\_CHAIN\_EXCEPT\_ROOT**</span></span> | <span data-ttu-id="773ec-111">Enregistre tous les certificats de la chaîne à l’exception de l’entité racine.</span><span class="sxs-lookup"><span data-stu-id="773ec-111">Saves all certificates in the chain with the exception of the root entity.</span></span><br/> | <span data-ttu-id="773ec-112">0</span><span class="sxs-lookup"><span data-stu-id="773ec-112">0</span></span>     |
| <span data-ttu-id="773ec-113">**le certificat CAPICOM \_ \_ inclut une \_ \_ chaîne entière**</span><span class="sxs-lookup"><span data-stu-id="773ec-113">**CAPICOM\_CERTIFICATE\_INCLUDE\_WHOLE\_CHAIN**</span></span>        | <span data-ttu-id="773ec-114">Enregistre la totalité de la chaîne de certificats.</span><span class="sxs-lookup"><span data-stu-id="773ec-114">Saves the complete certificate chain.</span></span><br/>                                      | <span data-ttu-id="773ec-115">1</span><span class="sxs-lookup"><span data-stu-id="773ec-115">1</span></span>     |
| <span data-ttu-id="773ec-116">**le certificat CAPICOM \_ \_ inclut \_ uniquement l' \_ entité \_ end**</span><span class="sxs-lookup"><span data-stu-id="773ec-116">**CAPICOM\_CERTIFICATE\_INCLUDE\_END\_ENTITY\_ONLY**</span></span>   | <span data-ttu-id="773ec-117">Enregistre uniquement le certificat d’entité finale.</span><span class="sxs-lookup"><span data-stu-id="773ec-117">Saves only the end entity certificate.</span></span><br/>                                     | <span data-ttu-id="773ec-118">2</span><span class="sxs-lookup"><span data-stu-id="773ec-118">2</span></span>     |



## <a name="remarks"></a><span data-ttu-id="773ec-119">Notes</span><span class="sxs-lookup"><span data-stu-id="773ec-119">Remarks</span></span>

<span data-ttu-id="773ec-120">Le type d’énumération d' **\_ \_ \_ option de certificat CAPICOM** est utilisé par la méthode [**Certificate. Save**](certificate-save.md) .</span><span class="sxs-lookup"><span data-stu-id="773ec-120">The **CAPICOM\_CERTIFICATE\_INCLUDE\_OPTION** enumeration type is used by the [**Certificate.Save**](certificate-save.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="773ec-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="773ec-121">Requirements</span></span>



| <span data-ttu-id="773ec-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="773ec-122">Requirement</span></span> | <span data-ttu-id="773ec-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="773ec-123">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="773ec-124">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="773ec-124">Redistributable</span></span><br/> | <span data-ttu-id="773ec-125">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="773ec-125">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="773ec-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="773ec-126">Header</span></span><br/>          | <dl> <span data-ttu-id="773ec-127"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="773ec-127"><dt>Capicom.h</dt></span></span> </dl> |



 

 




