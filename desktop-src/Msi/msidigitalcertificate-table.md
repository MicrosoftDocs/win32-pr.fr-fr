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
# <a name="msidigitalcertificate-table"></a>Table MsiDigitalCertificate

La table MsiDigitalCertificate stocke les certificats dans un format de flux binaire et associe chaque certificat à une clé primaire. La clé primaire est utilisée pour partager des certificats entre plusieurs objets signés numériquement. Un certificat numérique est une information d’identification qui fournit un moyen de vérifier l’identité. Pour plus d’informations, consultez [certificats numériques](../seccrypto/digital-certificates.md) dans la section [chiffrement](../seccrypto/cryptography-portal.md) du kit de développement logiciel (SDK) Microsoft Windows.

Les tables [MsiDigitalSignature](msidigitalsignature-table.md) et MsiDigitalCertificate sont disponibles à partir de Windows Installer version 2,0.

Windows Installer pouvez utiliser des signatures numériques pour détecter les ressources endommagées. Windows Installer version 2,0 peut uniquement vérifier les signatures numériques des armoires externes, et uniquement à l’aide des tables [MsiDigitalSignature](msidigitalsignature-table.md) et MsiDigitalCertificate.

À partir de Windows Installer version 3,0, les Windows Installer peuvent vérifier les signatures numériques des correctifs (fichiers. msp) à l’aide des tables [MsiPatchCertificate](msipatchcertificate-table.md) et MsiDigitalCertificate. Pour plus d’informations, consultez Instructions pour la création d’une mise à [jour corrective](user-account-control--uac--patching.md)des [installations sécurisées et du contrôle de compte d'](guidelines-for-authoring-secure-installations.md) utilisateur.

La table MsiDigitalCertificate contient les colonnes suivantes.



| Colonne             | Type                         | Clé | Nullable |
|--------------------|------------------------------|-----|----------|
| DigitalCertificate | [Identificateur](identifier.md) | O   | N        |
| CertData           | [Binaire](binary.md)         | N   | N        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="DigitalCertificate"></span><span id="digitalcertificate"></span><span id="DIGITALCERTIFICATE"></span>DigitalCertificate
</dt> <dd>

Identifie le certificat de signature numérique. Clé primaire de la table.

</dd> <dt>

<span id="CertData"></span><span id="certdata"></span><span id="CERTDATA"></span>CertData
</dt> <dd>

Représentation binaire du certificat numérique. La colonne CertData contient le tableau d’octets encodé d’un contexte de certificat. Il s’agit du membre **pbCertEncoded** de la structure de [**\_ contexte du certificat**](/windows/win32/api/wincrypt/ns-wincrypt-cert_context) . Le contexte de certificat peut être obtenu en appelant [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust), [**MsiGetFileSignatureInformation**](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa)ou en important un fichier. cer.

</dd> </dl>

## <a name="validation"></a>Validation

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE29](ice29.md)  
[ICE32](ice32.md)  
[ICE66](ice66.md)  
[ICE81](ice81.md)  
</dl>

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**MsiGetFileSignatureInformation**](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa)
</dt> <dt>

[Table MsiDigitalSignature](msidigitalsignature-table.md)
</dt> <dt>

[Signatures numériques et Windows Installer](digital-signatures-and-windows-installer.md)
</dt> </dl>

 

 
