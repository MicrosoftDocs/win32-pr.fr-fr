---
title: Magasins en ligne privés
description: Magasins en ligne privés
ms.assetid: c1e241f5-6d29-4b53-8be0-264597e03de7
keywords:
- Windows Media Player Online stores, privé
- magasins en ligne, privés
- tapez 1 magasins en ligne, privés
- tapez 2 magasins en ligne, privés
- magasins en ligne privés
- Registre, magasins en ligne privés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e11490a8a12659dfc1e2c5445167e8d71abaf00
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380129"
---
# <a name="private-online-stores"></a><span data-ttu-id="86f2c-109">Magasins en ligne privés</span><span class="sxs-lookup"><span data-stu-id="86f2c-109">Private Online Stores</span></span>

<span data-ttu-id="86f2c-110">Le lecteur Windows Media 10 ou version ultérieure prend en charge les magasins en ligne privés. autrement dit, les magasins qui sont visibles uniquement pour certains utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="86f2c-110">Windows Media Player 10 or later supports private online stores; that is, stores that are visible only to certain users.</span></span> <span data-ttu-id="86f2c-111">Pour qu’un magasin en ligne privé soit visible par l’utilisateur actuel, il doit y avoir une entrée qui représente la Banque en ligne privée sous la clé de Registre suivante.</span><span class="sxs-lookup"><span data-stu-id="86f2c-111">For a private online store to be visible to the current user, there must be an entry that represents the private online store under the following registry key.</span></span>

<span data-ttu-id="86f2c-112">HKEY \_ \_ logiciel utilisateur \\ actuel \\ Microsoft \\ MediaPlayer \\ PrivateServices</span><span class="sxs-lookup"><span data-stu-id="86f2c-112">HKEY\_CURRENT\_USER\\Software\\Microsoft\\MediaPlayer\\PrivateServices</span></span>

<span data-ttu-id="86f2c-113">L’entrée de registre requise doit avoir le format suivant.</span><span class="sxs-lookup"><span data-stu-id="86f2c-113">The required registry entry must have the following format.</span></span>



| <span data-ttu-id="86f2c-114">Nom</span><span class="sxs-lookup"><span data-stu-id="86f2c-114">Name</span></span>                                                         | <span data-ttu-id="86f2c-115">Type</span><span class="sxs-lookup"><span data-stu-id="86f2c-115">Type</span></span>           | <span data-ttu-id="86f2c-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="86f2c-116">Value</span></span>                                                                     |
|--------------------------------------------------------------|----------------|---------------------------------------------------------------------------|
| <span data-ttu-id="86f2c-117">Tout nom choisi par la personne qui crée l’entrée de Registre</span><span class="sxs-lookup"><span data-stu-id="86f2c-117">Any name chosen by the person who creates the registry entry</span></span> | <span data-ttu-id="86f2c-118">**\_valeur DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="86f2c-118">**REG\_DWORD**</span></span> | <span data-ttu-id="86f2c-119">Nombre, fourni par Microsoft, qui identifie le magasin en ligne privé</span><span class="sxs-lookup"><span data-stu-id="86f2c-119">A number, provided by Microsoft, that identifies the private online store</span></span> |



 

<span data-ttu-id="86f2c-120">Le contrôle ActiveX du lecteur Windows Media 10 prend en charge les magasins en ligne privés uniquement si le contrôle s’exécute en mode distant.</span><span class="sxs-lookup"><span data-stu-id="86f2c-120">The Windows Media Player 10 ActiveX control supports private online stores only if the control is running in remote mode.</span></span> <span data-ttu-id="86f2c-121">Le contrôle ActiveX du lecteur Windows Media 11 prend en charge les magasins en ligne privés, que le contrôle s’exécute en mode distant ou non.</span><span class="sxs-lookup"><span data-stu-id="86f2c-121">The Windows Media Player 11 ActiveX control supports private online stores regardless of whether the control is running in remote mode.</span></span>

## <a name="related-topics"></a><span data-ttu-id="86f2c-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="86f2c-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="86f2c-123">**Informations communes aux magasins en ligne de type 1 et de type 2**</span><span class="sxs-lookup"><span data-stu-id="86f2c-123">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> </dl>

 

 




