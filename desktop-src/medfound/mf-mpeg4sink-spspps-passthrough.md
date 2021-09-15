---
description: Spécifie si le récepteur de fichiers MPEG-4 filtre le jeu de paramètres de séquence (SPS) et le jeu de paramètres d’image (PPS) NALUs.
ms.assetid: B2574BE5-6334-4ED2-A008-86326CDC13B8
title: Attribut MF_MPEG4SINK_SPSPPS_PASSTHROUGH (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3c02f4f1cdcac17a104b5061c8899c92e0ad824
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127531240"
---
# <a name="mf_mpeg4sink_spspps_passthrough-attribute"></a>\_ \_ Attribut passthrough MPEG4SINK SPSPPS MF \_

Spécifie si le [**récepteur de fichiers MPEG-4**](mpeg-4-file-sink.md) filtre le jeu de paramètres de séquence (SPS) et le jeu de paramètres d’image (PPS) NALUs.

## <a name="data-type"></a>Type de données

**Bool** stocké comme **UInt32**

## <a name="applies-to"></a>S’applique à

[**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink)

## <a name="remarks"></a>Notes

Le [**récepteur de fichiers MPEG-4**](mpeg-4-file-sink.md) écrit les paramètres SPS et PPS dans la zone de description de l’exemple du fichier MP4. Par défaut, il élimine les NALUs SPS et PPS du flux vidéo. Pour remplacer ce comportement, affectez la valeur \_ \_ \_ **true** à l’attribut passthrough MPEG4SINK SPSPPS MF.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau \| UWP apps\]<br/>                                  |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau \| UWP apps\]<br/>                        |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




