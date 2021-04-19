---
title: À propos de la synchronisation des appareils
description: À propos de la synchronisation des appareils
ms.assetid: 87976357-f819-41ac-9645-36e799876881
keywords:
- Lecteur Windows Media, synchronisation des appareils
- Modèle objet du lecteur Windows Media, synchronisation des appareils
- modèle objet, synchronisation des appareils
- Contrôle ActiveX du lecteur Windows Media, synchronisation des appareils
- Contrôle ActiveX, synchronisation des appareils
- Windows Media Player Mobile contrôle ActiveX, synchronisation des appareils
- Windows Media Player Mobile, synchronisation des appareils
- synchronisation des appareils, à propos de
- synchronisation des appareils, à propos de
- synchronisation des appareils, transfert manuel
- synchronisation des appareils, transfert manuel
- synchronisation des appareils, synchronisation automatique
- synchronisation des appareils, synchronisation automatique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0ad6b6526698def2f7d58ec7afc04c8e22e89c7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106511419"
---
# <a name="about-device-synchronization"></a>À propos de la synchronisation des appareils

Le lecteur Windows Media 10 a introduit un nouveau modèle pour la synchronisation de contenu multimédia numérique avec des appareils portables. Du point de vue de l’utilisateur, cela signifie que vous pouvez spécifier les sélections (y compris les sélections automatiques) à synchroniser automatiquement avec les appareils. Vous pouvez également transférer manuellement du contenu multimédia numérique vers des appareils. Du point de vue du développeur, cela signifie qu’il existe de nouvelles fonctionnalités que vous pouvez exploiter dans vos applications. Pour ce faire, vous devez créer une instance distante du contrôle du lecteur Windows Media.

Il existe deux façons pour un utilisateur de copier du contenu multimédia numérique sur un appareil :

-   **Transfert manuel.** L’utilisateur sélectionne le contenu multimédia numérique dans la bibliothèque, puis lance un transfert du contenu vers l’appareil. Cela est similaire à la fonctionnalité fournie par les versions précédentes du lecteur Windows Media. Le kit de développement logiciel (SDK) du lecteur Windows Media ne fournit pas de méthodes pour transférer des médias numériques sur un appareil.
-   **Synchronisation automatique.** L’utilisateur spécifie les sélections qui se synchronisent automatiquement avec l’appareil. Il s’agit d’une fonctionnalité du lecteur Windows Media 10 ou version ultérieure. Le kit de développement logiciel (SDK) Windows Media Player fournit des fonctionnalités permettant de gérer la synchronisation automatique. Cette fonctionnalité est conçue pour vous permettre de créer une interface utilisateur personnalisée pour votre application afin de spécifier le comportement de la synchronisation des appareils et de fournir des informations d’État aux utilisateurs.

Pour que la synchronisation automatique fonctionne, une relation spéciale doit être établie entre le lecteur Windows Media et l’appareil. Cette relation est appelée *partenariat*.

Les sections suivantes fournissent plus d’informations sur la synchronisation des appareils.

-   [À propos des appareils](about-devices.md)
-   [À propos des partenariats](about-partnerships.md)
-   [À propos du moteur de synchronisation](about-the-synchronization-engine.md)
-   [À propos de la synchronisation des sélections](about-playlist-synchronization.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**À propos du modèle objet Player**](about-the-player-object-model.md)
</dt> <dt>

[**Utilisation à distance du contrôle Windows Media Player**](remoting-the-windows-media-player-control.md)
</dt> <dt>

[**Utilisation d’appareils mobiles**](working-with-portable-devices.md)
</dt> </dl>

 

 




