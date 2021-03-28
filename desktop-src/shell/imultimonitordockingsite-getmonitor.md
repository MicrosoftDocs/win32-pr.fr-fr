---
description: Obtient l’analyseur par défaut actuel.
title: 'IMultiMonitorDockingSite :: GetMonitor, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMultiMonitorDockingSite.GetMonitor
api_type:
- COM
api_location: ''
ms.assetid: 0bae75eb-ebd5-4de4-9249-0e9bb489f61f
ms.openlocfilehash: 1260da5ee4404a7ec4597a57e7e3836d6f133426
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991696"
---
# <a name="imultimonitordockingsitegetmonitor-method"></a>IMultiMonitorDockingSite :: GetMonitor, méthode

Obtient l’analyseur par défaut actuel.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetMonitor(
  [in]  IUnknown *punkSrc,
  [out] HMONITOR *phMon
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*punkSrc* \[ dans\]
</dt> <dd>

Tapez : **[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) \** _

Pointeur vers l’objet implémentant l’interface [_ *IDockingWindow* *](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) pour laquelle l’analyse est demandée.

</dd> <dt>

*phMon* \[ à\]
</dt> <dd>

Tapez : **HMONITOR \** _

Quand la fonction retourne une valeur, contient un pointeur vers le handle de l’analyseur par défaut.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : _ *HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                   |



 

 
