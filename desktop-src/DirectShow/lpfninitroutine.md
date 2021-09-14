---
description: Pointeur vers une fonction qui est appelée à partir du point d’entrée de la DLL.
ms.assetid: 30196657-38ab-42ca-b673-b0894999e566
title: Pointeur de fonction LPFNInitRoutine (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LPFNInitRoutine
api_type:
- UserDefined
api_location:
- Combase.h
ms.openlocfilehash: 375660399180196e2434030ea7551733affc4062
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127007483"
---
# <a name="lpfninitroutine-function-pointer"></a>Pointeur de fonction LPFNInitRoutine

Pointeur vers une fonction qui est appelée à partir du point d’entrée de la DLL.

## <a name="syntax"></a>Syntaxe


```C++
typedef void ( CALLBACK *LPFNInitRoutine)(
         BOOL  bLoading,
   const CLSID *rclsid
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*bLoading* 
</dt> <dd>

**True** lorsque la dll est chargée, **false** lorsque la dll est déchargée.

</dd> <dt>

*rclsid* 
</dt> <dd>

Pointeur vers le CLISD de l’objet, spécifié dans la variable de membre [**CFactoryTemplate :: m \_ ClsID**](cfactorytemplate-m-clsid.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Ce pointeur de fonction ne retourne pas de valeur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>combase. h (inclure Flux. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CFactoryTemplate, classe**](cfactorytemplate.md)
</dt> </dl>

 

 




