---
description: ICEM06 recherche des références directes non valides aux fonctionnalités par le module.
ms.assetid: 63e63a60-53e5-4881-ad71-efeceb73a70e
title: ICEM06
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 945d45471ec86605e0fa509fc1855aa1cfd5d698
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865762"
---
# <a name="icem06"></a>ICEM06

ICEM06 recherche des références directes non valides aux fonctionnalités par le module.

Le module de fusion CIEM est stocké dans un fichier de module de fusion. CUB appelé Mergemod. CUB et non dans le fichier. CUB contenant le CIEM utilisé pour la validation du package.

## <a name="result"></a>Résultats

ICEM06 publie une erreur lorsque la base de données du module contient des références directes à une fonctionnalité. Les informations sur les fonctionnalités doivent être fournies par l’utilisateur du module.

## <a name="example"></a>Exemple

ICEM06 publie les messages d’erreur suivants pour un module contenant les entrées de base de données présentées ci-dessous.

``` syntax
The target of shortcut Shortcut1.GUID1 is not a property and not a null GUID. 
Modules may not directly reference features.
The row GUID2.LocalServer32.Component2 in the Class table has a feature reference 
that is not a null GUID. Modules may not directly reference features.
```

[Table de raccourcis](shortcut-table.md) (partielle)



| Raccourci          | Cible                                 |
|-------------------|----------------------------------------|
| Shortcut1. *Guid1* | cmd.exe                                |
| Shortcut2. *Guid1* | \[MyProp\]                             |
| Shortcut3. *Guid1* | {00000000-0000-0000-0000-000000000000} |



 

[Table de classe](class-table.md) (partielle)



| CLSID   | Context       | -\_ | Fonctionnalité\_                              |
|---------|---------------|-------------|----------------------------------------|
| *GUID1* | LocalServer32 | Composant1  | {00000000-0000-0000-0000-000000000000} |
| *GUID2* | LocalServer32 | Component2  | MyFeature                              |



 

ICEM06 signale la première erreur, car le premier enregistrement de la table de raccourcis contient une entrée dans le champ cible qui n’est pas une propriété ou un GUID null. Un module ne peut pas référencer directement une fonctionnalité. Les informations sur les fonctionnalités doivent être fournies par l’utilisateur du module. Pour corriger cette erreur, les références à une fonctionnalité doivent être remplacées par un GUID null.

ICEM06 signale la deuxième erreur, car le deuxième enregistrement de la table de classe contient une entrée dans le champ Feature qui n’est pas un GUID null. Un module ne peut pas référencer directement une fonctionnalité. Les informations sur les fonctionnalités doivent être fournies par l’utilisateur du module. Pour corriger cette erreur, les références à une fonctionnalité doivent être remplacées par un GUID null.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE du module de fusion](merge-module-ice-reference.md)
</dt> </dl>

 

 



