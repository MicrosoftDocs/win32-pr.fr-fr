---
description: Types énumération utilisés avec la gestion des disques.
ms.assetid: ed8fe5c1-dbdf-43bc-a0a7-17e541eba950
title: Types d’énumération de gestion des disques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87e850e5161e4e8a6326d8014f67d6aad9373015e4354a01fa353087c6863a39
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119765909"
---
# <a name="disk-management-enumeration-types"></a>Types d’énumération de gestion des disques

Les types d’énumération suivants sont utilisés avec la gestion des disques.

## <a name="in-this-section"></a>Dans cette section



| Énumération                                                                              | Description                                                                                                                                                                                                                                                                                                          |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TYPE de média \_**](/windows/win32/api/winioctl/ne-winioctl-media_type)<br/>                                         | Représente les différentes formes de supports d’appareil.<br/>                                                                                                                                                                                                                                                             |
| [**STYLE de PARTITION \_**](/windows/win32/api/winioctl/ne-winioctl-partition_style)<br/>                               | Représente le format d’une partition.<br/>                                                                                                                                                                                                                                                                     |
| [**\_type de bus de stockage \_**](/windows/win32/api/winioctl/ne-winioctl-storage_bus_type)<br/>                                | Fournit un moyen symbolique de représenter les types de bus de stockage.<br/>                                                                                                                                                                                                                                              |
| [**\_État d' \_ intégrité du composant de stockage \_**](/windows/desktop/api/WinIoCtl/ne-winioctl-storage_component_health_status)<br/> | Spécifie l’état d’intégrité d’un composant de stockage.<br/>                                                                                                                                                                                                                                                       |
| [**\_facteur de \_ forme du dispositif de stockage \_**](/windows/desktop/api/WinIoCtl/ne-winioctl-storage_device_form_factor)<br/>           | Spécifie le facteur de forme d’un appareil.<br/>                                                                                                                                                                                                                                                                    |
| [**unités de capacité maximale du dispositif de stockage \_ \_ \_ \_**](/windows/desktop/api/winioctl/ne-winioctl-storage_device_power_cap_units)<br/>  | Unités du seuil d’alimentation maximal.<br/>                                                                                                                                                                                                                                                                 |
| [**\_jeu de \_ codes du port de stockage \_**](/windows/win32/api/winioctl/ne-winioctl-storage_port_code_set)<br/>                     | Réservé pour le système. <br/>                                                                                                                                                                                                                                                                                 |
| [**\_ID de propriété de stockage \_**](/windows/win32/api/winioctl/ne-winioctl-storage_property_id)<br/>                          | Énumère les valeurs possibles du membre **PropertyId** de la structure de [**la \_ \_ requête de propriété de stockage**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) passée comme entrée à la demande de [**\_ \_ \_ propriété de requête de stockage IOCTL**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) pour récupérer les propriétés d’un périphérique de stockage ou d’un adaptateur.<br/> |
| [**\_type de protocole de stockage \_**](/windows/desktop/api/WinIoCtl/ne-winioctl-storage_protocol_type)<br/>                      | Spécifie le protocole d’un dispositif de stockage.<br/>                                                                                                                                                                                                                                                               |
| [**\_type de requête de stockage \_**](/windows/desktop/api/WinIoCtl/ne-winioctl-storage_query_type)<br/>                            | Utilisé par la structure de [**\_ \_ requête de propriété de stockage**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) transmise au code de contrôle de [**\_ \_ \_ propriété de requête de stockage IOCTL**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) pour indiquer les informations qui sont retournées sur une propriété d’un périphérique de stockage ou d’un adaptateur.<br/>                             |
| [**\_modification du cache d’écriture \_**](/windows/win32/api/winioctl/ne-winioctl-write_cache_change)<br/>                            | Indique si les fonctionnalités du cache d’écriture d’un appareil sont modifiables.<br/>                                                                                                                                                                                                                                    |
| [**\_activation du cache d’écriture \_**](/windows/win32/api/winioctl/ne-winioctl-write_cache_enable)<br/>                            | Indique si le cache d’écriture est activé ou désactivé.<br/>                                                                                                                                                                                                                                                 |
| [**\_type de cache d’écriture \_**](/windows/win32/api/winioctl/ne-winioctl-write_cache_type)<br/>                                | Spécifie le type de cache.<br/>                                                                                                                                                                                                                                                                                 |
| [**ÉCRITURE \_**](/windows/win32/api/winioctl/ne-winioctl-write_through)<br/>                                       | Spécifie si un périphérique de stockage prend en charge la mise en cache en écriture.<br/>                                                                                                                                                                                                                                        |



 

 

