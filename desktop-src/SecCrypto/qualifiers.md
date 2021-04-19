---
description: Représente une collection de qualificateurs.
ms.assetid: 2f51404d-b26e-4153-b206-ab6b413363a1
title: Qualificateurs, objet (IADs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifiers
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e873019d6fbfb21de8be430d7960f697b39eeca7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525210"
---
# <a name="qualifiers-object"></a><span data-ttu-id="20735-103">Qualificateurs, objet</span><span class="sxs-lookup"><span data-stu-id="20735-103">Qualifiers object</span></span>

<span data-ttu-id="20735-104">\[L’objet **qualificateurs** peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="20735-104">\[The **Qualifiers** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="20735-105">Utilisez plutôt la [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) en appelant le constructeur qui prend un OID comme paramètre, puis utilisez l’OID pour les stratégies de certificat pour traiter les qualificateurs qui font partie des informations de stratégie dans l’extension des stratégies de certificat.\]</span><span class="sxs-lookup"><span data-stu-id="20735-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to process qualifiers that are part of the policy information in the Certificate Policies extension.\]</span></span>

<span data-ttu-id="20735-106">L’objet **qualificateurs** représente une collection de qualificateurs.</span><span class="sxs-lookup"><span data-stu-id="20735-106">The **Qualifiers** object represents a collection of qualifiers.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="20735-107">Quand l’utiliser</span><span class="sxs-lookup"><span data-stu-id="20735-107">When to use</span></span>

<span data-ttu-id="20735-108">L’objet **qualificateurs** est utilisé pour effectuer les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="20735-108">The **Qualifiers** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="20735-109">Récupère une propriété étendue spécifique de la collection.</span><span class="sxs-lookup"><span data-stu-id="20735-109">Retrieve a specific extended property from the collection.</span></span>
-   <span data-ttu-id="20735-110">Récupérez le nombre de propriétés étendues dans la collection.</span><span class="sxs-lookup"><span data-stu-id="20735-110">Retrieve the number of extended properties in the collection.</span></span>
-   <span data-ttu-id="20735-111">Itérez au sein de la collection.</span><span class="sxs-lookup"><span data-stu-id="20735-111">Iterate through the collection.</span></span>

## <a name="members"></a><span data-ttu-id="20735-112">Membres</span><span class="sxs-lookup"><span data-stu-id="20735-112">Members</span></span>

<span data-ttu-id="20735-113">L’objet **qualificateurs** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="20735-113">The **Qualifiers** object has these types of members:</span></span>

-   [<span data-ttu-id="20735-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="20735-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="20735-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="20735-115">Properties</span></span>

<span data-ttu-id="20735-116">L’objet **qualificateurs** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="20735-116">The **Qualifiers** object has these properties.</span></span>



| <span data-ttu-id="20735-117">Propriété</span><span class="sxs-lookup"><span data-stu-id="20735-117">Property</span></span>                                           | <span data-ttu-id="20735-118">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="20735-118">Access type</span></span>          | <span data-ttu-id="20735-119">Description</span><span class="sxs-lookup"><span data-stu-id="20735-119">Description</span></span>                                                                                                                                                                                                                     |
|:---------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="20735-120">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="20735-120">**\_NewEnum**</span></span>](qualifiers-newenum.md)<br/> | <span data-ttu-id="20735-121">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="20735-121">Read-only</span></span><br/> | <span data-ttu-id="20735-122">Récupère une interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) sur un objet qui peut être utilisé pour énumérer la collection.</span><span class="sxs-lookup"><span data-stu-id="20735-122">Retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="20735-123">Cette propriété est masquée dans Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="20735-123">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span><br/> |
| [<span data-ttu-id="20735-124">**Saut**</span><span class="sxs-lookup"><span data-stu-id="20735-124">**Count**</span></span>](qualifiers-count.md)<br/>       | <span data-ttu-id="20735-125">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="20735-125">Read-only</span></span><br/> | <span data-ttu-id="20735-126">Récupère le nombre de qualificateurs dans la collection.</span><span class="sxs-lookup"><span data-stu-id="20735-126">Retrieves the number of qualifiers in the collection.</span></span><br/>                                                                                                                                                                |
| [<span data-ttu-id="20735-127">**Élément**</span><span class="sxs-lookup"><span data-stu-id="20735-127">**Item**</span></span>](qualifiers-item.md)<br/>         | <span data-ttu-id="20735-128">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="20735-128">Read-only</span></span><br/> | <span data-ttu-id="20735-129">Récupère un objet [**qualificateur**](qualifier.md) qui représente le qualificateur indexé de la collection.</span><span class="sxs-lookup"><span data-stu-id="20735-129">Retrieves a [**Qualifier**](qualifier.md) object that represents the indexed qualifier of the collection.</span></span> <span data-ttu-id="20735-130">Il s’agit de la propriété par défaut.</span><span class="sxs-lookup"><span data-stu-id="20735-130">This is the default property.</span></span><br/>                                                                             |



 

## <a name="remarks"></a><span data-ttu-id="20735-131">Notes</span><span class="sxs-lookup"><span data-stu-id="20735-131">Remarks</span></span>

<span data-ttu-id="20735-132">Impossible de créer l’objet **qualificateurs** .</span><span class="sxs-lookup"><span data-stu-id="20735-132">The **Qualifiers** object cannot be created.</span></span>

<span data-ttu-id="20735-133">La propriété d’objet [**PolicyInformation. Qualifiers**](policyinformation-qualifiers.md) CAPICOM retourne un objet **qualificateurs** .</span><span class="sxs-lookup"><span data-stu-id="20735-133">The [**PolicyInformation.Qualifiers**](policyinformation-qualifiers.md) CAPICOM object property returns a **Qualifiers** object.</span></span>

## <a name="requirements"></a><span data-ttu-id="20735-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="20735-134">Requirements</span></span>



| <span data-ttu-id="20735-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="20735-135">Requirement</span></span> | <span data-ttu-id="20735-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="20735-136">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="20735-137">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="20735-137">Redistributable</span></span><br/> | <span data-ttu-id="20735-138">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="20735-138">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="20735-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="20735-139">Header</span></span><br/>          | <dl> <span data-ttu-id="20735-140"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="20735-140"><dt>Iads.h</dt></span></span> </dl>      |
| <span data-ttu-id="20735-141">DLL</span><span class="sxs-lookup"><span data-stu-id="20735-141">DLL</span></span><br/>             | <dl> <span data-ttu-id="20735-142"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="20735-142"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
