---
description: Vérifie si un pointeur est NULL. Si le pointeur est NULL, la fonction ou la méthode dans laquelle la macro apparaît retourne la valeur spécifiée.
ms.assetid: eca73fbf-5fd8-4b76-af06-ca0c22510b55
title: Macro de point de contrôle (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CheckPointer
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: ef1fa2370def45321958862ebaf3ded341b13f45ddae1ecafdc4a17e937aca08
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119999289"
---
# <a name="checkpointer-macro"></a>Point de contrôle, macro

Vérifie si un pointeur est **null**. Si le pointeur est **null**, la fonction ou la méthode dans laquelle la macro apparaît retourne la valeur spécifiée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CheckPointer(
    p,
    ret
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*p* 
</dt> <dd>

Pointeur à vérifier.

</dd> <dt>

*Av* 
</dt> <dd>

Valeur que la fonction ou la méthode retourne si *p* est **null**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La fonction environnante retourne *RET* si *p* est **null**. Dans le cas contraire, la macro n’entraîne pas le retour de la fonction environnante.

## <a name="examples"></a>Exemples


```
HRESULT MyFunction(VOID *pSomeParameter)
{
    // Return E_INVALIDARG if pSomeParameter is NULL.
    CheckPointer(pSomeParameter, E_INVALIDARG)

    // Rest of the function (not shown).
}
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Wxdebug. h (inclure Flux. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Macros de validation du pointeur](pointer-validation-macros.md)
</dt> </dl>

 

 




