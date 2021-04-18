---
description: La méthode Reset de la \_ classe NETWORKADAPTER CIM demande une réinitialisation de l’unité logique.
ms.assetid: ff4493b7-a9e1-4a39-a14a-05da75659d4e
ms.tgt_platform: multiple
title: Méthode Reset de la classe CIM_NetworkAdapter
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_NetworkAdapter.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4159a4e3232b4cd709848df178d2238b409996a4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523703"
---
# <a name="reset-method-of-the-cim_networkadapter-class"></a><span data-ttu-id="9e871-103">Méthode Reset de la \_ classe NETWORKADAPTER CIM</span><span class="sxs-lookup"><span data-stu-id="9e871-103">Reset method of the CIM\_NetworkAdapter class</span></span>

<span data-ttu-id="9e871-104">La méthode **Reset** de la \_ classe NetworkAdapter CIM demande une réinitialisation de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="9e871-104">The **Reset** method of the CIM\_NetworkAdapter class requests a reset of the logical device.</span></span> <span data-ttu-id="9e871-105">Cette méthode est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="9e871-105">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9e871-106">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="9e871-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="9e871-107">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="9e871-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="9e871-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9e871-108">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="9e871-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9e871-109">Parameters</span></span>

<span data-ttu-id="9e871-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="9e871-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9e871-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9e871-111">Return value</span></span>

<span data-ttu-id="9e871-112">Retourne 0 (zéro) si la requête a été exécutée avec succès, 1 (un) si la demande n’est pas prise en charge, et une autre valeur si une erreur s’est produite.</span><span class="sxs-lookup"><span data-stu-id="9e871-112">Returns 0 (zero) if the request was successfully executed, 1 (one) if the request is not supported, and some other value if an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e871-113">Notes</span><span class="sxs-lookup"><span data-stu-id="9e871-113">Remarks</span></span>

<span data-ttu-id="9e871-114">Actuellement, cette méthode n’est pas implémentée par WMI.</span><span class="sxs-lookup"><span data-stu-id="9e871-114">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="9e871-115">Pour utiliser cette méthode, vous devez l’implémenter dans votre propre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="9e871-115">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="9e871-116">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="9e871-116">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="9e871-117">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="9e871-117">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e871-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9e871-118">Requirements</span></span>



| <span data-ttu-id="9e871-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9e871-119">Requirement</span></span> | <span data-ttu-id="9e871-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="9e871-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9e871-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9e871-121">Minimum supported client</span></span><br/> | <span data-ttu-id="9e871-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9e871-122">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9e871-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9e871-123">Minimum supported server</span></span><br/> | <span data-ttu-id="9e871-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9e871-124">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9e871-125">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="9e871-125">Namespace</span></span><br/>                | <span data-ttu-id="9e871-126">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="9e871-126">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9e871-127">MOF</span><span class="sxs-lookup"><span data-stu-id="9e871-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9e871-128"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9e871-128"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9e871-129">DLL</span><span class="sxs-lookup"><span data-stu-id="9e871-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9e871-130"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9e871-130"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e871-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9e871-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e871-132">\_NETWORKADAPTER CIM</span><span class="sxs-lookup"><span data-stu-id="9e871-132">CIM\_NetworkAdapter</span></span>](reset-method-in-class-cim-networkadapter.md)
</dt> <dt>

[<span data-ttu-id="9e871-133">**\_NETWORKADAPTER CIM**</span><span class="sxs-lookup"><span data-stu-id="9e871-133">**CIM\_NetworkAdapter**</span></span>](cim-networkadapter.md)
</dt> </dl>

 

 




