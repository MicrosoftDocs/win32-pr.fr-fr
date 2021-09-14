---
title: DrawTextExPrivWrap fonction)
description: Dessine du texte mis en forme dans le rectangle spécifié. Cette fonction encapsule un appel à DrawTextEx.
ms.assetid: 3212282c-1adb-4f7e-b4d7-7d833b26ac60
keywords:
- DrawTextExPrivWrap, fonction Windows contrôles
topic_type:
- apiref
api_name:
- DrawTextExPrivWrap
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eba496a121af3ba88ed24ab6c9c7834c90153ec0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127124081"
---
# <a name="drawtextexprivwrap-function"></a>DrawTextExPrivWrap fonction)

\[**DrawTextExPrivWrap** est disponible via Windows XP avec Service Pack 2 (SP2). Il peut être modifié ou non disponible dans les versions ultérieures. Nous vous recommandons d’utiliser [**DrawTextEx**](/windows/desktop/api/winuser/nf-winuser-drawtextexa) directement à la place.\]

Dessine du texte mis en forme dans le rectangle spécifié. Cette fonction encapsule un appel à [**DrawTextEx**](/windows/desktop/api/winuser/nf-winuser-drawtextexa).

## <a name="syntax"></a>Syntaxe


```C++
int WINAPI DrawTextExPrivWrap(
  _In_    HDC              hdc,
  _Inout_ LPTSTR           lpchText,
  _In_    int              cchText,
  _Inout_ LPRECT           lprc,
  _In_    UINT             dwDTFormat,
  _In_    LPDRAWTEXTPARAMS lpDTParams
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*HDC* \[ dans\]
</dt> <dd>

Type : **[ **HDC**](/windows/desktop/WinProg/windows-data-types)**

Handle vers le contexte de périphérique dans lequel dessiner.

</dd> <dt>

*lpchText* \[ in, out\]
</dt> <dd>

Type : **[ **LPTStr**](/windows/desktop/WinProg/windows-data-types)**

Pointeur vers une mémoire tampon qui contient le texte à dessiner. Si le paramètre *cchText* a la valeur-1, la chaîne doit se terminer par un caractère null.

Si *dwDTFormat* comprend DT \_ MODIFYSTRING, la fonction peut ajouter jusqu’à quatre caractères supplémentaires à cette chaîne. La mémoire tampon qui contient la chaîne doit être suffisamment grande pour prendre en charge ces caractères supplémentaires.

</dd> <dt>

*cchText* \[ dans\]
</dt> <dd>

Type : **int**

Longueur de la chaîne vers laquelle pointe *lpchText*. Si *cchText* a la valeur-1, le paramètre *lpchText* est supposé être un pointeur vers une chaîne se terminant par le caractère null et [**DrawTextEx**](/windows/desktop/api/winuser/nf-winuser-drawtextexa) calcule le nombre de caractères automatiquement.

</dd> <dt>

*LPRC* \[ in, out\]
</dt> <dd>

Type : **LPRECT**

Pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) qui contient le rectangle, en coordonnées logiques, dans lequel le texte doit être mis en forme.

</dd> <dt>

*dwDTFormat* \[ dans\]
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Options de mise en forme. Pour obtenir la liste complète des options, consultez la documentation de [**DrawTextEx**](/windows/desktop/api/winuser/nf-winuser-drawtextexa) .

</dd> <dt>

*lpDTParams* \[ dans\]
</dt> <dd>

Type : **LPDRAWTEXTPARAMS**

Pointeur vers une structure [**DRAWTEXTPARAMS**](/windows/win32/api/winuser/ns-winuser-drawtextparams) qui spécifie des options de mise en forme supplémentaires. Ce paramètre peut être **NULL**.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **int**

Si la fonction est réussie, la valeur de retour est la hauteur du texte en unités logiques. Si **DT \_ VCENTER** ou **DT \_ Bottom** est spécifié, la valeur de retour est le décalage par rapport au membre **supérieur** de *LPRC* au bas du texte dessiné.

Si la fonction échoue, la valeur de retour est égale à zéro.

Pour obtenir des informations détaillées sur l’erreur, appelez [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Remarques

**DrawTextExPrivWrap** n’est pas exporté par nom ou déclaré dans un fichier d’en-tête public. Pour l’utiliser, vous devez utiliser [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) et demander l’ordinal 416 de ComCtl32.dll pour obtenir un pointeur de fonction.

Pour des remarques supplémentaires, consultez [**DrawTextEx**](/windows/desktop/api/winuser/nf-winuser-drawtextexa).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                                 |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                           |
| DLL<br/>                      | <dl> <dt>Comctl32.dll (version 6,0 ou ultérieure)</dt> </dl> |



 

