---
title: Fonctions d’informations de routeur
description: Utilisez les fonctions suivantes pour manipuler les en-têtes et les blocs d’informations de routeur. Un en-tête d’information est composé de métadonnées privées et de blocs d’informations. Les blocs d’informations sont des tableaux de structures d’informations de différents types.
ms.assetid: e88720aa-080b-4d87-a442-1b436c256ca6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f694d2dcd140d8af8950fa7a2a4ae5049a679ff8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028479"
---
# <a name="router-information-functions"></a><span data-ttu-id="0946e-105">Fonctions d’informations de routeur</span><span class="sxs-lookup"><span data-stu-id="0946e-105">Router Information Functions</span></span>

<span data-ttu-id="0946e-106">Utilisez les fonctions suivantes pour manipuler les en-têtes et les blocs d’informations de routeur.</span><span class="sxs-lookup"><span data-stu-id="0946e-106">Use the following functions to manipulate router information headers and blocks.</span></span> <span data-ttu-id="0946e-107">Un en-tête d’information est composé de métadonnées privées et de blocs d’informations.</span><span class="sxs-lookup"><span data-stu-id="0946e-107">An information header is composed of private meta-data and information blocks.</span></span> <span data-ttu-id="0946e-108">Les blocs d’informations sont des tableaux de [structures d’informations](router-information-structures.md) de différents [types](router-information-enumerations.md).</span><span class="sxs-lookup"><span data-stu-id="0946e-108">Information blocks are arrays of [information structures](router-information-structures.md) of various [types](router-information-enumerations.md).</span></span>

<span data-ttu-id="0946e-109">Les fonctions suivantes permettent de manipuler les en-têtes d’informations :</span><span class="sxs-lookup"><span data-stu-id="0946e-109">The following functions manipulate information headers:</span></span>

-   [<span data-ttu-id="0946e-110">**MprInfoCreate**</span><span class="sxs-lookup"><span data-stu-id="0946e-110">**MprInfoCreate**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprinfocreate)
-   [<span data-ttu-id="0946e-111">**MprInfoDelete**</span><span class="sxs-lookup"><span data-stu-id="0946e-111">**MprInfoDelete**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprinfodelete)
-   [<span data-ttu-id="0946e-112">**MprInfoDuplicate**</span><span class="sxs-lookup"><span data-stu-id="0946e-112">**MprInfoDuplicate**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoduplicate)
-   [<span data-ttu-id="0946e-113">**MprInfoRemoveAll**</span><span class="sxs-lookup"><span data-stu-id="0946e-113">**MprInfoRemoveAll**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprinforemoveall)

<span data-ttu-id="0946e-114">Les fonctions suivantes manipulent des blocs d’informations dans un en-tête d’information :</span><span class="sxs-lookup"><span data-stu-id="0946e-114">The following functions manipulate information blocks within an information header:</span></span>

-   [<span data-ttu-id="0946e-115">**MprInfoBlockAdd**</span><span class="sxs-lookup"><span data-stu-id="0946e-115">**MprInfoBlockAdd**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockadd)
-   [<span data-ttu-id="0946e-116">**MprInfoBlockFind**</span><span class="sxs-lookup"><span data-stu-id="0946e-116">**MprInfoBlockFind**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockfind)
-   [<span data-ttu-id="0946e-117">**MprInfoBlockQuerySize**</span><span class="sxs-lookup"><span data-stu-id="0946e-117">**MprInfoBlockQuerySize**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockquerysize)
-   [<span data-ttu-id="0946e-118">**MprInfoBlockRemove**</span><span class="sxs-lookup"><span data-stu-id="0946e-118">**MprInfoBlockRemove**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockremove)
-   [<span data-ttu-id="0946e-119">**MprInfoBlockSet**</span><span class="sxs-lookup"><span data-stu-id="0946e-119">**MprInfoBlockSet**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockset)

<span data-ttu-id="0946e-120">La plupart des [fonctions d’administration et de configuration de routeur](understanding-mprinfo-functions-and-information-headers.md) utilisent des en-têtes d’informations.</span><span class="sxs-lookup"><span data-stu-id="0946e-120">Many of the [router administration and configuration functions](understanding-mprinfo-functions-and-information-headers.md) use information headers.</span></span>

 

 




