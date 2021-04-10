---
description: Spécifie le mode de contrôle de plage dynamique qui sera utilisé par le décodeur audio.
ms.assetid: 0dbe0c40-39ac-4c1b-9da2-9b142b5bb0eb
title: MFPKEY_WMADEC_DRCMODE, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb612e08ff8bd799ec94faae68763f04db8ad052
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201883"
---
# <a name="mfpkey_wmadec_drcmode-property"></a>MFPKEY \_ WMADEC \_ DRCMODE, propriété

Spécifie le mode de contrôle de plage dynamique qui sera utilisé par le décodeur audio.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

\_wszWMACDRCSetting g

## <a name="data-type"></a>Type de données

VT \_

## <a name="default-value"></a>Valeur par défaut

0

## <a name="remarks"></a>Notes

Cette valeur entière est comprise entre 0 et 2. Plus la valeur est élevée, plus la plage dynamique de la sortie audio non compressée est petite. La valeur 0 indique au codec qu’il n’exécute aucun contrôle de plage dynamique, autrement dit, le codec ne modifiera pas la plage dynamique inhérente du contenu encodé.

Si cette valeur est définie sur 1 ou 2, le codec utilise les propriétés suivantes pour déterminer le contrôle de plage dynamique nécessaire :

-   [MFPKEY \_ WMADRC \_ AVGREF](mfpkey-wmadrc-avgrefproperty.md)
-   [MFPKEY \_ WMADRC \_ PEAKREF](mfpkey-wmadrc-peakrefproperty.md)
-   [MFPKEY \_ WMADRC \_ AVGTARGET](mfpkey-wmadrc-avgtargetproperty.md)
-   [MFPKEY \_ WMADRC \_ PEAKTARGET](mfpkey-wmadrc-peaktargetproperty.md)

Si vous ne fournissez pas de valeurs cibles, le codec fournira sa propre valeur.

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

 

 




