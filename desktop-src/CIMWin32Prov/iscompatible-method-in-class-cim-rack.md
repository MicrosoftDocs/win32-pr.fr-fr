---
description: Vérifie si le rack référencé peut être contenu ou inséré dans le package physique.
ms.assetid: 03276c6a-ca48-48bc-adbe-e53e02107abb
ms.tgt_platform: multiple
title: Méthode IsCompatible de la classe CIM_Rack
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Rack.IsCompatible
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6855b797e8941882aac1dc25d77b2ef7e3bc11c1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513933"
---
# <a name="iscompatible-method-of-the-cim_rack-class"></a><span data-ttu-id="0b799-103">Méthode IsCompatible de la \_ classe de rack CIM</span><span class="sxs-lookup"><span data-stu-id="0b799-103">IsCompatible method of the CIM\_Rack class</span></span>

<span data-ttu-id="0b799-104">La méthode **IsCompatible** vérifie si le rack référencé peut être contenu ou inséré dans le package physique.</span><span class="sxs-lookup"><span data-stu-id="0b799-104">The **IsCompatible** method verifies whether the referenced rack can be contained by, or inserted into, the physical package.</span></span> <span data-ttu-id="0b799-105">Dans une sous-classe, l’ensemble des codes de retour possibles peut être spécifié à l’aide d’un qualificateur **ValueMap** sur la méthode.</span><span class="sxs-lookup"><span data-stu-id="0b799-105">In a subclass, the set of possible return codes can be specified by using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="0b799-106">Les chaînes dans lesquelles le contenu **ValueMap** est traduit peuvent également être spécifiées dans la sous-classe en tant que qualificateur de tableau de **valeurs** .</span><span class="sxs-lookup"><span data-stu-id="0b799-106">The strings to which the **ValueMap** contents are translated can also be specified in the subclass as a **Values** array qualifier.</span></span> <span data-ttu-id="0b799-107">Cette méthode est héritée de la [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="0b799-107">This method is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0b799-108">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="0b799-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="0b799-109">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="0b799-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="0b799-110">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="0b799-110">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="0b799-111">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="0b799-111">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="0b799-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0b799-112">Syntax</span></span>


```mof
uint32 IsCompatible(
  [in] CIM_PhysicalElement ElementToCheck
);
```



## <a name="parameters"></a><span data-ttu-id="0b799-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0b799-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b799-114">*ElementToCheck* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0b799-114">*ElementToCheck* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b799-115">Référence à l’élément physique sur lequel cette méthode s’exécute.</span><span class="sxs-lookup"><span data-stu-id="0b799-115">Reference to the physical element that this method runs against.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b799-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0b799-116">Return value</span></span>

<span data-ttu-id="0b799-117">Retourne la valeur 0 (zéro) en cas de réussite, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="0b799-117">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b799-118">Notes</span><span class="sxs-lookup"><span data-stu-id="0b799-118">Remarks</span></span>

<span data-ttu-id="0b799-119">Actuellement, cette méthode n’est pas implémentée par WMI.</span><span class="sxs-lookup"><span data-stu-id="0b799-119">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="0b799-120">Pour utiliser cette méthode, vous devez l’implémenter dans votre propre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="0b799-120">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="0b799-121">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="0b799-121">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="0b799-122">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="0b799-122">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b799-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0b799-123">Requirements</span></span>



| <span data-ttu-id="0b799-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0b799-124">Requirement</span></span> | <span data-ttu-id="0b799-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="0b799-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0b799-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0b799-126">Minimum supported client</span></span><br/> | <span data-ttu-id="0b799-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0b799-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0b799-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0b799-128">Minimum supported server</span></span><br/> | <span data-ttu-id="0b799-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0b799-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0b799-130">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="0b799-130">Namespace</span></span><br/>                | <span data-ttu-id="0b799-131">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="0b799-131">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0b799-132">MOF</span><span class="sxs-lookup"><span data-stu-id="0b799-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0b799-133"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0b799-133"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0b799-134">DLL</span><span class="sxs-lookup"><span data-stu-id="0b799-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0b799-135"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b799-135"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b799-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0b799-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b799-137">**\_Rack CIM**</span><span class="sxs-lookup"><span data-stu-id="0b799-137">**CIM\_Rack**</span></span>](iscompatible-method-in-class-cim-rack.md)
</dt> <dt>

[<span data-ttu-id="0b799-138">**\_Rack CIM**</span><span class="sxs-lookup"><span data-stu-id="0b799-138">**CIM\_Rack**</span></span>](cim-rack.md)
</dt> </dl>

 

