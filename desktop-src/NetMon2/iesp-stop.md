---
description: 'IESP :: Stop, méthode : la méthode Stop arrête la capture en cours.'
ms.assetid: d2d4e51a-c6a4-4aec-a805-929af621ffb3
title: 'IESP :: Stop, méthode (NetMon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.Stop
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: ac262d8da5ab218db7300ea38da59d5c738421c0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103767"
---
# <a name="iespstop-method"></a>IESP :: Stop, méthode

La méthode **Stop** arrête la capture en cours.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT STDMETHODCALLTYPE Stop(
  [out] LPSTATISTICS lpStats
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lpStats* \[ à\]
</dt> <dd>

Pointeur vers une structure de [statistiques](statistics.md) qui contient des statistiques réseau, telles que les trames totales et le nombre total d’octets capturés.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Si la méthode réussit, la valeur de retour est NMERR \_ Success.

Si la méthode échoue, la valeur de retour est l’un des codes d’erreur suivants :



| Code de retour                                                                                          | Description                                                                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ non \_ connecté**</dt> </dl> | Le NPP n’est pas connecté au réseau. Appelez [IESP :: Connect](iesp-connect.md) pour connecter le NPP au réseau.<br/> |
| <dl> <dt>**NMERR \_ pas de \_ capture**</dt> </dl> | Le NPP ne capture pas de données. Appelez [IESP :: Start](iesp-start.md) pour démarrer la capture.<br/>                            |
| <dl> <dt>**NMERR \_ non \_ ESP**</dt> </dl>       | Le NPP est connecté au réseau, mais pas avec la méthode [IESP :: Connect](iesp-connect.md) .<br/>                     |



 

## <a name="remarks"></a>Notes 

Quand la méthode **IESP :: Stop** est appelée, moniteur réseau arrête la capture des données et ferme le [*fichier de capture.*](c.md) (Le nom du fichier de capture a été retourné lors de l’appel de [IESP :: Start](iesp-start.md) .) Vous pouvez maintenant examiner le contenu du fichier de capture.

Lorsque vous arrêtez et redémarrez la capture, veillez à appeler la méthode [IESP :: configure](iesp-configure.md) chaque fois que vous appelez [IESP :: Start](iesp-start.md) pour redémarrer la capture.

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

[IESP :: Start](iesp-start.md)
</dt> <dt>

[PORTENT](statistics.md)
</dt> </dl>

 

 




