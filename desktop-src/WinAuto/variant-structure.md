---
title: Structure de variante
description: La plupart des fonctions de Active Accessibility Microsoft et les propriétés et méthodes IAccessible prennent une structure de variante comme paramètre. Fondamentalement, la structure VARIANT est un conteneur pour une grande Union qui transporte de nombreux types de données.
ms.assetid: 774dfac8-e258-4266-b81e-072eb3961fb1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cafc63388de27ae01b3e1ca478add6802ac6b85c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101869"
---
# <a name="variant-structure"></a><span data-ttu-id="f2b93-104">Structure de variante</span><span class="sxs-lookup"><span data-stu-id="f2b93-104">VARIANT Structure</span></span>

<span data-ttu-id="f2b93-105">La plupart des fonctions de Active Accessibility Microsoft et les propriétés et méthodes [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) prennent une structure de [**variante**](/windows/win32/api/oaidl/ns-oaidl-variant) comme paramètre.</span><span class="sxs-lookup"><span data-stu-id="f2b93-105">Most of the Microsoft Active Accessibility functions and the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties and methods take a [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) structure as a parameter.</span></span> <span data-ttu-id="f2b93-106">Fondamentalement, la structure **Variant** est un conteneur pour une grande Union qui transporte de nombreux types de données.</span><span class="sxs-lookup"><span data-stu-id="f2b93-106">Essentially, the **VARIANT** structure is a container for a large union that carries many types of data.</span></span>

<span data-ttu-id="f2b93-107">La valeur du premier membre de la structure, **VT**, décrit les membres de l’Union qui sont valides.</span><span class="sxs-lookup"><span data-stu-id="f2b93-107">The value in the first member of the structure, **vt**, describes which of the union members is valid.</span></span> <span data-ttu-id="f2b93-108">Bien que la structure [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) prenne en charge de nombreux types de données différents, Microsoft Active Accessibility utilise uniquement les types suivants.</span><span class="sxs-lookup"><span data-stu-id="f2b93-108">Although the [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) structure supports many different data types, Microsoft Active Accessibility uses only the following types.</span></span>



| <span data-ttu-id="f2b93-109">Valeur VT</span><span class="sxs-lookup"><span data-stu-id="f2b93-109">vt Value</span></span>     | <span data-ttu-id="f2b93-110">Nom du membre de valeur correspondant</span><span class="sxs-lookup"><span data-stu-id="f2b93-110">Corresponding value member name</span></span> |
|--------------|---------------------------------|
| <span data-ttu-id="f2b93-111">VT \_</span><span class="sxs-lookup"><span data-stu-id="f2b93-111">VT\_I4</span></span>       | <span data-ttu-id="f2b93-112">**lVal**</span><span class="sxs-lookup"><span data-stu-id="f2b93-112">**lVal**</span></span>                        |
| <span data-ttu-id="f2b93-113">\_distribution vt</span><span class="sxs-lookup"><span data-stu-id="f2b93-113">VT\_DISPATCH</span></span> | <span data-ttu-id="f2b93-114">**pdispVal**</span><span class="sxs-lookup"><span data-stu-id="f2b93-114">**pdispVal**</span></span>                    |
| <span data-ttu-id="f2b93-115">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="f2b93-115">VT\_BSTR</span></span>     | <span data-ttu-id="f2b93-116">**bstrVal**</span><span class="sxs-lookup"><span data-stu-id="f2b93-116">**bstrVal**</span></span>                     |
| <span data-ttu-id="f2b93-117">VT \_ vide</span><span class="sxs-lookup"><span data-stu-id="f2b93-117">VT\_EMPTY</span></span>    | <span data-ttu-id="f2b93-118">aucun</span><span class="sxs-lookup"><span data-stu-id="f2b93-118">none</span></span>                            |



 

<span data-ttu-id="f2b93-119">Lorsque vous recevez des informations dans une structure de [**variante**](/windows/win32/api/oaidl/ns-oaidl-variant) , vérifiez le membre **VT** pour savoir quel membre contient des données valides.</span><span class="sxs-lookup"><span data-stu-id="f2b93-119">When you receive information in a [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) structure, check the **vt** member to find out which member contains valid data.</span></span> <span data-ttu-id="f2b93-120">De même, lorsque vous envoyez des informations à l’aide d’une structure **Variant** , définissez toujours **VT** pour refléter le membre d’Union qui contient les informations.</span><span class="sxs-lookup"><span data-stu-id="f2b93-120">Similarly, when you send information using a **VARIANT** structure, always set **vt** to reflect the union member that contains the information.</span></span>

<span data-ttu-id="f2b93-121">Avant d’utiliser la structure, initialisez-la en appelant la fonction COM (Component Object Model) [**VariantInit**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantinit) .</span><span class="sxs-lookup"><span data-stu-id="f2b93-121">Before using the structure, initialize it by calling the [**VariantInit**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantinit) Component Object Model (COM) function.</span></span> <span data-ttu-id="f2b93-122">Lorsque vous avez terminé avec la structure, effacez-la avant de libérer la mémoire qui contient la [**variante**](/windows/win32/api/oaidl/ns-oaidl-variant) en appelant [**VariantClear**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantclear).</span><span class="sxs-lookup"><span data-stu-id="f2b93-122">When finished with the structure, clear it before the memory that contains the [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) is freed by calling [**VariantClear**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantclear).</span></span>

 

 