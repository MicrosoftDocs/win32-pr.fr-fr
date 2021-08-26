---
title: " Directives ifdef et ifndef"
description: Directives de préprocesseur qui déterminent si une constante ou une macro de préprocesseur spécifique est définie.
ms.assetid: c1cc2e1d-2599-45ec-9629-56c4b42e0d0e
keywords:
- ifdef et ifndef directives HLSL
topic_type:
- apiref
api_name:
- ifdef and ifndef Directives
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 584cde8856c48aeafed5665016a71146f8c2ffb341b837faa6bf35d627152c39
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068319"
---
# <a name="ifdef-and-ifndef-directives"></a>\#Directives ifdef et \# ifndef

Directives de préprocesseur qui déterminent si une constante ou une macro de préprocesseur spécifique est définie.



| \#*identificateur* ifdef...  |
|---------------------------|
| \#endif                   |
| \#ifndef *identificateur* ... |
| \#endif                   |



 

## <a name="parameters"></a>Paramètres



| Élément                                                                              | Description                                               |
|-----------------------------------------------------------------------------------|-----------------------------------------------------------|
| <span id="identifier"></span><span id="IDENTIFIER"></span>*identificateur*<br/> | Identificateur de la constante ou de la macro à vérifier. <br/> |



 

## <a name="remarks"></a>Remarques

Vous pouvez utiliser les \# directives ifdef et \# ifndef partout où peut [ \# ](dx-graphics-hlsl-appendix-pre-if.md) être utilisé. L' \# instruction ifdef est équivalente à la directive. Ces directives vérifient uniquement la présence ou l’absence d’identificateurs définis à l’aide de la directive [ \# define](dx-graphics-hlsl-appendix-pre-define.md) , et non des identificateurs déclarés dans le code source C ou C++.

Ces directives sont fournies uniquement pour des raisons de compatibilité avec les versions antérieures du langage. L’utilisation de l’opérateur [défini](dx-graphics-hlsl-appendix-pre-if.md) avec la \# directive if est recommandée.

La \# directive ifndef vérifie l’inverse de la condition vérifiée par \# ifdef. Si l’identificateur n’est pas défini, la condition est vraie (différente de zéro); dans le cas contraire, la condition est false (zéro).

## <a name="examples"></a>Exemples

identifier peut être passé à partir de la ligne de commande à l'aide de l'option /D. Jusqu'à 30 macros peuvent être spécifiées avec /D. Cela est utile pour vérifier si une définition existe, car une définition peut être transmise à partir de la ligne de commande. L’exemple suivant utilise ce comportement pour déterminer s’il faut exécuter une application en mode test.


```
// PROG.CPP
#ifndef test
  #define final
#endif
int main()
{
}
```



En cas de compilation à l’aide de la commande suivante, Prog. cpp est compilé en mode test. dans le cas contraire, elle sera compilée en mode final.


```
CL.EXE /Dtest prog.cpp
```



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Directives de préprocesseur (DirectX HLSL)](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[\#Si,)](dx-graphics-hlsl-appendix-pre-if.md)
</dt> </dl>

 

 





