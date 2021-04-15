---
title: CNAMESP. COTISATIONS
description: Dans l’exemple de composant fournisseur, le code qui gère la durée de vie de l’exemple d’objet espace de noms du composant fournisseur se trouve dans cnamesp. cpp. Les méthodes prises en charge sont répertoriées dans le tableau suivant.
ms.assetid: 2f570f87-d8c3-42b1-b8b9-758905bf4b86
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8204c953218692d91c52fb77d757b5e917264a4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507035"
---
# <a name="cnamespcpp"></a><span data-ttu-id="aec09-104">CNAMESP. COTISATIONS</span><span class="sxs-lookup"><span data-stu-id="aec09-104">CNAMESP.CPP</span></span>

<span data-ttu-id="aec09-105">Dans l’exemple de composant fournisseur, le code qui gère la durée de vie de l’exemple d’objet espace de noms du composant fournisseur se trouve dans cnamesp. cpp.</span><span class="sxs-lookup"><span data-stu-id="aec09-105">In the example provider component, code that manages the lifetime of the example provider component namespace object is in cnamesp.cpp.</span></span> <span data-ttu-id="aec09-106">Les méthodes prises en charge sont répertoriées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="aec09-106">Supported methods are listed in the following table.</span></span>



| <span data-ttu-id="aec09-107">Méthode</span><span class="sxs-lookup"><span data-stu-id="aec09-107">Method</span></span>                                                   | <span data-ttu-id="aec09-108">Description</span><span class="sxs-lookup"><span data-stu-id="aec09-108">Description</span></span>                                            |
|----------------------------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="aec09-109">**CSampleDSNamespace::CSampleDSNamespace**</span><span class="sxs-lookup"><span data-stu-id="aec09-109">**CSampleDSNamespace::CSampleDSNamespace**</span></span>               | <span data-ttu-id="aec09-110">Constructeur standard.</span><span class="sxs-lookup"><span data-stu-id="aec09-110">Standard constructor.</span></span>                                  |
| <span data-ttu-id="aec09-111">**CSampleDSNamespace :: ~ CSampleDSNamespace**</span><span class="sxs-lookup"><span data-stu-id="aec09-111">**CSampleDSNamespace::~CSampleDSNamespace**</span></span>              | <span data-ttu-id="aec09-112">Destructeur standard.</span><span class="sxs-lookup"><span data-stu-id="aec09-112">Standard destructor.</span></span>                                   |
| <span data-ttu-id="aec09-113">Méthodes [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) standard.</span><span class="sxs-lookup"><span data-stu-id="aec09-113">Standard [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) methods.</span></span>                   |                                                        |
| <span data-ttu-id="aec09-114">Méthodes [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) standard.</span><span class="sxs-lookup"><span data-stu-id="aec09-114">Standard [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) methods.</span></span> |                                                        |
| <span data-ttu-id="aec09-115">**CSampleDSNamespace::AllocateNamespaceObject**</span><span class="sxs-lookup"><span data-stu-id="aec09-115">**CSampleDSNamespace::AllocateNamespaceObject**</span></span>          | <span data-ttu-id="aec09-116">Créez un objet Namespace et chargez ses données de type.</span><span class="sxs-lookup"><span data-stu-id="aec09-116">Create a namespace object and load its type data.</span></span>      |
| <span data-ttu-id="aec09-117">**CSampleDSNamespace::CreateNamespace**</span><span class="sxs-lookup"><span data-stu-id="aec09-117">**CSampleDSNamespace::CreateNamespace**</span></span>                  | <span data-ttu-id="aec09-118">Allouez, initialisez et validez un objet Namespace.</span><span class="sxs-lookup"><span data-stu-id="aec09-118">Allocate, initialize, and validate a namespace object.</span></span> |
| <span data-ttu-id="aec09-119">**CSampleDSNamespace :: QueryInterface**</span><span class="sxs-lookup"><span data-stu-id="aec09-119">**CSampleDSNamespace::QueryInterface**</span></span>                   | <span data-ttu-id="aec09-120">Vérifiez l’IID donné sur cet objet.</span><span class="sxs-lookup"><span data-stu-id="aec09-120">Verify the given IID on this object.</span></span>                   |



 

 

 




