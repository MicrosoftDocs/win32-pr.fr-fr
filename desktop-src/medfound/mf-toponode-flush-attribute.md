---
description: Spécifie quand une transformation est vidée.
ms.assetid: 1e87f58f-546f-4dd4-b218-1458ff17db53
title: Attribut MF_TOPONODE_FLUSH (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67e02c297efa68c6e6c585837675a46b729ec2382be072828059fd795d1c67a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663879"
---
# <a name="mf_toponode_flush-attribute"></a>\_Attribut de \_ vidage TOPONODE MF

Spécifie quand une transformation est vidée.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="remarks"></a>Remarques

Cet attribut s’applique aux nœuds de transformation (**\_ nœud de \_ transformation \_ de topologie MF**).

La valeur de l’attribut est un membre de l’énumération du [**\_ mode de \_ vidage \_ MF TOPONODE**](/windows/desktop/api/mfidl/ne-mfidl-mf_toponode_flush_mode) . Si cet attribut n’est pas défini, la valeur par défaut est **MF \_ TOPONODE \_ flush \_ Always**.

Le vidage est effectué en appelant [**IMFTransform ::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) sur la transformation à l’aide du message de vidage de la [**\_ commande du message \_ \_ MFT**](mft-message-command-flush.md) . Pour plus d’informations, consultez énumération des [**\_ \_ types de messages MFT**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type) .

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

 

 




