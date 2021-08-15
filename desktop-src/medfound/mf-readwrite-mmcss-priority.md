---
description: Définit la priorité de thread de base pour le lecteur source ou le writer de récepteur.
ms.assetid: 9513AE28-2AF4-45EC-AC19-C0718540E26F
title: Attribut MF_READWRITE_MMCSS_PRIORITY (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56f108b7cce9f1c9d6226803bf2a2cc32b62ac94077f7f84cbc78e632cb25ea8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118740601"
---
# <a name="mf_readwrite_mmcss_priority-attribute"></a>\_Attribut de \_ priorité MMCSS ReadWrite \_ MF

Définit la priorité de thread de base pour le lecteur source ou le writer de récepteur.

## <a name="data-type"></a>Type de données

**Int32** stocké comme **UInt32**

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Remarques

Vous pouvez éventuellement définir cet attribut lorsque vous créez une instance du [lecteur source](source-reader.md) ou du [writer du récepteur](sink-writer.md). Si vous définissez cet attribut, définissez également l’attribut de classe de la [ \_ \_ \_ classe MMCSS ReadWrite MF](mf-readwrite-mmcss-class.md) . Dans le cas contraire, cet attribut est ignoré.

Lorsque le lecteur source ou l’enregistreur du récepteur enregistre les threads avec le [service Planificateur de classes multimédias](../procthread/multimedia-class-scheduler-service.md), la valeur de cet attribut spécifie la priorité de thread de base. Si cet attribut n’est pas défini, la valeur par défaut est zéro.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau \| UWP apps\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau \| UWP apps\]<br/>                              |
| En-tête<br/>                   | <dl> <dt>Mfreadwrite. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
