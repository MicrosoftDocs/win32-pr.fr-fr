---
description: La classe CBaseControlWindow implémente l’interface IVideoWindow et contrôle l’accès externe à son filtre associé.
ms.assetid: 3657ba24-ffaa-491f-9eb3-f9913d5d421a
title: CBaseControlWindow, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow
api_type:
- COM
api_location: ''
ms.openlocfilehash: 500706531d7e7a934681dabe3bcd00b7de0d80e42b8bbf27a5456a8fd4415f21
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017231"
---
# <a name="cbasecontrolwindow-class"></a>CBaseControlWindow, classe

![hiérarchie de la classe cbasecontrolwindow](images/wctrl01.png)

La classe **CBaseControlWindow** implémente l’interface [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) et contrôle l’accès externe à son filtre associé. Vous devez synchroniser l’objet **CBaseControlWindow** avec le filtre en lui transmettant un pointeur vers un objet de synchronisation de section critique. La classe **CBaseControlWindow** fournit un certain nombre de méthodes qui retournent des paramètres de propriété sans gérer cette section critique. Par exemple, l’appel de [**CBaseControlWindow :: obtenir \_ AutoShow**](cbasecontrolwindow-get-autoshow.md) pour récupérer la valeur du membre de données **m \_ bAutoShow** verrouille la section critique. Toutefois, le filtre a peut-être déjà une section critique interne verrouillée, ce qui risque de violer la hiérarchie de verrous du filtre. Au lieu de cela, l’appel de la fonction membre [**CBaseControlWindow :: IsAutoShowEnabled**](cbasecontrolwindow-isautoshowenabled.md) retourne la valeur requise sans affecter la section critique.

Toutes les méthodes [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) implémentées par **CBaseControlWindow** requièrent que le filtre soit correctement connecté avec son filtre en amont. Pour cette raison, les objets de classe requièrent un code confidentiel de synchronisation que vous définissez en appelant la méthode [**CBaseControlWindow :: SetControlWindowPin**](cbasecontrolwindow-setcontrolwindowpin.md) . Chaque fois que vous appelez une méthode **IVideoWindow** , l’objet **CBaseControlWindow** vérifie que le code confidentiel est toujours connecté.



