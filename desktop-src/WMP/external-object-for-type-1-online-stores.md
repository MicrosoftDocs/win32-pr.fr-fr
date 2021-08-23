---
title: Objet externe pour les magasins de type 1 en ligne
description: Objet externe pour les magasins de type 1 en ligne
ms.assetid: 5c42e1a9-c5c6-4725-8528-de2839d84e77
keywords:
- Lecteur Windows Media magasins en ligne, objets externes
- magasins en ligne, objets externes
- types 1 magasins en ligne, objets externes
- objets externes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e7d95d2ca332b88edea73da2238374aeffc52e520d7bc0346eab9f4eb7a05f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119648999"
---
# <a name="external-object-for-type-1-online-stores"></a>Objet externe pour les magasins de type 1 en ligne

> [!Note]  
> Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.

 

l’objet **externe** fournit des fonctionnalités aux pages web, fournies par un magasin en ligne, hébergé dans Lecteur Windows Media.

L’objet **externe** expose les propriétés suivantes pour les magasins de type 1 en ligne.



| Propriété                                                                                  | Description                                                                                                                              |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [accountType](external-accounttype.md)                                                   | Récupère le type de compte de l’utilisateur actuel.                                                                                          |
| [appColorButtonHighlight](external-appcolorbuttonhighlight.md)                           | récupère la couleur de surbrillance du bouton actuel pour l’interface utilisateur Lecteur Windows Media.                                                |
| [appColorButtonHoverFace](external-appcolorbuttonhoverface.md)                           | récupère la couleur de pointage du bouton actuelle pour l’interface utilisateur Lecteur Windows Media.                                                    |
| [appColorButtonShadow](external-appcolorbuttonshadow.md)                                 | récupère la couleur d’ombre du bouton actuelle pour l’interface utilisateur Lecteur Windows Media.                                                   |
| [appColorDark](external-appcolordark.md)                                                 | récupère la couleur ombrée foncée actuelle de l’interface utilisateur Lecteur Windows Media.                                                      |
| [appColorLight](external-appcolorlight.md)                                               | récupère la couleur ombrée actuelle de l’interface utilisateur du Lecteur Windows Media.                                                     |
| [appColorMedium](external-appcolormedium.md)                                             | récupère la couleur moyenne ombrée moyenne de l’interface utilisateur Lecteur Windows Media.                                                    |
| [basketTitle](external-baskettitle.md)                                                   | récupère le titre du bouton dans le volet de liste (également appelé panier) dans Lecteur Windows Media.                                     |
| [filter](external-filter.md)                                                             | récupère le filtre de recherche en cours d’utilisation par Lecteur Windows Media.                                                                    |
| [ignoreIEHistory](external-ignoreiehistory.md)                                           | spécifie si Lecteur Windows Media doit ignorer l’historique d’Internet Explorer.                                                          |
| [libraryLocationID](external-librarylocationid.md)                                       | Récupère l’identificateur d’un élément multimédia spécifique qui est actuellement affiché dans la vue du joueur.                                      |
| [libraryLocationType](external-librarylocationtype.md)                                   | récupère une [constante d’emplacement de bibliothèque](library-location-constants.md) qui indique le type de la vue actuelle dans Lecteur Windows Media. |
| [pluginRunning](external-pluginrunning.md)                                               | Récupère une valeur qui indique si le plug-in du magasin en ligne est en cours d’exécution.                                                          |
| [selectedItemID](external-selecteditemid.md)                                             | récupère l’identificateur de l’élément multimédia actuellement sélectionné dans Lecteur Windows Media.                                           |
| [selectedItemType](external-selecteditemtype.md)                                         | récupère le type de l’élément multimédia actuellement sélectionné dans Lecteur Windows Media.                                                 |
| [tâche](external-task.md)                                                                 | Récupère le nom du volet de tâches actuel.                                                                                             |
| [templateBeingDisplayedInLocalLibrary](external-templatebeingdisplayedinlocallibrary.md) | Indique si le flux représenté par la page de découverte en cours est affiché dans le contrôle d’arborescence de la bibliothèque locale.          |
| [userLoggedIn](external-userloggedin.md)                                                 | Récupère une valeur indiquant si l’utilisateur est connecté au magasin en ligne.                                                          |
| [version](external-version.md)                                                           | récupère la version actuelle de Lecteur Windows Media.                                                                                   |
| [viewParameters](external-viewparameters.md)                                             | récupère les paramètres associés à la vue actuelle dans Lecteur Windows Media.                                                           |



 

