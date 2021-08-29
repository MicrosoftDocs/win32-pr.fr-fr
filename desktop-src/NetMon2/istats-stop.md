---
description: 'IStats :: Stop, méthode : la méthode Stop arrête la capture en cours.'
ms.assetid: 3aeeb29e-e174-46a2-82bb-44c466b8db98
title: 'IStats :: Stop, méthode (NetMon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.Stop
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 5ba7d2d9b3506b11da6ad25e2d6484f6440e9ed92b506d325138860fc1fc5ca1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119742689"
---
# <a name="istatsstop-method"></a>IStats :: Stop, méthode

La méthode **Stop** arrête la capture en cours.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT STDMETHODCALLTYPE Stop();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Si la méthode réussit, la valeur de retour est NMERR \_ Success.

Si la méthode échoue, la valeur de retour est l’un des codes d’erreur suivants :



| Code de retour                                                                                            | Description                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ non \_ connecté**</dt> </dl>   | Le NPP n’est pas connecté au réseau. appelez la méthode [IStats :: Connecter](istats-connect.md) pour connecter le NPP au réseau.<br/> |
| <dl> <dt>**NMERR \_ pas de \_ capture**</dt> </dl>   | Le NPP ne capture pas de données. Appelez la méthode [IStats :: Start](istats-start.md) pour démarrer la capture.<br/>                            |
| <dl> <dt>**NMERR \_ non \_ stats \_ uniquement**</dt> </dl> | le NPP est connecté au réseau, mais pas avec la méthode [IStats :: Connecter](istats-connect.md) .<br/>                                |



 

## <a name="remarks"></a>Remarques

Lors du redémarrage de la capture après l’appel de **IStats :: Stop** , veillez à appeler la méthode [IStats :: configure](istats-configure.md) chaque fois que vous appelez [IStats :: Start](istats-start.md) pour redémarrer la capture.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                                                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                                                                     |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll ; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[IStats](istats.md)
</dt> <dt>

[IStats :: Connecter](istats-connect.md)
</dt> <dt>

[IStats :: configure](istats-configure.md)
</dt> <dt>

[IStats :: Start](istats-start.md)
</dt> </dl>

 

 




