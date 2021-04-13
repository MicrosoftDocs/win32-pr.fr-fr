---
title: CENUMVAR. COTISATIONS
description: Dans l’exemple de composant fournisseur, l’implémentation de base pour les classes dérivées xxxEnumVariant se trouve dans cenumvar. cpp. Les méthodes associées sont répertoriées dans le tableau suivant.
ms.assetid: 6b38bc99-25d4-40af-863a-9cc37f786d9b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d361cb7d3e2657a31645fba05aa2e1a23762a3fc
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104316439"
---
# <a name="cenumvarcpp"></a><span data-ttu-id="61937-104">CENUMVAR. COTISATIONS</span><span class="sxs-lookup"><span data-stu-id="61937-104">CENUMVAR.CPP</span></span>

<span data-ttu-id="61937-105">Dans l’exemple de composant fournisseur, l’implémentation de base pour les classes dérivées xxxEnumVariant se trouve dans cenumvar. cpp.</span><span class="sxs-lookup"><span data-stu-id="61937-105">In the example provider component, the base implementation for xxxEnumVariant derived classes can be found in cenumvar.cpp.</span></span> <span data-ttu-id="61937-106">Les méthodes associées sont répertoriées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="61937-106">Associated methods are listed in the following table.</span></span>



| <span data-ttu-id="61937-107">Méthode</span><span class="sxs-lookup"><span data-stu-id="61937-107">Method</span></span>                                          | <span data-ttu-id="61937-108">Description</span><span class="sxs-lookup"><span data-stu-id="61937-108">Description</span></span>                                                                           |
|-------------------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="61937-109">**CSampleDSEnumVariant::CSampleDSEnumVariant**</span><span class="sxs-lookup"><span data-stu-id="61937-109">**CSampleDSEnumVariant::CSampleDSEnumVariant**</span></span>  | <span data-ttu-id="61937-110">Constructeur standard.</span><span class="sxs-lookup"><span data-stu-id="61937-110">Standard constructor.</span></span>                                                                 |
| <span data-ttu-id="61937-111">**CSampleDSEnumVariant :: ~ CSampleDSEnumVariant**</span><span class="sxs-lookup"><span data-stu-id="61937-111">**CSampleDSEnumVariant::~CSampleDSEnumVariant**</span></span> | <span data-ttu-id="61937-112">Destructeur standard.</span><span class="sxs-lookup"><span data-stu-id="61937-112">Standard destructor.</span></span>                                                                  |
| <span data-ttu-id="61937-113">**CSampleDSEnumVariant :: QueryInterface**</span><span class="sxs-lookup"><span data-stu-id="61937-113">**CSampleDSEnumVariant::QueryInterface**</span></span>        | <span data-ttu-id="61937-114">Implémentation de [**IUnknown :: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) standard.</span><span class="sxs-lookup"><span data-stu-id="61937-114">Standard [**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) implementation.</span></span> |
| <span data-ttu-id="61937-115">**CSampleDSEnumVariant :: AddRef**</span><span class="sxs-lookup"><span data-stu-id="61937-115">**CSampleDSEnumVariant::AddRef**</span></span>                | <span data-ttu-id="61937-116">Implémentation de [**IUnknown :: AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) standard.</span><span class="sxs-lookup"><span data-stu-id="61937-116">Standard [**IUnknown::AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) implementation.</span></span>                 |
| <span data-ttu-id="61937-117">**CSampleDSEnumVariant :: Release**</span><span class="sxs-lookup"><span data-stu-id="61937-117">**CSampleDSEnumVariant::Release**</span></span>               | <span data-ttu-id="61937-118">Implémentation de [**IUnknown :: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) standard.</span><span class="sxs-lookup"><span data-stu-id="61937-118">Standard [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) implementation.</span></span>               |
| <span data-ttu-id="61937-119">**CSampleDSEnumVariant :: Skip**</span><span class="sxs-lookup"><span data-stu-id="61937-119">**CSampleDSEnumVariant::Skip**</span></span>                  | <span data-ttu-id="61937-120">Implémentation standard de **IEnumXXXX :: Skip** .</span><span class="sxs-lookup"><span data-stu-id="61937-120">Standard **IEnumXXXX::Skip** implementation.</span></span>                                          |
| <span data-ttu-id="61937-121">**CSampleDSEnumVariant :: Reset**</span><span class="sxs-lookup"><span data-stu-id="61937-121">**CSampleDSEnumVariant::Reset**</span></span>                 | <span data-ttu-id="61937-122">Implémentation standard de **IEnumXXXX :: Reset** .</span><span class="sxs-lookup"><span data-stu-id="61937-122">Standard **IEnumXXXX::Reset** implementation.</span></span>                                         |
| <span data-ttu-id="61937-123">**CSampleDSEnumVariant :: Clone**</span><span class="sxs-lookup"><span data-stu-id="61937-123">**CSampleDSEnumVariant::Clone**</span></span>                 | <span data-ttu-id="61937-124">Implémentation standard de **IEnumXXXX :: Clone** .</span><span class="sxs-lookup"><span data-stu-id="61937-124">Standard **IEnumXXXX::Clone** implementation.</span></span>                                         |



 

 

 