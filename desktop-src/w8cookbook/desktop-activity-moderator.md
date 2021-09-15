---
title: Modérateur de l’activité du Bureau
description: Modérateur de l’activité du Bureau
ms.assetid: F1C54DB0-0AFC-4A1B-9697-6CEB519C2663
keywords:
- autonomie de la batterie
- veille connectée
- suspendu
- limitation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b8bb3d7925633d3feca8bb6ed5af191670af681
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127312834"
---
# <a name="desktop-activity-moderator"></a>Modérateur de l’activité du Bureau

## <a name="platform"></a>Plateforme

**Clients** – Windows 8 


> [!Note]  
> le DAM est présent uniquement sur les ordinateurs clients Windows 8 qui prennent en charge la veille connectée. Le DAM n’est pas présent sur les références de serveur.

 

  

> [!Note]  
> Windows les applications du Store générées pour des Windows 8 ne sont pas affectées par la mère.

 

  
</dl>

## <a name="description"></a>Description

Nos clients se déplacent vers des plates-formes plus légères, plus petites et plus mobiles pour répondre à leurs besoins informatiques. Dans le cadre de l’évolution des appareils mobiles, les utilisateurs s’inquiètent de plus en plus sur la durée de vie de la batterie de leurs appareils. le modérateur de l’activité du bureau (DAM) est l’une des nombreuses nouvelles fonctionnalités de Windows 8 conçues pour garantir une autonomie de batterie longue et cohérente pour les appareils qui prennent en charge la veille connectée.

La mise en veille connectée se produit lorsque l’appareil est sous tension, mais l’écran est désactivé. dans cet état d’alimentation, le système est techniquement toujours « activé » (pour prendre en charge des scénarios clés tels que la messagerie, VoIP, les réseaux sociaux et la messagerie instantanée avec les applications Windows store). Elle est analogue à l’État dans lequel se trouve un smartphone quand l’utilisateur appuie sur le bouton d’alimentation.

En tant que tel, les logiciels (y compris les applications et les logiciels du système d’exploitation) doivent se comporter correctement au cours de la mise en veille connectée. Le DAM a été créé pour supprimer l’exécution de l’application de bureau de manière similaire à l’état de veille (S3 sur les périphériques ACPI). Pour ce faire, il suspend ou limite les processus du logiciel de bureau sur le système en cas d’entrée de veille connectée. cela permet aux systèmes qui prennent en charge la veille connectée de fournir une utilisation réduite des ressources et une durée de vie de batterie longue et cohérente tout en permettant aux applications Windows Store de fournir les expériences connectées qu’elles promettent.

## <a name="details"></a>Détails

Le DAM est un pilote en mode noyau qui est chargé et initialisé au démarrage du système si le système prend en charge la veille connectée. (Cela est déterminé en évaluant si le champ alimentation AOAC du système \_ La \_ structure des capacités d’alimentation retournée par CallNtPowerInformation est définie sur true).

Lorsque la mère est activée et que votre processus de bureau est créé, la mère ajoute votre processus aux objets de travail gérés par le système :

-   Si le processus a été créé dans la session 0, DAM ajoute le processus à un objet de traitement sujet à la **limitation**
-   Si le processus a été créé dans une session interactive (session 1 ou version ultérieure), DAM ajoute le processus à un objet de travail sujet à la **suspension**

> [!Note]  
> par Windows 8, les objets de traitement peuvent être imbriqués. Cela signifie que l’utilisation par le DAM des objets de travail n’interfère pas avec l’utilisation existante d’objets de travail d’une application.

 

Lorsque l’écran est allumé, la mère est désactivée et n’a aucun impact sur les processus du système. Lorsque le système est en veille connectée, en fonction de l’activité sur le système, DAM peut limiter ou suspendre des processus.

