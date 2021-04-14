---
title: Gestion de l’allocation de mémoire
description: Gestion de l’allocation de mémoire
ms.assetid: 8a189fe8-5555-44bb-968b-04408fa7fce4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2af04b4ecc5b8480230b17ae710b84ce8e6ce5d
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104383011"
---
# <a name="managing-memory-allocation"></a>Gestion de l’allocation de mémoire

Dans COM, de nombreuses méthodes d’interface sont appelées par du code écrit par une organisation de programmation et implémentées par du code écrit par un autre. La plupart des paramètres et valeurs de retour de ces fonctions sont des types qui peuvent être passés par valeur. Toutefois, il est parfois nécessaire de passer des structures de données pour lesquelles ce n’est pas le cas. par conséquent, il est nécessaire que l’appelant et l’appel aient une stratégie d’allocation et de désallocation compatible. COM définit une Convention universelle pour l’allocation de mémoire, car il est plus raisonnable de définir des règles de cas par cas et de sorte que l’implémentation de l’appel de procédure distante COM puisse gérer correctement la mémoire.

Les méthodes d’une interface COM fournissent toujours la gestion de la mémoire des pointeurs à l’interface en appelant les fonctions [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) et [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) qui se trouvent dans l’interface [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) , à partir desquelles toutes les autres interfaces COM dérivent. (Pour plus d’informations, consultez [règles de gestion des décomptes de références](rules-for-managing-reference-counts.md) .)

Cette section décrit uniquement comment allouer de la mémoire pour des paramètres qui ne sont pas passés par valeur, et non des pointeurs vers des interfaces, mais des éléments plus banals comme des chaînes, des pointeurs vers des structures, etc.

Pour plus d'informations, voir les rubriques suivantes :

-   [Allocateur de mémoire OLE](the-ole-memory-allocator.md)
-   [Règles de gestion de la mémoire](memory-management-rules.md)
-   [Débogage des allocations de mémoire](debugging-memory-allocations.md)

 

 