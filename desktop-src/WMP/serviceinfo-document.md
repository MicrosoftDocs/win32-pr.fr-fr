---
title: Document ServiceInfo
description: Document ServiceInfo
ms.assetid: 48f84dd7-e458-4da2-ae2b-5949e867cd3a
keywords:
- Lecteur Windows Media les magasins en ligne, document ServiceInfo
- magasins en ligne, document ServiceInfo
- type 1 magasins en ligne, document ServiceInfo
- type 2 magasins en ligne, document ServiceInfo
- Document ServiceInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88863bb75cd0a7b85bead1c20759b77710c2db483b4d9e48ed1f53741dd0840d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995419"
---
# <a name="serviceinfo-document"></a>Document ServiceInfo

> [!Note]  
> Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.

 

Les magasins en ligne doivent créer le ServiceInfo.xml document. il s’agit du document utilisé par le magasin en ligne pour configurer l’interface utilisateur Lecteur Windows Media lorsque Lecteur Windows Media 10 ou version ultérieure héberge le magasin en ligne.

les éléments suivants et leurs attributs sont pris en charge pour les Lecteur Windows Media les magasins en ligne.



| Élément                                      | Description                                                                                                                                                                                                                                                                        |
|----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [AlbumInfo](albuminfo-element.md)           | spécifie l’URL de la page web qui Lecteur Windows Media s’affiche lorsque l’utilisateur choisit d’afficher plus d’informations sur un élément multimédia particulier. Type 1 : facultatif<br/> Musique de Type 2 : obligatoire<br/> Commerce de type 2 : ignoré<br/>                                |
| [ButtonText](buttontext-element.md)         | spécifie la chaîne de texte qui Lecteur Windows Media s’affiche pour un bouton du volet des tâches. Type 1 : obligatoire<br/> Musique de Type 2 : obligatoire<br/> Commerce de type 2 : obligatoire<br/>                                                                                             |
| [ButtonTip](buttontip-element.md)           | Spécifie l’info-bulle qui s’affiche lorsque l’utilisateur pointe sur un bouton du volet des tâches. Type 1 : facultatif<br/> Musique de Type 2 : facultatif<br/> Commerce de type 2 : facultatif<br/>                                                                                         |
| [BuyCD](buycd-element.md)                   | spécifie les url des pages web qui Lecteur Windows Media s’affichent lorsque l’utilisateur choisit d’effectuer un achat. Type 1 : obligatoire<br/> Musique de Type 2 : obligatoire<br/> Commerce de type 2 : ignoré<br/>                                                                      |
| [Couleur](color-element.md)                   | Spécifie la couleur d’arrière-plan des boutons de navigation magasins en ligne. Type 1 : facultatif<br/> Musique de Type 2 : facultatif<br/> Commerce de type 2 : facultatif<br/>                                                                                                             |
| [Description](description-element.md)       | spécifie une description du magasin en ligne qui s’affiche pendant la première expérience de l’utilisateur avec une installation de Lecteur Windows Media. requiert Lecteur Windows Media 11. Type 1 : obligatoire<br/> Musique de Type 2 : facultatif<br/> Commerce de type 2 : facultatif<br/> |
| [DownloadStatus](downloadstatus-element.md) | spécifie l’URL que le Lecteur Windows Media affiche sous la forme d’un lien pour permettre aux utilisateurs d’afficher l’état du téléchargement. Type 1 : ignoré<br/> Musique de Type 2 : facultatif<br/> Commerce de type 2 : facultatif<br/>                                                                         |
| [FriendlyName](friendlyname-element.md)     | spécifie la chaîne de texte que Lecteur Windows Media affiche à l’utilisateur pour identifier le magasin en ligne. Type 1 : obligatoire<br/> Musique de Type 2 : obligatoire<br/> Commerce de type 2 : obligatoire<br/>                                                                           |
| [HTMLView](htmlview-element.md)             | Spécifie l’URL de base d’une page Web HTMLView. Type 1 : facultatif<br/> Musique de Type 2 : facultatif<br/> Commerce de type 2 : facultatif<br/>                                                                                                                                   |
| [Image](image-element.md)                   | spécifie les images que Lecteur Windows Media affiche à l’utilisateur pour représenter le magasin en ligne. Type 1 : obligatoire<br/> Musique de Type 2 : facultatif<br/> Commerce de type 2 : facultatif<br/>                                                                               |
| [Relatif](infocenter-element.md)         | spécifie l’URL de la page web que Lecteur Windows Media affiche dans la fonctionnalité d’affichage du centre d’informations de en **cours** d’exécution lorsque le magasin en ligne est actif. Type 1 : obligatoire<br/> Musique de Type 2 : obligatoire<br/> Commerce de type 2 : ignoré<br/>                           |
| [Installer](install-element.md)               | spécifie les valeurs utilisées par le programme d’installation de Lecteur Windows Media pour installer le magasin en ligne par défaut. Type 1 : obligatoire<br/> Musique de Type 2 : facultatif<br/> Commerce de type 2 : ignoré<br/>                                                                                          |
| [Sélectionnez](navigate-element.md)             | Spécifie une URL de base utilisée par les appels à **External. NavigateTaskPaneURL**. Type 1 : facultatif<br/> Musique de Type 2 : facultatif<br/> Commerce de type 2 : facultatif<br/>                                                                                                          |
| [ServiceInfo](serviceinfo-element.md)       | Représente l’élément principal pour le document ServiceInfo.xml. Type 1 : obligatoire<br/> Musique de Type 2 : obligatoire<br/> Commerce de type 2 : obligatoire<br/>                                                                                                                    |
| [ServiceTask1](servicetask1-element.md)     | Représente le premier volet de tâches du magasin en ligne. Type 1 : obligatoire<br/> Musique de Type 2 : obligatoire<br/> Commerce de type 2 : obligatoire<br/>                                                                                                                                     |
| [ServiceTask2](servicetask2-element.md)     | Représente le deuxième volet des tâches du magasin en ligne. Type 1 : ignoré<br/> Musique de Type 2 : facultatif<br/> Commerce de type 2 : facultatif<br/>                                                                                                                                     |
| [ServiceTask3](servicetask3-element.md)     | Représente le troisième volet des tâches du magasin en ligne. Type 1 : ignoré<br/> Musique de Type 2 : facultatif<br/> Commerce de type 2 : facultatif<br/>                                                                                                                                      |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Exemple de document ServiceInfo pour une boutique en ligne de type 1**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Exemple de document ServiceInfo pour un magasin de type 2 en ligne**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**Informations communes aux magasins en ligne de type 1 et de type 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> </dl>

 

 





