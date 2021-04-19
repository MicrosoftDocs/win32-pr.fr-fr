---
description: Les composants sont souvent conçus pour effectuer des tâches d’initialisation lorsqu’ils sont appelés pour la première fois, plutôt que lorsqu’ils sont chargés.
ms.assetid: 404c083c-7bee-44c2-b8e7-da1901b6ab2f
title: Initialisation One-Time
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16f451e3c51716b4ff6f33b55d8d8602b5d5c28f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529452"
---
# <a name="one-time-initialization"></a>Initialisation One-Time

Les composants sont souvent conçus pour effectuer des tâches d’initialisation lorsqu’ils sont appelés pour la première fois, plutôt que lorsqu’ils sont chargés. Les fonctions d’initialisation ponctuelles garantissent que cette initialisation se produit une seule fois, même lorsque plusieurs threads peuvent tenter l’initialisation.

**Windows Server 2003 et Windows XP :** Les applications doivent fournir leur propre synchronisation pour une initialisation unique à l’aide des [fonctions bloquées](interlocked-variable-access.md) ou d’un autre mécanisme de synchronisation. Les fonctions d’initialisation unique sont disponibles à partir de Windows Vista et de Windows Server 2008.

Les fonctions d’initialisation unique fournissent des avantages significatifs pour s’assurer qu’un seul thread effectue l’initialisation :

-   Ils sont optimisés pour la vitesse.
-   Ils créent les barrières appropriées sur les architectures de processeur qui en ont besoin.
-   Ils prennent en charge l’initialisation verrouillée et parallèle.
-   Ils évitent le verrouillage interne afin que le code puisse fonctionner de manière asynchrone ou synchrone.

Le système gère le processus d’initialisation par le biais d’une structure **init opaque \_ une fois** qui contient des données et des informations d’État. L’appelant alloue cette structure et l’initialise en appelant [**InitOnceInitialize**](/windows/win32/api/synchapi/nf-synchapi-initonceinitialize) (pour initialiser la structure dynamiquement) ou en affectant l’initialisation de constante **\_ une fois \_ \_** l’initialisation statique à la variable de structure (pour initialiser la structure de manière statique). Initialement, les données stockées dans la structure d’initialisation à usage unique ont la valeur NULL et son état n’est pas initialisé.

Les structures d’initialisation à usage unique ne peuvent pas être partagées entre les processus.

Le thread qui effectue l’initialisation peut éventuellement définir un contexte qui est disponible pour l’appelant une fois l’initialisation terminée. Il peut s’agir d’un objet de synchronisation ou d’une valeur ou d’une structure de données. Si le contexte est une valeur, son initialisation de poids **faible \_ une fois que les \_ \_ \_ bits réservés CTX** doivent être nuls. Si le contexte est une structure de données, la structure de données doit être alignée sur la **valeur DWORD**. Le contexte est retourné à l’appelant dans le paramètre de sortie *lpContext* de la fonction [**InitOnceBeginInitialize**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize) ou [**InitOnceExecuteOnce**](/windows/win32/api/synchapi/nf-synchapi-initonceexecuteonce) .

Une initialisation unique peut être effectuée de façon synchrone ou asynchrone. Une fonction de rappel facultative peut être utilisée pour une initialisation unique synchrone.

## <a name="synchronous-one-time-initialization"></a>Initialisation unique synchrone

Les étapes suivantes décrivent une initialisation unique synchrone qui n’utilise pas de fonction de rappel.

1.  Le premier thread à appeler la fonction [**InitOnceBeginInitialize**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize) réussit à démarrer l’initialisation unique. Pour une initialisation unique synchrone, **InitOnceBeginInitialize** doit être appelé sans l’indicateur **Async init \_ once \_** .
2.  Les threads suivants qui tentent d’effectuer une initialisation sont bloqués jusqu’à ce que le premier thread ait terminé l’initialisation ou échoue. Si le premier thread échoue, le thread suivant est autorisé à tenter l’initialisation, et ainsi de suite.
3.  Une fois l’initialisation terminée, le thread appelle la fonction [**InitOnceComplete**](/windows/win32/api/synchapi/nf-synchapi-initoncecomplete) . Le thread peut éventuellement créer un objet de synchronisation (ou d’autres données de contexte) et le spécifier dans le paramètre *lpContext* de la fonction **InitOnceComplete** .
4.  Si l’initialisation est réussie, l’état de la structure d’initialisation à usage unique est remplacé par Initialized et le handle *lpContext* (le cas échéant) est stocké dans la structure d’initialisation. Les tentatives d’initialisation suivantes retournent ces données de contexte. Si l’initialisation échoue, les données ont la **valeur null**.

