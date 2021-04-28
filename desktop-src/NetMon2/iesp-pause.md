---
description: IESP ::P méthode ause-la méthode pause interrompt la capture en cours.
ms.assetid: efbc8947-b9fe-4dbd-8097-375b5f99845e
title: IESP ::P méthode ause (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.Pause
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 486c7aedc7092e0dd0f9f68cc1ea2ccad08d9438
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084237"
---
# <a name="iesppause-method"></a>IESP ::P méthode ause

La méthode **Pause** interrompt la capture en cours.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT STDMETHODCALLTYPE Pause(
   LPSTATISTICS lpStats
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lpStats* 
</dt> <dd>

Obsolète.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Si la méthode réussit, la valeur de retour est NMERR \_ Success.

Si la méthode échoue, la valeur de retour est l’un des codes d’erreur suivants :



| Code de retour                                                                                           | Description                                                                                                                   |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_capture NMERR \_ suspendue**</dt> </dl> | La capture est déjà suspendue.<br/>                                                                                     |
| <dl> <dt>**NMERR \_ pas de \_ capture**</dt> </dl>  | Le NPP ne capture pas de données. Appelez [IESP :: Start](iesp-start.md) pour démarrer la capture.<br/>                            |
| <dl> <dt>**NMERR \_ non \_ connecté**</dt> </dl>  | Le NPP n’est pas connecté au réseau. Appelez [IESP :: Connect](iesp-connect.md) pour connecter le NPP au réseau.<br/> |
| <dl> <dt>**NMERR \_ non \_ ESP**</dt> </dl>        | Le NPP est connecté au réseau, mais pas avec la méthode [IESP :: Connect](iesp-connect.md) .<br/>                     |



 

## <a name="remarks"></a>Notes 

Lorsque la capture est dans un état suspendu, les nouvelles données ne sont pas ajoutées au [*fichier de capture*](c.md) actuel tant que vous n’avez pas appelé la méthode [IESP :: Resume](iesp-resume.md) pour redémarrer la capture. Lorsque l' **interruption** et la **reprise** sont utilisées pour arrêter et redémarrer la capture, toutes les informations capturées sont placées dans le même fichier de capture.

Lorsque vous utilisez les méthodes **IESP ::P ause** et **IESP :: Resume** pour contrôler la capture, moniteur réseau continue à ajouter des [*statistiques de conversation*](c.md) chaque fois que la capture est en cours d’exécution.

Pour redémarrer la capture, appelez [IESP :: Resume](iesp-resume.md). Pour arrêter la capture, appelez [IESP :: Stop](iesp-stop.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                                                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                                                                     |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll ; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[IESP](iesp.md)
</dt> <dt>

[IESP :: Connect](iesp-connect.md)
</dt> <dt>

[IESP :: Resume](iesp-resume.md)
</dt> <dt>

[IESP :: Start](iesp-start.md)
</dt> <dt>

[IESP :: Stop](iesp-stop.md)
</dt> </dl>

 

 




