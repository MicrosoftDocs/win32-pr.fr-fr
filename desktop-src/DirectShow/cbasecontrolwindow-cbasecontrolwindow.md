---
description: Méthode constructeur CBaseControlWindow. CBaseControlWindow.
ms.assetid: 575f7f94-5f55-4834-bdb6-0db877187388
title: Constructeur CBaseControlWindow. CBaseControlWindow (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.CBaseControlWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e4944d121c4fe99ee36c893a4d51ca0cd72344dfa47dde17629f5ca2a1ce3fd1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118660764"
---
# <a name="cbasecontrolwindowcbasecontrolwindow-constructor"></a>Constructeur CBaseControlWindow. CBaseControlWindow

Méthode de constructeur.

## <a name="syntax"></a>Syntaxe


```C++
CBaseControlWindow(
   CBaseMediaFilter *pFilter,
   CCritSec         *pInterfaceLock,
   TCHAR            *pName,
   LPUNKNOWN        pUnk,
   HRESULT          *phr
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pFilter* 
</dt> <dd>

Pointeur vers l’objet de filtre de média propriétaire.

</dd> <dt>

*pInterfaceLock* 
</dt> <dd>

Pointeur vers la section critique à utiliser pour le verrouillage.

</dd> <dt>

*pName* 
</dt> <dd>

Pointeur vers la description de l’objet.

</dd> <dt>

*pUnk* 
</dt> <dd>

Pointeur vers l’interface de contrôle **IUnknown** , si l’objet fait partie d’un agrégat ; dans le cas contraire, doit avoir la **valeur null**.

</dd> <dt>

*phr* 
</dt> <dd>

Pointeur vers une variable qui reçoit une valeur HRESULT indiquant la réussite ou l’échec de la méthode de constructeur.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseControlWindow, classe**](cbasecontrolwindow.md)
</dt> </dl>

 

 




