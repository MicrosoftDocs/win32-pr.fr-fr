---
title: Types prédéfinis et de base MIDL
description: MIDL prend en charge les types de base et prédéfinis suivants.
ms.assetid: 72da24b6-253d-4032-ba0c-58b2542701fc
keywords:
- types de données MIDL, prédéfinis et de base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6ecbc76b3f680f0fffbabcff38e8562475e26be8ae4ac583a78c614d1651151
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067079"
---
# <a name="midl-predefined-and-base-types"></a>Types prédéfinis et de base MIDL

MIDL prend en charge les types de base et prédéfinis suivants.



| Type de données                                  | Description                                                                                                                                                                                             | Signe par défaut     |
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------|
| [**expression**](boolean.md)                 | 8 bits. Non compatible avec les interfaces [**oleautomation**](oleautomation.md) ; Utilisez à la \_ place variant bool.                                                                                               | Non signé         |
| [**poids**](byte.md)                       | 8 bits.                                                                                                                                                                                                 | (non applicable) |
| [**Char**](char-idl.md)                   | 8 bits.                                                                                                                                                                                                 | Non signé         |
| [**Cliquer**](double.md)                   | nombre à virgule flottante 64 bits.                                                                                                                                                                           | (non applicable) |
| [**État d’erreur \_ \_ t**](error-status-t.md) | entier non signé 32 bits pour retourner les valeurs d’État pour la gestion des erreurs.                                                                                                                                 | Non signé         |
| [**dissocié**](float.md)                     | nombre à virgule flottante 32 bits.                                                                                                                                                                           | (non applicable) |
| [**handle \_ t**](handle-t.md)              | Type de handle primitif pour la liaison.                                                                                                                                                                      | (non applicable) |
| [**hyper**](hyper.md)                     | entier 64 bits.                                                                                                                                                                                         | Signé           |
| [**int**](int.md)                         | entier 32 bits. Sur les plateformes 16 bits, ne peut pas apparaître dans les fonctions distantes sans qualificateur de taille, par exemple [**short**](short.md), [**Small**](small.md), [**long**](long.md) ou [**hyper**](hyper.md). | Signé           |
| **\_\_int8**                               | entier 8 bits. Équivalent à **Small**.                                                                                                                                                                 | Signé           |
| **\_\_Int16**                              | entier 16 bits. Équivalent à **short**.                                                                                                                                                                | Signé           |
| **\_\_entier**                              | entier 32 bits. Équivalent à [**long**](long.md).                                                                                                                                                     | Signé           |
| [**\_\_int3264**](--int3264.md)           | Entier qui est 32 bits sur les plateformes 32 bits et est 64 bits sur les plateformes 64 bits.                                                                                                                       | Signé           |
| [**\_\_Int64**](--int64.md)               | entier 64 bits. Équivalent à [**hyper**](hyper.md).                                                                                                                                                   | Signé           |
| [**long**](long.md)                       | entier 32 bits.                                                                                                                                                                                         | Signé           |
| [**short**](short.md)                     | entier 16-BT.                                                                                                                                                                                          | Signé           |
| [**Small**](small.md)                     | entier 8 bits.                                                                                                                                                                                          | Signé           |
| [**nullité**](void.md)                       | Indique que la procédure ne retourne pas de valeur.                                                                                                                                                   | (non applicable) |
| **nullité \***                                | pointeur 32 bits pour les handles de contexte uniquement.                                                                                                                                                                | (non applicable) |
| [**WCHAR \_ t**](wchar-t.md)                | type prédéfini 16 bits pour les caractères larges.                                                                                                                                                             | Non signé         |



 

 

 




