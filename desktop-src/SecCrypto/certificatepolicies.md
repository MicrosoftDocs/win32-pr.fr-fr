---
description: Collection d’objets PolicyInformation.
ms.assetid: 2abdd070-82ae-47fd-afbc-6d4361e5a3f1
title: Objet CertificatePolicies
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificatePolicies
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 8ec217276b5d038f85f33887b771b0afa0c6e40a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542579"
---
# <a name="certificatepolicies-object"></a><span data-ttu-id="2a183-103">Objet CertificatePolicies</span><span class="sxs-lookup"><span data-stu-id="2a183-103">CertificatePolicies object</span></span>

<span data-ttu-id="2a183-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="2a183-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="2a183-105">Utilisez plutôt la [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) en appelant le constructeur qui prend un OID comme paramètre, puis utilisez l’OID pour les stratégies de certificat pour récupérer les stratégies de certificat.\]</span><span class="sxs-lookup"><span data-stu-id="2a183-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to retrieve the certificate policies.\]</span></span>

<span data-ttu-id="2a183-106">L’objet **certificatePolicies** représente une collection d’objets [**PolicyInformation**](policyinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="2a183-106">The **CertificatePolicies** object represents a collection of [**PolicyInformation**](policyinformation.md) objects.</span></span> <span data-ttu-id="2a183-107">Chaque objet [**PolicyInformation**](policyinformation.md) représente une stratégie de certificat unique.</span><span class="sxs-lookup"><span data-stu-id="2a183-107">Each [**PolicyInformation**](policyinformation.md) object represents a single certificate policy.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="2a183-108">Quand l’utiliser</span><span class="sxs-lookup"><span data-stu-id="2a183-108">When to use</span></span>

<span data-ttu-id="2a183-109">L’objet **certificatePolicies** est utilisé pour effectuer les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="2a183-109">The **CertificatePolicies** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="2a183-110">Récupérez le nombre de stratégies de certificat dans la collection.</span><span class="sxs-lookup"><span data-stu-id="2a183-110">Retrieve the number of certificate policies in the collection.</span></span>
-   <span data-ttu-id="2a183-111">Récupérez un objet [**PolicyInformation**](policyinformation.md) spécifique de la collection.</span><span class="sxs-lookup"><span data-stu-id="2a183-111">Retrieve a specific [**PolicyInformation**](policyinformation.md) object from the collection.</span></span>
-   <span data-ttu-id="2a183-112">Itérez au sein de la collection.</span><span class="sxs-lookup"><span data-stu-id="2a183-112">Iterate through the collection.</span></span>

## <a name="members"></a><span data-ttu-id="2a183-113">Membres</span><span class="sxs-lookup"><span data-stu-id="2a183-113">Members</span></span>

<span data-ttu-id="2a183-114">L’objet **certificatePolicies** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="2a183-114">The **CertificatePolicies** object has these types of members:</span></span>

-   [<span data-ttu-id="2a183-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2a183-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2a183-116">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2a183-116">Properties</span></span>

<span data-ttu-id="2a183-117">L’objet **certificatePolicies** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="2a183-117">The **CertificatePolicies** object has these properties.</span></span>



| <span data-ttu-id="2a183-118">Propriété</span><span class="sxs-lookup"><span data-stu-id="2a183-118">Property</span></span>                                                    | <span data-ttu-id="2a183-119">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="2a183-119">Access type</span></span>          | <span data-ttu-id="2a183-120">Description</span><span class="sxs-lookup"><span data-stu-id="2a183-120">Description</span></span>                                                                                                                                                                                                                     |
|:------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2a183-121">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="2a183-121">**\_NewEnum**</span></span>](certificatepolicies-newenum.md)<br/> | <span data-ttu-id="2a183-122">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2a183-122">Read-only</span></span><br/> | <span data-ttu-id="2a183-123">Récupère une interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) sur un objet qui peut être utilisé pour énumérer la collection.</span><span class="sxs-lookup"><span data-stu-id="2a183-123">Retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="2a183-124">Cette propriété est masquée dans Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="2a183-124">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span><br/> |
| [<span data-ttu-id="2a183-125">**Saut**</span><span class="sxs-lookup"><span data-stu-id="2a183-125">**Count**</span></span>](certificatepolicies-count.md)<br/>       | <span data-ttu-id="2a183-126">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2a183-126">Read-only</span></span><br/> | <span data-ttu-id="2a183-127">Récupère le nombre d’objets [**PolicyInformation**](policyinformation.md) dans la collection.</span><span class="sxs-lookup"><span data-stu-id="2a183-127">Retrieves the number of [**PolicyInformation**](policyinformation.md) objects in the collection.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="2a183-128">**Élément**</span><span class="sxs-lookup"><span data-stu-id="2a183-128">**Item**</span></span>](certificatepolicies-item.md)<br/>         | <span data-ttu-id="2a183-129">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2a183-129">Read-only</span></span><br/> | <span data-ttu-id="2a183-130">Récupère un objet [**PolicyInformation**](policyinformation.md) qui représente la stratégie de certificat indexée de la collection.</span><span class="sxs-lookup"><span data-stu-id="2a183-130">Retrieves a [**PolicyInformation**](policyinformation.md) object that represents the indexed certificate policy of the collection.</span></span> <span data-ttu-id="2a183-131">Il s’agit de la propriété par défaut.</span><span class="sxs-lookup"><span data-stu-id="2a183-131">This is the default property.</span></span><br/>                                                    |



 

## <a name="remarks"></a><span data-ttu-id="2a183-132">Notes</span><span class="sxs-lookup"><span data-stu-id="2a183-132">Remarks</span></span>

<span data-ttu-id="2a183-133">Impossible de créer l’objet **certificatePolicies** .</span><span class="sxs-lookup"><span data-stu-id="2a183-133">The **CertificatePolicies** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a183-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2a183-134">Requirements</span></span>



| <span data-ttu-id="2a183-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2a183-135">Requirement</span></span> | <span data-ttu-id="2a183-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="2a183-136">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2a183-137">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="2a183-137">End of client support</span></span><br/> | <span data-ttu-id="2a183-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2a183-138">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="2a183-139">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="2a183-139">End of server support</span></span><br/> | <span data-ttu-id="2a183-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2a183-140">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="2a183-141">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="2a183-141">Redistributable</span></span><br/>       | <span data-ttu-id="2a183-142">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="2a183-142">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="2a183-143">DLL</span><span class="sxs-lookup"><span data-stu-id="2a183-143">DLL</span></span><br/>                   | <dl> <span data-ttu-id="2a183-144"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2a183-144"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
