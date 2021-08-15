---
description: Le terme FORMSOF effectue des correspondances à l’aide d’autres formes linguistiques du mot.
ms.assetid: b705b8bc-dc2c-4cee-8306-f494b0f96cbf
title: Terme FORMSOF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1ffcbd832833a506db99236bf26921a4b0145ffe5bfccaed8fff59103370291
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117863442"
---
# <a name="formsof-term"></a>Terme FORMSOF

Le terme FORMSOF effectue des correspondances à l’aide d’autres formes linguistiques du mot. Voici la syntaxe du terme FORMSOF :


```
FORMSOF (<generation_type>,<match_words>)
```



le type de génération spécifie la manière dont Microsoft Windows Search choisit les autres formes de mots. La valeur **fléchie** choisit d’autres formes fléchies pour les mots de correspondance. Si le mot est un verbe, d’autres dizaines sont utilisés. Si le mot est un substantif, les formes singulières, plurielles et de possession sont utilisées pour détecter les correspondances.

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

 

 



