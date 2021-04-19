---
description: Ouvre la clé de Registre spécifiée dans une ruche de Registre hors connexion.
ms.assetid: 4a4afbef-5107-4006-bd67-aecb5d3b5112
title: OROpenKey, fonction (Offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OROpenKey
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 4a55bb2c06d8b2d13491b766bf08184631fa2164
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106521684"
---
# <a name="oropenkey-function"></a>OROpenKey fonction)

Ouvre la clé de Registre spécifiée dans une ruche de Registre hors connexion.

## <a name="syntax"></a>Syntaxe


```C++
DWORD OROpenKey(
  _In_     ORHKEY  Handle,
  _In_opt_ PCWSTR  lpSubKeyName,
  _Out_    PORHKEY phkResult
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Gérer* \[ dans\]
</dt> <dd>

Handle d’une clé de Registre ouverte dans une ruche de Registre hors connexion.

</dd> <dt>

*lpSubKeyName* \[ dans, facultatif\]
</dt> <dd>

Pointeur vers une chaîne UNICODE qui contient le nom de la clé de Registre à ouvrir. Cette clé doit être une sous-clé de la clé identifiée par le paramètre *handle* .

Les noms de clés ne respectent pas la casse.

Si ce paramètre est **null** ou un pointeur vers une chaîne vide, la fonction retourne le même handle que celui qui a été passé. Si la clé spécifiée par le paramètre *descripteur* est la clé racine de la ruche, la fonction retourne un \_ paramètre non valide de l’erreur \_ .

Pour plus d’informations, consultez [limites de taille des éléments du Registre](../sysinfo/registry-element-size-limits.md).

</dd> <dt>

*phkResult* \[ à\]
</dt> <dd>

Pointeur vers une variable qui reçoit un handle vers la clé ouverte. Utilisez la fonction [**ORCloseKey**](orclosekey.md) pour fermer la clé une fois que vous avez fini d’utiliser le handle.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est une erreur de \_ réussite.

Si la fonction échoue, la valeur de retour est un code d’erreur différent de zéro défini dans Winerror. h. Vous pouvez utiliser la fonction [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) avec le format \_ message \_ de l' \_ indicateur système pour obtenir une description générique de l’erreur.

Si le handle à retourner est un descripteur de la clé racine de la ruche, la fonction retourne un \_ paramètre d’erreur non valide \_ .

Si la clé spécifiée a été marquée comme supprimée, cette fonction retourne la clé d’erreur \_ \_ supprimée.

## <a name="remarks"></a>Notes

Impossible d’utiliser la fonction **OROpenKey** pour ouvrir la clé racine dans une ruche de Registre hors connexion. Pour obtenir un descripteur de la clé racine d’une ruche, utilisez la fonction [**OROpenHive**](oropenhive.md) pour charger la ruche en mémoire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|---------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | Bibliothèque du Registre hors connexion Windows version 1,0 ou ultérieure<br/>                      |
| En-tête<br/>          | <dl> <dt>Offreg. h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ORCloseKey**](orclosekey.md)
</dt> <dt>

[**ORCreateKey**](orcreatekey.md)
</dt> <dt>

[**ORDeleteKey**](ordeletekey.md)
</dt> <dt>

[**OROpenHive**](oropenhive.md)
</dt> </dl>

 

 
