---
description: Bloc d’environnement de thread (remarques sur le débogage)
ms.assetid: 5040CB82-D32F-4C44-8C03-30238D5B897A
title: Bloc d’environnement de thread (remarques sur le débogage)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e9397c2d442b09b308c4886c2672e3be58b661c
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550584"
---
# <a name="thread-environment-block-debugging-notes"></a><span data-ttu-id="b29e4-103">Bloc d’environnement de thread (remarques sur le débogage)</span><span class="sxs-lookup"><span data-stu-id="b29e4-103">Thread Environment Block (Debugging Notes)</span></span>

<span data-ttu-id="b29e4-104">Le bloc d’environnement de thread ([**structure TEB**](/windows/win32/api/winternl/ns-winternl-teb)) contient des informations de contexte pour un thread.</span><span class="sxs-lookup"><span data-stu-id="b29e4-104">The Thread Environment Block ([**TEB structure**](/windows/win32/api/winternl/ns-winternl-teb)) holds context information for a thread.</span></span>

<span data-ttu-id="b29e4-105">Dans les versions suivantes de Windows, le décalage de l’adresse TEB bits 32 dans le TEB 64 bits est 0.</span><span class="sxs-lookup"><span data-stu-id="b29e4-105">In the following versions of Windows, the offset of the 32-bit TEB address within the 64-bit TEB is 0.</span></span> <span data-ttu-id="b29e4-106">Cela peut être utilisé pour accéder directement au TEB bits 32 d’un thread WOW64.</span><span class="sxs-lookup"><span data-stu-id="b29e4-106">This can be used to directly access the 32-bit TEB of a WOW64 thread.</span></span> <span data-ttu-id="b29e4-107">Cela peut changer dans les versions ultérieures de Windows</span><span class="sxs-lookup"><span data-stu-id="b29e4-107">This might change in later versions of Windows</span></span>



|  <span data-ttu-id="b29e4-108">Plate-forme</span><span class="sxs-lookup"><span data-stu-id="b29e4-108">Platform</span></span>     | <span data-ttu-id="b29e4-109">Version</span><span class="sxs-lookup"><span data-stu-id="b29e4-109">Version</span></span>                |
|---------------|------------------------|
| <span data-ttu-id="b29e4-110">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b29e4-110">Windows Vista</span></span> | <span data-ttu-id="b29e4-111">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b29e4-111">Windows Server 2008</span></span>    |
| <span data-ttu-id="b29e4-112">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b29e4-112">Windows 7</span></span>     | <span data-ttu-id="b29e4-113">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b29e4-113">Windows Server 2008 R2</span></span> |
| <span data-ttu-id="b29e4-114">Windows 8</span><span class="sxs-lookup"><span data-stu-id="b29e4-114">Windows 8</span></span>     | <span data-ttu-id="b29e4-115">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b29e4-115">Windows Server 2012</span></span>    |
| <span data-ttu-id="b29e4-116">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="b29e4-116">Windows 8.1</span></span>   | <span data-ttu-id="b29e4-117">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="b29e4-117">Windows Server 2012 R2</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="b29e4-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b29e4-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b29e4-119">Structures de débogage</span><span class="sxs-lookup"><span data-stu-id="b29e4-119">Debugging Structures</span></span>](debugging-structures.md)
</dt> <dt>

[<span data-ttu-id="b29e4-120">**\_Contexte WOW64**</span><span class="sxs-lookup"><span data-stu-id="b29e4-120">**WOW64\_CONTEXT**</span></span>](/windows/desktop/api/WinNT/ns-winnt-wow64_context)
</dt> </dl>

 

 
