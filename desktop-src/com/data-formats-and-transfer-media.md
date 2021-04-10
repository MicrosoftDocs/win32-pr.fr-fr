---
title: Formats de données et média de transfert
description: Formats de données et média de transfert
ms.assetid: c6023c42-ce20-40e4-9d88-55fa1d2a4d38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6893fabd776d196cbc7354dde7c330f9caffb0a
ms.sourcegitcommit: 89f99926f946dc6c5ea600fb7c41f6b19ceac516
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/21/2020
ms.locfileid: "104032079"
---
# <a name="data-formats-and-transfer-media"></a><span data-ttu-id="b44aa-103">Formats de données et média de transfert</span><span class="sxs-lookup"><span data-stu-id="b44aa-103">Data Formats and Transfer Media</span></span>

<span data-ttu-id="b44aa-104">La plupart des plateformes, y compris Windows, définissent un protocole standard pour transférer des données entre les applications, en fonction d’un ensemble de fonctions appelé le presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="b44aa-104">Most platforms, including Windows, define a standard protocol for transferring data between applications, based on a set of functions called the clipboard.</span></span> <span data-ttu-id="b44aa-105">Les applications qui utilisent ces fonctions peuvent partager des données même si leurs formats de données natifs sont très différents.</span><span class="sxs-lookup"><span data-stu-id="b44aa-105">Applications using these functions can share data even if their native data formats are wildly different.</span></span> <span data-ttu-id="b44aa-106">En règle générale, ces presse-papiers présentent deux lacunes importantes que COM a résolues.</span><span class="sxs-lookup"><span data-stu-id="b44aa-106">Generally, these clipboards have two significant shortcomings that COM has overcome.</span></span>

<span data-ttu-id="b44aa-107">Tout d’abord, les descriptions de données utilisent uniquement un identificateur de format, tel que l’identificateur de format du presse-papiers 16 bits unique sur Windows, ce qui signifie que le presse-papiers peut uniquement décrire la structure de ses données, c’est-à-dire le classement des bits.</span><span class="sxs-lookup"><span data-stu-id="b44aa-107">First, data descriptions use only a format identifier, such as the single 16-bit clipboard format identifier on Windows, which means the clipboard can only describe the structure of its data, that is, the ordering of the bits.</span></span> <span data-ttu-id="b44aa-108">Il peut créer un rapport, « j’ai une bitmap « » ou j’ai du texte», mais il ne peut pas spécifier les appareils cibles pour lesquels les données sont composées, les vues ou les aspects des données qu’ils peuvent fournir, ou les supports de stockage les mieux adaptés à son transfert.</span><span class="sxs-lookup"><span data-stu-id="b44aa-108">It can report, "I have a bitmap" "or I have some text," but it cannot specify the target devices for which the data is composed, which views or aspects of itself the data can provide, or which storage media are best suited for its transfer.</span></span> <span data-ttu-id="b44aa-109">Par exemple, il ne peut pas créer de rapport, « j’ai une chaîne de texte qui est stockée dans la mémoire globale et mise en forme pour une présentation à l’écran ou sur une imprimante » ou « j’ai une bitmap d’esquisse miniature restituée pour une imprimante à matrice à 100 ppp et stockée sous forme de fichier de disque ».</span><span class="sxs-lookup"><span data-stu-id="b44aa-109">For example, it cannot report, "I have a string of text that is stored in global memory and formatted for presentation either on screen or on a printer" or "I have a thumbnail sketch bitmap rendered for a 100 dpi dot-matrix printer and stored as a disk file."</span></span>

<span data-ttu-id="b44aa-110">Deuxièmement, tous les transferts de données à l’aide du presse-papiers se produisent généralement via la mémoire globale.</span><span class="sxs-lookup"><span data-stu-id="b44aa-110">Second, all data transfers using the clipboard generally occur through global memory.</span></span> <span data-ttu-id="b44aa-111">L’utilisation de la mémoire globale est raisonnablement efficace pour les petites quantités de données, mais littéralement inefficace pour des volumes importants, tels qu’un objet multimédia de 20 Mo.</span><span class="sxs-lookup"><span data-stu-id="b44aa-111">Using global memory is reasonably efficient for small amounts of data but horribly inefficient for large amounts, such as a 20 MB multimedia object.</span></span> <span data-ttu-id="b44aa-112">La mémoire globale est lente pour un objet de données volumineux, dont la taille nécessite une permutation importante de la mémoire virtuelle sur le disque.</span><span class="sxs-lookup"><span data-stu-id="b44aa-112">Global memory is slow for a large data object, whose size requires considerable swapping to virtual memory on disk.</span></span> <span data-ttu-id="b44aa-113">Dans les cas où les données qui sont échangées se trouvent principalement sur le disque, leur forçage dans ce goulot d’étranglement de la mémoire virtuelle est très inefficace.</span><span class="sxs-lookup"><span data-stu-id="b44aa-113">In cases where the data being exchanged is going to reside mostly on disk anyway, forcing it through this virtual-memory bottleneck is highly inefficient.</span></span> <span data-ttu-id="b44aa-114">Une meilleure méthode consiste à ignorer la mémoire globale entièrement et à transférer simplement les données directement sur le disque.</span><span class="sxs-lookup"><span data-stu-id="b44aa-114">A better way would skip global memory entirely and simply transfer the data directly to disk.</span></span>

<span data-ttu-id="b44aa-115">Pour atténuer ces problèmes, COM fournit deux structures de données : [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) et [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1).</span><span class="sxs-lookup"><span data-stu-id="b44aa-115">To alleviate these problems, COM provides two data structures: [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) and [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1).</span></span> <span data-ttu-id="b44aa-116">Pour plus d'informations, voir les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="b44aa-116">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="b44aa-117">La structure FORMATETC</span><span class="sxs-lookup"><span data-stu-id="b44aa-117">The FORMATETC Structure</span></span>](the-formatetc-structure.md)
-   [<span data-ttu-id="b44aa-118">La structure STGMEDIUM</span><span class="sxs-lookup"><span data-stu-id="b44aa-118">The STGMEDIUM Structure</span></span>](the-stgmedium-structure.md)

## <a name="related-topics"></a><span data-ttu-id="b44aa-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b44aa-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b44aa-120">Transfert de données</span><span class="sxs-lookup"><span data-stu-id="b44aa-120">Data Transfer</span></span>](data-transfer.md)
</dt> </dl>

 

 




