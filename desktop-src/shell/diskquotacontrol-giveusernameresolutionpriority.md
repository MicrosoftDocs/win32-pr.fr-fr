---
description: Place l’objet utilisateur spécifié en regard de la résolution de nom.
ms.assetid: 4c75f966-2e7d-4415-b1db-c98f8bdd4ce3
title: Méthode DiskQuotaControl. GiveUserNameResolutionPriority (dskquota. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.GiveUserNameResolutionPriority
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 1acf50e0cec59a7ee14fbd9d7760fb68b27c4de5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525330"
---
# <a name="diskquotacontrolgiveusernameresolutionpriority-method"></a>Méthode DiskQuotaControl. GiveUserNameResolutionPriority

Place l’objet utilisateur spécifié en regard de la résolution de nom.

## <a name="syntax"></a>Syntaxe


```JScript
DiskQuotaControl.GiveUserNameResolutionPriority(
  oUser
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*oUser* 
</dt> <dd>

Type : **Object**

Expression d’objet qui prend la valeur de l’objet [**DIDiskQuotaUser**](didiskquotauser-object.md) de l’utilisateur.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Si la résolution de noms asynchrone est activée, les objets utilisateur sont placés dans une file d’attente. Par défaut, elles sont desservies dans l’ordre dans lequel elles sont placées dans la file d’attente. La méthode **GiveUserNameResolutionPriority** déplace un objet au début de la file d’attente afin qu’il soit en ligne à traiter.

Utilisez la propriété [**UserNameResolution**](diskquotacontrol-usernameresolution.md) pour activer la résolution de noms asynchrone.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Dskquota. h</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 5,0 ou ultérieure)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet DiskQuotaControl**](diskquotacontrol-object.md)
</dt> </dl>

 

 




