---
title: Empêcher la déconnexion ou la suspension pendant une gravure
description: Si des précautions appropriées ne sont pas prises au sein d’une application, il est possible qu’un utilisateur se déconnecte pendant une opération de gravure. Cela entraîne l’interruption du processus de gravure, qui peut entraîner la perte de données et éventuellement rendre le disque inutilisable.
ms.assetid: 5223c9f6-30f6-43ce-b46c-267da0a53d4b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8f3dd6980db72854ff65d657cc58730335febcb1dbc8c4a467eedead88f5eab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118977129"
---
# <a name="preventing-logoff-or-suspend-during-a-burn"></a>Empêcher la déconnexion ou la suspension pendant une gravure

Si des précautions appropriées ne sont pas prises au sein d’une application, il est possible qu’un utilisateur se déconnecte pendant une opération de gravure. Cela entraîne l’interruption du processus de gravure, qui peut entraîner la perte de données et éventuellement rendre le disque inutilisable.

Pour éviter ce problème, l’application doit traiter le message [**WM \_ QUERYENDSESSION**](/windows/desktop/Shutdown/wm-queryendsession) qui est remis avant la fermeture de session. Si l’application reçoit ce message lors de l’exécution d’une opération de gravure, retournez **false** pour annuler la procédure de fermeture de session. Si l’application permet à l’utilisateur de décider s’il faut poursuivre la fermeture de session, un avertissement doit s’afficher pour indiquer que l’utilisateur perdra les données.

Les transitions d’alimentation pendant le processus de gravure peuvent également créer des problèmes potentiels dans la réussite d’une activité de gravure. Pour éviter ces complications pendant le processus de gravure, une application doit être consciente lorsque les transitions d’alimentation sont sur le point d’être effectuées. Pour ce faire, il permet à l’application de traiter le message [**WM \_ POWERBROADCAST**](/windows/desktop/Power/wm-powerbroadcast) . les Applications développées pour Windows XP ou Windows Server 2003 peuvent retourner un **\_ \_ refus de requête de diffusion** en réponse à [**PBT \_ APMQUERYSUSPEND**](/windows/desktop/Power/pbt-apmquerysuspend), ce qui empêche l’interruption pendant le processus de gravure.

en raison des modifications apportées au modèle de gestion de l’alimentation pour Windows Vista et Windows Server 2008, l’événement [**PBT \_ APMQUERYSUSPEND**](/windows/desktop/Power/pbt-apmquerysuspend) n’est plus remis aux applications. Au lieu de cela, l’événement [**PBT \_ APMSUSPEND**](/windows/desktop/Power/pbt-apmsuspend) est remis, ce qui permet à une application de se préparer à deux secondes pour la transition.

À la suite de ces modifications, il est recommandé que les applications appellent la fonction [**SetThreadExecutionState**](/windows/desktop/api/winbase/nf-winbase-setthreadexecutionstate) pour empêcher un délai d’inactivité du système, ce qui entraîne généralement une interruption de la transition. Il est important de se souvenir que l’appel de cette fonction avec les indicateurs appropriés définis empêchera uniquement le système inactif, pas une interruption en cours.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation d’IMAPi](using-imapi.md)
</dt> <dt>

[**SetThreadExecutionState**](/windows/desktop/api/winbase/nf-winbase-setthreadexecutionstate)
</dt> </dl>

 

 