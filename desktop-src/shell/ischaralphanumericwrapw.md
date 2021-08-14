---
description: Détermine si un caractère est un caractère alphabétique ou numérique.
ms.assetid: d4b01ba5-e42a-4040-a763-ecef0c73977f
title: IsCharAlphaNumericWrapW fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsCharAlphaNumericWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: bf0a9752162c1593928e1bed270859ec4166230fe1f7e2d46d979c5c989ca237
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118452994"
---
# <a name="ischaralphanumericwrapw-function"></a>IsCharAlphaNumericWrapW fonction)

\[**IsCharAlphaNumericWrapW** peut être utilisé dans Windows XP. Elle ne sera pas disponible dans les versions ultérieures. Vous devez utiliser [**IsCharAlphaNumericW**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica) à la place.\]

Détermine si un caractère est un caractère alphabétique ou numérique. Cette détermination est basée sur la sémantique de la langue sélectionnée par l’utilisateur pendant l’installation ou par le biais du panneau de configuration.

> [!Note]  
> **IsCharAlphaNumericWrapW** est un wrapper pour la fonction **IsCharAlphaNumericW** . Pour plus d’informations sur les remarques d’utilisation, consultez la page [**IsCharAlphaNumeric**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica) .

 

## <a name="syntax"></a>Syntaxe


```C++
BOOL IsCharAlphaNumericWrapW(
  _In_ WCHAR ch
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ch* \[ dans\]
</dt> <dd>

Type : **WCHAR**

Caractère Unicode à tester.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **bool**

Si le caractère est alphanumérique, la valeur de retour est différente de zéro.

Si le caractère n’est pas alphanumérique, la valeur de retour est zéro. Pour obtenir des informations détaillées sur l’erreur, appelez [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Remarques

**IsCharAlphaNumericWrapW** offre la possibilité d’utiliser des chaînes Unicode dans les systèmes d’exploitation antérieurs à Windows XP. La méthode recommandée consiste à utiliser [**IsCharAlphaNumericW**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica) conjointement avec la couche Microsoft pour Unicode (MSLU).

**IsCharAlphaNumericWrapW** doit être appelé directement à partir de Shlwapi.dll, à l’aide de l’ordinal 28.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professional, Windows XP \[ desktop apps uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shlwapi.dll (version 5,0 ou ultérieure)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IsCharAlphaNumeric**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica)
</dt> </dl>

 

 
