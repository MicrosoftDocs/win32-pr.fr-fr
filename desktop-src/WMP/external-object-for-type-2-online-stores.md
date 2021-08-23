---
title: Objet externe pour les magasins de type 2 en ligne
description: Objet externe pour les magasins de type 2 en ligne
ms.assetid: d12e7480-39ec-4d32-9cf9-5555d0f92d80
keywords:
- Lecteur Windows Media magasins en ligne, objets externes
- magasins en ligne, objets externes
- type 2 magasins en ligne, objets externes
- objets externes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57d177dd4bcac34e5a8e8a72f53f184c4e0dfffec41b3cef0c0080e2fe1840cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119648879"
---
# <a name="external-object-for-type-2-online-stores"></a>Objet externe pour les magasins de type 2 en ligne

> [!Note]  
> Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.

 

l’objet **externe** peut fournir des fonctionnalités aux pages web fournies par un magasin de type 2 en ligne et hébergées dans Lecteur Windows Media.

L’objet **externe** expose les propriétés suivantes.



| Propriété                                                        | Description                                                                               |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [appColorButtonHighlight](external-appcolorbuttonhighlight.md) | récupère la couleur de surbrillance du bouton actuel pour l’interface utilisateur Lecteur Windows Media. |
| [appColorButtonHoverFace](external-appcolorbuttonhoverface.md) | récupère la couleur de pointage du bouton actuelle pour l’interface utilisateur Lecteur Windows Media.     |
| [appColorButtonShadow](external-appcolorbuttonshadow.md)       | récupère la couleur d’ombre du bouton actuelle pour l’interface utilisateur Lecteur Windows Media.    |
| [appColorDark](external-appcolordark.md)                       | récupère la couleur ombrée foncée actuelle de l’interface utilisateur Lecteur Windows Media.       |
| [appColorLight](external-appcolorlight.md)                     | récupère la couleur ombrée actuelle de l’interface utilisateur du Lecteur Windows Media.      |
| [appColorMedium](external-appcolormedium.md)                   | récupère la couleur moyenne ombrée moyenne de l’interface utilisateur Lecteur Windows Media.     |
| [DownloadManager](external-downloadmanager.md)                 | Récupère l’objet **downloadmanager** .                                                 |
| [SelectedTaskPane](external-selectedtaskpane.md)               | Spécifie ou récupère le volet des tâches actuellement sélectionné.                                  |
| [version](external-version.md)                                 | récupère la version actuelle de Lecteur Windows Media.                                    |



 

L’objet **externe** expose les méthodes suivantes.



| Méthode                                                  | Description                                                                          |
|---------------------------------------------------------|--------------------------------------------------------------------------------------|
| [NavigateTaskPaneURL](external-navigatetaskpaneurl.md) | Ouvre une page Web dans le volet de tâches spécifié et active le volet spécifié. |
| [playMedia (déconseillée)](external-playmedia.md)        | Spécifie l’URL d’un élément multimédia numérique à lire.                                   |



 

L’objet **externe** expose l’événement suivant.



| Événement                                             | Description                                                               |
|---------------------------------------------------|---------------------------------------------------------------------------|
| [OnColorChange](external-oncolorchange-event.md) | se produit lorsque la couleur de l’interface utilisateur de Lecteur Windows Media change. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Référence pour les magasins en ligne de type 2**](reference-for-type-2-online-stores.md)
</dt> <dt>

[**Utilisation à distance du contrôle Windows Media Player**](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 




