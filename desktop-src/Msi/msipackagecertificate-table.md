---
description: Le tableau MsiPackageCertificate répertorie les certificats de signature numérique utilisés pour vérifier l’identité des packages d’installation qui effectuent cette installation Multiple-Package.
ms.assetid: d3a97325-2136-4745-8a7d-57e4d6b9d27e
title: Table MsiPackageCertificate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fd39ac93ff24da2fa8334a6e4865172471080b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210780"
---
# <a name="msipackagecertificate-table"></a><span data-ttu-id="20cd7-103">Table MsiPackageCertificate</span><span class="sxs-lookup"><span data-stu-id="20cd7-103">MsiPackageCertificate Table</span></span>

<span data-ttu-id="20cd7-104">Le tableau MsiPackageCertificate répertorie les certificats de signature numérique utilisés pour vérifier l’identité des packages d’installation qui effectuent cette [installation de plusieurs packages](multiple-package-installations.md).</span><span class="sxs-lookup"><span data-stu-id="20cd7-104">The MsiPackageCertificate Table lists digital signature certificates used to verify the identity of the installation packages that make this [Multiple-Package Installation](multiple-package-installations.md).</span></span>

<span data-ttu-id="20cd7-105">Utilisez ce tableau pour créer une [installation de plusieurs](multiple-package-installations.md) packages pour un produit contenant plusieurs packages de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="20cd7-105">Use this table to author a [multiple-package installation](multiple-package-installations.md) for a product containing multiple Windows Installer packages.</span></span> <span data-ttu-id="20cd7-106">Si le premier package est signé numériquement et contient une table MsiPackageCertificate spécifiant des certificats numériques pour tous les packages restants dans le produit, l’administrateur doit uniquement accepter l’invite de [*contrôle de compte d’utilisateur*](u-gly.md) (UAC) affichée pour le premier package.</span><span class="sxs-lookup"><span data-stu-id="20cd7-106">If the first package is digitally signed, and contains a MsiPackageCertificate Table specifying digital certificates for all the remaining packages in the product, the administrator needs only accept the [*User Account Control*](u-gly.md) (UAC) prompt displayed for the first package.</span></span> <span data-ttu-id="20cd7-107">Après avoir accepté l’invite du contrôle de compte d’utilisateur pour le premier package, les fonctions définies par l’utilisateur dans la [table MsiEmbeddedChainer](msiembeddedchainer-table.md) peuvent ensuite joindre les packages restants à l’installation de plusieurs packages sans afficher d’invite UAC et exiger une réponse de l’administrateur pour chaque package.</span><span class="sxs-lookup"><span data-stu-id="20cd7-107">After accepting the UAC's prompt for the first package, the user-defined functions in the [MsiEmbeddedChainer table](msiembeddedchainer-table.md) can then join the remaining packages to the multiple-package installation without displaying a UAC prompt and requiring an administrator response for each package.</span></span>

<span data-ttu-id="20cd7-108">Si une ou plusieurs des fonctions de la [table MsiEmbeddedChainer](msiembeddedchainer-table.md) demandent un package non signé, une autre invite UAC demandant l’intervention de l’administrateur s’affiche pour chaque package non signé.</span><span class="sxs-lookup"><span data-stu-id="20cd7-108">If one or more of the functions in the [MsiEmbeddedChainer table](msiembeddedchainer-table.md) request an unsigned package, another UAC prompt requiring administrator interaction is displayed for each unsigned package.</span></span> <span data-ttu-id="20cd7-109">Si l’administrateur accepte cette invite de contrôle de compte d’utilisateur, l’installation de plusieurs packages se poursuit.</span><span class="sxs-lookup"><span data-stu-id="20cd7-109">If the administrator accepts this UAC prompt, the multi-package installation continues.</span></span> <span data-ttu-id="20cd7-110">Une fois qu’un administrateur a fourni les informations d’identification d’un package, aucune invite UAC ne s’affiche à nouveau pour ce package lors de l’installation de plusieurs packages.</span><span class="sxs-lookup"><span data-stu-id="20cd7-110">Once an administrator has provided credentials for a package, no UAC prompt will again be displayed for that package during this multi-package installation.</span></span> <span data-ttu-id="20cd7-111">Si l’administrateur rejette une invite de contrôle de compte d’utilisateur pour un package, le programme d’installation de Windows restaure l’installation de plusieurs packages avant de valider l’installation des packages appartenant au produit.</span><span class="sxs-lookup"><span data-stu-id="20cd7-111">If the administrator rejects a UAC prompt for a package, the Windows installer rolls back the multi-package installation before it commits to install any packages belonging to the product.</span></span>

<span data-ttu-id="20cd7-112">**[Windows Installer 4,0 ou version antérieure](not-supported-in-windows-installer-4-0.md):** Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="20cd7-112">**[Windows Installer 4.0 or earlier](not-supported-in-windows-installer-4-0.md):** Not supported.</span></span> <span data-ttu-id="20cd7-113">Cette table est disponible à partir de Windows Installer 4,5.</span><span class="sxs-lookup"><span data-stu-id="20cd7-113">This table is available beginning with Windows Installer 4.5.</span></span>

