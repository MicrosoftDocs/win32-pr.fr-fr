---
description: Identifie les certificats de signataire possibles utilisés pour signer numériquement les correctifs.
ms.assetid: 8f76c27d-92f1-4de7-a69c-fba877e0325d
title: Table MsiPatchCertificate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01648e792931fd856a1231a5d876c7db843479df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034640"
---
# <a name="msipatchcertificate-table"></a><span data-ttu-id="649fb-103">Table MsiPatchCertificate</span><span class="sxs-lookup"><span data-stu-id="649fb-103">MsiPatchCertificate Table</span></span>

<span data-ttu-id="649fb-104">La table MsiPatchCertificate identifie les certificats de signataire possibles utilisés pour signer numériquement les correctifs.</span><span class="sxs-lookup"><span data-stu-id="649fb-104">The MsiPatchCertificate Table identifies the possible signer certificates used to digitally sign patches.</span></span> <span data-ttu-id="649fb-105">La table MsiPatchCertificate contient les informations nécessaires pour activer la mise à [jour corrective du contrôle de compte d’utilisateur (UAC)](user-account-control--uac--patching.md) pour une application.</span><span class="sxs-lookup"><span data-stu-id="649fb-105">The MsiPatchCertificate Table contains the information that is needed to enable [User Account Control (UAC) Patching](user-account-control--uac--patching.md) for an application.</span></span>

<span data-ttu-id="649fb-106">La table MsiPatchCertificate contient les colonnes suivantes :</span><span class="sxs-lookup"><span data-stu-id="649fb-106">The MsiPatchCertificate Table has the following columns:</span></span>



| <span data-ttu-id="649fb-107">Colonne</span><span class="sxs-lookup"><span data-stu-id="649fb-107">Column</span></span>               | <span data-ttu-id="649fb-108">Type</span><span class="sxs-lookup"><span data-stu-id="649fb-108">Type</span></span>                         | <span data-ttu-id="649fb-109">Clé</span><span class="sxs-lookup"><span data-stu-id="649fb-109">Key</span></span> | <span data-ttu-id="649fb-110">Nullable</span><span class="sxs-lookup"><span data-stu-id="649fb-110">Nullable</span></span> |
|----------------------|------------------------------|-----|----------|
| <span data-ttu-id="649fb-111">PatchCertificate</span><span class="sxs-lookup"><span data-stu-id="649fb-111">PatchCertificate</span></span>     | [<span data-ttu-id="649fb-112">Identificateur</span><span class="sxs-lookup"><span data-stu-id="649fb-112">Identifier</span></span>](identifier.md) | <span data-ttu-id="649fb-113">O</span><span class="sxs-lookup"><span data-stu-id="649fb-113">Y</span></span>   | <span data-ttu-id="649fb-114">N</span><span class="sxs-lookup"><span data-stu-id="649fb-114">N</span></span>        |
| <span data-ttu-id="649fb-115">DigitalCertificate\_</span><span class="sxs-lookup"><span data-stu-id="649fb-115">DigitalCertificate\_</span></span> | [<span data-ttu-id="649fb-116">Identificateur</span><span class="sxs-lookup"><span data-stu-id="649fb-116">Identifier</span></span>](identifier.md) | <span data-ttu-id="649fb-117">N</span><span class="sxs-lookup"><span data-stu-id="649fb-117">N</span></span>   | <span data-ttu-id="649fb-118">N</span><span class="sxs-lookup"><span data-stu-id="649fb-118">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="649fb-119">Colonnes</span><span class="sxs-lookup"><span data-stu-id="649fb-119">Columns</span></span>

<dl> <dt>

<span data-ttu-id="649fb-120"><span id="PatchCertificate"></span><span id="patchcertificate"></span><span id="PATCHCERTIFICATE"></span>PatchCertificate</span><span class="sxs-lookup"><span data-stu-id="649fb-120"><span id="PatchCertificate"></span><span id="patchcertificate"></span><span id="PATCHCERTIFICATE"></span>PatchCertificate</span></span>
</dt> <dd>

<span data-ttu-id="649fb-121">Identificateur unique de cette ligne dans la table MsiPatchCertificate.</span><span class="sxs-lookup"><span data-stu-id="649fb-121">The unique identifier for this row in the MsiPatchCertificate Table.</span></span>

</dd> <dt>

