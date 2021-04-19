---
description: Fournit un accès en lecture seule aux propriétés d’utilisation améliorée de la clé d’un certificat.
ms.assetid: 636d7f65-d286-4800-a576-a23e6e9811b2
title: Objet ExtendedKeyUsage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedKeyUsage
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5a93be1f6fe75559d0284ca955ca5b6e9c516eed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537567"
---
# <a name="extendedkeyusage-object"></a><span data-ttu-id="3084e-103">Objet ExtendedKeyUsage</span><span class="sxs-lookup"><span data-stu-id="3084e-103">ExtendedKeyUsage object</span></span>

<span data-ttu-id="3084e-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="3084e-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="3084e-105">Utilisez plutôt la [**classe X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="3084e-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="3084e-106">L’objet **ExtendedKeyUsage** fournit un accès en lecture seule aux propriétés d’utilisation améliorée de la clé d’un certificat.</span><span class="sxs-lookup"><span data-stu-id="3084e-106">The **ExtendedKeyUsage** object provides read-only access to the extended key usage (EKU) properties of a certificate.</span></span>

## <a name="members"></a><span data-ttu-id="3084e-107">Membres</span><span class="sxs-lookup"><span data-stu-id="3084e-107">Members</span></span>

<span data-ttu-id="3084e-108">L’objet **ExtendedKeyUsage** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="3084e-108">The **ExtendedKeyUsage** object has these types of members:</span></span>

-   [<span data-ttu-id="3084e-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3084e-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3084e-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3084e-110">Properties</span></span>

<span data-ttu-id="3084e-111">L’objet **ExtendedKeyUsage** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="3084e-111">The **ExtendedKeyUsage** object has these properties.</span></span>



| <span data-ttu-id="3084e-112">Propriété</span><span class="sxs-lookup"><span data-stu-id="3084e-112">Property</span></span>                                                     | <span data-ttu-id="3084e-113">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="3084e-113">Access type</span></span>          | <span data-ttu-id="3084e-114">Description</span><span class="sxs-lookup"><span data-stu-id="3084e-114">Description</span></span>                                                                                                                             |
|:-------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3084e-115">**Utilisations améliorées de la clé**</span><span class="sxs-lookup"><span data-stu-id="3084e-115">**EKUs**</span></span>](extendedkeyusage-ekus.md)<br/>             | <span data-ttu-id="3084e-116">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3084e-116">Read-only</span></span><br/> | <span data-ttu-id="3084e-117">[**Collection de EKU qui**](ekus.md) contient les objets [**EKU**](eku.md) pour le certificat.</span><span class="sxs-lookup"><span data-stu-id="3084e-117">[**EKUs**](ekus.md) collection that contains the [**EKU**](eku.md) objects for the certificate.</span></span><br/>                            |
| [<span data-ttu-id="3084e-118">**IsCritical**</span><span class="sxs-lookup"><span data-stu-id="3084e-118">**IsCritical**</span></span>](extendedkeyusage-iscritical.md)<br/> | <span data-ttu-id="3084e-119">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3084e-119">Read-only</span></span><br/> | <span data-ttu-id="3084e-120">Récupère une valeur **booléenne** qui indique si l’extension d’utilisation améliorée de la clé est marquée comme critique.</span><span class="sxs-lookup"><span data-stu-id="3084e-120">Retrieves a **Boolean** value that indicates whether the EKU extension is marked critical.</span></span><br/>                                   |
| [<span data-ttu-id="3084e-121">**IsPresent**</span><span class="sxs-lookup"><span data-stu-id="3084e-121">**IsPresent**</span></span>](extendedkeyusage-ispresent.md)<br/>   | <span data-ttu-id="3084e-122">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3084e-122">Read-only</span></span><br/> | <span data-ttu-id="3084e-123">Récupère une valeur **booléenne** qui indique si l’extension EKU est présente.</span><span class="sxs-lookup"><span data-stu-id="3084e-123">Retrieves a **Boolean** value that indicates whether the EKU extension is present.</span></span><br/> <span data-ttu-id="3084e-124">Il s’agit de la propriété par défaut.</span><span class="sxs-lookup"><span data-stu-id="3084e-124">This is the default property.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="3084e-125">Notes</span><span class="sxs-lookup"><span data-stu-id="3084e-125">Remarks</span></span>

<span data-ttu-id="3084e-126">Impossible de créer l’objet **ExtendedKeyUsage** .</span><span class="sxs-lookup"><span data-stu-id="3084e-126">The **ExtendedKeyUsage** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="3084e-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3084e-127">Requirements</span></span>



| <span data-ttu-id="3084e-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3084e-128">Requirement</span></span> | <span data-ttu-id="3084e-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="3084e-129">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3084e-130">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="3084e-130">End of client support</span></span><br/> | <span data-ttu-id="3084e-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3084e-131">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="3084e-132">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="3084e-132">End of server support</span></span><br/> | <span data-ttu-id="3084e-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3084e-133">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="3084e-134">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="3084e-134">Redistributable</span></span><br/>       | <span data-ttu-id="3084e-135">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="3084e-135">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="3084e-136">DLL</span><span class="sxs-lookup"><span data-stu-id="3084e-136">DLL</span></span><br/>                   | <dl> <span data-ttu-id="3084e-137"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3084e-137"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3084e-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3084e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3084e-139">**Objets de chiffrement**</span><span class="sxs-lookup"><span data-stu-id="3084e-139">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
