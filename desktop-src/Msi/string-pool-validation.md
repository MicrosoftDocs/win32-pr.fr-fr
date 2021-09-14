---
description: l’Windows Installer stocke toutes les chaînes de base de données dans un seul pool de chaînes partagé pour réduire la taille de la base de données et améliorer les performances.
ms.assetid: b627f3da-3545-4c1a-85b0-d8845fdac621
title: Validation de la String-Pool
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecb544b5c76026846f7e8b8f6f331195426ab55c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127223148"
---
# <a name="string-pool-validation"></a>Validation de la String-Pool

l’Windows Installer stocke toutes les chaînes de base de données dans un seul pool de chaînes partagé pour réduire la taille de la base de données et améliorer les performances. le seul moyen de valider le pool de chaînes consiste à utiliser l’outil MsiInfo disponible dans le kit de développement logiciel (SDK) Windows Installer.

La vérification du pool de chaînes se compose de deux vérifications principales :

-   [Tests de chaîne DBCS](#dbcs-string-tests)
-   [Vérification du nombre de références](#reference-count-verification)

## <a name="dbcs-string-tests"></a>Tests de chaîne DBCS

Les tests de chaîne DBCS analysent chaque chaîne dans la base de données à la recherche de deux critères : pour les packages avec une page de codes neutre marquée, si un caractère est un caractère étendu (supérieur à 127), la chaîne est marquée et un message indiquant que la page de codes de la base de données n’est pas valide, car ces caractères requièrent une page de codes spécifique pour être

Si la base de données comporte une page de codes, chaque chaîne est analysée pour rechercher un indicateur DBCS non valide. Si une chaîne non neutre n’a pas été correctement marquée, les caractères ne sont pas restitués correctement. (Cela est généralement dû au fait que la page de codes est forcée à une valeur particulière à l’aide de la \_ Table ForceCodepage avec des chaînes non neutres déjà présentes dans la base de données.) Notez que cette vérification requiert que la page de codes de la base de données soit installée sur le système.

En cas de problème de page de codes, l’utilisateur peut corriger l’erreur en utilisant la \_ table ForceCodepage pour forcer la page de codes de la base de données à la valeur appropriée. Pour plus d’informations, consultez [gestion des pages de codes](code-page-handling-windows-installer-.md).

## <a name="reference-count-verification"></a>Vérification du nombre de références

Pour vérifier le nombre de références de toutes les chaînes, chaque table est analysée pour rechercher les valeurs de chaîne, le nombre de chaque chaîne distincte est conservé et le résultat est comparé au décompte de références stocké dans le pool de chaînes de base de données.

En cas de problème de nombre de références de chaîne, l’utilisateur doit immédiatement exporter chaque table de la base de données à l’aide de [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta), créer une nouvelle base de données et importer les tables dans la nouvelle base de données à l’aide de [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta). La nouvelle base de données a ensuite le même contenu que l’ancienne, mais les nombres de références de chaîne sont corrects. L’ajout ou la suppression de données d’une base de données avec un pool de chaînes endommagé peut augmenter la corruption de la base de données et la perte de données. par conséquent, il est important de suivre ces étapes rapidement pour éviter toute perte de données.

lorsque vous reconstruisez des bases de données, n’oubliez pas d’incorporer les stockages et les flux nécessaires dans la nouvelle base de données (consultez tableau de [ \_ Flux table](-streams-table.md) et [ \_ stockage](-storages-table.md)) et tenez compte des problèmes de page de codes. N’oubliez pas également de définir chacune des propriétés de [flux d’informations de résumé](summary-information-stream.md) nécessaires.

 

 