L’objet **externe** expose les méthodes suivantes pour les magasins de type 1 en ligne.



| Méthode                                                            | Description                                                                                                                  |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [addToBasket](external-addtobasket.md)                           | ajoute des éléments multimédias au volet liste (également appelé panier) dans Lecteur Windows Media.                                          |
| [attemptLogin](external-attemptlogin.md)                         | Affiche une boîte de dialogue qui permet à l’utilisateur d’essayer de se connecter au magasin en ligne.                                                 |
| [authentifier](external-authenticate.md)                         | Lance une tentative d’authentification de l’utilisateur.                                                                               |
| [buy](external-buy.md)                                           | Lance l’achat d’un ensemble d’éléments multimédias.                                                                              |
| [cancelNavigate](external-cancelnavigate.md)                     | informe Lecteur Windows Media qu’il ne doit pas afficher une nouvelle page de découverte, même si la vue a été modifiée dans le lecteur. |
| [changeView](external-changeview.md)                             | modifie la vue dans Lecteur Windows Media.                                                                                    |
| [changeViewOnlineList](external-changeviewonlinelist.md)         | modifie la vue dans Lecteur Windows Media pour afficher une liste générée dynamiquement par le magasin en ligne.                        |
| [téléchargement](external-download.md)                                 | Lance le téléchargement d’un ensemble d’éléments multimédias.                                                                              |
| [répétition](external-play.md)                                         | indique à Lecteur Windows Media de lire un ensemble d’éléments multimédias.                                                                 |
| [saveCurrentViewToLibrary](external-savecurrentviewtolibrary.md) | Crée une sélection à partir des éléments multimédias dans l’affichage actuel et enregistre la sélection dans la bibliothèque locale.                     |
| [sendMessage](external-sendmessage.md)                           | Envoie un message au plug-in du magasin en ligne.                                                                               |
| [showPopup](external-showpopup.md)                               | ordonne à Lecteur Windows Media d’afficher une page web contextuelle ; autrement dit, une page Web qui s’affiche dans une fenêtre distincte.            |



 

L’objet **externe** expose les événements suivants pour les magasins de type 1 en ligne.



| Événement                                                                         | Description                                                                             |
|-------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [OnChangeViewError](external-onchangeviewerror-event.md)                     | Se produit lorsqu’un appel à la méthode **External. ChangeView** génère une erreur.           |
| [OnChangeViewOnlineListError](external-onchangeviewonlinelisterror-event.md) | Se produit lorsqu’un appel à la méthode **External. ChangeViewOnlineList** génère une erreur. |
| [OnColorChange](external-oncolorchange-event.md)                             | se produit lorsque la couleur de l’interface utilisateur de Lecteur Windows Media change.               |
| [OnLoginChange](external-onloginchange-event.md)                             | Se produit lorsque l’état de la connexion de l’utilisateur change ou lorsqu’une tentative de connexion échoue.        |
| [OnSendMessageComplete](external-onsendmessagecomplete-event.md)             | Se produit lorsque le magasin en ligne a terminé le traitement d’un message.                         |
| [OnViewChange](external-onviewchange-event.md)                               | se produit lorsque la vue change dans Lecteur Windows Media.                                   |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Référence pour les magasins en ligne de type 1**](reference-for-type-1-online-stores.md)
</dt> <dt>

[**Utilisation à distance du contrôle Windows Media Player**](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 




