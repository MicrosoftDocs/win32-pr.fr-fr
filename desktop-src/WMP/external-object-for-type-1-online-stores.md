---
title: Objet externe pour les magasins de type 1 en ligne
description: Objet externe pour les magasins de type 1 en ligne
ms.assetid: 5c42e1a9-c5c6-4725-8528-de2839d84e77
keywords:
- Windows Media Player Online stores, objets externes
- magasins en ligne, objets externes
- types 1 magasins en ligne, objets externes
- objets externes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f50e5e6bfc98ea3669996b06fa4a4defb52452fb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940276"
---
# <a name="external-object-for-type-1-online-stores"></a>Objet externe pour les magasins de type 1 en ligne

> [!Note]  
> Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.

 

L’objet **externe** fournit des fonctionnalités aux pages Web, fournies par un magasin en ligne, hébergé dans le lecteur Windows Media.

L’objet **externe** expose les propriétés suivantes pour les magasins de type 1 en ligne.



| Propriété                                                                                  | Description                                                                                                                              |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [accountType](external-accounttype.md)                                                   | Récupère le type de compte de l’utilisateur actuel.                                                                                          |
| [appColorButtonHighlight](external-appcolorbuttonhighlight.md)                           | Récupère la couleur de surbrillance du bouton en cours pour l’interface utilisateur du lecteur Windows Media.                                                |
| [appColorButtonHoverFace](external-appcolorbuttonhoverface.md)                           | Récupère la couleur de pointage du bouton actuelle pour l’interface utilisateur du lecteur Windows Media.                                                    |
| [appColorButtonShadow](external-appcolorbuttonshadow.md)                                 | Récupère la couleur d’ombre du bouton actuelle pour l’interface utilisateur du lecteur Windows Media.                                                   |
| [appColorDark](external-appcolordark.md)                                                 | Récupère la couleur ombrée foncée actuelle de l’interface utilisateur du lecteur Windows Media.                                                      |
| [appColorLight](external-appcolorlight.md)                                               | Récupère la couleur ombrée actuelle de l’interface utilisateur du lecteur Windows Media.                                                     |
| [appColorMedium](external-appcolormedium.md)                                             | Récupère la couleur de nuance moyenne en grisé de l’interface utilisateur du lecteur Windows Media.                                                    |
| [basketTitle](external-baskettitle.md)                                                   | Récupère le titre du bouton dans le volet Liste (également appelé panier) dans le lecteur Windows Media.                                     |
| [filter](external-filter.md)                                                             | Récupère le filtre de recherche en cours d’utilisation par le lecteur Windows Media.                                                                    |
| [ignoreIEHistory](external-ignoreiehistory.md)                                           | Spécifie si le lecteur Windows Media doit ignorer l’historique d’Internet Explorer.                                                          |
| [libraryLocationID](external-librarylocationid.md)                                       | Récupère l’identificateur d’un élément multimédia spécifique qui est actuellement affiché dans la vue du joueur.                                      |
| [libraryLocationType](external-librarylocationtype.md)                                   | Récupère une [constante d’emplacement de bibliothèque](library-location-constants.md) qui indique le type de la vue actuelle dans le lecteur Windows Media. |
| [pluginRunning](external-pluginrunning.md)                                               | Récupère une valeur qui indique si le plug-in du magasin en ligne est en cours d’exécution.                                                          |
| [selectedItemID](external-selecteditemid.md)                                             | Récupère l’identificateur de l’élément multimédia actuellement sélectionné dans le lecteur Windows Media.                                           |
| [selectedItemType](external-selecteditemtype.md)                                         | Récupère le type de l’élément multimédia actuellement sélectionné dans le lecteur Windows Media.                                                 |
| [tâche](external-task.md)                                                                 | Récupère le nom du volet de tâches actuel.                                                                                             |
| [templateBeingDisplayedInLocalLibrary](external-templatebeingdisplayedinlocallibrary.md) | Indique si le flux représenté par la page de découverte en cours est affiché dans le contrôle d’arborescence de la bibliothèque locale.          |
| [userLoggedIn](external-userloggedin.md)                                                 | Récupère une valeur indiquant si l’utilisateur est connecté au magasin en ligne.                                                          |
| [version](external-version.md)                                                           | Récupère la version actuelle du lecteur Windows Media.                                                                                   |
| [viewParameters](external-viewparameters.md)                                             | Récupère les paramètres associés à la vue actuelle dans le lecteur Windows Media.                                                           |



 

