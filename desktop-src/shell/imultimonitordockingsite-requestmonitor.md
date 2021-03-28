---
description: Vérifie que le moniteur est actif et disponible.
title: 'IMultiMonitorDockingSite :: RequestMonitor, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMultiMonitorDockingSite.RequestMonitor
api_type:
- COM
api_location: ''
ms.assetid: 9aa6eb20-de39-41f7-a17e-183f4088f972
ms.openlocfilehash: 5389b10af9aaa3da5d3106d82a4fbdcbd614a094
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103953193"
---
# <a name="imultimonitordockingsiterequestmonitor-method"></a>IMultiMonitorDockingSite :: RequestMonitor, méthode

Vérifie que le moniteur est actif et disponible.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT RequestMonitor(
  [in] IUnknown *punkSrc,
  [in] HMONITOR *phMon
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*punkSrc* \[ dans\]
</dt> <dd>

Tapez : **[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) \** _

Pointeur vers l’objet implémentant l’interface [_ *IDockingWindow* *](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) .

</dd> <dt>

*phMon* \[ dans\]
</dt> <dd>

Tapez : **HMONITOR \** _

Pointeur vers le handle de l’analyseur par défaut.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : _ *HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                   |



 

 
