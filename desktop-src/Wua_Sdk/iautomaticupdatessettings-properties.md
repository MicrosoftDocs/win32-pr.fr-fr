---
description: L’interface IAutomaticUpdatesSettings définit les propriétés suivantes.
ms.assetid: 663aaf7d-c701-4da8-ba92-7e0a6d0f35ba
title: Propriétés IAutomaticUpdatesSettings
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2463fdc69fc93960ee45c0003a65894eaaf7399
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951240"
---
# <a name="iautomaticupdatessettings-properties"></a>Propriétés IAutomaticUpdatesSettings

L’interface [**IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdatessettings) définit les propriétés suivantes.



| Propriété                                                                                 | Description                                                                                      |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**NotificationLevel**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_notificationlevel)                 | Obtient et définit la manière dont les utilisateurs sont avertis des événements de mise à jour automatique.                              |
| [**Seulement**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_readonly)                                   | Obtient une valeur booléenne qui indique si les paramètres de mise à jour automatique sont en lecture seule.         |
| [**Obligatoire**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_required)                                   | Obtient une valeur booléenne qui indique si stratégie de groupe requiert le service Mises à jour automatiques. |
| [**ScheduledInstallationDay**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationday)   | Obtient et définit les jours de la semaine où Mises à jour automatiques installe ou désinstalle des mises à jour.    |
| [**ScheduledInstallationTime**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationtime) | Obtient et définit l’heure à laquelle Mises à jour automatiques installe ou désinstalle des mises à jour.                |



 

> [!Note]  
> Windows 8, Windows 8.1, Windows Server 2012 et Windows Server 2012 R2 offrent uniquement une prise en charge limitée de [**ScheduledInstallationDay**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationday) et [**ScheduledInstallationTime**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationtime). Si l’ordinateur a été configuré par le biais d’stratégie de groupe pour utiliser un jour et une heure d’installation planifiés, les propriétés **ScheduledInstallationDay** et **ScheduledInstallationTime** retournent ce jour et cette heure planifiés. Si l’ordinateur n’a pas été configuré à l’aide de la stratégie de groupe de cette manière, les propriétés **ScheduledInstallationDay** et **ScheduledInstallationTime** retournent des valeurs par défaut et non fiables. Si vous essayez de modifier le jour et l’heure d’installation planifiés sur ces systèmes d’exploitation, **ScheduledInstallationDay** et **ScheduledInstallationTime** semblent être exécutés, mais n’ont aucun effet.

 

 

 



