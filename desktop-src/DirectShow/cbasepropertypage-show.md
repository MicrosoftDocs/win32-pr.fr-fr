---
description: 'La méthode Show affiche ou masque la boîte de dialogue. Cette méthode implémente la méthode IPropertyPage :: Show.'
ms.assetid: 03796779-ed41-4b68-852d-6b1849a9dc10
title: CBasePropertyPage. Show, méthode (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.Show
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1dadd1c187773df3ca41ac0e1e4daf06fb54761b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526359"
---
# <a name="cbasepropertypageshow-method"></a>CBasePropertyPage. Show, méthode

La `Show` méthode affiche ou masque la boîte de dialogue. Cette méthode implémente la méthode [IPropertyPage :: Show](/windows/win32/api/ocidl/nf-ocidl-ipropertypage-show) .

## <a name="syntax"></a>Syntaxe

```C++
HRESULT Show(
   UINT nCmdShow
);
```
## <a name="parameters"></a>Paramètres

*nCmdShow*

Type : **[uint](../winprog/windows-data-types.md)**

Valeur qui spécifie s’il faut afficher ou masquer la fenêtre. Pour plus d’informations, consultez la méthode [IPropertyPage :: Show](/windows/win32/api/ocidl/nf-ocidl-ipropertypage-show) .

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes.

| Code de retour                                                                                  | Description                    |
|----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | Opération réussie.<br/>            |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Argument non valide.<br/>   |
| <dl> <dt>**E \_ inattendu**</dt> </dl> | Erreur inattendue.<br/> |

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête  | <dl> <dt>Cprop. h (include streams. h)</dt> </dl>                                                                                     |
| Bibliothèque | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |

## <a name="see-also"></a>Voir aussi

[CBasePropertyPage, classe](cbasepropertypage.md)
