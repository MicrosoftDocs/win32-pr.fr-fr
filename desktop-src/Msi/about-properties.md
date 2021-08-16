---
description: Windows Le programme d’installation peut configurer l’installation des logiciels à l’aide des valeurs des variables définies dans un package d’installation ou par l’utilisateur.
ms.assetid: b7b715e7-e92c-4b84-b60d-a0ff8412749b
title: À propos des propriétés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb4a7bdd5a70721520c4d2afb975aabaca312975dc3bf4b7d94215112f69a0a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118382076"
---
# <a name="about-properties"></a>À propos des propriétés

Windows Le programme d’installation peut configurer l’installation des logiciels à l’aide des valeurs des variables définies dans un package d’installation ou par l’utilisateur.

Windows Le programme d’installation utilise trois catégories de variables globales au cours d’une installation :

-   Propriétés privées : le programme d’installation utilise des propriétés privées en interne et leurs valeurs doivent être créées dans la base de données d’installation ou définies sur des valeurs déterminées par l’environnement d’exploitation.
-   Propriétés publiques : les propriétés publiques peuvent être créées dans la base de données et modifiées par un utilisateur ou un administrateur système sur la ligne de commande, en appliquant une transformation ou en interagissant avec une interface utilisateur créée.
-   Propriétés publiques restreintes : pour des raisons de sécurité, l’auteur d’un package d’installation peut restreindre les propriétés publiques qu’un utilisateur peut modifier.

Toutes les propriétés ne doivent pas être définies dans chaque package, il existe un petit ensemble de propriétés requises qui doivent être définies dans chaque package. Le programme d’installation définit les valeurs des propriétés dans un ordre de priorité particulier.

[Propriétés privées](private-properties.md)

[Propri&amp;#233;t&amp;#233;s publiques](public-properties.md)

[Propriétés publiques restreintes](restricted-public-properties.md)

[Propriétés requises](required-properties.md)

[Ordre de priorité des propriétés](order-of-property-precedence.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de propriétés](using-properties.md)
</dt> <dt>

[Référence de propriété](property-reference.md)
</dt> </dl>

 

 



