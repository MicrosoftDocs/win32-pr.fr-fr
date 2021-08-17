---
description: Indique que les informations de longueur NALU sont envoyées en tant qu’objet BLOB avec chaque exemple H. 264 compressé.
ms.assetid: 71B50B44-6025-4EEC-8B37-53D80CF37B07
title: Attribut MF_NALU_LENGTH_SET (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f409cb3c1846667ac21e7d46c559eefb0afc4fe4efbce1f454454d286733157
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104385"
---
# <a name="mf_nalu_length_set-attribute"></a>\_ \_ Attribut Set de longueur Nalu MF \_

Indique que les informations de longueur NALU sont envoyées en tant qu' **objet BLOB** avec chaque exemple H. 264 compressé.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="remarks"></a>Remarques

Définissez cet attribut sur le type de média d’entrée de MEDIASUBTYPE \_ H264 –.

Définissez \_ \_ la longueur de Nalu MF \_ définie sur le type de média d’entrée du décodeur H. 264, indiquant que chaque exemple d’entrée aura une longueur de Nalu disponible et que chaque exemple d’entrée contient une image principale complète.

L' **objet BLOB** contenant les informations de longueur Nalu peut être récupéré à partir de l’attribut d' [ \_ \_ \_ informations de longueur Nalu MF](mf-nalu-length-information.md) sur l’exemple d’entrée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau \| UWP apps\]<br/>                                  |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau \| UWP apps\]<br/>                        |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributs du type de média](media-type-attributes.md)
</dt> </dl>

 

 




