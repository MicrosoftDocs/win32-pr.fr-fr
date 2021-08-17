---
description: Convertit une chaîne de caractères Unicode ou un caractère unique en minuscules.
ms.assetid: 09b7cf8e-6aed-40f4-9dfa-29be3559ae89
title: CharLowerWrapW fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CharLowerWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: c9a02e89713dd82de63817c00d5402fabe991fed565ebe33fa40286ad30058d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119710749"
---
# <a name="charlowerwrapw-function"></a>CharLowerWrapW fonction)

\[**CharLowerWrapW** peut être utilisé dans Windows XP. Elle n’est peut-être pas disponible dans les versions ultérieures. Vous devez utiliser [**CharLowerW**](/windows/win32/api/winuser/nf-winuser-charlowera) à la place.\]

Convertit une chaîne de caractères Unicode ou un caractère unique en minuscules. Si l’opérande est une chaîne de caractères, la fonction convertit les caractères sur place.

> [!Note]  
> **CharLowerWrapW** est un wrapper pour la fonction **CharLowerW** . Pour plus d’informations sur les remarques d’utilisation, consultez la page [**CharLower**](/windows/win32/api/winuser/nf-winuser-charlowera) .

 

## <a name="syntax"></a>Syntaxe


```C++
LPWSTR CharLowerWrapW(
  _Inout_ LPWSTR pch
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*PCH* \[ in, out\]
</dt> <dd>

Type : **LPWStr**

Pointeur vers une chaîne Unicode terminée par le caractère null ou un caractère unique. Si le mot de poids fort de ce paramètre est égal à zéro, le mot de poids faible ne doit contenir qu’un seul caractère à convertir.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **LPWStr**

Si *PCH* est une chaîne de caractères, la fonction retourne un pointeur vers la chaîne convertie. Étant donné que la chaîne est convertie sur place, la valeur de retour est égale à *PCH*.

Si *PCH* est un caractère unique, la valeur de retour est une valeur 32 bits dont le mot de poids fort est égal à zéro et le mot de poids faible contient le caractère converti.

Il n’existe aucune indication de réussite ou d’échec. L’échec est rare. Il n’y a pas d’informations d’erreur étendues pour cette fonction. ne pas appeler [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Remarques

La méthode recommandée consiste à utiliser [**CharLowerW**](/windows/win32/api/winuser/nf-winuser-charlowera) conjointement avec la couche Microsoft pour Unicode (MSLU).

**CharLowerWrapW** doit être appelé directement à partir de Shlwapi.dll, à l’aide de l’ordinal 38.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professional, Windows XP \[ desktop apps uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shlwapi.dll (version 5,0 ou ultérieure)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CharLower**](/windows/win32/api/winuser/nf-winuser-charlowera)
</dt> </dl>

 

 
