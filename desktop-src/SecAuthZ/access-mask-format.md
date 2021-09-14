---
description: Tous les objets sécurisables réorganisent leurs droits d’accès à l’aide du format de masque d’accès indiqué dans l’illustration suivante.
ms.assetid: c7b97cd8-66b6-42dc-b75b-2c0adb87d020
title: Format du masque d’accès
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2f6c66c99ed93dca399825621dfbd0cc01c2ec6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013755"
---
# <a name="access-mask-format"></a>Format du masque d’accès

Tous les objets sécurisables réorganisent leurs droits d’accès à l’aide du format de [*masque d’accès*](/windows/desktop/SecGloss/a-gly) indiqué dans l’illustration suivante.

![format du masque d’accès](images/accctrl4.png)

Dans ce format, les 16 bits de poids faible sont pour les droits d’accès spécifiques aux objets, les 8 bits suivants sont pour les [droits d’accès standard](standard-access-rights.md), qui s’appliquent à la plupart des types d’objets, et les 4 bits de poids fort sont utilisés pour spécifier des [droits d’accès génériques](generic-access-rights.md) que chaque type d’objet peut mapper à un ensemble de droits standard et spécifiques aux objets. Le \_ bit de \_ sécurité système Access correspond au [droit d’accéder à la liste SACL de l’objet](sacl-access-right.md).

 

 
