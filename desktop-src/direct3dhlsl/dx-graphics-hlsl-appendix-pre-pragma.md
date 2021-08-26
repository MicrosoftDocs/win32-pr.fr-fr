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
ms.openlocfilehash: a16101eac6f303dbba03819c8d9f460c06c2613c748ef8ce4c74ae3fe30bb0f9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120024609"
---
# <a name="pragma-directive"></a>\#pragma (directive)

Directive de préprocesseur qui fournit des fonctionnalités spécifiques à l’ordinateur ou au système d’exploitation tout en conservant la compatibilité générale avec les langages C et C++.



| \#pragma *Token-String* |
|-------------------------|



 

## <a name="parameters"></a>Paramètres



| Élément                                                                                    | Description                                                                                                                              |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="token-string"></span><span id="TOKEN-STRING"></span>*jeton-chaîne*<br/> | Série de caractères qui donne une instruction et des arguments spécifiques du compilateur. Ce paramètre est sujet à l’expansion macro. <br/> |



 

## <a name="remarks"></a>Remarques

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

 

 





