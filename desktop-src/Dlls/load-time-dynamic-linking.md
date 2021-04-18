---
description: Lorsque le système démarre un programme qui utilise la liaison dynamique au moment du chargement, il utilise les informations que l’éditeur de liens place dans le fichier pour localiser les noms des DLL utilisées par le processus.
ms.assetid: 29a17116-bb08-4fdd-857c-b7a7f8d2278c
title: Load-Time la liaison dynamique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28435fd6df4a3fc5311dc46dbb761b48c139a6fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530015"
---
# <a name="load-time-dynamic-linking"></a><span data-ttu-id="fe851-103">Load-Time la liaison dynamique</span><span class="sxs-lookup"><span data-stu-id="fe851-103">Load-Time Dynamic Linking</span></span>

<span data-ttu-id="fe851-104">Lorsque le système démarre un programme qui utilise la liaison dynamique au moment du chargement, il utilise les informations que l’éditeur de liens place dans le fichier pour localiser les noms des DLL utilisées par le processus.</span><span class="sxs-lookup"><span data-stu-id="fe851-104">When the system starts a program that uses load-time dynamic linking, it uses the information the linker placed in the file to locate the names of the DLLs that are used by the process.</span></span> <span data-ttu-id="fe851-105">Le système recherche ensuite les dll.</span><span class="sxs-lookup"><span data-stu-id="fe851-105">The system then searches for the DLLs.</span></span> <span data-ttu-id="fe851-106">Pour plus d’informations, consultez ordre de recherche de la [bibliothèque de liens dynamiques](dynamic-link-library-search-order.md).</span><span class="sxs-lookup"><span data-stu-id="fe851-106">For more information, see [Dynamic-Link Library Search Order](dynamic-link-library-search-order.md).</span></span>

<span data-ttu-id="fe851-107">Si le système ne parvient pas à localiser une DLL requise, il met fin au processus et affiche une boîte de dialogue qui signale l’erreur à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="fe851-107">If the system cannot locate a required DLL, it terminates the process and displays a dialog box that reports the error to the user.</span></span> <span data-ttu-id="fe851-108">Dans le cas contraire, le système mappe la DLL dans l’espace d’adressage virtuel du processus et incrémente le nombre de références de DLL.</span><span class="sxs-lookup"><span data-stu-id="fe851-108">Otherwise, the system maps the DLL into the virtual address space of the process and increments the DLL reference count.</span></span>

<span data-ttu-id="fe851-109">Le système appelle la fonction de point d’entrée.</span><span class="sxs-lookup"><span data-stu-id="fe851-109">The system calls the entry-point function.</span></span> <span data-ttu-id="fe851-110">La fonction reçoit un code indiquant que le processus est en train de charger la DLL.</span><span class="sxs-lookup"><span data-stu-id="fe851-110">The function receives a code indicating that the process is loading the DLL.</span></span> <span data-ttu-id="fe851-111">Si la fonction de point d’entrée ne retourne pas la valeur TRUE, le système met fin au processus et signale l’erreur.</span><span class="sxs-lookup"><span data-stu-id="fe851-111">If the entry-point function does not return TRUE, the system terminates the process and reports the error.</span></span> <span data-ttu-id="fe851-112">Pour plus d’informations sur la fonction de point d’entrée, consultez [bibliothèque de liens dynamiques Entry-Point fonction](dynamic-link-library-entry-point-function.md).</span><span class="sxs-lookup"><span data-stu-id="fe851-112">For more information about the entry-point function, see [Dynamic-Link Library Entry-Point Function](dynamic-link-library-entry-point-function.md).</span></span>

<span data-ttu-id="fe851-113">Enfin, le système modifie la table d’adresses des fonctions avec les adresses de départ des fonctions DLL importées.</span><span class="sxs-lookup"><span data-stu-id="fe851-113">Finally, the system modifies the function address table with the starting addresses for the imported DLL functions.</span></span>

<span data-ttu-id="fe851-114">La DLL est mappée dans l’espace d’adressage virtuel du processus lors de son initialisation et est chargée dans la mémoire physique uniquement lorsque cela est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="fe851-114">The DLL is mapped into the virtual address space of the process during its initialization and is loaded into physical memory only when needed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fe851-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fe851-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fe851-116">Utilisation de la liaison dynamique Load-Time</span><span class="sxs-lookup"><span data-stu-id="fe851-116">Using Load-Time Dynamic Linking</span></span>](using-load-time-dynamic-linking.md)
</dt> </dl>

 

 



