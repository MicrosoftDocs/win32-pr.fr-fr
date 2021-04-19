---
description: Spécifie si la session multimédia utilise le préroll sur le récepteur multimédia représenté par ce nœud de topologie.
ms.assetid: 1781f3a0-6baa-4e06-b2eb-9a8f572aa040
title: Attribut MF_TOPONODE_DISABLE_PREROLL (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d3d031a4ee50262e717731ae517d4441e9be9a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534750"
---
# <a name="mf_toponode_disable_preroll-attribute"></a>TOPONODE MF- \_ \_ désactiver l’attribut de \_ préroll

Spécifie si la session multimédia utilise le préroll sur le récepteur multimédia représenté par ce nœud de topologie.

## <a name="data-type"></a>Type de données

**UINT32**

Traiter en tant que valeur booléenne.

## <a name="remarks"></a>Notes

Cet attribut s’applique aux nœuds de sortie (**\_ nœud de \_ sortie \_ de topologie MF**).

Si la valeur de cet attribut est **true**, la session multimédia ne préroll aucune donnée au récepteur multimédia, même si le récepteur multimédia expose l’interface [**IMFMediaSinkPreroll**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasinkpreroll) . Si la valeur est **false**, la session multimédia préroll les données si le récepteur multimédia implémente **IMFMediaSinkPreroll**. La valeur par défaut est **FALSE**.

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                               |
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

 

 




