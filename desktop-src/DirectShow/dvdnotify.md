---
description: L’événement DVDNotify avertit une application de nombreux événements DVD et instructions sur le disque.
ms.assetid: 8e7d85fb-95c0-472d-ab17-a82da303b68f
title: DVDNotify (segment. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 988deaf53fb2b50555b4cf19a38684610aa0822a270dfba079defab92ce8aec0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119148702"
---
# <a name="dvdnotify"></a>DVDNotify

> [!Note]  
> ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

L' `DVDNotify` événement avertit une application de nombreux événements DVD et instructions sur le disque.

``` syntax
DVDNotify(EventCode, Param1, Param2)
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="EventCode"></span><span id="eventcode"></span><span id="EVENTCODE"></span>*EventCode*
</dt> <dd>

Spécifie le code de notification d’événement DVD.

</dd> <dt>

<span id="Param1"></span><span id="param1"></span><span id="PARAM1"></span>*Param1*
</dt> <dd>

Peut contenir des informations supplémentaires relatives à l’événement.

</dd> <dt>

<span id="Param2"></span><span id="param2"></span><span id="PARAM2"></span>*Param2*
</dt> <dd>

Peut contenir des informations supplémentaires relatives à l’événement.

</dd> </dl>

## <a name="remarks"></a>Remarques

Les [codes de notification d’événement DVD](dvd-notification-codes.md) donnent une explication complète de tous les codes de notification d’événements DVD et de leurs paramètres.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|--------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Segment. h</dt> </dl> |



 

 




