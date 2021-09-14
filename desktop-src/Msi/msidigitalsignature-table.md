---
description: La table MsiDigitalSignature contient les informations de signature pour chaque objet signé numériquement dans la base de données d’installation.
ms.assetid: 63d62152-4f01-454f-bdea-550f2a9f6b14
title: Table MsiDigitalSignature
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd0ec22b9a399b6248fd3b2781e1ac8d7ae14324
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011869"
---
# <a name="msidigitalsignature-table"></a>Table MsiDigitalSignature

La table MsiDigitalSignature contient les informations de signature pour chaque objet signé numériquement dans la base de données d’installation.

les tables MsiDigitalSignature et [MsiDigitalCertificate](msidigitalcertificate-table.md) sont disponibles à partir de Windows Installer version 2,0.

Windows La version du programme d’installation peut utiliser des signatures numériques pour détecter les ressources endommagées. Windows Le programme d’installation 2,0 peut uniquement vérifier les signatures numériques des armoires externes, et uniquement à l’aide des tables MsiDigitalSignature et [MsiDigitalCertificate](msidigitalcertificate-table.md) .

à partir de Windows Installer 3,0, le Windows Installer peut vérifier les signatures numériques des correctifs (fichiers. msp) à l’aide des tables [MsiPatchCertificate](msipatchcertificate-table.md) et MsiDigitalCertificate. Pour plus d’informations, consultez Instructions pour la création d’une mise à [jour corrective](user-account-control--uac--patching.md)des [installations sécurisées et du contrôle de compte d'](guidelines-for-authoring-secure-installations.md) utilisateur.

La table MsiDigitalSignature contient les colonnes suivantes.



| Colonne               | Type                         | Clé : | Nullable |
|----------------------|------------------------------|-----|----------|
| Table de charge de travail                | [Identificateur](identifier.md) | O   | N        |
| SignObject           | [Text](text.md)             | O   | N        |
| DigitalCertificate\_ | [Identificateur](identifier.md) | N   | N        |
| Hachage                 | [Binaire](binary.md)         | N   | O        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="Table"></span><span id="table"></span><span id="TABLE"></span>Tableau
</dt> <dd>

avec la version de Windows Installer 2,0, l’entrée de ce champ doit être « Media » pour la [table media](media-table.md). Le programme d’installation vérifie uniquement les signatures numériques sur les entrées de média du fichier CAB externe. Cette colonne et la colonne SignObject spécifient ensemble la ressource signée numériquement.

</dd> <dt>

<span id="SignObject"></span><span id="signobject"></span><span id="SIGNOBJECT"></span>SignObject
</dt> <dd>

Clé étrangère dans la clé primaire de la table spécifiée par la colonne de table. Cette colonne et la colonne de table spécifient ensemble la ressource signée numériquement.

</dd> <dt>

<span id="DigitalCertificate_"></span><span id="digitalcertificate_"></span><span id="DIGITALCERTIFICATE_"></span>DigitalCertificate\_
</dt> <dd>

Clé étrangère dans la [table MsiDigitalCertificate](msidigitalcertificate-table.md). Cela identifie le certificat qui doit exister dans le fichier pour que l’action associée aboutisse. La ressource (ou l’objet) est toujours nécessaire pour correspondre à ce certificat dans la table MsiDigitalCertificate.

</dd> <dt>

<span id="Hash"></span><span id="hash"></span><span id="HASH"></span>Format
</dt> <dd>

Dans ce champ, entrez le hachage de référence de la ressource (ou objet) qui doit être vérifiée par rapport au hachage réel de la ressource (ou objet) obtenue au moment de l’exécution. Si seul le certificat doit être vérifié, le champ Hash peut avoir la valeur null. Notez que le format du hachage dépend du type de la ressource (ou de l’objet) en cours de signature.

La colonne Hash contient la représentation binaire du hachage. Le contenu réel est le membre **pbData** de la structure de l' [**\_ \_ objet blob de hachage énigmatique**](/windows/win32/api/dpapi/ns-dpapi-crypt_integer_blob) , qui fait partie de la structure de l' **\_ objet BLOB CryptoAPI** . Cela peut être obtenu en appelant [WinVerifyTrust](/windows/win32/api/wintrust/nf-wintrust-winverifytrust) ou [**MsiGetFileSignatureInformation**](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa).

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

[Table MsiDigitalCertificate](msidigitalcertificate-table.md)
</dt> <dt>

[Signatures numériques et Windows Installer](digital-signatures-and-windows-installer.md)
</dt> </dl>

 

 
