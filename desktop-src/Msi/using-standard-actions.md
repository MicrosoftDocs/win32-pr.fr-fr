---
description: une action est exécutée dans la Windows Installer en appelant la fonction MsiDoAction ou en incluant l’action dans une table de séquences.
ms.assetid: ee5bdc72-adf4-46f4-ae1f-4c41d22a1ed8
title: Utilisation d’actions standard
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60696e79c12b054739d87ffe5696e898a8eb955c4c7bfe0aa9c2341db7c2d720
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996209"
---
# <a name="using-standard-actions"></a>Utilisation d’actions standard

une action est exécutée dans la Windows Installer en appelant la fonction [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) ou en incluant l’action dans une table de séquences. Étant donné que la plupart des actions encapsulent un seul objectif, la méthode la plus courante pour utiliser des actions consiste à ordonner une série d’actions dans une séquence pour accomplir une tâche plus importante. Le programme d’installation a trois actions de niveau supérieur standard qui appellent un ensemble de tables de séquences associé. Ces tables de séquence associées peuvent contenir des actions standard, des actions personnalisées et des éléments d’interface utilisateur. Chaque action dans une table de séquences a un numéro de séquence associé et peut également avoir une expression conditionnelle associée. Toutes les actions d’une table Sequence sont visitées dans l’ordre et ne sont exécutées que si l’expression conditionnelle prend la valeur true.

Alors qu’une action standard peut être associée à n’importe quel numéro de séquence, de nombreuses restrictions de séquence doivent être suivies pour que l’action fonctionne correctement. Par exemple, l' [action FileCost](filecost-action.md)doit être appelée après l' [action CostInitialize](costinitialize-action.md). Pour plus d’informations sur les restrictions de séquencement d’actions standard, consultez [actions avec restrictions de séquencement](actions-with-sequencing-restrictions.md), [actions sans restrictions de séquencement](actions-without-sequencing-restrictions.md)ou [référence d’actions standard](standard-actions-reference.md).

Les rubriques suivantes fournissent des informations supplémentaires sur l’utilisation des actions standard.

-   [Publication de produits, de fonctionnalités et de composants](publishing-products-features-and-components.md)
-   [Recherche de fichiers](file-searching.md)
-   [Coût des fichiers](file-costing.md)
-   [Installation du fichier](file-installation.md)
-   [Modification du Registre](modifying-the-registry.md)
-   [Actions en cours d’exécution](running-actions.md)

Voir aussi [à propos des actions standard](about-standard-actions.md) ou de la [référence aux actions standard](standard-actions-reference.md).

 

 



