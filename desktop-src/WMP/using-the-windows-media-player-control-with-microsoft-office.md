---
title: utilisation du contrôle Lecteur Windows Media avec Microsoft Office
description: utilisation du contrôle Lecteur Windows Media avec Microsoft Office
ms.assetid: bc7b2623-8e6d-4af6-b4d0-8087c0159273
keywords:
- Lecteur Windows Media, incorporation ActiveX contrôle
- modèle objet Lecteur Windows Media, incorporation ActiveX contrôle
- modèle objet, incorporation ActiveX contrôle
- Lecteur Windows Media Mobile, incorporation ActiveX contrôle
- contrôle de ActiveX Lecteur Windows Media, incorporation
- Lecteur Windows Media contrôle de ActiveX Mobile, incorporation
- contrôle de ActiveX, incorporation
- Lecteur Windows Media, Office
- Lecteur Windows Media modèle objet, Office
- modèle objet, Office
- Lecteur Windows Media Mobile, Office
- Lecteur Windows Media contrôle ActiveX, Office
- Lecteur Windows Media contrôle de ActiveX Mobile, Office
- contrôle ActiveX, Office
- incorporation de documents Office
- incorporation, Office de documents
- Lecteur Windows Media contrôle ActiveX, Excel
- Lecteur Windows Media contrôle de ActiveX Mobile, Excel
- contrôle ActiveX, Excel
- incorporation, Excel des feuilles de calcul
- incorporation de feuilles de calcul Excel
- Lecteur Windows Media contrôle ActiveX, PowerPoint
- Lecteur Windows Media contrôle de ActiveX Mobile, PowerPoint
- contrôle ActiveX, PowerPoint
- incorporation, PowerPoint diaporamas
- PowerPoint l’incorporation du diaporama
- Lecteur Windows Media ActiveX contrôle, Word
- Lecteur Windows Media contrôle Mobile ActiveX, Word
- contrôle ActiveX, Word
- Incorporation de documents Word
- incorporation, documents Word
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 418c082cad2793e3ebd676c4d648339f9e637f46c7519efc1b426a44b69ee05c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001399"
---
# <a name="using-the-windows-media-player-control-with-microsoft-office"></a>utilisation du contrôle Lecteur Windows Media avec Microsoft Office

cette section décrit comment incorporer la série Lecteur Windows Media 9 ou une version ultérieure ActiveX contrôle dans différents documents créés à l’aide de Microsoft Office XP.

dans Microsoft Word, Excel et PowerPoint®, vous incorporez le contrôle en sélectionnant **objet** dans le menu **insérer** , puis en choisissant **Lecteur Windows Media** dans la liste des types d’objets disponibles. le contrôle Lecteur Windows Media s’affiche dans le document à l’emplacement actuel. vous pouvez ensuite sélectionner le contrôle de mise en **forme** ( **objet de format** dans Excel) dans le menu contextuel du contrôle pour ajuster la disposition, le style d’habillage du texte et d’autres options de mise en forme. dans Word et Excel, vous devez être en mode design pour effectuer cette opération.

Une fois que vous avez placé et mis en forme le contrôle, vous pouvez le configurer à l’aide de la boîte de dialogue **Propriétés** , accessible à partir de la boîte **à outils contrôle** ou du menu contextuel en mode création pour Word et Excel. Ici, vous pouvez spécifier des propriétés de contrôle du lecteur de base, telles que le nom du contrôle, l’URL d’un fichier multimédia numérique et le mode de l’interface utilisateur. si vous affectez à la propriété **uiMode** la valeur « none », tous les éléments du contrôle sont masqués à l’exception de la fenêtre vidéo ou de visualisation, ce qui vous permet d’ajouter vos propres boutons et d’écrire du code de script à l’aide de Visual Basic pour Applications (VBA) pour gérer les clics de bouton et les événements de contrôle de joueur.

à partir de la boîte de dialogue **propriétés** de base, vous pouvez également accéder à la boîte de dialogue **propriétés du contrôle de Lecteur Windows Media** plus sophistiquées en double-cliquant sur la ligne « (personnalisée) » ou en cliquant sur le bouton de sélection (« ... ») après avoir sélectionné cette ligne. À partir de cette boîte de dialogue, vous pouvez modifier toutes les propriétés de contrôle de lecteur disponibles.

> [!Note]  
> Vous devez veiller à ne pas effectuer d’actions dans les gestionnaires d’événements de contrôle de lecteur qui entraînent la destruction du contrôle. par exemple, si vous incorporez le contrôle Lecteur Windows Media sur une diapositive dans une présentation PowerPoint, n’appelez pas la méthode PowerPoint **Next** à partir de l’événement **openStateChange** Player ou d’un autre événement.

 

> [!Note]  
> En outre, vous ne devez pas définir la propriété **Player. URL** à partir d’un gestionnaire d’événements de contrôle de joueur.

 

dans FrontPage, ajoutez le contrôle Lecteur Windows Media à une page web en sélectionnant **composant Web** dans le menu **insertion** . dans la boîte de dialogue **insérer un composant Web** , sélectionnez **contrôles avancés** dans la liste **type de composant** , puis sélectionnez **ActiveX contrôle** dans la liste des options de contrôle. dans la fenêtre suivante de la boîte de dialogue, sélectionnez **Lecteur Windows Media**. si elle ne figure pas dans la liste, cliquez sur **personnaliser** , puis activez la case à cocher **Lecteur Windows Media** dans la liste de **contrôles** .

une fois le contrôle Lecteur Windows Media incorporé, vous pouvez le positionner et le redimensionner, puis modifier ses propriétés en sélectionnant **ActiveX propriétés du contrôle** dans le menu contextuel du contrôle. dans l’affichage HTML, les valeurs de propriété que vous spécifiez s’affichent dans l’élément objet représentant le contrôle Lecteur Windows Media. Le nom de l’objet apparaît en tant qu’attribut d’ID, et les propriétés du contrôle apparaissent en tant que balises PARAM. le nom de l’objet vous donne accès au modèle objet de contrôle Lecteur Windows Media, que vous pouvez programmer à l’aide de Microsoft JScript. pour plus d’informations, consultez [utilisation du contrôle Lecteur Windows Media dans une Page Web](using-the-windows-media-player-control-in-a-web-page.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Guide de contrôle du lecteur**](player-control-guide.md)
</dt> </dl>

 

 




