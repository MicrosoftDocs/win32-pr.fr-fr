---
description: Paramètres de regroupement
ms.assetid: 088156f7-fb75-4fcf-b928-87e97b13bdab
title: Paramètres de regroupement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecfb674d4349f351ce36fe1e236d1ecd3b265d8e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748381"
---
# <a name="grouping-parameters"></a>Paramètres de regroupement

Un paramètre de regroupement identifie une collection de [sessions audio](audio-sessions.md) qui sont toutes contrôlées par un contrôle de volume unique dans le programme de contrôle de volume système, sndvol. Le paramètre GROUPING est un GUID qui identifie de façon unique la collection dans l’étendue de l’ordinateur.

L’objectif d’un paramètre de regroupement est semblable à celui du GUID de session pour une session inter-processus. Autrement dit, le paramètre GROUPING permet à l’utilisateur de contrôler une collection de flux à partir d’un nombre quelconque de processus en tant qu’unité unique. Toutefois, le paramètre de regroupement est utile dans les cas où les sessions inter-processus ne peuvent pas fournir de solution.

Si plusieurs clients attribuent leurs flux respectifs à des sessions distinctes, mais attribuent le même paramètre de regroupement à toutes les sessions, sndvol affiche un contrôle de volume unique pour ces sessions. Pour assurer la prise en charge des paramètres de regroupement, sndvol ou toute application de contrôle de volume similaire doit effectuer les opérations suivantes :

-   Avant d’afficher les contrôles de volume, vérifiez les paramètres de regroupement de toutes les sessions actives. Regroupez sous un seul contrôle de volume toutes les sessions qui ont le même paramètre de regroupement.
-   Lorsque l’utilisateur modifie le paramètre d’un contrôle du volume pour un paramètre de regroupement particulier, mettez à jour les niveaux de volume de toutes les sessions qui partagent ce paramètre de regroupement.

Le regroupement des paramètres permet de réduire le nombre de contrôles de volume affichés par sndvol. Les utilisateurs peuvent être déconcertés si sndvol encombre son affichage avec un trop grand nombre de contrôles. Sans prise en charge des paramètres de regroupement, sndvol afficherait toujours un contrôle de volume distinct pour chaque session, ce qui peut ne pas convenir dans tous les cas. En outre, les paramètres de regroupement offrent un moyen pratique de s’assurer que les sessions qui contiennent des types de contenu audio similaires peuvent être facilement définies sur le même niveau de volume.

Comme expliqué précédemment, les API audio de niveau supérieur attribuent généralement leurs flux à la session par défaut, spécifique au processus (identifiée par la valeur du GUID de session GUID \_ null). Cette valeur par défaut permet à sndvol d’afficher un contrôle de volume distinct pour chaque processus d’application cliente, qui est souvent le comportement souhaité. En outre, si plusieurs instances du même client s’exécutent dans des processus distincts, mais requièrent un seul contrôle de volume partagé, les clients peuvent simplement affecter leurs flux à la même session inter-processus. Aucun de ces cas ne requiert l’utilisation de paramètres de regroupement. Toutefois, un cas important, tel qu’illustré par Microsoft Internet Explorer, requiert l’utilisation de paramètres de regroupement pour obtenir le comportement souhaité.

Internet Explorer permet aux utilisateurs d’ouvrir plusieurs fenêtres de navigateur, et ces fenêtres peuvent ne pas s’exécuter toutes dans le même processus. Les utilisateurs peuvent être déconcertés si sndvol affiche un contrôle de volume distinct pour chaque instance d’application, qui avait la même étiquette, « Internet Explorer ». Une session inter-processus n’est pas une solution faisable dans ce cas. dans ce cas, si plusieurs instances d’Internet Explorer s’exécutent dans des processus différents, elles risquent de ne pas pouvoir attribuer l’ensemble de leurs flux audio à une seule session inter-processus. Cela est dû au fait que les fenêtres Internet Explorer peuvent exécuter des instances du lecteur Windows Media ou d’un autre plug-in multimédia qui utilise une API audio de niveau supérieur pour lire ses flux audio. Ces API attribuent généralement les flux d’un processus à une session par défaut spécifique au processus. Internet Explorer n’a aucun contrôle sur l’affectation de ces flux aux sessions.

WASAPI résout ce problème en permettant à chaque instance d’Internet Explorer d’accéder aux contrôles de session pour sa session par défaut, propre au processus, et d’affecter un paramètre de regroupement à cette session. Si toutes les instances d’Internet Explorer attribuent le même paramètre de regroupement à toutes leurs sessions audio, sndvol affiche un contrôle de volume unique pour ces sessions.

Par défaut, une session n’appartient à aucun regroupement. Si un client n’affecte pas explicitement une session à un regroupement, sndvol affiche un contrôle de volume dédié pour cette session. Le paramètre de regroupement valeur GUID \_ null indique qu’une session n’appartient à aucun regroupement. Si aucun paramètre de regroupement n’a été explicitement affecté à une session pour un client, la valeur du paramètre de regroupement pour cette session est le GUID \_ null par défaut.

Un client peut modifier dynamiquement le regroupement auquel une session est assignée.

Un regroupement peut inclure n’importe quelle combinaison de sessions inter-processus et de sessions spécifiques au processus sur un [périphérique de point de terminaison audio](audio-endpoint-devices.md).

L’interface utilisateur sndvol permet à l’utilisateur d’afficher les contrôles de volume pour un seul périphérique de point de terminaison audio à la fois. Lorsque l’utilisateur ajuste les contrôles de volume pour un périphérique particulier, les niveaux de volume des sessions qui se connectent à d’autres périphériques ne sont pas affectés. En particulier, un contrôle du volume pour un paramètre de regroupement particulier affecte uniquement les sessions qui partagent le paramètre de regroupement et qui sont connectées à l’appareil actuellement sélectionné. Une session qui a un paramètre de regroupement identique mais qui est connectée à un autre appareil n’est pas affectée.

Comme décrit précédemment, sndvol étiquette chaque contrôle de volume qu’il affiche avec un nom d’affichage et une icône. Dans le cas d’un contrôle de volume pour un regroupement, sndvol sélectionne de manière arbitraire l’une des sessions dans le regroupement comme source pour le nom d’affichage et l’icône qu’il affiche avec le contrôle du volume. Ainsi, pour vous assurer que sndvol affiche toujours le même nom complet et l’icône pour un regroupement, toutes les instances d’application qui affectent des sessions à ce regroupement doivent s’assurer que leurs sessions respectives ont le même nom d’affichage et l’icône. Pour plus d’informations sur les noms et les icônes d’affichage, consultez [sessions audio](audio-sessions.md).

Une application telle que sndvol peut s’inscrire pour recevoir des notifications lorsque le paramètre de regroupement d’une session change. Ces notifications peuvent être utiles si l’application met en cache les informations relatives à l’affectation de sessions au regroupement de paramètres. Une notification informe l’application que les informations mises en cache ne sont peut-être plus valides.

Pour assigner un paramètre de regroupement à une session, appelez la méthode [**IAudioSessionControl :: SetGroupingParam**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-setgroupingparam) . Pour obtenir le paramètre de regroupement affecté à une session, appelez la méthode [**IAudioSessionControl :: GetGroupingParam**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-getgroupingparam) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Sessions audio](audio-sessions.md)
</dt> </dl>

 

 



