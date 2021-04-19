---
description: Indique les longueurs de NALUs dans l’exemple. Il s’agit d’un objet BLOB MF qui est défini sur les exemples d’entrée compressés sur le décodeur H. 264.
ms.assetid: 09F54504-A6CF-4385-BDD7-8D23B1D0125C
title: Attribut MF_NALU_LENGTH_INFORMATION (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c46d9a0b7cbec92c4cde40548b8d3baecf955b50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517654"
---
# <a name="mf_nalu_length_information-attribute"></a>\_Attribut d' \_ information de longueur Nalu MF \_

Indique les longueurs de NALUs dans l’exemple. Il s’agit d’un **objet BLOB** MF qui est défini sur les exemples d’entrée compressés sur le décodeur H. 264.

## <a name="data-type"></a>Type de données

**OBJET BLOB**

## <a name="remarks"></a>Notes

Pour que cet attribut soit défini, le support doit être de type MEDIASUBTYPE \_ H264 – et l’attribut [set de \_ \_ longueur \_ Nalu MF](mf-nalu-length-set.md) doit être défini sur le type de média d’entrée de MEDIASUBTYPE \_ H264 –.

Définissez les \_ informations de longueur Nalu MF \_ \_ en tant qu' **objet BLOB** sur l’exemple d’entrée, avec un DWORD pour chaque Nalu dans l’exemple. Par exemple, s’il existe AUD (9 octets), SPS (25 octets), PPS (10 octets), slice1 (50 k), r tranche 2 (60 k), il doit y avoir 5 DWORDs avec les valeurs 9, 25, 10, 50 k, 60 k dans l' **objet BLOB**.

Ici, du code qui définit l' **objet BLOB**, où **rgdwNALULengthInfo** est un tableau de type DWORD et **uiNaluLengthIdx** les longueurs Nalu valides définies sur l' **objet BLOB**.


```C++
m_spSample->SetBlob( MF_NALU_LENGTH_INFORMATION, 
                    (UINT8*) m_wpParent->m_pdwNALULengthInfo, 
                    sizeof(DWORD)*uiNaluLengthIdx ), 
                    done );
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications Windows 8 \[ Desktop Apps \| UWP\]<br/>                                  |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ \| apps UWP\]<br/>                        |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributs du type de média](media-type-attributes.md)
</dt> </dl>

 

 




