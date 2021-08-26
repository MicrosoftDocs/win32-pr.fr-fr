---
title: À propos de la synchronisation des appareils
description: À propos de la synchronisation des appareils
ms.assetid: 87976357-f819-41ac-9645-36e799876881
keywords:
- Lecteur Windows Media, synchronisation des appareils
- Lecteur Windows Media modèle objet, synchronisation des appareils
- modèle objet, synchronisation des appareils
- contrôle de ActiveX Lecteur Windows Media, synchronisation des appareils
- contrôle de ActiveX, synchronisation des appareils
- Lecteur Windows Media contrôle des ActiveX mobiles, synchronisation des appareils
- Lecteur Windows Media Mobile, synchronisation des appareils
- synchronisation des appareils, à propos de
- synchronisation des appareils, à propos de
- synchronisation des appareils, transfert manuel
- synchronisation des appareils, transfert manuel
- synchronisation des appareils, synchronisation automatique
- synchronisation des appareils, synchronisation automatique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eed6a03781121a58bee36fd9ff1f74bf21a85347f81384f30c2db5afb4ef3e1f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903559"
---
# <a name="about-device-synchronization"></a>À propos de la synchronisation des appareils

Lecteur Windows Media 10 a introduit un nouveau modèle pour la synchronisation de contenu multimédia numérique avec des appareils portables. Du point de vue de l’utilisateur, cela signifie que vous pouvez spécifier les sélections (y compris les sélections automatiques) à synchroniser automatiquement avec les appareils. Vous pouvez également transférer manuellement du contenu multimédia numérique vers des appareils. Du point de vue du développeur, cela signifie qu’il existe de nouvelles fonctionnalités que vous pouvez exploiter dans vos applications. pour ce faire, vous devez créer une instance distante du contrôle Lecteur Windows Media.

Il existe deux façons pour un utilisateur de copier du contenu multimédia numérique sur un appareil :

-   **Transfert manuel.** L’utilisateur sélectionne le contenu multimédia numérique dans la bibliothèque, puis lance un transfert du contenu vers l’appareil. cela est similaire à la fonctionnalité fournie par les versions précédentes de Lecteur Windows Media. le kit de développement logiciel (SDK) Lecteur Windows Media ne fournit pas de méthodes pour transférer des médias numériques sur un appareil.
-   **Synchronisation automatique.** L’utilisateur spécifie les sélections qui se synchronisent automatiquement avec l’appareil. il s’agit d’une fonctionnalité de Lecteur Windows Media 10 ou version ultérieure. le kit de développement logiciel (SDK) Lecteur Windows Media fournit des fonctionnalités pour la gestion de la synchronisation automatique. Cette fonctionnalité est conçue pour vous permettre de créer une interface utilisateur personnalisée pour votre application afin de spécifier le comportement de la synchronisation des appareils et de fournir des informations d’État aux utilisateurs.

pour que la synchronisation automatique fonctionne, une relation spéciale doit être établie entre Lecteur Windows Media et l’appareil. Cette relation est appelée *partenariat*.

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

 

 




