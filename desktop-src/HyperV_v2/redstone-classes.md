---
description: contient les nouvelles classes pour Windows 10, version 1703.
ms.assetid: 33F993F0-2B20-49F7-9DAC-1D682633420C
title: Classes Redstone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d6a61f2b79cc9739cff7a3643096592186e42a257fbb101549cd6719b75fc7b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119980189"
---
# <a name="redstone-classes"></a>Classes Redstone

contient les nouvelles classes pour Windows 10, version 1703.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                                                | Description                                                                                                                                                                                                                                                                                               |
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MSVM \_ AssignableDeviceDismountSettingData**](msvm-assignabledevicedismountsettingdata.md)<br/>             | Représente les paramètres d’un système virtuel à importer. Utilisé par la méthode [**demount**](msvm-assignabledeviceservice-dismountassignabledevice.md) de la [**classe \_ AssignableDeviceService MSVM**](msvm-assignabledeviceservice.md) .<br/>                                                        |
| [**MSVM \_ AssignableDeviceService**](msvm-assignabledeviceservice.md)<br/>                                     | Gère les appareils attribuables sur un système d’ordinateur hôte.<br/>                                                                                                                                                                                                                                      |
| [**MSVM \_ CollectionReferencePointExportJob**](msvm-collectionreferencepointexportjob.md)<br/>                 | Cette classe représente un travail d’exportation de point de référence de collection.<br/>                                                                                                                                                                                                                       |
| [**MSVM \_ EthernetSwitchHardwareOffloadSettingData**](msvm-ethernetswitchhardwareoffloadsettingdata.md)<br/>   | Représente les paramètres de déchargement du commutateur.<br/>                                                                                                                                                                                                                                                        |
| [**MSVM \_ EthernetSwitchPortMigrationQosSettingData**](msvm-ethernetswitchportmigrationqossettingdata.md)<br/> | Représente les paramètres de QOS VFP.<br/>                                                                                                                                                                                                                                                               |
| [**MSVM \_ EthernetSwitchPortRdmaSettingData**](msvm-ethernetswitchportrdmasettingdata.md)<br/>                 | Représente les données du paramètre de fonctionnalité RDMA du port.<br/>                                                                                                                                                                                                                                                 |
| [**MSVM \_ EthernetSwitchPortTeamMappingSettingData**](msvm-ethernetswitchportteammappingsettingdata.md)<br/>   | Représente les données de paramètre de la fonctionnalité de mappage de l’équipe des ports.<br/>                                                                                                                                                                                                                                         |
| [**MSVM \_ GpuPartition**](msvm-gpupartition.md)<br/>                                                           | Représente l’état de la partition GPU.<br/>                                                                                                                                                                                                                                                     |
| [**MSVM \_ GpuPartitionSettingData**](msvm-gpupartitionsettingdata.md)<br/>                                     | Représente l’état configuré d’un périphérique de partition GPU.<br/>                                                                                                                                                                                                                                     |
| [**MSVM \_ NetworkConnectionDiagnosticInformation**](msvm-networkconnectiondiagnosticinformation.md)<br/>       | Fournit des informations sur la connectivité réseau pour un ordinateur virtuel.<br/>                                                                                                                                                                                                                     |
| [**MSVM \_ NetworkConnectionDiagnosticSettingData**](msvm-networkconnectiondiagnosticsettingdata.md)<br/>       | Représente les paramètres utilisés pour tester la connectivité réseau d’un ordinateur virtuel. <br/>                                                                                                                                                                                                           |
| [**MSVM \_ PartitionableGpu**](msvm-partitionablegpu.md)<br/>                                                   | Représente un GPU partitionné. Chaque GPU peut être divisé en plusieurs partitions GPU, qui peuvent être attribuées à un ordinateur virtuel en tant que processeur graphique virtuel.<br/>                                                                                                                                                  |
| [**MSVM \_ PciExpress**](msvm-pciexpress.md)<br/>                                                               | Représente l’état du port PCI Express.<br/>                                                                                                                                                                                                                                                  |
| [**MSVM \_ PciExpressSettingData**](msvm-pciexpresssettingdata.md)<br/>                                         | Représente l’état configuré d’un port PCI Express.<br/>                                                                                                                                                                                                                                         |
| [**MSVM \_ SecurityElement**](msvm-securityelement.md)<br/>                                                     | Représente les paramètres de sécurité du runtime d’un [**\_ ComputerSystem CIM**](cim-computersystem.md).<br/>                                                                                                                                                                                               |
| [**MSVM \_ securityservice**](msvm-securityservice.md)<br/>                                                     | Représente le service de sécurité. Il est utilisé pour configurer les paramètres de sécurité du système virtuel.<br/>                                                                                                                                                                                                  |
| [**MSVM \_ SecuritySettingData**](msvm-securitysettingdata.md)<br/>                                             | Représente l’état configuré des paramètres de sécurité pour <br/>                                                                                                                                                                                                                                  |
| [**MSVM \_ StorageSettingData**](msvm-storagesettingdata.md)<br/>                                               | Représente les paramètres spécifiques au stockage pour un système virtuel.<br/>                                                                                                                                                                                                                                 |
| [**MSVM \_ SummaryInformationBase**](msvm-summaryinformationbase.md)<br/>                                       | Utilisé dans la méthode [**GetSummaryInformation**](getsummaryinformation-msvm-virtualsystemmanagementservice.md) de la classe [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) pour récupérer rapidement les informations communes relatives à un système virtuel ou à un instantané.<br/> |
| [**MSVM \_ SystemComponentSettingData**](msvm-systemcomponentsettingdata.md)<br/>                               | Classe de base générique pour définir des classes de données qui représentent les composants d’un système virtuel.<br/>                                                                                                                                                                                                     |
| [**MSVM \_ VirtualSystemReferencePointExportJob**](msvm-virtualsystemreferencepointexportjob.md)<br/>           | Cette classe représente un travail d’exportation de point de référence système virtuel.<br/>                                                                                                                                                                                                                   |



 

 

 




