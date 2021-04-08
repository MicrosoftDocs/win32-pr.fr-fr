---
description: La méthode start démarre la capture.
ms.assetid: 1f676e19-18ff-4c34-a83f-2723ff356be2
title: 'IRTC :: Start, méthode (NetMon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Start
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 3ee30112baf7813c983230fb90cd15ea7f52e2bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864065"
---
# <a name="irtcstart-method"></a>IRTC :: Start, méthode

La méthode **Start** démarre la capture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT STDMETHODCALLTYPE Start();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Si la méthode réussit, la valeur de retour est NMERR \_ Success.

Si la méthode échoue, la valeur de retour est l’un des codes d’erreur suivants :



| Code de retour                                                                                           | Description                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_capture NMERR \_ suspendue**</dt> </dl> | La capture est dans un état suspendu et doit être arrêtée avant de pouvoir être redémarrée. Appelez [IRTC :: Stop](idelaydc-stop.md) pour arrêter la capture.<br/> |
| <dl> <dt>**\_capture NMERR**</dt> </dl>       | La capture a déjà démarré.<br/>                                                                                                            |
| <dl> <dt>**NMERR \_ non \_ connecté**</dt> </dl>  | Le NPP n’est pas connecté au réseau. Appelez [IRTC :: Connect](irtc-connect.md) pour connecter le NPP au réseau.<br/>                         |
| <dl> <dt>**NMERR \_ pas de \_ temps réel**</dt> </dl>   | Le NPP est connecté au réseau, mais pas avec la méthode [IRTC :: Connect](irtc-connect.md) .<br/>                                             |



 

## <a name="remarks"></a>Notes

Lorsque vous redémarrez la capture à l’aide des méthodes IRTC :: Start et [IRTC :: Stop](irtc-stop.md) , vous devez appeler la méthode [IRTC :: configure](irtc-configure.md) pour reconfigurer la connexion chaque fois que vous appelez IRTC :: Start pour redémarrer la capture de données.

> [!Note]  
> Vous pouvez également démarrer et arrêter la capture à l’aide des méthodes [IRTC ::P ause](irtc-pause.md) et [IRTC :: Resume](irtc-resume.md) .

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                                                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                                                                     |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll ; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[IRTC](irtc.md)
</dt> <dt>

[IRTC :: configure](irtc-configure.md)
</dt> <dt>

[IRTC :: Connect](irtc-connect.md)
</dt> <dt>

[IRTC ::P ause](irtc-pause.md)
</dt> <dt>

[IRTC :: Resume](irtc-resume.md)
</dt> <dt>

[IRTC :: Stop](irtc-stop.md)
</dt> </dl>

 

 




