---
description: IRTC ::P méthode ause-la méthode pause interrompt la capture en cours.
ms.assetid: 8c7b310e-de04-4bd8-9c96-3c5948e610be
title: IRTC ::P méthode ause (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Pause
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 1ad7ce342c1e0053622bfb77161ecd1e5d81c25d09af179108065b445dd4dc35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118365074"
---
# <a name="irtcpause-method"></a>IRTC ::P méthode ause

La méthode **Pause** interrompt la capture en cours.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT STDMETHODCALLTYPE Pause();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Si la méthode réussit, la valeur de retour est NMERR \_ Success.

Si la méthode échoue, la valeur de retour est l’un des codes d’erreur suivants :



| Code de retour                                                                                           | Description                                                                                                                   |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_capture NMERR \_ suspendue**</dt> </dl> | La capture est déjà suspendue.<br/>                                                                                     |
| <dl> <dt>**NMERR \_ pas de \_ capture**</dt> </dl>  | Le NPP ne capture pas de données. Appelez [IRTC :: Start](irtc-start.md) pour démarrer la capture.<br/>                            |
| <dl> <dt>**NMERR \_ non \_ connecté**</dt> </dl>  | Le NPP n’est pas connecté au réseau. appelez [IRTC :: Connecter](irtc-connect.md) pour connecter le NPP au réseau.<br/> |
| <dl> <dt>**NMERR \_ pas de \_ temps réel**</dt> </dl>   | le NPP est connecté au réseau, mais pas avec la méthode [IRTC :: Connecter](irtc-connect.md) .<br/>                     |



 

## <a name="remarks"></a>Remarques

Lorsque la capture est dans un état suspendu, les nouveaux frames ne sont pas capturés jusqu’à ce que la méthode [IRTC :: Resume](irtc-resume.md) soit appelée pour redémarrer la capture.

Lorsque vous utilisez les méthodes **IRTC ::P ause** et **IRTC :: Resume** pour contrôler la capture, moniteur réseau continue à ajouter des [*statistiques de conversation*](c.md) chaque fois que la capture est en cours d’exécution.

Pour redémarrer l’appel de capture [IRTC :: Resume](irtc-resume.md). Pour arrêter la capture, appelez [IRTC :: Stop](irtc-stop.md).

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

[IRTC :: Connecter](irtc-connect.md)
</dt> <dt>

[IRTC :: Resume](irtc-resume.md)
</dt> <dt>

[IRTC :: Start](irtc-start.md)
</dt> <dt>

[IRTC :: Stop](irtc-stop.md)
</dt> </dl>

 

 




