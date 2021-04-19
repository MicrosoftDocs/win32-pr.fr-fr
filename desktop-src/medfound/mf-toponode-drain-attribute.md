---
description: Spécifie quand une transformation est vidée.
ms.assetid: 68332106-d1fe-467b-8baa-1e592b9cc243
title: Attribut MF_TOPONODE_DRAIN (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 679b87d626738b82f4504673392bd0fe159e2722
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106534371"
---
# <a name="mf_toponode_drain-attribute"></a>\_ \_ Attribut drain TOPONODE MF

Spécifie quand une transformation est vidée.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="remarks"></a>Notes

Cet attribut s’applique aux nœuds de transformation (**\_ nœud de \_ transformation \_ de topologie MF**).

La valeur de l’attribut est un membre de l’énumération du [**\_ mode de \_ drainage \_ MF TOPONODE**](/windows/desktop/api/mfidl/ne-mfidl-mf_toponode_drain_mode) . Si cet attribut n’est pas défini, la valeur par défaut est **MF \_ TOPONODE \_ drain \_ default**.

La vidange est effectuée en appelant [**IMFTransform ::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) sur la transformation à l’aide du message de [**\_ drainage de \_ commande \_ de message MFT**](mft-message-command-drain.md) . Pour plus d’informations, consultez énumération des [**\_ \_ types de messages MFT**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type) .

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

 

 




