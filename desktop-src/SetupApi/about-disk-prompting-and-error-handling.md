---
description: Les fonctions de configuration peuvent générer des boîtes de dialogue pour gérer les situations d’installation courantes et collecter des informations auprès de l’utilisateur.
ms.assetid: 0bff17a6-590d-4410-9ed1-0a655d94caad
title: À propos des invites de disque et de gestion des erreurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f9aa7a43cc0efd81f066872a55cde20b66bb13d1c117153606f4b9fe2dd2e58
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118887962"
---
# <a name="about-disk-prompting-and-error-handling"></a>À propos des invites de disque et de gestion des erreurs

Bien que les fonctions d’installation ne fournissent pas d’interface utilisateur, il existe quatre fonctions de configuration qui génèrent des boîtes de dialogue pour gérer les situations d’installation courantes et collecter des informations auprès de l’utilisateur. Il s’agit des éléments suivants : [**SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska), [**SetupCopyError**](/windows/desktop/api/Setupapi/nf-setupapi-setupcopyerrora), [**SetupRenameError**](/windows/desktop/api/Setupapi/nf-setupapi-setuprenameerrora)et [**SetupDeleteError**](/windows/desktop/api/Setupapi/nf-setupapi-setupdeleteerrora).

Les routines de rappel peuvent appeler ces fonctions pour créer des boîtes de dialogue afin de faciliter le traitement des notifications envoyées par d’autres fonctions d’installation telles que [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) et [**SetupInstallFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea).

La fonction [**SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska) invite l’utilisateur à insérer un support amovible, à spécifier un nouveau chemin d’accès source ou à annuler l’installation. L’application peut offrir des options supplémentaires à l’utilisateur, en fonction des indicateurs spécifiés lorsque la fonction est appelée. Celles-ci incluent l’omission du fichier actuel ou la recherche d’un nouveau chemin d’accès source.

Les trois fonctions, [**SetupCopyError**](/windows/desktop/api/Setupapi/nf-setupapi-setupcopyerrora), [**SetupRenameError**](/windows/desktop/api/Setupapi/nf-setupapi-setuprenameerrora)et [**SetupDeleteError**](/windows/desktop/api/Setupapi/nf-setupapi-setupdeleteerrora), créent des boîtes de dialogue qui interagissent avec l’utilisateur pour collecter des informations de l’utilisateur sur la procédure à suivre lorsqu’une erreur s’est produite.

La fonction [**SetupCopyError**](/windows/desktop/api/Setupapi/nf-setupapi-setupcopyerrora) génère une boîte de dialogue qui demande à l’utilisateur comment récupérer à partir d’une erreur de copie. L’utilisateur peut spécifier un nouveau chemin source pour l’opération de copie ou annuler l’installation. Selon les indicateurs spécifiés lors de l’appel à **SetupCopyError**, l’utilisateur peut également être en mesure de rechercher un nouveau chemin d’accès source, d’afficher les détails de l’erreur ou d’ignorer le fichier actuel.

Une boîte de dialogue qui invite l’utilisateur à traiter les erreurs qui se produisent pendant une opération de changement de nom de fichier peut être générée en appelant [**SetupRenameError**](/windows/desktop/api/Setupapi/nf-setupapi-setuprenameerrora). Avec cette boîte de dialogue, l’utilisateur a la possibilité de réessayer l’opération, d’ignorer l’opération de changement de nom en cours ou d’abandonner.

La fonction [**SetupDeleteError**](/windows/desktop/api/Setupapi/nf-setupapi-setupdeleteerrora) génère une boîte de dialogue qui peut recueillir des informations sur la façon dont l’utilisateur souhaite gérer une erreur qui s’est produite pendant une opération de suppression de fichier. L’utilisateur a le choix entre les options pour réessayer l’opération, ignorer l’opération de suppression en cours ou abandonner.

La routine de rappel de file d’attente par défaut, [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka), utilise les quatre fonctions mentionnées précédemment pour générer des parties de son interface utilisateur et pour gérer les erreurs et demander un nouveau média.

 

 



