---
description: Un objet de section critique fournit une synchronisation similaire à celle fournie par un objet mutex, à ceci près qu’une section critique ne peut être utilisée que par les threads d’un processus unique.
ms.assetid: 2ec11a42-3d12-4d60-9dd7-dc38926d56e1
title: Objets de section critique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbcada1f2ddbc6d370445f36a3dbd51c5c9f54bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536519"
---
# <a name="critical-section-objects"></a>Objets de section critique

Un *objet de section critique* fournit une synchronisation similaire à celle fournie par un objet mutex, à ceci près qu’une section critique ne peut être utilisée que par les threads d’un processus unique. Les objets de section critique ne peuvent pas être partagés entre plusieurs processus.

Les objets Event, mutex et Semaphore peuvent également être utilisés dans une application à processus unique, mais les objets de section critique offrent un mécanisme plus rapide et plus efficace pour la synchronisation d’exclusion mutuelle (un test spécifique au processeur et une instruction SET). À l’instar d’un objet mutex, un objet de section critique ne peut appartenir qu’à un seul thread à la fois, ce qui le rend utile pour protéger une ressource partagée de l’accès simultané. Contrairement à un objet mutex, il n’existe aucun moyen de savoir si une section critique a été abandonnée.

À compter de Windows Server 2003 avec Service Pack 1 (SP1), les threads en attente d’une section critique n’acquièrent pas la section critique sur une base « premier arrivé, premier servi ». Cette modification augmente considérablement les performances pour la plupart du code. Toutefois, certaines applications dépendent du classement FIFO (premier entré, premier sorti) et peuvent s’exécuter mal ou pas du tout sur les versions actuelles de Windows (par exemple, les applications qui utilisent des sections critiques comme limiteur de débit). Pour vous assurer que votre code continue à fonctionner correctement, vous devrez peut-être ajouter un niveau de synchronisation supplémentaire. Par exemple, supposons que vous ayez un thread de producteur et un thread de consommateur qui utilisent un objet de section critique pour synchroniser leur travail. Créez deux objets d’événement, un pour chaque thread à utiliser pour signaler qu’il est prêt pour que l’autre thread continue. Le thread de consommateur attend que le producteur signale son événement avant d’entrer dans la section critique, et le thread producteur attend que le thread de consommateur signale son événement avant d’entrer dans la section critique. Une fois que chaque thread quitte la section critique, il signale son événement pour libérer l’autre thread.

**Windows Server 2003 et Windows XP :** Les threads qui attendent une section critique sont ajoutés à une file d’attente ; ils sont réveillés et acquièrent généralement la section critique dans l’ordre dans lequel ils ont été ajoutés à la file d’attente. Toutefois, si les threads sont ajoutés à cette file d’attente à un rythme suffisamment rapide, les performances peuvent être dégradées en raison du temps nécessaire pour réveiller chaque thread en attente.

Le processus est chargé d’allouer la mémoire utilisée par une section critique. En règle générale, cette opération est effectuée en déclarant simplement une variable de type **critique \_ section**. Avant que les threads du processus puissent l’utiliser, initialisez la section critique à l’aide de la fonction [**InitializeCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-initializecriticalsection) ou [**InitializeCriticalSectionAndSpinCount**](/windows/win32/api/synchapi/nf-synchapi-initializecriticalsectionandspincount) .

Un thread utilise la fonction [**EnterCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-entercriticalsection) ou [**TryEnterCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-tryentercriticalsection) pour demander la propriété d’une section critique. Elle utilise la fonction [**LeaveCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-leavecriticalsection) pour libérer la propriété d’une section critique. Si l’objet de section critique est actuellement détenu par un autre thread, **EnterCriticalSection** attend indéfiniment de la propriété. En revanche, lorsqu’un objet mutex est utilisé pour l’exclusion mutuelle, les [fonctions Wait](wait-functions.md) acceptent un intervalle de délai d’attente spécifié. La fonction **TryEnterCriticalSection** tente d’entrer dans une section critique sans bloquer le thread appelant.

Quand un thread possède une section critique, il peut effectuer des appels supplémentaires à [**EnterCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-entercriticalsection) ou [**TryEnterCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-tryentercriticalsection) sans bloquer son exécution. Cela empêche un thread de se bloquer lorsqu’il attend une section critique qu’il détient déjà. Pour libérer sa propriété, le thread doit appeler [**LeaveCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-leavecriticalsection) une fois pour chaque fois qu’il a entré la section critique. Il n’existe aucune garantie quant à l’ordre dans lequel les threads en attente acquièrent la propriété de la section critique.

Un thread utilise la fonction [**InitializeCriticalSectionAndSpinCount**](/windows/win32/api/synchapi/nf-synchapi-initializecriticalsectionandspincount) ou [**SetCriticalSectionSpinCount**](/windows/win32/api/synchapi/nf-synchapi-setcriticalsectionspincount) pour spécifier un nombre de spins pour l’objet de section critique. La rotation signifie que lorsqu’un thread essaie d’acquérir une section critique verrouillée, le thread entre dans une boucle, vérifie si le verrou est libéré et, si le verrou n’est pas libéré, le thread passe en mode veille. Sur les systèmes à un seul processeur, le nombre de spins est ignoré et le nombre de spins de la section critique est défini sur 0 (zéro). Sur les systèmes multiprocesseurs, si la section critique n’est pas disponible, le thread appelant tourne *dwSpinCount* fois avant d’effectuer une opération d’attente sur un sémaphore associé à la section critique. Si la section critique devient libre pendant l’opération de rotation, le thread appelant évite l’opération d’attente.

Tout thread du processus peut utiliser la fonction [**DeleteCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-deletecriticalsection) pour libérer les ressources système qui sont allouées lorsque l’objet de section critique est initialisé. Une fois cette fonction appelée, l’objet de section critique ne peut pas être utilisé pour la synchronisation.

Lorsqu’un objet de section critique est détenu, les seuls autres threads affectés sont les threads en attente de propriété dans un appel à [**EnterCriticalSection**](/windows/win32/api/synchapi/nf-synchapi-entercriticalsection). Les threads qui ne sont pas en attente sont libres de continuer à s’exécuter.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Objets mutex](mutex-objects.md)
</dt> <dt>

[Utilisation d’objets de section critique](using-critical-section-objects.md)
</dt> </dl>

 

 
