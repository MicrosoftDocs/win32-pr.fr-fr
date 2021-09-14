---
description: ICE14 valide la table des fonctionnalités d’une base de données Windows Installer.
ms.assetid: fb1970f8-1dba-4b06-aa03-5b33d213fc79
title: ICE14
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b2e64a6106ae359fe02c6ead271bbae267eeb18
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021613"
---
# <a name="ice14"></a>ICE14

ICE14 valide les éléments suivants pour les fonctionnalités :

-   Pour les fonctionnalités parentes racine, le bit msidbFeatureAttributesFollowParent n’est pas défini dans la colonne attributs du [tableau des fonctionnalités](feature-table.md). Une fonctionnalité racine n’a pas de parent.
-   Cette fonctionnalité n’a pas la même entrée dans les colonnes parentes Feature et Feature \_ de la [table Feature](feature-table.md). Aucune fonctionnalité ne peut être son propre parent.

## <a name="result"></a>Résultats

ICE14 publie un message d’erreur s’il trouve une fonctionnalité racine avec l’ensemble de bits msidbFeatureAttributesFollowParent ou une fonctionnalité avec des entrées identiques dans les \_ colonnes parentes de fonctionnalité et de fonctionnalité de la table des fonctionnalités.

## <a name="example"></a>Exemple

ICE14 retournerait les erreurs suivantes pour l’exemple suivant :

-   La fonctionnalité sport a la même valeur dans les colonnes parentes Feature et Feature \_ de la table file.
-   La fonctionnalité racine sport a le bit msidbFeatureAttributesFollowParent défini.

Dans l’arborescence des fonctionnalités de cet exemple, sport est la fonctionnalité racine et un parent des fonctionnalités de la natation et du football. Freestyle est une fonctionnalité enfant de la natation. TouchFootball est une fonctionnalité enfant du football.

[Table des fonctionnalités](feature-table.md) (partielle)



| Fonctionnalité       | Attributs | Parent de la fonctionnalité \_ |
|---------------|------------|-----------------|
| Sport         | 4          | Sport           |
| Nage      | 1          | Sport           |
| Terrain      | 4          | Sport           |
| Freestyle     | 1          | Nage        |
| TouchFootball | 4          | Terrain        |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE](ice-reference.md)
</dt> </dl>

 

 



