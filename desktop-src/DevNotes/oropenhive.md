---
description: Charge le fichier ruche de Registre spécifié en mémoire et valide la ruche.
ms.assetid: 5d8498b0-e1bb-4c3d-bf3d-7bfc3002eb1a
title: OROpenHive, fonction (Offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OROpenHive
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 86ff3d6ff15b030054d40ca7131e521cedb59ebf20c4942951f0e141f27a2840
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076013"
---
# <a name="oropenhive-function"></a>OROpenHive fonction)

Charge le fichier ruche de Registre spécifié en mémoire et valide la ruche.

## <a name="syntax"></a>Syntaxe


```C++
DWORD OROpenHive(
  _In_  PCWSTR  lpHivePath,
  _Out_ PORHKEY phkResult
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lpHivePath* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne Unicode qui spécifie le nom du fichier ruche du Registre à charger en mémoire. Il peut s’agir d’un fichier Hive qui a été enregistré avec la fonction [**ORSaveHive**](orsavehive.md) ou créé avec la fonction [RegSaveKey](/windows/win32/api/winreg/nf-winreg-regsavekeya) ou [RegSaveKeyEx](/windows/win32/api/winreg/nf-winreg-regsavekeyexa) . La taille du fichier doit être inférieure à 4 Go, et l’appelant doit disposer \_ d’un \_ accès aux données en lecture du fichier. Pour plus d’informations, consultez [sécurité des fichiers et droits d’accès](../fileio/file-security-and-access-rights.md).

</dd> <dt>

*phkResult* \[ à\]
</dt> <dd>

Pointeur vers une variable qui reçoit un handle vers la clé racine de la ruche de Registre hors connexion chargée. Si le fichier ruche du registre ne peut pas être ouvert ou si la validation échoue, la fonction affecte la **valeur null** à ce paramètre.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est une erreur de \_ réussite.

Si la fonction échoue, la valeur de retour est un code d’erreur différent de zéro défini dans Winerror. h. Vous pouvez utiliser la fonction [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) avec le format \_ message \_ de l' \_ indicateur système pour obtenir une description générique de l’erreur. Les codes d’erreur possibles sont les suivants :

-   Si la taille du fichier est vide ou supérieure à 4 Go, la fonction retourne l’erreur \_ BADDB.
-   Si l’appelant ne dispose pas des droits d’accès nécessaires pour ouvrir le fichier, la fonction retourne l’erreur \_ accès \_ refusé.
-   Si la ruche du Registre échoue à la validation, la fonction retourne l’erreur \_ non \_ fichier du Registre \_ .

## <a name="remarks"></a>Remarques

La fonction **OROpenHive** est la seule fonction de Registre hors connexion qui valide une ruche de registre. Si la validation échoue, aucune tentative n’est faite pour réparer la ruche.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|---------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | Windows Bibliothèque de Registre hors connexion version 1,0 ou ultérieure<br/>                      |
| En-tête<br/>          | <dl> <dt>Offreg. h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ORCloseHive**](orclosehive.md)
</dt> <dt>

[**ORCreateHive**](orcreatehive.md)
</dt> <dt>

[**ORSaveHive**](orsavehive.md)
</dt> <dt>

[RegSaveKey](/windows/win32/api/winreg/nf-winreg-regsavekeya)
</dt> <dt>

[RegSaveKeyEx](/windows/win32/api/winreg/nf-winreg-regsavekeyexa)
</dt> </dl>

 

 
