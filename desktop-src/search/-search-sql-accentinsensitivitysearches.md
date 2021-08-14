---
description: par défaut, les Windows le moteur de recherche et le catalogue sont insensibles aux signes diacritiques, qui sont des points d’accentuation ajoutés aux lettres pour modifier la signification ou la prononciation d’un mot.
ms.assetid: 71007bd4-5232-469c-982b-ff0d24bd0c1f
title: Respect des signes diacritiques dans les recherches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fcde4eb6cde6fe7a0b25a1d58f8026176de2fe30b6b0e2f020275821891a404
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117863682"
---
# <a name="diacritic-sensitivity-in-searches"></a>Respect des signes diacritiques dans les recherches

par défaut, les Windows le moteur de recherche et le catalogue sont insensibles aux signes diacritiques, qui sont des points d’accentuation ajoutés aux lettres pour modifier la signification ou la prononciation d’un mot. toutefois, Windows Search vous permet de modifier cette valeur pour votre catalogue à l’aide du [gestionnaire de catalogue](-search-3x-wds-mngidx-catalog-manager.md) pour définir la sensibilité des signes diacritiques. Par exemple, si la sensibilité des signes diacritiques est définie sur **false**, le catalogue traiterait « Resume » et « Resumé » comme s’il s’agissait du même mot.

Au niveau de la couche de requête, les termes de requête avec des signes diacritiques en FREETEXT et des clauses CONTAINs sont passés au moteur, puis normalisés (comme ils le seraient au moment de l’index) pour la mise en correspondance. La correspondance avec le catalogue est toujours respectée pour les signes diacritiques.

> [!Note]  
> Ce n’est pas le cas pour les plages de caractères 0x2e81-F8FF et 0x1100-0x11ff.

 

 

 



