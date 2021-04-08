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
# <a name="mixed-mode-serialization-of-context-handles"></a><span data-ttu-id="fe18e-106">Sérialisation en mode mixte des handles de contexte</span><span class="sxs-lookup"><span data-stu-id="fe18e-106">Mixed Mode Serialization of Context Handles</span></span>

<span data-ttu-id="fe18e-107">À partir de Windows XP, une seule interface peut s’adapter à la fois à des handles de contexte sérialisés et non sérialisés, ce qui permet à une méthode sur une interface d’accéder exclusivement à un handle de contexte (sérialisé), tandis que d’autres méthodes accèdent à ce handle de contexte en mode partagé (non sérialisé).</span><span class="sxs-lookup"><span data-stu-id="fe18e-107">Starting with Windows XP, a single interface can accommodate both serialized and nonserialized context handles, enabling one method on an interface to access a context handle exclusively (serialized), while other methods access that context handle in shared mode (nonserialized).</span></span> <span data-ttu-id="fe18e-108">Pour plus d’informations sur les handles de contexte, consultez les attributs suivants :</span><span class="sxs-lookup"><span data-stu-id="fe18e-108">For more information about context handles, see the following attributes:</span></span>

-   [<span data-ttu-id="fe18e-109">**handle de contexte \_**</span><span class="sxs-lookup"><span data-stu-id="fe18e-109">**context\_handle**</span></span>](context-handle.md)
-   [<span data-ttu-id="fe18e-110">**\_sérialisation du handle de contexte \_**</span><span class="sxs-lookup"><span data-stu-id="fe18e-110">**context\_handle\_serialize**</span></span>](context-handle-serialize.md)
-   [<span data-ttu-id="fe18e-111">**handle de contexte \_ \_ noserialize**</span><span class="sxs-lookup"><span data-stu-id="fe18e-111">**context\_handle\_noserialize**</span></span>](context-handle-noserialize.md)

<span data-ttu-id="fe18e-112">Les fonctionnalités d’accès en mode sérialisé et en mode partagé sont comparables aux mécanismes de verrouillage en lecture/écriture. les méthodes qui utilisent un handle de contexte sérialisé sont des utilisateurs exclusifs (enregistreurs), tandis que les méthodes qui utilisent un handle de contexte non sérialisé sont des utilisateurs partagés (lecteurs).</span><span class="sxs-lookup"><span data-stu-id="fe18e-112">Serialized and shared mode access capabilities are comparable to read/write locking mechanisms; methods using a serialized context handle are exclusive users (writers), whereas methods using a nonserialized context handle are shared users (readers).</span></span> <span data-ttu-id="fe18e-113">Les méthodes qui détruisent ou modifient l’état d’un handle de contexte doivent être sérialisées.</span><span class="sxs-lookup"><span data-stu-id="fe18e-113">Methods that destroy or modify the state of a context handle must be serialized.</span></span> <span data-ttu-id="fe18e-114">Les méthodes qui ne modifient pas l’état d’un handle de contexte, telles que les méthodes qui lisent simplement un handle de contexte, peuvent être non sérialisées.</span><span class="sxs-lookup"><span data-stu-id="fe18e-114">Methods that do not modify the state of a context handle, such as those methods that simply read from a context handle, can be nonserialized.</span></span> <span data-ttu-id="fe18e-115">L’utilisation d’un handle de contexte en mode mixte peut améliorer considérablement l’évolutivité d’un serveur, en particulier lorsque plusieurs threads effectuent des appels simultanés au même handle de contexte.</span><span class="sxs-lookup"><span data-stu-id="fe18e-115">Using a context handle in mixed mode can substantially improve the scalability of a server, especially when multiple threads make simultaneous calls to the same context handle.</span></span>

<span data-ttu-id="fe18e-116">RPC n’applique pas de « verrou d’écriture » sur les méthodes à l’aide d’un handle de contexte en mode partagé, ce qui signifie que les applications doivent s’assurer que les handles de contexte en mode partagé ne sont pas modifiés.</span><span class="sxs-lookup"><span data-stu-id="fe18e-116">RPC does not enforce "write lock" on methods using a context handle in shared mode, which means applications must ensure that shared mode context handles are not modified.</span></span> <span data-ttu-id="fe18e-117">La modification d’un handle de contexte utilisé en mode partagé peut entraîner des altérations subtiles du contenu des handles de contexte, ce qui est impossible à déboguer.</span><span class="sxs-lookup"><span data-stu-id="fe18e-117">Modification of a context handle used in shared mode can result in subtle corruptions of context handle contents, which are impossible to debug.</span></span>

