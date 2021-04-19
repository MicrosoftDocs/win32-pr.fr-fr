---
description: Avant de pouvoir faire des opérations de file d’attente, vous devez ouvrir une file d’attente de fichiers. L’appel de la fonction SetupOpenFileQueue retourne un handle vers un fichier de file d’attente. Ce descripteur est utilisé par les fonctions de file d’attente suivantes pour faire référence à la file d’attente ouverte et y ajouter des opérations ou l’analyser.
ms.assetid: 3eeb4f34-c89e-4733-8a8c-54e470a1fd30
title: Ouverture et fermeture d’une file d’attente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dcd8ece0e09c313857da6838a09e79e23bb46a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530648"
---
# <a name="opening-and-closing-a-queue"></a><span data-ttu-id="dde31-105">Ouverture et fermeture d’une file d’attente</span><span class="sxs-lookup"><span data-stu-id="dde31-105">Opening and Closing a Queue</span></span>

<span data-ttu-id="dde31-106">Avant de pouvoir faire des opérations de file d’attente, vous devez ouvrir une file d’attente de fichiers.</span><span class="sxs-lookup"><span data-stu-id="dde31-106">Before you can queue file operations, you must open a file queue.</span></span> <span data-ttu-id="dde31-107">L’appel de la fonction [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue) retourne un handle vers un fichier de file d’attente.</span><span class="sxs-lookup"><span data-stu-id="dde31-107">Calling the [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue) function returns a handle to a queue file.</span></span> <span data-ttu-id="dde31-108">Ce descripteur est utilisé par les fonctions de file d’attente suivantes pour faire référence à la file d’attente ouverte et y ajouter des opérations ou l’analyser.</span><span class="sxs-lookup"><span data-stu-id="dde31-108">This handle is used by subsequent queue functions to reference the open queue and add operations to it or scan it.</span></span>

<span data-ttu-id="dde31-109">Une fois que toutes les opérations de fichier spécifiées ont été mises en file d’attente et validées, vous devez appeler la fonction [**SetupCloseFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue) pour libérer les ressources allouées pendant l’appel à [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue).</span><span class="sxs-lookup"><span data-stu-id="dde31-109">After all the specified file operations have been queued and committed, you must call the [**SetupCloseFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue) function to release resources allocated during the call to [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue).</span></span>

> [!Note]  
> <span data-ttu-id="dde31-110">La fonction [**SetupCloseFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue) ne valide pas la file d’attente de fichiers.</span><span class="sxs-lookup"><span data-stu-id="dde31-110">The [**SetupCloseFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue) function does not commit the file queue.</span></span> <span data-ttu-id="dde31-111">Toutes les opérations qui ne sont pas validées quand **SetupCloseFileQueue** est appelé ne sont pas exécutées.</span><span class="sxs-lookup"><span data-stu-id="dde31-111">Any operations that are uncommitted when **SetupCloseFileQueue** is called will not be performed.</span></span>

 

 

 



