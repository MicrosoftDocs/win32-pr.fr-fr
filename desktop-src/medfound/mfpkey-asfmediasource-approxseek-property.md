---
description: Spécifie si la source du média ASF utilise la recherche approximative.
ms.assetid: 4877b67c-524c-4717-a90f-6de21918d3d8
title: MFPKEY_ASFMediaSource_ApproxSeek, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 253a18ebbdf78e3aa0ef0e79f41c4bf180a04b48
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127414100"
---
# <a name="mfpkey_asfmediasource_approxseek-property"></a>MFPKEY \_ ASFMediaSource \_ ApproxSeek, propriété

Spécifie si la source du média ASF utilise la recherche approximative.



Type de données

Type de PROPVARIANT (VT)

Membre PROPVARIANT

**VARIANT \_ booléen**

VT \_ bool

**boolVal**



## <a name="remarks"></a>Notes

Les applications peuvent utiliser cette propriété pour configurer la source de média ASF. Pour définir la propriété, transmettez un pointeur **IPropertyStore** au programme de résolution source. Pour plus d’informations, consultez [configuration d’une source de média](configuring-a-media-source.md).

La source du média ASF gère la recherche comme suit :

-   Si la valeur de cette propriété est **\_ true**, la source du média utilise une recherche approximative, ce qui est moins précis mais plus rapide que la recherche exacte.
-   Si la valeur est **\_ false** et que le fichier ASF a un index, la source du média utilise la recherche exacte.
-   Si le fichier ASF ne contient pas d’index, la source du média utilise la recherche approxmate, sauf si la propriété [MFPKEY \_ ASFMediaSource \_ IterativeSeekIfNoIndex](mfpkey-asfmediasource-iterativeseekifnoindex.md) est définie sur **Variant \_ true**.
-   Si le fichier ASF ne contient pas d’index et que la propriété [MFPKEY \_ ASFMediaSource \_ IterativeSeekIfNoIndex](mfpkey-asfmediasource-iterativeseekifnoindex.md) a la **\_ valeur variant true**, la source du média utilise la recherche itérative. La recherche itérative est plus précise, mais plus lente que la recherche approximative (mais généralement moins précise que la recherche exacte).
    > [!Note]  
    > requiert Windows 7.

     

La valeur par défaut de cette propriété **est \_ false false**.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




