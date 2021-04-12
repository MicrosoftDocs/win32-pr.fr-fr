---
title: Contrôle d’animation
description: Cette section contient des informations sur les éléments de programmation utilisés avec les contrôles d’animation.
ms.assetid: 16994f93-e0fd-4c71-9c8a-15642408b8de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd2a3fc7377c7258ba49b5a4188e6074270b5862
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104463794"
---
# <a name="animation-control"></a>Contrôle d’animation

Cette section contient des informations sur les éléments de programmation utilisés avec les contrôles d’animation.

### <a name="overviews"></a>Vues d'ensemble



| Rubrique                                                      | Contenu                                                                                                                                                                                                                           |
|------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [À propos des contrôles d’animation](animation-control-overview.md) | Un *contrôle d’animation* est une fenêtre qui affiche un clip Audio-Video entrelacé (AVI). Un clip AVI est une série de frames bitmap tels qu’un film. Les contrôles d’animation peuvent uniquement afficher des clips AVI qui ne contiennent pas de données audio.<br/> |
| [Utilisation de contrôles d’animation](using-animation-control.md)    | Cette section fournit des détails d’implémentation et un exemple de code pour les contrôles d’animation.<br/>                                                                                                                                      |



 

### <a name="macros"></a>Macros



| Rubrique                                           | Contenu                                                                                                                                                                                                                                                          |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Animer la \_ fermeture**](/windows/desktop/api/Commctrl/nf-commctrl-animate_close)         | Ferme un clip AVI. Vous pouvez utiliser cette macro ou envoyer explicitement le message [**ACM \_ Open**](acm-open.md) , en transmettant des paramètres **null** . <br/>                                                                                                              |
| [**Animer \_ créer**](/windows/desktop/api/Commctrl/nf-commctrl-animate_create)       | Crée un contrôle d’animation. [**Animer \_ Créer**](/windows/desktop/api/Commctrl/nf-commctrl-animate_create) appelle la fonction [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) pour créer le contrôle d’animation. <br/>                                                                                   |
| [**Animer \_ IsPlaying**](/windows/desktop/api/Commctrl/nf-commctrl-animate_isplaying) | Vérifie si un clip AVI est en train de fonctionner. Vous pouvez utiliser cette macro ou envoyer un [**message \_ ISPLAYING ACM**](acm-isplaying.md) .<br/>                                                                                                                            |
| [**Animer \_ ouvrir**](/windows/desktop/api/Commctrl/nf-commctrl-animate_open)           | Ouvre un clip AVI et affiche sa première image dans un contrôle d’animation. Vous pouvez utiliser cette macro ou envoyer explicitement le message [**ACM \_ Open**](acm-open.md) . <br/>                                                                                          |
| [**Animer \_ OpenEx**](/windows/desktop/api/Commctrl/nf-commctrl-animate_openex)       | Ouvre un clip AVI à partir d’une ressource dans un module spécifié et affiche sa première image dans un contrôle d’animation. Vous pouvez utiliser cette macro ou envoyer explicitement le message [**ACM \_ Open**](acm-open.md) . <br/>                                                    |
| [**Animer la \_ lecture**](/windows/desktop/api/Commctrl/nf-commctrl-animate_play)           | Lit un clip AVI dans un contrôle d’animation. Le contrôle lit le clip en arrière-plan pendant que le thread continue de s’exécuter. Vous pouvez utiliser cette macro ou envoyer le message de [**\_ lecture ACM**](acm-play.md) de manière explicite. <br/>                                    |
| [**Animer la \_ recherche**](/windows/desktop/api/Commctrl/nf-commctrl-animate_seek)           | Indique à un contrôle d’animation d’afficher un cadre particulier d’un clip AVI. Le contrôle affiche le clip en arrière-plan pendant que le thread continue de s’exécuter. Vous pouvez utiliser cette macro ou envoyer le message de [**\_ lecture ACM**](acm-play.md) de manière explicite. <br/> |
| [**Animer \_ arrêter**](/windows/desktop/api/Commctrl/nf-commctrl-animate_stop)           | Arrête la diffusion d’un clip AVI dans un contrôle d’animation. Vous pouvez utiliser cette macro ou envoyer le message d' [**\_ arrêt ACM**](acm-stop.md) de manière explicite. <br/>                                                                                                               |



 

### <a name="messages"></a>Messages



| Rubrique                                   | Contenu                                                                                                                                                                                                                                   |
|-----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ISPLAYING ACM**](acm-isplaying.md) | Vérifie si un clip AVI est lu. Vous pouvez envoyer ce message de manière explicite ou utiliser la macro [**animer \_ IsPlaying**](/windows/desktop/api/Commctrl/nf-commctrl-animate_isplaying) .<br/>                                                                                   |
| [**\_Open ACM**](acm-open.md)           | Ouvre un clip AVI et affiche sa première image dans un contrôle d’animation. Vous pouvez envoyer ce message de manière explicite ou utiliser la macro [**animer \_ ouvrir**](/windows/desktop/api/Commctrl/nf-commctrl-animate_open) ou [**animer \_ OpenEx**](/windows/desktop/api/Commctrl/nf-commctrl-animate_openex) . <br/>              |
| [**\_lecture ACM**](acm-play.md)           | Lit un clip AVI dans un contrôle d’animation. Le contrôle lit le clip en arrière-plan pendant que le thread continue de s’exécuter. Vous pouvez envoyer ce message de manière explicite ou à l’aide de la macro [**animer \_ Play**](/windows/desktop/api/Commctrl/nf-commctrl-animate_play) .<br/> |
| [**\_arrêt ACM**](acm-stop.md)           | Arrête la diffusion d’un clip AVI dans un contrôle d’animation. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**\_ arrêter l’animation**](/windows/desktop/api/Commctrl/nf-commctrl-animate_stop) .<br/>                                                                            |



 

### <a name="notifications"></a>Notifications



| Rubrique                           | Contenu                                                                                                                                                                                                       |
|---------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ACN \_ Démarrer**](acn-start.md) | Avertit la fenêtre parente d’un contrôle d’animation que le clip AVI associé a démarré. Ce code de notification est envoyé sous la forme d’un message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) . <br/>      |
| [**ACN \_ arrêter**](acn-stop.md)   | Notifie la fenêtre parente d’un contrôle d’animation que le clip AVI associé a cessé de fonctionner. Ce code de notification est envoyé sous la forme d’un message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) . <br/> |



 

### <a name="constants"></a>Constantes



| Rubrique                                                        | Contenu                                                                      |
|--------------------------------------------------------------|-------------------------------------------------------------------------------|
| [**Styles de contrôle d’animation**](animation-control-styles.md) | Cette section répertorie les styles de fenêtre utilisés avec les contrôles d’animation.<br/> |



 

 

