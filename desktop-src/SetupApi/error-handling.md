---
description: 'Trois fonctions génèrent des boîtes de dialogue pour gérer les erreurs : SetupCopyError, SetupDeleteError et SetupRenameError.'
ms.assetid: fcb310e1-5db7-47f3-b3d6-d528eb17e19a
title: Gestion des erreurs (API du programme d’installation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fb1347a3bec800200c2b6bda81e3f1eeeb866de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514220"
---
# <a name="error-handling-setup-api"></a>Gestion des erreurs (API du programme d’installation)

Trois fonctions génèrent des boîtes de dialogue pour gérer les erreurs : [**SetupCopyError**](/windows/desktop/api/Setupapi/nf-setupapi-setupcopyerrora), [**SetupDeleteError**](/windows/desktop/api/Setupapi/nf-setupapi-setupdeleteerrora)et [**SetupRenameError**](/windows/desktop/api/Setupapi/nf-setupapi-setuprenameerrora).

Les routines de rappel peuvent utiliser ces fonctions pour générer une interface utilisateur afin de gérer les notifications [**SPFILENOTIFY \_ COPYERROR**](spfilenotify-copyerror.md), [**SPFILENOTIFY \_ DELETEERROR**](spfilenotify-deleteerror.md)et [**SPFILENOTIFY \_ RENAMEERROR**](spfilenotify-renameerror.md) .

Chacune de ces fonctions de gestion des erreurs génère une boîte de dialogue qui demande à l’utilisateur des informations sur la procédure à suivre. Comme avec [**SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska), vous pouvez modifier la disposition et le comportement de la boîte de dialogue en spécifiant des indicateurs pendant l’appel de la fonction.

 

 