| Membres de données protégés                                                     | Description                                                                                                                                 |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| m \_ bAutoShow                                                               | Résultat lorsque l’état change.                                                                                                              |
| m \_ bCursorHidden                                                           | Déterminer si le curseur est affiché ou masqué.                                                                                 |
| m \_ BorderColour                                                            | Couleur de la bordure de la fenêtre active.                                                                                                         |
| m \_ hwndDrain                                                               | Handle de fenêtre auquel les messages reçus sont publiés.                                                                                        |
| m \_ hwndOwner                                                               | Fenêtre propriétaire.                                                                                                                              |
| m \_ pFilter                                                                 | Pointeur vers le filtre de média propriétaire.                                                                                                         |
| m \_ pInterfaceLock                                                          | Section critique définie de manière externe.                                                                                                        |
| m \_ pPin                                                                    | Contrôle des types de médias pour la connexion.                                                                                                  |
| Fonctions de membre                                                           | Description                                                                                                                                 |
| [**CBaseControlWindow**](cbasecontrolwindow-cbasecontrolwindow.md)        | Construit un objet **CBaseControlWindow** .                                                                                                 |
| [**DoGetWindowStyle**](cbasecontrolwindow-dogetwindowstyle.md)            | Récupère les styles de fenêtre par défaut ou étendus.                                                                                     |
| [**DoSetWindowStyle**](cbasecontrolwindow-dosetwindowstyle.md)            | Définit les styles de fenêtre par défaut ou étendus.                                                                                                 |
| [**GetBorderColour**](cbasecontrolwindow-getbordercolour.md)              | Récupère la couleur de bordure actuelle. Il s’agit d’une fonction membre d’assistance.                                                                       |
| [**GetOwnerWindow**](cbasecontrolwindow-getownerwindow.md)                | Récupère la fenêtre propriétaire. Il s’agit d’une fonction membre d’assistance.                                                                              |
| [**IsAutoShowEnabled**](cbasecontrolwindow-isautoshowenabled.md)          | Récupère des informations indiquant si la fenêtre vidéo s’affiche automatiquement lorsque le filtre de rendu s’interrompt ou s’exécute.                        |
| [**IsCursorHidden**](cbasecontrolwindow-iscursorhidden.md)                | Récupère l’état actuel du membre de données **m \_ bCursorHidden** sans verrouiller la section critique. Il s’agit d’une fonction membre d’assistance. |
| [**PossiblyEatMessage**](cbasecontrolwindow-possiblyeatmessage.md)        | Distribue des messages à la fenêtre parente.                                                                                                  |
| [**SetControlWindowPin**](cbasecontrolwindow-setcontrolwindowpin.md)      | Avertit l’objet du code confidentiel auquel il s’applique.                                                                                         |
| Méthodes IVideoWindow                                                       | Description                                                                                                                                 |
| [**recevoir l' \_ affichage automatique**](cbasecontrolwindow-get-autoshow.md)                   | Récupère le paramètre d’indicateur d’affichage automatique actuel.                                                                                                |
| [**Obtient \_ BackgroundPalette**](cbasecontrolwindow-get-backgroundpalette.md) | Récupère la palette réalisée dans l’indicateur d’arrière-plan.                                                                                      |
| [**Obtient la \_ CouleurBordure**](cbasecontrolwindow-get-bordercolor.md)             | Récupère la couleur de bordure actuelle.                                                                                                         |
| [**recevoir la \_ légende**](cbasecontrolwindow-get-caption.md)                     | Récupère le titre de la fenêtre active.                                                                                                       |
| [**Obtient \_ FullScreenMode**](cbasecontrolwindow-get-fullscreenmode.md)      | Récupère le mode plein écran actuel.                                                                                                     |
| [**afficher la \_ hauteur**](cbasecontrolwindow-get-height.md)                       | Récupère la hauteur de la fenêtre actuelle.                                                                                                        |
| [**aller à \_ gauche**](cbasecontrolwindow-get-left.md)                           | Récupère la coordonnée de la fenêtre de gauche actuelle.                                                                                               |
| [**GetMaxIdealImageSize**](cbasecontrolwindow-getmaxidealimagesize.md)    | Récupère la taille maximale de l’image idéale.                                                                                              |
| [**Obtient \_ MessageDrain**](cbasecontrolwindow-get-messagedrain.md)           | Récupère le drain de message actuel.                                                                                                        |
| [**GetMinIdealImageSize**](cbasecontrolwindow-getminidealimagesize.md)    | Récupère la taille minimale de l’image idéale.                                                                                              |
| [**acquérir le \_ propriétaire**](cbasecontrolwindow-get-owner.md)                         | Récupère le handle de fenêtre parente.                                                                                                         |
| [**GetRestorePosition**](cbasecontrolwindow-getrestoreposition.md)        | Récupère la position à laquelle la fenêtre sera restaurée lorsqu’elle est agrandie ou réduite.                                                    |
| [**en \_ haut**](cbasecontrolwindow-get-top.md)                             | Récupère la coordonnée y du haut de la fenêtre.                                                                                       |
| [**afficher \_**](cbasecontrolwindow-get-visible.md)                     | Récupère le paramètre de visibilité actuel de la fenêtre.                                                                                     |
| [**afficher la \_ largeur**](cbasecontrolwindow-get-width.md)                         | Récupère la largeur de la fenêtre.                                                                                                          |
| [**GetWindowPosition**](cbasecontrolwindow-getwindowposition.md)          | Récupère les coordonnées de la fenêtre active.                                                                                                   |
| [**récupérer la \_ WindowState**](cbasecontrolwindow-get-windowstate.md)             | Récupère l’état actuel de la fenêtre.                                                                                                  |
| [**Obtient \_ WindowStyle**](cbasecontrolwindow-get-windowstyle.md)             | Récupère les styles de fenêtre standard.                                                                                                       |
| [**Obtient \_ WindowStyleEx**](cbasecontrolwindow-get-windowstyleex.md)         | Récupère les styles de fenêtre étendus.                                                                                                       |
| [**HideCursor**](cbasecontrolwindow-hidecursor.md)                        | Masque ou affiche le curseur.                                                                                                               |
| [**IsCursorHidden**](cbasecontrolwindow-iscursorhidden.md)                | Récupère l’état actuel du membre de données **m \_ bCursorHidden** .                                                                        |
| [**NotifyOwnerMessage**](cbasecontrolwindow-notifyownermessage.md)        | Transmet les messages envoyés aux fenêtres propriétaires.                                                                                         |
| [**mettre l' \_ affichage automatique**](cbasecontrolwindow-put-autoshow.md)                   | Définit la propriété d’affichage automatique.                                                                                                                 |
| [**put \_ BackgroundPalette**](cbasecontrolwindow-put-backgroundpalette.md) | Définit un indicateur pour réaliser la palette en arrière-plan.                                                                                       |
| [**Placer la \_ CouleurBordure**](cbasecontrolwindow-put-bordercolor.md)             | Définit la couleur de bordure actuelle.                                                                                                              |
| [**Placer la \_ légende**](cbasecontrolwindow-put-caption.md)                     | Définit le titre de la fenêtre active.                                                                                                            |
| [**put \_ FullScreenMode**](cbasecontrolwindow-put-fullscreenmode.md)      | Définit le mode plein écran.                                                                                                                  |
| [**Placer la \_ hauteur**](cbasecontrolwindow-put-height.md)                       | Définit la hauteur de la fenêtre actuelle.                                                                                                             |
| [**placer à \_ gauche**](cbasecontrolwindow-put-left.md)                           | Définit la coordonnée gauche de la fenêtre.                                                                                                    |
| [**put \_ MessageDrain**](cbasecontrolwindow-put-messagedrain.md)           | Définit la fenêtre drain de message.                                                                                                              |
| [**Placer le \_ propriétaire**](cbasecontrolwindow-put-owner.md)                         | Définit le handle de fenêtre parente Win32 de Microsoft.                                                                                              |
| [**placer en \_ haut**](cbasecontrolwindow-put-top.md)                             | Définit la position du haut de la fenêtre.                                                                                                |
| [**mettre \_ visible**](cbasecontrolwindow-put-visible.md)                     | Masque ou affiche la fenêtre.                                                                                                                  |
| [**mettre la \_ largeur**](cbasecontrolwindow-put-width.md)                         | Définit la largeur de la fenêtre.                                                                                                               |
| [**put \_ WindowState**](cbasecontrolwindow-put-windowstate.md)             | Définit l’état de la fenêtre.                                                                                                               |
| [**placer \_ WindowStyle**](cbasecontrolwindow-put-windowstyle.md)             | Définit les styles de fenêtre standard.                                                                                                            |
| [**put \_ WindowStyleEx**](cbasecontrolwindow-put-windowstyleex.md)         | Définit les styles de fenêtre étendus.                                                                                                            |
| [**SetWindowForeground**](cbasecontrolwindow-setwindowforeground.md)      | Définit la fenêtre au premier plan.                                                                                                          |
| [**SetWindowPosition**](cbasecontrolwindow-setwindowposition.md)          | Définit la position de la fenêtre.                                                                                                                   |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[DirectShow Classes de base](directshow-base-classes.md)
</dt> </dl>

 

 



