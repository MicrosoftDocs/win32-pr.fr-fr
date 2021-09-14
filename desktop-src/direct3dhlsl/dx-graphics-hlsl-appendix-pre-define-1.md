---
title: '\#define, directive (constante)'
description: Directive de préprocesseur qui affecte un nom explicite à une constante dans votre application.
ms.assetid: cc9b34a3-4c83-4999-99ec-e6261ecb2785
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: deae1ca92c2280cd31cbec2bf3482c61fcf2b88a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126941180"
---
# <a name="define-directive-constant"></a>\#define, directive (constante)

Directive de préprocesseur qui affecte un nom explicite à une constante dans votre application.



| \#définir *identifiertoken-chaîne* |
|-----------------------------------|



 

## <a name="parameters"></a>Paramètres



| Élément                                                                                                                       | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="identifier"></span><span id="IDENTIFIER"></span>*identificateur*<br/>                                          | Identificateur de la constante. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="token-string__optional_"></span><span id="TOKEN-STRING__OPTIONAL_"></span>*jeton-chaîne* \[ facultatif\]<br/> | Valeur de la constante. Ce paramètre se compose d’une série de jetons, tels que les mots clés, les constantes ou les instructions complètes. Un ou plusieurs espaces blancs doivent séparer ce paramètre du paramètre *identificateur* ; Cet espace blanc n’est pas considéré comme faisant partie du texte substitué, et n’est pas un espace blanc qui suit le dernier jeton du texte. <br/> Si vous excluez ce paramètre, toutes les instances du paramètre d' *identificateur* sont supprimées du fichier source. L’identificateur reste défini et peut être testé à l’aide des directives [ \# If](dx-graphics-hlsl-appendix-pre-ifdef.md), \# ifdef et \# ifndef définies. <br/> |



 

## <a name="remarks"></a>Notes

Toutes les instances du paramètre d' *identificateur* qui se produisent après la directive [ \# define](dx-graphics-hlsl-appendix-pre-define.md) dans le fichier source sont remplacées par la valeur du paramètre de *chaîne de jeton* . L’identificateur est remplacé uniquement lorsqu’il forme un jeton. par exemple, l’identificateur n’est pas remplacé s’il apparaît dans un commentaire, dans une chaîne ou dans le cadre d’un identificateur plus long.

La directive [ \# undef](dx-graphics-hlsl-appendix-pre-undef.md) indique au préprocesseur d’oublier la définition d’un identificateur. pour plus d’informations, consultez \# directive undef (DirectX HLSL).

La définition de constantes avec l’option de compilateur/D a le même effet que l’utilisation de la directive [ \# define](dx-graphics-hlsl-appendix-pre-define.md) au début de votre fichier. Il est possible de définir jusqu’à 30 constantes avec l’option/D. Pour obtenir un exemple de la façon dont cela peut être utilisé, consultez la section Exemples de [ \# ifdef et)](dx-graphics-hlsl-appendix-pre-ifdef.md).

## <a name="examples"></a>Exemples

L’exemple suivant définit la largeur de l’identificateur en tant que constante entière 80, puis définit la longueur en termes de largeur et la constante entière 10.


```
#define WIDTH       80
#define LENGTH      ( WIDTH + 10 )
```



Chaque instance suivante de LENGTH est remplacée par (WIDTH + 10), et chaque instance suivante de WIDTH + 10 est remplacée par l’expression (80 + 10). Les parenthèses autour de la largeur + 10 sont importantes car elles contrôlent l’interprétation dans des instructions telles que la suivante.


```
var = LENGTH * 20;
```



Après l’étape de prétraitement, l’instruction devient la suivante, qui prend la valeur 1 800.


```
var = ( 80 + 10 ) * 20;
```



Sans parenthèses, le résultat est le suivant, qui prend la valeur 280.


```
var = 80 + 10 * 20;
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Directives de préprocesseur (DirectX HLSL)](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[\#définir des surcharges](dx-graphics-hlsl-appendix-pre-define.md)
</dt> <dt>

[\#undef, directive (DirectX HLSL)](dx-graphics-hlsl-appendix-pre-undef.md)
</dt> </dl>

 

 





