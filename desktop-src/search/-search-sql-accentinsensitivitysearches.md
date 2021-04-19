---
description: Par défaut, le catalogue et le moteur de recherche Windows sont insensibles aux signes diacritiques, qui sont des points d’accentuation ajoutés aux lettres pour modifier la signification ou la prononciation d’un mot.
ms.assetid: 71007bd4-5232-469c-982b-ff0d24bd0c1f
title: Respect des signes diacritiques dans les recherches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46fb68676418fc109fa24ed2d55fb9602b7ad41d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514792"
---
# <a name="diacritic-sensitivity-in-searches"></a>Respect des signes diacritiques dans les recherches

Par défaut, le catalogue et le moteur de recherche Windows sont insensibles aux signes diacritiques, qui sont des points d’accentuation ajoutés aux lettres pour modifier la signification ou la prononciation d’un mot. Toutefois, Windows Search vous permet de modifier cela pour votre catalogue à l’aide du [Gestionnaire de catalogue](-search-3x-wds-mngidx-catalog-manager.md) pour définir la sensibilité des signes diacritiques. Par exemple, si la sensibilité des signes diacritiques est définie sur **false**, le catalogue traiterait « Resume » et « Resumé » comme s’il s’agissait du même mot.

Au niveau de la couche de requête, les termes de requête avec des signes diacritiques en FREETEXT et des clauses CONTAINs sont passés au moteur, puis normalisés (comme ils le seraient au moment de l’index) pour la mise en correspondance. La correspondance avec le catalogue est toujours respectée pour les signes diacritiques.

> [!Note]  
> Ce n’est pas le cas pour les plages de caractères 0x2e81-F8FF et 0x1100-0x11ff.

 

 

 



