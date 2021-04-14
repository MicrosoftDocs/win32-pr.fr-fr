---
description: La méthode Reset de la \_ classe CIM PCMCIAController demande une réinitialisation de l’unité logique.
ms.assetid: c58e3265-2849-4154-a03e-2e1cfa9e3d30
ms.tgt_platform: multiple
title: Méthode Reset de la classe CIM_PCMCIAController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PCMCIAController.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8576bc5c1ce291c355d2907761e5b342ea6f3bc9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201008"
---
# <a name="reset-method-of-the-cim_pcmciacontroller-class"></a><span data-ttu-id="33010-103">Méthode Reset de la \_ classe CIM PCMCIAController</span><span class="sxs-lookup"><span data-stu-id="33010-103">Reset method of the CIM\_PCMCIAController class</span></span>

<span data-ttu-id="33010-104">La méthode **Reset** de la \_ classe CIM PCMCIAController demande une réinitialisation de l’unité logique.</span><span class="sxs-lookup"><span data-stu-id="33010-104">The **Reset** method of the CIM\_PCMCIAController class requests a reset of the logical device.</span></span> <span data-ttu-id="33010-105">Cette méthode est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="33010-105">This method is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="33010-106">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="33010-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="33010-107">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="33010-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="33010-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="33010-108">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="33010-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="33010-109">Parameters</span></span>

<span data-ttu-id="33010-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="33010-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="33010-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="33010-111">Return value</span></span>

<span data-ttu-id="33010-112">Retourne 0 (zéro) si la requête a été exécutée avec succès, 1 (un) si la demande n’est pas prise en charge, et une autre valeur si une erreur s’est produite.</span><span class="sxs-lookup"><span data-stu-id="33010-112">Returns 0 (zero) if the request was successfully executed, 1 (one) if the request is not supported, and some other value if an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="33010-113">Notes</span><span class="sxs-lookup"><span data-stu-id="33010-113">Remarks</span></span>

<span data-ttu-id="33010-114">Cette méthode n’est pas implémentée par WMI.</span><span class="sxs-lookup"><span data-stu-id="33010-114">This method is not implemented by WMI.</span></span> <span data-ttu-id="33010-115">Pour utiliser cette méthode, vous devez l’implémenter dans votre propre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="33010-115">To use this method, you must implement it in your own provider.</span></span> <span data-ttu-id="33010-116">Pour les classes WMI dérivées de [**CIM \_ PCMCIAController**](cim-pcmciacontroller.md), consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="33010-116">For WMI classes derived from [**CIM\_PCMCIAController**](cim-pcmciacontroller.md), see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="33010-117">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="33010-117">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="33010-118">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="33010-118">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="33010-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="33010-119">Requirements</span></span>



| <span data-ttu-id="33010-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="33010-120">Requirement</span></span> | <span data-ttu-id="33010-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="33010-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="33010-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="33010-122">Minimum supported client</span></span><br/> | <span data-ttu-id="33010-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="33010-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="33010-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="33010-124">Minimum supported server</span></span><br/> | <span data-ttu-id="33010-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="33010-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="33010-126">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="33010-126">Namespace</span></span><br/>                | <span data-ttu-id="33010-127">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="33010-127">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="33010-128">MOF</span><span class="sxs-lookup"><span data-stu-id="33010-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="33010-129"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="33010-129"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="33010-130">DLL</span><span class="sxs-lookup"><span data-stu-id="33010-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="33010-131"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="33010-131"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33010-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="33010-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33010-133">\_PCMCIACONTROLLER CIM</span><span class="sxs-lookup"><span data-stu-id="33010-133">CIM\_PCMCIAController</span></span>](reset-method-in-class-cim-pcmciacontroller.md)
</dt> <dt>

[<span data-ttu-id="33010-134">**\_PCMCIACONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="33010-134">**CIM\_PCMCIAController**</span></span>](cim-pcmciacontroller.md)
</dt> </dl>

 

 




