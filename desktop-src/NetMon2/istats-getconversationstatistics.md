---
description: Récupère les informations de session et de station relatives à la capture en cours.
ms.assetid: 7fc436fc-b569-402d-a1ea-c1bb65de8a9e
title: 'IStats :: GetConversationStatistics, méthode (NetMon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.GetConversationStatistics
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 030fafb4ccf041c2804179f8adf0088ca3fba845
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011546"
---
# <a name="istatsgetconversationstatistics-method"></a>IStats :: GetConversationStatistics, méthode

La méthode **GetConversationStatistics** récupère les informations de session et de station relatives à la capture en cours.

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

Pointeur vers une structure [**SESSIONSTATS**](sessionstats.md) .

</dd> <dt>

*nStations* \[ à\]
</dt> <dd>

Pointeur vers une valeur DWORD qui contient le nombre de [*stations*](s.md) enregistrées pour la capture en cours.

</dd> <dt>

*lpStationStats* \[ à\]
</dt> <dd>

Pointeur vers une structure [**STATIONSTATS**](stationstats.md) .

</dd> <dt>

*fClearAfterReading* \[ dans\]
</dt> <dd>

Indicateur utilisé pour indiquer à Moniteur réseau d’effacer le stockage interne des structures [**SESSIONSTATS**](sessionstats.md) et [**STATIONSTATS**](stationstats.md) une fois que les données actuelles ont été récupérées.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si la méthode réussit, la valeur de retour est NMERR \_ Success.

Si la méthode échoue, la valeur de retour est l’un des codes d’erreur suivants :



| Code de retour                                                                                                   | Description                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ non \_ connecté**</dt> </dl>          | Le NPP n’est pas connecté au réseau. appelez [**IStats :: Connecter**](istats-connect.md) pour connecter le NPP au réseau.<br/>                                                                                                      |
| <dl> <dt>**NMERR \_ pas de \_ capture**</dt> </dl>          | Le NPP ne capture pas de données. Appelez [**IStats :: Start**](istats-start.md) pour démarrer la capture.<br/>                                                                                                                                 |
| <dl> <dt>**NMERR \_ non \_ stats \_ uniquement**</dt> </dl>        | le NPP est connecté au réseau, mais pas avec la méthode [**IStats :: Connecter**](istats-connect.md) .<br/>                                                                                                                         |
| <dl> <dt>**NMERR \_ aucune \_ statistique de conversation \_**</dt> </dl> | La configuration de cette connexion est définie de façon à ne pas enregistrer les statistiques de conversation. Pour enregistrer les statistiques de conversation, arrêtez la capture, définissez **NoConversationStats = Yes** dans l’objet blob de configuration, puis redémarrez la capture.<br/> |



 

## <a name="remarks"></a>Notes

Cette méthode peut être appelée uniquement lorsque la capture de données est en cours ; Lorsque la capture en cours est suspendue, un appel à cette méthode échoue.

Pour démarrer une capture, appelez la méthode [**IStats :: Start**](istats-start.md) . Pour récupérer d’autres types de statistiques, appelez [**IStats :: GetTotalStatistics**](istats-gettotalstatistics.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                                                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                                                                     |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll ; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IStats**](istats.md)
</dt> <dt>

[**IStats::GetTotalStatistics**](istats-gettotalstatistics.md)
</dt> <dt>

[**IStats :: Start**](istats-start.md)
</dt> <dt>

[**IStats :: Connecter**](istats-connect.md)
</dt> <dt>

[**SESSIONSTATS**](sessionstats.md)
</dt> <dt>

[**STATIONSTATS**](stationstats.md)
</dt> </dl>

 

 




