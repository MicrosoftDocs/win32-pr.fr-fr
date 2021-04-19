---
description: Méthode de constructeur.
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
ms.openlocfilehash: 9eb3e50daef8ec4ad11bf96a8f0b605f4c8fe679
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523928"
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
| En-tête<br/>  | <dl> <dt>Ctlutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseControlWindow, classe**](cbasecontrolwindow.md)
</dt> </dl>

 

 




