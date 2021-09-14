---
description: 'IRTC :: GetConversationStatistics, méthode : la méthode GetConversationStatistics récupère les informations de session et de station relatives à la capture en cours.'
ms.assetid: 27f364cd-fee9-4262-b181-c5f15fb12e51
title: 'IRTC :: GetConversationStatistics, méthode (NetMon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.GetConversationStatistics
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 4d2476f4eb33d7e74d0de8363fa88d5e688a2e73
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127110370"
---
# <a name="irtcgetconversationstatistics-method"></a>IRTC :: GetConversationStatistics, méthode

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

## <a name="return-value"></a>Valeur de retour

Si la méthode réussit, la valeur de retour est NMERR \_ Success.

Si la méthode échoue, la valeur de retour est l’un des codes d’erreur suivants :



| Code de retour                                                                                                   | Description                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ non \_ connecté**</dt> </dl>          | Le NPP n’est pas connecté au réseau. appelez [IRTC :: Connecter](irtc-connect.md) pour connecter le NPP au réseau.<br/>                                                                                                      |
| <dl> <dt>**NMERR \_ pas de \_ capture**</dt> </dl>          | Le NPP ne capture pas de données. Appelez [IRTC :: Start](irtc-start.md) pour démarrer la capture.<br/>                                                                                                                                 |
| <dl> <dt>**NMERR \_ pas de \_ temps réel**</dt> </dl>           | le NPP est connecté au réseau, mais pas avec la méthode [IRTC :: Connecter](irtc-connect.md) .<br/>                                                                                                                          |
| <dl> <dt>**NMERR \_ aucune \_ statistique de conversation \_**</dt> </dl> | La configuration de cette connexion est définie de façon à ne pas enregistrer les statistiques de conversation. Pour enregistrer les statistiques de conversation, arrêtez la capture, définissez NoConversationStats = YES dans l’objet BLOB de configuration, puis redémarrez la capture.<br/> |



 

## <a name="remarks"></a>Notes

Cette méthode peut uniquement être appelée pendant que vous capturez des données ; Si vous appelez cette méthode alors que la capture en cours est suspendue, la méthode échoue. Pour démarrer une capture, appelez la méthode [IRTC :: Start](irtc-start.md) .

Pour récupérer d’autres types de statistiques, appelez la méthode [IRTC :: GetTotalStatistics](irtc-gettotalstatistics.md) .

## <a name="requirements"></a>Spécifications



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

[IRTC::GetTotalStatistics](irtc-gettotalstatistics.md)
</dt> <dt>

[IRTC :: Start](irtc-start.md)
</dt> <dt>

[SESSIONSTATS](sessionstats.md)
</dt> <dt>

[STATIONSTATS](stationstats.md)
</dt> </dl>

 

 




