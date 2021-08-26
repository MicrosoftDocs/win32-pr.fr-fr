---
description: les analyses sont conçues pour utiliser les Windows Management Instrumentation (WMI) pour déclencher des événements sur des ordinateurs locaux ou distants.
ms.assetid: b20746dd-d8d9-49b6-95b7-5151ee02901d
title: Surveiller les événements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ebe76ddd8df02694f871899e0b172dda3529fc29c0e16b6b4a65e2ad15bd2ed
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119995479"
---
# <a name="monitor-events"></a>Surveiller les événements

les analyses sont conçues pour utiliser les [Windows Management Instrumentation](/windows/desktop/WmiSdk/wmi-start-page) (WMI) pour déclencher des événements sur des ordinateurs locaux ou distants.

> [!Note]  
> Étant donné que les analyses utilisent une capture en temps réel, elles peuvent uniquement capturer des données sur l’ordinateur local. Il s’agit d’une limitation de l’interface **IRTC** du fournisseur de paquets réseau. Toutefois, à l’aide d’événements WMI, les données capturées peuvent être examinées localement, tandis que les événements peuvent être envoyés à des ordinateurs locaux ou distants.

 

Les analyses ne communiquent pas directement avec WMI. Le [*service de contrôle d’analyse*](m.md) (MCSVC) fournit une interface (appelée [IMonitorEventer](imonitoreventer.md)), que l’analyse peut utiliser pour obtenir une structure de données d’événement et la remplir avec les informations pertinentes. Le MCSVC peut ensuite envoyer la structure des données d’événement à WMI, qui à son tour déclenche l’événement.

 

 
