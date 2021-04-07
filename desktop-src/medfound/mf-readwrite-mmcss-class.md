---
description: Spécifie une classe de service Planificateur de classes multimédias (MMCSS) pour le lecteur source ou le writer de récepteur.
ms.assetid: A3A295E8-AC9C-4641-ADDA-B97D5AB13A9A
title: Attribut MF_READWRITE_MMCSS_CLASS (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d2088ba09bf4f8ad9516d9b2117ab54161d7ac4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759076"
---
# <a name="mf_readwrite_mmcss_class-attribute"></a>MF \_ ReadWrite \_ - \_ attribut de classe mmcss

Spécifie une classe de [service Planificateur de classes multimédias](../procthread/multimedia-class-scheduler-service.md) (MMCSS) pour le lecteur source ou le writer de récepteur.

## <a name="data-type"></a>Type de données

**LPWSTR**

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**IMFAttributes :: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).

Pour définir cet attribut, appelez [**IMFAttributes :: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).

## <a name="remarks"></a>Notes

Vous pouvez éventuellement définir cet attribut lorsque vous créez une instance du [lecteur source](source-reader.md) ou du [writer du récepteur](sink-writer.md). La valeur de l’attribut doit être un nom de classe MMCSS valide.

Si cet attribut est défini, le lecteur source ou l’enregistreur du récepteur enregistre tous ses threads avec la classe MMCSS spécifiée. MMCSS garantit que le traitement des données dans le lecteur source ou le writer du récepteur a priorité sur les autres tâches système.

Pour spécifier la priorité de base, définissez l’attribut de priorité de la [ \_ \_ \_ priorité MMCSS ReadWrite MF](mf-readwrite-mmcss-priority.md) . Si cet attribut n’est pas défini, la priorité de base est égale à zéro.

Pour les threads de traitement audio, l’attribut audio de la [ \_ \_ \_ \_ classe MMCSS ReadWrite MF](mf-readwrite-mmcss-class-audio.md) (s’il est défini) remplace cet attribut.

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

 

 
