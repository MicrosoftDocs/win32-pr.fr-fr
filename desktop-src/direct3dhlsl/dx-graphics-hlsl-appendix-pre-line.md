---
title: " Line (directive)"
description: Directive de préprocesseur qui définit le numéro de ligne et le nom de fichier stockés en interne du compilateur sur les valeurs spécifiées.
ms.assetid: 307410af-bd78-4b3d-b515-adf58298f35f
keywords:
- Directive de ligne HLSL
topic_type:
- apiref
api_name:
- line Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0932138ce5aec85ad3d3e7058db0c2a93e131181
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127519241"
---
# <a name="line-directive"></a>\#Line (directive)

Directive de préprocesseur qui définit le numéro de ligne et le nom de fichier stockés en interne du compilateur sur les valeurs spécifiées.



| \#ligne *LineNumber* "*nom_fichier*" |
|----------------------------------|



 

## <a name="parameters"></a>Paramètres



| Élément                                                                                                                              | Description                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="lineNumber"></span><span id="linenumber"></span><span id="LINENUMBER"></span>*lineNumber*<br/>                    | Numéro de ligne à définir. Il peut s’agir de n’importe quelle constante entière. Le remplacement des macros peut être effectué sur les jetons de prétraitement, à condition que le résultat corresponde à la syntaxe correcte. <br/>                     |
| <span id="filename__optional__________"></span><span id="FILENAME__OPTIONAL__________"></span>*nom du fichier* \[ facultatif\] <br/> | Nom de fichier à définir. Le nom de fichier peut être n’importe quelle combinaison de caractères et doit être placé entre guillemets doubles (""). Si ce paramètre est omis, le nom de fichier précédent reste inchangé. <br/> |



 

## <a name="remarks"></a>Notes

Le compilateur utilise le numéro de ligne et le nom de fichier pour faire référence aux erreurs qu’il trouve pendant la compilation. Le numéro de ligne fait généralement référence à la ligne d’entrée en cours et le nom de fichier fait référence au fichier d’entrée en cours. Le numéro de ligne est incrémenté après le traitement de chaque ligne. Si vous modifiez le numéro de ligne et le nom de fichier, le compilateur ignore les valeurs précédentes et continue le traitement avec les nouvelles valeurs. La \# directive line est généralement utilisée par les générateurs de programmes pour que les messages d’erreur fassent référence au fichier source d’origine et non au programme généré.

Le traducteur utilise le numéro de ligne et le nom de fichier pour déterminer les valeurs du fichier de macros prédéfinies et de la \_ \_ \_ \_ \_ \_ ligne \_ \_ . Vous pouvez utiliser ces macros pour insérer des messages d’erreur auto-descriptifs dans le texte du programme. La \_ \_ \_ \_ macro de fichier se développe en une chaîne dont le contenu est le nom de fichier, entouré par des guillemets doubles ("").

## <a name="examples"></a>Exemples

L’exemple suivant définit le numéro de ligne sur 151 et le nom de fichier sur « Copy. c ».


```
#line 151 "copy.c"
```



Dans l’exemple suivant, la macro Assert utilise la ligne et le fichier des macros prédéfinies \_ \_ \_ \_ \_ \_ \_ \_ pour imprimer un message d’erreur relatif au fichier source si l’assertion spécifiée n’a pas la valeur true.


```
#define ASSERT(cond)

if( !(cond) )\
{printf( "assertion error line %d, file(%s)\n", \
__LINE__, __FILE__ );}
```



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Directives de préprocesseur (DirectX HLSL)](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> </dl>

 

 





