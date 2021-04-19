---
title: CENUMNS. COTISATIONS
description: Dans l’exemple de composant fournisseur, l’énumération d’un objet Namespace utilise les méthodes de cenumns. cpp, listées dans le tableau suivant.
ms.assetid: 52e23977-8df6-44a4-9a5e-a7896471c17e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0a8bc745535014a346e8042c577d14222302679
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "106518035"
---
# <a name="cenumnscpp"></a><span data-ttu-id="7f97a-103">CENUMNS. COTISATIONS</span><span class="sxs-lookup"><span data-stu-id="7f97a-103">CENUMNS.CPP</span></span>

<span data-ttu-id="7f97a-104">Dans l’exemple de composant fournisseur, l’énumération d’un objet Namespace utilise les méthodes de cenumns. cpp, listées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="7f97a-104">In the example provider component, the enumeration of a namespace object uses the methods, from cenumns.cpp, listed in the following table.</span></span>



| <span data-ttu-id="7f97a-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="7f97a-105">Method</span></span>                                              | <span data-ttu-id="7f97a-106">Description</span><span class="sxs-lookup"><span data-stu-id="7f97a-106">Description</span></span>                                                                                                                                               |
|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f97a-107">**CSampleDSNamespaceEnum :: Create**</span><span class="sxs-lookup"><span data-stu-id="7f97a-107">**CSampleDSNamespaceEnum::Create**</span></span>                  | <span data-ttu-id="7f97a-108">Créez un objet pour permettre l’énumération d’un objet d’espace de noms ADS.</span><span class="sxs-lookup"><span data-stu-id="7f97a-108">Create an object to allow enumeration of an ADS namespace object.</span></span>                                                                                         |
| <span data-ttu-id="7f97a-109">**CSampleDSNamespaceEnum::CSampleDSNamespaceEnum**</span><span class="sxs-lookup"><span data-stu-id="7f97a-109">**CSampleDSNamespaceEnum::CSampleDSNamespaceEnum**</span></span>  | <span data-ttu-id="7f97a-110">Constructeur standard.</span><span class="sxs-lookup"><span data-stu-id="7f97a-110">Standard constructor.</span></span>                                                                                                                                     |
| <span data-ttu-id="7f97a-111">**CSampleDSNamespaceEnum :: ~ CSampleDSNamespaceEnum**</span><span class="sxs-lookup"><span data-stu-id="7f97a-111">**CSampleDSNamespaceEnum::~CSampleDSNamespaceEnum**</span></span> | <span data-ttu-id="7f97a-112">Destructeur standard.</span><span class="sxs-lookup"><span data-stu-id="7f97a-112">Standard destructor.</span></span>                                                                                                                                      |
| <span data-ttu-id="7f97a-113">**CSampleDSNamespaceEnum :: suivant**</span><span class="sxs-lookup"><span data-stu-id="7f97a-113">**CSampleDSNamespaceEnum::Next**</span></span>                    | <span data-ttu-id="7f97a-114">Récupère le nombre spécifié d’éléments de l’objet d’espace de noms indiqué.</span><span class="sxs-lookup"><span data-stu-id="7f97a-114">Retrieve the specified number of elements from the namespace object indicated.</span></span>                                                                            |
| <span data-ttu-id="7f97a-115">**CSampleDSNamespaceEnum :: EnumObjects**</span><span class="sxs-lookup"><span data-stu-id="7f97a-115">**CSampleDSNamespaceEnum::EnumObjects**</span></span>             | <span data-ttu-id="7f97a-116">Gérer la récupération des pointeurs d’interface aux objets.</span><span class="sxs-lookup"><span data-stu-id="7f97a-116">Manage retrieving the interface pointers to the objects.</span></span>                                                                                                  |
| <span data-ttu-id="7f97a-117">**CSampleDSNamespaceEnum::FetchObjects**</span><span class="sxs-lookup"><span data-stu-id="7f97a-117">**CSampleDSNamespaceEnum::FetchObjects**</span></span>            | <span data-ttu-id="7f97a-118">Récupérez l’ensemble de pointeurs [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="7f97a-118">Fetch the set of [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) pointers.</span></span>                                                                          |
| <span data-ttu-id="7f97a-119">**CSampleDSNamespaceEnum::FetchNextObject**</span><span class="sxs-lookup"><span data-stu-id="7f97a-119">**CSampleDSNamespaceEnum::FetchNextObject**</span></span>         | <span data-ttu-id="7f97a-120">Extrait l’objet suivant.</span><span class="sxs-lookup"><span data-stu-id="7f97a-120">Fetch the next object.</span></span> <span data-ttu-id="7f97a-121">S’il est trouvé, créez un objet Active Directory générique et récupérez son pointeur [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="7f97a-121">If found, create a generic Active Directory object and retrieve its [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) pointer.</span></span> |



 

 

 