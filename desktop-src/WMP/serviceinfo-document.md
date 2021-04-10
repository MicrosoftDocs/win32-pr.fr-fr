---
title: Document ServiceInfo
description: Document ServiceInfo
ms.assetid: 48f84dd7-e458-4da2-ae2b-5949e867cd3a
keywords:
- Windows Media Player Online stores, document ServiceInfo
- magasins en ligne, document ServiceInfo
- type 1 magasins en ligne, document ServiceInfo
- type 2 magasins en ligne, document ServiceInfo
- Document ServiceInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 539c4e1a58e5dbf88e1fc79909791a7dab767ef1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028859"
---
# <a name="serviceinfo-document"></a>Document ServiceInfo

> [!Note]  
> Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.

 

Les magasins en ligne doivent créer le ServiceInfo.xml document. Il s’agit du document utilisé par le magasin en ligne pour configurer l’interface utilisateur du lecteur Windows Media lorsque le lecteur Windows Media 10 ou une version ultérieure héberge la Banque en ligne.

Les éléments suivants et leurs attributs sont pris en charge pour les magasins en ligne du lecteur Windows Media.



| Élément                                      | Description                                                                                                                                                                                                                                                                        |
|----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [AlbumInfo](albuminfo-element.md)           | Spécifie l’URL de la page Web que le lecteur Windows Media affiche lorsque l’utilisateur choisit d’afficher plus d’informations sur un élément multimédia particulier. Type 1 : facultatif<br/> Musique de type 2 : obligatoire<br/> Commerce de type 2 : ignoré<br/>                                |
| [ButtonText](buttontext-element.md)         | Spécifie la chaîne de texte que le lecteur Windows Media affiche pour un bouton du volet des tâches. Type 1 : obligatoire<br/> Musique de type 2 : obligatoire<br/> Commerce de type 2 : obligatoire<br/>                                                                                             |
| [ButtonTip](buttontip-element.md)           | Spécifie l’info-bulle qui s’affiche lorsque l’utilisateur pointe sur un bouton du volet des tâches. Type 1 : facultatif<br/> Tape 2 Music : facultatif<br/> Commerce de type 2 : facultatif<br/>                                                                                         |
| [BuyCD](buycd-element.md)                   | Spécifie les URL des pages Web que le lecteur Windows Media affiche lorsque l’utilisateur choisit d’effectuer un achat. Type 1 : obligatoire<br/> Musique de type 2 : obligatoire<br/> Commerce de type 2 : ignoré<br/>                                                                      |
| [Color](color-element.md)                   | Spécifie la couleur d’arrière-plan des boutons de navigation magasins en ligne. Type 1 : facultatif<br/> Tape 2 Music : facultatif<br/> Commerce de type 2 : facultatif<br/>                                                                                                             |
| [Description](description-element.md)       | Spécifie une description du magasin en ligne qui s’affiche pendant la première expérience de l’utilisateur lors de l’installation du lecteur Windows Media. Requiert le lecteur Windows Media 11. type 1 : obligatoire<br/> Tape 2 Music : facultatif<br/> Commerce de type 2 : facultatif<br/> |
| [DownloadStatus](downloadstatus-element.md) | Spécifie une URL que le lecteur Windows Media affiche sous la forme d’un lien pour permettre aux utilisateurs d’afficher l’état du téléchargement. Type 1 : ignoré<br/> Tape 2 Music : facultatif<br/> Commerce de type 2 : facultatif<br/>                                                                         |
| [FriendlyName](friendlyname-element.md)     | Spécifie la chaîne de texte que le lecteur Windows Media affiche à l’utilisateur pour identifier le magasin en ligne. Type 1 : obligatoire<br/> Musique de type 2 : obligatoire<br/> Commerce de type 2 : obligatoire<br/>                                                                           |
| [HTMLView](htmlview-element.md)             | Spécifie l’URL de base d’une page Web HTMLView. Type 1 : facultatif<br/> Tape 2 Music : facultatif<br/> Commerce de type 2 : facultatif<br/>                                                                                                                                   |
| [Image](image-element.md)                   | Spécifie les images que le lecteur Windows Media affiche à l’utilisateur pour représenter le magasin en ligne. Type 1 : obligatoire<br/> Tape 2 Music : facultatif<br/> Commerce de type 2 : facultatif<br/>                                                                               |
| [Relatif](infocenter-element.md)         | Spécifie l’URL de la page Web affichée par le lecteur Windows Media dans la fonctionnalité d’affichage du centre d’informations de en **cours de lecture** lorsque le magasin en ligne est actif. Type 1 : obligatoire<br/> Musique de type 2 : obligatoire<br/> Commerce de type 2 : ignoré<br/>                           |
| [Installer](install-element.md)               | Spécifie les valeurs utilisées par le programme d’installation du lecteur Windows Media pour installer le magasin en ligne par défaut. Type 1 : obligatoire<br/> Tape 2 Music : facultatif<br/> Commerce de type 2 : ignoré<br/>                                                                                          |
| [Sélectionnez](navigate-element.md)             | Spécifie une URL de base utilisée par les appels à **External. NavigateTaskPaneURL**. Type 1 : facultatif<br/> Tape 2 Music : facultatif<br/> Commerce de type 2 : facultatif<br/>                                                                                                          |
| [ServiceInfo](serviceinfo-element.md)       | Représente l’élément principal pour le document ServiceInfo.xml. Type 1 : obligatoire<br/> Musique de type 2 : obligatoire<br/> Commerce de type 2 : obligatoire<br/>                                                                                                                    |
| [ServiceTask1](servicetask1-element.md)     | Représente le premier volet de tâches du magasin en ligne. Type 1 : obligatoire<br/> Musique de type 2 : obligatoire<br/> Commerce de type 2 : obligatoire<br/>                                                                                                                                     |
| [ServiceTask2](servicetask2-element.md)     | Représente le deuxième volet des tâches du magasin en ligne. Type 1 : ignoré<br/> Tape 2 Music : facultatif<br/> Commerce de type 2 : facultatif<br/>                                                                                                                                     |
| [ServiceTask3](servicetask3-element.md)     | Représente le troisième volet des tâches du magasin en ligne. Type 1 : ignoré<br/> Tape 2 Music : facultatif<br/> Commerce de type 2 : facultatif<br/>                                                                                                                                      |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Exemple de document ServiceInfo pour une boutique en ligne de type 1**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Exemple de document ServiceInfo pour un magasin de type 2 en ligne**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**Informations communes aux magasins en ligne de type 1 et de type 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> </dl>

 

 





