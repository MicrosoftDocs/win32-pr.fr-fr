---
description: Force le convertisseur de vidéo amélioré (EVR) à appeler par lots la méthode IDirect3D9Device ::P renouvely.
ms.assetid: d7523000-baa0-4011-97e1-d1ffe7263d01
title: Attribut EVRConfig_ForceBatching (UUID. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c6dff5d7a5e90377c8749519033b6a66ef7663a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524519"
---
# <a name="evrconfig_forcebatching-attribute"></a>\_Attribut EVRConfig ForceBatching

Force le convertisseur de vidéo amélioré (EVR) à appeler par lots la méthode [**IDirect3D9Device ::P**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) renouvely.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Notes

Cet attribut peut être défini sur le récepteur multimédia EVR. Pour définir l’attribut, utilisez **QueryInterface** pour interroger le récepteur multimédia EVR pour l’interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .

La définition de cet attribut a le même effet que la définition de l’indicateur **MFVideoRenderPrefs \_ FORCEBATCHING** sur EVR. Pour obtenir une description de cet indicateur, consultez [**MFVideoRenderPrefs**](/windows/desktop/api/evr/ne-evr-mfvideorenderprefs) .

La constante GUID de cet attribut est exportée à partir de strmiids. lib.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 R2 \[ uniquement\]<br/>                            |
| En-tête<br/>                   | <dl> <dt>UUID. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributs EVR](enhanced-video-renderer-attributes.md)
</dt> <dt>

[Gestion de la qualité vidéo](video-quality-management.md)
</dt> </dl>

 

 
