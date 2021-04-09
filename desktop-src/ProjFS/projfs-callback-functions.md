---
title: Fonctions de rappel ProjFS
description: Les fonctions de rappel suivantes sont déclarées dans projectedfslib. h.
ms.assetid: <GUID-GOES-HERE>
ms.date: 01/17/2020
ms.topic: article
ms.openlocfilehash: 1412fc4b406b668ad6651d69835f8cdea56857c5
ms.sourcegitcommit: 62e758931c610782807c7c9fad284921a6c56232
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/22/2020
ms.locfileid: "103841826"
---
# <a name="callback-functions"></a>Fonctions de rappel

Les fonctions de rappel suivantes sont déclarées dans projectedfslib. h.

## <a name="in-this-section"></a>Contenu de cette section

| Rubrique | Description |
|-|-|
| [**PRJ_CANCEL_COMMAND_CB**](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_cancel_command_cb) | Notifie le fournisseur qu’une opération par un appel antérieur d’un rappel doit être annulée. |
| [**PRJ_END_DIRECTORY_ENUMERATION_CB**](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_end_directory_enumeration_cb) | Informe le fournisseur qu’une énumération de répertoires est terminée. |
| [**PRJ_GET_DIRECTORY_ENUMERATION_CB**](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_directory_enumeration_cb) | Demande des informations sur l’énumération de répertoires à partir du fournisseur.
| [**PRJ_GET_FILE_DATA_CB**](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_file_data_cb) | Demande le contenu du flux de données principal d’un fichier.
| [**PRJ_GET_PLACEHOLDER_INFO_CB**](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_placeholder_info_cb) | Demande des informations pour un fichier ou un répertoire du fournisseur.
| [**PRJ_NOTIFICATION_CB**](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_notification_cb) | Fournit des notifications au fournisseur sur les opérations du système de fichiers.
| [**PRJ_QUERY_FILE_NAME_CB**](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_query_file_name_cb) | Détermine si un chemin d’accès de fichier donné existe dans le magasin de stockage du fournisseur.
| [**PRJ_START_DIRECTORY_ENUMERATION_CB**](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_start_directory_enumeration_cb) | Informe le fournisseur qu’une énumération de répertoire est en cours de démarrage.