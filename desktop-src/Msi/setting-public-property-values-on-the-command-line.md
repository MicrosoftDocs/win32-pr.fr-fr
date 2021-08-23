---
description: Pour définir une propriété publique sur une valeur de chaîne littérale, incluez la chaîne entre guillemets.
ms.assetid: ec2626fa-a3be-45e5-a566-658206d3d0bb
title: Définition des valeurs de propriété publiques sur la ligne de commande
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9db6c2f2b46a50ced914112b0ecb2b889c130ee7044130c11def9ad4ea0a5c85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118624934"
---
# <a name="setting-public-property-values-on-the-command-line"></a>Définition des valeurs de propriété publiques sur la ligne de commande

Pour définir une propriété publique sur une valeur de chaîne littérale, incluez la chaîne entre guillemets.

PROPERTY = "String"

Les guillemets sont requis uniquement si la chaîne contient des espaces. Pour effacer une propriété publique sur une ligne de commande (en lui affectant la valeur null), définissez la valeur de la propriété sur une chaîne vide. Dans ce cas, des guillemets sont requis.

PROPERTY = "".

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de propriétés](using-properties.md)
</dt> <dt>

[Obtention et définition des propriétés](getting-and-setting-properties.md)
</dt> </dl>

 

 



