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
ms.openlocfilehash: 04f442303e520ef758a3576d21c2df810ef26fb2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106538128"
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
| En-tête<br/> | <dl> <dt>Wxdebug. h (include streams. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Macros de validation du pointeur](pointer-validation-macros.md)
</dt> </dl>

 

 




