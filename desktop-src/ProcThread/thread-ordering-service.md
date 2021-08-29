---
description: Le service de classement des threads contrôle l’exécution d’un ou plusieurs threads clients. Il garantit que chaque thread client s’exécute une fois pendant la période spécifiée et dans l’ordre relatif.
ms.assetid: 5c37873a-ced4-447e-a6e1-55cfa8ab24b4
title: Service de classement des threads
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 726f846f390f6ef3c586a4798374b41494b18b11371dd363e27fddc838a18049
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127999"
---
# <a name="thread-ordering-service"></a>Service de classement des threads

Le *service de classement des threads* contrôle l’exécution d’un ou plusieurs threads clients. Il garantit que chaque thread client s’exécute une fois pendant la période spécifiée et dans l’ordre relatif.

**Windows Server 2003 et Windows XP :** le service de classement des threads est disponible à partir de Windows Vista et Windows Server 2008.

Le service de classement des threads est désactivé par défaut et doit être démarré par l’utilisateur. Pendant que le service de classement des threads est en cours d’exécution, il est activé toutes les 5 secondes pour vérifier s’il existe une nouvelle demande, même si le système est inactif. Cela empêche le système de se mettre en veille pendant plus de 5 secondes, ce qui a pour effet de consommer davantage d’énergie. Si l’efficacité énergétique est essentielle pour l’application, il est préférable de ne pas utiliser le service de classement des threads et d’autoriser à la place le planificateur système à gérer l’exécution des threads.

Chaque thread client appartient à un *groupe d’ordonnancement des threads*. Le *thread parent* crée un ou plusieurs groupes d’ordonnancement de thread en appelant la fonction [**AvRtCreateThreadOrderingGroup**](/windows/desktop/api/Avrt/nf-avrt-avrtcreatethreadorderinggroup) . Le thread parent utilise cette fonction pour spécifier la période pour le groupe d’ordonnancement de thread et un intervalle de délai d’attente.

Des threads clients supplémentaires appellent la fonction [**AvRtJoinThreadOrderingGroup**](/windows/desktop/api/Avrt/nf-avrt-avrtjointhreadorderinggroup) pour joindre un groupe d’ordonnancement de thread existant. Ces threads indiquent s’ils doivent être un prédécesseur ou un successeur du thread parent dans l’ordre d’exécution. Chaque thread client est censé effectuer une certaine quantité de traitement chaque période. Tous les threads du groupe doivent exécuter leur exécution dans la période plus l’intervalle de délai d’attente.

Les threads d’un groupe d’ordonnancement de threads encadrent leur code de traitement dans une boucle contrôlée par la fonction [**AvRtWaitOnThreadOrderingGroup**](/windows/desktop/api/Avrt/nf-avrt-avrtwaitonthreadorderinggroup) . Tout d’abord, les threads prédécesseurs sont exécutés un par un, dans l’ordre dans lequel ils ont rejoint le groupe, tandis que les threads parents et successeurs sont bloqués lors de leurs appels à **AvRtWaitOnThreadOrderingGroup**. Lorsque chaque thread prédécesseur a fini son traitement, le contrôle de l’exécution retourne au sommet de sa boucle de traitement et le thread appelle à nouveau **AvRtWaitOnThreadOrderingGroup** pour se bloquer jusqu’à son tour suivant. Une fois que tous les threads précédents ont appelé cette fonction, le service de classement des threads peut planifier le thread parent. Enfin, lorsque le thread parent termine son traitement et appelle à nouveau **AvRtWaitOnThreadOrderingGroup** , le service de classement des threads peut planifier les threads successeurs un par un dans l’ordre dans lequel ils ont rejoint le groupe. Si tous les threads terminent leur exécution avant la fin d’une période, tous les threads attendent jusqu’à ce que le reste de la période s’arrête avant que les autres soient exécutés à nouveau.

Lorsque le client n’a plus besoin de s’exécuter dans le cadre du groupe d’ordonnancement des threads, il appelle la fonction [**AvRtLeaveThreadOrderingGroup**](/windows/desktop/api/Avrt/nf-avrt-avrtleavethreadorderinggroup) pour se supprimer du groupe. Notez que le thread parent ne doit pas se supprimer lui-même d’un groupe d’ordonnancement des threads. Si un thread ne termine pas son exécution avant que le délai n’expire, il est supprimé du groupe.

Le thread parent appelle la fonction [**AvRtDeleteThreadOrderingGroup**](/windows/desktop/api/Avrt/nf-avrt-avrtdeletethreadorderinggroup) pour supprimer le groupe d’ordonnancement des threads. Le groupe d’ordonnancement des threads est également détruit si le thread parent n’effectue pas son exécution avant le délai écoulé. Lorsque le groupe d’ordonnancement des threads est détruit, tous les appels à [**AvRtWaitOnThreadOrderingGroup**](/windows/desktop/api/Avrt/nf-avrt-avrtwaitonthreadorderinggroup) à partir de threads de ce groupe échouent ou expirent.

 

 



