---
description: Durée de la diffusion en continu accélérée pour la source réseau, en millisecondes.
ms.assetid: 3f9cd762-f393-4130-ba25-d16da0642093
title: MFNETSOURCE_ACCELERATEDSTREAMINGDURATION, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ec37cfd7dd0aa8d60c3e192ae0f445f8a121e9e3cd3f85d46e8c18b21fc2b06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118243863"
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

cette propriété s’applique à la fonctionnalité de démarrage rapide de Services Windows Media, qui lit le contenu rapidement sans attendre une longue mise en mémoire tampon initiale. lorsque vous utilisez le démarrage rapide, le serveur exécutant Services Windows Media envoie des données au début du contenu à un débit plus rapide que celui spécifié par la vitesse de transmission du contenu.

La valeur par défaut de cette propriété est 10 000 millisecondes.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Fonctionnalités de la source réseau](network-source-features.md)
</dt> <dt>

[Mise en réseau dans Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




