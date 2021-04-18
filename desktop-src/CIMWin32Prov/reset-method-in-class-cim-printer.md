---
description: La méthode de réinitialisation de la \_ classe d’imprimante CIM demande une réinitialisation de l’unité logique.
ms.assetid: 7d5c9e57-0f48-4a31-855d-d06197a9b5df
ms.tgt_platform: multiple
title: Méthode Reset de la classe CIM_Printer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Printer.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 42e4f4ff44eb1de7b0834239cf0d8af0ea88b42c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515921"
---
# <a name="reset-method-of-the-cim_printer-class"></a><span data-ttu-id="5f74c-103">Méthode de réinitialisation de la \_ classe d’imprimante CIM</span><span class="sxs-lookup"><span data-stu-id="5f74c-103">Reset method of the CIM\_Printer class</span></span>

<span data-ttu-id="5f74c-104">La méthode de **réinitialisation** de la \_ classe d’imprimante CIM demande une réinitialisation de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="5f74c-104">The **Reset** method of the CIM\_Printer class requests a reset of the logical device.</span></span> <span data-ttu-id="5f74c-105">Cette méthode est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="5f74c-105">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5f74c-106">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="5f74c-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="5f74c-107">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="5f74c-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="5f74c-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5f74c-108">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="5f74c-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5f74c-109">Parameters</span></span>

<span data-ttu-id="5f74c-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="5f74c-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5f74c-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5f74c-111">Return value</span></span>

<span data-ttu-id="5f74c-112">Retourne 0 (zéro) si la requête a été exécutée avec succès, 1 (un) si la demande n’est pas prise en charge, et une autre valeur si une erreur s’est produite.</span><span class="sxs-lookup"><span data-stu-id="5f74c-112">Returns 0 (zero) if the request was successfully executed, 1 (one) if the request is not supported, and some other value if an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f74c-113">Notes</span><span class="sxs-lookup"><span data-stu-id="5f74c-113">Remarks</span></span>

<span data-ttu-id="5f74c-114">Actuellement, cette méthode n’est pas implémentée par WMI.</span><span class="sxs-lookup"><span data-stu-id="5f74c-114">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="5f74c-115">Pour utiliser cette méthode, vous devez l’implémenter dans votre propre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="5f74c-115">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="5f74c-116">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="5f74c-116">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="5f74c-117">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="5f74c-117">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f74c-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5f74c-118">Requirements</span></span>



| <span data-ttu-id="5f74c-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5f74c-119">Requirement</span></span> | <span data-ttu-id="5f74c-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="5f74c-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5f74c-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5f74c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="5f74c-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5f74c-122">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5f74c-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5f74c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="5f74c-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5f74c-124">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5f74c-125">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="5f74c-125">Namespace</span></span><br/>                | <span data-ttu-id="5f74c-126">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="5f74c-126">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5f74c-127">MOF</span><span class="sxs-lookup"><span data-stu-id="5f74c-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5f74c-128"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5f74c-128"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5f74c-129">DLL</span><span class="sxs-lookup"><span data-stu-id="5f74c-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5f74c-130"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5f74c-130"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f74c-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5f74c-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f74c-132">\_Imprimante CIM</span><span class="sxs-lookup"><span data-stu-id="5f74c-132">CIM\_Printer</span></span>](reset-method-in-class-cim-printer.md)
</dt> <dt>

[<span data-ttu-id="5f74c-133">**\_Imprimante CIM**</span><span class="sxs-lookup"><span data-stu-id="5f74c-133">**CIM\_Printer**</span></span>](cim-printer.md)
</dt> </dl>

 

 