<span data-ttu-id="20cd7-114">La table MsiPackageCertificate contient les colonnes suivantes :</span><span class="sxs-lookup"><span data-stu-id="20cd7-114">The MsiPackageCertificate Table has the following columns:</span></span>



| <span data-ttu-id="20cd7-115">Colonne</span><span class="sxs-lookup"><span data-stu-id="20cd7-115">Column</span></span>               | <span data-ttu-id="20cd7-116">Type</span><span class="sxs-lookup"><span data-stu-id="20cd7-116">Type</span></span>                         | <span data-ttu-id="20cd7-117">Clé</span><span class="sxs-lookup"><span data-stu-id="20cd7-117">Key</span></span> | <span data-ttu-id="20cd7-118">Nullable</span><span class="sxs-lookup"><span data-stu-id="20cd7-118">Nullable</span></span> |
|----------------------|------------------------------|-----|----------|
| <span data-ttu-id="20cd7-119">PackageCertificate</span><span class="sxs-lookup"><span data-stu-id="20cd7-119">PackageCertificate</span></span>   | [<span data-ttu-id="20cd7-120">Identificateur</span><span class="sxs-lookup"><span data-stu-id="20cd7-120">Identifier</span></span>](identifier.md) | <span data-ttu-id="20cd7-121">O</span><span class="sxs-lookup"><span data-stu-id="20cd7-121">Y</span></span>   | <span data-ttu-id="20cd7-122">N</span><span class="sxs-lookup"><span data-stu-id="20cd7-122">N</span></span>        |
| <span data-ttu-id="20cd7-123">DigitalCertificate\_</span><span class="sxs-lookup"><span data-stu-id="20cd7-123">DigitalCertificate\_</span></span> | [<span data-ttu-id="20cd7-124">Identificateur</span><span class="sxs-lookup"><span data-stu-id="20cd7-124">Identifier</span></span>](identifier.md) | <span data-ttu-id="20cd7-125">N</span><span class="sxs-lookup"><span data-stu-id="20cd7-125">N</span></span>   | <span data-ttu-id="20cd7-126">N</span><span class="sxs-lookup"><span data-stu-id="20cd7-126">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="20cd7-127">Colonnes</span><span class="sxs-lookup"><span data-stu-id="20cd7-127">Columns</span></span>

<dl> <dt>

<span data-ttu-id="20cd7-128"><span id="PackageCertificate"></span><span id="packagecertificate"></span><span id="PACKAGECERTIFICATE"></span>PackageCertificate</span><span class="sxs-lookup"><span data-stu-id="20cd7-128"><span id="PackageCertificate"></span><span id="packagecertificate"></span><span id="PACKAGECERTIFICATE"></span>PackageCertificate</span></span>
</dt> <dd>

<span data-ttu-id="20cd7-129">Identificateur unique de cette ligne dans la table MsiPackageCertificate.</span><span class="sxs-lookup"><span data-stu-id="20cd7-129">The unique identifier for this row in the MsiPackageCertificate Table.</span></span>

</dd> <dt>

<span data-ttu-id="20cd7-130"><span id="DigitalCertificate"></span><span id="digitalcertificate"></span><span id="DIGITALCERTIFICATE"></span>DigitalCertificate</span><span class="sxs-lookup"><span data-stu-id="20cd7-130"><span id="DigitalCertificate"></span><span id="digitalcertificate"></span><span id="DIGITALCERTIFICATE"></span>DigitalCertificate</span></span>
</dt> <dd>

<span data-ttu-id="20cd7-131">Une clé externe dans la première colonne de la [table MsiDigitalCertificate](msidigitalcertificate-table.md).</span><span class="sxs-lookup"><span data-stu-id="20cd7-131">An external key into the first column of the [MsiDigitalCertificate Table](msidigitalcertificate-table.md).</span></span> <span data-ttu-id="20cd7-132">La ligne indiquée dans la table MsiDigitalCertificate contient la représentation binaire du certificat du signataire.</span><span class="sxs-lookup"><span data-stu-id="20cd7-132">The row indicated in the MsiDigitalCertificate Table contains the binary representation of the signer certificate.</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="20cd7-133">Validation</span><span class="sxs-lookup"><span data-stu-id="20cd7-133">Validation</span></span>

<dl>

[<span data-ttu-id="20cd7-134">ICE39</span><span class="sxs-lookup"><span data-stu-id="20cd7-134">ICE39</span></span>](ice39.md)  
[<span data-ttu-id="20cd7-135">ICE81</span><span class="sxs-lookup"><span data-stu-id="20cd7-135">ICE81</span></span>](ice81.md)  
</dl>

## <a name="related-topics"></a><span data-ttu-id="20cd7-136">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="20cd7-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="20cd7-137">MsiEmbeddedChainer</span><span class="sxs-lookup"><span data-stu-id="20cd7-137">MsiEmbeddedChainer</span></span>](msiembeddedchainer-table.md)
</dt> <dt>

[<span data-ttu-id="20cd7-138">Table MsiDigitalCertificate</span><span class="sxs-lookup"><span data-stu-id="20cd7-138">MsiDigitalCertificate Table</span></span>](msidigitalcertificate-table.md)
</dt> </dl>

 

 



