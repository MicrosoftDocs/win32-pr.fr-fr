---
description: Énumère les sous-clés de la clé de Registre ouverte spécifiée dans une ruche de Registre hors connexion. La fonction récupère des informations sur une sous-clé chaque fois qu’elle est appelée.
ms.assetid: 46d13c37-473a-4772-992c-a565ad702fb9
title: OREnumKey, fonction (Offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OREnumKey
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: ab72c9b0df79d464f802a1c574b749d04a8a16e89645f25959681e7f03eea5ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120058709"
---
# <a name="orenumkey-function"></a>OREnumKey fonction)

Énumère les sous-clés de la clé de Registre ouverte spécifiée dans une ruche de Registre hors connexion. La fonction récupère des informations sur une sous-clé chaque fois qu’elle est appelée.

## <a name="syntax"></a>Syntaxe


```C++
DWORD OREnumKey(
  _In_        ORHKEY    Handle,
  _In_        DWORD     dwIndex,
  _Out_       PWSTR     lpName,
  _Inout_     PDWORD    lpcName,
  _Out_opt_   PWSTR     lpClass,
  _Inout_opt_ PDWORD    lpcClass,
  _Out_opt_   PFILETIME lpftLastWriteTime
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Gérer* \[ dans\]
</dt> <dd>

Handle d’une clé de Registre ouverte dans une ruche de Registre hors connexion.

</dd> <dt>

*dwIndex* \[ dans\]
</dt> <dd>

Index de la sous-clé à récupérer. Ce paramètre doit avoir la valeur zéro pour le premier appel à la fonction, puis être incrémenté pour les appels suivants.

Comme les sous-clés ne sont pas triées, toute nouvelle sous-clé aura un index arbitraire. Cela signifie que la fonction peut retourner des sous-clés dans n’importe quel ordre.

</dd> <dt>

*lpName* \[ à\]
</dt> <dd>

Pointeur vers une mémoire tampon qui reçoit le nom de la sous-clé, y compris le caractère null de fin. La fonction copie uniquement le nom de la sous-clé, et non la hiérarchie de clé complète, dans la mémoire tampon. Si la fonction échoue, aucune information n’est copiée dans cette mémoire tampon.

Pour plus d’informations, consultez [limites de taille des éléments du Registre](../sysinfo/registry-element-size-limits.md).

</dd> <dt>

*lpcName* \[ in, out\]
</dt> <dd>

Pointeur vers une variable qui spécifie la taille de la mémoire tampon spécifiée par le paramètre *lpName* , dans **WCHARs**. Cette taille doit inclure le caractère null de fin. Si la fonction est réussie, la variable vers laquelle pointe *lpcName* contient le nombre de caractères stockés dans la mémoire tampon, à l’exclusion du caractère null de fin.

</dd> <dt>

*lpClass* \[ out, facultatif\]
</dt> <dd>

Pointeur vers une mémoire tampon qui reçoit la chaîne de classe terminée par le caractère null de la sous-clé énumérée. Ce paramètre peut être **NULL**.

</dd> <dt>

*lpcClass* \[ in, out, facultatif\]
</dt> <dd>

Pointeur vers une variable qui spécifie la taille de la mémoire tampon spécifiée par le paramètre *lpClass* , dans **WCHARs**. La taille doit inclure le caractère null de fin. Si la fonction est réussie, *lpcClass* contient le nombre de caractères stockés dans la mémoire tampon, à l’exclusion du caractère null de fin. Ce paramètre peut être **null** uniquement si *LpClass* a la **valeur null**.

</dd> <dt>

*lpftLastWriteTime* \[ out, facultatif\]
</dt> <dd>

Pointeur vers une structure [fileTime](/windows/win32/api/minwinbase/ns-minwinbase-filetime) qui reçoit l’heure de la dernière écriture dans la sous-clé énumérée. Ce paramètre peut être **NULL**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est une erreur de \_ réussite.

Si la fonction échoue, la valeur de retour est un code d’erreur différent de zéro défini dans Winerror. h. Vous pouvez utiliser la fonction [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) avec le format \_ message \_ de l' \_ indicateur système pour obtenir une description générique de l’erreur. Les codes d’erreur possibles sont les suivants :

-   Si la mémoire tampon *lpName* est trop petite pour recevoir le nom de la clé, la fonction retourne l’erreur \_ plus de \_ données.
-   S’il n’y a plus de sous-clés disponibles, la fonction retourne l’erreur plus \_ aucun \_ \_ élément.

## <a name="remarks"></a>Remarques

Pour énumérer les sous-clés, une application doit appeler initialement la fonction **OREnumKey** avec le paramètre *dwIndex* défini sur zéro. L’application doit ensuite incrémenter le paramètre *dwIndex* et appeler **OREnumKey** jusqu’à ce qu’il n’y ait plus de sous-clés (ce qui signifie que la fonction retourne l’erreur \_ aucun \_ autre \_ élément).

L’application peut également définir *dwIndex* sur l’index de la dernière sous-clé sur le premier appel à la fonction et décrémenter l’index jusqu’à ce que la sous-clé avec l’index 0 soit énumérée. Pour récupérer l’index de la dernière sous-clé, utilisez la fonction [**ORQueryInfoKey**](/windows/win32/api/winreg/nf-winreg-regqueryinfokeya) .

Lorsqu’une application utilise la fonction **OREnumKey** , elle ne doit pas effectuer d’appels à des fonctions de Registre hors connexion qui peuvent modifier la clé énumérée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|---------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | Windows Bibliothèque de Registre hors connexion version 1,0 ou ultérieure<br/>                      |
| En-tête<br/>          | <dl> <dt>Offreg. h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ORCreateKey**](orcreatekey.md)
</dt> <dt>

[**ORDeleteKey**](ordeletekey.md)
</dt> <dt>

[**OROpenKey**](oropenkey.md)
</dt> <dt>

[**ORQueryInfoKey**](orqueryinfokey.md)
</dt> </dl>

 

 
