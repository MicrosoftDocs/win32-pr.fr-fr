---
description: Indique que les informations de longueur NALU sont envoyées en tant qu’objet BLOB avec chaque exemple H. 264 compressé.
ms.assetid: 71B50B44-6025-4EEC-8B37-53D80CF37B07
title: Attribut MF_NALU_LENGTH_SET (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a01034cf62758787747882da40ac703d205fa55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522211"
---
# <a name="mf_nalu_length_set-attribute"></a>\_ \_ Attribut Set de longueur Nalu MF \_

Indique que les informations de longueur NALU sont envoyées en tant qu' **objet BLOB** avec chaque exemple H. 264 compressé.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="remarks"></a>Notes

Définissez cet attribut sur le type de média d’entrée de MEDIASUBTYPE \_ H264 –.

Définissez \_ \_ la longueur de Nalu MF \_ définie sur le type de média d’entrée du décodeur H. 264, indiquant que chaque exemple d’entrée aura une longueur de Nalu disponible et que chaque exemple d’entrée contient une image principale complète.

L' **objet BLOB** contenant les informations de longueur Nalu peut être récupéré à partir de l’attribut d' [ \_ \_ \_ informations de longueur Nalu MF](mf-nalu-length-information.md) sur l’exemple d’entrée.

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

 

 




