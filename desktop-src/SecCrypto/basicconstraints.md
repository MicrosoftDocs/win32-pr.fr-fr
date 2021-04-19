---
description: Représente l’extension de contraintes de base d’un certificat.
ms.assetid: c21794f6-7654-4140-8114-0edb398d6de8
title: Objet BasicConstraints
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BasicConstraints
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 85e912542b09b02297f5119392115857259f70f0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541677"
---
# <a name="basicconstraints-object"></a><span data-ttu-id="a1122-103">Objet BasicConstraints</span><span class="sxs-lookup"><span data-stu-id="a1122-103">BasicConstraints object</span></span>

<span data-ttu-id="a1122-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista, Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a1122-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="a1122-105">Utilisez plutôt la [**classe X509BasicConstraintsExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509basicconstraintsextension?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/previous-versions/windows/) .\]</span><span class="sxs-lookup"><span data-stu-id="a1122-105">Instead, use the [**X509BasicConstraintsExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509basicconstraintsextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/previous-versions/windows/) namespace.\]</span></span>

<span data-ttu-id="a1122-106">L’objet **basicConstraints** représente l’extension de contraintes de base d’un certificat.</span><span class="sxs-lookup"><span data-stu-id="a1122-106">The **BasicConstraints** object represents the basic constraints extension of a certificate.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="a1122-107">Quand l’utiliser</span><span class="sxs-lookup"><span data-stu-id="a1122-107">When to use</span></span>

<span data-ttu-id="a1122-108">L’objet **basicConstraints** est utilisé pour effectuer les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="a1122-108">The **BasicConstraints** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="a1122-109">Déterminez si l’extension de contraintes de base est présente.</span><span class="sxs-lookup"><span data-stu-id="a1122-109">Determine whether the basic constraints extension is present.</span></span>
-   <span data-ttu-id="a1122-110">Déterminez si l’extension de contraintes de base est marquée comme critique.</span><span class="sxs-lookup"><span data-stu-id="a1122-110">Determine whether the basic constraints extension is marked critical.</span></span>
-   <span data-ttu-id="a1122-111">Déterminez si le certificat est imposé aux autorités de certification.</span><span class="sxs-lookup"><span data-stu-id="a1122-111">Determine whether the certificate is constrained to certificate authorities.</span></span>
-   <span data-ttu-id="a1122-112">Déterminez si la contrainte de longueur de chemin d’accès est présente et récupérez la valeur de contrainte de longueur du chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="a1122-112">Determine whether the path length constraint is present and retrieve the path length constraint value.</span></span>

## <a name="members"></a><span data-ttu-id="a1122-113">Membres</span><span class="sxs-lookup"><span data-stu-id="a1122-113">Members</span></span>

<span data-ttu-id="a1122-114">L’objet **basicConstraints** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="a1122-114">The **BasicConstraints** object has these types of members:</span></span>

