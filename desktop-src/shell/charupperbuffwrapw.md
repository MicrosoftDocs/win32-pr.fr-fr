---
description: Convertit les caractères minuscules d’une mémoire tampon en caractères majuscules.
ms.assetid: 63293fda-6f55-419a-b5b4-7a3ada31580c
title: CharUpperBuffWrapW fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CharUpperBuffWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: 288a119586e9f2e58172daaba33a8b9f27c791aa0005b5349f47cb0b2670a631
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117861554"
---
# <a name="charupperbuffwrapw-function"></a>CharUpperBuffWrapW fonction)

\[**CharUpperBuffWrapW** peut être utilisé dans Windows XP. Elle n’est peut-être pas disponible dans les versions ultérieures. Vous devez utiliser [**CharUpperBuffW**](/windows/win32/api/winuser/nf-winuser-charupperbuffa) à la place.\]

Convertit les caractères minuscules d’une mémoire tampon en caractères majuscules. La fonction convertit les caractères sur place.

> [!Note]  
> **CharUpperBuffWrapW** est un wrapper pour la fonction **CharUpperBuffW** . Pour plus d’informations sur les remarques d’utilisation, consultez la page [**CharUpperBuff**](/windows/win32/api/winuser/nf-winuser-charupperbuffa) .

 

## <a name="syntax"></a>Syntaxe


```C++
DWORD CharUpperBuffWrapW(
  _In_ LPWSTR pch,
  _In_ DWORD  cchLength
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*PCH* \[ dans\]
</dt> <dd>

Type : **LPWStr**

Pointeur vers une mémoire tampon qui contient un ou plusieurs caractères Unicode à traiter.

</dd> <dt>

*cchLength* \[ dans\]
</dt> <dd>

Type : **DWORD**

Spécifie la taille, en caractères, de la mémoire tampon vers laquelle pointe *PCH*.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **DWORD**

Nombre de caractères traités.

## <a name="remarks"></a>Remarques

La méthode recommandée consiste à utiliser [**CharUpperBuffW**](/windows/win32/api/winuser/nf-winuser-charupperbuffa) conjointement avec la couche Microsoft pour Unicode (MSLU).

**CharUpperBuffWrapW** doit être appelé directement à partir de Shlwapi.dll, à l’aide de l’ordinal 44.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professional, Windows XP \[ desktop apps uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shlwapi.dll (version 5,0 ou ultérieure)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CharUpperBuff**](/windows/win32/api/winuser/nf-winuser-charupperbuffa)
</dt> </dl>

 

 
