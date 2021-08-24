---
description: Définit les données pour la valeur d’une clé de Registre spécifiée dans une ruche de Registre hors connexion.
ms.assetid: 62fd3a3a-6ce3-4313-b0e7-37ceea0ce302
title: ORSetValue, fonction (Offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORSetValue
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: ae677a5dff2bcb7189b17c7d1477c95df5a5ae32b0065104b92e426e364d775d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749639"
---
# <a name="orsetvalue-function"></a>ORSetValue fonction)

Définit les données pour la valeur d’une clé de Registre spécifiée dans une ruche de Registre hors connexion.

## <a name="syntax"></a>Syntaxe


```C++
DWORD ORSetValue(
  _In_     ORHKEY Handle,
  _In_opt_ PCWSTR lpValueName,
  _In_     DWORD  dwType,
  _In_opt_ const BYTE *lpData,
  _In_     DWORD  cbData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Gérer* \[ dans\]
</dt> <dd>

Handle d’une clé de Registre ouverte dans une ruche de Registre hors connexion.

</dd> <dt>

*lpValueName* \[ dans, facultatif\]
</dt> <dd>

Nom de la valeur à définir. Si une valeur portant ce nom n’est pas déjà présente dans la clé, la fonction l’ajoute à la clé.

Si *lpValueName* a la valeur **null** ou est une chaîne vide, "", la fonction définit le type et les données pour la valeur sans nom ou par défaut de la clé.

Pour plus d’informations, consultez [limites de taille des éléments du Registre](../sysinfo/registry-element-size-limits.md).

Les clés de Registre n’ont pas de valeurs par défaut, mais elles peuvent avoir une valeur sans nom, qui peut être de n’importe quel type.

</dd> <dt>

*dwType* \[ dans\]
</dt> <dd>

Type de données vers lequel pointe le paramètre *lpData* . Pour obtenir la liste des types possibles, consultez [types de valeurs de Registre](../sysinfo/registry-value-types.md).

</dd> <dt>

*lpData* \[ dans, facultatif\]
</dt> <dd>

Données à stocker.

Pour les types basés sur une chaîne, tels que REG \_ SZ, la chaîne doit se terminer par un caractère null. Pour le \_ type de données Reg multi- \_ SZ, la chaîne doit se terminer par deux caractères null.

</dd> <dt>

*cbData* \[ dans\]
</dt> <dd>

Taille des informations vers lesquelles pointe le paramètre *lpData* , en octets. Si les données sont de type REG \_ SZ, reg \_ expand \_ SZ ou reg \_ \_ multisz, *cbData* doit inclure la taille du ou des caractères null de fin.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est une erreur de \_ réussite.

Si la fonction échoue, la valeur de retour est un code d’erreur différent de zéro défini dans Winerror. h. Vous pouvez utiliser la fonction [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) avec le format \_ message \_ de l' \_ indicateur système pour obtenir une description générique de l’erreur.

## <a name="remarks"></a>Remarques

Les tailles de valeur sont limitées par la mémoire disponible. Les valeurs longues (plus de 2048 octets) doivent être stockées sous forme de fichiers avec les noms de fichiers stockés dans le registre. Cela permet au registre de fonctionner efficacement. Les éléments d’application, tels que les icônes, les bitmaps et les fichiers exécutables, doivent être stockés en tant que fichiers et ne peuvent pas être placés dans le registre.

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

[**OROpenKey**](oropenkey.md)
</dt> </dl>

 

 
