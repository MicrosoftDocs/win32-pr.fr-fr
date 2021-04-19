---
description: Représente une extension de certificat unique.
ms.assetid: cca3121d-0f0f-4de2-a225-6dd3910078d7
title: Objet d’extension (Mmcobj. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Extension
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: a048cd5f29825c2d96a9d924473159e93d3e0be1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532574"
---
# <a name="extension-object"></a><span data-ttu-id="fda48-103">Objet d’extension</span><span class="sxs-lookup"><span data-stu-id="fda48-103">Extension object</span></span>

<span data-ttu-id="fda48-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="fda48-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="fda48-105">Utilisez plutôt la [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="fda48-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="fda48-106">L’objet d' **extension** représente une extension de certificat unique.</span><span class="sxs-lookup"><span data-stu-id="fda48-106">The **Extension** object represents a single certificate extension.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="fda48-107">Quand l’utiliser</span><span class="sxs-lookup"><span data-stu-id="fda48-107">When to use</span></span>

<span data-ttu-id="fda48-108">L’objet d' **extension** est utilisé pour effectuer les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="fda48-108">The **Extension** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="fda48-109">Récupérez l’OID de l’extension de certificat.</span><span class="sxs-lookup"><span data-stu-id="fda48-109">Retrieve the OID of the certificate extension.</span></span>
-   <span data-ttu-id="fda48-110">Récupérer les données d’extension de certificat représentées par un objet [**EncodedData**](encodeddata.md) .</span><span class="sxs-lookup"><span data-stu-id="fda48-110">Retrieve the certificate extension data represented by an [**EncodedData**](encodeddata.md) object.</span></span>
-   <span data-ttu-id="fda48-111">Déterminez si l’extension de certificat est marquée comme critique.</span><span class="sxs-lookup"><span data-stu-id="fda48-111">Determine whether the certificate extension is marked as critical.</span></span>

## <a name="members"></a><span data-ttu-id="fda48-112">Membres</span><span class="sxs-lookup"><span data-stu-id="fda48-112">Members</span></span>

<span data-ttu-id="fda48-113">L’objet d' **extension** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="fda48-113">The **Extension** object has these types of members:</span></span>

-   [<span data-ttu-id="fda48-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="fda48-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fda48-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="fda48-115">Properties</span></span>

<span data-ttu-id="fda48-116">L’objet d' **extension** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="fda48-116">The **Extension** object has these properties.</span></span>



| <span data-ttu-id="fda48-117">Propriété</span><span class="sxs-lookup"><span data-stu-id="fda48-117">Property</span></span>                                                | <span data-ttu-id="fda48-118">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="fda48-118">Access type</span></span>          | <span data-ttu-id="fda48-119">Description</span><span class="sxs-lookup"><span data-stu-id="fda48-119">Description</span></span>                                                                                   |
|:--------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fda48-120">**EncodedData**</span><span class="sxs-lookup"><span data-stu-id="fda48-120">**EncodedData**</span></span>](extension-encodeddata.md)<br/> | <span data-ttu-id="fda48-121">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fda48-121">Read-only</span></span><br/> | <span data-ttu-id="fda48-122">Récupère les données encodées pour l’extension.</span><span class="sxs-lookup"><span data-stu-id="fda48-122">Retrieves the encoded data for the extension.</span></span><br/>                                      |
| [<span data-ttu-id="fda48-123">**IsCritical**</span><span class="sxs-lookup"><span data-stu-id="fda48-123">**IsCritical**</span></span>](extension-iscritical.md)<br/>   | <span data-ttu-id="fda48-124">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fda48-124">Read-only</span></span><br/> | <span data-ttu-id="fda48-125">Récupère une valeur booléenne qui indique si l’extension est marquée comme critique.</span><span class="sxs-lookup"><span data-stu-id="fda48-125">Retrieves a Boolean value that indicates whether the extension is marked critical.</span></span><br/> |
| [<span data-ttu-id="fda48-126">**OID**</span><span class="sxs-lookup"><span data-stu-id="fda48-126">**OID**</span></span>](extension-oid.md)<br/>                 | <span data-ttu-id="fda48-127">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fda48-127">Read-only</span></span><br/> | <span data-ttu-id="fda48-128">Récupère l’identificateur d’objet pour l’extension.</span><span class="sxs-lookup"><span data-stu-id="fda48-128">Retrieves the object identifier for the extension.</span></span> <span data-ttu-id="fda48-129">Il s’agit de la propriété par défaut.</span><span class="sxs-lookup"><span data-stu-id="fda48-129">This is the default property.</span></span><br/>   |



 

## <a name="remarks"></a><span data-ttu-id="fda48-130">Notes</span><span class="sxs-lookup"><span data-stu-id="fda48-130">Remarks</span></span>

<span data-ttu-id="fda48-131">Impossible de créer l’objet d' **extension** .</span><span class="sxs-lookup"><span data-stu-id="fda48-131">The **Extension** object cannot be created.</span></span>

<span data-ttu-id="fda48-132">L’objet d' **extension** est utilisé par l’objet de collection d' [**Extensions**](extensions.md) .</span><span class="sxs-lookup"><span data-stu-id="fda48-132">The **Extension** object is used by the [**Extensions**](extensions.md) collection object.</span></span>

## <a name="requirements"></a><span data-ttu-id="fda48-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fda48-133">Requirements</span></span>



| <span data-ttu-id="fda48-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fda48-134">Requirement</span></span> | <span data-ttu-id="fda48-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="fda48-135">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fda48-136">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="fda48-136">End of client support</span></span><br/> | <span data-ttu-id="fda48-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fda48-137">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="fda48-138">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="fda48-138">End of server support</span></span><br/> | <span data-ttu-id="fda48-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fda48-139">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="fda48-140">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="fda48-140">Redistributable</span></span><br/>       | <span data-ttu-id="fda48-141">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="fda48-141">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="fda48-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="fda48-142">Header</span></span><br/>                | <dl> <span data-ttu-id="fda48-143"><dt>Mmcobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="fda48-143"><dt>Mmcobj.h</dt></span></span> </dl>    |
| <span data-ttu-id="fda48-144">DLL</span><span class="sxs-lookup"><span data-stu-id="fda48-144">DLL</span></span><br/>                   | <dl> <span data-ttu-id="fda48-145"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fda48-145"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
