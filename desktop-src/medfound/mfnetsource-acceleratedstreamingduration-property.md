---
description: Durée de la diffusion en continu accélérée pour la source réseau, en millisecondes.
ms.assetid: 3f9cd762-f393-4130-ba25-d16da0642093
title: MFNETSOURCE_ACCELERATEDSTREAMINGDURATION, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57980fbe08d3c6f48cf2638b35e88c455e566e75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863166"
---
# <a name="mfnetsource_acceleratedstreamingduration-property"></a>MFNETSOURCE \_ propriété ACCELERATEDSTREAMINGDURATION

Durée de la diffusion en continu accélérée pour la source réseau, en millisecondes.



Type de données

Type de PROPVARIANT (VT)

Membre PROPVARIANT

**DWORD** (stocké en tant que **long**)

VT \_

**lVal**



## <a name="remarks"></a>Notes

La constante **MFNETSOURCE \_ ACCELERATEDSTREAMINGDURATION** définit le GUID de cette clé de propriété. L’identificateur de propriété (PID) est égal à zéro.

Les applications peuvent utiliser cette propriété pour configurer la source réseau. Pour définir la propriété, transmettez un objet **IPropertyStore** au programme de résolution source. Pour plus d’informations, consultez [configuration d’une source de média](configuring-a-media-source.md).

Cette propriété s’applique à la fonctionnalité de démarrage rapide de Windows Media Services, qui lit rapidement le contenu sans attendre une longue mise en mémoire tampon initiale. Lorsque vous utilisez le démarrage rapide, le serveur exécutant Windows Media Services enverra des données au début du contenu à un rythme plus rapide que celui spécifié par la vitesse de transmission du contenu.

La valeur par défaut de cette propriété est 10 000 millisecondes.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Fonctionnalités de la source réseau](network-source-features.md)
</dt> <dt>

[Mise en réseau dans Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




