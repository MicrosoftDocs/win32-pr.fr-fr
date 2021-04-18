---
title: Objet externe pour les magasins de type 2 en ligne
description: Objet externe pour les magasins de type 2 en ligne
ms.assetid: d12e7480-39ec-4d32-9cf9-5555d0f92d80
keywords:
- Windows Media Player Online stores, objets externes
- magasins en ligne, objets externes
- type 2 magasins en ligne, objets externes
- objets externes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c412cac301d61aeb791131e85bb8bc60f390201d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507303"
---
# <a name="external-object-for-type-2-online-stores"></a>Objet externe pour les magasins de type 2 en ligne

> [!Note]  
> Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.

 

L’objet **externe** peut fournir des fonctionnalités aux pages Web fournies par un magasin de type 2 en ligne et hébergées dans le lecteur Windows Media.

L’objet **externe** expose les propriétés suivantes.



| Propriété                                                        | Description                                                                               |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [appColorButtonHighlight](external-appcolorbuttonhighlight.md) | Récupère la couleur de surbrillance du bouton en cours pour l’interface utilisateur du lecteur Windows Media. |
| [appColorButtonHoverFace](external-appcolorbuttonhoverface.md) | Récupère la couleur de pointage du bouton actuelle pour l’interface utilisateur du lecteur Windows Media.     |
| [appColorButtonShadow](external-appcolorbuttonshadow.md)       | Récupère la couleur d’ombre du bouton actuelle pour l’interface utilisateur du lecteur Windows Media.    |
| [appColorDark](external-appcolordark.md)                       | Récupère la couleur ombrée foncée actuelle de l’interface utilisateur du lecteur Windows Media.       |
| [appColorLight](external-appcolorlight.md)                     | Récupère la couleur ombrée actuelle de l’interface utilisateur du lecteur Windows Media.      |
| [appColorMedium](external-appcolormedium.md)                   | Récupère la couleur de nuance moyenne en grisé de l’interface utilisateur du lecteur Windows Media.     |
| [DownloadManager](external-downloadmanager.md)                 | Récupère l’objet **downloadmanager** .                                                 |
| [SelectedTaskPane](external-selectedtaskpane.md)               | Spécifie ou récupère le volet des tâches actuellement sélectionné.                                  |
| [version](external-version.md)                                 | Récupère la version actuelle du lecteur Windows Media.                                    |



 

L’objet **externe** expose les méthodes suivantes.



| Méthode                                                  | Description                                                                          |
|---------------------------------------------------------|--------------------------------------------------------------------------------------|
| [NavigateTaskPaneURL](external-navigatetaskpaneurl.md) | Ouvre une page Web dans le volet de tâches spécifié et active le volet spécifié. |
| [playMedia (déconseillée)](external-playmedia.md)        | Spécifie l’URL d’un élément multimédia numérique à lire.                                   |



 

L’objet **externe** expose l’événement suivant.



| Événement                                             | Description                                                               |
|---------------------------------------------------|---------------------------------------------------------------------------|
| [OnColorChange](external-oncolorchange-event.md) | Se produit lorsque la couleur de l’interface utilisateur du lecteur Windows Media change. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Référence pour les magasins en ligne de type 2**](reference-for-type-2-online-stores.md)
</dt> <dt>

[**Utilisation à distance du contrôle Windows Media Player**](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 




