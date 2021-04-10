---
title: Utilisation du contrôle du lecteur Windows Media avec Microsoft Office
description: Utilisation du contrôle du lecteur Windows Media avec Microsoft Office
ms.assetid: bc7b2623-8e6d-4af6-b4d0-8087c0159273
keywords:
- Lecteur Windows Media, incorporer un contrôle ActiveX
- Modèle objet du lecteur Windows Media, incorporer un contrôle ActiveX
- modèle objet, incorporer un contrôle ActiveX
- Windows Media Player Mobile, incorporer un contrôle ActiveX
- Contrôle ActiveX du lecteur Windows Media, incorporation
- Windows Media Player Mobile, contrôle ActiveX, incorporation
- Contrôle ActiveX, incorporation
- Windows Media Player, Office
- Windows Media Player Object Model, Office
- modèle objet, Office
- Windows Media Player Mobile, Office
- Contrôle ActiveX du lecteur Windows Media, Office
- Windows Media Player Mobile, contrôle ActiveX, Office
- Contrôle ActiveX, Office
- Incorporation de documents Office
- incorporation, documents Office
- Contrôle ActiveX du lecteur Windows Media, Excel
- Contrôle ActiveX Windows Media Player Mobile, Excel
- Contrôle ActiveX, Excel
- incorporation, feuilles de calcul Excel
- Incorporation dans une feuille de calcul Excel
- Contrôle ActiveX du lecteur Windows Media, PowerPoint
- Windows Media Player Mobile contrôle ActiveX, PowerPoint
- Contrôle ActiveX, PowerPoint
- incorporation, diaporamas PowerPoint
- Incorporation de diaporama PowerPoint
- Windows Media Player ActiveX (contrôle), Word
- Windows Media Player Mobile contrôle ActiveX, Word
- Contrôle ActiveX, Word
- Incorporation de documents Word
- incorporation, documents Word
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2504b46b4fb409dede108c41b43014c3aaeae5ec
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940024"
---
# <a name="using-the-windows-media-player-control-with-microsoft-office"></a>Utilisation du contrôle du lecteur Windows Media avec Microsoft Office

Cette section explique comment incorporer le contrôle ActiveX du lecteur Windows Media série 9 ou ultérieur dans différents documents créés à l’aide de Microsoft Office XP.

Dans Microsoft Word, Excel et PowerPoint®, vous incorporez le contrôle en sélectionnant **objet** dans le menu **insertion** , puis en choisissant **lecteur Windows Media** dans la liste des types d’objets disponibles. Le contrôle du lecteur Windows Media apparaît dans le document à l’emplacement actuel. Vous pouvez ensuite sélectionner le contrôle de mise en **forme** (mettre en **forme l’objet** dans Excel) dans le menu contextuel du contrôle pour ajuster la disposition, le style d’habillage du texte et d’autres options de mise en forme. Dans Word et Excel, vous devez être en mode création pour effectuer cette opération.

Une fois que vous avez placé et mis en forme le contrôle, vous pouvez le configurer à l’aide de la boîte de dialogue **Propriétés** , accessible à partir de la boîte **à outils contrôle** ou du menu contextuel en mode création pour Word et Excel. Ici, vous pouvez spécifier des propriétés de contrôle du lecteur de base, telles que le nom du contrôle, l’URL d’un fichier multimédia numérique et le mode de l’interface utilisateur. Si vous affectez à la propriété **UIMODE** la valeur « None », tous les éléments du contrôle sont masqués à l’exception de la fenêtre vidéo ou de visualisation, ce qui vous permet d’ajouter vos propres boutons et d’écrire du code de script à l’aide de Visual Basic pour applications (VBA) pour gérer les clics de bouton et les événements de contrôle de joueur.

À partir de la boîte de dialogue **Propriétés** de base, vous pouvez également accéder à la boîte de dialogue **Propriétés du contrôle du lecteur Windows Media** plus sophistiqué en double-cliquant sur la ligne « (personnalisé) » ou en cliquant sur le bouton de sélection (« ... ») après avoir sélectionné cette ligne. À partir de cette boîte de dialogue, vous pouvez modifier toutes les propriétés de contrôle de lecteur disponibles.

> [!Note]  
> Vous devez veiller à ne pas effectuer d’actions dans les gestionnaires d’événements de contrôle de lecteur qui entraînent la destruction du contrôle. Par exemple, si vous incorporez le contrôle du lecteur Windows Media sur une diapositive d’une présentation PowerPoint, n’appelez pas la méthode PowerPoint **Next** à partir de l’événement **openStateChange** Player ou d’un autre événement.

 

> [!Note]  
> En outre, vous ne devez pas définir la propriété **Player. URL** à partir d’un gestionnaire d’événements de contrôle de joueur.

 

Dans FrontPage, ajoutez le contrôle du lecteur Windows Media à une page Web en sélectionnant **composant Web** dans le menu **insertion** . Dans la boîte de dialogue **Insérer un composant Web** , sélectionnez **contrôles avancés** dans la liste **type de composant** , puis sélectionnez **contrôle ActiveX** dans la liste des options de contrôle. Dans la fenêtre suivante de la boîte de dialogue, sélectionnez **lecteur Windows Media**. Si elle ne figure pas dans la liste, cliquez sur **personnaliser** , puis activez la case à cocher **lecteur Windows Media** dans la liste de **contrôles** .

Une fois le contrôle du lecteur Windows Media incorporé, vous pouvez le positionner et le redimensionner, puis modifier ses propriétés en sélectionnant **Propriétés du contrôle ActiveX** dans le menu contextuel du contrôle. Dans l’affichage HTML, les valeurs de propriété que vous spécifiez s’affichent dans l’élément objet représentant le contrôle du lecteur Windows Media. Le nom de l’objet apparaît en tant qu’attribut d’ID, et les propriétés du contrôle apparaissent en tant que balises PARAM. Le nom de l’objet vous permet d’accéder au modèle objet de contrôle du lecteur Windows Media, que vous pouvez programmer à l’aide de Microsoft JScript. Pour plus d’informations, consultez [utilisation du contrôle du lecteur Windows Media dans une page Web](using-the-windows-media-player-control-in-a-web-page.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Guide de contrôle du lecteur**](player-control-guide.md)
</dt> </dl>

 

 




