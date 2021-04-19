---
description: Représente une collection d’objets EKU.
ms.assetid: 04b9f0bf-e1d4-4a2c-be5d-bae7c1090bdb
title: Objet EKU
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EKUs
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 56fd6eaeb5a00549cbb4ee659b99ece391e0ebed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535330"
---
# <a name="ekus-object"></a><span data-ttu-id="ba112-103">Objet EKU</span><span class="sxs-lookup"><span data-stu-id="ba112-103">EKUs object</span></span>

<span data-ttu-id="ba112-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ba112-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="ba112-105">Utilisez plutôt la [**classe X509ExtensionCollection**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="ba112-105">Instead, use the [**X509ExtensionCollection Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="ba112-106">L’objet **EKU** représente une collection d’objets [**EKU**](eku.md) .</span><span class="sxs-lookup"><span data-stu-id="ba112-106">The **EKUs** object represents a collection of [**EKU**](eku.md) objects.</span></span> <span data-ttu-id="ba112-107">Chaque objet [**EKU**](eku.md) représente une propriété d’utilisation améliorée de la clé (EKU) d’un certificat.</span><span class="sxs-lookup"><span data-stu-id="ba112-107">Each [**EKU**](eku.md) object represents a single extended key usage (EKU) property of a certificate.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="ba112-108">Quand l’utiliser</span><span class="sxs-lookup"><span data-stu-id="ba112-108">When to use</span></span>

<span data-ttu-id="ba112-109">La collection de **EKU** est utilisée pour effectuer les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="ba112-109">The **EKUs** collection is used to perform the following tasks:</span></span>

-   <span data-ttu-id="ba112-110">Récupérez le nombre de propriétés EKU dans la collection.</span><span class="sxs-lookup"><span data-stu-id="ba112-110">Retrieve the number of EKU properties in the collection.</span></span>
-   <span data-ttu-id="ba112-111">Récupérez un objet [**EKU**](eku.md) spécifique de la collection.</span><span class="sxs-lookup"><span data-stu-id="ba112-111">Retrieve a specific [**EKU**](eku.md) object from the collection.</span></span>
-   <span data-ttu-id="ba112-112">Itérez au sein de la collection.</span><span class="sxs-lookup"><span data-stu-id="ba112-112">Iterate through the collection.</span></span>

## <a name="members"></a><span data-ttu-id="ba112-113">Membres</span><span class="sxs-lookup"><span data-stu-id="ba112-113">Members</span></span>

<span data-ttu-id="ba112-114">L’objet **EKU** contient les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="ba112-114">The **EKUs** object has these types of members:</span></span>

-   [<span data-ttu-id="ba112-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ba112-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ba112-116">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ba112-116">Properties</span></span>

<span data-ttu-id="ba112-117">L’objet **EKU** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="ba112-117">The **EKUs** object has these properties.</span></span>



| <span data-ttu-id="ba112-118">Propriété</span><span class="sxs-lookup"><span data-stu-id="ba112-118">Property</span></span>                                     | <span data-ttu-id="ba112-119">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="ba112-119">Access type</span></span>          | <span data-ttu-id="ba112-120">Description</span><span class="sxs-lookup"><span data-stu-id="ba112-120">Description</span></span>                                                                                                                                                                                                                     |
|:---------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ba112-121">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="ba112-121">**\_NewEnum**</span></span>](ekus-newenum.md)<br/> | <span data-ttu-id="ba112-122">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ba112-122">Read-only</span></span><br/> | <span data-ttu-id="ba112-123">Récupère une interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) sur un objet qui peut être utilisé pour énumérer la collection.</span><span class="sxs-lookup"><span data-stu-id="ba112-123">Retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="ba112-124">Cette propriété est masquée dans Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="ba112-124">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span><br/> |
| [<span data-ttu-id="ba112-125">**Saut**</span><span class="sxs-lookup"><span data-stu-id="ba112-125">**Count**</span></span>](ekus-count.md)<br/>       | <span data-ttu-id="ba112-126">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ba112-126">Read-only</span></span><br/> | <span data-ttu-id="ba112-127">Récupère le nombre d’objets [**EKU**](eku.md) dans la collection.</span><span class="sxs-lookup"><span data-stu-id="ba112-127">Retrieves the number of [**EKU**](eku.md) objects in the collection.</span></span><br/>                                                                                                                                                |
| [<span data-ttu-id="ba112-128">**Élément**</span><span class="sxs-lookup"><span data-stu-id="ba112-128">**Item**</span></span>](ekus-item.md)<br/>         | <span data-ttu-id="ba112-129">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ba112-129">Read-only</span></span><br/> | <span data-ttu-id="ba112-130">Récupère l’objet [**EKU**](eku.md) qui représente la propriété EKU indexée.</span><span class="sxs-lookup"><span data-stu-id="ba112-130">Retrieves the [**EKU**](eku.md) object that represents the indexed EKU property.</span></span> <span data-ttu-id="ba112-131">Il s’agit de la propriété par défaut.</span><span class="sxs-lookup"><span data-stu-id="ba112-131">This is the default property.</span></span><br/>                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="ba112-132">Notes</span><span class="sxs-lookup"><span data-stu-id="ba112-132">Remarks</span></span>

<span data-ttu-id="ba112-133">Cette collection est récupérée par la propriété [**ExtendedKeyUsage. EKU**](extendedkeyusage-ekus.md) .</span><span class="sxs-lookup"><span data-stu-id="ba112-133">This collection is retrieved by the [**ExtendedKeyUsage.EKUs**](extendedkeyusage-ekus.md) property.</span></span>

<span data-ttu-id="ba112-134">Impossible de créer l’objet **EKU** .</span><span class="sxs-lookup"><span data-stu-id="ba112-134">The **EKUs** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba112-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ba112-135">Requirements</span></span>



| <span data-ttu-id="ba112-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ba112-136">Requirement</span></span> | <span data-ttu-id="ba112-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="ba112-137">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ba112-138">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="ba112-138">End of client support</span></span><br/> | <span data-ttu-id="ba112-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ba112-139">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="ba112-140">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="ba112-140">End of server support</span></span><br/> | <span data-ttu-id="ba112-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ba112-141">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="ba112-142">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="ba112-142">Redistributable</span></span><br/>       | <span data-ttu-id="ba112-143">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="ba112-143">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="ba112-144">DLL</span><span class="sxs-lookup"><span data-stu-id="ba112-144">DLL</span></span><br/>                   | <dl> <span data-ttu-id="ba112-145"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ba112-145"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
