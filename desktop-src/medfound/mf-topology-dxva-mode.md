---
description: Spécifie si le chargeur de topologie Active l’accélération vidéo Microsoft DirectX (DXVA) dans la topologie.
ms.assetid: 03783ef3-f957-41e3-9734-94cb34ecc088
title: Attribut MF_TOPOLOGY_DXVA_MODE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5462ccf575f94935d100eb70a6d806e139f09762151c2dad8d4e155ca5d1d17e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117875726"
---
# <a name="mf_topology_dxva_mode-attribute"></a>\_ \_ Attribut de mode DXVA de topologie MF \_

Spécifie si le chargeur de topologie Active l’accélération vidéo Microsoft DirectX (DXVA) dans la topologie.

## <a name="data-type"></a>Type de données

**[**MFTOPOLOGY \_ \_Mode DXVA**](/windows/desktop/api/mfidl/ne-mfidl-mftopology_dxva_mode)** stocké comme **UInt32**

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>S’applique à

[**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a>Remarques

La valeur de cet attribut est une constante d’énumération du [**\_ \_ mode DXVA MFTOPOLOGY**](/windows/desktop/api/mfidl/ne-mfidl-mftopology_dxva_mode) . La valeur par défaut est **MFTOPOLOGY \_ DXVA \_ par défaut**.

Cet attribut contrôle les MFTs qui reçoivent un pointeur vers le gestionnaire de périphériques Direct3D. Pour activer l’accélération vidéo complète, définissez la valeur sur **MFTOPOLOGY \_ DXVA \_ Full**. La valeur **MFTOPOLOGY \_ DXVA \_ default** est définie pour la compatibilité descendante. elle correspond au comportement de toutes les versions antérieures de Microsoft Media Foundation.

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

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

 

 




