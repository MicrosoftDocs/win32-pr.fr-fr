---
description: cette section décrit les fonctions de rappel de l’interpréteur de commandes Windows.
title: Fonctions de rappel de l’interpréteur de commandes
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 617a73d9-e3e6-4def-a5b2-557faa7b03c0
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: d3fd334dd49d2b9cec3322630866fde4a99ccad0b5f253dd7253e551264737a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118460842"
---
# <a name="shell-callback-functions"></a>Fonctions de rappel de l’interpréteur de commandes

cette section décrit les fonctions de rappel de l’interpréteur de commandes Windows.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                     | Description                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BFFCALLBACK**](/previous-versions/windows/desktop/legacy/bb762598(v=vs.85))<br/>                      | Spécifie une fonction de rappel définie par l’application utilisée pour envoyer des messages à et traiter des messages à partir d’une boîte de dialogue **Parcourir** affichée en réponse à un appel à [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera).<br/> |
| [*FMExtensionProc*](fmextensionproc.md)<br/>                       | Spécifie une fonction de rappel définie par l’application appelée par le gestionnaire de fichiers pour communiquer avec une extension du gestionnaire de fichiers.<br/>                                                                                            |
| [*MRUCMPPROC*](mrucmpproc.md)<br/>                                 | Utilisé pour déterminer si un élément est présent dans une liste des derniers fichiers utilisés.<br/>                                                                                                                                   |
| [**\_routine de modification PAPPSTATE \_**](/windows/desktop/api/appnotify/nc-appnotify-pappstate_change_routine)<br/> | Spécifie une fonction de rappel définie par l’application qui notifie l’application lorsque l’application entre ou quitte un état suspendu.<br/>                                                                                            |
| [**SUBCLASSPROC**](/windows/win32/api/commctrl/nc-commctrl-subclassproc)<br/>                  | Définit le prototype pour la fonction de rappel utilisée par [**RemoveWindowSubclass**](/windows/desktop/api/Commctrl/nf-commctrl-removewindowsubclass) et [**SetWindowSubclass**](/windows/desktop/api/Commctrl/nf-commctrl-setwindowsubclass).<br/>                                                   |
| [**\_procédure d’annulation de suppression FM \_**](undeletefile.md)<br/>                     | Spécifie une fonction de rappel définie par l’application appelée par le gestionnaire de fichiers lorsque l’utilisateur choisit la commande **annuler la suppression** dans le menu **fichier** .<br/>                                                                   |



 

 

 
