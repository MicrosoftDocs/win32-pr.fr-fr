---
description: 'IStats :: GetTotalStatistics, méthode : la méthode GetTotalStatistics récupère les statistiques totales pour la capture actuelle.'
ms.assetid: 494634f6-a9b3-4a50-8920-2387be9ba30f
title: 'IStats :: GetTotalStatistics, méthode (NetMon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.GetTotalStatistics
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: e6566a58212e8f20d0d999302f41ab97cb9f005e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011544"
---
# <a name="istatsgettotalstatistics-method"></a>IStats :: GetTotalStatistics, méthode

La méthode **GetTotalStatistics** récupère les [*statistiques totales*](t.md) pour la [*capture*](c.md)en cours.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT STDMETHODCALLTYPE GetTotalStatistics(
  [out] LPSTATISTICS lpStats,
  [in]  BOOL         fClearAfterReading
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lpStats* \[ à\]
</dt> <dd>

Pointeur vers une structure de [statistiques](statistics.md)qui fournit le total des statistiques pour la capture. Il incombe à l’appelant d’allouer et de libérer la mémoire utilisée par la structure des **statistiques** .

</dd> <dt>

*fClearAfterReading* \[ dans\]
</dt> <dd>

Indicateur utilisé pour indiquer Moniteur réseau comment gérer le stockage interne du total des statistiques. La valeur TRUE indique Moniteur réseau d’effacer le stockage interne du total des statistiques une fois que les informations actuelles ont été récupérées.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si la méthode réussit, la valeur de retour est NMERR \_ Success.

Si la méthode échoue, la valeur de retour est l’un des codes d’erreur suivants :



| Code de retour                                                                                            | Description                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ non \_ connecté**</dt> </dl>   | Le NPP n’est pas connecté au réseau. appelez la méthode [IStats :: Connecter](istats-connect.md) pour connecter le NPP au réseau.<br/> |
| <dl> <dt>**NMERR \_ non \_ stats \_ uniquement**</dt> </dl> | le NPP est connecté au réseau, mais pas avec la méthode [IStats :: Connecter](istats-connect.md) .<br/>                                |
| <dl> <dt>**NMERR \_ pas de \_ capture**</dt> </dl>   | Le NPP ne capture pas de données. Appelez la méthode [IStats :: Start](istats-start.md) pour commencer à capturer des données.<br/>                         |



 

## <a name="remarks"></a>Notes

Cette méthode retourne les données uniquement lorsqu’une capture est en cours, y compris pendant la suspension de la capture.

Moniteur réseau stocke également les [*statistiques de conversation*](c.md), qui peuvent être récupérées en appelant la méthode [IStats :: GetConversationStatistics](istats-getconversationstatistics.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                                                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                                                                     |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll ; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[IStats](istats.md)
</dt> <dt>

[IStats :: Connecter](istats-connect.md)
</dt> <dt>

[IStats::GetConversationStatistics](istats-getconversationstatistics.md)
</dt> <dt>

[IStats :: Start,](istats-start.md)
</dt> <dt>

[PORTENT](statistics.md)
</dt> </dl>

 

 




