---
description: Définit les informations à interroger à partir d’un certificat.
ms.assetid: b603c06b-e6d4-4d5d-92b2-3b4f5b93478a
title: Énumération CAPICOM_CERT_INFO_TYPE (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_CERT_INFO_TYPE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 8e38bb8940645bbefecb3822bce8de8c2e0eb902
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528503"
---
# <a name="capicom_cert_info_type-enumeration"></a><span data-ttu-id="f94b0-103">\_ \_ Énumération du type d’informations de certificat CAPICOM \_</span><span class="sxs-lookup"><span data-stu-id="f94b0-103">CAPICOM\_CERT\_INFO\_TYPE enumeration</span></span>

<span data-ttu-id="f94b0-104">Le type d’énumération de **\_ \_ \_ type** d’informations de certificat CAPICOM définit les informations qui doivent être interrogées à partir d’un certificat.</span><span class="sxs-lookup"><span data-stu-id="f94b0-104">The **CAPICOM\_CERT\_INFO\_TYPE** enumeration type defines what information is to be queried from a certificate.</span></span>

## <a name="members"></a><span data-ttu-id="f94b0-105">Membres</span><span class="sxs-lookup"><span data-stu-id="f94b0-105">Members</span></span>



| <span data-ttu-id="f94b0-106">Membre</span><span class="sxs-lookup"><span data-stu-id="f94b0-106">Member</span></span>                                         | <span data-ttu-id="f94b0-107">Description</span><span class="sxs-lookup"><span data-stu-id="f94b0-107">Description</span></span>                                                                                  | <span data-ttu-id="f94b0-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="f94b0-108">Value</span></span> |
|------------------------------------------------|----------------------------------------------------------------------------------------------|-------|
| <span data-ttu-id="f94b0-109">**\_ \_ \_ \_ \_ nom simple de l’objet du certificat CAPICOM**</span><span class="sxs-lookup"><span data-stu-id="f94b0-109">**CAPICOM\_CERT\_INFO\_SUBJECT\_SIMPLE\_NAME**</span></span> | <span data-ttu-id="f94b0-110">Retourne le nom complet de l’objet du certificat.</span><span class="sxs-lookup"><span data-stu-id="f94b0-110">Returns the display name of the certificate subject.</span></span><br/>                              | <span data-ttu-id="f94b0-111">0</span><span class="sxs-lookup"><span data-stu-id="f94b0-111">0</span></span>     |
| <span data-ttu-id="f94b0-112">**\_ \_ \_ \_ \_ nom simple de l’émetteur d’informations de certificat CAPICOM**</span><span class="sxs-lookup"><span data-stu-id="f94b0-112">**CAPICOM\_CERT\_INFO\_ISSUER\_SIMPLE\_NAME**</span></span>  | <span data-ttu-id="f94b0-113">Retourne le nom complet de l’émetteur du certificat.</span><span class="sxs-lookup"><span data-stu-id="f94b0-113">Returns the display name of the issuer of the certificate.</span></span><br/>                        | <span data-ttu-id="f94b0-114">1</span><span class="sxs-lookup"><span data-stu-id="f94b0-114">1</span></span>     |
| <span data-ttu-id="f94b0-115">**nom du message de l’objet de l' \_ information du certificat CAPICOM \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f94b0-115">**CAPICOM\_CERT\_INFO\_SUBJECT\_EMAIL\_NAME**</span></span>  | <span data-ttu-id="f94b0-116">Retourne l’adresse de messagerie de l’objet du certificat.</span><span class="sxs-lookup"><span data-stu-id="f94b0-116">Returns the email address of the certificate subject.</span></span><br/>                             | <span data-ttu-id="f94b0-117">2</span><span class="sxs-lookup"><span data-stu-id="f94b0-117">2</span></span>     |
| <span data-ttu-id="f94b0-118">**nom de messagerie de l' \_ émetteur du certificat CAPICOM \_ info \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f94b0-118">**CAPICOM\_CERT\_INFO\_ISSUER\_EMAIL\_NAME**</span></span>   | <span data-ttu-id="f94b0-119">Retourne l’adresse de messagerie de l’émetteur du certificat.</span><span class="sxs-lookup"><span data-stu-id="f94b0-119">Returns the email address of the issuer of the certificate.</span></span><br/>                       | <span data-ttu-id="f94b0-120">3</span><span class="sxs-lookup"><span data-stu-id="f94b0-120">3</span></span>     |
| <span data-ttu-id="f94b0-121">**UPN de l' \_ \_ objet d’informations de certificat CAPICOM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f94b0-121">**CAPICOM\_CERT\_INFO\_SUBJECT\_UPN**</span></span>          | <span data-ttu-id="f94b0-122">Retourne l’UPN de l’objet du certificat.</span><span class="sxs-lookup"><span data-stu-id="f94b0-122">Returns the UPN of the certificate subject.</span></span> <span data-ttu-id="f94b0-123">Introduit dans CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="f94b0-123">Introduced in CAPICOM 2.0.</span></span><br/>            | <span data-ttu-id="f94b0-124">4</span><span class="sxs-lookup"><span data-stu-id="f94b0-124">4</span></span>     |
| <span data-ttu-id="f94b0-125">**UPN de l' \_ \_ émetteur des informations de certificat CAPICOM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f94b0-125">**CAPICOM\_CERT\_INFO\_ISSUER\_UPN**</span></span>           | <span data-ttu-id="f94b0-126">Retourne l’UPN de l’émetteur du certificat.</span><span class="sxs-lookup"><span data-stu-id="f94b0-126">Returns the UPN of the issuer of the certificate.</span></span> <span data-ttu-id="f94b0-127">Introduit dans CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="f94b0-127">Introduced in CAPICOM 2.0.</span></span><br/>      | <span data-ttu-id="f94b0-128">5</span><span class="sxs-lookup"><span data-stu-id="f94b0-128">5</span></span>     |
| <span data-ttu-id="f94b0-129">**\_ \_ \_ \_ \_ nom DNS de l’objet du certificat CAPICOM**</span><span class="sxs-lookup"><span data-stu-id="f94b0-129">**CAPICOM\_CERT\_INFO\_SUBJECT\_DNS\_NAME**</span></span>    | <span data-ttu-id="f94b0-130">Retourne le nom DNS de l’objet du certificat.</span><span class="sxs-lookup"><span data-stu-id="f94b0-130">Returns the DNS name of the certificate subject.</span></span> <span data-ttu-id="f94b0-131">Introduit dans CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="f94b0-131">Introduced in CAPICOM 2.0.</span></span><br/>       | <span data-ttu-id="f94b0-132">6</span><span class="sxs-lookup"><span data-stu-id="f94b0-132">6</span></span>     |
| <span data-ttu-id="f94b0-133">**\_ \_ \_ \_ nom DNS de l’émetteur CAPICOM informations CERT \_**</span><span class="sxs-lookup"><span data-stu-id="f94b0-133">**CAPICOM\_CERT\_INFO\_ISSUER\_DNS\_NAME**</span></span>     | <span data-ttu-id="f94b0-134">Retourne le nom DNS de l’émetteur du certificat.</span><span class="sxs-lookup"><span data-stu-id="f94b0-134">Returns the DNS name of the issuer of the certificate.</span></span> <span data-ttu-id="f94b0-135">Introduit dans CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="f94b0-135">Introduced in CAPICOM 2.0.</span></span><br/> | <span data-ttu-id="f94b0-136">7</span><span class="sxs-lookup"><span data-stu-id="f94b0-136">7</span></span>     |



## <a name="remarks"></a><span data-ttu-id="f94b0-137">Notes</span><span class="sxs-lookup"><span data-stu-id="f94b0-137">Remarks</span></span>

<span data-ttu-id="f94b0-138">Le type d’énumération de **\_ type d' \_ informations \_ de certificat CAPICOM** est utilisé par la méthode [**Certificate. GetInfo**](certificate-getinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="f94b0-138">The **CAPICOM\_CERT\_INFO\_TYPE** enumeration type is used by the [**Certificate.GetInfo**](certificate-getinfo.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="f94b0-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f94b0-139">Requirements</span></span>



| <span data-ttu-id="f94b0-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f94b0-140">Requirement</span></span> | <span data-ttu-id="f94b0-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="f94b0-141">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f94b0-142">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="f94b0-142">Redistributable</span></span><br/> | <span data-ttu-id="f94b0-143">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="f94b0-143">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="f94b0-144">En-tête</span><span class="sxs-lookup"><span data-stu-id="f94b0-144">Header</span></span><br/>          | <dl> <span data-ttu-id="f94b0-145"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="f94b0-145"><dt>Capicom.h</dt></span></span> </dl> |



 

 




