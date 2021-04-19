---
description: La méthode Resume redémarre une capture suspendue.
ms.assetid: 047ea5f8-de3d-40db-ada3-fc0ef4deccef
title: 'IESP :: Resume, méthode (NetMon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.Resume
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 01bbb748fc91bcc5a78b281ec9ebdd2a6d479888
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106536109"
---
# <a name="iespresume-method"></a>IESP :: Resume, méthode

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



| Code de retour                                                                                                | Description                                                                                                               |
|------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_capture NMERR \_ non \_ suspendue**</dt> </dl> | La capture n’est pas suspendue. Appelez [**IESP ::P ause**](iesp-pause.md) pour suspendre la capture.<br/>                        |
| <dl> <dt>**NMERR \_ non \_ connecté**</dt> </dl>       | Le NPP n’est pas connecté au réseau. Appelez [**IESP :: Connect**](iesp-connect.md) pour vous connecter au réseau.<br/> |
| <dl> <dt>**NMERR \_ non \_ ESP**</dt> </dl>             | Le NPP est connecté au réseau, mais pas avec la méthode [**IESP :: Connect**](iesp-connect.md) .<br/>            |



 

## <a name="remarks"></a>Notes

Lorsque la capture est dans un état suspendu, les nouvelles données ne sont pas ajoutées au [*fichier de capture*](c.md) actuel tant que **IESP :: Resume** n’est pas appelé pour redémarrer la capture. Lorsque l' **interruption** et la **reprise** sont utilisées pour arrêter et redémarrer la capture, toutes les informations capturées sont placées dans le même fichier de capture.

Lorsque vous utilisez **suspendre** et **reprendre** pour contrôler la capture, moniteur réseau continue à ajouter des [*statistiques de conversation*](c.md) aux statistiques existantes pour la capture actuelle.

Pour arrêter la capture, appelez [**IESP :: Stop**](iesp-stop.md).

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

[**IESP :: Connect**](iesp-connect.md)
</dt> <dt>

[**IESP ::P ause**](iesp-pause.md)
</dt> <dt>

[**IESP :: Stop**](iesp-stop.md)
</dt> </dl>

 

 




