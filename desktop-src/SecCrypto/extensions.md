---
description: Représente une collection d’objets d’extension.
ms.assetid: f2a6854d-1831-489f-adf6-31a0b26511e3
title: Objet extensions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3af518d6f1918c82d5819b04a086195c06b79740
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533098"
---
# <a name="extensions-object"></a><span data-ttu-id="c7fa3-103">Objet extensions</span><span class="sxs-lookup"><span data-stu-id="c7fa3-103">Extensions object</span></span>

<span data-ttu-id="c7fa3-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c7fa3-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="c7fa3-105">Utilisez plutôt la [**classe X509ExtensionCollection**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="c7fa3-105">Instead, use the [**X509ExtensionCollection Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="c7fa3-106">L’objet **Extensions** représente une collection d’objets d' [**extension**](extension.md) .</span><span class="sxs-lookup"><span data-stu-id="c7fa3-106">The **Extensions** object represents a collection of [**Extension**](extension.md) objects.</span></span> <span data-ttu-id="c7fa3-107">Chaque objet d' [**extension**](extension.md) représente une extension de certificat unique.</span><span class="sxs-lookup"><span data-stu-id="c7fa3-107">Each [**Extension**](extension.md) object represents a single certificate extension.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="c7fa3-108">Quand l’utiliser</span><span class="sxs-lookup"><span data-stu-id="c7fa3-108">When to use</span></span>

<span data-ttu-id="c7fa3-109">L’objet **Extensions** est utilisé pour effectuer les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="c7fa3-109">The **Extensions** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="c7fa3-110">Récupérez le nombre d’extensions de certificat dans la collection.</span><span class="sxs-lookup"><span data-stu-id="c7fa3-110">Retrieve the number of certificate extensions in the collection.</span></span>
-   <span data-ttu-id="c7fa3-111">Récupérez un objet d' [**extension**](extension.md) spécifique de la collection.</span><span class="sxs-lookup"><span data-stu-id="c7fa3-111">Retrieve a specific [**Extension**](extension.md) object from the collection.</span></span>
-   <span data-ttu-id="c7fa3-112">Itérez au sein de la collection.</span><span class="sxs-lookup"><span data-stu-id="c7fa3-112">Iterate through the collection.</span></span>

## <a name="members"></a><span data-ttu-id="c7fa3-113">Membres</span><span class="sxs-lookup"><span data-stu-id="c7fa3-113">Members</span></span>

<span data-ttu-id="c7fa3-114">L’objet **Extensions** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="c7fa3-114">The **Extensions** object has these types of members:</span></span>

-   [<span data-ttu-id="c7fa3-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c7fa3-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c7fa3-116">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c7fa3-116">Properties</span></span>

<span data-ttu-id="c7fa3-117">L’objet **Extensions** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="c7fa3-117">The **Extensions** object has these properties.</span></span>



| <span data-ttu-id="c7fa3-118">Propriété</span><span class="sxs-lookup"><span data-stu-id="c7fa3-118">Property</span></span>                                           | <span data-ttu-id="c7fa3-119">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="c7fa3-119">Access type</span></span>          | <span data-ttu-id="c7fa3-120">Description</span><span class="sxs-lookup"><span data-stu-id="c7fa3-120">Description</span></span>                                                                                                                                                                                                                     |
|:---------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c7fa3-121">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="c7fa3-121">**\_NewEnum**</span></span>](extensions-newenum.md)<br/> | <span data-ttu-id="c7fa3-122">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c7fa3-122">Read-only</span></span><br/> | <span data-ttu-id="c7fa3-123">Récupère une interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) sur un objet qui peut être utilisé pour énumérer la collection.</span><span class="sxs-lookup"><span data-stu-id="c7fa3-123">Retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="c7fa3-124">Cette propriété est masquée dans Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="c7fa3-124">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span><br/> |
| [<span data-ttu-id="c7fa3-125">**Saut**</span><span class="sxs-lookup"><span data-stu-id="c7fa3-125">**Count**</span></span>](extensions-count.md)<br/>       | <span data-ttu-id="c7fa3-126">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c7fa3-126">Read-only</span></span><br/> | <span data-ttu-id="c7fa3-127">Récupère le nombre d’objets d' [**extension**](extension.md) dans la collection.</span><span class="sxs-lookup"><span data-stu-id="c7fa3-127">Retrieves the number of [**Extension**](extension.md) objects in the collection.</span></span><br/>                                                                                                                                    |
| [<span data-ttu-id="c7fa3-128">**Élément**</span><span class="sxs-lookup"><span data-stu-id="c7fa3-128">**Item**</span></span>](extensions-item.md)<br/>         | <span data-ttu-id="c7fa3-129">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c7fa3-129">Read-only</span></span><br/> | <span data-ttu-id="c7fa3-130">Récupère l’objet d' [**extension**](extension.md) qui représente l’extension de certificat indexée de la collection.</span><span class="sxs-lookup"><span data-stu-id="c7fa3-130">Retrieves the [**Extension**](extension.md) object that represents the indexed certificate extension of the collection.</span></span> <span data-ttu-id="c7fa3-131">Il s’agit de la propriété par défaut.</span><span class="sxs-lookup"><span data-stu-id="c7fa3-131">This is the default property.</span></span><br/>                                                               |



 

## <a name="remarks"></a><span data-ttu-id="c7fa3-132">Notes</span><span class="sxs-lookup"><span data-stu-id="c7fa3-132">Remarks</span></span>

<span data-ttu-id="c7fa3-133">L’objet **Extensions** est retourné par la méthode [**Certificate. extensions**](certificate-extensions.md) .</span><span class="sxs-lookup"><span data-stu-id="c7fa3-133">The **Extensions** object is returned by the [**Certificate.Extensions**](certificate-extensions.md) method.</span></span>

<span data-ttu-id="c7fa3-134">Impossible de créer l’objet **Extensions** .</span><span class="sxs-lookup"><span data-stu-id="c7fa3-134">The **Extensions** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7fa3-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c7fa3-135">Requirements</span></span>



| <span data-ttu-id="c7fa3-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c7fa3-136">Requirement</span></span> | <span data-ttu-id="c7fa3-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="c7fa3-137">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c7fa3-138">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="c7fa3-138">End of client support</span></span><br/> | <span data-ttu-id="c7fa3-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c7fa3-139">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="c7fa3-140">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="c7fa3-140">End of server support</span></span><br/> | <span data-ttu-id="c7fa3-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c7fa3-141">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="c7fa3-142">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="c7fa3-142">Redistributable</span></span><br/>       | <span data-ttu-id="c7fa3-143">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="c7fa3-143">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="c7fa3-144">DLL</span><span class="sxs-lookup"><span data-stu-id="c7fa3-144">DLL</span></span><br/>                   | <dl> <span data-ttu-id="c7fa3-145"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c7fa3-145"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
