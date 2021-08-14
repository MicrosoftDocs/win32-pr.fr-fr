---
description: Fonction de créateur statique qui peut créer un XamlUIPresenter pour une surface de rendu dans une application de bureau.
ms.assetid: 3160E4C2-39D3-8FF5-ED37-78E645D1AC2E
title: CreateXamlUIPresenter fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateXamlUIPresenter
api_type:
- DllExport
api_location:
- Windows.UI.Xaml.dll
ms.openlocfilehash: 247d676e3e2c85404f96324b1d78e1cd6ec2ab2159092d9a66717b2653ee5a02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118323432"
---
# <a name="createxamluipresenter-function"></a>CreateXamlUIPresenter fonction)

Fonction de créateur statique qui peut créer un [**XamlUIPresenter**](/uwp/api/Windows.UI.Xaml.Hosting.XamlUIPresenter?view=winrt-19041) pour une surface de rendu dans une application de bureau.

## <a name="syntax"></a>Syntaxe


```C++
 static HRESULT WINAPI CreateXamlUIPresenter(
  _In_  IViewObjectPresentNotifySite                 *pPresentSite,
  _Out_ Windows::UI::Xaml::Hosting::IXamlUIPresenter **ppPresenter
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pPresentSite* \[ dans\]
</dt> <dd>

Une interface d’hébergement existante. Consultez **IViewObjectPresentNotifySite** dans la documentation d’Internet Explorer.

</dd> <dt>

*ppPresenter* \[ à\]
</dt> <dd>

Interface **\[ exclusiveto \]** pour un [**XamlUIPresenter**](/uwp/api/Windows.UI.Xaml.Hosting.XamlUIPresenter?view=winrt-19041).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

**HRESULT** standard, **S \_ OK** pour réussite.

## <a name="remarks"></a>Remarques

L’appel de cette méthode requiert un **DllImport** de Windows.UI.Xaml.dll.

vous ne pouvez pas appeler cette méthode à partir d’une application Windows Store.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Windows. ui. xaml-coretypes. idl</dt> </dl> |
| DLL<br/>    | <dl> <dt>Windows.UI.Xaml.dll</dt> </dl>           |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**XamlUIPresenter**](/uwp/api/Windows.UI.Xaml.Hosting.XamlUIPresenter?view=winrt-19041)
</dt> </dl>

 

 
