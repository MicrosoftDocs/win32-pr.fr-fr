---
description: 'IDelaydC :: GetConversationStatistics, méthode : la méthode GetConversationStatistics récupère les informations de session et de station relatives à la capture en cours.'
ms.assetid: 0164fa0e-90f2-4b97-be9d-55d172f8112d
title: 'IDelaydC :: GetConversationStatistics, méthode (NetMon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.GetConversationStatistics
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 60fc768a1b93a752a91d431e79fb3e875416ac2b82b2bad5603e3d4cddaccbaf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910569"
---
# <a name="idelaydcgetconversationstatistics-method"></a>IDelaydC :: GetConversationStatistics, méthode

La méthode **GetConversationStatistics** récupère les informations de [*session*](s.md) et de [*station*](s.md) relatives à la capture en cours.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT STDMETHODCALLTYPE GetConversationStatistics(
  [out] DWORD          *nSessions,
  [out] LPSESSIONSTATS lpSessionStats,
  [out] DWORD          *nStations,
  [out] LPSTATIONSTATS lpStationStats,
  [in]  BOOL           fClearAfterReading
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*nSessions* \[ à\]
</dt> <dd>

Pointeur vers une valeur DWORD qui contient le nombre de [*sessions*](s.md) enregistrées pour la capture en cours.

</dd> <dt>

*lpSessionStats* \[ à\]
</dt> <dd>

Pointeur vers une structure [SESSIONSTATS](sessionstats.md) .

</dd> <dt>

*nStations* \[ à\]
</dt> <dd>

Pointeur vers une valeur DWORD qui contient le nombre de [*stations*](s.md) enregistrées pour la capture en cours.

</dd> <dt>

*lpStationStats* \[ à\]
</dt> <dd>

Pointeur vers une structure [STATIONSTATS](stationstats.md) .

</dd> <dt>

*fClearAfterReading* \[ dans\]
</dt> <dd>

Indicateur utilisé pour indiquer à Moniteur réseau d’effacer le stockage interne des structures [SESSIONSTATS](sessionstats.md) et [STATIONSTATS](stationstats.md) après avoir récupéré les informations actuelles.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la méthode réussit, la valeur de retour est NMERR \_ Success.

Si la méthode échoue, la valeur de retour est l’un des codes d’erreur suivants :



| Code de retour                                                                                                   | Description                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ non \_ connecté**</dt> </dl>          | Le NPP n’est pas connecté au réseau. appelez [IDelaydC :: Connecter](idelaydc-connect.md) pour connecter le NPP au réseau.<br/>                                                                                                  |
| <dl> <dt>**NMERR \_ pas de \_ capture**</dt> </dl>          | Le NPP ne capture pas de données. Appelez [IDelaydC :: Start](idelaydc-start.md) pour démarrer la capture.<br/>                                                                                                                             |
| <dl> <dt>**NMERR \_ non \_ retardé**</dt> </dl>            | le NPP est connecté au réseau, mais pas avec la méthode [IDelaydC :: Connecter](idelaydc-connect.md) .<br/>                                                                                                                      |
| <dl> <dt>**NMERR \_ aucune \_ statistique de conversation \_**</dt> </dl> | La configuration de cette connexion est définie de façon à ne pas enregistrer les statistiques de conversation. Pour enregistrer les statistiques de conversation, arrêtez la capture, définissez NoConversationStats = YES dans l’objet BLOB de configuration, puis redémarrez la capture.<br/> |



 

## <a name="remarks"></a>Remarques

Cette méthode ne peut être appelée que lorsque la capture de données est en cours ; Lorsque la capture en cours est suspendue, les appels à cette méthode échouent. Pour démarrer une capture, appelez la méthode [IDelaydC :: Start](idelaydc-start.md) .

Pour récupérer d’autres types de statistiques, appelez [IDelaydC :: GetTotalStatistics](idelaydc-gettotalstatistics.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                                                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                                                                     |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll ; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[IDelaydC](idelaydc.md)
</dt> <dt>

[IDelaydC :: Connecter](idelaydc-connect.md)
</dt> <dt>

[IDelaydC::GetTotalStatistics](idelaydc-gettotalstatistics.md)
</dt> <dt>

[IDelaydC :: Start](idelaydc-start.md)
</dt> <dt>

[SESSIONSTATS](sessionstats.md)
</dt> <dt>

[STATIONSTATS](stationstats.md)
</dt> </dl>

 

 




