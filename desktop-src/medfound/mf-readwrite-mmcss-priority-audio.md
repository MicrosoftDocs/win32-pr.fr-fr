---
description: Définit la priorité de base pour les threads de traitement audio créés par le lecteur source ou le writer du récepteur.
ms.assetid: C0E3A472-959F-4F74-8906-03630DE4CB8C
title: Attribut MF_READWRITE_MMCSS_PRIORITY_AUDIO (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22c33f3e4cab26a448c3b5a28c6f3cfe631a7c1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106536983"
---
# <a name="mf_readwrite_mmcss_priority_audio-attribute"></a>MF \_ ReadWrite \_ ReadWrite \_ priorité \_ audio attribut

Définit la priorité de base pour les threads de traitement audio créés par le lecteur source ou le writer du récepteur.

## <a name="data-type"></a>Type de données

**Int32** stocké comme **UInt32**

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Notes

Vous pouvez éventuellement définir cet attribut lorsque vous créez une instance du [lecteur source](source-reader.md) ou du [writer du récepteur](sink-writer.md). Si vous définissez cet attribut, définissez également l’attribut audio de la [ \_ \_ \_ classe \_ MMCSS ReadWrite MF](mf-readwrite-mmcss-class-audio.md) . Dans le cas contraire, cet attribut est ignoré.

Lorsque le lecteur source ou l’enregistreur du récepteur enregistre les threads de traitement audio auprès du [service Planificateur de classes multimédias](../procthread/multimedia-class-scheduler-service.md), la valeur de cet attribut spécifie la priorité de thread de base. Si cet attribut n’est pas défini, la valeur par défaut est zéro.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications Windows 8 \[ Desktop Apps \| UWP\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ \| apps UWP\]<br/>                              |
| En-tête<br/>                   | <dl> <dt>Mfreadwrite. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
