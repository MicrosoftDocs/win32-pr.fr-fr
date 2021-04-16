---
title: À propos du moteur de synchronisation
description: À propos du moteur de synchronisation
ms.assetid: bb57ffb0-3833-463b-b66c-c23224fa2ba7
keywords:
- Lecteur Windows Media, moteur de synchronisation
- Modèle objet du lecteur Windows Media, moteur de synchronisation
- modèle objet, moteur de synchronisation
- Contrôle Windows Media Player ActiveX, moteur de synchronisation
- Contrôle ActiveX, moteur de synchronisation
- Contrôle ActiveX Windows Media Player Mobile, moteur de synchronisation
- Lecteur Windows Media Mobile, moteur de synchronisation
- synchronisation des appareils, moteur de synchronisation
- synchronisation des appareils, moteur de synchronisation
- moteur de synchronisation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfe0768c4805b074fdaf628a25daf47b9ced97ee
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104381533"
---
# <a name="about-the-synchronization-engine"></a>À propos du moteur de synchronisation

Le moteur de synchronisation est le composant du lecteur Windows Media qui gère la copie de contenu multimédia numérique sur des appareils mobiles. Le lecteur Windows Media prend en charge une seule instance du moteur de synchronisation pour chaque appareil. Vous devez utiliser une instance distante du contrôle du lecteur Windows Media pour effectuer des tâches de synchronisation par programme. En effet, votre programme partage les instances du moteur de synchronisation avec le lecteur Windows Media et tous les autres programmes qui utilisent les interfaces du lecteur pour la synchronisation des appareils.

Vous pouvez utiliser [IWMPSyncDevice :: Start](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-start) et [IWMPSyncDevice :: Stop](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-stop) pour contrôler le moment où le moteur de synchronisation effectue son travail. Dans la plupart des cas, vous ne devez pas utiliser ces méthodes. Au lieu de cela, vous devez laisser le moteur de synchronisation planifier son travail automatiquement. Les méthodes de **démarrage** et d' **arrêt** existent afin que vous puissiez les utiliser si votre programme est conçu pour remplacer l’interface utilisateur du lecteur Windows Media. Dans ce cas, vous souhaiterez peut-être fournir un bouton Démarrer/arrêter similaire à celui fourni par le lecteur Windows Media dans l’onglet **périphériques** .

Vous pouvez surveiller la progression de la synchronisation d’un appareil en interrogeant [IWMPSyncDevice :: obtenir la \_ progression](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_progress). Cette méthode récupère une valeur de progression pour l’ensemble du processus de synchronisation avec un appareil particulier. La valeur récupérée est un nombre qui représente le pourcentage de synchronisation terminée. Vous pouvez recevoir deux événements liés à la synchronisation. L’événement **DeviceSyncError** vous avertit lorsqu’un problème se produit. L’événement **DeviceSyncStateChange** vous avertit lorsque le moteur de synchronisation a changé d’État pour l’appareil actuel.

Vous pouvez limiter la quantité de stockage des appareils que le lecteur Windows Media utilise pour la synchronisation en appelant [IWMPSyncDevice2 :: setItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice2-setiteminfo) avec l’attribut **PercentSpaceReserved** . L’utilisation de cette interface requiert le lecteur Windows Media 11.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**À propos de la synchronisation des appareils**](about-device-synchronization.md)
</dt> <dt>

[**Interface IWMPEvents2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents2)
</dt> <dt>

[**Indication de la progression de la synchronisation**](showing-synchronization-progress.md)
</dt> </dl>

 

 




