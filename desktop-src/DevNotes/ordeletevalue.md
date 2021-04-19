---
description: Supprime une valeur nommée de la clé de Registre spécifiée dans une ruche de Registre hors connexion.
ms.assetid: d2192607-34b8-4915-ac86-8ee206993071
title: ORDeleteValue, fonction (Offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORDeleteValue
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 426765950fd38cbb3e3c99f4001db2965ddb07e3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545630"
---
# <a name="ordeletevalue-function"></a>ORDeleteValue fonction)

Supprime une valeur nommée de la clé de Registre spécifiée dans une ruche de Registre hors connexion.

## <a name="syntax"></a>Syntaxe


```C++
DWORD ORDeleteValue(
  _In_     ORHKEY Handle,
  _In_opt_ PCWSTR lpValueName
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

Valeur de Registre à supprimer. Si ce paramètre a la valeur **null** ou est une chaîne vide, la valeur par défaut sans nom définie par la fonction [**ORSetValue**](orsetvalue.md) est supprimée.

Les noms de valeurs ne respectent pas la casse.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est une erreur de \_ réussite.

Si la fonction échoue, la valeur de retour est un code d’erreur différent de zéro défini dans Winerror. h. Vous pouvez utiliser la fonction [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) avec le format \_ message \_ de l' \_ indicateur système pour obtenir une description générique de l’erreur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|---------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | Bibliothèque du Registre hors connexion Windows version 1,0 ou ultérieure<br/>                      |
| En-tête<br/>          | <dl> <dt>Offreg. h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ORSetValue**](orsetvalue.md)
</dt> </dl>

 

 
