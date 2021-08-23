---
description: Spécifie si l’application nécessite la prise en charge de Microsoft Direct3D dans le lecteur source ou le writer du récepteur.
ms.assetid: 3844ED7B-E1E5-4CD7-B080-FE7EC7B28AC5
title: Attribut MF_READWRITE_D3D_OPTIONAL (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cebc24991e5c2bfb90b7153f3a90a2e7447c2daef987b2956680e89f162223ed
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119664109"
---
# <a name="mf_readwrite_d3d_optional-attribute"></a>MF \_ ReadWrite de l' \_ \_ attribut facultatif D3D

Spécifie si l’application nécessite la prise en charge de Microsoft Direct3D dans le [lecteur source](source-reader.md) ou le [writer du récepteur](sink-writer.md).

## <a name="data-type"></a>Type de données

**Bool** stocké comme **UInt32**

## <a name="remarks"></a>Remarques

Cet attribut s’applique uniquement si l’application active la prise en charge Direct3D à l’aide de l’attribut du gestionnaire [ \_ \_ D3D du lecteur \_ \_ source MF](mf-source-reader-d3d-manager.md) ou du gestionnaire D3D du [récepteur du \_ récepteur \_ \_ \_ MF](mf-sink-writer-d3d-manager.md) .

Si l’application active la prise en charge Direct3D, le lecteur source et le writer du récepteur essaient tous deux d’allouer des surfaces Direct3D pour la vidéo. Si cette opération échoue et que l' \_ \_ attribut facultatif MF ReadWrite D3D \_ est **true**, l’enregistreur de lecture/récepteur source revient à allouer des surfaces vidéo dans la mémoire système. Sinon, si les surfaces Direct3D ne peuvent pas être allouées et que \_ \_ l’option MF ReadWrite D3D \_ facultative a la **valeur false**, une erreur se produit pendant le traitement.

Si l’application n’active pas la prise en charge Direct3D, le writer de lecteur/récepteur source utilise la mémoire système et ignore la valeur de l' \_ option MF ReadWrite \_ D3D \_ facultative.

Cet attribut est facultatif. La valeur par défaut est **FALSE**. Définissez l’attribut lorsque vous créez le lecteur source ou le writer du récepteur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                     |
| En-tête<br/>                   | <dl> <dt>Mfreadwrite. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributs du writer du récepteur](sink-writer-attributes.md)
</dt> <dt>

[Attributs du lecteur source](source-reader-attributes.md)
</dt> </dl>

 

 




