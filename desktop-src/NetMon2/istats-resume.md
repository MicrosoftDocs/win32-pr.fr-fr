---
description: La méthode Resume redémarre une capture suspendue.
ms.assetid: 128e38c4-7459-4376-a3d7-2c6944fcf535
title: 'IStats :: Resume, méthode (NetMon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.Resume
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: db84f51d2a2a2c2d15e3b4164fe1fac09e72bf20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867021"
---
# <a name="istatsresume-method"></a>IStats :: Resume, méthode

La méthode **Resume** redémarre une capture suspendue.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT STDMETHODCALLTYPE Resume();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Si la méthode réussit, la valeur de retour est NMERR \_ Success.

Si la méthode échoue, la valeur de retour est l’un des codes d’erreur suivants :



| Code de retour                                                                                                | Description                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ non \_ connecté**</dt> </dl>       | Le NPP n’est pas connecté au réseau.<br/>                                                                                          |
| <dl> <dt>**\_capture NMERR \_ non \_ suspendue**</dt> </dl> | La capture n’est pas suspendue. Appelez la méthode [IStats ::P ause](istats-pause.md) pour arrêter temporairement la capture.<br/>                     |
| <dl> <dt>**NMERR \_ non \_ connecté**</dt> </dl>       | Le NPP n’est pas connecté au réseau. Appelez la méthode [IStats :: Connect](istats-connect.md) pour connecter le NPP au réseau.<br/> |
| <dl> <dt>**NMERR \_ non \_ stats \_ uniquement**</dt> </dl>     | Le NPP est connecté au réseau, mais pas avec la méthode [IStats :: Connect](istats-connect.md) .<br/>                                |



 

## <a name="remarks"></a>Notes

Lorsque la capture est dans un état suspendu, les nouvelles données ne sont pas capturées tant que la méthode IStats :: Resume n’est pas appelée pour redémarrer la capture.

Lorsque vous utilisez les méthodes **Pause** et **Resume** pour contrôler la capture, moniteur réseau continue à ajouter des [*statistiques de conversation*](c.md) aux statistiques existantes pour la capture en cours.

Pour arrêter la capture, appelez [IStats :: Stop](istats-stop.md).

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

[IStats ::P ause](istats-pause.md)
</dt> <dt>

[IStats :: Stop](istats-stop.md)
</dt> </dl>

 

 