<span data-ttu-id="649fb-122"><span id="DigitalCertificate"></span><span id="digitalcertificate"></span><span id="DIGITALCERTIFICATE"></span>DigitalCertificate</span><span class="sxs-lookup"><span data-stu-id="649fb-122"><span id="DigitalCertificate"></span><span id="digitalcertificate"></span><span id="DIGITALCERTIFICATE"></span>DigitalCertificate</span></span>
</dt> <dd>

<span data-ttu-id="649fb-123">Une clé externe dans la première colonne de la [table MsiDigitalCertificate](msidigitalcertificate-table.md).</span><span class="sxs-lookup"><span data-stu-id="649fb-123">An external key into the first column of the [MsiDigitalCertificate Table](msidigitalcertificate-table.md).</span></span> <span data-ttu-id="649fb-124">La ligne indiquée dans la table MsiDigitalCertificate contient la représentation binaire du certificat du signataire.</span><span class="sxs-lookup"><span data-stu-id="649fb-124">The row indicated in the MsiDigitalCertificate Table contains the binary representation of the signer certificate.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="649fb-125">Notes</span><span class="sxs-lookup"><span data-stu-id="649fb-125">Remarks</span></span>

<span data-ttu-id="649fb-126">Les correctifs sont toujours évalués par rapport à la table MsiPatchCertificate qui est active au moment de l’application du correctif.</span><span class="sxs-lookup"><span data-stu-id="649fb-126">Patches are always evaluated against the MsiPatchCertificate Table that is current at the time the patch is applied.</span></span> <span data-ttu-id="649fb-127">Un correctif peut modifier la table MsiPatchCertificate en ajoutant ou en supprimant des entrées.</span><span class="sxs-lookup"><span data-stu-id="649fb-127">A patch can modify the MsiPatchCertificate Table by adding or removing entries.</span></span> <span data-ttu-id="649fb-128">Cela permet à un correctif de modifier l’évaluation des futurs correctifs appliqués ultérieurement dans la séquence de mise à jour corrective.</span><span class="sxs-lookup"><span data-stu-id="649fb-128">This enables a patch to modify the evaluation of future patches that are applied later in the patching sequence.</span></span> <span data-ttu-id="649fb-129">Plusieurs certificats peuvent exister dans la table, et le correctif doit correspondre à au moins un certificat à appliquer.</span><span class="sxs-lookup"><span data-stu-id="649fb-129">Multiple certificates can exist in the table, and the patch must match at least one certificate to be applied.</span></span>

## <a name="validation"></a><span data-ttu-id="649fb-130">Validation</span><span class="sxs-lookup"><span data-stu-id="649fb-130">Validation</span></span>

<dl>

[<span data-ttu-id="649fb-131">ICE03</span><span class="sxs-lookup"><span data-stu-id="649fb-131">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="649fb-132">ICE06</span><span class="sxs-lookup"><span data-stu-id="649fb-132">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="649fb-133">ICE32</span><span class="sxs-lookup"><span data-stu-id="649fb-133">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="649fb-134">ICE81</span><span class="sxs-lookup"><span data-stu-id="649fb-134">ICE81</span></span>](ice81.md)  
</dl>

## <a name="related-topics"></a><span data-ttu-id="649fb-135">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="649fb-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="649fb-136">DisableLUAPatching</span><span class="sxs-lookup"><span data-stu-id="649fb-136">DisableLUAPatching</span></span>](disableluapatching.md)
</dt> <dt>

[<span data-ttu-id="649fb-137">Mise à jour corrective du contrôle de compte d’utilisateur (UAC)</span><span class="sxs-lookup"><span data-stu-id="649fb-137">User Account Control (UAC) Patching</span></span>](user-account-control--uac--patching.md)
</dt> <dt>

[<span data-ttu-id="649fb-138">**MSIDISABLELUAPATCHING**</span><span class="sxs-lookup"><span data-stu-id="649fb-138">**MSIDISABLELUAPATCHING**</span></span>](msidisableluapatching.md)
</dt> <dt>

[<span data-ttu-id="649fb-139">Signatures numériques et Windows Installer</span><span class="sxs-lookup"><span data-stu-id="649fb-139">Digital Signatures and Windows Installer</span></span>](digital-signatures-and-windows-installer.md)
</dt> <dt>

[<span data-ttu-id="649fb-140">Non pris en charge dans Windows Installer 2,0 et versions antérieures</span><span class="sxs-lookup"><span data-stu-id="649fb-140">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



