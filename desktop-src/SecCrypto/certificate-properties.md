---
description: Les services de certificats prennent en charge l’utilisation de certificats tels que définis dans la recommandation ITU-T X. 509 (également ISO/IEC 9594-8).
ms.assetid: 59f20de0-de24-43c7-a1a2-bdc91ee28059
title: Propriétés du certificat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbc234f574e0b5bef2d4884706584b5c33ea9c31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864362"
---
# <a name="certificate-properties"></a><span data-ttu-id="36bad-103">Propriétés du certificat</span><span class="sxs-lookup"><span data-stu-id="36bad-103">Certificate Properties</span></span>

<span data-ttu-id="36bad-104">Les services de certificats prennent en charge l’utilisation de certificats tels que définis dans la recommandation ITU-T [*X. 509*](../secgloss/x-gly.md) (également ISO/IEC 9594-8).</span><span class="sxs-lookup"><span data-stu-id="36bad-104">Certificate Services supports the use of certificates as defined in the ITU-T recommendation [*X.509*](../secgloss/x-gly.md) (also, ISO/IEC 9594-8).</span></span> <span data-ttu-id="36bad-105">Voici les propriétés contenues dans un certificat X. 509 standard.</span><span class="sxs-lookup"><span data-stu-id="36bad-105">The following are properties that are contained in a standard X.509 certificate.</span></span>



| <span data-ttu-id="36bad-106">Champ</span><span class="sxs-lookup"><span data-stu-id="36bad-106">Field</span></span>                                       | <span data-ttu-id="36bad-107">Description</span><span class="sxs-lookup"><span data-stu-id="36bad-107">Description</span></span>                                                                                                                                                                                                     |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36bad-108">Version</span><span class="sxs-lookup"><span data-stu-id="36bad-108">Version</span></span>                                     | <span data-ttu-id="36bad-109">Numéro de version du format du certificat.</span><span class="sxs-lookup"><span data-stu-id="36bad-109">Version number of the certificate format.</span></span>                                                                                                                                                                       |
| <span data-ttu-id="36bad-110">Numéro de série</span><span class="sxs-lookup"><span data-stu-id="36bad-110">Serial Number</span></span>                               | <span data-ttu-id="36bad-111">Numéro de série du certificat.</span><span class="sxs-lookup"><span data-stu-id="36bad-111">Serial number of the certificate.</span></span> <span data-ttu-id="36bad-112">Ce nombre est attribué par l’émetteur et est unique dans la liste des certificats émis de l’émetteur.</span><span class="sxs-lookup"><span data-stu-id="36bad-112">This number is assigned by the issuer and is unique within the issuer's list of issued certificates.</span></span>                                                                          |
| <span data-ttu-id="36bad-113">Identificateurs et paramètres d’algorithme</span><span class="sxs-lookup"><span data-stu-id="36bad-113">Algorithm Identifier and Parameters</span></span>         | <span data-ttu-id="36bad-114">Algorithme de signature et tous les paramètres utilisés par l’émetteur.</span><span class="sxs-lookup"><span data-stu-id="36bad-114">Signature algorithm and any parameters used by the issuer.</span></span>                                                                                                                                                      |
| <span data-ttu-id="36bad-115">Émetteur</span><span class="sxs-lookup"><span data-stu-id="36bad-115">Issuer</span></span>                                      | <span data-ttu-id="36bad-116">Nom de l' [*autorité de certification*](../secgloss/c-gly.md) qui a émis le certificat.</span><span class="sxs-lookup"><span data-stu-id="36bad-116">Name of the [*certification authority*](../secgloss/c-gly.md) which issued the certificate.</span></span>                                               |
| <span data-ttu-id="36bad-117">Pas avant (date)</span><span class="sxs-lookup"><span data-stu-id="36bad-117">Not Before (Date)</span></span>                           | <span data-ttu-id="36bad-118">Le certificat n’est pas valide avant cette date.</span><span class="sxs-lookup"><span data-stu-id="36bad-118">Certificate not valid before this date.</span></span>                                                                                                                                                                         |
| <span data-ttu-id="36bad-119">Pas après (date)</span><span class="sxs-lookup"><span data-stu-id="36bad-119">Not After (Date)</span></span>                            | <span data-ttu-id="36bad-120">Le certificat n’est pas valide après cette date.</span><span class="sxs-lookup"><span data-stu-id="36bad-120">Certificate not valid after this date.</span></span>                                                                                                                                                                          |
| <span data-ttu-id="36bad-121">Nom de sujet</span><span class="sxs-lookup"><span data-stu-id="36bad-121">Subject Name</span></span>                                | <span data-ttu-id="36bad-122">Nom de la personne ou de l’entité à qui le certificat est émis.</span><span class="sxs-lookup"><span data-stu-id="36bad-122">Name of the person or entity to whom the certificate is being issued.</span></span> <span data-ttu-id="36bad-123">Ce champ peut également inclure l’organisation, l’unité d’organisation, la localité, l’État ou la région, le pays ou la région du destinataire du certificat.</span><span class="sxs-lookup"><span data-stu-id="36bad-123">This field can also include the certificate recipient's organization, organization unit, locality, state or province, and country/region.</span></span> |
| <span data-ttu-id="36bad-124">Algorithme de clé publique de l’objet et paramètres</span><span class="sxs-lookup"><span data-stu-id="36bad-124">Subject Public Key Algorithm and Parameters</span></span> | <span data-ttu-id="36bad-125">L’algorithme et les paramètres utilisés pour la [*clé publique*](../secgloss/p-gly.md)du sujet.</span><span class="sxs-lookup"><span data-stu-id="36bad-125">The algorithm and any parameters used for the subject's [*public key*](../secgloss/p-gly.md).</span></span>                                                                       |
| <span data-ttu-id="36bad-126">Clé publique de l’objet</span><span class="sxs-lookup"><span data-stu-id="36bad-126">Subject Public Key</span></span>                          | <span data-ttu-id="36bad-127">Clé publique réelle (une chaîne de bits).</span><span class="sxs-lookup"><span data-stu-id="36bad-127">The actual public key (a bit string).</span></span>                                                                                                                                                                           |
| <span data-ttu-id="36bad-128">Signature</span><span class="sxs-lookup"><span data-stu-id="36bad-128">Signature</span></span>                                   | <span data-ttu-id="36bad-129">Signature fournie par l’émetteur.</span><span class="sxs-lookup"><span data-stu-id="36bad-129">Signature as provided by the issuer.</span></span>                                                                                                                                                                            |



 

