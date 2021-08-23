---
description: Supprime une sous-clé et ses valeurs d’une ruche de Registre hors connexion.
ms.assetid: 651795d3-4328-4281-9a7f-ba75b4ec4da1
title: ORDeleteKey, fonction (Offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORDeleteKey
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 9f3be934eca97d88f4dfeb1b1576d9fcd06f5681351a2e85d8ae7f6ba31e8860
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119571929"
---
# <a name="ordeletekey-function"></a>ORDeleteKey fonction)

Supprime une sous-clé et ses valeurs d’une ruche de Registre hors connexion.

## <a name="syntax"></a>Syntaxe


```C++
DWORD ORDeleteKey(
  _In_     ORHKEY Handle,
  _In_opt_ PCWSTR lpSubKey
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Gérer* \[ dans\]
</dt> <dd>

Handle d’une clé de Registre ouverte dans une ruche de Registre hors connexion. Ce descripteur est retourné par la fonction [**ORCreateKey**](orcreatekey.md) ou [**OROpenKey**](oropenkey.md) .

</dd> <dt>

*lpSubKey* \[ dans, facultatif\]
</dt> <dd>

Nom de la clé à supprimer. Il doit s’agir d’une sous-clé de la clé que le *handle* identifie, mais il ne peut pas avoir de sous-clés.

Si la sous-clé n’existe pas, la fonction retourne l’erreur \_ \_ introuvable.

Si ce paramètre a la **valeur null**, la fonction supprime la clé spécifiée par le paramètre *handle* . Si la clé spécifiée par le paramètre *descripteur* est la clé racine de la ruche, la fonction retourne un \_ paramètre non valide de l’erreur \_ .

Les noms de clés ne respectent pas la casse.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est une erreur de \_ réussite.

Si la fonction échoue, la valeur de retour est un code d’erreur différent de zéro défini dans Winerror. h. Vous pouvez utiliser la fonction [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) avec le format \_ message \_ de l' \_ indicateur système pour obtenir une description générique de l’erreur. Les codes d’erreur possibles sont les suivants :

-   Si la sous-clé spécifiée n’existe pas, la fonction retourne le fichier d’erreur \_ \_ \_ introuvable.
-   Si la sous-clé spécifiée est la clé racine de la ruche du Registre, la fonction retourne un paramètre d’erreur \_ non valide \_ .
-   Si la sous-clé spécifiée a des sous-clés, la fonction retourne la clé d’erreur \_ \_ a des \_ enfants.

## <a name="remarks"></a>Remarques

Si la clé de Registre spécifiée existe, elle est marquée comme supprimée. Une clé supprimée n’est pas supprimée tant que le dernier descripteur n’est pas fermé.

La clé à supprimer ne doit pas avoir de sous-clés. Pour supprimer une clé et toutes ses sous-clés, utilisez la fonction [**OREnumKey**](orenumkey.md) pour énumérer les sous-clés et les supprimer individuellement.

Seule la fonction [**ORCloseKey**](orclosekey.md) peut être appelée sur une clé supprimée. toutes les autres opérations de Registre hors connexion échouent. Si la clé supprimée a été créée explicitement en appelant [**ORCreateKey**](orcreatekey.md), les ressources associées à la clé sont libérées lorsque le dernier handle de la clé supprimée est fermé.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|---------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | Windows Bibliothèque de Registre hors connexion version 1,0 ou ultérieure<br/>                      |
| En-tête<br/>          | <dl> <dt>Offreg. h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ORCloseKey**](orclosekey.md)
</dt> <dt>

[**ORCreateKey**](orcreatekey.md)
</dt> <dt>

[**OREnumKey**](orenumkey.md)
</dt> <dt>

[**OROpenKey**](oropenkey.md)
</dt> </dl>

 

 
