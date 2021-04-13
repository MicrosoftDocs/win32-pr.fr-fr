---
description: Se produit lors de l’activation d’une application du Windows Store.
ms.assetid: CA0DB2D4-3417-48F5-8455-D87D0F323A1E
title: 'ICoreApplicationView :: Activated, événement (Windows. ApplicationModel. Core. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 612f7110aa149396b18815afe664ee404c70fc52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201444"
---
# <a name="icoreapplicationviewactivated-event"></a>ICoreApplicationView :: Activated, événement

Se produit lors de l’activation d’une application du Windows Store.

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

## <a name="remarks"></a>Notes

N’appelez pas la méthode [**Exit**](/previous-versions//hh438368(v=vs.85)) à partir du *Gestionnaire*.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8<br/>                                                                                         |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                                               |
| En-tête<br/>                   | <dl> <dt>Windows. ApplicationModel. Core. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>Windows. ApplicationModel. Core. idl</dt> </dl> |



 

 
