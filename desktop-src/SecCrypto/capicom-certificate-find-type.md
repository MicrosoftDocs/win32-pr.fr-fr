---
description: Le \_ \_ \_ type d’énumération de type d’énumération de certificat CAPICOM définit le type de critère de recherche utilisé pour rechercher des certificats spécifiques. Ce type d’énumération a été introduit dans CAPICOM 2,0.
ms.assetid: d71436e5-d921-4b84-8028-301d8fc4aedb
title: Énumération CAPICOM_CERTIFICATE_FIND_TYPE (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_CERTIFICATE_FIND_TYPE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: c5c867b230ba2045d97619d7f55e257bd7803b74
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525979"
---
# <a name="capicom_certificate_find_type-enumeration"></a><span data-ttu-id="a7878-104">L' \_ \_ \_ énumération de type de certificat CAPICOM</span><span class="sxs-lookup"><span data-stu-id="a7878-104">CAPICOM\_CERTIFICATE\_FIND\_TYPE enumeration</span></span>

<span data-ttu-id="a7878-105">Le type d’énumération de **\_ \_ \_ type** d’énumération de certificat CAPICOM définit le type de critère de recherche utilisé pour rechercher des certificats spécifiques.</span><span class="sxs-lookup"><span data-stu-id="a7878-105">The **CAPICOM\_CERTIFICATE\_FIND\_TYPE** enumeration type defines the type of search criteria used to find specific certificates.</span></span> <span data-ttu-id="a7878-106">Ce type d’énumération a été introduit dans CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="a7878-106">This enumeration type was introduced in CAPICOM 2.0.</span></span>

## <a name="members"></a><span data-ttu-id="a7878-107">Membres</span><span class="sxs-lookup"><span data-stu-id="a7878-107">Members</span></span>



| <span data-ttu-id="a7878-108">Membre</span><span class="sxs-lookup"><span data-stu-id="a7878-108">Member</span></span>                                                | <span data-ttu-id="a7878-109">Description</span><span class="sxs-lookup"><span data-stu-id="a7878-109">Description</span></span>                                                                                                                                 | <span data-ttu-id="a7878-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="a7878-110">Value</span></span> |
|-------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|-------|
| <span data-ttu-id="a7878-111">**Le certificat CAPICOM \_ \_ trouve un \_ \_ hachage SHA1**</span><span class="sxs-lookup"><span data-stu-id="a7878-111">**CAPICOM\_CERTIFICATE\_FIND\_SHA1\_HASH**</span></span>            | <span data-ttu-id="a7878-112">Retourne les certificats correspondant à un hachage SHA1 spécifié.</span><span class="sxs-lookup"><span data-stu-id="a7878-112">Returns certificates matching a specified SHA1 hash.</span></span><br/>                                                                             | <span data-ttu-id="a7878-113">0</span><span class="sxs-lookup"><span data-stu-id="a7878-113">0</span></span>     |
| <span data-ttu-id="a7878-114">**le certificat CAPICOM \_ trouve le nom de l' \_ \_ objet \_**</span><span class="sxs-lookup"><span data-stu-id="a7878-114">**CAPICOM\_CERTIFICATE\_FIND\_SUBJECT\_NAME**</span></span>         | <span data-ttu-id="a7878-115">Retourne les certificats dont le nom de sujet correspond exactement ou partiellement à un nom d’objet spécifié.</span><span class="sxs-lookup"><span data-stu-id="a7878-115">Returns certificates whose subject name exactly or partially matches a specified subject name.</span></span><br/>                                   | <span data-ttu-id="a7878-116">1</span><span class="sxs-lookup"><span data-stu-id="a7878-116">1</span></span>     |
| <span data-ttu-id="a7878-117">**le certificat CAPICOM \_ trouve le nom de l' \_ \_ émetteur \_**</span><span class="sxs-lookup"><span data-stu-id="a7878-117">**CAPICOM\_CERTIFICATE\_FIND\_ISSUER\_NAME**</span></span>          | <span data-ttu-id="a7878-118">Retourne les certificats dont le nom d’émetteur correspond exactement ou partiellement à un nom d’émetteur spécifié.</span><span class="sxs-lookup"><span data-stu-id="a7878-118">Returns certificates whose issuer name exactly or partially matches a specified issuer name.</span></span><br/>                                     | <span data-ttu-id="a7878-119">2</span><span class="sxs-lookup"><span data-stu-id="a7878-119">2</span></span>     |
| <span data-ttu-id="a7878-120">**\_ \_ \_ nom racine de la recherche du certificat CAPICOM \_**</span><span class="sxs-lookup"><span data-stu-id="a7878-120">**CAPICOM\_CERTIFICATE\_FIND\_ROOT\_NAME**</span></span>            | <span data-ttu-id="a7878-121">Retourne les certificats dont le nom d’objet racine correspond exactement ou partiellement à un nom d’objet racine spécifié.</span><span class="sxs-lookup"><span data-stu-id="a7878-121">Returns certificates whose root subject name exactly or partially matches a specified root subject name.</span></span><br/>                         | <span data-ttu-id="a7878-122">3</span><span class="sxs-lookup"><span data-stu-id="a7878-122">3</span></span>     |
| <span data-ttu-id="a7878-123">**\_nom du modèle de \_ recherche de certificat \_ CAPICOM \_**</span><span class="sxs-lookup"><span data-stu-id="a7878-123">**CAPICOM\_CERTIFICATE\_FIND\_TEMPLATE\_NAME**</span></span>        | <span data-ttu-id="a7878-124">Retourne les certificats dont le nom de modèle correspond à un nom de modèle spécifié.</span><span class="sxs-lookup"><span data-stu-id="a7878-124">Returns certificates whose template name matches a specified template name.</span></span><br/>                                                      | <span data-ttu-id="a7878-125">4</span><span class="sxs-lookup"><span data-stu-id="a7878-125">4</span></span>     |
| <span data-ttu-id="a7878-126">**EXTENSION de recherche de \_ certificat CAPICOM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a7878-126">**CAPICOM\_CERTIFICATE\_FIND\_EXTENSION**</span></span>             | <span data-ttu-id="a7878-127">Retourne les certificats qui ont une extension qui correspond à une extension spécifiée.</span><span class="sxs-lookup"><span data-stu-id="a7878-127">Returns certificates that have an extension that matches a specified extension.</span></span><br/>                                                  | <span data-ttu-id="a7878-128">5</span><span class="sxs-lookup"><span data-stu-id="a7878-128">5</span></span>     |
| <span data-ttu-id="a7878-129">**la \_ \_ \_ \_ propriété étendue de la recherche du certificat CAPICOM**</span><span class="sxs-lookup"><span data-stu-id="a7878-129">**CAPICOM\_CERTIFICATE\_FIND\_EXTENDED\_PROPERTY**</span></span>    | <span data-ttu-id="a7878-130">Retourne les certificats qui ont une propriété étendue dont l’identificateur de propriété correspond à un identificateur de propriété spécifié.</span><span class="sxs-lookup"><span data-stu-id="a7878-130">Returns certificates that have an extended property whose property identifier matches a specified property identifier.</span></span><br/>           | <span data-ttu-id="a7878-131">6</span><span class="sxs-lookup"><span data-stu-id="a7878-131">6</span></span>     |
| <span data-ttu-id="a7878-132">**certificat CAPICOM- \_ \_ stratégie d' \_ application de recherche \_**</span><span class="sxs-lookup"><span data-stu-id="a7878-132">**CAPICOM\_CERTIFICATE\_FIND\_APPLICATION\_POLICY**</span></span>   | <span data-ttu-id="a7878-133">Retourne les certificats dans le magasin qui ont une extension ou une propriété d’utilisation avancée de la clé associée à un identificateur d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="a7878-133">Returns certificates in the store that have either an enhanced key usage extension or property combined with a usage identifier.</span></span><br/> | <span data-ttu-id="a7878-134">7</span><span class="sxs-lookup"><span data-stu-id="a7878-134">7</span></span>     |
| <span data-ttu-id="a7878-135">**certificat CAPICOM- \_ \_ Rechercher la \_ stratégie de certificat \_**</span><span class="sxs-lookup"><span data-stu-id="a7878-135">**CAPICOM\_CERTIFICATE\_FIND\_CERTIFICATE\_POLICY**</span></span>   | <span data-ttu-id="a7878-136">Retourne les certificats contenant un OID de stratégie spécifié.</span><span class="sxs-lookup"><span data-stu-id="a7878-136">Returns certificates containing a specified policy OID.</span></span><br/>                                                                          | <span data-ttu-id="a7878-137">8</span><span class="sxs-lookup"><span data-stu-id="a7878-137">8</span></span>     |
| <span data-ttu-id="a7878-138">**\_temps de recherche du certificat CAPICOM \_ \_ \_ valide**</span><span class="sxs-lookup"><span data-stu-id="a7878-138">**CAPICOM\_CERTIFICATE\_FIND\_TIME\_VALID**</span></span>           | <span data-ttu-id="a7878-139">Retourne les certificats dont l’heure est valide.</span><span class="sxs-lookup"><span data-stu-id="a7878-139">Returns certificates whose time is valid.</span></span><br/>                                                                                        | <span data-ttu-id="a7878-140">9</span><span class="sxs-lookup"><span data-stu-id="a7878-140">9</span></span>     |
| <span data-ttu-id="a7878-141">**l’heure de la \_ recherche du certificat CAPICOM n’est \_ \_ \_ pas \_ encore \_ valide**</span><span class="sxs-lookup"><span data-stu-id="a7878-141">**CAPICOM\_CERTIFICATE\_FIND\_TIME\_NOT\_YET\_VALID**</span></span> | <span data-ttu-id="a7878-142">Retourne des certificats dont l’heure n’est pas encore valide.</span><span class="sxs-lookup"><span data-stu-id="a7878-142">Returns certificates whose time is not yet valid.</span></span><br/>                                                                                | <span data-ttu-id="a7878-143">10</span><span class="sxs-lookup"><span data-stu-id="a7878-143">10</span></span>    |
| <span data-ttu-id="a7878-144">**\_temps de recherche du certificat CAPICOM \_ \_ \_ expiré**</span><span class="sxs-lookup"><span data-stu-id="a7878-144">**CAPICOM\_CERTIFICATE\_FIND\_TIME\_EXPIRED**</span></span>         | <span data-ttu-id="a7878-145">Retourne les certificats dont le temps a expiré.</span><span class="sxs-lookup"><span data-stu-id="a7878-145">Returns certificates whose time has expired.</span></span><br/>                                                                                     | <span data-ttu-id="a7878-146">11</span><span class="sxs-lookup"><span data-stu-id="a7878-146">11</span></span>    |
| <span data-ttu-id="a7878-147">**utilisation de la \_ \_ clé de recherche de certificat CAPICOM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a7878-147">**CAPICOM\_CERTIFICATE\_FIND\_KEY\_USAGE**</span></span>            | <span data-ttu-id="a7878-148">Retourne les certificats contenant une clé qui peut être utilisée de la manière spécifiée.</span><span class="sxs-lookup"><span data-stu-id="a7878-148">Returns certificates containing a key that can be used in the specified manner.</span></span><br/>                                                  | <span data-ttu-id="a7878-149">12</span><span class="sxs-lookup"><span data-stu-id="a7878-149">12</span></span>    |



## <a name="remarks"></a><span data-ttu-id="a7878-150">Notes</span><span class="sxs-lookup"><span data-stu-id="a7878-150">Remarks</span></span>

<span data-ttu-id="a7878-151">Le type d’énumération de **\_ \_ \_ type du certificat CAPICOM** est utilisé par la méthode [**Certificates. Find**](certificates-find.md) .</span><span class="sxs-lookup"><span data-stu-id="a7878-151">The **CAPICOM\_CERTIFICATE\_FIND\_TYPE** enumeration type is used by the [**Certificates.Find**](certificates-find.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7878-152">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a7878-152">Requirements</span></span>



| <span data-ttu-id="a7878-153">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a7878-153">Requirement</span></span> | <span data-ttu-id="a7878-154">Valeur</span><span class="sxs-lookup"><span data-stu-id="a7878-154">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a7878-155">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="a7878-155">Redistributable</span></span><br/> | <span data-ttu-id="a7878-156">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="a7878-156">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="a7878-157">En-tête</span><span class="sxs-lookup"><span data-stu-id="a7878-157">Header</span></span><br/>          | <dl> <span data-ttu-id="a7878-158"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="a7878-158"><dt>Capicom.h</dt></span></span> </dl> |



 

 




