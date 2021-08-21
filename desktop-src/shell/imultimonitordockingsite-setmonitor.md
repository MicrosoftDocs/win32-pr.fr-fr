---
description: Modifie l’analyse qui est utilisée pour les barres d’outils ancrées sur un système à plusieurs écrans.
title: 'IMultiMonitorDockingSite :: SetMonitor, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMultiMonitorDockingSite.SetMonitor
api_type:
- COM
api_location: ''
ms.assetid: ba4ace13-7096-4f05-bcb0-ab37f1632406
ms.openlocfilehash: c79a2ec497e8eaaafead20e6fa01e10844f9c4786a158f869fe16e4eee19e7c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032397"
---
# <a name="imultimonitordockingsitesetmonitor-method"></a>IMultiMonitorDockingSite :: SetMonitor, méthode

Modifie l’analyse qui est utilisée pour les barres d’outils ancrées sur un système à plusieurs écrans.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetMonitor(
  [in]  IUnknown *punkSrc,
  [in]  HMONITOR hMonNew,
  [out] HMONITOR *phMonOld
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*punkSrc* \[ dans\]
</dt> <dd>

Type : **[ **IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***

Pointeur vers l’objet implémentant l’interface [**IDockingWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) pour laquelle l’analyse est en cours de modification.

</dd> <dt>

*hMonNew* \[ dans\]
</dt> <dd>

Type : **HMONITOR**

Handle vers l’analyseur qui remplace l’analyse par défaut existante.

</dd> <dt>

*phMonOld* \[ à\]
</dt> <dd>

Type : **HMONITOR \***

Lorsque cette fonction est retournée, contient un pointeur vers le handle de l’analyseur par défaut précédent.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professional, Windows XP \[ desktop apps uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                   |



 

 
