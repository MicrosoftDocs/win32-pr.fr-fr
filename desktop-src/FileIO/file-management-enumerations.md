---
description: Énumérations utilisées dans la gestion de fichiers.
ms.assetid: 14b1cfff-5e47-4309-8e62-fb5c8da9ce97
title: Énumérations de la gestion de fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7b53d8f53bf9dbe16c15d21171e52ea3dd0015d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009963"
---
# <a name="file-management-enumerations"></a>Énumérations de la gestion de fichiers

Les énumérations suivantes sont utilisées dans la gestion des fichiers.

## <a name="in-this-section"></a>Dans cette section



| Énumération                                                                   | Description                                                                                                                                                                                                                                 |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_Phase de copie COPYFILE2 \_**](/windows/desktop/api/WinBase/ne-winbase-copyfile2_copy_phase)<br/>             | Indique la phase d’une copie au moment d’une erreur.<br/>                                                                                                                                                                           |
| [**\_Action de message COPYFILE2 \_**](/windows/desktop/api/WinBase/ne-winbase-copyfile2_message_action)<br/>     | Retourné par la fonction de rappel [*CopyFile2ProgressRoutine*](/windows/desktop/api/WinBase/nc-winbase-pcopyfile2_progress_routine) pour indiquer l’action à entreprendre pour l’opération de copie en attente.<br/>                                                             |
| [**\_Type de message COPYFILE2 \_**](/windows/desktop/api/WinBase/ne-winbase-copyfile2_message_type)<br/>         | Indique le type de message passé dans la structure de [**\_ message COPYFILE2**](/windows/desktop/api/WinBase/ns-winbase-copyfile2_message) à la fonction de rappel [*CopyFile2ProgressRoutine*](/windows/desktop/api/WinBase/nc-winbase-pcopyfile2_progress_routine) .<br/>                                       |
| [**contrôle de fichier CSV \_ \_**](/windows/desktop/api/WinIoCtl/ne-winioctl-csv_control_op)<br/>                         | Spécifie le type d’opération de contrôle de fichier CSV à utiliser avec le code de contrôle de contrôle de fichier [**\_ \_ CSV FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_csv_control) .<br/>                                                                                                       |
| [**\_type d’ID de fichier \_**](/windows/desktop/api/WinBase/ne-winbase-file_id_type)<br/>                             | Discriminateur de l’Union dans la structure du [**\_ \_ descripteur**](/windows/desktop/api/WinBase/ns-winbase-file_id_descriptor) de l’ID de fichier.<br/>                                                                                                                                 |
| [**\_informations \_ de fichier \_ par \_ classe de handle**](/windows/win32/api/minwinbase/ne-minwinbase-file_info_by_handle_class)<br/> | Identifie le type d’informations de fichier que [**GetFileInformationByHandleEx**](/windows/desktop/api/WinBase/nf-winbase-getfileinformationbyhandleex) doit récupérer ou [**SetFileInformationByHandle**](/windows/desktop/api/FileAPI/nf-fileapi-setfileinformationbyhandle) doit définir.<br/>                |
| [**\_niveaux d’informations findex \_**](/windows/win32/api/minwinbase/ne-minwinbase-findex_info_levels)<br/>             | Définit les valeurs utilisées avec la fonction [**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa) pour spécifier le niveau d’information des données retournées.<br/>                                                                                 |
| [**\_opérations de recherche findex \_**](/windows/win32/api/minwinbase/ne-minwinbase-findex_search_ops)<br/>               | Définit les valeurs utilisées avec la fonction [**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa) pour spécifier le type de filtrage à effectuer.<br/>                                                                                           |
| [**Obtient \_ les \_ niveaux d’informations FILEEX \_**](/windows/win32/api/minwinbase/ne-minwinbase-get_fileex_info_levels)<br/>        | Définit les valeurs utilisées avec les fonctions [**GetFileAttributesEx**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesexa) et [**GetFileAttributesTransacted**](/windows/desktop/api/WinBase/nf-winbase-getfileattributestransacteda) pour spécifier le niveau d’information des données retournées.<br/> |
| [**indicateur de priorité \_**](/windows/desktop/api/WinBase/ne-winbase-priority_hint)<br/>                            | Définit les valeurs utilisées avec la structure d’informations de l’indicateur de priorité d’e/s de fichier pour spécifier l’indicateur de priorité pour une opération d’e/s de fichier. [**\_ \_ \_ \_**](/windows/desktop/api/WinBase/ns-winbase-file_io_priority_hint_info)<br/>                                                      |
| [**\_niveaux d’informations de flux \_**](/windows/desktop/api/fileapi/ne-fileapi-stream_info_levels)<br/>                 | Définit les valeurs utilisées avec la fonction [**FindFirstStreamW**](/windows/desktop/api/fileapi/nf-fileapi-findfirststreamw) pour spécifier le niveau d’information des données retournées.<br/>                                                                               |



 

 

