---
description: Récupère des informations sur la clé de Registre spécifiée dans une ruche de Registre hors connexion.
ms.assetid: b565c55c-acc2-4880-91eb-7bd9188e4749
title: ORQueryInfoKey, fonction (Offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORQueryInfoKey
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: bb7bf6d4a9440e648844e6e18d9b4965b0240de98f8f27f4aac142276142515b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120058609"
---
# <a name="orqueryinfokey-function"></a>ORQueryInfoKey fonction)

Récupère des informations sur la clé de Registre spécifiée dans une ruche de Registre hors connexion.

## <a name="syntax"></a>Syntaxe


```C++
DWORD ORQueryInfoKey(
  _In_        ORHKEY    Handle,
  _Out_opt_   PWSTR     lpClass,
  _Inout_opt_ PDWORD    lpcClass,
  _Out_opt_   PDWORD    lpcSubKeys,
  _Out_opt_   PDWORD    lpcMaxSubKeyLen,
  _Out_opt_   PDWORD    lpcMaxClassLen,
  _Out_opt_   PDWORD    lpcValues,
  _Out_opt_   PDWORD    lpcMaxValueNameLen,
  _Out_opt_   PDWORD    lpcMaxValueLen,
  _Out_opt_   PDWORD    lpcbSecurityDescriptor,
  _Out_opt_   PFILETIME lpftLastWriteTime
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Gérer* \[ dans\]
</dt> <dd>

Handle d’une clé de Registre ouverte dans une ruche de Registre hors connexion.

</dd> <dt>

*lpClass* \[ out, facultatif\]
</dt> <dd>

Pointeur vers une mémoire tampon qui reçoit la classe de clé. Ce paramètre peut être **NULL**.

</dd> <dt>

*lpcClass* \[ in, out, facultatif\]
</dt> <dd>

Pointeur vers une variable qui spécifie la taille de la mémoire tampon vers laquelle pointe le paramètre *lpClass* , en caractères.

La taille doit inclure le caractère null de fin. Quand la fonction retourne une valeur, cette variable contient la taille de la chaîne de classe qui est stockée dans la mémoire tampon. Le nombre retourné n’inclut pas le caractère null de fin. Si la mémoire tampon n’est pas assez grande, la fonction retourne l’erreur \_ plus \_ de données et la variable contient la taille de la chaîne, en caractères, sans compter le caractère null de fin.

Si *lpClass* a la **valeur null**, *LpcClass* peut avoir la **valeur null**.

Si le paramètre *lpClass* est une adresse valide, mais que le paramètre *lpcClass* n’est pas (par exemple, si le paramètre *lpcClass* a la **valeur null**), la fonction retourne un paramètre d’erreur \_ non valide \_ .

</dd> <dt>

*lpcSubKeys* \[ out, facultatif\]
</dt> <dd>

Pointeur vers une variable qui reçoit le nombre de sous-clés contenues dans la clé spécifiée. Ce paramètre peut être **NULL**.

</dd> <dt>

*lpcMaxSubKeyLen* \[ out, facultatif\]
</dt> <dd>

Pointeur vers une variable qui reçoit la taille de la sous-clé de la clé avec le nom le plus long, en caractères Unicode, à l’exclusion du caractère null de fin. Ce paramètre peut être **NULL**.

</dd> <dt>

*lpcMaxClassLen* \[ out, facultatif\]
</dt> <dd>

Pointeur vers une variable qui reçoit la taille de la chaîne la plus longue qui spécifie une classe de sous-clé, en caractères Unicode. Le nombre retourné n’inclut pas le caractère null de fin. Ce paramètre peut être **NULL**.

</dd> <dt>

*lpcValues* \[ out, facultatif\]
</dt> <dd>

Pointeur vers une variable qui reçoit le nombre de valeurs associées à la clé. Ce paramètre peut être **NULL**.

</dd> <dt>

*lpcMaxValueNameLen* \[ out, facultatif\]
</dt> <dd>

Pointeur vers une variable qui reçoit la taille du nom de la valeur la plus longue de la clé, en caractères Unicode. La taille n’inclut pas le caractère null de fin. Ce paramètre peut être **NULL**.

</dd> <dt>

*lpcMaxValueLen* \[ out, facultatif\]
</dt> <dd>

Pointeur vers une variable qui reçoit la taille du composant de données le plus long parmi les valeurs de la clé, en octets. Ce paramètre peut être **NULL**.

</dd> <dt>

*lpcbSecurityDescriptor* \[ out, facultatif\]
</dt> <dd>

Pointeur vers une variable qui reçoit la taille du descripteur de sécurité de la clé, en octets. Ce paramètre peut être **NULL**.

</dd> <dt>

*lpftLastWriteTime* \[ out, facultatif\]
</dt> <dd>

Pointeur vers une structure [fileTime](/windows/win32/api/minwinbase/ns-minwinbase-filetime) qui reçoit l’heure de la dernière écriture. Ce paramètre peut être **NULL**.

La fonction définit les membres de la structure [fileTime](/windows/win32/api/minwinbase/ns-minwinbase-filetime) pour indiquer l’heure de la dernière modification de la clé ou de l’une de ses entrées de valeur.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est une erreur de \_ réussite.

Si la fonction échoue, la valeur de retour est un code d’erreur différent de zéro défini dans Winerror. h. Vous pouvez utiliser la fonction [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) avec le format \_ message \_ de l' \_ indicateur système pour obtenir une description générique de l’erreur.

Si la mémoire tampon *lpClass* est trop petite pour recevoir le nom de la classe, la fonction retourne l’erreur \_ plus de \_ données.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|---------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | Windows Bibliothèque de Registre hors connexion version 1,0 ou ultérieure<br/>                      |
| En-tête<br/>          | <dl> <dt>Offreg. h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime)
</dt> <dt>

[**ORCreateKey**](orcreatekey.md)
</dt> <dt>

[**OROpenKey**](oropenkey.md)
</dt> <dt>

[**ORDeleteKey**](ordeletekey.md)
</dt> </dl>

 

 
