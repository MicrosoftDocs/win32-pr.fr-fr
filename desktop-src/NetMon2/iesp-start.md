---
description: La méthode start démarre une capture.
ms.assetid: 8bf8c0c7-20be-4404-8ea5-b28b4c658523
title: 'IESP :: Start, méthode (NetMon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.Start
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 2d9fc3a75fc82964f6fc5a5660ef77414ae065d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524598"
---
# <a name="iespstart-method"></a>IESP :: Start, méthode

La méthode **Start** démarre une capture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT STDMETHODCALLTYPE Start(
  [out] char *pFileName
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pFileName* \[ à\]
</dt> <dd>

Pointeur vers le nom du [*fichier de capture*](c.md) utilisé pour stocker les données réseau. Veillez à mettre en cache ce nom de fichier s’il est nécessaire à des fins de référence ultérieure.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la méthode réussit, la valeur de retour est NMERR \_ Success.

Si la méthode échoue, la valeur de retour est l’un des codes d’erreur suivants :



| Code de retour                                                                                           | Description                                                                                                                            |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_capture NMERR \_ suspendue**</dt> </dl> | La capture est suspendue et doit être arrêtée avant de pouvoir être redémarrée. Appelez [IESP :: Stop](iesp-stop.md) pour arrêter la capture.<br/> |
| <dl> <dt>**\_capture NMERR**</dt> </dl>       | La capture a déjà démarré.<br/>                                                                                             |
| <dl> <dt>**NMERR \_ non \_ connecté**</dt> </dl>  | Le NPP n’est pas connecté au réseau. Appelez [IESP :: Connect](iesp-connect.md) pour connecter le NPP au réseau.<br/>          |
| <dl> <dt>**NMERR \_ non \_ ESP**</dt> </dl>        | Le NPP est connecté au réseau, mais pas avec la méthode [IESP :: Connect](iesp-connect.md) .<br/>                              |



 

## <a name="remarks"></a>Notes

L’emplacement du [*fichier de capture*](c.md) est spécifié dans le Registre Windows, mais vous pouvez utiliser Moniteur réseau pour modifier l’emplacement du répertoire.

Lorsque vous redémarrez la capture à l’aide des méthodes IESP :: Start et [IESP :: Stop](iesp-stop.md) , vous devez appeler la méthode [IESP :: configure](iesp-configure.md) pour reconfigurer la connexion chaque fois que vous appelez IESP :: Start pour redémarrer la capture des données. Lorsque vous démarrez et arrêtez la capture à l’aide de ces trois méthodes, un nouveau fichier de capture est créé chaque fois que la capture est démarrée.

> [!Note]  
> Vous pouvez également démarrer et arrêter la capture à l’aide des méthodes [IESP ::P ause](iesp-pause.md) et [IESP :: Resume](iesp-resume.md) . Lorsque ces deux méthodes sont utilisées, les données capturées sont stockées dans le même fichier de capture.

 

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

[IESP :: configure](iesp-configure.md)
</dt> <dt>

[IESP :: Connect](iesp-connect.md)
</dt> <dt>

[IESP ::P ause](iesp-pause.md)
</dt> <dt>

[IESP :: Resume](iesp-resume.md)
</dt> <dt>

[IESP :: Stop](iesp-stop.md)
</dt> </dl>

 

 




