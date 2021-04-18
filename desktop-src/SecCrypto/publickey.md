---
description: L’objet PublicKey représente une clé publique dans un objet de certificat.
title: PublicKey, objet
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PublicKey
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 12ab8fcf61d30b47fc809fb05e1ffa524bb2488e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526686"
---
# <a name="publickey-object"></a><span data-ttu-id="d092e-103">PublicKey, objet</span><span class="sxs-lookup"><span data-stu-id="d092e-103">PublicKey object</span></span>

<span data-ttu-id="d092e-104">\[L’objet **PublicKey** peut être utilisé dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.</span><span class="sxs-lookup"><span data-stu-id="d092e-104">\[The **PublicKey** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="d092e-105">Utilisez plutôt la [**propriété X509Certificate2. PublicKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.publickey?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="d092e-105">Instead, use the [**X509Certificate2.PublicKey Property**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.publickey?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="d092e-106">L’objet **PublicKey** représente une clé publique dans un objet de [**certificat**](certificate.md) .</span><span class="sxs-lookup"><span data-stu-id="d092e-106">The **PublicKey** object represents a public key in a [**Certificate**](certificate.md) object.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="d092e-107">Quand l’utiliser</span><span class="sxs-lookup"><span data-stu-id="d092e-107">When to use</span></span>

<span data-ttu-id="d092e-108">L’objet **PublicKey** est utilisé pour récupérer les données relatives à la clé publique.</span><span class="sxs-lookup"><span data-stu-id="d092e-108">The **PublicKey** object is used to retrieve data about the public key.</span></span>

## <a name="members"></a><span data-ttu-id="d092e-109">Membres</span><span class="sxs-lookup"><span data-stu-id="d092e-109">Members</span></span>

<span data-ttu-id="d092e-110">L’objet **PublicKey** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="d092e-110">The **PublicKey** object has these types of members:</span></span>

-   [<span data-ttu-id="d092e-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d092e-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d092e-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d092e-112">Properties</span></span>

<span data-ttu-id="d092e-113">L’objet **PublicKey** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="d092e-113">The **PublicKey** object has these properties.</span></span>



| <span data-ttu-id="d092e-114">Propriété</span><span class="sxs-lookup"><span data-stu-id="d092e-114">Property</span></span>                                                            | <span data-ttu-id="d092e-115">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="d092e-115">Access type</span></span>          | <span data-ttu-id="d092e-116">Description</span><span class="sxs-lookup"><span data-stu-id="d092e-116">Description</span></span>                                                                                                                            |
|:--------------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d092e-117">**Algorithme**</span><span class="sxs-lookup"><span data-stu-id="d092e-117">**Algorithm**</span></span>](publickey-algorithm.md)<br/>                 | <span data-ttu-id="d092e-118">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d092e-118">Read-only</span></span><br/> | <span data-ttu-id="d092e-119">Récupère l’objet [**OID**](oid.md) qui identifie l’algorithme utilisé par la clé publique.</span><span class="sxs-lookup"><span data-stu-id="d092e-119">Retrieves the [**OID**](oid.md) object that identifies the algorithm used by the public key.</span></span> <span data-ttu-id="d092e-120">Il s’agit de la propriété par défaut.</span><span class="sxs-lookup"><span data-stu-id="d092e-120">This is the default property.</span></span><br/> |
| [<span data-ttu-id="d092e-121">**EncodedKey**</span><span class="sxs-lookup"><span data-stu-id="d092e-121">**EncodedKey**</span></span>](publickey-encodedkey.md)<br/>               | <span data-ttu-id="d092e-122">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d092e-122">Read-only</span></span><br/> | <span data-ttu-id="d092e-123">Récupère un objet [**EncodedData**](encodeddata.md) qui fournit l’accès à la valeur de la clé publique.</span><span class="sxs-lookup"><span data-stu-id="d092e-123">Retrieves an [**EncodedData**](encodeddata.md) object that provides access to the value of the public key.</span></span><br/>                 |
| [<span data-ttu-id="d092e-124">**EncodedParameters**</span><span class="sxs-lookup"><span data-stu-id="d092e-124">**EncodedParameters**</span></span>](publickey-encodedparameters.md)<br/> | <span data-ttu-id="d092e-125">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d092e-125">Read-only</span></span><br/> | <span data-ttu-id="d092e-126">Récupère un objet [**EncodedData**](encodeddata.md) qui fournit l’accès aux paramètres de l’algorithme de clé publique.</span><span class="sxs-lookup"><span data-stu-id="d092e-126">Retrieves an [**EncodedData**](encodeddata.md) object that provides access to the parameters of the public key algorithm.</span></span><br/>  |
| [<span data-ttu-id="d092e-127">**Longueur**</span><span class="sxs-lookup"><span data-stu-id="d092e-127">**Length**</span></span>](publickey-length.md)<br/>                       | <span data-ttu-id="d092e-128">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d092e-128">Read-only</span></span><br/> | <span data-ttu-id="d092e-129">Récupère la longueur de la clé publique en bits.</span><span class="sxs-lookup"><span data-stu-id="d092e-129">Retrieves the length of the public key in bits.</span></span><br/>                                                                             |



 

## <a name="remarks"></a><span data-ttu-id="d092e-130">Notes</span><span class="sxs-lookup"><span data-stu-id="d092e-130">Remarks</span></span>

<span data-ttu-id="d092e-131">Impossible de créer l’objet **PublicKey** .</span><span class="sxs-lookup"><span data-stu-id="d092e-131">The **PublicKey** object cannot be created.</span></span>

<span data-ttu-id="d092e-132">L’objet **PublicKey** est utilisé par la méthode [**Certificate. PublicKey**](certificate-publickey.md) .</span><span class="sxs-lookup"><span data-stu-id="d092e-132">The **PublicKey** object is used by the [**Certificate.PublicKey**](certificate-publickey.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="d092e-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d092e-133">Requirements</span></span>



| <span data-ttu-id="d092e-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d092e-134">Requirement</span></span> | <span data-ttu-id="d092e-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="d092e-135">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d092e-136">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="d092e-136">Redistributable</span></span><br/> | <span data-ttu-id="d092e-137">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="d092e-137">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="d092e-138">DLL</span><span class="sxs-lookup"><span data-stu-id="d092e-138">DLL</span></span><br/>             | <dl> <span data-ttu-id="d092e-139"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d092e-139"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
