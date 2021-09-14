---
description: ICE76 vérifie l’utilisation du catalogue SFP (WFP) au sein des packages Windows Installer pour Windows Me. Cette ICE vérifie également qu’aucun fichier de la table BindImage ne fait référence aux catalogues SFP.
ms.assetid: e8b60b11-19ac-4ec4-aa36-a1f7a3ccd6f6
title: ICE76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5beb0157053e9bd3e4bf0d896f52af04a511ac24
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021487"
---
# <a name="ice76"></a>ICE76

ICE76 vérifie l’utilisation du catalogue SFP (WFP) au sein des packages Windows Installer pour Windows Me. Cette ICE vérifie également qu’aucun fichier de la [table](bindimage-table.md) BindImage ne fait référence aux catalogues SFP.

Windows La protection des fichiers nécessite une correspondance exacte entre le fichier et la signature incorporée dans le fichier catalogue. Les fichiers qui font référence à un catalogue SFP ne doivent pas figurer dans la table BindImage, car l’effet de l' [action BindImage](bindimage-action.md) sur ces fichiers diffère entre les ordinateurs. Les fichiers référencés par les catalogues SFP doivent se trouver dans des composants permanents ou installés localement.

## <a name="result"></a>Résultats

ICE76 publie une erreur pour chaque fichier de la [table BindImage](bindimage-table.md) qui se trouve également dans la [table FileSFPCatalog](filesfpcatalog-table.md).

ICE76 génère une erreur si un fichier de la table FileSFPCatalog appartient à un composant avec l’une des valeurs suivantes :

-   **msidbComponentAttributesPermanent** n’est pas défini dans la colonne attributs de la [table des composants](component-table.md).
-   **msidbComponentAttributesSourceOnly** est défini dans la colonne attributs de la table des composants.
-   **msidbAttributesOptional** est défini dans la colonne attributs de la table des composants.

## <a name="example"></a>Exemple

ICE76 signale l’erreur suivante pour l’exemple :

``` syntax
File 'File1' references a SFP catalog. Therefore it cannot be in the BindImage table.
```

[Table FileSFPCatalog](filesfpcatalog-table.md) (partielle)



| fichier\_ | SFPCatalog\_ |
|--------|--------------|
| Fichier1  | Catalog1.Cat |



 

[Table BindImage](bindimage-table.md) (partielle)



| fichier\_ |
|--------|
| Fichier1  |



 

Pour résoudre ce problème, n’entrez aucun fichier référençant les catalogues SFP dans la table BindImage.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Table BindImage](bindimage-table.md)
</dt> <dt>

[Table des composants](component-table.md)
</dt> <dt>

[Table FileSFPCatalog](filesfpcatalog-table.md)
</dt> <dt>

[Référence ICE](ice-reference.md)
</dt> </dl>

 

 



