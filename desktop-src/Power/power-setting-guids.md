---
description: Les GUID des paramètres d’alimentation identifient les événements de changement d’alimentation.
ms.assetid: 39D432A7-54F8-4135-B98C-7290F95B054A
title: GUID des paramètres d’alimentation (Winnt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b05909509e0c3ed581582ebe90b10e5df4e91a31b7ab050b3fd1ef6679b1a3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887029"
---
# <a name="power-setting-guids"></a>GUID des paramètres d’alimentation

Les **GUID** des paramètres d’alimentation identifient les événements de changement d’alimentation. Cette rubrique répertorie les **GUID** des paramètres d’alimentation pour les notifications les plus utiles pour les applications. Une application doit s’inscrire à chaque événement de changement d’alimentation qui peut avoir un impact sur son comportement. La notification est envoyée chaque fois qu’un paramètre change.

Les **GUID** des paramètres d’alimentation sont définis dans Winnt. h.

<dl> <dt>

<span id="GUID_ACDC_POWER_SOURCE"></span><span id="guid_acdc_power_source"></span>**\_ \_ source d’alimentation du GUID ACDC \_**
</dt> <dd> <dl> <dt>

5D3E9A59-E9D5-4B00-A6BD-FF34FF516548
</dt> <dt>



La source d’alimentation du système a changé. Le membre de **données** est une **valeur DWORD** avec les valeurs de l’énumération des [**\_ \_ conditions d’alimentation du système**](/windows/desktop/api/WinNT/ne-winnt-system_power_condition) qui indiquent la source d’alimentation actuelle.

<dl> <dt>

**PoAc** (0) : l’ordinateur est alimenté par une source d’alimentation secteur (ou similaire, par exemple un ordinateur portable équipé d’un adaptateur d’automobile 12V).
</dt> <dt>

**PoDc** (1) : l’ordinateur est alimenté par une source d’alimentation de batterie intégrée.
</dt> <dt>

**PoHot** (2) : l’ordinateur est alimenté par une source d’alimentation à faible terme, par exemple un appareil UPS.
</dt> </dl>

</dl> </dd> <dt>

<span id="GUID_BATTERY_PERCENTAGE_REMAINING"></span><span id="guid_battery_percentage_remaining"></span>**pourcentage de batterie du GUID \_ \_ \_ restant**
</dt> <dd> <dl> <dt>

A7AD8041-B45A-4CAE-87A3-EECBB468A9E1
</dt> <dt>



La capacité restante de la batterie a changé. La granularité varie d’un système à l’autres, mais la granularité la plus fine est de 1%. Le membre de **données** est une **valeur DWORD** qui indique la capacité actuelle de la batterie restante en pourcentage compris entre 0 et 100.


</dt> </dl> </dd> <dt>

<span id="GUID_CONSOLE_DISPLAY_STATE"></span><span id="guid_console_display_state"></span>**État d’affichage de la \_ console GUID \_ \_**
</dt> <dd> <dl> <dt>

6FE69556-704A-47A0-8F24-C28D936FDA47
</dt> <dt>



L’état d’affichage de l’analyseur actuel a changé.

**Windows 7, Windows server 2008 R2, Windows Vista et Windows server 2008 :** cette notification est disponible à partir de Windows 8 et Windows Server 2012.

Le membre de **données** est une **valeur DWORD** avec l’une des valeurs suivantes.

<dl> <dt>

0x0-l’affichage est désactivé.
</dt> <dt>

0x1 : l’affichage est activé.
</dt> <dt>

0X2-l’affichage est grisé.
</dt> </dl>

</dl> </dd> <dt>

<span id="GUID_GLOBAL_USER_PRESENCE"></span><span id="guid_global_user_presence"></span>**\_présence globale de l' \_ utilisateur GUID \_**
</dt> <dd> <dl> <dt>

786E8A1D-B427-4344-9207-09E70BDCBEA9
</dt> <dt>



L’état de l’utilisateur associé à n’importe quelle session a changé. Cela représente l’état combiné de la présence de l’utilisateur sur toutes les sessions locales et distantes sur le système.

Cette notification est envoyée uniquement aux services et autres programmes s’exécutant dans la session 0. Les applications en mode utilisateur doivent s’inscrire à la présence d’un **\_ utilisateur de session \_ \_ GUID** à la place.

**Windows 7, Windows server 2008 R2, Windows Vista et Windows server 2008 :** cette notification est disponible à partir de Windows 8 et Windows Server 2012.

Le membre de **données** est une **valeur DWORD** avec l’une des valeurs suivantes.

<dl> <dt>

**PowerUserPresent** (0)-l’utilisateur est présent dans une session locale ou distante sur le système.
</dt> <dt>

**PowerUserInactive** (2)-l’utilisateur n’est pas présent dans une session locale ou distante sur le système.
</dt> </dl>

</dl> </dd> <dt>

<span id="GUID_IDLE_BACKGROUND_TASK"></span><span id="guid_idle_background_task"></span>**\_tâche en \_ arrière-plan du GUID inactif \_**
</dt> <dd> <dl> <dt>

515C31D8-F734-163D-A0FD-11A08C91E8F1
</dt> <dt>



Le système est occupé. Cela indique que le système ne passera pas dans un état d’inactivité dans un avenir proche et que l’heure actuelle est un bon moment pour que les composants exécutent des tâches d’arrière-plan ou inactives qui pourraient empêcher l’ordinateur d’entrer dans un état d’inactivité.

Il n’y a aucune notification lorsque le système est en mesure de passer à un état d’inactivité. La notification de tâche en arrière-plan Idle n’indique pas si un utilisateur est présent sur l’ordinateur. Les **données** membres n’ont pas d’informations et peuvent être ignorées.


</dt> </dl> </dd> <dt>

<span id="GUID_MONITOR_POWER_ON"></span><span id="guid_monitor_power_on"></span>**\_mise sous \_ tension \_ du moniteur GUID**
</dt> <dd> <dl> <dt>

02731015-4510-4526-99E6-E5A17EBD1AEA
</dt> <dt>



Le moniteur système principal a été mis sous tension ou hors tension. Cette notification est utile pour les composants qui affichent activement le contenu sur le périphérique d’affichage, comme la visualisation des médias. Ces applications doivent s’inscrire à cette notification et arrêter le rendu du contenu des graphiques lorsque l’analyse est désactivée pour réduire la consommation d’énergie du système. Le membre de **données** est une **valeur DWORD** qui indique l’état actuel de l’analyse.

<dl> <dt>

0x0-l’analyse est désactivée.
</dt> <dt>

0x1-l’analyse est activée.
</dt> </dl>

**Windows 8 et Windows Server 2012 :** Les nouvelles applications doivent utiliser l’état d’affichage de la **\_ console \_ \_ GUID** au lieu de cette notification.

</dl> </dd> <dt>

<span id="GUID_POWER_SAVING_STATUS"></span><span id="guid_power_saving_status"></span>**\_État de \_ l’économie d’énergie GUID \_**
</dt> <dd> <dl> <dt>

E00958C0-C213-4ACE-AC77-FECCED2EEEA5
</dt> <dt>



L’économiseur de batterie a été désactivé ou activé en réponse à la modification des conditions d’alimentation. Cette notification est utile pour les composants qui participent à la conservation de l’énergie. Ces applications doivent s’inscrire à cette notification et économiser de l’énergie lorsque l’économiseur de batterie est activé.

Le membre de **données** est une **valeur DWORD** qui indique l’état de l’économiseur de batterie.

<dl> <dt>

0x0-l’économiseur de batterie est désactivé.
</dt> <dt>

0x1-l’économiseur de batterie est activé. Économisez de l’énergie dans la mesure du possible.
</dt> </dl>

Pour obtenir des informations générales sur l’économiseur de batterie, consultez [économiseur de batterie (dans les instructions relatives aux composants matériels)](/windows-hardware/design/component-guidelines/battery-saver).

</dl> </dd> <dt>

<span id="GUID_POWERSCHEME_PERSONALITY"></span><span id="guid_powerscheme_personality"></span>**POWERSCHEME de GUID \_ \_**
</dt> <dd> <dl> <dt>

245d8541-3943-4422-b025-13A784F679B7
</dt> <dt>



La personnalité active du mode de gestion de l’alimentation a changé. Tous les modes de gestion de l’alimentation sont mappés à l’une de ces personnalités. Le membre de **données** est un **GUID** qui indique la nouvelle personnalité active du mode de gestion de l’alimentation.

<dl> <dt>



**GUID \_ \_ \_ Économie d’énergie minimale** (8C5E7FDA-E8BF-4A96-9A85-A6E23A8C635C)

Hautes performances : le schéma est conçu pour offrir des performances maximales au détriment des économies de la consommation énergétique.


</dt> <dt>



**GUID \_ \_ \_ Économies d’énergie max** . (A1841308-3541-4FAB-BC81-F71556F20B4A)

Économiseur d’énergie : le schéma est conçu pour offrir des économies d’énergie maximales au détriment des performances et de la réactivité du système.


</dt> <dt>



**GUID \_ \_ \_ Économie d’énergie classique** (381B4222-F694-41F0-9685-FF5BB260DF2E)

Automatique-le schéma est conçu pour équilibrer automatiquement les performances et les économies de consommation énergétique.


</dt> </dl>

</dl> </dd> <dt>

<span id="GUID_SESSION_DISPLAY_STATUS"></span><span id="guid_session_display_status"></span>**État d’affichage de la \_ session GUID \_ \_**
</dt> <dd> <dl> <dt>

2B84C20E-AD23-4ddf-93DB-05FFBD7EFCA5
</dt> <dt>



L’affichage associé à la session de l’application a été activé ou désactivé.

**Windows 7, Windows server 2008 R2, Windows Vista et Windows server 2008 :** cette notification est disponible à partir de Windows 8 et Windows Server 2012.

Cette notification est envoyée uniquement aux applications en mode utilisateur. Les services et autres programmes s’exécutant dans la session 0 ne reçoivent pas cette notification. Le membre de **données** est une **valeur DWORD** avec l’une des valeurs suivantes.

<dl> <dt>

0x0-l’affichage est désactivé.
</dt> <dt>

0x1 : l’affichage est activé.
</dt> <dt>

0X2-l’affichage est grisé.
</dt> </dl>

</dl> </dd> <dt>

<span id="GUID_SESSION_USER_PRESENCE"></span><span id="guid_session_user_presence"></span>**présence d’un \_ utilisateur de session GUID \_ \_**
</dt> <dd> <dl> <dt>

3C0F4548-C03F-4c4d-B9F2-237EDE686376
</dt> <dt>



L’état de l’utilisateur associé à la session de l’application a changé.

**Windows 7, Windows server 2008 R2, Windows Vista et Windows server 2008 :** cette notification est disponible à partir de Windows 8 et Windows Server 2012.

Cette notification est envoyée uniquement aux applications en mode utilisateur qui s’exécutent dans une session interactive. Les services et autres programmes en cours d’exécution dans la session 0 doivent s’inscrire à la **\_ \_ \_ présence globale de l’utilisateur GUID**. Le membre de **données** est une **valeur DWORD** avec l’une des valeurs suivantes.

<dl> <dt>

**PowerUserPresent** (0)-l’utilisateur fournit une entrée à la session.
</dt> <dt>

**PowerUserInactive** (2)-le délai d’attente de l’activité de l’utilisateur s’est écoulé sans interaction de l’utilisateur.
</dt> </dl>

> [!Note]  
> Toutes les applications qui s’exécutent dans une session interactive en mode utilisateur doivent utiliser ce paramètre. Lorsque les applications en mode noyau s’inscrivent pour surveiller l’État, elles doivent utiliser l’état d’affichage de la **\_ console \_ \_ GUID** à la place.

 

</dl> </dd> <dt>

<span id="GUID_SYSTEM_AWAYMODE"></span><span id="guid_system_awaymode"></span>**\_mode absence système \_ GUID**
</dt> <dd> <dl> <dt>

98A7F580-01F7-48AA-9C0F-44352C29E5C0
</dt> <dt>



Le système est en cours d’entrée ou de sortie. Le membre de **données** est une **valeur DWORD** qui indique l’état actuel du mode absence.

<dl> <dt>

0x0-l’ordinateur quitte le mode away.
</dt> <dt>

0x1-l’ordinateur entre en mode absence.
</dt> </dl>

</dl> </dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Winnt. h</dt> </dl> |



 

