---
description: Tous les noms de propriété doivent respecter ces restrictions.
ms.assetid: 4447013a-86c4-48a9-bfe1-5e758c799a2f
title: Restrictions sur les noms de propriété
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c137bc4902bdd62b42e4f3888243a11de43399b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104204180"
---
# <a name="restrictions-on-property-names"></a>Restrictions sur les noms de propriété

Tous les noms de propriété doivent respecter ces restrictions.

-   Un nom de propriété est un [identificateur](identifier.md), qui est une chaîne de texte qui doit commencer par une lettre ou un trait de soulignement. Les identificateurs et les noms de propriété peuvent contenir des lettres, des chiffres, des traits de soulignement ou des points. mais ne peut pas commencer par un chiffre ou une période.
-   Les noms de [propriétés publiques](public-properties.md) ne peuvent pas contenir de lettres minuscules.
-   Les noms de [propriétés privées](private-properties.md) doivent contenir des lettres minuscules.
-   Les noms de propriétés précédés de% représentent les variables d’environnement système et utilisateur. Celles-ci ne sont jamais entrées dans la [table de propriétés](property-table.md). Les paramètres permanents des variables d’environnement peuvent être modifiés uniquement à l’aide de la [table d’environnement](environment-table.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de propriétés](using-properties.md)
</dt> </dl>

 

 



