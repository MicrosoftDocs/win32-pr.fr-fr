---
title: Partage d’une procédure d’e/s avec d’autres applications
description: Partage d’une procédure d’e/s avec d’autres applications
ms.assetid: 56e4804b-fe88-4b3b-93f6-f8e41048780d
keywords:
- e/s de fichier multimédia, procédures partagées
- e/s de fichier, procédures partagées
- entrées et sorties (e/s), procédures partagées
- E/s (entrée et sortie), procédures partagées
- partage de procédures d’e/s avec d’autres applications
- mmioInstallIOProc fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd7931bde28338cc625c828128e05047d8ec3370
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104381836"
---
# <a name="sharing-an-io-procedure-with-other-applications"></a><span data-ttu-id="1fa17-109">Partage d’une procédure d’e/s avec d’autres applications</span><span class="sxs-lookup"><span data-stu-id="1fa17-109">Sharing an I/O Procedure with Other Applications</span></span>

<span data-ttu-id="1fa17-110">Si vous souhaitez partager une procédure d’e/s avec d’autres applications, vous devez écrire une bibliothèque de liens dynamiques (DLL) pour votre application.</span><span class="sxs-lookup"><span data-stu-id="1fa17-110">If you want to share an I/O procedure with other applications, you need to write a dynamic-link library (DLL) for your application.</span></span> <span data-ttu-id="1fa17-111">Vous pouvez partager la procédure d’e/s en procédant de l’une des manières suivantes :</span><span class="sxs-lookup"><span data-stu-id="1fa17-111">You can share the I/O procedure by doing one of the following:</span></span>

-   <span data-ttu-id="1fa17-112">Incluez le code de la procédure d’e/s dans la DLL.</span><span class="sxs-lookup"><span data-stu-id="1fa17-112">Include the code for the I/O procedure in the DLL.</span></span>
-   <span data-ttu-id="1fa17-113">Créez une fonction dans la DLL qui appelle la fonction [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc) pour installer la procédure d’e/s.</span><span class="sxs-lookup"><span data-stu-id="1fa17-113">Create a function in the DLL that calls the [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc) function to install the I/O procedure.</span></span>
-   <span data-ttu-id="1fa17-114">Exportez cette fonction dans le fichier de définitions de module de la DLL.</span><span class="sxs-lookup"><span data-stu-id="1fa17-114">Export this function in the module-definitions file of the DLL.</span></span>

<span data-ttu-id="1fa17-115">Pour utiliser la procédure d’e/s partagée, une application doit d’abord appeler la fonction dans la DLL pour installer la procédure d’e/s.</span><span class="sxs-lookup"><span data-stu-id="1fa17-115">To use the shared I/O procedure, an application must first call the function in the DLL to install the I/O procedure.</span></span>

 

 