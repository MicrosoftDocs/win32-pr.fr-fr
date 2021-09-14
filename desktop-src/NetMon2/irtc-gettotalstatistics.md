---
description: 'IRTC :: GetTotalStatistics, méthode : la méthode GetTotalStatistics récupère les statistiques totales pour la capture actuelle.'
ms.assetid: e5098984-c69e-4cd5-9143-d85dfcbd7b92
title: 'IRTC :: GetTotalStatistics, méthode (NetMon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.GetTotalStatistics
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 8ed659efe388f4eb9c9ac8afd6aa2c74fd0af7d3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127233634"
---
# <a name="irtcgettotalstatistics-method"></a>IRTC :: GetTotalStatistics, méthode

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

Pointeur vers une structure de [statistiques](statistics.md) qui fournit le total des statistiques pour la capture. Il incombe aux appelants d’allouer et de libérer la mémoire utilisée par la structure des **statistiques** .

</dd> <dt>

*fClearAfterReading* \[ dans\]
</dt> <dd>

Indicateur utilisé pour indiquer Moniteur réseau comment gérer le stockage interne du total des statistiques. La **valeur true** indique Moniteur réseau d’effacer le stockage interne du total des statistiques une fois que les informations actuelles ont été récupérées.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si la méthode réussit, la valeur de retour est NMERR \_ Success.

Si la méthode échoue, la valeur de retour est l’un des codes d’erreur suivants :



| Code de retour                                                                                          | Description                                                                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ non \_ connecté**</dt> </dl> | Le NPP n’est pas connecté au réseau. appelez [IRTC :: Connecter](irtc-connect.md) pour connecter le NPP au réseau.<br/> |
| <dl> <dt>**NMERR \_ pas de \_ temps réel**</dt> </dl>  | le NPP est connecté au réseau, mais pas avec la méthode [IRTC :: Connecter](irtc-connect.md) .<br/>                     |
| <dl> <dt>**NMERR \_ pas de \_ capture**</dt> </dl> | Le NPP ne capture pas de données. Appelez [IRTC :: Start](irtc-start.md) pour commencer à capturer des données.<br/>                         |



 

## <a name="remarks"></a>Notes

Cette méthode retourne les données uniquement lorsqu’une capture est en cours, y compris pendant la suspension de la capture.

Moniteur réseau stocke également les [*statistiques de conversation*](c.md). Pour récupérer des statistiques de conversation, appelez la méthode [IRTC :: GetConversationStatistics](irtc-getconversationstatistics.md) .

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

[IRTC::GetConversationStatistics](irtc-getconversationstatistics.md)
</dt> <dt>

[IRTC :: Start](irtc-start.md)
</dt> <dt>

[PORTENT](statistics.md)
</dt> </dl>

 

 




