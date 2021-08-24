---
description: Spécifie si une table de Media Foundation matérielle (MFT, Hardware-Based transformation) est connectée à une autre table MFT matérielle.
ms.assetid: 9166c43f-d2ae-4dc7-84e9-02146b67efe2
title: Attribut MFT_CONNECTED_TO_HW_STREAM (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31ff2a2dea2fcb67cff776ba02c43193b571a382df57a5d0562f3f2cd1fb7248
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119602869"
---
# <a name="mft_connected_to_hw_stream-attribute"></a>MFT \_ connecté \_ à \_ l' \_ attribut de flux de matériel

Spécifie si une table de Media Foundation matérielle (MFT, Hardware-Based transformation) est connectée à une autre table MFT matérielle.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Remarques

En général, les applications n’utilisent pas cet attribut.

Cet attribut est utilisé avec les MFTs basés sur le matériel. Lorsque deux MFTs matériels sont connectés dans une topologie, le chargeur de topologie affecte la **valeur true** à cet attribut sur les objets suivants :

-   Flux de sortie de la table MFT en amont
-   Flux d’entrée de la table MFT en aval

Pour obtenir le magasin d’attributs du flux de sortie, le chargeur de topologie appelle [**IMFTransform :: GetOutputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes) sur la table MFT en amont. Pour obtenir le magasin d’attributs pour le flux d’entrée, le chargeur de topologie appelle [**IMFTransform :: GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes) sur la table MFT en aval.

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 \| applications UWP\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Applications du serveur 2008 R2 \[ Desktop Apps \| UWP\]<br/>                           |
| En-tête<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Matériel MFTs](hardware-mfts.md)
</dt> <dt>

[Attributs de transformation](transform-attributes.md)
</dt> </dl>

 

 




