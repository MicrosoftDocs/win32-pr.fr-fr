---
description: Crée une ruche de Registre hors connexion qui contient une clé racine vide unique.
ms.assetid: 985cfea4-6f15-4d63-8e41-df2a490296a3
title: ORCreateHive, fonction (Offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORCreateHive
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: b7eae388675cebe300a3dd84607d6bff56078a14addb29d42d6fe76d2b2f6427
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045301"
---
# <a name="orcreatehive-function"></a>ORCreateHive fonction)

Crée une ruche de Registre hors connexion qui contient une clé racine vide unique.

## <a name="syntax"></a>Syntaxe


```C++
DWORD ORCreateHive(
  _Out_ PORHKEY phkResult
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*phkResult* \[ à\]
</dt> <dd>

Pointe vers une variable pour recevoir un descripteur de la clé racine de la ruche de Registre hors connexion nouvellement créée. Si la ruche ne peut pas être créée, la fonction affecte la **valeur null** à ce paramètre.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est une erreur de \_ réussite.

Si la fonction échoue, la valeur de retour est un code d’erreur différent de zéro défini dans Winerror. h. Vous pouvez utiliser la fonction [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) avec le format \_ message \_ de l' \_ indicateur système pour obtenir une description générique de l’erreur.

Si la mémoire est insuffisante pour créer la ruche du Registre, la fonction retourne une erreur de \_ \_ mémoire insuffisante \_ .

## <a name="remarks"></a>Remarques

La fonction **ORCreateHive** crée une ruche de Registre hors connexion vide en mémoire. Utilisez les fonctions [**ORCreateKey**](orcreatekey.md) et [**ORSetValue**](orsetvalue.md) pour ajouter des clés et définir leurs valeurs.

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

[**OROpenHive**](oropenhive.md)
</dt> <dt>

[**ORSaveHive**](orsavehive.md)
</dt> <dt>

[**ORSetValue**](orsetvalue.md)
</dt> </dl>

 

 