-   [<span data-ttu-id="a1122-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a1122-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a1122-116">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a1122-116">Properties</span></span>

<span data-ttu-id="a1122-117">L’objet **basicConstraints** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="a1122-117">The **BasicConstraints** object has these properties.</span></span>



| <span data-ttu-id="a1122-118">Propriété</span><span class="sxs-lookup"><span data-stu-id="a1122-118">Property</span></span>                                                                                     | <span data-ttu-id="a1122-119">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="a1122-119">Access type</span></span>          | <span data-ttu-id="a1122-120">Description</span><span class="sxs-lookup"><span data-stu-id="a1122-120">Description</span></span>                                                                                                                                                                                                        |
|:---------------------------------------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a1122-121">**IsCertificateAuthority**</span><span class="sxs-lookup"><span data-stu-id="a1122-121">**IsCertificateAuthority**</span></span>](basicconstraints-iscertificateauthority.md)<br/>         | <span data-ttu-id="a1122-122">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a1122-122">Read-only</span></span><br/> | <span data-ttu-id="a1122-123">Récupère une valeur booléenne qui indique si le certificat est destiné à une [*autorité de certification*](../secgloss/c-gly.md) (ca).</span><span class="sxs-lookup"><span data-stu-id="a1122-123">Retrieves a Boolean value that indicates whether the certificate is for a [*certification authority*](../secgloss/c-gly.md) (CA).</span></span><br/> |
| [<span data-ttu-id="a1122-124">**IsCritical**</span><span class="sxs-lookup"><span data-stu-id="a1122-124">**IsCritical**</span></span>](basicconstraints-iscritical.md)<br/>                                 | <span data-ttu-id="a1122-125">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a1122-125">Read-only</span></span><br/> | <span data-ttu-id="a1122-126">Récupère une valeur booléenne qui indique si l’extension de contrainte de base est marquée comme critique.</span><span class="sxs-lookup"><span data-stu-id="a1122-126">Retrieves a Boolean value that indicates whether the basic constraint extension is marked critical.</span></span><br/>                                                                                                     |
| [<span data-ttu-id="a1122-127">**IsPathLenConstraintPresent**</span><span class="sxs-lookup"><span data-stu-id="a1122-127">**IsPathLenConstraintPresent**</span></span>](basicconstraints-ispathlenconstraintpresent.md)<br/> | <span data-ttu-id="a1122-128">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a1122-128">Read-only</span></span><br/> | <span data-ttu-id="a1122-129">Récupère une valeur booléenne qui indique si la contrainte de longueur de chemin d’accès du certificat est présente.</span><span class="sxs-lookup"><span data-stu-id="a1122-129">Retrieves a Boolean value that indicates whether the certificate's path length constraint is present.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="a1122-130">**IsPresent**</span><span class="sxs-lookup"><span data-stu-id="a1122-130">**IsPresent**</span></span>](basicconstraints-ispresent.md)<br/>                                   | <span data-ttu-id="a1122-131">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a1122-131">Read-only</span></span><br/> | <span data-ttu-id="a1122-132">Récupère une valeur booléenne qui indique si l’extension de contraintes de base est présente.</span><span class="sxs-lookup"><span data-stu-id="a1122-132">Retrieves a Boolean value that indicates whether the basic constraints extension is present.</span></span> <span data-ttu-id="a1122-133">Il s’agit de la propriété par défaut.</span><span class="sxs-lookup"><span data-stu-id="a1122-133">This is the default property.</span></span><br/>                                                                              |
| [<span data-ttu-id="a1122-134">**PathLenConstraint**</span><span class="sxs-lookup"><span data-stu-id="a1122-134">**PathLenConstraint**</span></span>](basicconstraints-pathlenconstraint.md)<br/>                   | <span data-ttu-id="a1122-135">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a1122-135">Read-only</span></span><br/> | <span data-ttu-id="a1122-136">Récupère la valeur de la contrainte de longueur de chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="a1122-136">Retrieves the value of the path length constraint.</span></span><br/>                                                                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="a1122-137">Notes</span><span class="sxs-lookup"><span data-stu-id="a1122-137">Remarks</span></span>

<span data-ttu-id="a1122-138">Impossible de créer l’objet **basicConstraints** .</span><span class="sxs-lookup"><span data-stu-id="a1122-138">The **BasicConstraints** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1122-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a1122-139">Requirements</span></span>



| <span data-ttu-id="a1122-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a1122-140">Requirement</span></span> | <span data-ttu-id="a1122-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="a1122-141">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a1122-142">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="a1122-142">End of client support</span></span><br/> | <span data-ttu-id="a1122-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a1122-143">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="a1122-144">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="a1122-144">End of server support</span></span><br/> | <span data-ttu-id="a1122-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a1122-145">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="a1122-146">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="a1122-146">Redistributable</span></span><br/>       | <span data-ttu-id="a1122-147">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="a1122-147">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="a1122-148">DLL</span><span class="sxs-lookup"><span data-stu-id="a1122-148">DLL</span></span><br/>                   | <dl> <span data-ttu-id="a1122-149"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a1122-149"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1122-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a1122-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1122-151">Objets de chiffrement</span><span class="sxs-lookup"><span data-stu-id="a1122-151">Cryptography Objects</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
