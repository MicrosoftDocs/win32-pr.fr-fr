---
description: ICE04 vérifie que le numéro de séquence de chaque fichier de la table de fichiers est inférieur ou égal au numéro de séquence le plus élevé dans la colonne LastSequence de la table des médias.
ms.assetid: ecde1389-50ea-479e-bbc1-a36ce3aceccd
title: ICE04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b77bf11d26d694a25f62db8da005139566b2c92310e2bb2dded4eecbca79719
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118635661"
---
# <a name="ice04"></a>ICE04

ICE04 vérifie que le numéro de séquence de chaque fichier de la [table de fichiers](file-table.md) est inférieur ou égal au numéro de séquence le plus élevé dans la colonne LastSequence de la [table des médias](media-table.md).

Chaque enregistrement de la table des médias représente un disque sur le support source contenant tous les fichiers dont le numéro de séquence est inférieur ou égal à la valeur de la colonne LastSequence et supérieur à la valeur LastSequence dans l’enregistrement du disque précédent.

## <a name="result"></a>Résultats

ICE04 publie un message d’erreur s’il existe un fichier avec un numéro de séquence supérieur au plus grand numéro de LastSequence du support source.

## <a name="example"></a>Exemple

ICE04 signale l’erreur suivante pour l’exemple ci-dessous :

``` syntax
File: MyFile, Sequence: 210 Greater Than Max Allowed by Media Table.
```

[Table de fichiers](file-table.md) (partielle)



| Fichier   | Séquence |
|--------|----------|
| Monfichier | 210      |



 

[Table des médias](media-table.md) (partielle)



| DiskId | LastSequence |
|--------|--------------|
| 1      | 100          |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE](ice-reference.md)
</dt> </dl>

 

 