<span data-ttu-id="fe18e-118">La modification de la logique de sérialisation d’un handle de contexte affecte uniquement le serveur.</span><span class="sxs-lookup"><span data-stu-id="fe18e-118">Changing the serialization logic of a context handle affects only the server.</span></span> <span data-ttu-id="fe18e-119">En outre, la modification de la logique de sérialisation d’un handle de contexte n’affecte pas le format de câble, et par conséquent, les modifications apportées à la logique de sérialisation sur un serveur n’affectent pas la capacité des clients existants à interagir avec le serveur.</span><span class="sxs-lookup"><span data-stu-id="fe18e-119">Also, changing the serialization logic of a context handle does not affect the wire format, and therefore, changes to serialization logic on a server do not affect existing clients' capability to interact with the server.</span></span>

<span data-ttu-id="fe18e-120">Il n’est pas recommandé d’utiliser uniquement des handles de contexte non sérialisés.</span><span class="sxs-lookup"><span data-stu-id="fe18e-120">Using only nonserialized context handles is not recommended.</span></span> <span data-ttu-id="fe18e-121">Les serveurs qui utilisent des handles non sérialisés doivent basculer vers l’accès sérialisé pour la méthode qui ferme le handle de contexte.</span><span class="sxs-lookup"><span data-stu-id="fe18e-121">Servers that use nonserialized handles are should switch to serialized access for the method that closes the context handle.</span></span>

<span data-ttu-id="fe18e-122">Les handles de contexte en \[ sortie \] seule sont généralement utilisés par les méthodes de création et ne nécessitent aucune sérialisation.</span><span class="sxs-lookup"><span data-stu-id="fe18e-122">Context handles that are \[out\]-only are typically used by creation methods, and do not require any serialization.</span></span> <span data-ttu-id="fe18e-123">Par conséquent, tous les attributs de sérialisation appliqués à des \[ \] Handles de contexte en sortie seule, tels que [**\_ \_ la sérialisation de handle de contexte**](context-handle-serialize.md) ou le gestionnaire de [**contexte \_ \_ noserialize**](context-handle-noserialize.md), sont ignorés par RPC.</span><span class="sxs-lookup"><span data-stu-id="fe18e-123">Therefore, any serialization attribute applied to \[out\]-only context handles, such as [**context\_handle\_serialize**](context-handle-serialize.md) or [**context\_handle\_noserialize**](context-handle-noserialize.md), is ignored by RPC.</span></span>

> [!Note]  
> <span data-ttu-id="fe18e-124">Les méthodes de création sont sérialisées implicitement.</span><span class="sxs-lookup"><span data-stu-id="fe18e-124">Creation methods are implicitly serialized.</span></span>

 

## <a name="examples"></a><span data-ttu-id="fe18e-125">Exemples</span><span class="sxs-lookup"><span data-stu-id="fe18e-125">Examples</span></span>

<span data-ttu-id="fe18e-126">Les deux exemples suivants montrent comment activer la sérialisation en mode mixte des handles de contexte.</span><span class="sxs-lookup"><span data-stu-id="fe18e-126">The following two examples show how to enable mixed mode serialization of context handles.</span></span>

<span data-ttu-id="fe18e-127">Le premier exemple montre comment procéder dans le fichier IDL :</span><span class="sxs-lookup"><span data-stu-id="fe18e-127">The first example shows how to do so in the IDL file:</span></span>

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

<span data-ttu-id="fe18e-128">Le deuxième exemple montre comment activer la sérialisation en mode mixte des handles de contexte dans le fichier ACF :</span><span class="sxs-lookup"><span data-stu-id="fe18e-128">The second example shows how to enable mixed mode serialization of context handles in the ACF file:</span></span>

``` syntax
typedef [context_handle_serialize] TestContextHandleExclusive;

typedef [context_handle_noserialize] TestContextHandleShared;
```

## <a name="related-topics"></a><span data-ttu-id="fe18e-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fe18e-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fe18e-130">**handle de contexte \_**</span><span class="sxs-lookup"><span data-stu-id="fe18e-130">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="fe18e-131">**\_sérialisation du handle de contexte \_**</span><span class="sxs-lookup"><span data-stu-id="fe18e-131">**context\_handle\_serialize**</span></span>](context-handle-serialize.md)
</dt> <dt>

[<span data-ttu-id="fe18e-132">**handle de contexte \_ \_ noserialize**</span><span class="sxs-lookup"><span data-stu-id="fe18e-132">**context\_handle\_noserialize**</span></span>](context-handle-noserialize.md)
</dt> </dl>

 

 




