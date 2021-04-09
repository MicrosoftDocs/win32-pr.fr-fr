---
description: Spécifie la taille de la fenêtre de destination pour la lecture vidéo.
ms.assetid: 46af4c11-042c-4580-ba9d-3aee6172de56
title: Attribut MF_TOPOLOGY_PLAYBACK_MAX_DIMS (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d1fc6a57c5e031bc6f35f36e688bd44986f541b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201974"
---
# <a name="mf_topology_playback_max_dims-attribute"></a>\_ \_ \_ Attribut Dim Max playback de lecture de la topologie MF \_

Spécifie la taille de la fenêtre de destination pour la lecture vidéo.

## <a name="data-type"></a>Type de données

**UINT64**

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**MFGetAttributeSize**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributesize).

Pour définir cet attribut, appelez [**MFSetAttributeSize**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributesize).

## <a name="applies-to"></a>S’applique à

[**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a>Notes

Le chargeur de topologie utilise cet attribut pour optimiser le pipeline avant le démarrage de la lecture. Si vous définissez cet attribut, affectez également à l’attribut [ \_ \_ \_ \_ optimisations de la lecture statique de la topologie MF](mf-topology-static-playback-optimizations.md) la **valeur true**.

Les 32 bits supérieurs de la valeur de l’attribut contiennent la largeur et les 32 bits inférieurs contiennent la hauteur, en pixels.

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 R2 \[ uniquement\]<br/>                            |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributs de topologie](topology-attributes.md)
</dt> <dt>

[Gestion de la qualité vidéo](video-quality-management.md)
</dt> </dl>

 

 