L’objet **externe** expose les méthodes suivantes pour les magasins de type 1 en ligne.



| Méthode                                                            | Description                                                                                                                  |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [addToBasket](external-addtobasket.md)                           | Ajoute des éléments multimédias au volet Liste (également appelé panier) dans le lecteur Windows Media.                                          |
| [attemptLogin](external-attemptlogin.md)                         | Affiche une boîte de dialogue qui permet à l’utilisateur d’essayer de se connecter au magasin en ligne.                                                 |
| [authentifier](external-authenticate.md)                         | Lance une tentative d’authentification de l’utilisateur.                                                                               |
| [Buy](external-buy.md)                                           | Lance l’achat d’un ensemble d’éléments multimédias.                                                                              |
| [cancelNavigate](external-cancelnavigate.md)                     | Informe le lecteur Windows Media qu’il ne doit pas afficher de nouvelle page de découverte, même si la vue a été modifiée dans le lecteur. |
| [changeView](external-changeview.md)                             | Modifie la vue dans le lecteur Windows Media.                                                                                    |
| [changeViewOnlineList](external-changeviewonlinelist.md)         | Modifie la vue dans le lecteur Windows Media pour afficher une liste générée dynamiquement par le magasin en ligne.                        |
| [téléchargement](external-download.md)                                 | Lance le téléchargement d’un ensemble d’éléments multimédias.                                                                              |
| [répétition](external-play.md)                                         | Indique au lecteur Windows Media de lire un ensemble d’éléments multimédias.                                                                 |
| [saveCurrentViewToLibrary](external-savecurrentviewtolibrary.md) | Crée une sélection à partir des éléments multimédias dans l’affichage actuel et enregistre la sélection dans la bibliothèque locale.                     |
| [sendMessage](external-sendmessage.md)                           | Envoie un message au plug-in du magasin en ligne.                                                                               |
| [showPopup](external-showpopup.md)                               | Indique au lecteur Windows Media d’afficher une page Web contextuelle ; autrement dit, une page Web qui s’affiche dans une fenêtre distincte.            |



 

L’objet **externe** expose les événements suivants pour les magasins de type 1 en ligne.



| Événement                                                                         | Description                                                                             |
|-------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [OnChangeViewError](external-onchangeviewerror-event.md)                     | Se produit lorsqu’un appel à la méthode **External. ChangeView** génère une erreur.           |
| [OnChangeViewOnlineListError](external-onchangeviewonlinelisterror-event.md) | Se produit lorsqu’un appel à la méthode **External. ChangeViewOnlineList** génère une erreur. |
| [OnColorChange](external-oncolorchange-event.md)                             | Se produit lorsque la couleur de l’interface utilisateur du lecteur Windows Media change.               |
| [OnLoginChange](external-onloginchange-event.md)                             | Se produit lorsque l’état de la connexion de l’utilisateur change ou lorsqu’une tentative de connexion échoue.        |
| [OnSendMessageComplete](external-onsendmessagecomplete-event.md)             | Se produit lorsque le magasin en ligne a terminé le traitement d’un message.                         |
| [OnViewChange](external-onviewchange-event.md)                               | Se produit lorsque la vue change dans le lecteur Windows Media.                                   |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Référence pour les magasins en ligne de type 1**](reference-for-type-1-online-stores.md)
</dt> <dt>

[**Utilisation à distance du contrôle Windows Media Player**](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 




