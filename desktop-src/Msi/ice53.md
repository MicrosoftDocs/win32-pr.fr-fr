---
description: ICE53 recherche des entrées dans la table de Registre qui écrivent des informations de stratégie d’installation privées ou des valeurs de stratégie dans le registre système.
ms.assetid: f5afca1f-bd36-4f95-a62a-f6b2e37238a6
title: ICE53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a2d1e661eb832439a9b4fde423e005dc4b3a0c3ca9b266045c0ddd04daa63f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118635130"
---
# <a name="ice53"></a>ICE53

ICE53 recherche des entrées dans la table de Registre qui écrivent des informations de stratégie d’installation privées ou des valeurs de stratégie dans le registre système.

## <a name="result"></a>Résultat

ICE53 publie un avertissement si la table du Registre spécifie l’écriture des informations internes ou de stratégie dans le registre.

## <a name="example"></a>Exemple

ICE53 publie l’avertissement suivant pour l’exemple indiqué.

``` syntax
Registry Key 'Registry1' writes Installer internal or policy information.
```

[Table du Registre](registry-table.md) (partielle)



| Registre             | Root         | Clé                                                                                                   |
|----------------------|--------------|-------------------------------------------------------------------------------------------------------|
| Registry1<br/> | 1<br/> | **Logiciel** \\ **Stratégies** \\ **Microsoft** \\ **Windows** \\ **Programme d’installation** \\ **DisableRollback**<br/> |



 

La ligne de la table de Registre « Registry1 » écrit une valeur de stratégie système dans le Registre qui affecte l’installation de tous les packages. Selon le package, il peut être possible de désactiver la restauration pour ce package seul en définissant la propriété [**disablerollback**](-disablerollback.md) dans la [table de propriétés](property-table.md). Consultez [restauration de l’installation](rollback-installation.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE](ice-reference.md)
</dt> </dl>

 

 




