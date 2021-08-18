---
description: La \_ table UpgradedFile OptionalData contient des informations sur des fichiers spécifiques d’une image mise à niveau. Cette table est facultative dans la base de données de création de correctifs (fichier. PCP) et est utilisée par la fonction UiCreatePatchPackageEx.
ms.assetid: 8b96a83a-2bfa-47b7-bde0-896bdcc97d29
title: Table UpgradedFiles_OptionalData (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08eb766f8db9d295546670c80627284991da1ff8dccb5a0c2900be74bd785dab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012837"
---
# <a name="upgradedfiles_optionaldata-table-patchwizdll"></a>UpgradedFiles \_ OptionalData, table (Patchwiz.dll)

La \_ table UpgradedFile OptionalData contient des informations sur des fichiers spécifiques d’une image mise à niveau. Cette table est facultative dans la base de données de création de correctifs (fichier. PCP) et est utilisée par la fonction [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) .

La \_ table UpgradedFile OptionalData contient les colonnes suivantes.



| Colonne                  | Type    | Clé | Nullable |
|-------------------------|---------|-----|----------|
| Upgraded                | text    | O   | N        |
| TCTI                     | text    | O   | N        |
| SymbolPaths             | text    |     | O        |
| AllowIgnoreOnPatchError | entier |     | O        |
| IncludeWholeFile        | entier |     | O        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="Upgraded"></span><span id="upgraded"></span><span id="UPGRADED"></span>Mis à niveau
</dt> <dd>

Clé étrangère vers la colonne mise à niveau de la [table UpgradedImages (Patchwiz.dll)](upgradedimages-table-patchwiz-dll-.md).

</dd> <dt>

<span id="FTK"></span><span id="ftk"></span>TCTI
</dt> <dd>

Clé de table de fichiers. Clé étrangère dans la [table de fichiers](file-table.md) du fichier .msi de l’image mise à niveau. Si au moins deux images mises à niveau dans une famille ont la même valeur TCTI, la valeur doit faire référence au même fichier. Les fichiers partagés par plusieurs images de mise à niveau doivent avoir le même TCTI pour réduire la taille du fichier CAB.

</dd> <dt>

<span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths
</dt> <dd>

La valeur de ce champ est ajoutée à la liste de dossiers délimités par des points-virgules dans la colonne SymbolPaths de la [table UpgradedImages (Patchwiz.dll)](upgradedimages-table-patchwiz-dll-.md) lorsque le correctif est généré et peut être utilisé pour ajouter des fichiers de symboles pour un fichier spécifique.

</dd> <dt>

<span id="AllowIgnoreOnPatchError"></span><span id="allowignoreonpatcherror"></span><span id="ALLOWIGNOREONPATCHERROR"></span>AllowIgnoreOnPatchError
</dt> <dd>

Affectez la valeur 1 pour indiquer que le correctif logiciel n’est pas vital. Attribuez la valeur 0 pour indiquer que le correctif est vital. si Windows Installer rencontre un problème lors de l’application de ce correctif au fichier spécifié dans la colonne tcti, la valeur de ce champ détermine si la boîte de message d’erreur contient un bouton **ignorer** pour permettre à l’utilisateur de poursuivre le processus de mise à jour corrective.

</dd> <dt>

<span id="IncludeWholeFile"></span><span id="includewholefile"></span><span id="INCLUDEWHOLEFILE"></span>IncludeWholeFile
</dt> <dd>

Affectez une valeur différente de zéro si l’intégralité du fichier spécifié dans la colonne TCTI doit être installée au lieu de créer un correctif binaire.

</dd> </dl>

 

 



