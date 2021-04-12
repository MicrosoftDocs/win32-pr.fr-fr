---
description: COM+ offre aux développeurs plus de contrôle sur leurs applications en autorisant des niveaux d’isolation des transactions configurables.
ms.assetid: a59e262c-41f2-4c80-a04c-50a39af8b009
title: Configuration des niveaux d’isolation des transactions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36d789b9eaed6dfdd2f2419c7eae391d628e75b4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483056"
---
# <a name="configuring-transaction-isolation-levels"></a>Configuration des niveaux d’isolation des transactions

COM+ offre aux développeurs plus de contrôle sur leurs applications en autorisant des niveaux d’isolation des transactions configurables. Les versions de COM+ antérieures à COM+ 1,5 utilisaient toujours le niveau d’isolation le plus élevé pour les transactions. Bien que ce niveau garantisse que l’intégrité des données soit toujours préservée, cela peut entraîner des problèmes de performances, tels que des délais d’attente, lorsque de nombreuses transactions doivent être exécutées sur une base de données volumineuse. Avec des niveaux d’isolation configurables, les développeurs expérimentés peuvent augmenter la concurrence pour améliorer les performances et l’extensibilité.

COM+ fournit les niveaux d’isolation des transactions suivants.



| Level            | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| de données       | Les données lues par une transaction en cours ne peuvent pas être modifiées par une autre transaction jusqu’à ce que la transaction en cours se termine. Aucune nouvelle donnée ne peut être insérée qui affecterait la transaction en cours. Il s’agit du niveau d’isolement le plus sûr. il s’agit de la valeur par défaut.                                                                                                                                                                                                                                                                                                                                                    |
| Lecture renouvelable  | Les données lues par une transaction en cours ne peuvent pas être modifiées par une autre transaction jusqu’à ce que la transaction en cours se termine. Tous les types de nouvelles données peuvent être insérés au cours d’une transaction.                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Lecture validée   | Une transaction ne peut pas lire les données qui sont modifiées par une autre transaction qui n’a pas été validée. Il s’agit du niveau d’isolement par défaut dans Microsoft SQL Server.                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Lecture non validée | Une transaction peut lire toutes les données, même si elles sont modifiées par une autre transaction. Il s’agit du niveau d’isolation le moins sûr, mais autorise la concurrence la plus élevée.                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Quelconque              | Tout niveau d’isolement est pris en charge. Ce paramètre est généralement utilisé par les composants en aval pour éviter les conflits. Ce paramètre est utile, car tout composant en aval doit être configuré avec un niveau d’isolement inférieur ou égal au niveau d’isolation de son composant en amont immédiat. Par conséquent, un composant en aval qui a son niveau d’isolation configuré comme n’importe lequel utilise toujours le même niveau d’isolation que celui utilisé par son composant en amont immédiat. Si le niveau d’isolation de l’objet racine d’une transaction est configuré sur any, son niveau d’isolation est sérialisé. |



 

> [!Note]  
> Si un composant en aval est configuré avec un niveau d’isolation supérieur à celui d’un composant en amont et tente de s’inscrire dans une transaction, une erreur se produit et la transaction est abandonnée.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Définition du niveau d’isolation des transactions](setting-the-transaction-isolation-level.md)
</dt> </dl>

 

 



