---
description: Révocation de certificat OPM
ms.assetid: 21faf809-1335-4d93-be06-628c5a05a4c8
title: Révocation de certificat OPM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47ebf38a3fa6bd2b61a756d6103453fd0356f693
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108092727"
---
# <a name="opm-certificate-revocation"></a><span data-ttu-id="eae17-103">Révocation de certificat OPM</span><span class="sxs-lookup"><span data-stu-id="eae17-103">OPM Certificate Revocation</span></span>

<span data-ttu-id="eae17-104">Un certificat de sortie Protection Manager (OPM) peut être révoqué par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="eae17-104">An output protection manager (OPM) certificate can be revoked by Microsoft.</span></span> <span data-ttu-id="eae17-105">La liste des certificats révoqués est stockée dans une liste de révocation globale (GRL).</span><span class="sxs-lookup"><span data-stu-id="eae17-105">The list of revoked certificates is stored in a global revocation list (GRL).</span></span> <span data-ttu-id="eae17-106">Le GRL a le format suivant :</span><span class="sxs-lookup"><span data-stu-id="eae17-106">The GRL has the following format:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="eae17-107">Section</span><span class="sxs-lookup"><span data-stu-id="eae17-107">Section</span></span></th>
<th><span data-ttu-id="eae17-108">Description</span><span class="sxs-lookup"><span data-stu-id="eae17-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="eae17-109">En-tête</span><span class="sxs-lookup"><span data-stu-id="eae17-109">Header</span></span></td>
<td><span data-ttu-id="eae17-110">Structure <a href="grl-header.md"><strong>GRL_HEADER</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="eae17-110">A <a href="grl-header.md"><strong>GRL_HEADER</strong></a> structure.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eae17-111">Base</span><span class="sxs-lookup"><span data-stu-id="eae17-111">Core</span></span></td>
<td><span data-ttu-id="eae17-112">Contient les listes de révocation suivantes :</span><span class="sxs-lookup"><span data-stu-id="eae17-112">Contains the following revocation lists:</span></span>
<ul>
<li><span data-ttu-id="eae17-113">Révocations binaires du noyau</span><span class="sxs-lookup"><span data-stu-id="eae17-113">Kernel binary revocations</span></span></li>
<li><span data-ttu-id="eae17-114">Révocations binaires en mode utilisateur</span><span class="sxs-lookup"><span data-stu-id="eae17-114">User-mode binary revocations</span></span></li>
<li><span data-ttu-id="eae17-115">Révocations de certificats</span><span class="sxs-lookup"><span data-stu-id="eae17-115">Certificate revocations</span></span></li>
<li><span data-ttu-id="eae17-116">Racines de confiance (réservées)</span><span class="sxs-lookup"><span data-stu-id="eae17-116">Trusted roots (reserved)</span></span></li>
</ul>
<span data-ttu-id="eae17-117">La liste des racines de confiance n’est pas utilisée actuellement et est réservée à une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="eae17-117">The list of trusted roots is currently not used, and is reserved for future use.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eae17-118">Entrées extensibles</span><span class="sxs-lookup"><span data-stu-id="eae17-118">Extensible entries</span></span></td>
<td><span data-ttu-id="eae17-119">Contient des informations utilisées par d’autres composants.</span><span class="sxs-lookup"><span data-stu-id="eae17-119">Contains information used by other components.</span></span> <span data-ttu-id="eae17-120">Cette section ne concerne pas OPM.</span><span class="sxs-lookup"><span data-stu-id="eae17-120">This section is not relevant to OPM.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eae17-121">Renouvellements</span><span class="sxs-lookup"><span data-stu-id="eae17-121">Renewals:</span></span></td>
<td><span data-ttu-id="eae17-122">Contient des GUID qui définissent des identificateurs de Windows Update.</span><span class="sxs-lookup"><span data-stu-id="eae17-122">Contains GUIDs that define Windows Update identifiers.</span></span> <span data-ttu-id="eae17-123">Cette section contient des identificateurs pour les listes suivantes :</span><span class="sxs-lookup"><span data-stu-id="eae17-123">This section contains identifiers for the following lists:</span></span>
<ul>
<li><span data-ttu-id="eae17-124">Révocations binaires du noyau</span><span class="sxs-lookup"><span data-stu-id="eae17-124">Kernel binary revocations</span></span></li>
<li><span data-ttu-id="eae17-125">Révocations binaires en mode utilisateur</span><span class="sxs-lookup"><span data-stu-id="eae17-125">User-mode binary revocations</span></span></li>
<li><span data-ttu-id="eae17-126">Révocations de certificats</span><span class="sxs-lookup"><span data-stu-id="eae17-126">Certificate revocations</span></span></li>
</ul>
<span data-ttu-id="eae17-127">Une application peut utiliser ces identificateurs pour demander une version renouvelée d’un binaire révoqué, si celle-ci est disponible.</span><span class="sxs-lookup"><span data-stu-id="eae17-127">An application can use these identifiers to request a renewed version of a revoked binary, if one is available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eae17-128">Signature : section principale</span><span class="sxs-lookup"><span data-stu-id="eae17-128">Signature: Core section</span></span></td>
<td><span data-ttu-id="eae17-129">Signe l’en-tête et les sections principales.</span><span class="sxs-lookup"><span data-stu-id="eae17-129">Signs the header and core sections.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eae17-130">Signature : section extensible</span><span class="sxs-lookup"><span data-stu-id="eae17-130">Signature: Extensible section</span></span></td>
<td><span data-ttu-id="eae17-131">Signe l’en-tête et les sections extensibles.</span><span class="sxs-lookup"><span data-stu-id="eae17-131">Signs the header and extensible sections.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="eae17-132">L’en-tête GRL est une structure d' [**\_ en-tête GRL**](grl-header.md) .</span><span class="sxs-lookup"><span data-stu-id="eae17-132">The GRL header is a [**GRL\_HEADER**](grl-header.md) structure.</span></span> <span data-ttu-id="eae17-133">Le membre **dwSequenceNumber** de la structure contient le numéro de version GRL.</span><span class="sxs-lookup"><span data-stu-id="eae17-133">The **dwSequenceNumber** member of the structure contains the GRL version number.</span></span> <span data-ttu-id="eae17-134">Ce nombre est incrémenté chaque fois que le GRL est mis à jour et qu’une nouvelle version est placée sur l’ordinateur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="eae17-134">This number is incremented whenever the GRL is updated and a new version placed on the user's computer.</span></span>

