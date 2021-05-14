---
description: 'Prend une structure STRRET retournée par IShellFolder :: GetDisplayNameOf, le convertit en une chaîne et place le résultat dans une mémoire tampon.'
title: StrRetToStrN fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StrRetToStrN
api_type:
- DllExport
api_location:
- Shell32.dll
ms.assetid: a816fb5f-8320-4b63-a85d-dd4c59596ead
ms.openlocfilehash: 50295d712e539c94f10a708674cea595a47ae4e0
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841030"
---
# <a name="strrettostrn-function"></a>StrRetToStrN fonction)

Prend une structure [**STRRET**](/windows/desktop/api/Shtypes/ns-shtypes-strret) retournée par [**IShellFolder :: GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof), le convertit en une chaîne et place le résultat dans une mémoire tampon.

## <a name="syntax"></a>Syntaxe


```C++
BOOL StrRetToStrN(
  _Out_   LPTSTR        pszOut,
  _In_    UINT          cchOut,
  _Inout_ LPSTRRET      pStrRet,
  _In_    LPCITEMIDLIST pidl
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pszOut* \[ à\]
</dt> <dd>

Type : **LPTStr**

Mémoire tampon devant contenir le nom complet. Elle est retournée en tant que chaîne terminée par le caractère null. Si *cchOut* est trop petit, le nom sera tronqué pour s’ajuster.

</dd> <dt>

*cchOut* \[ dans\]
</dt> <dd>

Type : **uint**

Taille de *pszOut*, en caractères. Si *cchOut* est trop petit, la chaîne est tronquée pour s’ajuster.

</dd> <dt>

*pStrRet* \[ in, out\]
</dt> <dd>

Type : **LPSTRRET**

Pointeur vers une structure [**STRRET**](/windows/desktop/api/Shtypes/ns-shtypes-strret) . Quand la fonction retourne, ce pointeur n’est plus valide.

</dd> <dt>

*PIDL* \[ dans\]
</dt> <dd>

Type : **LPCITEMIDLIST**

Pointeur vers la structure [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) de l’élément.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Type : **bool**

**True** en cas de réussite, **false** en cas d’échec.

## <a name="remarks"></a>Notes

> [!Note]  
> À partir de Shell32.dll version 5,0, l’appel de cette fonction équivaut à appeler [**StrRetToBuf**](/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobufa).

 

**StrRetToStrN** n’est pas exporté par nom. Pour l’utiliser, vous devez utiliser [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) et demander l’ordinal 96 de Shell32.dll pour obtenir un pointeur de fonction.

Si le membre **uType** de la structure vers laquelle pointe *pStrRet* est défini sur **STRRET \_ WSTR**, le membre **pOleStr** de cette structure sera libéré au retour.

Notez que cette fonction est exportée à partir de Shell32.dll plutôt que Shlwapi.dll. Il est également inclus dans shlobj. h plutôt que sur Shlwapi. h.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                           |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 4,71 ou ultérieure)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**StrRetToStr**](/windows/desktop/api/Shlwapi/nf-shlwapi-strrettostra)
</dt> <dt>

[**StrRetToBuf**](/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobufa)
</dt> </dl>

 

 
