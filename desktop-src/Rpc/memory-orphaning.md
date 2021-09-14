---
title: Mémoire orpheline
description: Si votre application distribuée utilise un paramètre \ in, out, unique \ ou \ in, out, PTR \ pointer, le côté serveur de l’application peut remplacer la valeur du paramètre de pointeur par null.
ms.assetid: 65588b4d-6bf4-44f7-994c-29a5b185c6b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32042911695f377e0a628168e91387bfa25f0d79
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127194060"
---
# <a name="memory-orphaning"></a>Mémoire orpheline

Si votre application distribuée utilise un \[ paramètre [de pointeur in](/windows/desktop/Midl/in), [out](/windows/desktop/Midl/out-idl), [unique](/windows/desktop/Midl/unique) \] ou \[ **in**, **out**, [ptr](/windows/desktop/Midl/ptr) \] , le côté serveur de l’application peut remplacer la valeur du paramètre de pointeur par null. Quand le serveur retourne par la suite la valeur null au client, la mémoire référencée par le pointeur avant l’appel de procédure distante est toujours présente côté client, mais n’est plus accessible à partir de ce pointeur (sauf dans le cas d’un pointeur complet avec alias). Cette mémoire est dite *orpheline*. Il s’agit également d’une *fuite de mémoire*. L’orpheline de la mémoire sur le client entraîne l’insuffisance des ressources mémoire disponibles sur le client.

La mémoire peut également être orpheline chaque fois que le serveur fait passer un pointeur incorporé à une valeur null. Par exemple, si le paramètre pointe vers une structure de données complexe telle qu’une arborescence, le côté serveur de l’application peut supprimer des nœuds de l’arborescence et définir des pointeurs à l’intérieur de l’arborescence sur la valeur null.

Une autre situation qui peut entraîner une fuite de mémoire implique des tableaux conformes, variables et ouverts contenant des pointeurs. Lorsque l’application serveur modifie le paramètre qui spécifie la taille du tableau ou la plage transmise afin qu’elle représente une valeur inférieure, les stubs utilisent la ou les plus petites valeurs pour libérer de la mémoire. Les éléments de tableau avec des index supérieurs au paramètre de taille sont orphelins. Votre application doit libérer des éléments en dehors de la plage transmise.

 

 