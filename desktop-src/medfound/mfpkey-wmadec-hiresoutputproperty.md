---
description: Spécifie si le décodeur audio doit fournir une sortie haute résolution.
ms.assetid: a96bd78f-982c-43fa-b2d3-8caba4aa84b6
title: MFPKEY_WMADEC_HIRESOUTPUT, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd59bc6b8b0e74be1daaea4a61ca82c810a0ca79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519629"
---
# <a name="mfpkey_wmadec_hiresoutput-property"></a>MFPKEY \_ WMADEC \_ HIRESOUTPUT, propriété

Spécifie si le décodeur audio doit fournir une sortie haute résolution.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

\_wszWMACHiResOutput g

## <a name="data-type"></a>Type de données

**VT \_ bool**

## <a name="default-value"></a>Valeur par défaut

**VARIANTE \_ false**

## <a name="remarks"></a>Notes

Affectez à cette propriété la \_ valeur variant true pour décoder le contenu audio multicanaux ou 24 bits, ou l’audio avec un taux d’échantillonnage supérieur à 48 000 Hz. Si le contenu est encodé en haute résolution, mais que cette propriété a \_ la valeur false, les comportements suivants s’appliquent :

-   La sortie DMO sera limitée à 16 bits, 48-KHz stéréo.
-   La table MFT énumère les modes de sortie qui sont limités à 16 bits et n’implique pas de modifications du nombre de canaux ou du taux d’échantillonnage.

Les propriétés du son haute résolution sont transmises dans une structure [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) , et non [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)).

La sortie haute résolution est disponible uniquement si le décodeur s’exécute sous Windows XP ou une version ultérieure. Vous pouvez définir cette propriété indépendamment du système d’exploitation sur lequel votre application s’exécute. Dans les versions de Windows antérieures à Windows XP, le décodeur ignore ce paramètre et remet la sortie standard.

De nombreux lecteurs (y compris le lecteur Windows Media série 9 et versions ultérieures) définissent cette valeur pour tout le contenu.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
