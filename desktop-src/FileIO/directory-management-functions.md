---
description: Fonctions utilisées dans la gestion des répertoires.
ms.assetid: 5517b0e7-2264-4173-8e10-ff7626458bfa
title: Fonctions de gestion d’annuaire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2042b7fc4cc7f6af64c3c0eba0938b3f5d78e7b551981e1cc820b38000b1d745
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118150437"
---
# <a name="directory-management-functions"></a>Fonctions de gestion d’annuaire

Les fonctions suivantes sont utilisées dans la gestion des répertoires.

## <a name="in-this-section"></a>Dans cette section



| Fonction                                                                      | Description                                                                                                                                                               |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya)<br/>                         | Crée un répertoire.<br/>                                                                                                                                       |
| [**CreateDirectoryEx**](/windows/desktop/api/WinBase/nf-winbase-createdirectoryexa)<br/>                     | Crée un répertoire avec les attributs d’un répertoire de modèles spécifié.<br/>                                                                                 |
| [**CreateDirectoryTransacted**](/windows/desktop/api/WinBase/nf-winbase-createdirectorytransacteda)<br/>     | Crée un nouveau répertoire en tant qu’opération traitée avec les attributs d’un répertoire de modèles spécifié.<br/>                                                      |
| [**FindCloseChangeNotification**](/windows/desktop/api/FileAPI/nf-fileapi-findclosechangenotification)<br/> | Arrête la surveillance du handle de notification de modification.<br/>                                                                                                                   |
| [**FindFirstChangeNotification**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstchangenotificationa)<br/> | Crée un handle de notification de modification et définit des conditions de filtre de notification de modification initiales.<br/>                                                                |
| [**FindNextChangeNotification**](/windows/desktop/api/FileAPI/nf-fileapi-findnextchangenotification)<br/>   | Demande que le système d’exploitation signale un handle de notification de modification la prochaine fois qu’il détecte une modification appropriée.<br/>                                         |
| [**GetCurrentDirectory**](/windows/desktop/api/WinBase/nf-winbase-getcurrentdirectory)<br/>                 | Récupère le répertoire actif pour le processus en cours.<br/>                                                                                                       |
| [**ReadDirectoryChangesExW**](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesexw)<br/>         | Récupère des informations qui décrivent les modifications dans le répertoire spécifié, qui peuvent inclure des informations étendues si ce type d’informations est spécifié.<br/> |
| [**ReadDirectoryChangesW**](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesw)<br/>             | Récupère des informations qui décrivent les modifications dans le répertoire spécifié.<br/>                                                                               |
| [**RemoveDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-removedirectorya)<br/>                         | Supprime un répertoire vide existant.<br/>                                                                                                                           |
| [**RemoveDirectoryTransacted**](/windows/desktop/api/WinBase/nf-winbase-removedirectorytransacteda)<br/>     | Supprime un répertoire vide existant en tant qu’opération traitée.<br/>                                                                                                 |
| [**SetCurrentDirectory**](/windows/desktop/api/WinBase/nf-winbase-setcurrentdirectory)<br/>                 | Modifie le répertoire actif pour le processus en cours.<br/>                                                                                                         |



 

 

 




