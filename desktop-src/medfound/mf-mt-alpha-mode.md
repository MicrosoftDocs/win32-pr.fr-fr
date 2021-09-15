---
description: Spécifie si le mode Alpha pour les types de vidéo multimédias couleur est prémultiplié ou droit.
ms.assetid: A263C3F7-357B-426D-B38C-533F9F6A1262
title: Attribut MF_MT_ALPHA_MODE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06b81da14bc0a9e089a5af4815e5bf97359a9cb4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127530745"
---
# <a name="mf_mt_alpha_mode-attribute"></a>MF \_ - \_ attribut de mode Alpha MT \_

\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation. Microsoft exclut toute garantie, expresse ou implicite, concernant les informations fournies ici.\]

Spécifie si le mode Alpha pour les types de vidéo multimédias couleur est prémultiplié ou droit.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="remarks"></a>Notes

Cette valeur peut être convertie en valeur de [**\_ \_ mode Alpha dxgi**](/windows/win32/api/dxgi1_2/ne-dxgi1_2-dxgi_alpha_mode) . Si cet attribut n’est pas présent, pour des raisons de compatibilité descendante, la valeur est **dxgi \_ \_ mode Alpha \_ directement** pour le format vidéo prenant en charge le canal alpha, tel que ARGB32 ou le **\_ mode Alpha dxgi \_ \_ ignore** pour le format vidéo sans canal alpha, tel que RGB32.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10, les applications de bureau version 1709 \[ uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows Serveur, version 1709 \[ applications de bureau uniquement\]<br/>                      |
| En-tête<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



 

 
