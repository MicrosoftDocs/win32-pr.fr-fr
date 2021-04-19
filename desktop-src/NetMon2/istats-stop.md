---
description: La méthode Stop arrête la capture en cours.
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
ms.openlocfilehash: 7b7b58527e7bde0c3bbdec4fc162b705dd178c10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518548"
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
| <dl> <dt>**NMERR \_ non \_ connecté**</dt> </dl>   | Le NPP n’est pas connecté au réseau. Appelez la méthode [IStats :: Connect](istats-connect.md) pour connecter le NPP au réseau.<br/> |
| <dl> <dt>**NMERR \_ pas de \_ capture**</dt> </dl>   | Le NPP ne capture pas de données. Appelez la méthode [IStats :: Start](istats-start.md) pour démarrer la capture.<br/>                            |
| <dl> <dt>**NMERR \_ non \_ stats \_ uniquement**</dt> </dl> | Le NPP est connecté au réseau, mais pas avec la méthode [IStats :: Connect](istats-connect.md) .<br/>                                |



 

## <a name="remarks"></a>Notes

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

[IStats :: Connect](istats-connect.md)
</dt> <dt>

[IStats :: configure](istats-configure.md)
</dt> <dt>

[IStats :: Start](istats-start.md)
</dt> </dl>

 

 




