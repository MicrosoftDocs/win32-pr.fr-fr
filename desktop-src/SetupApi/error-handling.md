---
description: 'Trois fonctions génèrent des boîtes de dialogue pour gérer les erreurs : SetupCopyError, SetupDeleteError et SetupRenameError.'
ms.assetid: fcb310e1-5db7-47f3-b3d6-d528eb17e19a
title: Gestion des erreurs (API du programme d’installation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59f3c69a4ab4943589d00354c401b1f35aa984b04552ecd03a1c4863fcf9134a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119665989"
---
# <a name="error-handling-setup-api"></a>Gestion des erreurs (API du programme d’installation)

Trois fonctions génèrent des boîtes de dialogue pour gérer les erreurs : [**SetupCopyError**](/windows/desktop/api/Setupapi/nf-setupapi-setupcopyerrora), [**SetupDeleteError**](/windows/desktop/api/Setupapi/nf-setupapi-setupdeleteerrora)et [**SetupRenameError**](/windows/desktop/api/Setupapi/nf-setupapi-setuprenameerrora).

Les routines de rappel peuvent utiliser ces fonctions pour générer une interface utilisateur afin de gérer les notifications [**SPFILENOTIFY \_ COPYERROR**](spfilenotify-copyerror.md), [**SPFILENOTIFY \_ DELETEERROR**](spfilenotify-deleteerror.md)et [**SPFILENOTIFY \_ RENAMEERROR**](spfilenotify-renameerror.md) .

Chacune de ces fonctions de gestion des erreurs génère une boîte de dialogue qui demande à l’utilisateur des informations sur la procédure à suivre. Comme avec [**SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska), vous pouvez modifier la disposition et le comportement de la boîte de dialogue en spécifiant des indicateurs pendant l’appel de la fonction.

 

 



