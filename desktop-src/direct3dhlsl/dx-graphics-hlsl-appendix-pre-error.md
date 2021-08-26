---
title: " Error (directive)"
description: Directive de préprocesseur qui génère des messages d’erreur au moment du compilateur.
ms.assetid: e32bcd6f-f2c1-43f7-a0bb-2c384b056492
keywords:
- Directive d’erreur (HLSL)
topic_type:
- apiref
api_name:
- error Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5fa1af02a693b5168a2d96e653726fd0a468587bf2b8c1825afbf8e73057f61f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068329"
---
# <a name="error-directive"></a>\#Error (directive)

Directive de préprocesseur qui génère des messages d’erreur au moment du compilateur.



| \#jeton d’erreur *-chaîne* |
|------------------------|



 

## <a name="parameters"></a>Paramètres



| Élément                                                                                    | Description                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="token-string"></span><span id="TOKEN-STRING"></span>*jeton-chaîne*<br/> | Message d’erreur. Ce paramètre se compose d’une série de jetons, tels que les mots clés, les constantes ou les instructions complètes. La chaîne de jeton est sujette à l’expansion macro. <br/> |



 

## <a name="remarks"></a>Remarques

\#les directives d’erreur sont particulièrement utiles pour détecter les incohérences du programmeur et la violation des contraintes lors du prétraitement. Lorsqu’une \# directive d’erreur est rencontrée, la compilation se termine.

## <a name="examples"></a>Exemples

L’exemple suivant illustre le traitement des erreurs pendant le prétraitement.


```
#if !defined(__cplusplus)
  #error C++ compiler required.
#endif
```



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Directives de préprocesseur (DirectX HLSL)](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> </dl>

 

 





