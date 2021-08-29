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
ms.openlocfilehash: eb5dc2939ea0fbc2c8037dc22c5b690e93a5727ecad6b2249e99e4c337340710
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119943099"
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

## <a name="remarks"></a>Remarques

Si la résolution de noms asynchrone est activée, les objets utilisateur sont placés dans une file d’attente. Par défaut, elles sont desservies dans l’ordre dans lequel elles sont placées dans la file d’attente. La méthode **GiveUserNameResolutionPriority** déplace un objet au début de la file d’attente afin qu’il soit en ligne à traiter.

Utilisez la propriété [**UserNameResolution**](diskquotacontrol-usernameresolution.md) pour activer la résolution de noms asynchrone.

## <a name="requirements"></a>Configuration requise



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

 

 




