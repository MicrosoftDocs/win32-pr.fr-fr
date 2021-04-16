---
title: Modèle objet de lecteur pour les langages de script
description: Modèle objet de lecteur pour les langages de script
ms.assetid: 785c1a3a-902a-4f30-8419-bbfb11b584a3
keywords:
- Lecteur Windows Media, modèle objet
- Windows Media Player Object Model, à propos de
- modèle objet, à propos de
- Contrôle ActiveX du lecteur Windows Media, modèle objet
- Contrôle ActiveX, modèle objet
- Windows Media Player Mobile contrôle ActiveX, modèle objet
- Windows Media Player Mobile, modèle objet
- Kit de développement logiciel (SDK), modèle objet de contrôle ActiveX du lecteur Windows Media
- SDK (kit de développement logiciel), modèle objet de contrôle ActiveX du lecteur Windows Media
- documentation, modèle objet de contrôle ActiveX du lecteur Windows Media
- Windows Media Player, langages de script
- Windows Media Player Object Model, langages de script
- modèle objet, langages de script
- Contrôle ActiveX du lecteur Windows Media, langages de script
- Contrôle ActiveX, langages de script
- Windows Media Player Mobile contrôle ActiveX, langages de script
- Windows Media Player Mobile, langages de script
- langages de script
- Lecteur Windows Media, objet Player
- Modèle objet du lecteur Windows Media, objet Player
- modèle objet, objet Player
- Contrôle ActiveX du lecteur Windows Media, objet Player
- Contrôle ActiveX, objet Player
- Windows Media Player Mobile contrôle ActiveX, objet Player
- Windows Media Player Mobile, objet Player
- Objet Player
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 670bff03075fd98812dbee269115e297a137e92d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104571074"
---
# <a name="player-object-model-for-scripting-languages"></a>Modèle objet de lecteur pour les langages de script

ActiveX utilise le concept d’objets pour contenir des fonctionnalités de programmation. Le lecteur Windows Media utilise plusieurs objets pour diviser les fonctionnalités fournies par le contrôle. L’objet racine est l’objet **Player** , et les autres objets sont attachés à l’objet **Player** par le biais de propriétés spécifiques.

Le diagramme suivant montre comment le modèle objet de contrôle ActiveX du lecteur Windows Media 11 fonctionne pour les langages de script.

![diagramme du modèle objet du lecteur Windows Media 11](images/playeromdiag.png)

En C++ et parfois dans les langages .NET, les objets sont représentés par des interfaces COM. Dans le modèle objet du lecteur Windows Media, les noms d’interface COM sont identiques au nom de l’objet, mais ils portent le préfixe « IWMP ». Par exemple, l’objet **réseau** est exposé via l’interface **IWMPNetwork** .

Les sections suivantes fournissent des vues d’ensemble conceptuelles pour chaque objet :

-   [À propos des objets cdrom et CdromCollection](about-the-cdrom-and-cdromcollection-objects.md)
-   [À propos de l’objet ClosedCaption](about-the-closedcaption-object.md)
-   [À propos de l’objet contrôles](about-the-controls-object.md)
-   [À propos de l’objet DVD](about-the-dvd-object.md)
-   [À propos des objets Error et ErrorItem](about-the-error-and-erroritem-objects.md)
-   [À propos des objets MediaCollection et Media](about-the-mediacollection-and-media-objects.md)
-   [À propos de l’objet MetadataPicture](about-the-metadatapicture-object.md)
-   [À propos de l’objet MetadataText](about-the-metadatatext-object.md)
-   [À propos de l’objet réseau](about-the-network-object.md)
-   [À propos de l’objet Player](about-the-player-object.md)
-   [À propos de l’objet PlayerApplication](about-the-playerapplication-object.md)
-   [À propos des objets playlist, PlaylistCollection et PlaylistArray](about-the-playlist--playlistcollection--and-playlistarray-objects.md)
-   [À propos de l’objet de requête](about-the-query-object.md)
-   [À propos de l’objet Settings](about-the-settings-object.md)
-   [À propos de l’objet StringCollection](about-the-stringcollection-object.md)

Des fonctionnalités supplémentaires sont disponibles par le biais de certaines interfaces COM. La possibilité d’accéder à ces interfaces peut dépendre du langage que vous utilisez pour la programmation et d’autres facteurs, tels que le mode utilisé pour créer l’instance du contrôle du lecteur Windows Media. Pour obtenir la liste complète des interfaces COM exposées par le contrôle du lecteur Windows Media, consultez la [Référence du modèle objet pour C++](object-model-reference-for-c.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**À propos du modèle objet Player**](about-the-player-object-model.md)
</dt> <dt>

[**Utilisation du contrôle du lecteur Windows Media dans une solution .NET Framework**](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> </dl>

 

 




