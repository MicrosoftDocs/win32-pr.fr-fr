---
title: Règles de gestion de la mémoire
description: Règles de gestion de la mémoire
ms.assetid: 769127a1-1a14-4ed4-9d38-7cf3e571b661
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56e7ad2483b794ec5c2e9c325bca8e469ff4ae0b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127293667"
---
# <a name="memory-management-rules"></a>Règles de gestion de la mémoire

La durée de vie des pointeurs vers les interfaces est toujours gérée par le biais des méthodes [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) et [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sur chaque interface com. Pour plus d’informations, consultez [règles de gestion des décomptes de références](rules-for-managing-reference-counts.md).

Pour tous les autres paramètres, il est important d’adhérer à certaines règles de gestion de la mémoire. Les règles suivantes s’appliquent à tous les paramètres de l’interface MethodsÂ, y compris les valueâ de retour, qui ne sont pas passés par valeur :

-   Les paramètres in doivent être alloués et libérés par l’appelant.
-   Les paramètres out doivent être alloués par celui appelé ; ils sont libérés par l’appelant à l’aide de l’allocateur de mémoire de tâche COM standard. Pour plus d’informations, consultez [l’allocation de mémoire OLE](the-ole-memory-allocator.md) .
-   In/out : les paramètres sont initialement alloués par l’appelant, puis libérés et réalloués par celui-ci, si nécessaire. Comme c’est le cas pour les paramètres out, l’appelant est responsable de la libération de la valeur finale retournée. L’allocateur de mémoire COM standard doit être utilisé.

Dans les deux derniers cas, où un morceau de code alloue la mémoire et un morceau de code différent le libère, l’utilisation de l’allocateur COM permet de s’assurer que les deux parties du code utilisent les mêmes méthodes d’allocation.

Un autre domaine nécessitant une attention particulière est le traitement des paramètres out et out en cas de défaillance. Si une fonction retourne un code d’échec, l’appelant n’a généralement aucun moyen de nettoyer les paramètres out ou out. Cela provoque les règles supplémentaires suivantes :

-   En cas de condition d’erreur, les paramètres doivent toujours être définis de manière fiable sur une valeur qui sera nettoyée sans aucune action de l’appelant.
-   Tous les paramètres de point de sortie doivent avoir explicitement la valeur **null**. Elles sont généralement passées dans un paramètre pointeur vers pointeur, mais peuvent également être passées en tant que membres d’une structure que l’appelant alloue et que le code appelé remplit. Le moyen le plus simple de s’en assurer est (en partie) de définir ces valeurs sur **null** dans l’entrée de la fonction. Cette règle est importante, car elle favorise une interopérabilité des applications plus robuste.
-   Dans les conditions d’erreur, tous les paramètres d’entrée-sortie doivent être laissés seul par le code appelé (par conséquent, restant à la valeur à laquelle ils ont été initialisés par l’appelant) ou être définis explicitement, comme dans le cas d’une erreur de retour de paramètre de sortie.

N’oubliez pas que ces conventions de gestion de la mémoire pour les applications COM s’appliquent uniquement à travers les interfaces publiques et APIsâ. en effet, il n’y a aucune exigence à ce que l’allocation de mémoire strictement interne à une application COM doive être effectuée à l’aide de ces mécanismes.

COM utilise en interne les appels de procédure distante (RPC) pour communiquer entre les clients et les serveurs. Pour plus d’informations sur la gestion de la mémoire dans les stubs de serveur RPC, consultez la rubrique gestion de la [mémoire de serveur stub](../rpc/server-stub-memory-management.md) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Gestion de l’allocation de mémoire](managing-memory-allocation.md)
</dt> </dl>

 

 