<span data-ttu-id="36bad-130">Un certificat peut contenir les éléments suivants, en fonction de la version [*X. 509*](../secgloss/x-gly.md) du certificat.</span><span class="sxs-lookup"><span data-stu-id="36bad-130">A certificate can contain the following items, depending on the [*X.509*](../secgloss/x-gly.md) version of the certificate.</span></span>



| <span data-ttu-id="36bad-131">Champ facultatif</span><span class="sxs-lookup"><span data-stu-id="36bad-131">Optional field</span></span>    | <span data-ttu-id="36bad-132">Description</span><span class="sxs-lookup"><span data-stu-id="36bad-132">Description</span></span>                                                                                                                                                                                               |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36bad-133">ID unique de l’émetteur</span><span class="sxs-lookup"><span data-stu-id="36bad-133">Issuer Unique ID</span></span>  | <span data-ttu-id="36bad-134">Utilisé pour rendre le nom de l’émetteur non ambigu s’il a été utilisé par plusieurs entités.</span><span class="sxs-lookup"><span data-stu-id="36bad-134">Used to make the issuer name unambiguous if it has been used by more than one entity.</span></span> <span data-ttu-id="36bad-135">Présent uniquement dans les versions [*X. 509*](../secgloss/x-gly.md) 2,0 ou ultérieures.</span><span class="sxs-lookup"><span data-stu-id="36bad-135">Present only in versions [*X.509*](../secgloss/x-gly.md) 2.0 or later.</span></span><br/> |
| <span data-ttu-id="36bad-136">ID unique de l’objet</span><span class="sxs-lookup"><span data-stu-id="36bad-136">Subject unique ID</span></span> | <span data-ttu-id="36bad-137">Permet de rendre le nom de l’objet non ambigu s’il a été utilisé par plusieurs entités.</span><span class="sxs-lookup"><span data-stu-id="36bad-137">Used to make the subject name unambiguous if it has been used by more than one entity.</span></span> <span data-ttu-id="36bad-138">Présent uniquement dans X. 509 2,0 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="36bad-138">Present only in X.509 2.0 or later.</span></span><br/>                                                                     |
| <span data-ttu-id="36bad-139">Extensions</span><span class="sxs-lookup"><span data-stu-id="36bad-139">Extensions</span></span>        | <span data-ttu-id="36bad-140">Pour spécifier les propriétés personnalisées souhaitées.</span><span class="sxs-lookup"><span data-stu-id="36bad-140">For specifying any desired custom properties.</span></span> <span data-ttu-id="36bad-141">N’importe quel nombre de champs d’extension peut être inclus dans le certificat.</span><span class="sxs-lookup"><span data-stu-id="36bad-141">Any number of extension fields can be included in the certificate.</span></span> <span data-ttu-id="36bad-142">Présent uniquement dans la version X. 509 3,0.</span><span class="sxs-lookup"><span data-stu-id="36bad-142">Present only in version X.509 3.0.</span></span><br/>                                            |



 

> [!Note]  
> <span data-ttu-id="36bad-143">Les services de certificats Microsoft délivrent des certificats X. 509 version 3.</span><span class="sxs-lookup"><span data-stu-id="36bad-143">Microsoft Certificate Services issues X.509 version 3 certificates.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="36bad-144">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="36bad-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="36bad-145">Propriétés du nom</span><span class="sxs-lookup"><span data-stu-id="36bad-145">Name Properties</span></span>](name-properties.md)
</dt> </dl>

 

 
