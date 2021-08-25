---
title: DrawTextWrap fonction)
description: Dessine du texte mis en forme dans le rectangle spécifié. Il met en forme le texte en fonction de la méthode spécifiée (en développant les onglets, en justifiant les caractères, les sauts de ligne, etc.). Cette fonction encapsule un appel à DrawText.
ms.assetid: 28ab4c5e-3b8f-49e8-b072-500ba1916caf
keywords:
- DrawTextWrap, fonction Windows contrôles
topic_type:
- apiref
api_name:
- DrawTextWrap
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dcbd504955b6ae772ffb3db7bc4cc0223215d6d9ecf880fe7d7e3aa359c992ce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119878289"
---
# <a name="drawtextwrap-function"></a>DrawTextWrap fonction)

\[**DrawTextWrap** est disponible via Windows XP avec Service Pack 2 (SP2). Il peut être modifié ou non disponible dans les versions ultérieures. Il est recommandé d’utiliser [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) directement à la place.\]

Dessine du texte mis en forme dans le rectangle spécifié. Il met en forme le texte en fonction de la méthode spécifiée (en développant les onglets, en justifiant les caractères, les sauts de ligne, etc.). Cette fonction encapsule un appel à [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext).

## <a name="syntax"></a>Syntaxe


```C++
int WINAPI DrawTextWrap(
  _In_    HDC              hdc,
  _Inout_ LPCTSTR          lpString,
  _In_    int              nCount,
  _Inout_ LPRECT           lpRect,
  _In_    UINT             uFormat,
  _In_    LPDRAWTEXTPARAMS lpDTParams
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*HDC* \[ dans\]
</dt> <dd>

Type : **[ **HDC**](/windows/desktop/WinProg/windows-data-types)**

Handle vers le contexte de périphérique (Device Context).

</dd> <dt>

*lpString* \[ in, out\]
</dt> <dd>

Type : **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**

Pointeur vers une mémoire tampon qui contient le texte à dessiner. Si le paramètre *nCount* a la valeur-1, la chaîne doit se terminer par un caractère null.

Si *uFormat* comprend DT \_ MODIFYSTRING, la fonction peut ajouter jusqu’à quatre caractères supplémentaires à cette chaîne. La mémoire tampon qui contient la chaîne doit être suffisamment grande pour prendre en charge ces caractères supplémentaires.

</dd> <dt>

*nCount* \[ dans\]
</dt> <dd>

Type : **int**

Longueur de la chaîne vers laquelle pointe *lpString*. Si *nCount* a la valeur-1, le paramètre *lpString* est supposé être un pointeur vers une chaîne terminée par le caractère null et [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) calcule automatiquement le nombre de caractères.

</dd> <dt>

*lpRect* \[ in, out\]
</dt> <dd>

Type : **LPRECT**

Pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) qui contient le rectangle, en coordonnées logiques, dans lequel le texte doit être mis en forme.

</dd> <dt>

*uFormat* \[ dans\]
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Options de mise en forme. Pour obtenir la liste complète des options, consultez la documentation de [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) .

</dd> <dt>

*lpDTParams* \[ dans\]
</dt> <dd>

Type : **LPDRAWTEXTPARAMS**

Pointeur vers une structure [**DRAWTEXTPARAMS**](/windows/win32/api/winuser/ns-winuser-drawtextparams) qui spécifie des options de mise en forme supplémentaires. Ce paramètre peut être **NULL**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **int**

Si la fonction est réussie, la valeur de retour est la hauteur du texte en unités logiques. Si **DT \_ VCENTER** ou **DT \_ Bottom** est spécifié, la valeur de retour est le décalage par rapport au membre **supérieur** de *LPRC* au bas du texte dessiné si la fonction échoue, la valeur de retour est zéro.

Si la fonction échoue, la valeur de retour est égale à zéro.

Pour obtenir des informations détaillées sur l’erreur, appelez [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Remarques

**DrawTextWrap** n’est pas exporté par nom ou déclaré dans un en-tête public. Pour l’utiliser, vous devez utiliser [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) et demander l’ordinal 415 de ComCtl32.dll pour obtenir un pointeur de fonction.

Pour des remarques supplémentaires, consultez [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                                 |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                           |
| DLL<br/>                      | <dl> <dt>Comctl32.dll (version 6,0 ou ultérieure)</dt> </dl> |



 