Les étapes suivantes décrivent l’initialisation unique synchrone qui utilise une fonction de rappel.

1.  Le premier thread à appeler avec succès la fonction [**InitOnceExecuteOnce**](/windows/win32/api/synchapi/nf-synchapi-initonceexecuteonce) passe un pointeur vers une fonction de rappel [*InitOnceCallback*](/windows/win32/api/synchapi/nc-synchapi-pinit_once_fn) définie par l’application et toutes les données requises par la fonction de rappel. Si l’appel réussit, la fonction de rappel *InitOnceCallback* s’exécute.
2.  Les threads suivants qui tentent d’effectuer une initialisation sont bloqués jusqu’à ce que le premier thread ait terminé l’initialisation ou échoue. Si le premier thread échoue, le thread suivant est autorisé à tenter l’initialisation, et ainsi de suite.
3.  Une fois l’initialisation terminée, la fonction de rappel retourne. La fonction de rappel peut éventuellement créer un objet de synchronisation (ou d’autres données de contexte) et la spécifier dans son paramètre de sortie *Context* .
4.  Si l’initialisation est réussie, l’état de la structure d’initialisation à usage unique est remplacé par Initialized et le handle de *contexte* (le cas échéant) est stocké dans la structure d’initialisation. Les tentatives d’initialisation suivantes retournent ces données de contexte. Si l’initialisation échoue, les données ont la **valeur null**.

## <a name="asynchronous-one-time-initialization"></a>Initialisation unique asynchrone

Les étapes suivantes décrivent l’initialisation unique asynchrone.

1.  Si plusieurs threads tentent simultanément de commencer l’initialisation en appelant [**InitOnceBeginInitialize**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize) avec **init \_ une fois \_ Async**, la fonction parvient à tous les threads avec le paramètre *fPending* défini sur **true**. Un seul thread parviendra en fait au moment de l’initialisation. les autres tentatives simultanées ne modifient pas l’état d’initialisation.
2.  Quand [**InitOnceBeginInitialize**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize) retourne, le paramètre *fPending* indique l’état d’initialisation :
    -   Si *fPending* a la **valeur false**, un thread a réussi à s’initialiser. Les autres threads doivent nettoyer les données de contexte qu’ils ont créées et utiliser les données de contexte dans le paramètre de sortie *lpContext* de [**InitOnceBeginInitialize**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize).
    -   Si *fPending* a la **valeur true**, l’initialisation n’est pas encore terminée et les autres threads doivent continuer.
3.  Chaque thread appelle la fonction [**InitOnceComplete**](/windows/win32/api/synchapi/nf-synchapi-initoncecomplete) . Le thread peut éventuellement créer un objet de synchronisation (ou d’autres données de contexte) et le spécifier dans le paramètre *lpContext* de **InitOnceComplete**.
4.  Quand [**InitOnceComplete**](/windows/win32/api/synchapi/nf-synchapi-initoncecomplete) retourne, sa valeur de retour indique si le thread appelant a réussi lors de l’initialisation.
    -   Si [**InitOnceComplete**](/windows/win32/api/synchapi/nf-synchapi-initoncecomplete) réussit, le thread appelant a réussi lors de l’initialisation. L’état de la structure d’initialisation à usage unique est remplacé par Initialized et le handle *lpContext* (le cas échéant) est stocké dans la structure d’initialisation.
    -   Si [**InitOnceComplete**](/windows/win32/api/synchapi/nf-synchapi-initoncecomplete) échoue, un autre thread a réussi à s’initialiser. Le thread appelant doit nettoyer toutes les données de contexte qu’il a créées et appeler [**InitOnceBeginInitialize**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize) à l’aide de la fonction **init \_ une fois la \_ vérification \_ uniquement** pour récupérer les données de contexte stockées dans la structure d’initialisation à usage unique.

## <a name="calling-one-time-initialization-from-multiple-sites"></a>Appel One-Time l’initialisation à partir de plusieurs sites

Une initialisation unique protégée par une seule structure **init \_** unique peut être effectuée à partir de sites multiples ; un rappel différent peut être passé à partir de chaque site, et la synchronisation avec et sans rappel peut être mélangée. L’initialisation est toujours garantie pour exécuter sucesfully une seule fois.

Toutefois, l’initialisation asynchrone et synchrone ne peut pas être mixte : une fois l’initialisation asynchrone tentée, les tentatives de démarrage de l’initialisation synchrone échouent.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de One-Time initialisation](using-one-time-initialization.md)
</dt> </dl>

 

 
