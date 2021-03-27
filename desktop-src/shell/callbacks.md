---
description: Cette section décrit les fonctions de rappel de l’interpréteur de commandes Windows.
title: Fonctions de rappel de l’interpréteur de commandes
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 617a73d9-e3e6-4def-a5b2-557faa7b03c0
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 4f6ae93437caa740c8c1349690b7e1452a032491
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393451"
---
# <a name="shell-callback-functions"></a><span data-ttu-id="2ca22-103">Fonctions de rappel de l’interpréteur de commandes</span><span class="sxs-lookup"><span data-stu-id="2ca22-103">Shell Callback Functions</span></span>

<span data-ttu-id="2ca22-104">Cette section décrit les fonctions de rappel de l’interpréteur de commandes Windows.</span><span class="sxs-lookup"><span data-stu-id="2ca22-104">This section describes the Windows Shell callback functions.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="2ca22-105">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="2ca22-105">In this section</span></span>



| <span data-ttu-id="2ca22-106">Rubrique</span><span class="sxs-lookup"><span data-stu-id="2ca22-106">Topic</span></span>                                                                     | <span data-ttu-id="2ca22-107">Description</span><span class="sxs-lookup"><span data-stu-id="2ca22-107">Description</span></span>                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ca22-108">[**BFFCALLBACK**](/previous-versions/windows/desktop/legacy/bb762598(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2ca22-108">[**BFFCALLBACK**](/previous-versions/windows/desktop/legacy/bb762598(v=vs.85))</span></span><br/>                      | <span data-ttu-id="2ca22-109">Spécifie une fonction de rappel définie par l’application utilisée pour envoyer des messages à et traiter des messages à partir d’une boîte de dialogue **Parcourir** affichée en réponse à un appel à [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera).</span><span class="sxs-lookup"><span data-stu-id="2ca22-109">Specifies an application-defined callback function used to send messages to, and process messages from, a **Browse** dialog box displayed in response to a call to [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera).</span></span><br/> |
| [<span data-ttu-id="2ca22-110">*FMExtensionProc*</span><span class="sxs-lookup"><span data-stu-id="2ca22-110">*FMExtensionProc*</span></span>](fmextensionproc.md)<br/>                       | <span data-ttu-id="2ca22-111">Spécifie une fonction de rappel définie par l’application appelée par le gestionnaire de fichiers pour communiquer avec une extension du gestionnaire de fichiers.</span><span class="sxs-lookup"><span data-stu-id="2ca22-111">Specifies an application-defined callback function called by File Manager to communicate with a File Manager extension.</span></span><br/>                                                                                            |
| [<span data-ttu-id="2ca22-112">*MRUCMPPROC*</span><span class="sxs-lookup"><span data-stu-id="2ca22-112">*MRUCMPPROC*</span></span>](mrucmpproc.md)<br/>                                 | <span data-ttu-id="2ca22-113">Utilisé pour déterminer si un élément est présent dans une liste des derniers fichiers utilisés.</span><span class="sxs-lookup"><span data-stu-id="2ca22-113">Used to determine whether an item is present in a most recently used (MRU) list.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="2ca22-114">**\_routine de modification PAPPSTATE \_**</span><span class="sxs-lookup"><span data-stu-id="2ca22-114">**PAPPSTATE\_CHANGE\_ROUTINE**</span></span>](/windows/desktop/api/appnotify/nc-appnotify-pappstate_change_routine)<br/> | <span data-ttu-id="2ca22-115">Spécifie une fonction de rappel définie par l’application qui notifie l’application lorsque l’application entre ou quitte un état suspendu.</span><span class="sxs-lookup"><span data-stu-id="2ca22-115">Specifies an app-defined callback function that notifies the app when the app is entering or leaving a suspended state.</span></span><br/>                                                                                            |
| [<span data-ttu-id="2ca22-116">**SUBCLASSPROC**</span><span class="sxs-lookup"><span data-stu-id="2ca22-116">**SUBCLASSPROC**</span></span>](/windows/win32/api/commctrl/nc-commctrl-subclassproc)<br/>                  | <span data-ttu-id="2ca22-117">Définit le prototype pour la fonction de rappel utilisée par [**RemoveWindowSubclass**](/windows/desktop/api/Commctrl/nf-commctrl-removewindowsubclass) et [**SetWindowSubclass**](/windows/desktop/api/Commctrl/nf-commctrl-setwindowsubclass).</span><span class="sxs-lookup"><span data-stu-id="2ca22-117">Defines the prototype for the callback function used by [**RemoveWindowSubclass**](/windows/desktop/api/Commctrl/nf-commctrl-removewindowsubclass) and [**SetWindowSubclass**](/windows/desktop/api/Commctrl/nf-commctrl-setwindowsubclass).</span></span><br/>                                                   |
| [<span data-ttu-id="2ca22-118">**\_procédure d’annulation de suppression FM \_**</span><span class="sxs-lookup"><span data-stu-id="2ca22-118">**FM\_UNDELETE\_PROC**</span></span>](undeletefile.md)<br/>                     | <span data-ttu-id="2ca22-119">Spécifie une fonction de rappel définie par l’application appelée par le gestionnaire de fichiers lorsque l’utilisateur choisit la commande **annuler la suppression** dans le menu **fichier** .</span><span class="sxs-lookup"><span data-stu-id="2ca22-119">Specifies an application-defined callback function called by File Manager when the user chooses the **Undelete** command from the **File** menu.</span></span><br/>                                                                   |



 

 

 
