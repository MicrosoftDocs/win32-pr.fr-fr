---
title: ExtTextOutWrap fonction)
description: Dessine le texte à l’aide de la police, de la couleur d’arrière-plan et de la couleur de texte actuellement sélectionnées. Vous pouvez éventuellement fournir des dimensions à utiliser pour le découpage, l’opacité ou les deux. Cette fonction encapsule un appel à ExtTextOut.
ms.assetid: 0804c231-53f9-4de6-b703-0077cdcebcb5
keywords:
- Contrôles Windows de la fonction ExtTextOutWrap
topic_type:
- apiref
api_name:
- ExtTextOutWrap
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a173fedb7d8534dbd926a8a147e833435a7710b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102977"
---
# <a name="exttextoutwrap-function"></a>ExtTextOutWrap fonction)

\[**ExtTextOutWrap** est disponible via Windows XP avec Service Pack 2 (SP2). Il peut être modifié ou non disponible dans les versions ultérieures. Nous vous recommandons d’utiliser [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta) directement à la place.\]

Dessine le texte à l’aide de la police, de la couleur d’arrière-plan et de la couleur de texte actuellement sélectionnées. Vous pouvez éventuellement fournir des dimensions à utiliser pour le découpage, l’opacité ou les deux. Cette fonction encapsule un appel à [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta).

## <a name="syntax"></a>Syntaxe


```C++
BOOL ExtTextOutWrap(
  _In_       HDC     hdc,
  _In_       int     X,
  _In_       int     Y,
  _In_       UINT    uOptions,
  _In_ const RECT    *lprc,
  _In_       LPCTSTR lpString,
  _In_       UINT    cbCount,
  _In_ const INT     *lpDx
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*HDC* \[ dans\]
</dt> <dd>

Type : **[ **HDC**](/windows/desktop/WinProg/windows-data-types)**

Handle vers le contexte de périphérique (Device Context).

</dd> <dt>

*X* \[ dans\]
</dt> <dd>

Type : **int**

Coordonnée x, en coordonnées logiques, du point de référence utilisé pour positionner la chaîne.

</dd> <dt>

*Y* \[ dans\]
</dt> <dd>

Type : **int**

Coordonnée y, en coordonnées logiques, du point de référence utilisé pour positionner la chaîne.

</dd> <dt>

*uOptions* \[ dans\]
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Valeurs qui spécifient comment utiliser le rectangle défini par l’application. Pour obtenir la liste complète des options, consultez [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta) .

</dd> <dt>

*LPRC* \[ dans\]
</dt> <dd>

Type : **const [**Rect**](/previous-versions//dd162897(v=vs.85)) \** _

Pointeur vers une structure [_ *Rect* *](/previous-versions//dd162897(v=vs.85)) facultative qui spécifie les dimensions, en coordonnées logiques, d’un rectangle utilisé pour le découpage, l’opacité ou les deux.

</dd> <dt>

*lpString* \[ dans\]
</dt> <dd>

Type : **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**

Pointeur vers une mémoire tampon qui contient le texte à dessiner. Il n’est pas nécessaire que la chaîne se termine par zéro, car *cbCount* spécifie la longueur de la chaîne.

</dd> <dt>

*cbCount* \[ dans\]
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Longueur de la chaîne, en octets, vers laquelle pointe *lpString*.

</dd> <dt>

*lpDx* \[ dans\]
</dt> <dd>

Type : **const [**int**](/windows/desktop/WinProg/windows-data-types) \** _

Pointeur vers un tableau facultatif de valeurs qui indiquent la distance entre les origines des cellules de caractères adjacentes. Par exemple, \[ \] les unités logiques _lpDx * x séparent les origines de la cellule de caractère x et de la cellule de caractère (x + 1).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **bool**](/windows/desktop/WinProg/windows-data-types)**

Retourne une valeur différente de zéro si la chaîne est dessinée correctement. Toutefois, si la version ANSI de [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta) est appelée avec l' \_ index de glyphes ETO \_ , la fonction retourne la **valeur true** même si la fonction ne fait rien.

Si la fonction échoue, la valeur de retour est égale à zéro.

Pour obtenir des informations détaillées sur l’erreur, appelez [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Remarques

**ExtTextOutWrap** n’est pas exporté par nom ou déclaré dans un fichier d’en-tête public. Pour l’utiliser, vous devez utiliser [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) et demander l’ordinal 417 de ComCtl32.dll pour obtenir un pointeur de fonction.

Pour des remarques supplémentaires, consultez [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                                 |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                           |
| DLL<br/>                      | <dl> <dt>Comctl32.dll (version 6,0 ou ultérieure)</dt> </dl> |



 

