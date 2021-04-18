---
title: Interopérabilité des processus
description: Vous pouvez exécuter des applications Win32 sur Windows 64 bits à l’aide d’une couche d’émulation. Windows 10 sur ARM comprend une couche d’émulation x86-on-ARM64. Pour plus d’informations, consultez exécution d’applications 32 bits.
ms.assetid: a573f26c-7577-4ff0-b314-ae0a33274738
keywords:
- interopérabilité des processus 64-programmation Windows bits
- interopérabilité de la programmation Windows 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 023be0dafabfa8b17cf460542ae06467db517c11
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106512256"
---
# <a name="process-interoperability"></a><span data-ttu-id="183a8-107">Interopérabilité des processus</span><span class="sxs-lookup"><span data-stu-id="183a8-107">Process Interoperability</span></span>

<span data-ttu-id="183a8-108">Vous pouvez exécuter des applications Win32 sur Windows 64 bits à l’aide d’une couche d’émulation.</span><span class="sxs-lookup"><span data-stu-id="183a8-108">You can run Win32-based applications on 64-bit Windows using an emulation layer.</span></span> <span data-ttu-id="183a8-109">Windows 10 sur ARM comprend une couche d’émulation x86-on-ARM64.</span><span class="sxs-lookup"><span data-stu-id="183a8-109">Windows 10 on ARM includes an x86-on-ARM64 emulation layer.</span></span> <span data-ttu-id="183a8-110">Pour plus d’informations, consultez [exécution d’Applications 32 bits](running-32-bit-applications.md).</span><span class="sxs-lookup"><span data-stu-id="183a8-110">For more information, see [Running 32-bit Applications](running-32-bit-applications.md).</span></span>

<span data-ttu-id="183a8-111">Sur Windows 64 bits, un processus 64 bits ne peut pas charger une bibliothèque de liens dynamiques (DLL) 32 bits.</span><span class="sxs-lookup"><span data-stu-id="183a8-111">On 64-bit Windows, a 64-bit process cannot load a 32-bit dynamic-link library (DLL).</span></span> <span data-ttu-id="183a8-112">En outre, un processus 32 bits ne peut pas charger une DLL 64 bits.</span><span class="sxs-lookup"><span data-stu-id="183a8-112">Additionally, a 32-bit process cannot load a 64-bit DLL.</span></span> <span data-ttu-id="183a8-113">Toutefois, Windows 64 bits prend en charge les appels de procédure distante (RPC) entre les processus 64 bits et 32 bits (sur le même ordinateur et sur plusieurs ordinateurs).</span><span class="sxs-lookup"><span data-stu-id="183a8-113">However, 64-bit Windows supports remote procedure calls (RPC) between 64-bit and 32-bit processes (both on the same computer and across computers).</span></span> <span data-ttu-id="183a8-114">Sur Windows 64 bits, un serveur COM hors processus de 32 bits peut communiquer avec un client 64 bits, et un serveur COM hors processus de 64 bits peut communiquer avec un client 32-bit Server.</span><span class="sxs-lookup"><span data-stu-id="183a8-114">On 64-bit Windows, an out-of-process 32-bit COM server can communicate with a 64-bit client, and an out-of-process 64-bit COM server can communicate with a 32-bit client.</span></span> <span data-ttu-id="183a8-115">Par conséquent, si vous avez une DLL 32 bits qui ne prend pas en charge COM, vous pouvez la placer dans un wrapper dans un serveur COM hors processus et utiliser COM pour marshaler les appels vers et à partir d’un processus 64 bits.</span><span class="sxs-lookup"><span data-stu-id="183a8-115">Therefore, if you have a 32-bit DLL that is not COM-aware, you can wrap it in an out-of-process COM server and use COM to marshal calls to and from a 64-bit process.</span></span>

<span data-ttu-id="183a8-116">Les serveurs in-process sont actuellement inscrits à l’aide de l’entrée de Registre **InprocServer** .</span><span class="sxs-lookup"><span data-stu-id="183a8-116">In-process servers are currently registered using the **InprocServer** registry entry.</span></span> <span data-ttu-id="183a8-117">Sur les serveurs Windows 64 bits, les serveurs in-process 64 et 32 bits doivent utiliser l’entrée **InprocServer32** .</span><span class="sxs-lookup"><span data-stu-id="183a8-117">On 64-bit Windows, 64- and 32-bit in-process servers should use the **InprocServer32** entry.</span></span>

<span data-ttu-id="183a8-118">Pour les descripteurs de port qui, par leur nature, sont locaux sur l’ordinateur et ne seraient jamais utilisés sur la limite 32 bits à 64 bits, utilisez le type de pointeur de **handle \_** à la place du type PTR **int \_** ou **DWORD \_** .</span><span class="sxs-lookup"><span data-stu-id="183a8-118">To port handles, which by their nature are local to the computer and would never be used across the 32-bit to 64-bit boundary, use the **HANDLE\_PTR** type instead of the **INT\_PTR** or **DWORD\_PTR** type.</span></span> <span data-ttu-id="183a8-119">Cela comprend le portage des interfaces RPC qui passent des handles comme valeurs **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="183a8-119">This includes porting RPC interfaces passing such handles as **DWORD** values.</span></span> <span data-ttu-id="183a8-120">Le pointeur de **HANDLE 64 \_** bits est 64 bits sur le câble (non tronqué) et n’a donc pas besoin d’être mappé.</span><span class="sxs-lookup"><span data-stu-id="183a8-120">The 64-bit **HANDLE\_PTR** is 64 bits on the wire (not truncated) and thus does not need mapping.</span></span> <span data-ttu-id="183a8-121">(Le pointeur de **HANDLE 32 \_** bits est 32 bits sur le câble.)</span><span class="sxs-lookup"><span data-stu-id="183a8-121">(The 32-bit **HANDLE\_PTR** is 32 bits on the wire.)</span></span>

<span data-ttu-id="183a8-122">Pour plus d’informations, consultez [conception d’interfaces compatibles avec 64 bits](designing-64-bit-compatible-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="183a8-122">For more information, see [Designing 64-bit-Compatible Interfaces](designing-64-bit-compatible-interfaces.md).</span></span>

 

 




