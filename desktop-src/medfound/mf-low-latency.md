---
description: Active le traitement à faible latence dans le pipeline Microsoft Media Foundation.
ms.assetid: 4D11B4D6-8CFF-4850-BF8F-9019A1F79153
title: Attribut MF_LOW_LATENCY (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c51421b68e23ab3f29c15b0b360a7d189befb45cd9046176e6dcb99f1b0748f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119956449"
---
# <a name="mf_low_latency-attribute"></a>\_Attribut de \_ latence faible MF

Active le traitement à faible latence dans le pipeline Microsoft Media Foundation.

## <a name="data-type"></a>Type de données

**Bool** stocké comme **UInt32**

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Remarques

Une latence faible est définie comme le plus petit délai possible entre le moment où les données multimédia sont générées (ou reçues) et le moment où elles sont affichées. Une faible latence est souhaitable pour les scénarios de communication en temps réel. Pour d’autres scénarios, tels que la lecture ou le transcodage local, vous ne devez généralement pas activer le mode de latence faible, car cela peut affecter la qualité.

> [!Note]  
> La valeur GUID de cet attribut est identique à la propriété [CODECAPI \_ AVLowLatencyMode](codecapi-avlowlatencymode.md) définie pour l’interface [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) .

 

Définissez cet attribut sur les composants de pipeline comme suit :

-   Source du média : utilisez la méthode [**IMFMediaSourceEx :: GetSourceAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getsourceattributes) .
-   Media Foundation Transform (MFT) : utilisez la méthode [**IMFTransform :: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) . Pour les encodeurs, l’encodeur peut prendre en charge une faible latence par le biais de l’interface [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) .
-   Récepteur multimédia : interrogez le récepteur multimédia pour l’interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .

En général, les applications ne définissent pas cet attribut directement sur les composants de pipeline, mais définissent l’attribut sur l’un des objets suivants :

-   [Session multimédia](media-session.md): utilisez le paramètre *pConfiguation* de la fonction [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) ou [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) , ou définissez l’attribut sur la topologie.
-   [Lecteur source](source-reader.md): définissez l’attribut avec les propriétés de configuration lorsque vous créez le lecteur source. Pour plus d’informations, consultez [attributs du lecteur source](source-reader-attributes.md).
-   [Enregistreur du récepteur](sink-writer.md): définissez l’attribut avec les propriétés de configuration lorsque vous créez le writer du récepteur. Pour plus d’informations, consultez [attributs du writer du récepteur](sink-writer-attributes.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau \| UWP apps\]<br/>                                  |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau \| UWP apps\]<br/>                        |
| En-tête<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributs du writer du récepteur](sink-writer-attributes.md)
</dt> <dt>

[Attributs du lecteur source](source-reader-attributes.md)
</dt> <dt>

[Attributs de transformation](transform-attributes.md)
</dt> </dl>

 

 
