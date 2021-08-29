---
description: Ferme la ruche de Registre hors connexion spécifiée et libère la mémoire allouée pour la ruche.
ms.assetid: e30a92dd-8533-406f-ad63-96306f125d78
title: ORCloseHive, fonction (Offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORCloseHive
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 4852112ff1de3d0650c78b07a2ebbba780e89a485a176cf610fd2cf7b1fa234f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119824829"
---
# <a name="orclosehive-function"></a>ORCloseHive fonction)

Ferme la ruche de Registre hors connexion spécifiée et libère la mémoire allouée pour la ruche.

## <a name="syntax"></a>Syntaxe


```C++
DWORD ORCloseHive(
  _In_ ORHKEY Handle
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Gérer* \[ dans\]
</dt> <dd>

Handle de la clé racine de la ruche de Registre hors connexion à fermer.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est une erreur de \_ réussite.

Si la fonction échoue, la valeur de retour est un code d’erreur différent de zéro défini dans Winerror. h. Vous pouvez utiliser la fonction [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) avec le format \_ message \_ de l' \_ indicateur système pour obtenir une description générique de l’erreur.

## <a name="remarks"></a>Remarques

La fonction **ORCloseHive** libère toute la mémoire allouée par les fonctions de Registre hors connexion pour le compte de la ruche spécifiée.

Pour conserver les modifications apportées à la ruche, appelez la fonction [**ORSaveHive**](orsavehive.md) avant d’appeler **ORCloseHive**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|---------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | Windows Bibliothèque de Registre hors connexion version 1,0 ou ultérieure<br/>                      |
| En-tête<br/>          | <dl> <dt>Offreg. h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**OROpenHive**](oropenhive.md)
</dt> <dt>

[**ORSaveHive**](orsavehive.md)
</dt> </dl>

 

 
