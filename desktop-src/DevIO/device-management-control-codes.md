---
description: Les codes de contrôle suivants sont utilisés avec les appareils changeur.
ms.assetid: b3a3ffa1-e710-4d96-aff8-5b6876ab032b
title: Codes de contrôle de la gestion des appareils
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f87bd6aa147407618c6df82686f175cb92690ec
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127114362"
---
# <a name="device-management-control-codes"></a>Codes de contrôle de la gestion des appareils

Les codes de contrôle suivants sont utilisés avec les appareils changeur.



| Valeur                                                                                          | Signification                                                                                                                                              |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_moyenne Exchange du changeur IOCTL \_ \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_exchange_medium)                      | Déplace un élément multimédia d’un élément source vers une destination, et le média à l’origine dans la première destination vers une autre destination. |
| [**\_État de l' \_ \_ élément \_ du changeur IOCTL**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_get_element_status)               | Récupère l’état de tous les éléments ou un nombre spécifié d’éléments d’un type particulier.                                                         |
| [**\_paramètres d’extraction du changeur IOCTL \_ \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_get_parameters)                        | Récupère les paramètres du périphérique spécifié.                                                                                                    |
| [**le \_ changeur IOCTL \_ obtient les \_ données du produit \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_get_product_data)                   | Récupère les données de produit pour l’appareil spécifié.                                                                                                 |
| [**\_État d’extraction du changeur IOCTL \_ \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_get_status)                                | Récupère l’état actuel de l’appareil spécifié.                                                                                                |
| [**\_ \_ État de l’élément d’initialisation du CHANGEur IOCTL \_ \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_initialize_element_status) | Initialise l’état de tous les éléments ou des éléments spécifiés d’un type particulier.                                                               |
| [**\_moyenne de déplacement du changeur IOCTL \_ \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_move_medium)                              | Déplace un élément multimédia vers une destination.                                                                                                             |
| [**\_étiquettes de volume de requête du changeur IOCTL \_ \_ \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_query_volume_tags)                 | Récupère les informations de balise de volume pour les éléments spécifiés.                                                                                     |
| [**le \_ changeur IOCTL \_ réinitialise le \_ transport**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_reinitialize_transport)        | Réétalonne physiquement un élément de transport.                                                                                                         |
| [**\_accès au changeur IOCTL \_ défini \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_set_access)                                | Définit l’état du port d’insertion/éjection, de la porte ou du pavé numérique de l’appareil.                                                                                   |
| [**POSITION définie par le \_ changeur IOCTL \_ \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_changer_set_position)                            | Définit le mécanisme de transport robotique du changeur sur l’adresse d’élément spécifiée.                                                                     |



 

Les codes de contrôle suivants sont utilisés avec la gestion des périphériques.



| Code de contrôle                                                                                      | Opération                                                                                                    |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**vérification de la vérification du \_ stockage IOCTL \_ \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_check_verify)                               | Vérifie la modification d’un périphérique multimédia amovible.                                                               |
| [**\_support d' \_ éjection du stockage IOCTL \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_eject_media)                                 | Éjecte le média d’un périphérique SCSI.                                                                             |
| [**\_contrôle d' \_ éjection du stockage IOCTL \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_ejection_control)                       | Active ou désactive le mécanisme qui éjecte le média.                                                         |
| [**Numéro de l’appareil de \_ stockage IOCTL \_ \_ \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_get_device_number)                    | Récupère le type d’appareil, le numéro de périphérique et, pour un périphérique partitionné, le numéro de partition d’un appareil. |
| [**informations d’accès à chaud pour le \_ stockage IOCTL \_ \_ \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_get_hotplug_info)                      | Récupère la configuration de la réchaud du périphérique spécifié.                                                 |
| [**\_numéro de \_ série du support d’extraction du stockage IOCTL \_ \_ \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_get_media_serial_number)       | Récupère le numéro de série d’un périphérique USB.                                                                 |
| [**\_types de \_ médias d’extraction de stockage IOCTL \_ \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_get_media_types)                        | Récupère les informations géométriques de l’appareil.                                                            |
| [**\_type de média d’extraction de stockage IOCTL \_ \_ \_ \_ ex**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_get_media_types_ex)                 | Récupère des informations sur les types de médias pris en charge par un appareil.                                        |
| [**\_support de \_ chargement du stockage IOCTL \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_load_media)                                   | Charge un média dans un appareil.                                                                                   |
| [**\_attributs du \_ jeu de données de gestion du stockage IOCTL \_ \_ \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_manage_data_set_attributes) |                                                                                                              |
| [**\_contrôle de \_ MCN de stockage IOCTL \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_mcn_control)                                 | Active ou désactive la notification de modification du média.                                                               |
| [**\_suppression du \_ support de stockage IOCTL \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_media_removal)                             | Active ou désactive le mécanisme d’éjection de support.                                                               |
| [**\_capacité de \_ lecture du stockage IOCTL \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_read_capacity)                             | Récupère les informations géométriques de l’appareil.                                                           |
| [**\_informations de \_ \_ réchaud du jeu de stockage IOCTL \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_set_hotplug_info)                      | Définit la configuration de la réchaud du périphérique spécifié.                                                      |



 

 

 



