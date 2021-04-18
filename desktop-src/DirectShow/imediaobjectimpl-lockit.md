---
description: La classe LockIt est une classe interne qui verrouille et déverrouille la classe DMO.
ms.assetid: f516ce22-17ad-488e-a768-3f3849c56087
title: 'IMediaObjectImpl :: LockIt, classe (Dmoimpl. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24fe896ea293ec5e60b038f908cab794274d26e7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526021"
---
# <a name="imediaobjectimpllockit-class"></a>IMediaObjectImpl :: LockIt, classe

La `LockIt` classe est une classe interne qui verrouille et déverrouille la classe DMO.

``` syntax
LockIt(
    _DERIVED_ *p
);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="p"></span><span id="P"></span>*p*
</dt> <dd>

Pointeur vers l’objet dérivé.

</dd> </dl>

## <a name="remarks"></a>Notes

Le `LockIt` constructeur verrouille la DMO, et le destructeur déverrouille la DMO. Pour verrouiller l’objet à l’intérieur de votre classe dérivée, déclarez une variable locale de type `LockIt` . Le DMO est verrouillé alors que l' `LockIt` objet reste dans la portée :


```C++
void SomeMethod()
{
    // The DMO is not locked.
    {
        LockIt dmoLock(this); // Locks the DMO.
        /* ... */
    } 
    // dmoLock goes out of scope, DMO is unlocked.
}
```



Les méthodes dans **IMediaObjectImpl** verrouillent automatiquement la méthode DMO.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Dmoimpl. h</dt> </dl>                                                                     |
| Bibliothèque<br/> | <dl> <dt>Dmoguids. lib ; </dt> <dt>Msdmo. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Modèle de classe IMediaObjectImpl**](imediaobjectimpl-class-template.md)
</dt> </dl>

 

 