<span data-ttu-id="eae17-135">Les certificats OPM révoqués sont répertoriés dans la liste de révocation des certificats de la section principale.</span><span class="sxs-lookup"><span data-stu-id="eae17-135">Revoked OPM certificates are listed in the certificate revocations list of the Core section.</span></span> <span data-ttu-id="eae17-136">Chaque entrée de cœur dans le GRL est un tableau de 20 octets qui contient le hachage SHA-1 de la clé publique du certificat révoqué.</span><span class="sxs-lookup"><span data-stu-id="eae17-136">Each Core entry in the GRL is a 20-byte array that contains the SHA-1 hash of the public key of the revoked certificate.</span></span>

<span data-ttu-id="eae17-137">Les sections signature contiennent des signatures qui peuvent être utilisées pour vérifier que le GRL n’a pas été falsifié.</span><span class="sxs-lookup"><span data-stu-id="eae17-137">The Signature sections contains signatures that can be used to verify that the GRL has not been tampered with.</span></span> <span data-ttu-id="eae17-138">Chaque section de signature contient la structure de [**\_ signature am MF**](mf-signature.md) .</span><span class="sxs-lookup"><span data-stu-id="eae17-138">Each Signature sections contains am [**MF\_SIGNATURE**](mf-signature.md) structure.</span></span> <span data-ttu-id="eae17-139">La première signature signe l’en-tête plus la section principale.</span><span class="sxs-lookup"><span data-stu-id="eae17-139">The first signature signs the header plus the Core section.</span></span> <span data-ttu-id="eae17-140">La deuxième signature signe l’en-tête plus la section extensible ; Cette signature n’est pas pertinente pour OPM.</span><span class="sxs-lookup"><span data-stu-id="eae17-140">The second signature signs the header plus the Extensible section; this signature is not relevant to OPM.</span></span>

