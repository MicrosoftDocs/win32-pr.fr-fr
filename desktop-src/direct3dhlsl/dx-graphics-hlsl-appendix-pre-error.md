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
ms.openlocfilehash: 362150e494398abbc708416e6bfca6aa83756c52
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104380786"
---
# <a name="error-directive"></a>\#Error (directive)

Directive de préprocesseur qui génère des messages d’erreur au moment du compilateur.



| \#jeton d’erreur *-chaîne* |
|------------------------|



 

## <a name="parameters"></a>Paramètres



| Élément                                                                                    | Description                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="token-string"></span><span id="TOKEN-STRING"></span>*jeton-chaîne*<br/> | Message d’erreur. Ce paramètre se compose d’une série de jetons, tels que les mots clés, les constantes ou les instructions complètes. La chaîne de jeton est sujette à l’expansion macro. <br/> |



 

## <a name="remarks"></a>Notes

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

 

 





