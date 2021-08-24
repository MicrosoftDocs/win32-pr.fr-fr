---
description: Les \_ constantes d’indicateur de bit LINEDEVSTATUSFLAGS décrivent une collection d’éléments de l’état du périphérique de ligne booléenne.
ms.assetid: 5fa754d3-07b2-4b75-91ef-1bf961d9fef4
title: Constantes LINEDEVSTATUSFLAGS_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6649dc39c787be7c0b7f027637f12ff7f5d028add09b9f7d568149c6e9f76c97
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119682006"
---
# <a name="linedevstatusflags_-constants"></a>\_Constantes LINEDEVSTATUSFLAGS

Les constantes d’indicateur de bit **LINEDEVSTATUSFLAGS \_** décrivent une collection d’éléments de l’état du périphérique de ligne booléenne.

<dl> <dt>

<span id="LINEDEVSTATUSFLAGS_CONNECTED"></span><span id="linedevstatusflags_connected"></span>**LINEDEVSTATUSFLAGS \_ connecté**
</dt> <dd> <dl> <dt>



Spécifie si la ligne est connectée à l’interface TAPI. Si la **valeur est true**, la ligne est connectée et l’interface TAPI peut fonctionner sur le périphérique de ligne. Si la **valeur est false**, la ligne est déconnectée et l’application ne peut pas contrôler l’appareil de ligne via TAPI.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATUSFLAGS_INSERVICE"></span><span id="linedevstatusflags_inservice"></span>**InService LINEDEVSTATUSFLAGS \_**
</dt> <dd> <dl> <dt>



Indique si la ligne est en service. Si la **valeur est true**, la ligne est en service ; Si la **valeur est false**, la ligne est hors service.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATUSFLAGS_LOCKED"></span><span id="linedevstatusflags_locked"></span>**LINEDEVSTATUSFLAGS \_ verrouillé**
</dt> <dd> <dl> <dt>



Indique si la ligne est verrouillée ou déverrouillée. Ce bit est le plus souvent utilisé avec des appareils de ligne associés à des téléphones cellulaires. De nombreux téléphones cellulaires disposent d’un mécanisme de sécurité qui nécessite l’entrée d’un mot de passe pour permettre au téléphone de passer des appels. Ce bit peut être utilisé pour indiquer aux applications que le téléphone est verrouillé et ne peut pas effectuer d’appels jusqu’à ce que le mot de passe soit entré sur l’interface utilisateur du téléphone afin que l’application puisse présenter une alerte appropriée à l’utilisateur.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATUSFLAGS_MSGWAIT"></span><span id="linedevstatusflags_msgwait"></span>**LINEDEVSTATUSFLAGS \_ MSGWAIT**
</dt> <dd> <dl> <dt>



Indique si la ligne a un message en attente. Si la **valeur est true**, un message est en attente ; Si la **valeur est false**, aucun message n’est en attente.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Remarques

Aucune extensibilité. Tous les 32 bits sont réservés.

\_Les constantes LINEDEVSTATUSFLAGS sont utilisées dans le membre **dwDevStatusFlags** de la structure de données [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,0 ou une version ultérieure<br/>                                             |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




