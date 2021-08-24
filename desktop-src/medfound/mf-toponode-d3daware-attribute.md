---
description: Spécifie si la transformation associée à un nœud de topologie prend en charge l’accélération vidéo DirectX (DXVA).
ms.assetid: b9e393be-0bc0-4cf6-be44-e9e95339c434
title: Attribut MF_TOPONODE_D3DAWARE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e49735a1178cc521efd152f4fa11ab7c84069b07d0e5001f0f0e8e38bec940ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119607149"
---
# <a name="mf_toponode_d3daware-attribute"></a>\_ \_ Attribut D3DAWARE TOPONODE MF

Spécifie si la transformation associée à un nœud de topologie prend en charge l’accélération vidéo DirectX (DXVA).

## <a name="data-type"></a>Type de données

**UINT32**

Traiter en tant que valeur booléenne.

## <a name="remarks"></a>Remarques

Cet attribut s’applique aux nœuds de transformation (**\_ nœud de \_ transformation \_ de topologie MF**).

En général, les applications n’utilisent pas cet attribut directement. La session multimédia définit cet attribut sur un nœud de transformation si la transformation de Media Foundation sous-jacente a l’attribut [**\_ \_ \_ compatible Direct3D sa**](mf-sa-d3d-aware-attribute.md) .

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[Attributs de nœud de topologie](topology-node-attributes.md)
</dt> </dl>

 

 




