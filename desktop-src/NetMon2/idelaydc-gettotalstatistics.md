---
description: 'IDelaydC :: GetTotalStatistics, méthode : la méthode GetTotalStatistics récupère les statistiques totales pour la capture actuelle.'
ms.assetid: 904c7496-5603-41b9-8481-06fa31f6f112
title: 'IDelaydC :: GetTotalStatistics, méthode (NetMon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.GetTotalStatistics
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: e6b4d76b3035e156da1f1d4decf7a5c59b28bf0ca13bc2bdaa33e319422509af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037549"
---
# <a name="idelaydcgettotalstatistics-method"></a>IDelaydC :: GetTotalStatistics, méthode

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

Indicateur utilisé pour indiquer Moniteur réseau comment gérer le stockage interne du total des statistiques. La **valeur true** indique Moniteur réseau d’effacer le stockage interne du total des statistiques une fois que les informations actuelles ont été récupérées.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la méthode réussit, la valeur de retour est NMERR \_ Success.

Si la méthode échoue, la valeur de retour est l’un des codes d’erreur suivants :



| Code de retour                                                                                          | Description                                                                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ non \_ connecté**</dt> </dl> | Le NPP n’est pas connecté au réseau. appelez [IDelaydC :: Connecter](idelaydc-connect.md) pour vous connecter au réseau.<br/> |
| <dl> <dt>**NMERR \_ non \_ retardé**</dt> </dl>   | le NPP est connecté au réseau, mais pas avec la méthode [IDelaydC :: Connecter](idelaydc-connect.md) .<br/>             |
| <dl> <dt>**NMERR \_ pas de \_ capture**</dt> </dl> | Le NPP ne capture pas de données. Appelez [IDelaydC :: Start](idelaydc-start.md) pour commencer à capturer des données.<br/>                 |



 

## <a name="remarks"></a>Remarques

Cette méthode retourne les données uniquement lorsqu’une capture est en cours ; Lorsque la capture est suspendue, les appels à cette méthode échouent.

Moniteur réseau stocke également les [*statistiques de conversation*](c.md), qui peuvent être récupérées en appelant la méthode [IDelaydC :: GetConversationStatistics](idelaydc-getconversationstatistics.md) .

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

[IDelaydC::GetConversationStatistics](idelaydc-getconversationstatistics.md)
</dt> <dt>

[IDelaydC :: Start](idelaydc-start.md)
</dt> <dt>

[PORTENT](statistics.md)
</dt> </dl>

 

 




