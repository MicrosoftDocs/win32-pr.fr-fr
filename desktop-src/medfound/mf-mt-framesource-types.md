---
description: Valeur qui indique le type de capteur fourni par une source de frame, telle que la couleur, l’infrarouge ou la profondeur.
ms.assetid: F327B9E9-C01C-4F5B-9A26-6404ECD7F27F
title: Attribut MF_MT_FRAMESOURCE_TYPES (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4475d66aea245ac9295a7996da2c37cabdb9627
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127313970"
---
# <a name="mf_mt_framesource_types-attribute"></a>\_Attribut des \_ types FRAMESOURCE MF MT \_

\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation. Microsoft exclut toute garantie, expresse ou implicite, concernant les informations fournies ici.\]

Valeur qui indique le type de capteur fourni par une source de frame, telle que la couleur, l’infrarouge ou la profondeur.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="remarks"></a>Notes

Cette valeur doit être un membre de l’énumération [**\_ MFFrameSourceTypes**](/previous-versions/windows/desktop/legacy/mt846679(v=vs.85)) . Pour la compatibilité descendante, lorsque cet attribut n’est pas défini sur un type de média, il est supposé être **\_ MFFrameSourceTyes :: Color**.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10, les applications de bureau version 1709 \[ uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows Serveur, version 1709 \[ applications de bureau uniquement\]<br/>                      |
| En-tête<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



 

 
