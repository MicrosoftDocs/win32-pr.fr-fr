---
description: Bloc d’environnement de thread (remarques sur le débogage)
ms.assetid: 5040CB82-D32F-4C44-8C03-30238D5B897A
title: Bloc d’environnement de thread (remarques sur le débogage)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d66b04b522bed8bdf7f5a5571c300019e4537b5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861142"
---
# <a name="thread-environment-block-debugging-notes"></a><span data-ttu-id="4616f-103">Bloc d’environnement de thread (remarques sur le débogage)</span><span class="sxs-lookup"><span data-stu-id="4616f-103">Thread Environment Block (Debugging Notes)</span></span>

<span data-ttu-id="4616f-104">Le bloc d’environnement de thread ([**structure TEB**](/windows/win32/api/winternl/ns-winternl-teb)) contient des informations de contexte pour un thread.</span><span class="sxs-lookup"><span data-stu-id="4616f-104">The Thread Environment Block ([**TEB structure**](/windows/win32/api/winternl/ns-winternl-teb)) holds context information for a thread.</span></span>

<span data-ttu-id="4616f-105">Dans les versions suivantes de Windows, le décalage de l’adresse TEB bits 32 dans le TEB 64 bits est 0.</span><span class="sxs-lookup"><span data-stu-id="4616f-105">In the following versions of Windows, the offset of the 32-bit TEB address within the 64-bit TEB is 0.</span></span> <span data-ttu-id="4616f-106">Cela peut être utilisé pour accéder directement au TEB bits 32 d’un thread WOW64.</span><span class="sxs-lookup"><span data-stu-id="4616f-106">This can be used to directly access the 32-bit TEB of a WOW64 thread.</span></span> <span data-ttu-id="4616f-107">Cela peut changer dans les versions ultérieures de Windows</span><span class="sxs-lookup"><span data-stu-id="4616f-107">This might change in later versions of Windows</span></span>



|               |                        |
|---------------|------------------------|
| <span data-ttu-id="4616f-108">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4616f-108">Windows Vista</span></span> | <span data-ttu-id="4616f-109">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4616f-109">Windows Server 2008</span></span>    |
| <span data-ttu-id="4616f-110">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4616f-110">Windows 7</span></span>     | <span data-ttu-id="4616f-111">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4616f-111">Windows Server 2008 R2</span></span> |
| <span data-ttu-id="4616f-112">Windows 8</span><span class="sxs-lookup"><span data-stu-id="4616f-112">Windows 8</span></span>     | <span data-ttu-id="4616f-113">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4616f-113">Windows Server 2012</span></span>    |
| <span data-ttu-id="4616f-114">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="4616f-114">Windows 8.1</span></span>   | <span data-ttu-id="4616f-115">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="4616f-115">Windows Server 2012 R2</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="4616f-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4616f-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4616f-117">Structures de débogage</span><span class="sxs-lookup"><span data-stu-id="4616f-117">Debugging Structures</span></span>](debugging-structures.md)
</dt> <dt>

[<span data-ttu-id="4616f-118">**\_Contexte WOW64**</span><span class="sxs-lookup"><span data-stu-id="4616f-118">**WOW64\_CONTEXT**</span></span>](/windows/desktop/api/WinNT/ns-winnt-wow64_context)
</dt> </dl>

 

 
