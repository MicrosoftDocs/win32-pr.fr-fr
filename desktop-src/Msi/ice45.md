---
description: ICE45 valide que les colonnes de champ de bits dans la base de données ne définissent pas de bits réservés sur 1.
ms.assetid: 43fa5e9c-2059-4217-8f8e-c194e37f238a
title: ICE45
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0651d94c296ae14f66b562841c3c4e2bca7b8e32
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021553"
---
# <a name="ice45"></a>ICE45

ICE45 valide que les colonnes de champ de bits dans la base de données ne définissent pas de bits réservés sur 1.

Les bits réservés ne fournissent aucune fonctionnalité dans les versions actuelles du programme d’installation, mais peuvent l’être dans les versions ultérieures. ils doivent avoir la valeur 0 pour être compatibles avec les futures versions de Windows Installer.

## <a name="result"></a>Résultats

ICE45 publie un message d’erreur si l’une des tables suivantes contient un champ de bits avec un bit réservé défini sur la valeur 1.

-   [Table BBControl](bbcontrol-table.md)
-   [Table de boîtes de dialogue](dialog-table.md)
-   [Tableau des fonctionnalités](feature-table.md)
-   [Table de fichiers](file-table.md)
-   [Table MoveFile](movefile-table.md)
-   [Table ModuleConfiguration](moduleconfiguration-table.md)
-   [Table ODBCDataSource](odbcdatasource-table.md)
-   [Table des correctifs](patch-table.md)
-   [Table RemoveFile](removefile-table.md)
-   [Table ServiceControl](servicecontrol-table.md)
-   [Table ServiceInstall](serviceinstall-table.md)
-   [Table TextStyle](textstyle-table.md)

ICE45 publie l’un des deux messages d’avertissement si la [table de contrôle](control-table.md) contient un champ de bits avec un bit réservé défini sur la valeur 1.

## <a name="example"></a>Exemple

ICE45 signale l’erreur suivante pour l’exemple indiqué.

``` syntax
Row 'File1' in table 'File' has bits set in the 'Attributes' 
    column that are reserved. They must be 0 to ensure 
    compatibility with future installer versions.
```

ICE45 signale l’avertissement suivant pour l’exemple indiqué.

``` syntax
Row 'Dialog1.Edit2' in table 'Control' has bits set in the 'Attribute' 
    column that are reserved. They should be 0 to ensure compatibility 
    with future installer versions.
```

[Table de fichiers](file-table.md) (partielle)



| Fichier  | Attributs |
|-------|------------|
| Fichier1 | 128        |



 

[Table de contrôle](control-table.md) (partielle)



| Boîte de dialogue  | Control | Attributs |
|---------|---------|------------|
| Dialog1 | Edit1   | 2 097 152    |
| Dialog1 | Edit2   | 1 048 576    |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE](ice-reference.md)
</dt> </dl>

 

 



