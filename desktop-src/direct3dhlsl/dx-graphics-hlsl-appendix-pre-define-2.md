---
title: '\#define, directive (macro)'
description: Directive de préprocesseur qui crée une macro de type fonction.
ms.assetid: 73c19cf8-fbc5-444b-a51f-dc9f881f397b
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d0c54c0c433c91522c8a72c5955a419eb72f9eee
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387515"
---
# <a name="define-directive-macro"></a>\#define, directive (macro)

Directive de préprocesseur qui crée une macro de type fonction.



| \#définir l' *identificateur*( *argument0*,..., *argumentN-1* ) *-chaîne de jeton* |
|--------------------------------------------------------------------------|



 

## <a name="parameters"></a>Paramètres



| Élément                                                                                                                                                                                                                                                          | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="identifier"></span><span id="IDENTIFIER"></span>*identificateur*<br/>                                                                                                                                                                             | Identificateur de la macro. <br/> Une deuxième [ \# définition](dx-graphics-hlsl-appendix-pre-define.md) pour une macro avec un identificateur qui existe déjà dans le contexte actuel génère une erreur, à moins que la deuxième séquence de jeton soit identique à la première. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="___________argument0___...___argumentN-1_________"></span><span id="___________argument0___...___argumentn-1_________"></span><span id="___________ARGUMENT0___...___ARGUMENTN-1_________"></span> ( *argument0*,..., *argumentN-1* ) <br/> | Liste d’arguments pour la macro. La liste d’arguments est délimitée par des virgules, peut être de n’importe quelle longueur et doit être placée entre parenthèses. Chaque nom d’argument dans la liste doit être unique. Aucun espace blanc ne peut séparer le paramètre d' *identificateur* et la parenthèse ouvrante. <br/> Utiliser la concaténation de ligne Placez une barre oblique inverse ( \\ ) juste avant le caractère de saut de ligne pour fractionner les directives longues en plusieurs lignes sources. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="token-string__optional________"></span><span id="TOKEN-STRING__OPTIONAL________"></span>*jeton-chaîne* \[ facultatif\] <br/>                                                                                                                     | Valeur de la macro. Ce paramètre se compose d’une série de jetons, tels que les mots clés, les constantes ou les instructions complètes. Un ou plusieurs espaces blancs doivent séparer ce paramètre du paramètre *identificateur* ; Cet espace blanc n’est pas considéré comme faisant partie du texte substitué, et n’est pas un espace blanc qui suit le dernier jeton du texte. Utilisez des parenthèses pour vous assurer que les arguments complexes sont interprétés correctement. <br/> Si la valeur du paramètre *identificateur* est comprise dans le paramètre de *chaîne de jeton* (même suite à une autre expansion macro), il n’est pas développé. <br/> Si vous excluez ce paramètre, toutes les instances du paramètre d' *identificateur* sont supprimées du fichier source. L’identificateur reste défini et peut être testé à l’aide des directives [ \# If](dx-graphics-hlsl-appendix-pre-ifdef.md), \# ifdef et \# ifndef définies. <br/> |



 

## <a name="remarks"></a>Remarques

Toutes les instances du paramètre d' *identificateur* qui se produisent après la directive [ \# define](dx-graphics-hlsl-appendix-pre-define.md) dans le fichier source constituent un appel de macro, et l’identificateur est remplacé par une version du paramètre de *chaîne de jeton* dont les arguments réels sont remplacés par des paramètres formels. Le nombre de paramètres dans l’appel doit correspondre au nombre de paramètres dans la définition de macro. L’identificateur est remplacé uniquement lorsqu’il forme un jeton. par exemple, l’identificateur n’est pas remplacé s’il apparaît dans un commentaire, dans une chaîne ou dans le cadre d’un identificateur plus long.

La directive [ \# undef](dx-graphics-hlsl-appendix-pre-undef.md) indique au préprocesseur d’oublier la définition d’un identificateur. pour plus d’informations, consultez \# directive undef (DirectX HLSL).

La définition de constantes avec l’option de compilateur/D a le même effet que l’utilisation de la directive [ \# define](dx-graphics-hlsl-appendix-pre-define.md) au début de votre fichier. Jusqu’à 30 macros peuvent être définies avec l’option/D.

Les arguments réels dans l’appel de macro sont mis en correspondance avec les arguments formels correspondants dans la définition de macro. Chaque argument formel dans la chaîne de jeton est remplacé par l’argument réel correspondant, à moins que l’argument ne soit précédé d’un \# opérateur String (), Charing ( \# @) ou de collage de jeton ( \# \# ), ou qu’il soit suivi d’un \# \# opérateur. Toutes les macros figurant dans l'argument réel sont développées avant que la directive ne remplace le paramètre formel.

Le collage de jetons dans le compilateur HLSL est légèrement différent du collage de jeton dans le compilateur C, en ce que les jetons collés doivent être eux-mêmes des jetons valides. Par exemple, considérez la définition de macro suivante :


```
#define MERGE(a, b) a##b
MERGE(float, 4x4) test;
```



Dans le compilateur C, les résultats sont les suivants :


```
float4x4 test
```



Toutefois, dans le compilateur HLSL, les résultats sont les suivants :


```
float4 x4 test
```



Vous pouvez contourner ce comportement en utilisant la définition de macro suivante à la place.


```
MERGE(MERGE(float, 4), x4) test;
```



## <a name="examples"></a>Exemples

L’exemple suivant utilise une macro pour définir des lignes de curseur.


```
#define CURSOR(top, bottom) (((top) << 8) | (bottom))
```



L’exemple suivant définit une macro qui récupère un entier Pseudo-aléatoire dans la plage spécifiée.


```
#define getrandom(min, max) \
((rand()%(int)(((max) + 1)-(min)))+ (min))
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Directives de préprocesseur (DirectX HLSL)](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[\#définir des surcharges](dx-graphics-hlsl-appendix-pre-define.md)
</dt> <dt>

[\#undef, directive (DirectX HLSL)](dx-graphics-hlsl-appendix-pre-undef.md)
</dt> </dl>

 

 





