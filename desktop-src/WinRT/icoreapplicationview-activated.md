---
description: se produit lors de l’activation d’une application du windows Store Windows.
ms.assetid: CA0DB2D4-3417-48F5-8455-D87D0F323A1E
title: 'Événement ICoreApplicationView :: Activated (Windows. ApplicationModel. Core. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93e736d0fb5403fe76d6d402c261e6b7e5336dfc096d8c39d7b3300b93ab1332
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118560993"
---
# <a name="icoreapplicationviewactivated-event"></a>ICoreApplicationView :: Activated, événement

se produit lors de l’activation d’une application du windows Store Windows.

## <a name="syntax"></a>Syntaxe


```C++
void Activated(
  [in] ITypedEventHandler<ICoreApplicationView*, IActivatedEventArgs*> handler
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Gestionnaire* \[ dans\]
</dt> <dd></dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

N’appelez pas la méthode [**Exit**](/previous-versions//hh438368(v=vs.85)) à partir du *Gestionnaire*.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8<br/>                                                                                         |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                                               |
| En-tête<br/>                   | <dl> <dt>Windows. ApplicationModel. Core. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>Windows. ApplicationModel. Core. idl</dt> </dl> |



 

 
