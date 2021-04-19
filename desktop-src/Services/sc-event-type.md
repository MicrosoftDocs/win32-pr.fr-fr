---
description: Indique un type de changement d’état de service pour l’analyse et la création de rapports.
ms.assetid: 7508526c-02ce-4ac2-8616-491390a4afad
title: Énumération SC_EVENT_TYPE (Winsvcp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SC_EVENT_TYPE
api_type:
- HeaderDef
api_location:
- Winsvcp.h
ms.openlocfilehash: 55853d13844d3bb255ab0e84a50e8cbbea2d76ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106545105"
---
# <a name="sc_event_type-enumeration"></a>\_Énumération des types d’événements SC \_

Indique un type de changement d’état de service pour l’analyse et la création de rapports.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum _SC_EVENT_TYPE { 
  SC_EVENT_DATABASE_CHANGE  = 0,
  SC_EVENT_PROPERTY_CHANGE  = 1,
  SC_EVENT_STATUS_CHANGE    = 2
} SC_EVENT_TYPE, *PSC_EVENT_TYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="SC_EVENT_DATABASE_CHANGE"></span><span id="sc_event_database_change"></span>**\_ \_ modification de la base de données d’événements SC \_**
</dt> <dd>

Un service a été ajouté ou supprimé. Le paramètre *hService* de la fonction [**SubscribeServiceChangeNotifications**](subscribeservicechangenotifications.md) doit être un handle vers le SCM.

</dd> <dt>

<span id="SC_EVENT_PROPERTY_CHANGE"></span><span id="sc_event_property_change"></span>**modification de la propriété de l' \_ événement SC \_ \_**
</dt> <dd>

Une ou plusieurs propriétés de service ont été mises à jour. Le paramètre *hService* de la fonction [**SubscribeServiceChangeNotifications**](subscribeservicechangenotifications.md) doit être un handle du service.

</dd> <dt>

<span id="SC_EVENT_STATUS_CHANGE"></span><span id="sc_event_status_change"></span>**modification de l’état de l' \_ événement SC \_ \_**
</dt> <dd>

L’état d’un service a changé. Le paramètre *hService* de la fonction [**SubscribeServiceChangeNotifications**](subscribeservicechangenotifications.md) doit être un handle du service.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8<br/>                                                                 |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                       |
| En-tête<br/>                   | <dl> <dt>Winsvcp. h</dt> </dl> |



 

 




