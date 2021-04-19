---
description: Spécifie le niveau de volume moyen de contenu audio.
ms.assetid: eabb36ff-300f-4ed1-aca3-9415627ac1a7
title: MFPKEY_WMADRC_AVGREF, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf18c37b00f84cc3ae3fdf1f44b2fbefcc56d9f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106521455"
---
# <a name="mfpkey_wmadrc_avgref-property"></a>MFPKEY \_ WMADRC \_ AVGREF, propriété

Spécifie le niveau de volume moyen de contenu audio.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

\_wszWMADRCAverageReference g

## <a name="data-type"></a>Type de données

VT \_

## <a name="remarks"></a>Notes

Vous pouvez récupérer cette valeur à partir de l’encodeur une fois le contenu traité. Cette valeur peut également être définie sur le décodeur à des fins de contrôle de plage dynamique, mais n’a d’effet que si la propriété [MFPKEY \_ WMADEC \_ DRCMODE](mfpkey-wmadec-drcmodeproperty.md) est définie.

Pour plus d’informations sur le contrôle de plage dynamique, consultez l’article Web [Windows Media Audio fonctionnalités du codec professionnel](/previous-versions/ms867218(v=msdn.10)).

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

 

 
