---
title: " pragma (directive)"
description: Directive de préprocesseur qui fournit des fonctionnalités spécifiques à l’ordinateur ou au système d’exploitation tout en conservant la compatibilité générale avec les langages C et C++.
ms.assetid: 806ddb9b-ae4b-4dd3-a2c4-39c9cb7f3820
keywords:
- Directive de pragma HLSL
topic_type:
- apiref
api_name:
- pragma Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1f843a218e39daf616fa6c59ca27f73a5511f17b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127519228"
---
# <a name="pragma-directive"></a>\#pragma (directive)

Directive de préprocesseur qui fournit des fonctionnalités spécifiques à l’ordinateur ou au système d’exploitation tout en conservant la compatibilité générale avec les langages C et C++.



| \#pragma *Token-String* |
|-------------------------|



 

## <a name="parameters"></a>Paramètres



| Élément                                                                                    | Description                                                                                                                              |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="token-string"></span><span id="TOKEN-STRING"></span>*jeton-chaîne*<br/> | Série de caractères qui donne une instruction et des arguments spécifiques du compilateur. Ce paramètre est sujet à l’expansion macro. <br/> |



 

## <a name="remarks"></a>Notes

Si le compilateur trouve un pragma qu’il ne reconnaît pas, il émet un avertissement, mais la compilation se poursuit.

Le compilateur HLSL reconnaît les pragmas suivants :

-   [def](dx-graphics-hlsl-appendix-pre-pragma-def.md)
-   [message](message-pragma-directive--directx-hlsl-.md)
-   [matrice de Pack \_](dx-graphics-hlsl-appendix-pre-pragma-pack-matrix.md)
-   [warning](dx-graphics-hlsl-appendix-pre-pragma-warning.md)

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Directives de préprocesseur (DirectX HLSL)](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> </dl>

 

 





