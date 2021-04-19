---
title: Attribut SyncState
description: L’attribut SyncState est une représentation sous forme de chaîne d’une valeur 32 bits que le lecteur Windows Media utilise lorsqu’il synchronise des sélections avec des appareils portables.
ms.assetid: affc3d1c-7fe6-4811-acfc-57285cb181ca
keywords:
- Attribut SyncState lecteur Windows Media
topic_type:
- apiref
api_name:
- SyncState
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a948f6c649d548b375ccb676134177b0273c85c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535888"
---
# <a name="syncstate-attribute"></a>Attribut SyncState

L’attribut **SyncState** est une représentation sous forme de chaîne d’une valeur 32 bits que le lecteur Windows Media utilise lorsqu’il synchronise des sélections avec des appareils portables.

## <a name="applies-to"></a>S'applique à

-   [Éléments audio](audio-item-attributes.md)
-   [Autres éléments](other-item-attributes.md)
-   [Éléments de photo](photo-item-attributes.md)
-   [Éléments vidéo](video-item-attributes.md)

## <a name="remarks"></a>Notes

Cet attribut se compose de valeurs 16 2 bits, chacune spécifiant l’état de synchronisation d’un appareil mobile. Le bit le plus significatif (MSB) de cette valeur de 32 bits correspond à l’appareil 16. Le bit le moins significatif (LSB) correspond à l’appareil 1.

L’octet de poids fort de chaque valeur de 2 bits indique si le lecteur Windows Media a synchronisé le contenu avec l’appareil correspondant. La valeur 1 indique qu’elle a été exécutée. La valeur 0 indique qu’elle ne l’a pas fait.

Si le MSB est 0, le LSB spécifie la raison de l’échec de la synchronisation. La valeur 1 dans le LSB indique qu’il n’y avait pas suffisamment d’espace libre pour le contenu. La valeur 0 dans le LSB indique une autre raison empêchait la synchronisation.

Pour récupérer l’état de synchronisation d’un appareil donné, vous devez effectuer les opérations suivantes :

1.  Appelez **IWMPSyncDevice :: obtenir l' \_ État** pour déterminer si un appareil donné est synchronisé.
2.  Si elle est synchronisée, appelez **IWMPSyncDevice :: obtenir \_ partnershipIndex** pour récupérer l’index de la paire de bits de l’appareil dans l’attribut **SyncState** .
3.  À l’aide de cet index, masquez la paire de bits correspondante de l’attribut **SyncState** et examinez le résultat pour déterminer l’état de synchronisation de la playlist avec l’appareil.

Pour déterminer si vous pouvez modifier la valeur de cet attribut, utilisez la méthode [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------|
| Version<br/> | Lecteur Windows Media 10 ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Référence d’attribut**](attribute-reference.md)
</dt> <dt>

[**Détermination de l’état de synchronisation des sélections**](determining-playlist-synchronization-state.md)
</dt> <dt>

[**IWMPSyncDevice :: obtient \_ partnershipIndex**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_partnershipindex)
</dt> <dt>

[**IWMPSyncDevice :: obtient l' \_ État**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_status)
</dt> </dl>

 

 





