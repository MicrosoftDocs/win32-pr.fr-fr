---
description: Représente une collection d’objets signataires.
ms.assetid: 72e86acd-eb87-4eff-bd4e-327630ebbfc4
title: Objet des signataires
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signers
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 75eba0ecb2592bf7efc27ecdd63288179e306651
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532533"
---
# <a name="signers-object"></a><span data-ttu-id="1ebca-103">Objet des signataires</span><span class="sxs-lookup"><span data-stu-id="1ebca-103">Signers object</span></span>

<span data-ttu-id="1ebca-104">\[L’objet **signataires** peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="1ebca-104">\[The **Signers** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="1ebca-105">Utilisez plutôt une collection d’objets CmsSigner.</span><span class="sxs-lookup"><span data-stu-id="1ebca-105">Instead, use a collection of CmsSigner objects.</span></span> <span data-ttu-id="1ebca-106">Pour plus d’informations, consultez la [**classe CmsSigner**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) dans l’espace de noms [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="1ebca-106">For more information, see the [**CmsSigner Class**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="1ebca-107">L’objet **signataires** représente une collection d’objets [**signataires**](signer.md) .</span><span class="sxs-lookup"><span data-stu-id="1ebca-107">The **Signers** object represents a collection of [**Signer**](signer.md) objects.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="1ebca-108">Quand l’utiliser</span><span class="sxs-lookup"><span data-stu-id="1ebca-108">When to use</span></span>

<span data-ttu-id="1ebca-109">L’objet **signataires** est utilisé pour effectuer les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="1ebca-109">The **Signers** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="1ebca-110">Récupérez le nombre de certificats dans la collection.</span><span class="sxs-lookup"><span data-stu-id="1ebca-110">Retrieve the number of certificates in the collection.</span></span>
-   <span data-ttu-id="1ebca-111">Récupérez un objet **signataires** spécifique de la collection.</span><span class="sxs-lookup"><span data-stu-id="1ebca-111">Retrieve a specific **Signers** object from the collection.</span></span>
-   <span data-ttu-id="1ebca-112">Itérez au sein de la collection.</span><span class="sxs-lookup"><span data-stu-id="1ebca-112">Iterate through the collection.</span></span>

## <a name="members"></a><span data-ttu-id="1ebca-113">Membres</span><span class="sxs-lookup"><span data-stu-id="1ebca-113">Members</span></span>

<span data-ttu-id="1ebca-114">L’objet **signataires** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="1ebca-114">The **Signers** object has these types of members:</span></span>

-   [<span data-ttu-id="1ebca-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="1ebca-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1ebca-116">Propriétés</span><span class="sxs-lookup"><span data-stu-id="1ebca-116">Properties</span></span>

<span data-ttu-id="1ebca-117">L’objet des **signataires** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="1ebca-117">The **Signers** object has these properties.</span></span>



| <span data-ttu-id="1ebca-118">Propriété</span><span class="sxs-lookup"><span data-stu-id="1ebca-118">Property</span></span>                                        | <span data-ttu-id="1ebca-119">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="1ebca-119">Access type</span></span>          | <span data-ttu-id="1ebca-120">Description</span><span class="sxs-lookup"><span data-stu-id="1ebca-120">Description</span></span>                                                                                                                                                                                                                     |
|:------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1ebca-121">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="1ebca-121">**\_NewEnum**</span></span>](signers-newenum.md)<br/> | <span data-ttu-id="1ebca-122">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1ebca-122">Read-only</span></span><br/> | <span data-ttu-id="1ebca-123">Récupère une interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) sur un objet qui peut être utilisé pour énumérer la collection.</span><span class="sxs-lookup"><span data-stu-id="1ebca-123">Retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="1ebca-124">Cette propriété est masquée dans Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="1ebca-124">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span><br/> |
| [<span data-ttu-id="1ebca-125">**Saut**</span><span class="sxs-lookup"><span data-stu-id="1ebca-125">**Count**</span></span>](signers-count.md)<br/>       | <span data-ttu-id="1ebca-126">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1ebca-126">Read-only</span></span><br/> | <span data-ttu-id="1ebca-127">Nombre d’objets [**signataires**](signer.md) dans la collection.</span><span class="sxs-lookup"><span data-stu-id="1ebca-127">Number of [**Signer**](signer.md) objects in the collection.</span></span><br/>                                                                                                                                                        |
| [<span data-ttu-id="1ebca-128">**Élément**</span><span class="sxs-lookup"><span data-stu-id="1ebca-128">**Item**</span></span>](signers-item.md)<br/>         | <span data-ttu-id="1ebca-129">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="1ebca-129">Read-only</span></span><br/> | <span data-ttu-id="1ebca-130">Récupère l’objet [**signataire**](signer.md) qui représente le signataire indexé.</span><span class="sxs-lookup"><span data-stu-id="1ebca-130">Retrieves the [**Signer**](signer.md) object that represents the indexed signer.</span></span> <span data-ttu-id="1ebca-131">Il s’agit de la propriété par défaut.</span><span class="sxs-lookup"><span data-stu-id="1ebca-131">This is the default property.</span></span><br/>                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="1ebca-132">Notes</span><span class="sxs-lookup"><span data-stu-id="1ebca-132">Remarks</span></span>

<span data-ttu-id="1ebca-133">Impossible de créer l’objet des **signataires** .</span><span class="sxs-lookup"><span data-stu-id="1ebca-133">The **Signers** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ebca-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1ebca-134">Requirements</span></span>



| <span data-ttu-id="1ebca-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1ebca-135">Requirement</span></span> | <span data-ttu-id="1ebca-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="1ebca-136">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1ebca-137">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="1ebca-137">Redistributable</span></span><br/> | <span data-ttu-id="1ebca-138">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="1ebca-138">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="1ebca-139">DLL</span><span class="sxs-lookup"><span data-stu-id="1ebca-139">DLL</span></span><br/>             | <dl> <span data-ttu-id="1ebca-140"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1ebca-140"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ebca-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1ebca-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ebca-142">**Objets de chiffrement**</span><span class="sxs-lookup"><span data-stu-id="1ebca-142">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
