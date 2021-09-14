---
title: Modèle objet de lecteur pour les langages de script
description: Modèle objet de lecteur pour les langages de script
ms.assetid: 785c1a3a-902a-4f30-8419-bbfb11b584a3
keywords:
- Lecteur Windows Media, modèle objet
- Lecteur Windows Media modèle objet, à propos de
- modèle objet, à propos de
- contrôle ActiveX Lecteur Windows Media, modèle objet
- contrôle ActiveX, modèle objet
- Lecteur Windows Media contrôle Mobile ActiveX, modèle objet
- Lecteur Windows Media Mobile, modèle objet
- kit de développement logiciel (SDK), Lecteur Windows Media ActiveX modèle objet de contrôle
- SDK (kit de développement logiciel), Lecteur Windows Media ActiveX modèle objet de contrôle
- documentation, Lecteur Windows Media ActiveX modèle objet de contrôle
- Lecteur Windows Media, langages de script
- Lecteur Windows Media modèle objet, langages de script
- modèle objet, langages de script
- contrôle de ActiveX Lecteur Windows Media, langages de script
- contrôle de ActiveX, langages de script
- Lecteur Windows Media contrôle de ActiveX Mobile, langages de script
- Lecteur Windows Media Mobile, langages de script
- langages de script
- Lecteur Windows Media, objet Player
- Lecteur Windows Media modèle objet, objet Player
- modèle objet, objet Player
- contrôle ActiveX Lecteur Windows Media, objet Player
- contrôle ActiveX, objet Player
- Lecteur Windows Media contrôle Mobile ActiveX, objet Player
- Lecteur Windows Media Mobile, objet Player
- Objet Player
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 670bff03075fd98812dbee269115e297a137e92d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127122693"
---
# <a name="player-object-model-for-scripting-languages"></a>Modèle objet de lecteur pour les langages de script

ActiveX utilise le concept d’objets pour contenir des fonctionnalités de programmation. Lecteur Windows Media utilise plusieurs objets pour diviser les fonctionnalités fournies par le contrôle. L’objet racine est l’objet **Player** , et les autres objets sont attachés à l’objet **Player** par le biais de propriétés spécifiques.

le diagramme suivant montre comment le modèle objet de contrôle Lecteur Windows Media 11 ActiveX fonctionne pour les langages de script.

![diagramme du modèle objet du lecteur Windows Media 11](images/playeromdiag.png)

En C++ et parfois dans les langages .NET, les objets sont représentés par des interfaces COM. dans le modèle objet Lecteur Windows Media, les noms d’interface COM sont identiques au nom de l’objet, mais ils portent le préfixe « IWMP ». Par exemple, l’objet **réseau** est exposé via l’interface **IWMPNetwork** .

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
-   [à propos de l’objet Paramètres](about-the-settings-object.md)
-   [À propos de l’objet StringCollection](about-the-stringcollection-object.md)

Des fonctionnalités supplémentaires sont disponibles par le biais de certaines interfaces COM. la possibilité d’accéder à ces interfaces peut dépendre du langage que vous utilisez pour la programmation et d’autres facteurs, tels que le mode utilisé pour créer l’instance du contrôle Lecteur Windows Media. pour obtenir la liste complète des interfaces COM exposées par le contrôle Lecteur Windows Media, consultez la [référence du modèle objet pour C++](object-model-reference-for-c.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**À propos du modèle objet Player**](about-the-player-object-model.md)
</dt> <dt>

[**utilisation du contrôle Lecteur Windows Media dans une Solution .NET Framework**](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> </dl>

 

 




