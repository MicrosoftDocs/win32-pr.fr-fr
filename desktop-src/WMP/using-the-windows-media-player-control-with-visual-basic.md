---
title: utilisation du contrôle Lecteur Windows Media avec Visual Basic
description: utilisation du contrôle Lecteur Windows Media avec Visual Basic
ms.assetid: 83e5440b-096b-42e1-9038-d779895d9519
keywords:
- Lecteur Windows Media, incorporation ActiveX contrôle
- modèle objet Lecteur Windows Media, incorporation ActiveX contrôle
- modèle objet, incorporation ActiveX contrôle
- Lecteur Windows Media Mobile, incorporation ActiveX contrôle
- contrôle de ActiveX Lecteur Windows Media, incorporation
- Lecteur Windows Media contrôle de ActiveX Mobile, incorporation
- contrôle de ActiveX, incorporation
- Lecteur Windows Media, Visual Basic
- Lecteur Windows Media modèle objet, Visual Basic
- modèle objet, Visual Basic
- Lecteur Windows Media Mobile, Visual Basic
- Lecteur Windows Media contrôle ActiveX, Visual Basic
- Lecteur Windows Media contrôle de ActiveX Mobile, Visual Basic
- contrôle ActiveX, Visual Basic
- incorporation de programmes basés sur Visual Basic
- incorporation, programmes basés sur des Visual Basic
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b90c03e4b55644b8eceba837b7dfbde15992be7469b102a6194c8a08af1cb73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134272"
---
# <a name="using-the-windows-media-player-control-with-visual-basic"></a>utilisation du contrôle Lecteur Windows Media avec Visual Basic

cette section décrit comment utiliser le contrôle de la série Lecteur Windows Media 9 ou version ultérieure ActiveX dans les applications créées avec Microsoft Visual Basic 6,0.

## <a name="getting-started"></a>Mise en route

pour ajouter le contrôle Lecteur Windows Media à la boîte à outils, commencez par sélectionner des **composants** dans le menu **Project** . dans la boîte de dialogue composants, activez la case à cocher en regard de « Lecteur Windows Media ». En bas de la boîte de dialogue, vérifiez que le fichier sélectionné est wmp.dll. après avoir fermé la boîte de dialogue, vous pouvez placer une instance du contrôle Lecteur Windows Media sur votre formulaire de la façon habituelle.

Vous pouvez définir de nombreuses propriétés de contrôle à l’aide de l’Fenêtre Propriétés. pour définir certaines propriétés, vous devez utiliser la boîte de dialogue propriétés de la Lecteur Windows Media, que vous ouvrez à l’aide de l’élément « (personnalisé) » dans le Fenêtre Propriétés.

## <a name="object-references"></a>Références d'objet

Vous utilisez certaines propriétés de contrôle de lecteur pour récupérer des références à des objets particuliers. Par exemple, la propriété **cdromCollection** retourne une référence à un objet **cdromCollection** . Vous devez assigner une telle référence à une variable que vous avez déclarée en tant qu’interface correspondante. Dans le cas de la propriété **cdromCollection** , par exemple, vous affectez sa valeur de retour à une variable de type **IWMPCdromCollection**.

Lisez la rubrique [interfaces](interfaces.md) dans la [Référence du modèle objet pour C++](object-model-reference-for-c.md) afin d’identifier les objets qui implémentent plusieurs interfaces. Dans ce cas, vous devez déclarer une variable objet en tant qu’interface avec un numéro le plus élevé documenté dans ce kit de développement logiciel (SDK) pour accéder à toutes les propriétés et méthodes de cet objet. par exemple, vous devez affecter la valeur de la propriété de contrôle de Lecteur Windows Media **currentMedia** à une variable déclarée comme **IWMPMedia3** pour vous assurer que vous avez accès aux méthodes **getAttributeCountByType** et **getItemInfoByType** .

> [!Note]  
> L’objet **WindowsMediaPlayer** implémente toutes les propriétés et méthodes des interfaces **IWMPCore**, **IWMPCore2**, **IWMPCore3**, **IWMPPlayer**, **IWMPPlayer2**, **IWMPPlayer3** et **IWMPPlayer4** . Vous n’avez pas besoin de déclarer des variables distinctes pour l’une de ces interfaces. Vous pouvez accéder à l’ensemble de ses membres à l’aide du nom que vous avez attribué à votre instance **WindowsMediaPlayer** .

 

dans l’explorateur d’objets Visual Basic, vous verrez de nombreuses interfaces destinées à une utilisation privée par le contrôle Lecteur Windows Media, y compris certains qui prennent en charge les développeurs d’apparences. Vous devez utiliser uniquement les objets, les propriétés, les méthodes et les événements documentés dans ce kit de développement logiciel (SDK).

## <a name="additional-tips"></a>Conseils supplémentaires

-   la documentation de référence montre JScript syntaxe. dans JScript, les arguments passés aux méthodes sont toujours placés entre parenthèses. dans Visual Basic 6,0, les arguments passés aux méthodes qui ne retournent pas de valeur ne doivent pas être placés entre parenthèses.
-   certaines propriétés ou méthodes peuvent ne pas s’afficher dans la fonctionnalité de saisie semi-automatique de code dans le Visual Basic éditeur de code. Vous pouvez toujours utiliser ces membres en tapant leurs noms exactement tels qu’ils apparaissent dans cette documentation.
-   Gérez l’apparence visuelle du contrôle à l’aide de la propriété **UIMODE** . Vous pouvez le faire de deux manières. vous pouvez utiliser la liste déroulante **sélectionner un mode** dans la boîte de dialogue propriétés du Lecteur Windows Media, ou vous pouvez taper la valeur correcte dans la Fenêtre Propriétés.

    En particulier, n’utilisez pas la propriété **visible** pour masquer le contrôle. Affectez plutôt la valeur « invisible » à la propriété **UIMODE** .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Guide de contrôle du lecteur**](player-control-guide.md)
</dt> </dl>

 

 




