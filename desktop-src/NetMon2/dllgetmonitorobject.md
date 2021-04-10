---
description: La fonction DllGetMonitorObject doit être implémentée par le moniteur. Le MCSVC appelle cette fonction pour créer une instance de l’analyse.
ms.assetid: 2c39f752-264c-4ab9-8710-a0d660c4772f
title: Fonction de rappel DllGetMonitorObject (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DllGetMonitorObject
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 723c085fe86e8c24ebc13d83c760e5bfdd08eab2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868222"
---
# <a name="dllgetmonitorobject-callback-function"></a>DllGetMonitorObject fonction de rappel

La fonction **DllGetMonitorObject** doit être implémentée par le moniteur. Le MCSVC appelle cette fonction pour créer une instance de l’analyse.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT DllGetMonitorObject(
  _In_  REFIID riid,
  _Out_ LPVOID *ppObj
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*riid* \[ dans\]
</dt> <dd>

UUID des analyses, illustré ci-dessous, tel que défini dans le fichier d’en-tête IMonitor. h. Si un UUID non valide est fourni, la fonction échoue et l’analyse doit retourner E \_ nointerface.

``` syntax
IID_IMonitor
```

</dd> <dt>

*ppObj* \[ à\]
</dt> <dd>

Pointeur vers un pointeur qui reçoit l’interface demandée dans *riid*.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est S \_ OK (ce qui est identique à la valeur de l’erreur).

Si la fonction échoue, la valeur de retour est un code d’échec. Lorsqu’un code d’erreur est retourné, MCSVC ne crée pas l’objet d’analyse, et la méthode [IUnknown :: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) n’est pas appelée sur le pointeur d’interface.

## <a name="remarks"></a>Notes

La fonction **DllGetMonitorObject** est appelée chaque fois que le MCSVC essaie de créer une instance de l’analyse. Cette fonction est intentionnellement une forte ressemblance avec la fonction [**DllGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject) la plus courante. La principale différence est qu’un CLSID n’est pas transmis à **DllGetMonitorObject**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

