---
description: 'IStats :: Start, méthode-la méthode start démarre une capture.'
ms.assetid: d4086e30-e5ed-4f29-90f0-d65125d9af6d
title: 'IStats :: Start, méthode (NetMon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.Start
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 64f02529ba10d98092eb30a1bcc350d5c72049fc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011535"
---
# <a name="istatsstart-method"></a>IStats :: Start, méthode

La méthode **Start** démarre une capture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT STDMETHODCALLTYPE Start();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Si la méthode réussit, la valeur de retour est NMERR \_ Success.

Si la méthode échoue, la valeur de retour est l’un des codes d’erreur suivants :



| Code de retour                                                                                            | Description                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_capture NMERR \_ suspendue**</dt> </dl>  | La capture a été suspendue et doit être arrêtée avant de pouvoir être redémarrée. Appelez la méthode [IStats :: Stop](istats-stop.md) pour arrêter la capture.<br/> |
| <dl> <dt>**\_capture NMERR**</dt> </dl>        | La capture a déjà démarré.<br/>                                                                                                            |
| <dl> <dt>**NMERR \_ non \_ connecté**</dt> </dl>   | Le NPP n’est pas connecté au réseau. appelez la méthode [IStats :: Connecter](istats-connect.md) pour connecter le NPP au réseau.<br/>           |
| <dl> <dt>**NMERR \_ non \_ stats \_ uniquement**</dt> </dl> | le NPP est connecté au réseau, mais pas avec la méthode [IStats :: Connecter](istats-connect.md) .<br/>                                          |



 

## <a name="remarks"></a>Notes

Lors du redémarrage de la capture à l’aide des méthodes IStats :: Start et [IStats :: Stop](istats-stop.md) , vous devez appeler la méthode [IStats :: configure](istats-configure.md) pour reconfigurer la connexion chaque fois que vous appelez IStats :: Start pour redémarrer la capture de données.

> [!Note]  
> Vous pouvez également démarrer et arrêter la capture à l’aide des méthodes [IStats ::P ause](istats-pause.md) et [IStats :: Resume](istats-resume.md) . Lorsque vous utilisez ces méthodes, les données capturées sont stockées dans le même fichier de capture.

 

## <a name="requirements"></a>Spécifications



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

[IStats :: configure](istats-configure.md)
</dt> <dt>

[IStats :: Connecter](istats-connect.md)
</dt> <dt>

[IStats ::P ause](istats-pause.md)
</dt> <dt>

[IStats :: Resume](istats-resume.md)
</dt> <dt>

[IStats :: Stop](istats-stop.md)
</dt> </dl>

 

 




