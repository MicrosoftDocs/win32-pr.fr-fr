---
description: Arrête le service représenté par l’objet dérivé de CIM \_ BootService.
ms.assetid: 443a2afa-ed46-4378-a06f-5f9f94af51c9
ms.tgt_platform: multiple
title: Méthode StopService de la classe CIM_BootService (Sdoias. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BootService.StopService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c054a9d05410ddbe7ee7d11c5bd4adba9e0ce83b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523692"
---
# <a name="stopservice-method-of-the-cim_bootservice-class"></a><span data-ttu-id="47d3d-103">Méthode StopService de la \_ classe CIM BootService</span><span class="sxs-lookup"><span data-stu-id="47d3d-103">StopService method of the CIM\_BootService class</span></span>

<span data-ttu-id="47d3d-104">La méthode **StopService** arrête le service représenté par l’objet dérivé de [**CIM \_ BootService**](cim-bootservice.md).</span><span class="sxs-lookup"><span data-stu-id="47d3d-104">The **StopService** method stops the service represented by the object derived from [**CIM\_BootService**](cim-bootservice.md).</span></span> <span data-ttu-id="47d3d-105">Cette méthode est héritée [**du \_ service CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="47d3d-105">This method is inherited from [**CIM\_Service**](cim-service.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="47d3d-106">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="47d3d-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="47d3d-107">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="47d3d-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="47d3d-108">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="47d3d-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="47d3d-109">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="47d3d-109">For more information about using this method see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="47d3d-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="47d3d-110">Syntax</span></span>


```mof
Integer StopService();
```



## <a name="parameters"></a><span data-ttu-id="47d3d-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="47d3d-111">Parameters</span></span>

<span data-ttu-id="47d3d-112">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="47d3d-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="47d3d-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="47d3d-113">Return value</span></span>

<span data-ttu-id="47d3d-114">Retourne la valeur 0 (zéro) en cas de réussite, 1 (un) si la demande n’est pas prise en charge, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="47d3d-114">Returns a value of 0 (zero) on success, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="47d3d-115">Notes</span><span class="sxs-lookup"><span data-stu-id="47d3d-115">Remarks</span></span>

<span data-ttu-id="47d3d-116">Actuellement, cette méthode n’est pas implémentée par WMI.</span><span class="sxs-lookup"><span data-stu-id="47d3d-116">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="47d3d-117">Pour utiliser cette méthode, vous devez l’implémenter dans votre propre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="47d3d-117">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="47d3d-118">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="47d3d-118">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="47d3d-119">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="47d3d-119">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="47d3d-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="47d3d-120">Requirements</span></span>



| <span data-ttu-id="47d3d-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="47d3d-121">Requirement</span></span> | <span data-ttu-id="47d3d-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="47d3d-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="47d3d-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="47d3d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="47d3d-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="47d3d-124">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="47d3d-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="47d3d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="47d3d-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="47d3d-126">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="47d3d-127">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="47d3d-127">Namespace</span></span><br/>                | <span data-ttu-id="47d3d-128">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="47d3d-128">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="47d3d-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="47d3d-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="47d3d-130"><dt>Sdoias. h</dt></span><span class="sxs-lookup"><span data-stu-id="47d3d-130"><dt>Sdoias.h</dt></span></span> </dl>     |
| <span data-ttu-id="47d3d-131">MOF</span><span class="sxs-lookup"><span data-stu-id="47d3d-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="47d3d-132"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="47d3d-132"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="47d3d-133">DLL</span><span class="sxs-lookup"><span data-stu-id="47d3d-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="47d3d-134"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="47d3d-134"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47d3d-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="47d3d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47d3d-136">\_BOOTSERVICE CIM</span><span class="sxs-lookup"><span data-stu-id="47d3d-136">CIM\_BootService</span></span>](stopservice-method-in-class-cim-bootservice.md)
</dt> <dt>

[<span data-ttu-id="47d3d-137">**\_BOOTSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="47d3d-137">**CIM\_BootService**</span></span>](cim-bootservice.md)
</dt> </dl>

 

