---
description: La table MsiDigitalCertificate stocke les certificats dans un format de flux binaire et associe chaque certificat à une clé primaire.
ms.assetid: 834534b8-540a-48c2-8eb0-3511d5a20cb4
title: Table MsiDigitalCertificate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff4765dee433cfab989e79c7ef4663d8939381ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755413"
---
# <a name="msidigitalcertificate-table"></a><span data-ttu-id="f20fb-103">Table MsiDigitalCertificate</span><span class="sxs-lookup"><span data-stu-id="f20fb-103">MsiDigitalCertificate Table</span></span>

<span data-ttu-id="f20fb-104">La table MsiDigitalCertificate stocke les certificats dans un format de flux binaire et associe chaque certificat à une clé primaire.</span><span class="sxs-lookup"><span data-stu-id="f20fb-104">The MsiDigitalCertificate table stores certificates in binary stream format and associates each certificate with a primary key.</span></span> <span data-ttu-id="f20fb-105">La clé primaire est utilisée pour partager des certificats entre plusieurs objets signés numériquement.</span><span class="sxs-lookup"><span data-stu-id="f20fb-105">The primary key is used to share certificates among multiple digitally signed objects.</span></span> <span data-ttu-id="f20fb-106">Un certificat numérique est une information d’identification qui fournit un moyen de vérifier l’identité.</span><span class="sxs-lookup"><span data-stu-id="f20fb-106">A digital certificate is a credential that provides a means to verify identity.</span></span> <span data-ttu-id="f20fb-107">Pour plus d’informations, consultez [certificats numériques](../seccrypto/digital-certificates.md) dans la section [chiffrement](../seccrypto/cryptography-portal.md) du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="f20fb-107">For more information, see [Digital Certificates](../seccrypto/digital-certificates.md) in the [Cryptography](../seccrypto/cryptography-portal.md) section of the Microsoft Windows Software Development Kit (SDK).</span></span>

<span data-ttu-id="f20fb-108">Les tables [MsiDigitalSignature](msidigitalsignature-table.md) et MsiDigitalCertificate sont disponibles à partir de Windows Installer version 2,0.</span><span class="sxs-lookup"><span data-stu-id="f20fb-108">The [MsiDigitalSignature](msidigitalsignature-table.md) and MsiDigitalCertificate tables are available starting with Windows Installer version 2.0.</span></span>

<span data-ttu-id="f20fb-109">Windows Installer pouvez utiliser des signatures numériques pour détecter les ressources endommagées.</span><span class="sxs-lookup"><span data-stu-id="f20fb-109">Windows Installer can use digital signatures as a means to detect corrupted resources.</span></span> <span data-ttu-id="f20fb-110">Windows Installer version 2,0 peut uniquement vérifier les signatures numériques des armoires externes, et uniquement à l’aide des tables [MsiDigitalSignature](msidigitalsignature-table.md) et MsiDigitalCertificate.</span><span class="sxs-lookup"><span data-stu-id="f20fb-110">Windows Installer version 2.0 can only verify the digital signatures of external cabinets, and only by the use of the [MsiDigitalSignature](msidigitalsignature-table.md) and MsiDigitalCertificate tables.</span></span>

