---
description: La liste suivante fournit des liens vers chaque module de fusion ICE.
ms.assetid: 3b106a81-99b6-4ac6-95be-537fc14e0510
title: Référence ICE du module de fusion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df445ad214808edfa40a47f036436877f5c0ba34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518910"
---
# <a name="merge-module-ice-reference"></a>Référence ICE du module de fusion

La liste suivante fournit des liens vers chaque module de fusion ICE.



| ICEM                 | Brève description de la glace du module de fusion                                                                                                                                                                                                                    |
|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ICEM01](icem01.md) | Valide le fonctionnement du mécanisme ICE.                                                                                                                                                                                                             |
| [ICEM02](icem02.md) | Valide que toutes les exclusions et toutes les dépendances de module sont liées au module actuel.                                                                                                                                                                      |
| [ICEM03](icem03.md) | Valide que toutes les actions du module sont des actions de base ou qu’elles dérivent d’une action de base.                                                                                                                                                           |
| [ICEM04](icem04.md) | Vérifie que les tables vides requises du module de fusion sont effectivement vides.                                                                                                                                                                                 |
| [ICEM05](icem05.md) | Recherche les associations non valides avec les composants.                                                                                                                                                                                                         |
| [ICEM06](icem06.md) | Recherche des références non valides aux fonctionnalités par le module.                                                                                                                                                                                                 |
| [ICEM07](icem07.md) | Valide que l’ordre des fichiers dans les tables de séquence et dans [MergeModule.CABfichier inet](mergemodule-cabinet.md) correspond.                                                                                                                               |
| [ICEM08](icem08.md) | Garantit qu’un module n’exclut pas les éléments dont il dépend.                                                                                                                                                                                          |
| [ICEM09](icem09.md) | Vérifie que le module de fusion gère en toute sécurité les répertoires prédéfinis.                                                                                                                                                                                    |
| [ICEM10](icem10.md) | Vérifie qu’un module de fusion ne contient pas de propriétés non autorisées dans la [table de propriétés](property-table.md).                                                                                                                                         |
| [ICEM11](icem11.md) | Vérifie qu’un module de fusion configurable répertorie la [table ModuleConfiguration](moduleconfiguration-table.md) et la [table ModuleSubstitution](modulesubstitution-table.md) dans la [table ModuleIgnoreTable](moduleignoretable-table.md) du module. |
| [ICEM12](icem12.md) | Vérifie que dans une table ModuleSequence, les actions standard ont des numéros de séquence et les actions personnalisées ont des valeurs BaseAction et after.                                                                                                                     |
| [ICEM13](icem13.md) | Vérifie que les assemblys de stratégie et de configuration de l’éditeur ne sont pas inclus dans le module de fusion.                                                                                                                                                        |
| [ICEM14](icem14.md) | Valide la colonne de valeur de la [table ModuleSubstitution](modulesubstitution-table.md).                                                                                                                                                              |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Validation des modules de fusion](validating-merge-modules.md)
</dt> </dl>

 

 



