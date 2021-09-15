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
ms.openlocfilehash: be773ee68c214f6a2fab8da89f1f48b867e71239
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127525400"
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

## <a name="return-value"></a>Valeur de retour

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professional, Windows XP \[ desktop apps uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                   |



 

 
