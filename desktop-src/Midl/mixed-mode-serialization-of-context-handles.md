---
title: Sérialisation en mode mixte des handles de contexte
description: Dans Microsoft Windows XP, une seule interface peut s’adapter à la fois à des handles de contexte sérialisés et non sérialisés, appelée sérialisation en mode mixte.
ms.assetid: b52c1d6f-cdc5-4597-a36e-bb957e4aab01
keywords:
- Référence du langage MIDL MIDL, sérialisation en mode mixte des handles de contexte
- handles de contexte MIDL
- sérialisation en mode mixte MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0922b53bfc7ba2e30ad8df0764e3cf9a36f0f723
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839961"
---
# <a name="mixed-mode-serialization-of-context-handles"></a>Sérialisation en mode mixte des handles de contexte

À partir de Windows XP, une seule interface peut s’adapter à la fois à des handles de contexte sérialisés et non sérialisés, ce qui permet à une méthode sur une interface d’accéder exclusivement à un handle de contexte (sérialisé), tandis que d’autres méthodes accèdent à ce handle de contexte en mode partagé (non sérialisé). Pour plus d’informations sur les handles de contexte, consultez les attributs suivants :

-   [**handle de contexte \_**](context-handle.md)
-   [**\_sérialisation du handle de contexte \_**](context-handle-serialize.md)
-   [**handle de contexte \_ \_ noserialize**](context-handle-noserialize.md)

Les fonctionnalités d’accès en mode sérialisé et en mode partagé sont comparables aux mécanismes de verrouillage en lecture/écriture. les méthodes qui utilisent un handle de contexte sérialisé sont des utilisateurs exclusifs (enregistreurs), tandis que les méthodes qui utilisent un handle de contexte non sérialisé sont des utilisateurs partagés (lecteurs). Les méthodes qui détruisent ou modifient l’état d’un handle de contexte doivent être sérialisées. Les méthodes qui ne modifient pas l’état d’un handle de contexte, telles que les méthodes qui lisent simplement un handle de contexte, peuvent être non sérialisées. L’utilisation d’un handle de contexte en mode mixte peut améliorer considérablement l’évolutivité d’un serveur, en particulier lorsque plusieurs threads effectuent des appels simultanés au même handle de contexte.

RPC n’applique pas de « verrou d’écriture » sur les méthodes à l’aide d’un handle de contexte en mode partagé, ce qui signifie que les applications doivent s’assurer que les handles de contexte en mode partagé ne sont pas modifiés. La modification d’un handle de contexte utilisé en mode partagé peut entraîner des altérations subtiles du contenu des handles de contexte, ce qui est impossible à déboguer.

La modification de la logique de sérialisation d’un handle de contexte affecte uniquement le serveur. En outre, la modification de la logique de sérialisation d’un handle de contexte n’affecte pas le format de câble, et par conséquent, les modifications apportées à la logique de sérialisation sur un serveur n’affectent pas la capacité des clients existants à interagir avec le serveur.

Il n’est pas recommandé d’utiliser uniquement des handles de contexte non sérialisés. Les serveurs qui utilisent des handles non sérialisés doivent basculer vers l’accès sérialisé pour la méthode qui ferme le handle de contexte.

Les handles de contexte en \[ sortie \] seule sont généralement utilisés par les méthodes de création et ne nécessitent aucune sérialisation. Par conséquent, tous les attributs de sérialisation appliqués à des \[ \] Handles de contexte en sortie seule, tels que [**\_ \_ la sérialisation de handle de contexte**](context-handle-serialize.md) ou le gestionnaire de [**contexte \_ \_ noserialize**](context-handle-noserialize.md), sont ignorés par RPC.

> [!Note]  
> Les méthodes de création sont sérialisées implicitement.

 

## <a name="examples"></a>Exemples

Les deux exemples suivants montrent comment activer la sérialisation en mode mixte des handles de contexte.

Le premier exemple montre comment procéder dans le fichier IDL :

``` syntax
typedef [context_handle] void *TestContextHandleExclusive;
typedef [context_handle] TestContextHandleExclusive TestContextHandleShared;

void
UseShared(...
          [in] TestContextHandleShared *Ctx,
          ...);

void
UseExclusive(...
             [in, out] TestContextHandleExclusive *Ctx,
             ...);
```

Le deuxième exemple montre comment activer la sérialisation en mode mixte des handles de contexte dans le fichier ACF :

``` syntax
typedef [context_handle_serialize] TestContextHandleExclusive;

typedef [context_handle_noserialize] TestContextHandleShared;
```

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**handle de contexte \_**](context-handle.md)
</dt> <dt>

[**\_sérialisation du handle de contexte \_**](context-handle-serialize.md)
</dt> <dt>

[**handle de contexte \_ \_ noserialize**](context-handle-noserialize.md)
</dt> </dl>

 

 




