---
title: Collections et groupes
description: ADSI utilise des objets de collection pour représenter tout ensemble arbitraire d’éléments dans un service d’annuaire qui peut être représenté à l’aide du même type de données.
ms.assetid: 03257cc9-f354-4e1c-8880-936a7acac3ef
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, utilisation de, collections et groupes
- ADSI de collections
- groupes ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9f0f4d699d8dde0c3d70c7449dfe146212b2b30
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103941351"
---
# <a name="collections-and-groups"></a><span data-ttu-id="1c9d1-106">Collections et groupes</span><span class="sxs-lookup"><span data-stu-id="1c9d1-106">Collections and Groups</span></span>

<span data-ttu-id="1c9d1-107">ADSI utilise des objets de collection pour représenter tout ensemble arbitraire d’éléments dans un service d’annuaire qui peut être représenté à l’aide du même type de données.</span><span class="sxs-lookup"><span data-stu-id="1c9d1-107">ADSI uses collection objects to represent any arbitrary set of items in a directory service that can be represented using the same data type.</span></span> <span data-ttu-id="1c9d1-108">Les objets de collection sont définis sous la forme d’un ensemble de valeurs **Variant** , représentant l’un des types de données Automation valides.</span><span class="sxs-lookup"><span data-stu-id="1c9d1-108">Collection objects are defined as a set of **VARIANT** values, representing any of the valid Automation data types.</span></span> <span data-ttu-id="1c9d1-109">Les objets de collection peuvent représenter des informations persistantes telles que les listes de contrôle d’accès et les informations volatiles telles que les travaux d’impression dans une file d’attente à l’impression.</span><span class="sxs-lookup"><span data-stu-id="1c9d1-109">Collection objects can represent both persistent information such as access-control lists and volatile information such as print jobs in a print queue.</span></span>

<span data-ttu-id="1c9d1-110">La Convention COM standard pour répertorier le contenu d’un objet collection (ou conteneur) consiste à créer un objet énumérateur qui prend en charge [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant), qui a des méthodes pour parcourir la liste d’objets de collection.</span><span class="sxs-lookup"><span data-stu-id="1c9d1-110">The standard COM convention for listing the contents of a collection (or container) object is to create an enumerator object that supports [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant), which has methods to step through the list of collection objects.</span></span> <span data-ttu-id="1c9d1-111">Les interfaces dans ADSI qui fournissent la méthode d’extraction de la méthode **\_ \_ NewEnum** (Notez les deux traits de soulignement) sont [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer), [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers) et [**IADsCollection**](/windows/desktop/api/Iads/nn-iads-iadscollection).</span><span class="sxs-lookup"><span data-stu-id="1c9d1-111">The interfaces in ADSI that supply the **get\_\_NewEnum** method (note the two underscores) are [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer), [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers) and [**IADsCollection**](/windows/desktop/api/Iads/nn-iads-iadscollection).</span></span> <span data-ttu-id="1c9d1-112">ADSI fournit également les fonctions d’assistance [**ADsBuildEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator) et [**ADsEnumerateNext**](/windows/desktop/api/Adshlp/nf-adshlp-adsenumeratenext) pour les programmes C et C++ afin de simplifier l’énumération.</span><span class="sxs-lookup"><span data-stu-id="1c9d1-112">ADSI also supplies the helper functions [**ADsBuildEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator) and [**ADsEnumerateNext**](/windows/desktop/api/Adshlp/nf-adshlp-adsenumeratenext) for C and C++ programs to simplify enumeration.</span></span> <span data-ttu-id="1c9d1-113">Les clients Automation utilisent implicitement l’énumération lorsqu’ils appellent **Next** dans une boucle **for** .</span><span class="sxs-lookup"><span data-stu-id="1c9d1-113">Automation clients use enumeration implicitly when they call **Next** in a **For** loop.</span></span>

<span data-ttu-id="1c9d1-114">Les groupes sont simplement des collections d’objets prenant en charge l’interface [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers) .</span><span class="sxs-lookup"><span data-stu-id="1c9d1-114">Groups are simply collections of objects supporting the [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers) interface.</span></span>

 

 