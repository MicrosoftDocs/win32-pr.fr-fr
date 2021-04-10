---
title: Comment les serveurs implémentent des ID enfants
description: Les développeurs de serveurs peuvent assigner des ID enfants à des éléments simples et à des objets accessibles. Toutefois, l’approche recommandée consiste à prendre en charge l’interface COM (Component Object Model) standard IEnumVARIANT dans chaque objet accessible qui a des enfants.
ms.assetid: 236de46e-8fe0-4f53-b989-267c9ee87545
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0721c9660aa02fb16e9ec33495279cd90e872a37
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941163"
---
# <a name="how-servers-implement-child-ids"></a><span data-ttu-id="7e9cd-104">Comment les serveurs implémentent des ID enfants</span><span class="sxs-lookup"><span data-stu-id="7e9cd-104">How Servers Implement Child IDs</span></span>

<span data-ttu-id="7e9cd-105">Les développeurs de serveurs peuvent assigner des ID enfants à des éléments simples et à des objets accessibles.</span><span class="sxs-lookup"><span data-stu-id="7e9cd-105">Server developers can assign child IDs to both simple elements and accessible objects.</span></span> <span data-ttu-id="7e9cd-106">Toutefois, l’approche recommandée consiste à prendre en charge l’interface COM (Component Object Model) standard [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) dans chaque objet accessible qui a des enfants.</span><span class="sxs-lookup"><span data-stu-id="7e9cd-106">However, the recommended approach is to support the standard Component Object Model (COM) interface [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) in every accessible object that has children.</span></span>

<span data-ttu-id="7e9cd-107">Si vous implémentez [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant), vous devez :</span><span class="sxs-lookup"><span data-stu-id="7e9cd-107">If you implement [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant), you must:</span></span>

-   <span data-ttu-id="7e9cd-108">Énumérer tous les enfants, à la fois les éléments simples et les objets accessibles.</span><span class="sxs-lookup"><span data-stu-id="7e9cd-108">Enumerate all children, both simple elements and accessible objects.</span></span> <span data-ttu-id="7e9cd-109">Fournissez des ID enfants pour tous les éléments simples et fournissez le [**IDispatch**](idispatch-interface.md) à chaque objet accessible.</span><span class="sxs-lookup"><span data-stu-id="7e9cd-109">Provide child IDs for all simple elements and provide the [**IDispatch**](idispatch-interface.md) to each accessible object.</span></span>
-   <span data-ttu-id="7e9cd-110">Pour les objets accessibles, définissez le membre **VT** du [**Variant**](variant-structure.md) sur VT \_ Dispatch.</span><span class="sxs-lookup"><span data-stu-id="7e9cd-110">For accessible objects, set the **vt** member of the [**VARIANT**](variant-structure.md) to VT\_DISPATCH.</span></span> <span data-ttu-id="7e9cd-111">Le membre **pdispVal** doit contenir un pointeur vers l’interface [**IDispatch**](idispatch-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="7e9cd-111">The **pdispVal** member must contain a pointer to the [**IDispatch**](idispatch-interface.md) interface.</span></span> <span data-ttu-id="7e9cd-112">Notez que le **Variant** est alloué et libéré par le client.</span><span class="sxs-lookup"><span data-stu-id="7e9cd-112">Note that the **VARIANT** is allocated and freed by the client.</span></span>
-   <span data-ttu-id="7e9cd-113">Pour les éléments simples, l’ID enfant est un entier positif de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="7e9cd-113">For simple elements, the child ID is any 32-bit positive integer.</span></span> <span data-ttu-id="7e9cd-114">Notez que les entiers nuls et négatifs sont réservés par Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="7e9cd-114">Note that zero and negative integers are reserved by Microsoft Active Accessibility.</span></span> <span data-ttu-id="7e9cd-115">Définissez le membre **VT** de la structure [**Variant**](variant-structure.md) sur VT \_ I4 et le membre **lVal** sur l’ID enfant.</span><span class="sxs-lookup"><span data-stu-id="7e9cd-115">Set the [**VARIANT**](variant-structure.md) structure **vt** member to VT\_I4 and the **lVal** member to the child ID.</span></span>

<span data-ttu-id="7e9cd-116">Si vous ne prenez pas en charge [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant), vous devez assigner des ID enfants et numéroter les enfants de chaque objet de manière séquentielle à partir de 1.</span><span class="sxs-lookup"><span data-stu-id="7e9cd-116">If you do not support [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant), you must assign child IDs and number the children in each object sequentially starting with one.</span></span>

<span data-ttu-id="7e9cd-117">Il est recommandé que les clients utilisent la fonction Microsoft Active Accessibility Function [**AccessibleChildren**](/windows/desktop/api/Oleacc/nf-oleacc-accessiblechildren) au lieu d’appeler directement l’interface Server [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) .</span><span class="sxs-lookup"><span data-stu-id="7e9cd-117">It is recommended that clients use the Microsoft Active Accessibility function [**AccessibleChildren**](/windows/desktop/api/Oleacc/nf-oleacc-accessiblechildren) rather than call the server [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface directly.</span></span>

 

 