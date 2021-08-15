---
description: Les variables de condition sont des primitives de synchronisation qui autorisent les threads à attendre qu’une condition particulière se produise. Les variables de condition sont des objets en mode utilisateur qui ne peuvent pas être partagés entre les processus.
ms.assetid: fef9bab0-cd69-4812-869a-b43a10772d86
title: Variables de condition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed05d7ee98b4f5c5a65e633f7d1647b6c624840f9740efb639959c1500bec591
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118886359"
---
# <a name="condition-variables"></a>Variables de condition

Les variables de condition sont des primitives de synchronisation qui autorisent les threads à attendre qu’une condition particulière se produise. Les variables de condition sont des objets en mode utilisateur qui ne peuvent pas être partagés entre les processus.

Les variables de condition permettent aux threads de libérer atomiquement un verrou et de passer en état de veille. Ils peuvent être utilisés avec des sections critiques ou des verrous SRW (Slim Reader/Writer). Les variables de condition prennent en charge les opérations « réveiller un » ou « mettre en éveil tous les threads en attente ». Une fois qu’un thread est en éveil, il acquiert à nouveau le verrou libéré lorsque le thread est passé à l’état de veille.

Notez que l’appelant doit allouer une structure de **\_ variable de condition** et l’initialiser en appelant [**InitializeConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-initializeconditionvariable) (pour initialiser la structure de manière dynamique) ou affecter la variable de **condition constante \_ \_ init** à la variable de structure (pour initialiser la structure de manière statique).

**Windows Server 2003 et Windows XP :** Les variables de condition ne sont pas prises en charge.

Les fonctions de variable conditionnelle sont les suivantes.



| Fonction de variable conditionnelle                                        | Description                                                                                                    |
|--------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**InitializeConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-initializeconditionvariable) | Initialise une variable de condition.                                                                              |
| [**SleepConditionVariableCS**](/windows/win32/api/synchapi/nf-synchapi-sleepconditionvariablecs)       | Met en veille la variable de condition spécifiée et libère la section critique spécifiée sous la forme d’une opération atomique. |
| [**SleepConditionVariableSRW**](/windows/win32/api/synchapi/nf-synchapi-sleepconditionvariablesrw)     | Met en veille la variable de condition spécifiée et libère le verrou SRW spécifié sous la forme d’une opération atomique.         |
| [**WakeAllConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-wakeallconditionvariable)       | Sort tous les threads en attente de la variable de condition spécifiée.                                                 |
| [**WakeConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-wakeconditionvariable)             | Veille un thread unique en attente sur la variable de condition spécifiée.                                             |



 

Le pseudo-code suivant illustre le modèle d’utilisation classique des variables de condition.

``` syntax
CRITICAL_SECTION CritSection;
CONDITION_VARIABLE ConditionVar;

void PerformOperationOnSharedData()
{ 
   EnterCriticalSection(&CritSection);

   // Wait until the predicate is TRUE

   while( TestPredicate() == FALSE )
   {
      SleepConditionVariableCS(&ConditionVar, &CritSection, INFINITE);
   }

   // The data can be changed safely because we own the critical 
   // section and the predicate is TRUE

   ChangeSharedData();

   LeaveCriticalSection(&CritSection);

   // If necessary, signal the condition variable by calling
   // WakeConditionVariable or WakeAllConditionVariable so other
   // threads can wake
}
```

Par exemple, dans une implémentation d’un verrou en lecture/écriture, la `TestPredicate` fonction vérifie que la requête de verrou en cours est compatible avec les propriétaires existants. Si c’est le cas, acquérir le verrou ; Sinon, veille. Pour obtenir un exemple plus détaillé, consultez [utilisation de variables de condition](using-condition-variables.md).

Les variables de condition sont soumises à des réveils paraparasites (ceux qui ne sont pas associés à une éveil explicite) et des réveils volés (un autre thread gère pour s’exécuter avant le thread réveill). Par conséquent, vous devez revérifier un prédicat (généralement dans une boucle **while** ) après le retour d’une opération Sleep.

Vous pouvez réveiller d’autres threads à l’aide de [**WakeConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-wakeconditionvariable) ou [**WakeAllConditionVariable**](/windows/win32/api/synchapi/nf-synchapi-wakeallconditionvariable) , à l’intérieur ou à l’extérieur du verrou associé à la variable de condition. Il est généralement préférable de libérer le verrou avant de sortir d’autres threads afin de réduire le nombre de changements de contexte.

Il est souvent pratique d’utiliser plusieurs variables de condition avec le même verrou. Par exemple, une implémentation d’un verrou en lecture/écriture peut utiliser une seule section critique, mais des variables de condition distinctes pour les lecteurs et les enregistreurs.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de variables de condition](using-condition-variables.md)
</dt> </dl>

 

 
