---
title: GetTextExtentPoint32Wrap fonction)
description: Calcule la largeur et la hauteur de la chaîne de texte spécifiée. Cette fonction encapsule un appel à GetTextExtentPoint.
ms.assetid: 156f9344-6071-451c-94c7-63f369a5573a
keywords:
- Contrôles Windows de la fonction GetTextExtentPoint32Wrap
topic_type:
- apiref
api_name:
- GetTextExtentPoint32Wrap
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6a0db92ad019950cf8be0a72260da75acc06779
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740109"
---
# <a name="gettextextentpoint32wrap-function"></a>GetTextExtentPoint32Wrap fonction)

\[**GetTextExtentPoint32Wrap** est disponible via Windows XP avec Service Pack 2 (SP2). Il peut être modifié ou non disponible dans les versions ultérieures. Nous vous recommandons d’utiliser [**GetTextExtentPoint**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpointa) directement à la place.\]

Calcule la largeur et la hauteur de la chaîne de texte spécifiée. Cette fonction encapsule un appel à [**GetTextExtentPoint**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpointa).

## <a name="syntax"></a>Syntaxe


```C++
BOOL GetTextExtentPoint32Wrap(
  _In_  HDC     hdc,
  _In_  LPCTSTR lpString,
  _In_  UINT    cbCount,
  _Out_ LPSIZE  lpSize
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*HDC* \[ dans\]
</dt> <dd>

Type : **[ **HDC**](/windows/desktop/WinProg/windows-data-types)**

Handle vers le contexte de périphérique (Device Context).

</dd> <dt>

*lpString* \[ dans\]
</dt> <dd>

Type : **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**

Pointeur vers une mémoire tampon qui contient le texte à dessiner. Il n’est pas nécessaire que la chaîne se termine par zéro, car *cbCount* spécifie la longueur de la chaîne.

</dd> <dt>

*cbCount* \[ dans\]
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Longueur, en octets, de la chaîne vers laquelle pointe *lpString*.

</dd> <dt>

*lpSize* \[ à\]
</dt> <dd>

Type : **LPSIZE**

Lorsque cette méthode est retournée, contient un pointeur vers une structure de [**taille**](/previous-versions//dd145106(v=vs.85)) contenant les dimensions de la chaîne, en unités logiques.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **bool**](/windows/desktop/WinProg/windows-data-types)**

Retourne une valeur différente de zéro en cas de réussite ; Sinon, 0.

Pour obtenir des informations détaillées sur l’erreur, appelez [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Remarques

**GetTextExtentPoint32Wrap** n’est pas exporté par nom ou déclaré dans un fichier d’en-tête public. Pour l’utiliser, vous devez utiliser [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) et demander l’ordinal 420 de ComCtl32.dll pour obtenir un pointeur de fonction.

Pour des remarques supplémentaires, consultez [**GetTextExtentPoint**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpointa).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                                  |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                            |
| DLL<br/>                      | <dl> <dt>Comctl32.dll (version 5,81 ou ultérieure)</dt> </dl> |



 

