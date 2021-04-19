---
description: La méthode Resume redémarre une capture suspendue.
ms.assetid: 685dfdee-3bd0-44b3-ac4f-c9960cf77c5c
title: 'IRTC :: Resume, méthode (NetMon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Resume
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 991f70944b44ce13641318219788d9d6122b15c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106525000"
---
# <a name="irtcresume-method"></a>IRTC :: Resume, méthode

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



| Code de retour                                                                                                | Description                                                                                                                   |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_capture NMERR \_ non \_ suspendue**</dt> </dl> | La capture n’est pas suspendue. Appelez [IRTC ::P ause](irtc-pause.md) pour suspendre la capture.<br/>                                |
| <dl> <dt>**NMERR \_ non \_ connecté**</dt> </dl>       | Le NPP n’est pas connecté au réseau. Appelez [IRTC :: Connect](irtc-connect.md) pour connecter le NPP au réseau.<br/> |
| <dl> <dt>**NMERR \_ pas de \_ temps réel**</dt> </dl>        | Le NPP est connecté au réseau, mais pas avec la méthode [IRTC :: Connect](irtc-connect.md) .<br/>                     |



 

## <a name="remarks"></a>Notes

Lorsque la capture est dans un état suspendu, les nouvelles données ne sont pas capturées tant qu’un appel à la méthode [IRTC :: Resume](idelaydc-resume.md) n’a pas redémarré la capture.

Lorsque vous utilisez les méthodes **Pause** et **Resume** pour contrôler la capture, moniteur réseau continue à ajouter des [*statistiques de conversation*](c.md) aux statistiques existantes pour la capture en cours.

Pour arrêter la capture, appelez la méthode [IRTC :: Stop](irtc-stop.md) .

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

[IRTC :: Connect](irtc-connect.md)
</dt> <dt>

[IRTC ::P ause](irtc-pause.md)
</dt> <dt>

[IRTC :: Stop](irtc-stop.md)
</dt> </dl>

 

 




