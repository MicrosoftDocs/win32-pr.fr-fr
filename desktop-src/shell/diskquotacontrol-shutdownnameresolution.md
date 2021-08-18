---
description: Arrête le thread de résolution de nom d’utilisateur.
ms.assetid: 6c4544b9-81e7-4a72-aa00-70011e5cd85a
title: Méthode DiskQuotaControl. ShutdownNameResolution (dskquota. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.ShutdownNameResolution
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: da02f79ea8f7b582056e9c3c7c0c3f1db53fa9e08181559c99dd983924861c78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118459836"
---
# <a name="diskquotacontrolshutdownnameresolution-method"></a>Méthode DiskQuotaControl. ShutdownNameResolution

Arrête le thread de résolution de nom d’utilisateur.

## <a name="syntax"></a>Syntaxe


```JScript
DiskQuotaControl.ShutdownNameResolution()
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Le programme de résolution de noms de l’identificateur de sécurité (SID) traduit le SID en noms d’utilisateur sur un thread d’arrière-plan. Ce thread s’arrête automatiquement lorsque l’objet de contrôle de quota associé est détruit. Toutefois, dans certains cas, le thread n’est plus nécessaire, mais l’objet n’est pas encore prêt à être détruit. Un exemple typique est quand aucun traitement supplémentaire n’a lieu, mais les clients comportent toujours des références à l’objet. La méthode **ShutdownNameResolution** vous permet de terminer le thread de résolution et de libérer les ressources associées sans détruire l’objet de contrôle de quota.

> [!Note]  
> Lorsque vous arrêtez le thread de résolution, la résolution de noms asynchrone s’arrête immédiatement. Si des appels sont effectués par la suite sur des méthodes telles que [**adduser**](diskquotacontrol-adduser.md) ou [**FindUser**](diskquotacontrol-finduser.md), l’objet quota peut recréer le thread de résolution.

 

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

 

 




