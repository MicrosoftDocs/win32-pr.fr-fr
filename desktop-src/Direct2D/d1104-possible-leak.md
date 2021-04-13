---
title: Fuite de D1104 possible
ms.assetid: 564de2e2-5004-43e8-8616-1ab11127738a
description: La fabrique a été libérée mais l’interface créée à partir de celle-ci est toujours active. Bien qu’il soit possible de libérer des ressources après avoir libéré la fabrique, cette condition peut indiquer une fuite de mémoire.
keywords:
- D1104 de fuite possible
topic_type:
- apiref
api_name:
- D1104 Possible Leak
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 71ccbee152d60a73fbea5ebac2a1074534b69c3a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312196"
---
# <a name="d1104-possible-leak"></a><span data-ttu-id="2434d-105">D1104 : fuite possible</span><span class="sxs-lookup"><span data-stu-id="2434d-105">D1104: Possible Leak</span></span>

<span data-ttu-id="2434d-106">La \[ *fabrique* \] de fabrique a été libérée mais l' \[ *interface* \] d’interface créée à partir de celle-ci est toujours active.</span><span class="sxs-lookup"><span data-stu-id="2434d-106">The factory \[*factory*\] was released but the interface \[*interface*\] created from it is still alive.</span></span> <span data-ttu-id="2434d-107">Bien qu’il soit possible de libérer des ressources après avoir libéré la fabrique, cette condition peut indiquer une fuite de mémoire.</span><span class="sxs-lookup"><span data-stu-id="2434d-107">While it is valid to release resources after releasing the factory, this condition could be indicative of a memory leak.</span></span>

## <a name="placeholders"></a><span data-ttu-id="2434d-108">Espaces réservés</span><span class="sxs-lookup"><span data-stu-id="2434d-108">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="2434d-109"><span id="factory"></span><span id="FACTORY"></span>*fabrique*</span><span class="sxs-lookup"><span data-stu-id="2434d-109"><span id="factory"></span><span id="FACTORY"></span>*factory*</span></span>
</dt> <dd>

<span data-ttu-id="2434d-110">Adresse de la fabrique qui a été libérée.</span><span class="sxs-lookup"><span data-stu-id="2434d-110">The address of the factory that was released.</span></span>

</dd> <dt>

<span data-ttu-id="2434d-111"><span id="interface"></span><span id="INTERFACE"></span>*interface*</span><span class="sxs-lookup"><span data-stu-id="2434d-111"><span id="interface"></span><span id="INTERFACE"></span>*interface*</span></span>
</dt> <dd>

<span data-ttu-id="2434d-112">Adresse de l’interface qui a été créée sur la *fabrique*.</span><span class="sxs-lookup"><span data-stu-id="2434d-112">The address of the interface that was created on the *factory*.</span></span>

</dd> </dl> 

|             |             |
|-------------|-------------|
| <span data-ttu-id="2434d-113">Niveau d’erreur</span><span class="sxs-lookup"><span data-stu-id="2434d-113">Error Level</span></span> | <span data-ttu-id="2434d-114">Information</span><span class="sxs-lookup"><span data-stu-id="2434d-114">Information</span></span> |



 

## <a name="possible-causes"></a><span data-ttu-id="2434d-115">Causes possibles</span><span class="sxs-lookup"><span data-stu-id="2434d-115">Possible Causes</span></span>

<span data-ttu-id="2434d-116">La fabrique a été libérée mais l’interface créée à partir de celle-ci est toujours active.</span><span class="sxs-lookup"><span data-stu-id="2434d-116">The factory was released but the interface created from it is still alive.</span></span>

 

 




