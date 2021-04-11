---
title: Pilotes (Guide de programmation pour Windows 64 bits)
description: La version 64 bits de Windows est conçue pour permettre aux développeurs d’utiliser une base de code source unique pour leurs applications 32 bits et 64 bits. Dans une large mesure, cela est également vrai pour les pilotes Windows 32 bits et 64 bits.
ms.assetid: 85d789c9-91dd-4cdc-a10b-c38a455fc940
keywords:
- pilotes de programmation Windows 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6843a4efbb68652bf269c819c3a11ba102521318
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104317061"
---
# <a name="drivers-programming-guide-for-64-bit-windows"></a><span data-ttu-id="7a195-105">Pilotes (Guide de programmation pour Windows 64 bits)</span><span class="sxs-lookup"><span data-stu-id="7a195-105">Drivers (Programming Guide for 64-bit Windows)</span></span>

<span data-ttu-id="7a195-106">La version 64 bits de Windows est conçue pour permettre aux développeurs d’utiliser une base de code source unique pour leurs applications 32 bits et 64 bits.</span><span class="sxs-lookup"><span data-stu-id="7a195-106">The 64-bit version of Windows is designed to make it possible for developers to use a single source-code base for their 32-bit and 64-bit applications.</span></span> <span data-ttu-id="7a195-107">Dans une large mesure, cela est également vrai pour les pilotes Windows 32 bits et 64 bits.</span><span class="sxs-lookup"><span data-stu-id="7a195-107">To a large extent, this is also true for 32-bit and 64-bit Windows drivers.</span></span>

<span data-ttu-id="7a195-108">Toutefois, les pilotes 32 bits ne peuvent pas s’exécuter sous Windows 64 bits et doivent être portés.</span><span class="sxs-lookup"><span data-stu-id="7a195-108">However, 32-bit drivers cannot run on 64-bit Windows and must be ported.</span></span> <span data-ttu-id="7a195-109">Pour les applications en mode utilisateur, Windows 64 bits comprend WOW64, ce qui permet aux applications Windows 32 bits de s’exécuter (avec une perte de performances) sur les systèmes qui exécutent Windows 64 bits.</span><span class="sxs-lookup"><span data-stu-id="7a195-109">For user-mode applications, 64-bit Windows includes WOW64, which enables 32-bit Windows applications to execute (with some loss of performance) on systems running 64-bit Windows.</span></span> <span data-ttu-id="7a195-110">Il n’existe aucune couche de traduction équivalente pour les pilotes.</span><span class="sxs-lookup"><span data-stu-id="7a195-110">No equivalent translation layer exists for drivers.</span></span>

<span data-ttu-id="7a195-111">Pour plus d’informations sur le portage des pilotes vers Windows 64 bits, consultez [problèmes liés à 64 bits](https://msdn.microsoft.com/library/aa489627.aspx) dans le kit de pilotes Windows (WDK).</span><span class="sxs-lookup"><span data-stu-id="7a195-111">For information about porting drivers to 64-bit Windows, see [64-Bit Issues](https://msdn.microsoft.com/library/aa489627.aspx) in the Windows Driver Kit (WDK).</span></span>

 

 




