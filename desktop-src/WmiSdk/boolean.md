---
title: booléen (WMI)
description: Est un \_ paramètre VT bool qui prend la valeur de la variante \_ TRUE (&\# 8211 ; 1) ou la variante \_ false (0).
ms.assetid: 3928ff39-ed17-4a61-bb72-a3c9be16ae45
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50422990a45dd59c2bedc3ac90bddcf06f7796cd3308daf03a11db0dca38f0b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051057"
---
# <a name="boolean-wmi"></a>booléen (WMI)

Le type de données Boolean est un \_ paramètre VT bool qui prend la valeur de la variante \_ true (– 1) ou de la variante \_ false (0). Le tableau suivant répertorie la différence entre les représentations de programmation de la **valeur logique true** en C/C++ et le type Automation.

| Langage   | Valeur         | Valeur numérique |
|------------|---------------|-----------------|
| C/C++      | **TRUE**      | 1               |
| Automatisation | VARIANTE \_ true | –1              |

Les deux types sont différents de zéro et, par conséquent, n’ont pas la valeur **false**, mais ont des représentations différentes pour **true**.
