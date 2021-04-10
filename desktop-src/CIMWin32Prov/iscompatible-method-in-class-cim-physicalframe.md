---
description: Vérifie si le cadre physique référencé peut être contenu ou inséré dans le package physique.
ms.assetid: 8102569d-a956-445a-ae42-23eb206ba224
ms.tgt_platform: multiple
title: Méthode IsCompatible de la classe CIM_PhysicalFrame
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalFrame.IsCompatible
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 121405e66a9361e832f6accb24ca6e303bb8e280
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950550"
---
# <a name="iscompatible-method-of-the-cim_physicalframe-class"></a><span data-ttu-id="10ba8-103">Méthode IsCompatible de la \_ classe CIM PhysicalFrame</span><span class="sxs-lookup"><span data-stu-id="10ba8-103">IsCompatible method of the CIM\_PhysicalFrame class</span></span>

<span data-ttu-id="10ba8-104">La méthode **IsCompatible** vérifie si le cadre physique référencé peut être contenu ou inséré dans le package physique.</span><span class="sxs-lookup"><span data-stu-id="10ba8-104">The **IsCompatible** method verifies whether the referenced physical frame can be contained by, or inserted into, the physical package.</span></span> <span data-ttu-id="10ba8-105">Dans une sous-classe, l’ensemble des codes de retour possibles peut être spécifié à l’aide d’un qualificateur **ValueMap** sur la méthode.</span><span class="sxs-lookup"><span data-stu-id="10ba8-105">In a subclass, the set of possible return codes can be specified by using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="10ba8-106">Les chaînes dans lesquelles le contenu **ValueMap** est traduit peuvent également être spécifiées dans la sous-classe en tant que qualificateur de tableau de **valeurs** .</span><span class="sxs-lookup"><span data-stu-id="10ba8-106">The strings to which the **ValueMap** contents are translated can also be specified in the subclass as a **Values** array qualifier.</span></span> <span data-ttu-id="10ba8-107">Cette méthode est héritée de la [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="10ba8-107">This method is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="10ba8-108">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="10ba8-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="10ba8-109">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="10ba8-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="10ba8-110">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="10ba8-110">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="10ba8-111">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="10ba8-111">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="10ba8-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="10ba8-112">Syntax</span></span>


```mof
uint32 IsCompatible(
  [in] CIM_PhysicalElement ElementToCheck
);
```



## <a name="parameters"></a><span data-ttu-id="10ba8-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="10ba8-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10ba8-114">*ElementToCheck* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="10ba8-114">*ElementToCheck* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10ba8-115">Référence à l’élément physique sur lequel la méthode **IsCompatible** s’exécute.</span><span class="sxs-lookup"><span data-stu-id="10ba8-115">Reference to the physical element that the **IsCompatible** method runs against.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10ba8-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="10ba8-116">Return value</span></span>

<span data-ttu-id="10ba8-117">Retourne la valeur 0 (zéro) en cas de réussite, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="10ba8-117">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="10ba8-118">Notes</span><span class="sxs-lookup"><span data-stu-id="10ba8-118">Remarks</span></span>

<span data-ttu-id="10ba8-119">Actuellement, cette méthode n’est pas implémentée par WMI.</span><span class="sxs-lookup"><span data-stu-id="10ba8-119">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="10ba8-120">Pour utiliser cette méthode, vous devez l’implémenter dans votre propre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="10ba8-120">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="10ba8-121">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="10ba8-121">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="10ba8-122">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="10ba8-122">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="10ba8-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="10ba8-123">Requirements</span></span>



| <span data-ttu-id="10ba8-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="10ba8-124">Requirement</span></span> | <span data-ttu-id="10ba8-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="10ba8-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="10ba8-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="10ba8-126">Minimum supported client</span></span><br/> | <span data-ttu-id="10ba8-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="10ba8-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="10ba8-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="10ba8-128">Minimum supported server</span></span><br/> | <span data-ttu-id="10ba8-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="10ba8-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="10ba8-130">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="10ba8-130">Namespace</span></span><br/>                | <span data-ttu-id="10ba8-131">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="10ba8-131">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="10ba8-132">MOF</span><span class="sxs-lookup"><span data-stu-id="10ba8-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="10ba8-133"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="10ba8-133"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="10ba8-134">DLL</span><span class="sxs-lookup"><span data-stu-id="10ba8-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="10ba8-135"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="10ba8-135"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10ba8-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="10ba8-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10ba8-137">**\_PHYSICALFRAME CIM**</span><span class="sxs-lookup"><span data-stu-id="10ba8-137">**CIM\_PhysicalFrame**</span></span>](iscompatible-method-in-class-cim-physicalframe.md)
</dt> <dt>

[<span data-ttu-id="10ba8-138">**\_PHYSICALFRAME CIM**</span><span class="sxs-lookup"><span data-stu-id="10ba8-138">**CIM\_PhysicalFrame**</span></span>](cim-physicalframe.md)
</dt> </dl>

 

