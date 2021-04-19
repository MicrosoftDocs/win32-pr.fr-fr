---
description: La méthode Stop arrête la capture en cours.
ms.assetid: 64a80ff1-5a48-4be8-835d-a3d304ebb324
title: 'IRTC :: Stop, méthode (NetMon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Stop
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: f25bf9d56a6f41acefad9a552dd2f591158bc74e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519636"
---
# <a name="irtcstop-method"></a>IRTC :: Stop, méthode

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



| Code de retour                                                                                          | Description                                                                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ non \_ connecté**</dt> </dl> | Le NPP n’est pas connecté au réseau. Appelez [IRTC :: Connect](irtc-connect.md) pour connecter le NPP au réseau.<br/> |
| <dl> <dt>**NMERR \_ pas de \_ capture**</dt> </dl> | Le NPP ne capture pas de données. Appelez [IRTC :: Start](irtc-start.md) pour démarrer la capture.<br/>                            |
| <dl> <dt>**NMERR \_ pas de \_ temps réel**</dt> </dl>  | Le NPP est connecté au réseau, mais pas avec la méthode [IRTC :: Connect](irtc-connect.md) .<br/>                     |



 

## <a name="remarks"></a>Notes

Lorsque vous redémarrez la capture après avoir appelé la méthode **IRTC :: Stop** , veillez à appeler [IRTC :: configure](irtc-configure.md) chaque fois que vous appelez [IRTC :: Start](irtc-start.md) pour redémarrer la capture.

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

[IRTC :: configure](irtc-configure.md)
</dt> <dt>

[IRTC :: Start](irtc-start.md)
</dt> </dl>

 

 