-   Les processus qui sont soumis à la suspension ont tous leurs threads suspendus (ne sont pas autorisés à s’exécuter dans toutes les circonstances); l’état de l’application (mémoire de processus) est conservé
-   Les processus soumis à un cycle de limitation entre suspendu et non suspendu (une grande majorité du temps est passé à l’état suspendu)
    -   n’oubliez pas que Windows pouvez également détecter les activités critiques en cours et peut annuler l’interruption des services limités pendant des périodes plus longues pendant cette activité.
    -   Notez également qu’en mode veille connectée, les capteurs et les réseaux peuvent ne pas être disponibles. par conséquent, les processus limités doivent être conçus pour être résilients à des conditions réseau médiocres (pour la plupart des processus, cela ne nécessite aucune modification)

Lorsque la suspension de la mère est engagée ou désactivée, DAM déclenche la remise d’un \_ message WM POWERBROADCAST aux processus soumis à la suspension qui a opté pour la remise des messages (via un appel d’API ou un shim de compatibilité, décrit plus loin). Après quelques secondes, DAM interrompt le processus.

Il n’y a aucune notification lorsque la limitation de la mère est engagée ou désactivée. Les processus ne doivent pas être modifiés ; les processus continuent à fonctionner, même si leur vitesse est plus lente.

## <a name="manifestation"></a>Manifestation

Les processus sont souvent suspendus ou limités pendant l’état de veille connectée. Pour la majorité des applications suspendues, cette valeur doit être très similaire à une transition S3/reprise ou mise en veille/reprise S4. Les manifestes peuvent inclure, mais ne sont pas limités à des incohérences dans le temps d’activité/Runtime par rapport à l’heure de la paroi, les incohérences dans le comportement de la minuterie ou les modifications spectaculaires de l’état du système d’exploitation avant et après la fin de la suspension.

La suspension et la limitation se produisent en tant qu’unité (tous les processus suspendus sont suspendus et ne sont pas suspendus, et tous les processus qui peuvent être limités sont limités et non accélérés), de sorte que la communication entre deux processus interrompus ou deux processus limités ne pose pas de problème.

Les logiciels qui s’appuient sur la communication entre processus peuvent nécessiter une attention particulière :

-   **Communication entre les processus dans la session 0 (limitée) et la session 1 + (suspendu)** : exemples : icônes de la barre d’État ou composants de l’interface utilisateur représentant l’état actuel du service
-   **Communication entre les composants en mode utilisateur (session 0 ou 1) et les pilotes (qui ne sont ni limités ni suspendus) : les** exemples incluent des services qui fonctionnent pour le compte d’un pilote

Dans ce cas, si la communication entre processus n’est pas gérée correctement, les applications peuvent apparaître bloquées ou ne pas répondre (bien que l’utilisateur ne puisse pas voir cet impact directement, car l’écran est désactivé en mode veille connectée). Dans la plupart des cas, toutefois, les services et les pilotes doivent déjà être développés pour être robustes contre les problèmes de communication entre processus.

Les fournisseurs qui créent des logiciels pour, ou dépendants du Web, doivent réfléchir à la manière dont la suspension de processus affecte les durées de vie et les négociations de connexion. En outre, étant donné que la connectivité réseau peut ne pas être disponible en mode de veille connectée, les développeurs de processus créés dans la session 0 doivent être particulièrement conscients de la façon dont les connexions réseau intermittentes affectent le processus.

## <a name="solution"></a>Solution

Windows Les applications du Store ne sont pas affectées par la mère. Si votre application de bureau est affectée par la mère, vous pouvez demander des notifications avant que la suspension soit engagée (par exemple, pour enregistrer l’État ou fermer les connexions réseau) à l’aide de l’une des méthodes suivantes :

