---
description: Spécifie si le chargeur de topologie Active le processeur vidéo de transcodage (XVP). pour les conversions, activation de la conversion des couleurs à accélération matérielle.
title: Attribut MF_TOPOLOGY_ENABLE_XVP_FOR_PLAYBACK (Mfidl. h)
ms.topic: reference
ms.date: 02/22/2021
ms.openlocfilehash: 3f315463ce1719617c5a48066401219f4b971f0a555cadf2af43b055a2b0e9a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117875727"
---
# <a name="mf_topology_enable_xvp_for_playback-attribute"></a>\_La topologie MF \_ active \_ XVP \_ pour l' \_ attribut de lecture

Spécifie si le chargeur de topologie Active le processeur vidéo de transcodage (XVP). pour les conversions, activation de la conversion des couleurs à accélération matérielle.

## <a name="data-type"></a>Type de données

**Bool** stocké comme **UInt32**

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>S’applique à

[**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a>Remarques

Si cet attribut est défini, le chargeur de topologie extrait le processeur vidéo, si nécessaire, pendant la résolution de la topologie de non-transcodage. Lorsque vous utilisez la topologie pour créer vos propres [IMFTopology](/windows/win32/api/mfidl/nn-mfidl-imftopology) , cet attribut indique au chargeur d’utiliser XVP pour les conversions au lieu du convertisseur de couleur hérité, ce qui permet de convertir les couleurs à accélération matérielle. le convertisseur de couleurs hérité est un logiciel uniquement.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/>                            |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Gestionnaire de périphériques Direct3D](direct3d-device-manager.md)
</dt> <dt>

[Attributs de topologie](topology-attributes.md)
</dt> </dl>

 

 




