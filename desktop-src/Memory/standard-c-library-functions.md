---
description: Les applications peuvent utiliser en toute sécurité les fonctionnalités de gestion de la mémoire de la bibliothèque Runtime C (malloc, Free, etc.) et C++ (New, Delete, etc.).
ms.assetid: c58ed263-577d-47c5-93cb-5a7c83604171
title: Fonctions de la bibliothèque C standard
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 303333b32f5645f19d8d22a072d25692cea4607f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524496"
---
# <a name="standard-c-library-functions"></a><span data-ttu-id="d124a-103">Fonctions de la bibliothèque C standard</span><span class="sxs-lookup"><span data-stu-id="d124a-103">Standard C Library Functions</span></span>

<span data-ttu-id="d124a-104">Les applications peuvent utiliser en toute sécurité les fonctionnalités de gestion de la mémoire de la bibliothèque Runtime C (**malloc**, **Free**, etc.) et C++ (**New**, **Delete**, etc.).</span><span class="sxs-lookup"><span data-stu-id="d124a-104">Applications can safely use the memory management features of the C run-time library (**malloc**, **free**, and so on) and C++ (**new**, **delete**, and so on).</span></span> <span data-ttu-id="d124a-105">Les fonctions de la bibliothèque Runtime C ne présentent pas les problèmes potentiels sous Windows 16 bits.</span><span class="sxs-lookup"><span data-stu-id="d124a-105">The C run-time library functions do not have the potential problems they have under 16-bit Windows.</span></span> <span data-ttu-id="d124a-106">La gestion de la mémoire n’est plus un problème, car le système est libre de gérer la mémoire en déplaçant les pages de la mémoire physique sans affecter les adresses virtuelles.</span><span class="sxs-lookup"><span data-stu-id="d124a-106">Memory management is no longer a problem because the system is free to manage memory by moving pages of physical memory without affecting the virtual addresses.</span></span> <span data-ttu-id="d124a-107">De même, la distinction entre les pointeurs near et Far n’est plus pertinente.</span><span class="sxs-lookup"><span data-stu-id="d124a-107">Similarly, the distinction between near and far pointers is no longer relevant.</span></span> <span data-ttu-id="d124a-108">Par conséquent, vous pouvez utiliser les fonctions de la bibliothèque C standard pour la gestion de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="d124a-108">Therefore, you can use the standard C library functions for memory management.</span></span> <span data-ttu-id="d124a-109">Toutefois, les fonctions de gestion de la mémoire fournissent des fonctionnalités qui ne sont pas disponibles dans la bibliothèque Runtime C.</span><span class="sxs-lookup"><span data-stu-id="d124a-109">However, the memory management functions do provide functionality that is unavailable in the C run-time library.</span></span>

 

 



