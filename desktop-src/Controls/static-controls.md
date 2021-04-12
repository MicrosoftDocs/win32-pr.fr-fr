---
title: Contrôle statique
description: Cette section contient des informations sur les éléments de programmation utilisés avec les contrôles statiques. Un contrôle statique est un contrôle qui permet à une application de fournir à l’utilisateur un texte et des graphiques informatifs qui ne requièrent généralement aucune réponse.
ms.assetid: vs|controls|~\controls\staticcontrols\staticcontrols.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62c8c5b554dad8c6f3c18d0c1ceb9300dde57b20
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104031942"
---
# <a name="static-control"></a>Contrôle statique

Cette section contient des informations sur les éléments de programmation utilisés avec les contrôles statiques. Un *contrôle statique* est un contrôle qui permet à une application de fournir à l’utilisateur un texte et des graphiques informatifs qui ne requièrent généralement aucune réponse.

### <a name="overviews"></a>Vues d'ensemble



| Rubrique                                              | Contenu                                                              |
|----------------------------------------------------|-----------------------------------------------------------------------|
| [À propos des contrôles statiques](about-static-controls.md) | Cette rubrique explique comment les contrôles statiques sont utilisés.<br/>         |
| [Styles de contrôle statiques](static-control-styles.md) |                                                                       |
| [Utilisation de contrôles statiques](using-static-controls.md) | Cette rubrique fournit un exemple qui utilise un contrôle statique.<br/> |



 

### <a name="messages"></a>Messages



| Rubrique                                 | Contenu                                                                                                                                                                        |
|---------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_GETICON STM**](stm-geticon.md)   | Une application envoie le message [**STM \_ GETICON**](stm-geticon.md) pour récupérer un handle vers l’icône associée à un contrôle statique avec le style d' \_ icône SS. <br/> |
| [**STM \_ GETIMAGE**](stm-getimage.md) | Une application envoie un message [**STM \_ GETIMAGE**](stm-getimage.md) pour récupérer un handle de l’image (icône ou bitmap) associé à un contrôle statique. <br/>          |
| [**\_SETICON STM**](stm-seticon.md)   | Une application envoie le message [**STM \_ SETICON**](stm-seticon.md) pour associer une icône à un contrôle Icon. <br/>                                                     |
| [**\_SETIMAGE STM**](stm-setimage.md) | Une application envoie un message [**STM \_ SETIMAGE**](stm-setimage.md) pour associer une nouvelle image à un contrôle statique.<br/>                                                |



 

### <a name="notifications"></a>Notifications



| Rubrique                                           | Contenu                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [STN \_ sur lequel l’utilisateur a cliqué](stn-clicked.md)                 | Le code de notification [ \_ cliqué sur le STN](stn-clicked.md) est envoyé lorsque l’utilisateur clique sur un contrôle statique avec le style de notification [**SS \_**](static-control-styles.md) . La fenêtre parente du contrôle reçoit ce code de notification via le message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) .<br/>                                                                                                                                                                  |
| [STN \_ DBLCLK](stn-dblclk.md)                   | Le code de notification [STN \_ DBLCLK](stn-dblclk.md) est envoyé lorsque l’utilisateur double-clique sur un contrôle statique avec le style de **\_ notification SS** . La fenêtre parente du contrôle reçoit ce code de notification via le message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) .<br/>                                                                                                                                                                                          |
| [désactivation de STN \_](stn-disable.md)                 | Le code de notification de [ \_ désactivation de STN](stn-disable.md) est envoyé lorsqu’un contrôle statique est désactivé. Le contrôle statique doit avoir le style **SS \_ Notify** pour recevoir ce code de notification. La fenêtre parente du contrôle reçoit ce code de notification via le message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) .<br/>                                                                                                                                            |
| [STN \_ activer](stn-enable.md)                   | Le [STN \_ activer](stn-enable.md) le code de notification est envoyé lorsqu’un contrôle statique est activé. Le contrôle statique doit avoir le style **SS \_ Notify** pour recevoir ce code de notification. La fenêtre parente du contrôle reçoit ce code de notification via le message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) .<br/>                                                                                                                                               |
| [**\_CTLCOLORSTATIC WM**](wm-ctlcolorstatic.md) | Un contrôle statique, ou un contrôle d’édition qui est en lecture seule ou qui est désactivé, envoie le message [**WM \_ CTLCOLORSTATIC**](wm-ctlcolorstatic.md) à sa fenêtre parente lorsque le contrôle va être dessiné. En répondant à ce message, la fenêtre parente peut utiliser le handle de contexte de périphérique spécifié pour définir les couleurs de texte et d’arrière-plan du contrôle statique. <br/> Une fenêtre reçoit ce message par le biais de sa fonction [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) . <br/> |



 

 

