---
description: Le programme d’installation définit les propriétés selon l’ordre de priorité suivant. Une valeur de propriété dans cette liste peut remplacer une valeur qui vient après celle-ci et être remplacée par une valeur antérieure à celle-ci dans la liste.
ms.assetid: ba9240fe-2e5a-43f5-8cdf-59dd6348092b
title: Ordre de priorité des propriétés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90c114594b9a825a3847db37f5b98dc990211d9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522446"
---
# <a name="order-of-property-precedence"></a>Ordre de priorité des propriétés

Le programme d’installation définit les propriétés selon l’ordre de priorité suivant. Une valeur de propriété dans cette liste peut remplacer une valeur qui vient après celle-ci et être remplacée par une valeur antérieure à celle-ci dans la liste.

1.  Propriétés spécifiées par l’environnement d’exploitation.
2.  [Propriétés publiques](public-properties.md) définies sur la ligne de commande.
3.  Propriétés publiques listées par [**AdminProperties**](adminproperties.md) PropertySet pendant une [installation administrative](administrative-installation.md) .
4.  Propriétés publiques ou privées définies lors de l’application d’une [*transformation*](t-gly.md).
5.  Propriété publique ou privée définie par la création de la [table de propriétés](property-table.md) du fichier. msi.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos des propriétés](about-properties.md)
</dt> </dl>

 

 



