---
description: Cette classe est la classe parente pour les événements d’e/s fractionnées. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: d65c5180-6f1a-45cc-bca8-eac13857d383
title: SplitIo, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SplitIo
api_type:
- NA
api_location: ''
ms.openlocfilehash: 0268c3dfa778eb8694a81f57b9212b68bd6674e6c7de6324cdc297550745b2a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069719"
---
# <a name="splitio-class"></a>SplitIo, classe

Cette classe est la classe parente pour les événements d’e/s fractionnées.

La syntaxe suivante est simplifiée à partir du code MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Guid("{d837ca92-12b9-44a5-ad6a-3a65b3578aa8}")]
class SplitIo : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Membres

La classe **SplitIo** ne définit aucun membre.

## <a name="remarks"></a>Remarques

Pour activer les événements d’e/s fractionnés dans une session de journalisation du noyau NT, spécifiez l’indicateur d' **\_ \_ \_ \_ e/s Split** de l’indicateur de suivi d’événement dans le membre **EnableFlags** d’une structure de [**\_ \_ Propriétés de trace d’événements**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) lors de l’appel de la fonction [](/windows/win32/api/evntrace/nf-evntrace-starttracea)

Les consommateurs de suivi d’événements peuvent implémenter un traitement spécial pour les événements d’e/s fractionnées en appelant la fonction [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) et en spécifiant [**SplitIoGuid**](nt-kernel-logger-constants.md) comme paramètre *pguid* . Utilisez le type d’événement suivant pour identifier l’événement réel lors de la consommation d’événements.



| Type d'événement           | Description                                                                                                |
|----------------------|------------------------------------------------------------------------------------------------------------|
| Valeur de type d’événement, 32 | Événement de fractionnement d’e/s. La classe [**SplitIo \_ info**](splitio-info.md) MOF définit les données d’événement pour cet événement. |



 

Les événements de fractionnement des e/s indiquent que les demandes d’e/s ont été fractionnées en plusieurs demandes d’e/s disque en raison du disque de mise en miroir sous-jacent.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



 

 
