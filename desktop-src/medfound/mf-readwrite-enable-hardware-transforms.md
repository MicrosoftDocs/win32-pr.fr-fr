---
description: Permet au lecteur source ou au writer de récepteur d’utiliser des transformations Media Foundation basées sur le matériel (MFTs).
ms.assetid: 03f2fa76-b828-40b1-929d-60e7d5ab49bb
title: Attribut MF_READWRITE_ENABLE_HARDWARE_TRANSFORMS (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 642be732a51f064d07e57609a886810f2a9c40b2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127414130"
---
# <a name="mf_readwrite_enable_hardware_transforms-attribute"></a>MF \_ ReadWrite \_ activer \_ l' \_ attribut de transformations de matériel

Permet au lecteur source ou au writer de récepteur d’utiliser des transformations Media Foundation basées sur le matériel (MFTs).

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Notes

Par défaut, le lecteur source et le writer du récepteur n’utilisent pas de décodeurs ou d’encodeurs matériels. Pour activer l’utilisation du matériel MFTs, affectez la valeur **true** à cet attribut lorsque vous créez le lecteur source ou le writer du récepteur.

Utilisez cet attribut avec les fonctions suivantes :

-   [**MFCreateSourceReaderFromByteStream**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)
-   [**MFCreateSourceReaderFromMediaSource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource)
-   [**MFCreateSourceReaderFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)
-   [**MFCreateSinkWriterFromMediaSink**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink)
-   [**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl)

Il existe une exception au comportement par défaut. Le lecteur source et le writer du récepteur utilisent automatiquement des MFTs qui sont inscrits localement dans le processus de l’appelant. Pour inscrire une table MFT localement, appelez [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal) ou [**MFTRegisterLocalByCLSID**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocalbyclsid). Les MFTs matériels inscrits localement sont utilisés, même si l’attribut de **\_ \_ \_ \_ transformations matérielles MF ReadWrite Enable** n’est pas défini.

Cet attribut n’affecte pas le décodage vidéo accéléré par le matériel qui utilise l’accélération vidéo DirectX (DXVA). Pour activer le décodage DXVA dans le lecteur source, définissez l’attribut du [ \_ \_ \_ \_ Gestionnaire D3D du lecteur source MF](mf-source-reader-d3d-manager.md) .

Si cet attribut a la **valeur true**, ne définissez pas l’attribut de [ \_ \_ \_ convertisseurs de désactivation MF ReadWrite](mf-readwrite-disable-converters.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 \| applications UWP\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Applications du serveur 2008 R2 \[ Desktop Apps \| UWP\]<br/>                           |
| En-tête<br/>                   | <dl> <dt>Mfreadwrite. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributs du writer du récepteur](sink-writer-attributes.md)
</dt> <dt>

[Attributs du lecteur source](source-reader-attributes.md)
</dt> </dl>

 

 




