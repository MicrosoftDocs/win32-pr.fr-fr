---
description: Spécifie le nombre de passes d’encodage pris en charge par l’encodeur.
ms.assetid: 8b476164-fd44-4277-89bd-ba9929bf93a2
title: Propriété AVEncCommonMultipassMode (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4302cf0a9524f16dee8e7b84060065a4c750e4e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846669"
---
# <a name="avenccommonmultipassmode-property"></a>Propriété AVEncCommonMultipassMode

Spécifie le nombre de passes d’encodage pris en charge par l’encodeur.

Cette propriété est en lecture seule.

## <a name="data-type"></a>Type de données

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>Guid de propriété

**CODECAPI \_ AVEncCommonMultipassMode**

## <a name="property-value"></a>Valeur de la propriété

Cette propriété est retournée sous la forme d’une plage de valeurs. Pour accéder à la plage prise en charge, appelez [**ICodecAPI :: GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).

## <a name="remarks"></a>Notes

La latence du décodage est définie comme la quantité de données que le décodeur doit mettre en mémoire tampon. Par exemple, la définition de cette propriété sur la **\_ valeur variant true** sur un encodeur vidéo MPEG limite les types de structures GOP que l’encodeur peut utiliser.

Pour définir l’étape d’encodage actuelle, définissez la propriété [**AVEncCommonPassStart**](avenccommonpassstart-property.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows 2000 professionnel- \[ \| applications UWP\]<br/>                     |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows 2000 Server \[ apps- \| applications UWP\]<br/>                           |
| En-tête<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de l’API codec](codec-api-properties.md)
</dt> <dt>

[**Interface ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




