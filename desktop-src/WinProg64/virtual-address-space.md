---
title: Espace d’adressage virtuel (Guide de programmation pour Windows 64 bits)
description: Par défaut, les applications basées sur Microsoft Windows 64 bits disposent d’un espace d’adressage en mode utilisateur de plusieurs téraoctets.
ms.assetid: c5c4af39-727e-46e1-821e-8342c555bf4c
keywords:
- Guide de programmation Windows 64 bits-programmation Windows 64 bits, espace d’adressage virtuel
- espace d’adressage virtuel 64-programmation Windows bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91e4aa6eb67ebf931d1152b3a1101df2757e899b
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104032162"
---
# <a name="virtual-address-space-programming-guide-for-64-bit-windows"></a><span data-ttu-id="8d5fa-105">Espace d’adressage virtuel (Guide de programmation pour Windows 64 bits)</span><span class="sxs-lookup"><span data-stu-id="8d5fa-105">Virtual Address Space (Programming Guide for 64-bit Windows)</span></span>

<span data-ttu-id="8d5fa-106">Par défaut, les applications basées sur Microsoft Windows 64 bits disposent d’un espace d’adressage en mode utilisateur de plusieurs téraoctets.</span><span class="sxs-lookup"><span data-stu-id="8d5fa-106">By default, 64-bit Microsoft Windows-based applications have a user-mode address space of several terabytes.</span></span> <span data-ttu-id="8d5fa-107">Pour obtenir des valeurs précises, consultez [limites de mémoire pour les versions de Windows et Windows Server](/windows/desktop/Memory/memory-limits-for-windows-releases).</span><span class="sxs-lookup"><span data-stu-id="8d5fa-107">For precise values, see [Memory Limits for Windows and Windows Server Releases](/windows/desktop/Memory/memory-limits-for-windows-releases).</span></span> <span data-ttu-id="8d5fa-108">Toutefois, les applications peuvent spécifier que le système doit allouer toute la mémoire pour l’application inférieure à 2 gigaoctets.</span><span class="sxs-lookup"><span data-stu-id="8d5fa-108">However, applications can specify that the system should allocate all memory for the application below 2 gigabytes.</span></span> <span data-ttu-id="8d5fa-109">Cette fonctionnalité est utile pour les applications 64 bits si les conditions suivantes sont remplies :</span><span class="sxs-lookup"><span data-stu-id="8d5fa-109">This feature is beneficial for 64-bit applications if the following conditions are true:</span></span>

-   <span data-ttu-id="8d5fa-110">Un espace d’adressage de 2 Go suffit.</span><span class="sxs-lookup"><span data-stu-id="8d5fa-110">A 2 GB address space is sufficient.</span></span>
-   <span data-ttu-id="8d5fa-111">Le code contient de nombreux avertissements de troncation de pointeur.</span><span class="sxs-lookup"><span data-stu-id="8d5fa-111">The code has many pointer truncation warnings.</span></span>
-   <span data-ttu-id="8d5fa-112">Les pointeurs et les entiers sont librement mélangés.</span><span class="sxs-lookup"><span data-stu-id="8d5fa-112">Pointers and integers are freely mixed.</span></span>
-   <span data-ttu-id="8d5fa-113">Le code présente un polymorphisme utilisant des types de données 32 bits.</span><span class="sxs-lookup"><span data-stu-id="8d5fa-113">The code has polymorphism using 32-bit data types.</span></span>

<span data-ttu-id="8d5fa-114">Tous les pointeurs sont toujours des pointeurs 64 bits, mais le système garantit que toutes les allocations de mémoire se produisent au-dessous de la limite de 2 Go, de sorte que si l’application tronque un pointeur, aucune donnée significative n’est perdue.</span><span class="sxs-lookup"><span data-stu-id="8d5fa-114">All pointers are still 64-bit pointers, but the system ensures that every memory allocation occurs below the 2 GB limit, so that if the application truncates a pointer, no significant data is lost.</span></span> <span data-ttu-id="8d5fa-115">Les pointeurs peuvent être tronqués aux valeurs 32 bits, puis étendus aux valeurs 64 bits par extension de signe ou par extension de zéro.</span><span class="sxs-lookup"><span data-stu-id="8d5fa-115">Pointers can be truncated to 32-bit values, then extended to 64-bit values by either sign extension or zero extension.</span></span>

<span data-ttu-id="8d5fa-116">Pour spécifier cette limitation de mémoire, utilisez l’option **/LARGEADDRESSAWARE : no** linker.</span><span class="sxs-lookup"><span data-stu-id="8d5fa-116">To specify this memory limitation, use the **/LARGEADDRESSAWARE:NO** linker option.</span></span> <span data-ttu-id="8d5fa-117">Notez que **/LARGEADDRESSAWARE : no** est ignoré pour un binaire ARM64.</span><span class="sxs-lookup"><span data-stu-id="8d5fa-117">Note that **/LARGEADDRESSAWARE:NO** is ignored for an ARM64 binary.</span></span> <span data-ttu-id="8d5fa-118">Toutefois, gardez à l’esprit que des problèmes peuvent survenir lors de l’utilisation de cette option.</span><span class="sxs-lookup"><span data-stu-id="8d5fa-118">However, be aware that problems can occur when using this option.</span></span> <span data-ttu-id="8d5fa-119">Si vous générez une DLL qui utilise cette option et que la DLL est appelée par une application qui n’utilise pas cette option, la DLL peut tronquer un pointeur 64 bits dont les 32 premiers bits sont significatifs.</span><span class="sxs-lookup"><span data-stu-id="8d5fa-119">If you build a DLL that uses this option and the DLL is called by an application that does not use this option, the DLL could truncate a 64-bit pointer whose upper 32 bits are significant.</span></span> <span data-ttu-id="8d5fa-120">Cela peut entraîner une défaillance de l’application sans aucun avertissement.</span><span class="sxs-lookup"><span data-stu-id="8d5fa-120">This can cause application failure without any warning.</span></span>

 

 
