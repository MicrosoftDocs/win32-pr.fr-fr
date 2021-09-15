---
description: Spécifie une classe de service Planificateur de classes multimédias (MMCSS) pour les threads de traitement audio dans le lecteur source ou le writer de récepteur.
ms.assetid: F1B8A8C8-2E41-4321-A94D-C50447C69941
title: Attribut MF_READWRITE_MMCSS_CLASS_AUDIO (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa35db710c6b72c103855fa2c0a9f169f49c4511
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127411501"
---
# <a name="mf_readwrite_mmcss_class_audio-attribute"></a>MF \_ ReadWrite de la \_ classe MMCSS, \_ \_ attribut audio

Spécifie une classe de [service Planificateur de classes multimédias](../procthread/multimedia-class-scheduler-service.md) (MMCSS) pour les threads de traitement audio dans le lecteur source ou le writer de récepteur.

## <a name="data-type"></a>Type de données

**LPWSTR**

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**IMFAttributes :: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).

Pour définir cet attribut, appelez [**IMFAttributes :: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).

## <a name="remarks"></a>Notes

Vous pouvez éventuellement définir cet attribut lorsque vous créez une instance du [lecteur source](source-reader.md) ou du [writer du récepteur](sink-writer.md). La valeur de l’attribut doit être un nom de classe MMCSS valide.

Si cet attribut est défini, le lecteur source ou l’enregistreur du récepteur enregistre ses threads de traitement audio avec la classe MMCSS spécifiée. MMCSS garantit que le traitement des données dans le lecteur source ou le writer du récepteur a priorité sur les autres tâches système.

Pour spécifier la priorité de base pour les threads audio, définissez l’attribut [ \_ audio MF ReadWrite \_ MMCSS \_ Priority \_ ](mf-readwrite-mmcss-priority-audio.md) . Si cet attribut n’est pas défini, la priorité de base pour les threads audio est égale à zéro.

Cet attribut remplace l’attribut de [classe de la \_ \_ \_ classe MMCSS ReadWrite MF](mf-readwrite-mmcss-class.md) pour les threads de traitement audio. Si aucun attribut n’est défini, les threads audio ne sont pas inscrits auprès de MCSS.

Pour la plupart des applications, le problème audio est bien plus perceptible pour l’utilisateur que le problème de vidéo, et donc moins acceptable. Pour cette raison, une application doit généralement définir l' \_ audio de la classe MF ReadWrite ReadWrite \_ \_ \_ sur une classe MMCSS de priorité supérieure à celle de la [ \_ classe MF ReadWrite \_ MMCSS \_ ](mf-readwrite-mmcss-class.md). Cela garantit que le traitement audio reçoit une priorité plus élevée que d’autres tâches.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau \| UWP apps\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau \| UWP apps\]<br/>                              |
| En-tête<br/>                   | <dl> <dt>Mfreadwrite. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
