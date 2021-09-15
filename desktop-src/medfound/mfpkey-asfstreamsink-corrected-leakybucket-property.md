---
description: Spécifie le &\# 0034 ; compartiment avec fuite&\# 0034 ; paramètres pour un flux sur un récepteur multimédia ASF.
ms.assetid: b01e59b6-0a7f-4125-867c-532385a27c15
title: MFPKEY_ASFSTREAMSINK_CORRECTED_LEAKYBUCKET, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05a4ebc2dc41a1f43906aff5d2fe8caea8d53057
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127412943"
---
# <a name="mfpkey_asfstreamsink_corrected_leakybucket-property"></a>MFPKEY \_ ASFSTREAMSINK \_ corrigé \_ LEAKYBUCKET, propriété

Spécifie les paramètres de « compartiment perdu » (consultez la section Notes) pour un flux sur un récepteur multimédia ASF.



Type de données

Type de PROPVARIANT (VT)

Membre PROPVARIANT

Tableau de valeurs **DWORD** (**CAUL**)

VT \_ Vector \| VT \_ UI4

**caul**



## <a name="remarks"></a>Notes

Une application peut définir cette propriété sur un flux du récepteur de média ASF une fois que le type de média du flux est négocié. utilisez cette propriété pour spécifier la fenêtre de mémoire tampon réelle que le codec de média Windows utilisera. vous pouvez obtenir ces informations à partir du codec à l’aide de l’interface **IWMCodecLeakyBucket** , qui est documentée dans le kit de développement logiciel (SDK) de Format multimédia Windows.

La valeur de cette propriété est un tableau de trois valeurs **DWORD** dans l’ordre suivant :

-   Vitesse de transmission, en bits par seconde.
-   Taille de la mémoire tampon, en octets.
-   Saturation de la mémoire tampon initiale, en octets.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink)
</dt> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




