---
description: Spécifie si le chargeur de topologie Active le processeur vidéo de transcodage (XVP). pour les conversions, activation de la conversion des couleurs à accélération matérielle.
title: Attribut MF_TOPOLOGY_ENABLE_XVP_FOR_PLAYBACK (Mfidl. h)
ms.topic: reference
ms.date: 02/22/2021
ms.openlocfilehash: e36841db57e8343248ef5e369915d4bc357815bb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106542129"
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

## <a name="remarks"></a>Notes

Si cet attribut est défini, le chargeur de topologie extrait le processeur vidéo, si nécessaire, pendant la résolution de la topologie de non-transcodage. Lorsque vous utilisez la topologie pour créer vos propres [IMFTopology](/windows/win32/api/mfidl/nn-mfidl-imftopology) , cet attribut indique au chargeur d’utiliser XVP pour les conversions au lieu du convertisseur de couleur hérité, ce qui permet de convertir les couleurs à accélération matérielle. le convertisseur de couleurs hérité est un logiciel uniquement.

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

[Gestionnaire de périphériques Direct3D](direct3d-device-manager.md)
</dt> <dt>

[Attributs de topologie](topology-attributes.md)
</dt> </dl>

 

 




