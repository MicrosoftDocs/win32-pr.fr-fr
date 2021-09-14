---
description: Le tableau MsiPackageCertificate répertorie les certificats de signature numérique utilisés pour vérifier l’identité des packages d’installation qui effectuent cette installation Multiple-Package.
ms.assetid: d3a97325-2136-4745-8a7d-57e4d6b9d27e
title: Table MsiPackageCertificate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fd39ac93ff24da2fa8334a6e4865172471080b4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127119749"
---
# <a name="msipackagecertificate-table"></a>Table MsiPackageCertificate

Le tableau MsiPackageCertificate répertorie les certificats de signature numérique utilisés pour vérifier l’identité des packages d’installation qui effectuent cette [installation de plusieurs packages](multiple-package-installations.md).

utilisez ce tableau pour créer une [installation de plusieurs](multiple-package-installations.md) packages pour un produit contenant plusieurs packages de Windows Installer. Si le premier package est signé numériquement et contient une table MsiPackageCertificate spécifiant des certificats numériques pour tous les packages restants dans le produit, l’administrateur doit uniquement accepter l’invite de [*contrôle de compte d’utilisateur*](u-gly.md) (UAC) affichée pour le premier package. Après avoir accepté l’invite du contrôle de compte d’utilisateur pour le premier package, les fonctions définies par l’utilisateur dans la [table MsiEmbeddedChainer](msiembeddedchainer-table.md) peuvent ensuite joindre les packages restants à l’installation de plusieurs packages sans afficher d’invite UAC et exiger une réponse de l’administrateur pour chaque package.

Si une ou plusieurs des fonctions de la [table MsiEmbeddedChainer](msiembeddedchainer-table.md) demandent un package non signé, une autre invite UAC demandant l’intervention de l’administrateur s’affiche pour chaque package non signé. Si l’administrateur accepte cette invite de contrôle de compte d’utilisateur, l’installation de plusieurs packages se poursuit. Une fois qu’un administrateur a fourni les informations d’identification d’un package, aucune invite UAC ne s’affiche à nouveau pour ce package lors de l’installation de plusieurs packages. si l’administrateur rejette une invite de contrôle de compte d’utilisateur pour un package, le programme d’installation de Windows restaure l’installation de plusieurs packages avant de valider l’installation des packages appartenant au produit.

**[Windows Installer 4,0 ou version antérieure](not-supported-in-windows-installer-4-0.md):** Non pris en charge. cette table est disponible à partir de Windows Installer 4,5.

La table MsiPackageCertificate contient les colonnes suivantes :



| Colonne               | Type                         | Clé | Nullable |
|----------------------|------------------------------|-----|----------|
| PackageCertificate   | [Identificateur](identifier.md) | O   | N        |
| DigitalCertificate\_ | [Identificateur](identifier.md) | N   | N        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="PackageCertificate"></span><span id="packagecertificate"></span><span id="PACKAGECERTIFICATE"></span>PackageCertificate
</dt> <dd>

Identificateur unique de cette ligne dans la table MsiPackageCertificate.

</dd> <dt>

<span id="DigitalCertificate"></span><span id="digitalcertificate"></span><span id="DIGITALCERTIFICATE"></span>DigitalCertificate
</dt> <dd>

Une clé externe dans la première colonne de la [table MsiDigitalCertificate](msidigitalcertificate-table.md). La ligne indiquée dans la table MsiDigitalCertificate contient la représentation binaire du certificat du signataire.

</dd> </dl>

## <a name="validation"></a>Validation

<dl>

[ICE39](ice39.md)  
[ICE81](ice81.md)  
</dl>

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[MsiEmbeddedChainer](msiembeddedchainer-table.md)
</dt> <dt>

[Table MsiDigitalCertificate](msidigitalcertificate-table.md)
</dt> </dl>

 

 



