---
description: Control Flow Guard (CFG) est une fonctionnalité de sécurité de plateforme hautement optimisée qui a été créée pour combattre les vulnérabilités d’altération de la mémoire.
ms.assetid: 116EAD64-7CAE-455C-BA43-9492F78DE873
title: Control Flow Guard
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62186a86f821e7eb350381c7dfbc500c80dd040f4321a8f630c7d408937a8460
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119622816"
---
# <a name="control-flow-guard"></a>Control Flow Guard

## <a name="what-is-control-flow-guard"></a>qu’est-ce que Control Flow Guard ?

Control Flow Guard (CFG) est une fonctionnalité de sécurité de plateforme hautement optimisée qui a été créée pour combattre les vulnérabilités d’altération de la mémoire. En plaçant des restrictions strictes sur l’emplacement à partir duquel une application peut exécuter du code, il est beaucoup plus difficile pour les attaques d’exécuter du code arbitraire par le biais de vulnérabilités telles que les débordements de mémoire tampon. CFG étend les technologies d’atténuation des vulnérabilités précédentes telles que [/GS](/cpp/build/reference/gs-buffer-security-check?view=vs-2019), [DEP](../memory/data-execution-prevention.md)et [ASLR](/archive/blogs/michael_howard/address-space-layout-randomization-in-windows-vista).

cette fonctionnalité est disponible dans Microsoft Visual Studio 2015 et s’exécute sur les versions « compatibles CFG » de Windows, les versions x86 et x64 pour les ordinateurs de bureau et les serveurs de Windows 10 et de Mise à jour Windows 8.1 (KB3000850).

Nous encourageons vivement les développeurs à activer CFG pour leurs applications. Vous n’avez pas besoin d’activer CFG pour chaque partie de votre code, car une combinaison de CFG est activée et le code non activé par CFG s’exécute parfaitement. Toutefois, l’activation de CFG pour l’ensemble du code peut entraîner des lacunes dans la protection. en outre, le code cfg activé fonctionne correctement sur les versions « ne connaissant pas cfg » de Windows et est donc entièrement compatible avec eux.

## <a name="how-can-i-enable-cfg"></a>Comment activer CFG ?

Dans la plupart des cas, il est inutile de modifier le code source. il vous suffit d’ajouter une option à votre projet Visual Studio 2015, et le compilateur et l’éditeur de liens activent CFG.

la méthode la plus simple consiste à accéder à **Project \| propriétés Configuration propriétés de la génération de \| \| \| Code C/C++** et à choisir **oui (/guard : cf)** pour le contrôle Flow guard.

![propriété cfg dans Visual Studio](images/cfg-vs.png)

vous pouvez également ajouter **/guard : cf** pour **Project \| propriétés \| configuration propriétés \| \| \| options supplémentaires de la ligne de commande c/C++** (pour le compilateur) et **/guard : cf** pour Project propriétés propriétés de **\| \| configuration \| \| \| options supplémentaires** de la ligne de commande de l’éditeur de liens (pour l’éditeur de liens).

![propriété cfg pour le compilateur](images/cfg-compiler.png)![propriété cfg pour l’éditeur de liens](images/cfg-linker.png)

pour plus d’informations, consultez [/guard (activer le contrôle Flow guard)](/cpp/build/reference/guard-enable-control-flow-guard?view=vs-2019) .

Si vous générez votre projet à partir de la ligne de commande, vous pouvez ajouter les mêmes options. Par exemple, si vous compilez un projet appelé test. cpp, utilisez **CL/Guard : cf test. cpp/Link/Guard : cf**.

Vous avez également la possibilité de contrôler dynamiquement l’ensemble des adresses cibles iCal qui sont considérées comme valides par CFG à l’aide de [**SetProcessValidCallTargets**](/windows/desktop/api/memoryapi/nf-memoryapi-setprocessvalidcalltargets) de l’API de gestion de la mémoire. La même API peut être utilisée pour spécifier si les pages sont des cibles non valides ou valides pour CFG. Les fonctions [**VirtualProtect**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualprotect) et [**VirtualAlloc**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc) traitent par défaut une région spécifiée de pages exécutables et validées comme cibles d’appel indirect valides. Il est possible de substituer ce comportement, par exemple lors de l’implémentation d’un compilateur juste-à-temps, en spécifiant des **cibles de page \_ \_ non valides** lors de l’appel de **VirtualAlloc** ou des **cibles de page \_ \_ aucune \_ mise à jour** lors de l’appel de **VirtualProtect** comme détaillé sous [**constantes de protection**](/windows/desktop/Memory/memory-protection-constants)de la mémoire.

## <a name="how-do-i-tell-that-a-binary-is-under-control-flow-guard"></a>comment puis-je savoir qu’un fichier binaire est sous contrôle Flow Guard ?

exécutez l' [outil dumpbin](/cpp/build/reference/dumpbin-reference) (inclus dans l’installation Visual Studio 2015) à partir de l’invite de commandes Visual Studio avec les options */headers* et */loadconfig* : **dumpbin/headers/loadconfig test.exe**. La sortie d’un binaire sous CFG doit indiquer que les valeurs d’en-tête incluent « Guard », et que les valeurs de la configuration de chargement incluent « instrumentation CF » et « table FID présente ».

![sortie de dumpbin/headers](images/cfg-dumpbin-headers.png)

![sortie de DUMPBIN/loadConfig](images/cfg-dumpbin-loadconfig.png)

## <a name="how-does-cfg-really-work"></a>Comment CFG fonctionne-t-il vraiment ?

Les vulnérabilités logicielles sont souvent exploitées en fournissant des données peu probables, inhabituelles ou extrêmes à un programme en cours d’exécution. Par exemple, une personne malveillante peut exploiter une vulnérabilité de débordement de mémoire tampon en fournissant plus d’entrées à un programme que prévu, ce qui a pour effet de surExécuter la zone réservée par le programme pour contenir une réponse. Cela peut corrompre la mémoire adjacente qui peut contenir un pointeur de fonction. Quand le programme appelle par le biais de cette fonction, il peut alors accéder à un emplacement non souhaité spécifié par l’attaquant.

Toutefois, une combinaison puissante de prise en charge de compilation et d’exécution à partir de CFG implémente l’intégrité du workflow de contrôle qui restreint étroitement les endroits où les instructions d’appel indirect peuvent s’exécuter.

Le compilateur effectue les opérations suivantes :

1.  Ajoute des vérifications de sécurité légères au code compilé.
2.  Identifie l’ensemble des fonctions de l’application qui sont des cibles valides pour les appels indirects.

la prise en charge du runtime, fournie par le noyau du Windows :

1.  Gère efficacement l’État qui identifie les cibles d’appel indirectes valides.
2.  Implémente la logique qui vérifie qu’une cible d’appel indirect est valide.

Pour illustrer ce qui suit :

![Pseudo-code cfg](images/cfg-pseudocode.jpg)

lorsqu’une vérification de CFG échoue au moment de l’exécution, Windows met immédiatement fin au programme, ce qui rompt toute attaque qui tente d’appeler indirectement une adresse non valide.

 

 
