---
title: Utilisation du contrôle du lecteur Windows Media avec Visual Basic
description: Utilisation du contrôle du lecteur Windows Media avec Visual Basic
ms.assetid: 83e5440b-096b-42e1-9038-d779895d9519
keywords:
- Lecteur Windows Media, incorporer un contrôle ActiveX
- Modèle objet du lecteur Windows Media, incorporer un contrôle ActiveX
- modèle objet, incorporer un contrôle ActiveX
- Windows Media Player Mobile, incorporer un contrôle ActiveX
- Contrôle ActiveX du lecteur Windows Media, incorporation
- Windows Media Player Mobile, contrôle ActiveX, incorporation
- Contrôle ActiveX, incorporation
- Lecteur Windows Media, Visual Basic
- Windows Media Player Object Model, Visual Basic
- modèle objet, Visual Basic
- Windows Media Player Mobile, Visual Basic
- Contrôle ActiveX du lecteur Windows Media, Visual Basic
- Contrôle ActiveX Windows Media Player Mobile, Visual Basic
- Contrôle ActiveX, Visual Basic
- Incorporation de programmes basés sur Visual Basic
- incorporation, programmes basés sur des Visual Basic
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8f2ddd78fe5a254f5bf699fbd2557f1e8700c73
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310458"
---
# <a name="using-the-windows-media-player-control-with-visual-basic"></a>Utilisation du contrôle du lecteur Windows Media avec Visual Basic

Cette section décrit comment utiliser le contrôle ActiveX du lecteur Windows Media série 9 ou une version ultérieure dans les applications créées avec Microsoft Visual Basic 6,0.

## <a name="getting-started"></a>Mise en route

Pour ajouter le contrôle du lecteur Windows Media à la boîte à outils, commencez par sélectionner **composants** dans le menu **projet** . Dans la boîte de dialogue composants, activez la case à cocher en regard de « lecteur Windows Media ». En bas de la boîte de dialogue, vérifiez que le fichier sélectionné est wmp.dll. Après avoir fermé la boîte de dialogue, vous pouvez placer une instance du contrôle du lecteur Windows Media sur votre formulaire de la façon habituelle.

Vous pouvez définir de nombreuses propriétés de contrôle à l’aide de l’Fenêtre Propriétés. Pour définir certaines propriétés, vous devez utiliser la boîte de dialogue Propriétés du lecteur Windows Media, que vous ouvrez à l’aide de l’élément « (personnalisé) » dans le Fenêtre Propriétés.

## <a name="object-references"></a>Références d'objet

Vous utilisez certaines propriétés de contrôle de lecteur pour récupérer des références à des objets particuliers. Par exemple, la propriété **cdromCollection** retourne une référence à un objet **cdromCollection** . Vous devez assigner une telle référence à une variable que vous avez déclarée en tant qu’interface correspondante. Dans le cas de la propriété **cdromCollection** , par exemple, vous affectez sa valeur de retour à une variable de type **IWMPCdromCollection**.

Lisez la rubrique [interfaces](interfaces.md) dans la [Référence du modèle objet pour C++](object-model-reference-for-c.md) afin d’identifier les objets qui implémentent plusieurs interfaces. Dans ce cas, vous devez déclarer une variable objet en tant qu’interface avec un numéro le plus élevé documenté dans ce kit de développement logiciel (SDK) pour accéder à toutes les propriétés et méthodes de cet objet. Par exemple, vous devez affecter la valeur de la propriété **currentMedia** du contrôle du lecteur Windows Media à une variable déclarée comme **IWMPMedia3** pour vous assurer que vous avez accès aux méthodes **getAttributeCountByType** et **getItemInfoByType** .

> [!Note]  
> L’objet **WindowsMediaPlayer** implémente toutes les propriétés et méthodes des interfaces **IWMPCore**, **IWMPCore2**, **IWMPCore3**, **IWMPPlayer**, **IWMPPlayer2**, **IWMPPlayer3** et **IWMPPlayer4** . Vous n’avez pas besoin de déclarer des variables distinctes pour l’une de ces interfaces. Vous pouvez accéder à l’ensemble de ses membres à l’aide du nom que vous avez attribué à votre instance **WindowsMediaPlayer** .

 

Dans l’Explorateur d’objets Visual Basic, vous verrez de nombreuses interfaces destinées à une utilisation privée par le contrôle du lecteur Windows Media, y compris certains qui prennent en charge les développeurs d’apparences. Vous devez utiliser uniquement les objets, les propriétés, les méthodes et les événements documentés dans ce kit de développement logiciel (SDK).

## <a name="additional-tips"></a>Conseils supplémentaires

-   La documentation de référence montre la syntaxe JScript. En JScript, les arguments passés aux méthodes sont toujours placés entre parenthèses. Dans Visual Basic 6,0, les arguments passés aux méthodes qui ne retournent pas de valeur ne doivent pas être placés entre parenthèses.
-   Certaines propriétés ou méthodes peuvent ne pas s’afficher dans la fonctionnalité de saisie semi-automatique de code dans le Visual Basic éditeur de code. Vous pouvez toujours utiliser ces membres en tapant leurs noms exactement tels qu’ils apparaissent dans cette documentation.
-   Gérez l’apparence visuelle du contrôle à l’aide de la propriété **UIMODE** . Vous pouvez le faire de deux manières. Vous pouvez utiliser la liste déroulante **Sélectionner un mode** dans la boîte de dialogue Propriétés du lecteur Windows Media, ou vous pouvez taper la valeur correcte dans la fenêtre Propriétés.

    En particulier, n’utilisez pas la propriété **visible** pour masquer le contrôle. Affectez plutôt la valeur « invisible » à la propriété **UIMODE** .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Guide de contrôle du lecteur**](player-control-guide.md)
</dt> </dl>

 

 




