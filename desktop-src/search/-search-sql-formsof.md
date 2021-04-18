---
description: Le terme FORMSOF effectue des correspondances à l’aide d’autres formes linguistiques du mot.
ms.assetid: b705b8bc-dc2c-4cee-8306-f494b0f96cbf
title: Terme FORMSOF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20504a7a36c7f0cb9c69b9513f33446501641bc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106512940"
---
# <a name="formsof-term"></a>Terme FORMSOF

Le terme FORMSOF effectue des correspondances à l’aide d’autres formes linguistiques du mot. Voici la syntaxe du terme FORMSOF :


```
FORMSOF (<generation_type>,<match_words>)
```



Le type de génération spécifie la manière dont Microsoft Windows Search choisit les autres formes de mots. La valeur **fléchie** choisit d’autres formes fléchies pour les mots de correspondance. Si le mot est un verbe, d’autres dizaines sont utilisés. Si le mot est un substantif, les formes singulières, plurielles et de possession sont utilisées pour détecter les correspondances.

La valeur de correspondance des \_ mots correspond à un ou plusieurs mots, séparés par des virgules.

## <a name="examples"></a>Exemples

L’exemple suivant recherche des correspondances fléchies pour le mot « Run ». Cet exemple correspond à des documents contenant « exécuter », « en cours d’exécution » ou « exécuté ».


```
...CONTAINS('FORMSOF(INFLECTIONAL,"run")')
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Informations de référence**
</dt> <dt>

[Prédicat FREETEXT](-search-sql-freetext.md)
</dt> <dt>

[Clause WHERE](-search-sql-where.md)
</dt> </dl>

 

 



