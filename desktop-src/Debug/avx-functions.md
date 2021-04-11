---
description: Fonctions Intel AVX.
ms.assetid: 237f356a-9ee8-4c52-b08c-a6695c52713a
title: AVX, fonctions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b0b56c83b6beb674bc284b139bb656441956705
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104200861"
---
# <a name="avx-functions"></a><span data-ttu-id="3bca1-103">AVX, fonctions</span><span class="sxs-lookup"><span data-stu-id="3bca1-103">AVX Functions</span></span>

<span data-ttu-id="3bca1-104">Les fonctions Intel AVX sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="3bca1-104">The following are the Intel AVX functions.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="3bca1-105">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="3bca1-105">In this section</span></span>



| <span data-ttu-id="3bca1-106">Rubrique</span><span class="sxs-lookup"><span data-stu-id="3bca1-106">Topic</span></span>                                                                   | <span data-ttu-id="3bca1-107">Description</span><span class="sxs-lookup"><span data-stu-id="3bca1-107">Description</span></span>                                                                                                                    |
|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3bca1-108">**CopyContext**</span><span class="sxs-lookup"><span data-stu-id="3bca1-108">**CopyContext**</span></span>](/windows/desktop/api/WinBase/nf-winbase-copycontext)<br/>                           | <span data-ttu-id="3bca1-109">Copie une structure de contexte source (y compris les XState) dans une structure de contexte de destination initialisée.</span><span class="sxs-lookup"><span data-stu-id="3bca1-109">Copies a source context structure (including any XState) onto an initialized destination context structure.</span></span><br/>         |
| [<span data-ttu-id="3bca1-110">**GetEnabledXStateFeatures**</span><span class="sxs-lookup"><span data-stu-id="3bca1-110">**GetEnabledXStateFeatures**</span></span>](/windows/desktop/api/WinBase/nf-winbase-getenabledxstatefeatures)<br/> | <span data-ttu-id="3bca1-111">Obtient un masque de fonctionnalités XState activées sur des processeurs x86 ou x64.</span><span class="sxs-lookup"><span data-stu-id="3bca1-111">Gets a mask of enabled XState features on x86 or x64 processors.</span></span><br/>                                                    |
| [<span data-ttu-id="3bca1-112">**GetXStateFeaturesMask**</span><span class="sxs-lookup"><span data-stu-id="3bca1-112">**GetXStateFeaturesMask**</span></span>](/windows/desktop/api/WinBase/nf-winbase-getxstatefeaturesmask)<br/>       | <span data-ttu-id="3bca1-113">Retourne le masque des fonctionnalités XState définies dans une structure de [**contexte**](/windows/desktop/api/WinNT/ns-winnt-wow64_context) .</span><span class="sxs-lookup"><span data-stu-id="3bca1-113">Returns the mask of XState features set within a [**CONTEXT**](/windows/desktop/api/WinNT/ns-winnt-wow64_context) structure.</span></span><br/>                        |
| [<span data-ttu-id="3bca1-114">**InitializeContext**</span><span class="sxs-lookup"><span data-stu-id="3bca1-114">**InitializeContext**</span></span>](/windows/desktop/api/WinBase/nf-winbase-initializecontext)<br/>               | <span data-ttu-id="3bca1-115">Initialise une structure de [**contexte**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context) à l’intérieur d’une mémoire tampon avec la taille et l’alignement nécessaires.</span><span class="sxs-lookup"><span data-stu-id="3bca1-115">Initializes a [**CONTEXT**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context) structure inside a buffer with the necessary size and alignment.</span></span><br/>       |
| [<span data-ttu-id="3bca1-116">**LocateXStateFeature**</span><span class="sxs-lookup"><span data-stu-id="3bca1-116">**LocateXStateFeature**</span></span>](/windows/desktop/api/WinBase/nf-winbase-locatexstatefeature)<br/>           | <span data-ttu-id="3bca1-117">Récupère un pointeur vers l’état du processeur pour une fonctionnalité XState dans une structure de [**contexte**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context) .</span><span class="sxs-lookup"><span data-stu-id="3bca1-117">Retrieves a pointer to the processor state for an XState feature within a [**CONTEXT**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context) structure.</span></span><br/> |
| [<span data-ttu-id="3bca1-118">**SetXStateFeaturesMask**</span><span class="sxs-lookup"><span data-stu-id="3bca1-118">**SetXStateFeaturesMask**</span></span>](/windows/desktop/api/WinBase/nf-winbase-setxstatefeaturesmask)<br/>       | <span data-ttu-id="3bca1-119">Définit le masque des fonctionnalités XState définies dans une structure de [**contexte**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context) .</span><span class="sxs-lookup"><span data-stu-id="3bca1-119">Sets the mask of XState features set within a [**CONTEXT**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context) structure.</span></span><br/>                             |



 

 

 




