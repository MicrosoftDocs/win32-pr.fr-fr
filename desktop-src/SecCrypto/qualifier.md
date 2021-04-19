---
description: Représente un pointeur CPS (certification Practice Statement) ou un qualificateur d’avis utilisateur.
ms.assetid: 857af3d6-aa7b-429a-a056-72573232f72c
title: Qualificateur (objet)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifier
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 3b1740e064cac53f93d9c81603477a1230c7fd7a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525495"
---
# <a name="qualifier-object"></a><span data-ttu-id="c7bd9-103">Qualificateur (objet)</span><span class="sxs-lookup"><span data-stu-id="c7bd9-103">Qualifier object</span></span>

<span data-ttu-id="c7bd9-104">\[L’objet **qualificateur** peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="c7bd9-104">\[The **Qualifier** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="c7bd9-105">Utilisez plutôt la [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) en appelant le constructeur qui prend un OID comme paramètre, puis utilisez l’OID pour les stratégies de certificat pour traiter les qualificateurs qui font partie des informations de stratégie dans l’extension des stratégies de certificat.\]</span><span class="sxs-lookup"><span data-stu-id="c7bd9-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to process qualifiers that are part of the policy information in the Certificate Policies extension.\]</span></span>

<span data-ttu-id="c7bd9-106">L’objet **qualificateur** représente un pointeur CPS (certification Practice Statement) ou un qualificateur d’avis utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c7bd9-106">The **Qualifier** object represents a Certification Practice Statement (CPS) pointer or user notice qualifier.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="c7bd9-107">Quand l’utiliser</span><span class="sxs-lookup"><span data-stu-id="c7bd9-107">When to use</span></span>

<span data-ttu-id="c7bd9-108">L’objet **qualificateur** est utilisé pour effectuer les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="c7bd9-108">The **Qualifier** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="c7bd9-109">Récupérez l’identificateur d’objet du qualificateur.</span><span class="sxs-lookup"><span data-stu-id="c7bd9-109">Retrieve the object identifier of the qualifier.</span></span>
-   <span data-ttu-id="c7bd9-110">Récupérez le Uniform Resource Identifier (URI) qui pointe vers un CPS publié par l' [*autorité de certification*](../secgloss/c-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="c7bd9-110">Retrieve the Uniform Resource Identifier (URI) that points to a CPS published by the [*certification authority*](../secgloss/c-gly.md) (CA).</span></span>
-   <span data-ttu-id="c7bd9-111">Récupérez le nom de l’organisation associée au qualificateur.</span><span class="sxs-lookup"><span data-stu-id="c7bd9-111">Retrieve the name of the organization associated with the qualifier.</span></span>
-   <span data-ttu-id="c7bd9-112">Récupérez le nom et le contenu d’une notification utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c7bd9-112">Retrieve the name and content of a user notice.</span></span>

## <a name="members"></a><span data-ttu-id="c7bd9-113">Membres</span><span class="sxs-lookup"><span data-stu-id="c7bd9-113">Members</span></span>

<span data-ttu-id="c7bd9-114">L’objet **qualificateur** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="c7bd9-114">The **Qualifier** object has these types of members:</span></span>

-   [<span data-ttu-id="c7bd9-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c7bd9-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c7bd9-116">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c7bd9-116">Properties</span></span>

<span data-ttu-id="c7bd9-117">L’objet **qualificateur** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="c7bd9-117">The **Qualifier** object has these properties.</span></span>



| <span data-ttu-id="c7bd9-118">Propriété</span><span class="sxs-lookup"><span data-stu-id="c7bd9-118">Property</span></span>                                                          | <span data-ttu-id="c7bd9-119">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="c7bd9-119">Access type</span></span>          | <span data-ttu-id="c7bd9-120">Description</span><span class="sxs-lookup"><span data-stu-id="c7bd9-120">Description</span></span>                                                                                                                         |
|:------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c7bd9-121">**CPSPointer**</span><span class="sxs-lookup"><span data-stu-id="c7bd9-121">**CPSPointer**</span></span>](qualifier-cpspointer.md)<br/>             | <span data-ttu-id="c7bd9-122">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c7bd9-122">Read-only</span></span><br/> | <span data-ttu-id="c7bd9-123">Récupère une chaîne qui contient l’URI qui pointe vers un CPS publié par l’autorité de certification.</span><span class="sxs-lookup"><span data-stu-id="c7bd9-123">Retrieves a string that contains the URI that points to a CPS published by the CA.</span></span><br/>                                       |
| [<span data-ttu-id="c7bd9-124">**ExplicitText**</span><span class="sxs-lookup"><span data-stu-id="c7bd9-124">**ExplicitText**</span></span>](qualifier-explicittext.md)<br/>         | <span data-ttu-id="c7bd9-125">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c7bd9-125">Read-only</span></span><br/> | <span data-ttu-id="c7bd9-126">Récupère une chaîne qui contient le contenu de l’avis de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c7bd9-126">Retrieves a string that contains the content of the user notice.</span></span> <span data-ttu-id="c7bd9-127">Cette propriété peut être vide.</span><span class="sxs-lookup"><span data-stu-id="c7bd9-127">This property may be empty.</span></span><br/>                             |
| [<span data-ttu-id="c7bd9-128">**NoticeNumbers**</span><span class="sxs-lookup"><span data-stu-id="c7bd9-128">**NoticeNumbers**</span></span>](qualifier-noticenumbers.md)<br/>       | <span data-ttu-id="c7bd9-129">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c7bd9-129">Read-only</span></span><br/> | <span data-ttu-id="c7bd9-130">Récupère un objet **NoticeNumbers** qui contient la collection de numéros d’avis d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c7bd9-130">Retrieves a **NoticeNumbers** object that contains the collection of user notice numbers.</span></span> <span data-ttu-id="c7bd9-131">Cette propriété peut être vide.</span><span class="sxs-lookup"><span data-stu-id="c7bd9-131">This property may be empty.</span></span><br/>    |
| [<span data-ttu-id="c7bd9-132">**OID**</span><span class="sxs-lookup"><span data-stu-id="c7bd9-132">**OID**</span></span>](qualifier-oid.md)<br/>                           | <span data-ttu-id="c7bd9-133">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c7bd9-133">Read-only</span></span><br/> | <span data-ttu-id="c7bd9-134">Récupère un objet [**OID**](oid.md) qui identifie le qualificateur.</span><span class="sxs-lookup"><span data-stu-id="c7bd9-134">Retrieves an [**OID**](oid.md) object that identifies the qualifier.</span></span> <span data-ttu-id="c7bd9-135">Il s’agit de la propriété par défaut.</span><span class="sxs-lookup"><span data-stu-id="c7bd9-135">This is the default property.</span></span><br/>                      |
| [<span data-ttu-id="c7bd9-136">**Morgan**</span><span class="sxs-lookup"><span data-stu-id="c7bd9-136">**OrganizationName**</span></span>](qualifier-organizationname.md)<br/> | <span data-ttu-id="c7bd9-137">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c7bd9-137">Read-only</span></span><br/> | <span data-ttu-id="c7bd9-138">Récupère une chaîne qui contient le nom de l’organisation associée au qualificateur.</span><span class="sxs-lookup"><span data-stu-id="c7bd9-138">Retrieves a string that contains the name of the organization associated with the qualifier.</span></span> <span data-ttu-id="c7bd9-139">Cette propriété peut être vide.</span><span class="sxs-lookup"><span data-stu-id="c7bd9-139">This property may be empty.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c7bd9-140">Notes</span><span class="sxs-lookup"><span data-stu-id="c7bd9-140">Remarks</span></span>

<span data-ttu-id="c7bd9-141">Impossible de créer l’objet **qualificateur** .</span><span class="sxs-lookup"><span data-stu-id="c7bd9-141">The **Qualifier** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7bd9-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c7bd9-142">Requirements</span></span>



| <span data-ttu-id="c7bd9-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c7bd9-143">Requirement</span></span> | <span data-ttu-id="c7bd9-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="c7bd9-144">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c7bd9-145">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="c7bd9-145">Redistributable</span></span><br/> | <span data-ttu-id="c7bd9-146">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="c7bd9-146">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="c7bd9-147">DLL</span><span class="sxs-lookup"><span data-stu-id="c7bd9-147">DLL</span></span><br/>             | <dl> <span data-ttu-id="c7bd9-148"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c7bd9-148"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