-   Si votre application a une fenêtre (HWND) et que vous souhaitez gérer ces notifications par le biais de votre procédure de fenêtre, appelez [RegisterSuspendResumeNotification](/windows/win32/api/winuser/nf-winuser-registersuspendresumenotification) pour vous inscrire pour ces messages (ou [UnregisterSuspendResumeNotification](/windows/win32/api/winuser/nf-winuser-unregistersuspendresumenotification) pour annuler l’inscription). Vous pouvez utiliser \_ \_ le handle de fenêtre de notification d’appareil \_ dans le paramètre flags et passer le HWND de votre fenêtre dans en tant que paramètre Recipient. Le message received est le \_ message WM POWERBROADCAST.
-   Si votre application n’a pas de fenêtre (HWND) ou si vous souhaitez un rappel direct, appelez [PowerRegisterSuspendResumeNotification](/windows/win32/api/powerbase/nf-powerbase-powerregistersuspendresumenotification) pour vous inscrire à ces messages (ou [PowerUnregisterSuspendResumeNotification](/windows/win32/api/powerbase/nf-powerbase-powerunregistersuspendresumenotification) pour annuler l’inscription). Vous devez utiliser \_ \_ le rappel de notification de l’appareil dans le paramètre flags et passer une valeur de type PDEVICE \_ notifier \_ \_ les paramètres d’abonnement dans le paramètre Recipient.
-   Si votre application ne peut pas être recompilée, vous pouvez choisir de recevoir ces \_ messages WM POWERBROADCAST via la [boîte à outils AppCompat](../win7appqual/application-compatibility-toolkit--act-.md) (à l’aide du shim PromoteDAM).

Le message d’interruption est WM \_ POWERBROADCAST avec wParam = PBT \_ APMSUSPEND ; ce message est diffusé simultanément pour tous les processus sur le système. Votre application doit effectuer un travail sur le chemin d’interruption rapidement et efficacement. Le délai d’attente après la notification de diffusion est global et non par processus. par conséquent, votre processus peut être en train de faire l’expérience des ressources système si le travail requis dans ce chemin d’accès est important.

Le message Resume est WM \_ POWERBROADCAST avec wParam = PBT \_ APMRESUME ; ce message est diffusé simultanément pour tous les processus activés après une reprise. La durée relative de la livraison à la sortie du système à partir de la veille connectée n’est pas garantie.

Pour les applications associées à l’appareil photo, lorsque la transition de l’état d’alimentation a lieu, pendant la notification de suspension, les applications doivent libérer toutes les références à l’appareil photo (tous les objets de pipeline de capture doivent être arrêtés et supprimés).  pour éviter l’épuisement possible de la batterie, sur Windows 10 RS3 + systems Caméra Windows service du serveur de frames ferme toutes les sessions de capture si l’application ne gère pas correctement la notification de suspension.  L’effet secondaire est que lorsque le système sort de l’état de veille ou S3/S4, le pipeline de capture de l’application n’est plus en état de fonctionnement.

## <a name="tests"></a>Tests

Testez vos logiciels sur les transitions de veille connectée.

## <a name="resources"></a>Ressources

-   [Solutions de durée de vie des batteries Mobile pour Windows 7](/previous-versions/windows/hardware/design/dn641606(v=vs.85))
-   [\_capacités d’alimentation du système \_](/windows/win32/api/winnt/ns-winnt-system_power_capabilities)
-   [CallNtPowerInformation fonction)](/windows/win32/api/powerbase/nf-powerbase-callntpowerinformation)
-   [Objets de traitement](../procthread/job-objects.md)
-   [RegisterSuspendResumeNotification](/windows/win32/api/winuser/nf-winuser-registersuspendresumenotification)
-   [UnregisterSuspendResumeNotification](/windows/win32/api/winuser/nf-winuser-unregistersuspendresumenotification)
-   [PowerRegisterSuspendResumeNotification](/windows/win32/api/powerbase/nf-powerbase-powerregistersuspendresumenotification)
-   [PowerUnregisterSuspendResumeNotification](/windows/win32/api/powerbase/nf-powerbase-powerunregistersuspendresumenotification)
-   [Boîte à outils AppCompat](../win7appqual/application-compatibility-toolkit--act-.md)

 

 