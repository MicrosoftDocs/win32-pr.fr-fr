---
title: Sessions enfants
description: À compter de Windows Server 2012 et Windows 8, Bureau à distance prend en charge le concept de session enfant, qui est une session de Bureau à distance de bouclage spéciale qui est liée à la session existante d’un utilisateur.
ms.assetid: 65B9DB67-4EE8-40B5-B465-CA425792C62B
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 788b36bf9799da9b0cb7486963f3154451ca5392
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104190791"
---
# <a name="child-sessions"></a>Sessions enfants

À compter de Windows Server 2012 et Windows 8, Bureau à distance prend en charge le concept de *session enfant*, qui est une session de bureau à distance de bouclage spéciale qui est liée à la session existante d’un utilisateur.

Les sessions enfants ne sont pas prises en charge sur les systèmes d’exploitation suivants :

<dl> Windows RT  
Option d’installation minimale de Windows Server 2012  
Microsoft Hyper-V Server 2012  
</dl>

Un système ne peut avoir qu’une seule session enfant active et connectée à un moment donné.

La session enfant peut être arrêtée en se déconnectant directement de celle-ci, ou elle sera arrêtée lorsque sa session parente se terminera.

Avant de pouvoir utiliser des sessions enfants sur un système, vous devez activer la fonctionnalité de session enfant en appelant la fonction [**WTSEnableChildSessions**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenablechildsessions) . Vous pouvez également déterminer si les sessions enfants ont été activées à l’aide de la fonction [**WTSIsChildSessionsEnabled**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsischildsessionsenabled) .

Une session enfant ne peut être créée qu’à partir d’une session d’utilisateur existante à l’aide du [contrôle ActiveX Bureau à distance](remote-desktop-activex-control.md) et en définissant la propriété « ConnectToChildSession » avec [**IMsRdpExtendedSettings. Property**](imsrdpextendedsettings-property.md) avant la connexion. Lorsque la méthode [**IMsTscAx. Connect**](imstscax-connect.md) est appelée, le contrôle ActiveX Bureau à distance se connecte automatiquement à la session enfant sans demander d’informations d’identification, sauf si l’utilisateur est connecté à la session parente à l’aide d’une carte à puce. Contrairement à une session de Bureau à distance normale, un utilisateur n’a pas besoin du droit interactif distant pour se connecter à la session enfant, car il s’agit d’une session de bouclage.

Une session enfant ne peut pas être verrouillée. Il n’a pas d’écran de veille et aucun écran d’ouverture de session. Par ailleurs, contrairement à une session normale, si la stratégie de texte de connexion WinLogon est définie, le texte d’ouverture de session ne sera pas affiché dans cette session enfant. En outre, il n’y aura aucun effet sur les stratégies de groupe Connexion Bureau à distance Timeout sur la session enfant si ces stratégies sont définies.

Les API suivantes sont utilisées conjointement avec les sessions enfants :

-   [**WTSEnableChildSessions**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenablechildsessions)
-   [**WTSIsChildSessionsEnabled**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsischildsessionsenabled)
-   [**WTSGetChildSessionId**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsgetchildsessionid)
-   Propriété « ConnectToChildSession » dans [ **IMsRdpExtendedSettings. Property**](imsrdpextendedsettings-property.md)

 

 