<span data-ttu-id="f20fb-111">À partir de Windows Installer version 3,0, les Windows Installer peuvent vérifier les signatures numériques des correctifs (fichiers. msp) à l’aide des tables [MsiPatchCertificate](msipatchcertificate-table.md) et MsiDigitalCertificate.</span><span class="sxs-lookup"><span data-stu-id="f20fb-111">Beginning with Windows Installer version 3.0, the Windows Installer can verify the digital signatures of patches (.msp files) by using the [MsiPatchCertificate](msipatchcertificate-table.md) and MsiDigitalCertificate tables.</span></span> <span data-ttu-id="f20fb-112">Pour plus d’informations, consultez Instructions pour la création d’une mise à [jour corrective](user-account-control--uac--patching.md)des [installations sécurisées et du contrôle de compte d'](guidelines-for-authoring-secure-installations.md) utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f20fb-112">For more information, see [Guidelines for Authoring Secure Installations](guidelines-for-authoring-secure-installations.md) and [User Account Control (UAC) Patching](user-account-control--uac--patching.md).</span></span>

<span data-ttu-id="f20fb-113">La table MsiDigitalCertificate contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="f20fb-113">The MsiDigitalCertificate table has the following columns.</span></span>



| <span data-ttu-id="f20fb-114">Colonne</span><span class="sxs-lookup"><span data-stu-id="f20fb-114">Column</span></span>             | <span data-ttu-id="f20fb-115">Type</span><span class="sxs-lookup"><span data-stu-id="f20fb-115">Type</span></span>                         | <span data-ttu-id="f20fb-116">Clé</span><span class="sxs-lookup"><span data-stu-id="f20fb-116">Key</span></span> | <span data-ttu-id="f20fb-117">Nullable</span><span class="sxs-lookup"><span data-stu-id="f20fb-117">Nullable</span></span> |
|--------------------|------------------------------|-----|----------|
| <span data-ttu-id="f20fb-118">DigitalCertificate</span><span class="sxs-lookup"><span data-stu-id="f20fb-118">DigitalCertificate</span></span> | [<span data-ttu-id="f20fb-119">Identificateur</span><span class="sxs-lookup"><span data-stu-id="f20fb-119">Identifier</span></span>](identifier.md) | <span data-ttu-id="f20fb-120">O</span><span class="sxs-lookup"><span data-stu-id="f20fb-120">Y</span></span>   | <span data-ttu-id="f20fb-121">N</span><span class="sxs-lookup"><span data-stu-id="f20fb-121">N</span></span>        |
| <span data-ttu-id="f20fb-122">CertData</span><span class="sxs-lookup"><span data-stu-id="f20fb-122">CertData</span></span>           | [<span data-ttu-id="f20fb-123">Binaire</span><span class="sxs-lookup"><span data-stu-id="f20fb-123">Binary</span></span>](binary.md)         | <span data-ttu-id="f20fb-124">N</span><span class="sxs-lookup"><span data-stu-id="f20fb-124">N</span></span>   | <span data-ttu-id="f20fb-125">N</span><span class="sxs-lookup"><span data-stu-id="f20fb-125">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="f20fb-126">Colonnes</span><span class="sxs-lookup"><span data-stu-id="f20fb-126">Columns</span></span>

<dl> <dt>

<span data-ttu-id="f20fb-127"><span id="DigitalCertificate"></span><span id="digitalcertificate"></span><span id="DIGITALCERTIFICATE"></span>DigitalCertificate</span><span class="sxs-lookup"><span data-stu-id="f20fb-127"><span id="DigitalCertificate"></span><span id="digitalcertificate"></span><span id="DIGITALCERTIFICATE"></span>DigitalCertificate</span></span>
</dt> <dd>

<span data-ttu-id="f20fb-128">Identifie le certificat de signature numérique.</span><span class="sxs-lookup"><span data-stu-id="f20fb-128">Identifies the digital signature certificate.</span></span> <span data-ttu-id="f20fb-129">Clé primaire de la table.</span><span class="sxs-lookup"><span data-stu-id="f20fb-129">Primary key of table.</span></span>

</dd> <dt>

<span data-ttu-id="f20fb-130"><span id="CertData"></span><span id="certdata"></span><span id="CERTDATA"></span>CertData</span><span class="sxs-lookup"><span data-stu-id="f20fb-130"><span id="CertData"></span><span id="certdata"></span><span id="CERTDATA"></span>CertData</span></span>
</dt> <dd>

<span data-ttu-id="f20fb-131">Représentation binaire du certificat numérique.</span><span class="sxs-lookup"><span data-stu-id="f20fb-131">The binary representation of the digital certificate.</span></span> <span data-ttu-id="f20fb-132">La colonne CertData contient le tableau d’octets encodé d’un contexte de certificat.</span><span class="sxs-lookup"><span data-stu-id="f20fb-132">The CertData column contains the encoded byte array of a certificate context.</span></span> <span data-ttu-id="f20fb-133">Il s’agit du membre **pbCertEncoded** de la structure de [**\_ contexte du certificat**](/windows/win32/api/wincrypt/ns-wincrypt-cert_context) .</span><span class="sxs-lookup"><span data-stu-id="f20fb-133">This is the **pbCertEncoded** member of the [**CERT\_CONTEXT**](/windows/win32/api/wincrypt/ns-wincrypt-cert_context) structure.</span></span> <span data-ttu-id="f20fb-134">Le contexte de certificat peut être obtenu en appelant [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust), [**MsiGetFileSignatureInformation**](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa)ou en important un fichier. cer.</span><span class="sxs-lookup"><span data-stu-id="f20fb-134">The certificate context can be obtained by calling [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust), [**MsiGetFileSignatureInformation**](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa), or by importing a .cer file.</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="f20fb-135">Validation</span><span class="sxs-lookup"><span data-stu-id="f20fb-135">Validation</span></span>

<dl>

[<span data-ttu-id="f20fb-136">ICE03</span><span class="sxs-lookup"><span data-stu-id="f20fb-136">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="f20fb-137">ICE06</span><span class="sxs-lookup"><span data-stu-id="f20fb-137">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="f20fb-138">ICE29</span><span class="sxs-lookup"><span data-stu-id="f20fb-138">ICE29</span></span>](ice29.md)  
[<span data-ttu-id="f20fb-139">ICE32</span><span class="sxs-lookup"><span data-stu-id="f20fb-139">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="f20fb-140">ICE66</span><span class="sxs-lookup"><span data-stu-id="f20fb-140">ICE66</span></span>](ice66.md)  
[<span data-ttu-id="f20fb-141">ICE81</span><span class="sxs-lookup"><span data-stu-id="f20fb-141">ICE81</span></span>](ice81.md)  
</dl>

## <a name="related-topics"></a><span data-ttu-id="f20fb-142">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f20fb-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f20fb-143">**MsiGetFileSignatureInformation**</span><span class="sxs-lookup"><span data-stu-id="f20fb-143">**MsiGetFileSignatureInformation**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa)
</dt> <dt>

[<span data-ttu-id="f20fb-144">Table MsiDigitalSignature</span><span class="sxs-lookup"><span data-stu-id="f20fb-144">MsiDigitalSignature table</span></span>](msidigitalsignature-table.md)
</dt> <dt>

[<span data-ttu-id="f20fb-145">Signatures numériques et Windows Installer</span><span class="sxs-lookup"><span data-stu-id="f20fb-145">Digital Signatures and Windows Installer</span></span>](digital-signatures-and-windows-installer.md)
</dt> </dl>

 

 