<span data-ttu-id="eae17-141">Pour vous assurer que le GRL lui-même n’a pas été falsifié, vérifiez la signature comme suit :</span><span class="sxs-lookup"><span data-stu-id="eae17-141">To ensure that the GRL itself has not been tampered with, verify the signature as follows:</span></span>

1.  <span data-ttu-id="eae17-142">Recherche le début de la structure de [**\_ signature MF**](mf-signature.md) .</span><span class="sxs-lookup"><span data-stu-id="eae17-142">Find the start of the [**MF\_SIGNATURE**](mf-signature.md) structure.</span></span> <span data-ttu-id="eae17-143">L’emplacement de la structure de **\_ signature MF** est indiqué dans le membre **cbSignatureCoreOffset** de la structure d' [**\_ en-tête GRL**](grl-header.md) .</span><span class="sxs-lookup"><span data-stu-id="eae17-143">The location of the **MF\_SIGNATURE** structure is given in the **cbSignatureCoreOffset** member of the [**GRL\_HEADER**](grl-header.md) structure.</span></span> <span data-ttu-id="eae17-144">L’emplacement est spécifié en tant que décalage en octets à partir du début du GRL.</span><span class="sxs-lookup"><span data-stu-id="eae17-144">The location is specified as an offset in bytes from the start of the GRL.</span></span>
2.  <span data-ttu-id="eae17-145">Analyser la structure de [**\_ signature MF**](mf-signature.md) en tant que \# signature PKCS 7 avec une chaîne de certificats.</span><span class="sxs-lookup"><span data-stu-id="eae17-145">Parse the [**MF\_SIGNATURE**](mf-signature.md) structure as a PKCS \#7 signature with a certificate chain.</span></span>
3.  <span data-ttu-id="eae17-146">Vérifiez la chaîne de certificats jusqu’à une racine approuvée.</span><span class="sxs-lookup"><span data-stu-id="eae17-146">Verify the certificate chain up to a trusted root.</span></span>
4.  <span data-ttu-id="eae17-147">Vérifiez que le certificat feuille a l’identificateur d’objet suivant dans l’EKU : « 1.3.6.1.4.1.311.10.5.4 ».</span><span class="sxs-lookup"><span data-stu-id="eae17-147">Verify that the leaf certificate has the following object identifier in the EKU: "1.3.6.1.4.1.311.10.5.4".</span></span>
5.  <span data-ttu-id="eae17-148">Calculez un hachage des octets qui incluent l’en-tête et les sections principales du GRL.</span><span class="sxs-lookup"><span data-stu-id="eae17-148">Compute a hash of the bytes that include the header and the core sections of the GRL.</span></span>
6.  <span data-ttu-id="eae17-149">Vérifiez que le hachage correspond à la signature dans le certificat feuille.</span><span class="sxs-lookup"><span data-stu-id="eae17-149">Verify that the hash matches the signature in the leaf certificate.</span></span>

## <a name="related-topics"></a><span data-ttu-id="eae17-150">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="eae17-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eae17-151">Gestionnaire de protection de sortie</span><span class="sxs-lookup"><span data-stu-id="eae17-151">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> <dt>

[<span data-ttu-id="eae17-152">**\_en-tête GRL**</span><span class="sxs-lookup"><span data-stu-id="eae17-152">**GRL\_HEADER**</span></span>](grl-header.md)
</dt> <dt>

[<span data-ttu-id="eae17-153">**\_signature MF**</span><span class="sxs-lookup"><span data-stu-id="eae17-153">**MF\_SIGNATURE**</span></span>](mf-signature.md)
</dt> </dl>

 

 



