---
description: La table MsiDigitalSignature contient les informations de signature pour chaque objet signé numériquement dans la base de données d’installation.
ms.assetid: 63d62152-4f01-454f-bdea-550f2a9f6b14
title: Table MsiDigitalSignature
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd0ec22b9a399b6248fd3b2781e1ac8d7ae14324
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527412"
---
# <a name="msidigitalsignature-table"></a><span data-ttu-id="0d326-103">Table MsiDigitalSignature</span><span class="sxs-lookup"><span data-stu-id="0d326-103">MsiDigitalSignature Table</span></span>

<span data-ttu-id="0d326-104">La table MsiDigitalSignature contient les informations de signature pour chaque objet signé numériquement dans la base de données d’installation.</span><span class="sxs-lookup"><span data-stu-id="0d326-104">The MsiDigitalSignature table contains the signature information for every digitally signed object in the installation database.</span></span>

<span data-ttu-id="0d326-105">Les tables MsiDigitalSignature et [MsiDigitalCertificate](msidigitalcertificate-table.md) sont disponibles à partir de Windows Installer version 2,0.</span><span class="sxs-lookup"><span data-stu-id="0d326-105">The MsiDigitalSignature and [MsiDigitalCertificate](msidigitalcertificate-table.md) tables are available starting with Windows Installer version 2.0.</span></span>

<span data-ttu-id="0d326-106">Windows Installer version peut utiliser des signatures numériques pour détecter les ressources endommagées.</span><span class="sxs-lookup"><span data-stu-id="0d326-106">Windows Installer version can use digital signatures as a means to detect corrupted resources.</span></span> <span data-ttu-id="0d326-107">Windows Installer 2,0 peut uniquement vérifier les signatures numériques des armoires externes, et uniquement à l’aide des tables MsiDigitalSignature et [MsiDigitalCertificate](msidigitalcertificate-table.md) .</span><span class="sxs-lookup"><span data-stu-id="0d326-107">Windows Installer 2.0 can only verify the digital signatures of external cabinets, and only by the use of the MsiDigitalSignature and [MsiDigitalCertificate](msidigitalcertificate-table.md) tables.</span></span>

