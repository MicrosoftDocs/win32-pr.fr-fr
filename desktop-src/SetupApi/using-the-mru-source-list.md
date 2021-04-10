---
description: La fonction SetupSetSourceList ouvre ou crée une liste source sur le système de l’utilisateur.
ms.assetid: cda632cf-6c92-48fb-aef1-25b320affd3e
title: Utilisation de la liste de sources MRU
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dbecb9e32a554d1818661b1fd7f6e782744c16e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951672"
---
# <a name="using-the-mru-source-list"></a><span data-ttu-id="21a27-103">Utilisation de la liste de sources MRU</span><span class="sxs-lookup"><span data-stu-id="21a27-103">Using the MRU Source List</span></span>

<span data-ttu-id="21a27-104">La fonction [**SetupSetSourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupsetsourcelista) ouvre ou crée une liste source sur le système de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="21a27-104">The [**SetupSetSourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupsetsourcelista) function will open or create a source list on the user's system.</span></span> <span data-ttu-id="21a27-105">Vous pouvez choisir de définir la liste des utilisateurs, la liste système, une combinaison des listes utilisateur et système ou une liste temporaire comme liste de sources MRU.</span><span class="sxs-lookup"><span data-stu-id="21a27-105">You can specify to set the user list, the system list, a combination of the user and system lists, or a temporary list as the MRU source list.</span></span> <span data-ttu-id="21a27-106">Si une liste temporaire est utilisée, il s’agit de la seule liste disponible pour l’application d’installation jusqu’à ce que [**SetupCancelTemporarySourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupcanceltemporarysourcelist) soit appelé, ou **SetupSetSourceList** est appelée une deuxième fois.</span><span class="sxs-lookup"><span data-stu-id="21a27-106">If a temporary list is used, it will be the only list available to the setup application until [**SetupCancelTemporarySourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupcanceltemporarysourcelist) is called, or **SetupSetSourceList** is called a second time.</span></span>

<span data-ttu-id="21a27-107">Une fois qu’une liste est définie, vous pouvez interroger la liste source à l’aide de [**SetupQuerySourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupquerysourcelista) pour obtenir un tableau des chemins d’accès source.</span><span class="sxs-lookup"><span data-stu-id="21a27-107">After a list is set, you can query the source list by using [**SetupQuerySourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupquerysourcelista) to obtain an array of the source paths.</span></span> <span data-ttu-id="21a27-108">Lorsque le tableau de liste source n’est plus nécessaire, vous devez appeler la fonction [**SetupFreeSourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupfreesourcelista) pour libérer les ressources allouées par [**SetupQuerySourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupquerysourcelista).</span><span class="sxs-lookup"><span data-stu-id="21a27-108">When the source list array is no longer needed, you must call the [**SetupFreeSourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupfreesourcelista) function to free the resources allocated by [**SetupQuerySourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupquerysourcelista).</span></span>

<span data-ttu-id="21a27-109">Pour ajouter un chemin d’accès à une liste source, l’un d’eux résidant sur le système de l’utilisateur ou une liste temporaire, appelez [**SetupAddToSourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddtosourcelista).</span><span class="sxs-lookup"><span data-stu-id="21a27-109">To add a path to a source list, either one that is resident on the user's system, or a temporary list, call [**SetupAddToSourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddtosourcelista).</span></span> <span data-ttu-id="21a27-110">Si la liste source spécifiée n’est pas temporaire, cette source restera sur le système de l’utilisateur et sera accessible aux installations suivantes.</span><span class="sxs-lookup"><span data-stu-id="21a27-110">If the source list specified is not temporary, that source will remain on the user's system and is accessible to subsequent installations.</span></span>

<span data-ttu-id="21a27-111">Pour supprimer un chemin d’accès du chemin source, appelez la fonction [**SetupRemoveFromSourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovefromsourcelista) .</span><span class="sxs-lookup"><span data-stu-id="21a27-111">To remove a path from the source path, call the [**SetupRemoveFromSourceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovefromsourcelista) function.</span></span>

 

 



