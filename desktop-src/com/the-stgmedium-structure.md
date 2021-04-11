---
title: La structure STGMEDIUM
description: La structure STGMEDIUM
ms.assetid: ff1e1128-d228-45a6-a19d-2875b6c4e003
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86faf52ab93bab39b8413ea2eb6381da24b643b5
ms.sourcegitcommit: 89f99926f946dc6c5ea600fb7c41f6b19ceac516
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/21/2020
ms.locfileid: "104032074"
---
# <a name="the-stgmedium-structure"></a><span data-ttu-id="5a1e6-103">La structure STGMEDIUM</span><span class="sxs-lookup"><span data-stu-id="5a1e6-103">The STGMEDIUM Structure</span></span>

<span data-ttu-id="5a1e6-104">Tout comme la structure [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) est une amélioration de l’identificateur de format du presse-papiers Windows, la structure [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) est donc une amélioration du descripteur de mémoire globale utilisé pour transférer les données.</span><span class="sxs-lookup"><span data-stu-id="5a1e6-104">Just as the [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) structure is an enhancement of the Windows clipboard format identifier, so the [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) structure is an improvement of the global memory handle used to transfer the data.</span></span> <span data-ttu-id="5a1e6-105">La structure **STGMEDIUM** inclut un membre, **TYMED**, qui indique le support à utiliser, et une Union comprenant des pointeurs et un handle pour obtenir le support spécifié dans **TYMED**.</span><span class="sxs-lookup"><span data-stu-id="5a1e6-105">The **STGMEDIUM** structure includes a member, **tymed**, which indicates the medium to be used, and a union comprising pointers and a handle for getting whichever medium is specified in **tymed**.</span></span>

<span data-ttu-id="5a1e6-106">La structure [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) permet aux sources de données et aux consommateurs de choisir le support Exchange le plus efficace pour chaque rendu.</span><span class="sxs-lookup"><span data-stu-id="5a1e6-106">The [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) structure enables both data sources and consumers to choose the most efficient exchange medium on a per-rendering basis.</span></span> <span data-ttu-id="5a1e6-107">Si les données sont tellement volumineuses qu’elles doivent être conservées sur le disque, la source de données peut indiquer un support sur disque dans son format préféré, en utilisant uniquement la mémoire globale comme sauvegarde uniquement si c’est le seul moyen que le consommateur comprend.</span><span class="sxs-lookup"><span data-stu-id="5a1e6-107">If the data is so large that it should be kept on disk, the data source can indicate a disk-based medium in its preferred format, only using global memory as a backup if that's the only medium the consumer understands.</span></span> <span data-ttu-id="5a1e6-108">La possibilité d’utiliser le meilleur moyen pour les échanges comme par défaut améliore les performances globales d’échange de données entre les applications.</span><span class="sxs-lookup"><span data-stu-id="5a1e6-108">Being able to use the best medium for exchanges as the default improves overall performance of data exchange between applications.</span></span> <span data-ttu-id="5a1e6-109">Par exemple, si certaines des données à transférer sont déjà sur le disque, l’application source peut les déplacer ou les copier vers une nouvelle destination, soit dans la même application, soit dans d’autres, sans avoir à charger les données dans la mémoire globale.</span><span class="sxs-lookup"><span data-stu-id="5a1e6-109">For example, if some of the data to be transferred is already on disk, the source application can move or copy it to a new destination, either in the same application or in some other, without having first to load the data into global memory.</span></span> <span data-ttu-id="5a1e6-110">À l’extrémité de réception, le consommateur des données n’a pas à les réécrire sur le disque.</span><span class="sxs-lookup"><span data-stu-id="5a1e6-110">At the receiving end, the consumer of the data does not have to write it back to disk.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5a1e6-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5a1e6-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5a1e6-112">Formats de données et média de transfert</span><span class="sxs-lookup"><span data-stu-id="5a1e6-112">Data Formats and Transfer Media</span></span>](data-formats-and-transfer-media.md)
</dt> </dl>

 

 