<span data-ttu-id="0d326-108">À partir de Windows Installer 3,0, le Windows Installer peut vérifier les signatures numériques des correctifs (fichiers. msp) à l’aide des tables [MsiPatchCertificate](msipatchcertificate-table.md) et MsiDigitalCertificate.</span><span class="sxs-lookup"><span data-stu-id="0d326-108">Beginning with Windows Installer 3.0, the Windows Installer can verify the digital signatures of patches (.msp files) by using the [MsiPatchCertificate](msipatchcertificate-table.md) and MsiDigitalCertificate tables.</span></span> <span data-ttu-id="0d326-109">Pour plus d’informations, consultez Instructions pour la création d’une mise à [jour corrective](user-account-control--uac--patching.md)des [installations sécurisées et du contrôle de compte d'](guidelines-for-authoring-secure-installations.md) utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0d326-109">For more information, see [Guidelines for Authoring Secure Installations](guidelines-for-authoring-secure-installations.md) and [User Account Control (UAC) Patching](user-account-control--uac--patching.md).</span></span>

<span data-ttu-id="0d326-110">La table MsiDigitalSignature contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="0d326-110">The MsiDigitalSignature table has the following columns.</span></span>



| <span data-ttu-id="0d326-111">Colonne</span><span class="sxs-lookup"><span data-stu-id="0d326-111">Column</span></span>               | <span data-ttu-id="0d326-112">Type</span><span class="sxs-lookup"><span data-stu-id="0d326-112">Type</span></span>                         | <span data-ttu-id="0d326-113">Clé</span><span class="sxs-lookup"><span data-stu-id="0d326-113">Key</span></span> | <span data-ttu-id="0d326-114">Nullable</span><span class="sxs-lookup"><span data-stu-id="0d326-114">Nullable</span></span> |
|----------------------|------------------------------|-----|----------|
| <span data-ttu-id="0d326-115">Table de charge de travail</span><span class="sxs-lookup"><span data-stu-id="0d326-115">Table</span></span>                | [<span data-ttu-id="0d326-116">Identificateur</span><span class="sxs-lookup"><span data-stu-id="0d326-116">Identifier</span></span>](identifier.md) | <span data-ttu-id="0d326-117">O</span><span class="sxs-lookup"><span data-stu-id="0d326-117">Y</span></span>   | <span data-ttu-id="0d326-118">N</span><span class="sxs-lookup"><span data-stu-id="0d326-118">N</span></span>        |
| <span data-ttu-id="0d326-119">SignObject</span><span class="sxs-lookup"><span data-stu-id="0d326-119">SignObject</span></span>           | [<span data-ttu-id="0d326-120">Text</span><span class="sxs-lookup"><span data-stu-id="0d326-120">Text</span></span>](text.md)             | <span data-ttu-id="0d326-121">O</span><span class="sxs-lookup"><span data-stu-id="0d326-121">Y</span></span>   | <span data-ttu-id="0d326-122">N</span><span class="sxs-lookup"><span data-stu-id="0d326-122">N</span></span>        |
| <span data-ttu-id="0d326-123">DigitalCertificate\_</span><span class="sxs-lookup"><span data-stu-id="0d326-123">DigitalCertificate\_</span></span> | [<span data-ttu-id="0d326-124">Identificateur</span><span class="sxs-lookup"><span data-stu-id="0d326-124">Identifier</span></span>](identifier.md) | <span data-ttu-id="0d326-125">N</span><span class="sxs-lookup"><span data-stu-id="0d326-125">N</span></span>   | <span data-ttu-id="0d326-126">N</span><span class="sxs-lookup"><span data-stu-id="0d326-126">N</span></span>        |
| <span data-ttu-id="0d326-127">Hachage</span><span class="sxs-lookup"><span data-stu-id="0d326-127">Hash</span></span>                 | [<span data-ttu-id="0d326-128">Binaire</span><span class="sxs-lookup"><span data-stu-id="0d326-128">Binary</span></span>](binary.md)         | <span data-ttu-id="0d326-129">N</span><span class="sxs-lookup"><span data-stu-id="0d326-129">N</span></span>   | <span data-ttu-id="0d326-130">O</span><span class="sxs-lookup"><span data-stu-id="0d326-130">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="0d326-131">Colonnes</span><span class="sxs-lookup"><span data-stu-id="0d326-131">Columns</span></span>

<dl> <dt>

<span data-ttu-id="0d326-132"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Tableau</span><span class="sxs-lookup"><span data-stu-id="0d326-132"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Table</span></span>
</dt> <dd>

<span data-ttu-id="0d326-133">Avec la version de Windows Installer 2,0, l’entrée de ce champ doit être « Media » pour la [table Media](media-table.md).</span><span class="sxs-lookup"><span data-stu-id="0d326-133">With the Windows Installer version 2.0, the entry in this field must be "Media" for the [Media table](media-table.md).</span></span> <span data-ttu-id="0d326-134">Le programme d’installation vérifie uniquement les signatures numériques sur les entrées de média du fichier CAB externe.</span><span class="sxs-lookup"><span data-stu-id="0d326-134">The installer only verifies the digital signatures on external cabinet media entries.</span></span> <span data-ttu-id="0d326-135">Cette colonne et la colonne SignObject spécifient ensemble la ressource signée numériquement.</span><span class="sxs-lookup"><span data-stu-id="0d326-135">This column and the SignObject column together specify the resource that is digitally signed.</span></span>

</dd> <dt>

<span data-ttu-id="0d326-136"><span id="SignObject"></span><span id="signobject"></span><span id="SIGNOBJECT"></span>SignObject</span><span class="sxs-lookup"><span data-stu-id="0d326-136"><span id="SignObject"></span><span id="signobject"></span><span id="SIGNOBJECT"></span>SignObject</span></span>
</dt> <dd>

<span data-ttu-id="0d326-137">Clé étrangère dans la clé primaire de la table spécifiée par la colonne de table.</span><span class="sxs-lookup"><span data-stu-id="0d326-137">A foreign key into the primary key of the table specified by the Table column.</span></span> <span data-ttu-id="0d326-138">Cette colonne et la colonne de table spécifient ensemble la ressource signée numériquement.</span><span class="sxs-lookup"><span data-stu-id="0d326-138">This column and the Table column together specify the resource that is digitally signed.</span></span>

</dd> <dt>

<span data-ttu-id="0d326-139"><span id="DigitalCertificate_"></span><span id="digitalcertificate_"></span><span id="DIGITALCERTIFICATE_"></span>DigitalCertificate\_</span><span class="sxs-lookup"><span data-stu-id="0d326-139"><span id="DigitalCertificate_"></span><span id="digitalcertificate_"></span><span id="DIGITALCERTIFICATE_"></span>DigitalCertificate\_</span></span>
</dt> <dd>

<span data-ttu-id="0d326-140">Clé étrangère dans la [table MsiDigitalCertificate](msidigitalcertificate-table.md).</span><span class="sxs-lookup"><span data-stu-id="0d326-140">A foreign key into the [MsiDigitalCertificate table](msidigitalcertificate-table.md).</span></span> <span data-ttu-id="0d326-141">Cela identifie le certificat qui doit exister dans le fichier pour que l’action associée aboutisse.</span><span class="sxs-lookup"><span data-stu-id="0d326-141">This identifies the certificate that must exist on the file for the associated action to succeed.</span></span> <span data-ttu-id="0d326-142">La ressource (ou l’objet) est toujours nécessaire pour correspondre à ce certificat dans la table MsiDigitalCertificate.</span><span class="sxs-lookup"><span data-stu-id="0d326-142">The resource (or object) is always required to match this certificate in the MsiDigitalCertificate table.</span></span>

</dd> <dt>

<span data-ttu-id="0d326-143"><span id="Hash"></span><span id="hash"></span><span id="HASH"></span>Format</span><span class="sxs-lookup"><span data-stu-id="0d326-143"><span id="Hash"></span><span id="hash"></span><span id="HASH"></span>Hash</span></span>
</dt> <dd>

<span data-ttu-id="0d326-144">Dans ce champ, entrez le hachage de référence de la ressource (ou objet) qui doit être vérifiée par rapport au hachage réel de la ressource (ou objet) obtenue au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="0d326-144">In this field enter the reference hash of the resource (or object) that is to be checked against the actual hash of the resource (or object) obtained at run-time.</span></span> <span data-ttu-id="0d326-145">Si seul le certificat doit être vérifié, le champ Hash peut avoir la valeur null.</span><span class="sxs-lookup"><span data-stu-id="0d326-145">If only the certificate needs to be verified, the Hash field may be null.</span></span> <span data-ttu-id="0d326-146">Notez que le format du hachage dépend du type de la ressource (ou de l’objet) en cours de signature.</span><span class="sxs-lookup"><span data-stu-id="0d326-146">Note that the format of the hash depends on the type of the resource (or object) being signed.</span></span>

<span data-ttu-id="0d326-147">La colonne Hash contient la représentation binaire du hachage.</span><span class="sxs-lookup"><span data-stu-id="0d326-147">The Hash column contains the binary representation of the hash.</span></span> <span data-ttu-id="0d326-148">Le contenu réel est le membre **pbData** de la structure de l' [**\_ \_ objet blob de hachage énigmatique**](/windows/win32/api/dpapi/ns-dpapi-crypt_integer_blob) , qui fait partie de la structure de l' **\_ objet BLOB CryptoAPI** .</span><span class="sxs-lookup"><span data-stu-id="0d326-148">The actual content is the **pbData** member of the [**CRYPT\_HASH\_BLOB**](/windows/win32/api/dpapi/ns-dpapi-crypt_integer_blob) structure, which is part of the **CRYPTOAPI\_BLOB** structure.</span></span> <span data-ttu-id="0d326-149">Cela peut être obtenu en appelant [WinVerifyTrust](/windows/win32/api/wintrust/nf-wintrust-winverifytrust) ou [**MsiGetFileSignatureInformation**](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa).</span><span class="sxs-lookup"><span data-stu-id="0d326-149">This may be obtained by calling [WinVerifyTrust](/windows/win32/api/wintrust/nf-wintrust-winverifytrust) or [**MsiGetFileSignatureInformation**](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa).</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="0d326-150">Validation</span><span class="sxs-lookup"><span data-stu-id="0d326-150">Validation</span></span>

<dl>

[<span data-ttu-id="0d326-151">ICE03</span><span class="sxs-lookup"><span data-stu-id="0d326-151">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="0d326-152">ICE06</span><span class="sxs-lookup"><span data-stu-id="0d326-152">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="0d326-153">ICE29</span><span class="sxs-lookup"><span data-stu-id="0d326-153">ICE29</span></span>](ice29.md)  
[<span data-ttu-id="0d326-154">ICE32</span><span class="sxs-lookup"><span data-stu-id="0d326-154">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="0d326-155">ICE66</span><span class="sxs-lookup"><span data-stu-id="0d326-155">ICE66</span></span>](ice66.md)  
[<span data-ttu-id="0d326-156">ICE81</span><span class="sxs-lookup"><span data-stu-id="0d326-156">ICE81</span></span>](ice81.md)  
</dl>

## <a name="related-topics"></a><span data-ttu-id="0d326-157">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0d326-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0d326-158">**MsiGetFileSignatureInformation**</span><span class="sxs-lookup"><span data-stu-id="0d326-158">**MsiGetFileSignatureInformation**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa)
</dt> <dt>

[<span data-ttu-id="0d326-159">Table MsiDigitalCertificate</span><span class="sxs-lookup"><span data-stu-id="0d326-159">MsiDigitalCertificate table</span></span>](msidigitalcertificate-table.md)
</dt> <dt>

[<span data-ttu-id="0d326-160">Signatures numériques et Windows Installer</span><span class="sxs-lookup"><span data-stu-id="0d326-160">Digital Signatures and Windows Installer</span></span>](digital-signatures-and-windows-installer.md)
</dt> </dl>

 

 
