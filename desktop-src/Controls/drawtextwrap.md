---
title: DrawTextWrap fonction)
description: Dessine du texte mis en forme dans le rectangle spécifié. Il met en forme le texte en fonction de la méthode spécifiée (en développant les onglets, en justifiant les caractères, les sauts de ligne, etc.). Cette fonction encapsule un appel à DrawText.
ms.assetid: 28ab4c5e-3b8f-49e8-b072-500ba1916caf
keywords:
- Contrôles Windows de la fonction DrawTextWrap
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
ms.openlocfilehash: cfc5eb707b4016a592ad339223e0f32ab21d4a29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941719"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                                 |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                           |
| DLL<br/>                      | <dl> <dt>Comctl32.dll (version 6,0 ou ultérieure)</dt> </dl> |



 

