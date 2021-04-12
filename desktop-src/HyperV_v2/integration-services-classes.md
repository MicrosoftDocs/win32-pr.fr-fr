---
description: Les services d’intégration sont des services logiciels qui s’exécutent sur le système d’exploitation invité à l’intérieur d’une machine virtuelle enfant et dans le cadre de la pile de virtualisation dans le système d’exploitation de gestion pour fournir un certain niveau d’intégration au système d’exploitation de gestion.
ms.assetid: 7A8E9EF2-AC67-47CB-81A5-BF4C8A55D710
title: Classes Integration Services
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04d60a913159c49387848b5e18a3e37b942f3e7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528203"
---
# <a name="integration-services-classes"></a>Classes Integration Services

Les services d’intégration sont des services logiciels qui s’exécutent sur le système d’exploitation invité à l’intérieur d’une machine virtuelle enfant et dans le cadre de la pile de virtualisation dans le système d’exploitation de gestion pour fournir un certain niveau d’intégration au système d’exploitation de gestion. Ils sont utilisés pour résoudre les problèmes qui surviennent au niveau élevé d’isolation fourni par les machines virtuelles.

Les classes WMI de virtualisation associées aux services d’intégration sont les suivantes.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                                                | Description                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MSVM \_ CopyFileToGuestJob**](msvm-copyfiletoguestjob.md)<br/>                                               | Représente un travail d’opération de service de fichiers invité. <br/>                                                                                                                                                                                                            |
| [**MSVM \_ CopyFileToGuestSettingData**](msvm-copyfiletoguestsettingdata.md)<br/>                               | Représente les paramètres de copie d’un fichier à partir de l’hôte dans l’invité. <br/>                                                                                                                                                                                |
| [**MSVM \_ GuestFileService**](msvm-guestfileservice.md)<br/>                                                   | [**MSVM \_ GuestFileService**](msvm-guestfileservice.md) contient une méthode qui peut être utilisée pour copier un fichier sur un ordinateur virtuel à partir de l’hôte Hyper-V. <br/>                                                                                                     |
| [**MSVM \_ GuestService**](msvm-guestservice.md)<br/>                                                           | [**MSVM \_ GuestService**](msvm-guestservice.md) est la classe de base abstraite pour les services de l’invité qui sont accessibles à partir de l’hôte. <br/>                                                                                                                  |
| [**MSVM \_ GuestServiceInterfaceComponent**](msvm-guestserviceinterfacecomponent.md)<br/>                       | Représente l’état du composant d’interface de service invité, qui fournit un mécanisme permettant d’interagir avec l’ordinateur virtuel à partir des interfaces de gestion sur le système hôte. <br/>                                                                         |
| [**MSVM \_ GuestServiceInterfaceComponentSettingData**](msvm-guestserviceinterfacecomponentsettingdata.md)<br/> | Représente l’état configuré du composant d’interface de service invité. <br/>                                                                                                                                                                                 |
| [**MSVM \_ KvpExchangeComponent**](msvm-kvpexchangecomponent.md)<br/>                                           | Représente l’état du service d’échange de paires clé/valeur, qui fournit un mécanisme permettant d’échanger des données entre l’ordinateur virtuel et le système d’exploitation s’exécutant sur le système d’exploitation de gestion.<br/>                                                  |
| [**MSVM \_ KvpExchangeComponentSettingData**](msvm-kvpexchangecomponentsettingdata.md)<br/>                     | Représente l’état configuré du service d’échange de paires clé/valeur.<br/>                                                                                                                                                                                    |
| [**MSVM \_ KvpExchangeDataItem**](msvm-kvpexchangedataitem.md)<br/>                                             | Représente une paire clé/valeur.<br/>                                                                                                                                                                                                                               |
| [**MSVM \_ RegisteredGuestService**](msvm-registeredguestservice.md)<br/>                                       | Représente une association entre une instance de [**MSVM \_ GuestServiceInterfaceComponent**](msvm-guestserviceinterfacecomponent.md) et une instance de [**MSVM \_ GuestService**](msvm-guestservice.md), qui représente un service s’exécutant dans l’invité. <br/> |
| [**MSVM \_ ShutdownComponent**](msvm-shutdowncomponent.md)<br/>                                                 | Représente l’état du service d’arrêt, qui fournit un mécanisme permettant d’arrêter le système d’exploitation de l’ordinateur virtuel à partir des interfaces de gestion sur le système hôte.<br/>                                                                       |
| [**MSVM \_ ShutdownComponentSettingData**](msvm-shutdowncomponentsettingdata.md)<br/>                           | Représente l’état configuré du service d’arrêt.<br/>                                                                                                                                                                                                   |
| [**MSVM \_ TimeSyncComponent**](msvm-timesynccomponent.md)<br/>                                                 | Représente l’état du service de synchronisation de l’heure, qui est chargé de synchroniser l’heure système d’un ordinateur virtuel avec l’heure système du système d’exploitation en cours d’exécution dans le système d’exploitation de gestion.<br/>                             |
| [**MSVM \_ TimeSyncComponentSettingData**](msvm-timesynccomponentsettingdata.md)<br/>                           | Représente l’état configuré du service de synchronisation de l’heure.<br/>                                                                                                                                                                                       |
| [**MSVM \_ VssComponent**](msvm-vsscomponent.md)<br/>                                                           | Représente l’état du service Service VSS (VSS), qui implémente le demandeur VSS dans le système d’exploitation invité.<br/>                                                                                                                    |
| [**MSVM \_ VssComponentSettingData**](msvm-vsscomponentsettingdata.md)<br/>                                     | Représente l’état configuré du service Service VSS (VSS).<br/>                                                                                                                                                                           |



 

 

 




