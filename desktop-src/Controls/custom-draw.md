---
title: Dessin personnalisé
description: Le dessin personnalisé n’est pas un contrôle courant ; Il s’agit d’un service que de nombreux contrôles communs fournissent.
ms.assetid: vs|controls|~\controls\custdraw\custdraw.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16271e915a942e21f3f3763237a25c37a8b934fc1a44a016bb7e3938491a3c66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118413177"
---
# <a name="custom-draw"></a>Dessin personnalisé

Le dessin personnalisé n’est pas un contrôle courant ; Il s’agit d’un service que de nombreux contrôles communs fournissent. Le service de dessin personnalisé permet à une application de bénéficier d’une plus grande souplesse dans la personnalisation de l’apparence d’un contrôle. Votre application peut exploiter des notifications de dessin personnalisées pour modifier facilement la police utilisée pour afficher des éléments ou dessiner manuellement un élément sans avoir à effectuer une Owner Draw complète.

Cette section contient des informations sur les éléments de programmation utilisés avec le dessin personnalisé.

## <a name="overviews"></a>Vues d'ensemble



| Rubrique                                      | Contenu                                                                                                                                                               |
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [À propos du dessin personnalisé](about-custom-draw.md) | Cette section contient des informations générales sur la fonctionnalité de dessin personnalisée et fournit une vue d’ensemble conceptuelle de la façon dont une application peut prendre en charge le dessin personnalisé.<br/> |
| [Utilisation d’un dessin personnalisé](using-custom-draw.md) | Cette section contient des exemples qui montrent comment implémenter un dessin personnalisé. <br/>                                                                              |



 

## <a name="notifications"></a>Notifications



| Rubrique                               | Contenu                                                                                                                                                                 |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [\_CUSTOMDRAW nm](nm-customdraw.md) | Avertit la fenêtre parente d’un contrôle des opérations de dessin personnalisées. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) . <br/> |



 

## <a name="structures"></a>Structures



| Rubrique                                | Contenu                                                                                              |
|--------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) | Contient des informations spécifiques à un code de notification [ \_ CUSTOMDRAW nm](nm-customdraw.md) .<br/> |



 

 

 





