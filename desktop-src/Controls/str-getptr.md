---
title: Str_GetPtr fonction)
description: Copie une chaîne d’une mémoire tampon vers une autre.
ms.assetid: a3dd55a0-3f8b-4d6c-9956-666bebc3ab8d
keywords:
- Str_GetPtr Windows des contrôles de fonction
topic_type:
- apiref
api_name:
- Str_GetPtr
- Str_GetPtrA
- Str_GetPtrW
api_location:
- ComCtl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fec99bb4d91bde86d901c0e7ed4761bafd15f3a5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127116925"
---
# <a name="str_getptr-function"></a>\_Fonction Str GetPtr

\[cette fonction est disponible par le biais de Windows XP avec Service Pack 2 (SP2) et Windows Server 2003. Il peut être modifié ou non disponible dans les versions ultérieures de Windows.\]

Copie une chaîne d’une mémoire tampon vers une autre.

## <a name="syntax"></a>Syntaxe


```C++
int WINAPI Str_GetPtr(
  _In_    LPCTSTR pszSource,
  _Inout_ LPCSTR  pszDest,
  _In_    int     cchDest
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pszSource* \[ dans\]
</dt> <dd>

Type : **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**

Pointeur vers une chaîne source.

</dd> <dt>

*pszDest* \[ in, out\]
</dt> <dd>

Type : **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Pointeur vers la mémoire tampon de destination. Cette valeur peut être **null**.

</dd> <dt>

*cchDest* \[ dans\]
</dt> <dd>

Type : **int**

Taille de *pszDest*, en caractères.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **int**

Si *pszDest* a la **valeur null** ou si *cchDest* est égal à zéro, retourne la taille de la mémoire tampon, en caractères, nécessaire pour contenir une copie terminée par un caractère null de la chaîne pointée par *pszSource*.

Si *pszDest* n’a pas la **valeur null**, retourne le nombre de caractères copiés avec succès, y compris le caractère null de fin.

Si *pszDest* ne peut pas contenir la totalité de la chaîne pointée par *PszSource*, (*cchDest*-1) caractères sont copiés, la chaîne se termine par null et *cchDest* retournée.

## <a name="remarks"></a>Notes

**Chaîne \_ GetPtr** est disponible en tant que versions ANSI (**Str \_ GetPtrA**) et Unicode (**Str \_ GetPtrW**). Ces fonctions ne sont pas exportées par nom ou déclarées dans un fichier d’en-tête public. Pour les utiliser, vous devez utiliser [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) et la requête ordinale 233 (**Str \_ GetPtrA**) ou 235 (**str \_ GetPtrW**) à partir de ComCtl32.dll pour obtenir un pointeur de fonction.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>ComCtl32.dll</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **Chaîne \_ GetPtrW** (Unicode) et **Str \_ GetPtrA** (ANSI)<br/>                       |



 

