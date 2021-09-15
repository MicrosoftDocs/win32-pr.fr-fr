---
title: DEF (directive pragma)
description: Directive pragma qui alloue manuellement un registre de nuanceur à virgule flottante.
ms.assetid: 45db94c4-f6f6-4c88-9bf2-4eaa9abf7844
keywords:
- DEF (directive de pragma)
topic_type:
- apiref
api_name:
- def pragma Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2a921e17f8ddee4aaabfe50e75f42ce44812863d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127519236"
---
# <a name="def-pragma-directive"></a>DEF (directive pragma)

Directive pragma qui alloue manuellement un registre de nuanceur à virgule flottante.



| \#pragma def ( *target*, *Register*, *val1*, *val2*,*val3*, *Val4* ) |
|---------------------------------------------------------------------|



 

## <a name="parameters"></a>Paramètres



| Élément                                                                        | Description                                                                 |
|-----------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="target"></span><span id="TARGET"></span>*Indicatif*<br/>       | Cible qui contient le registre à allouer. <br/>                  |
| <span id="register"></span><span id="REGISTER"></span>*annuler*<br/> | Registre de nuanceur à virgule flottante à allouer. <br/>                     |
| <span id="val0"></span><span id="VAL0"></span>*val0*<br/>             | Premier octet de la valeur à allouer au registre spécifié. <br/>  |
| <span id="val1"></span><span id="VAL1"></span>*val1*<br/>             | Deuxième octet de la valeur à allouer au registre spécifié. <br/> |
| <span id="val2"></span><span id="VAL2"></span>*val2*<br/>             | Troisième octet de la valeur à allouer au registre spécifié. <br/>  |
| <span id="val3"></span><span id="VAL3"></span>*val3*<br/>             | Quatrième octet de la valeur à allouer au registre spécifié. <br/> |



 

## <a name="remarks"></a>Notes

Le pragma def permet à un développeur de préremplir un registre de nuanceur à virgule flottante avec la valeur spécifiée. Ce pragma est rarement utilisé.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Directives de préprocesseur (DirectX HLSL)](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[\#Directive pragma (DirectX HLSL)](dx-graphics-hlsl-appendix-pre-pragma.md)
</dt> </dl>

 

 





