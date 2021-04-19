---
description: Vérifie si l’élément physique référencé peut être contenu ou inséré dans le package physique.
ms.assetid: 406aaa75-b48c-4377-adb5-e900676b6e36
ms.tgt_platform: multiple
title: Méthode IsCompatible de la classe CIM_PhysicalPackage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalPackage.IsCompatible
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1957b8d0c1929ff6f7b4ef8c69fa55ea4ccc83b9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106512891"
---
# <a name="iscompatible-method-of-the-cim_physicalpackage-class"></a><span data-ttu-id="6a130-103">Méthode IsCompatible de la \_ classe CIM PhysicalPackage</span><span class="sxs-lookup"><span data-stu-id="6a130-103">IsCompatible method of the CIM\_PhysicalPackage class</span></span>

<span data-ttu-id="6a130-104">La méthode **IsCompatible** vérifie si l’élément physique référencé peut être contenu ou inséré dans le package physique.</span><span class="sxs-lookup"><span data-stu-id="6a130-104">The **IsCompatible** method verifies whether the referenced physical element can be contained by, or inserted into, the physical package.</span></span> <span data-ttu-id="6a130-105">Dans une sous-classe, l’ensemble des codes de retour possibles peut être spécifié à l’aide d’un qualificateur **ValueMap** sur la méthode.</span><span class="sxs-lookup"><span data-stu-id="6a130-105">In a subclass, the set of possible return codes can be specified by using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="6a130-106">Les chaînes dans lesquelles le contenu **ValueMap** est traduit peuvent également être spécifiées dans la sous-classe en tant que qualificateur de tableau de **valeurs** .</span><span class="sxs-lookup"><span data-stu-id="6a130-106">The strings to which the **ValueMap** contents are translated can also be specified in the subclass as a **Values** array qualifier.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6a130-107">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="6a130-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="6a130-108">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="6a130-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="6a130-109">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="6a130-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="6a130-110">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="6a130-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="6a130-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6a130-111">Syntax</span></span>


```mof
uint32 IsCompatible(
  [in] CIM_PhysicalElement REF ElementToCheck
);
```



## <a name="parameters"></a><span data-ttu-id="6a130-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6a130-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a130-113">*ElementToCheck* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6a130-113">*ElementToCheck* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a130-114">Référence à l’élément physique sur lequel la méthode **IsCompatible** s’exécute.</span><span class="sxs-lookup"><span data-stu-id="6a130-114">Reference to the physical element that the **IsCompatible** method runs against.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a130-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6a130-115">Return value</span></span>

<span data-ttu-id="6a130-116">Retourne la valeur 0 (zéro) en cas de réussite, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="6a130-116">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a130-117">Notes</span><span class="sxs-lookup"><span data-stu-id="6a130-117">Remarks</span></span>

<span data-ttu-id="6a130-118">Actuellement, cette méthode n’est pas implémentée par WMI.</span><span class="sxs-lookup"><span data-stu-id="6a130-118">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="6a130-119">Pour utiliser cette méthode, vous devez l’implémenter dans votre propre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="6a130-119">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="6a130-120">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="6a130-120">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="6a130-121">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="6a130-121">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a130-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6a130-122">Requirements</span></span>



| <span data-ttu-id="6a130-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6a130-123">Requirement</span></span> | <span data-ttu-id="6a130-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="6a130-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6a130-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6a130-125">Minimum supported client</span></span><br/> | <span data-ttu-id="6a130-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6a130-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6a130-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6a130-127">Minimum supported server</span></span><br/> | <span data-ttu-id="6a130-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6a130-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6a130-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="6a130-129">Namespace</span></span><br/>                | <span data-ttu-id="6a130-130">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="6a130-130">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6a130-131">MOF</span><span class="sxs-lookup"><span data-stu-id="6a130-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6a130-132"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6a130-132"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6a130-133">DLL</span><span class="sxs-lookup"><span data-stu-id="6a130-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6a130-134"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6a130-134"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a130-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6a130-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a130-136">**\_PHYSICALPACKAGE CIM**</span><span class="sxs-lookup"><span data-stu-id="6a130-136">**CIM\_PhysicalPackage**</span></span>](iscompatible-method-in-class-cim-physicalpackage.md)
</dt> <dt>

[<span data-ttu-id="6a130-137">**\_PHYSICALPACKAGE CIM**</span><span class="sxs-lookup"><span data-stu-id="6a130-137">**CIM\_PhysicalPackage**</span></span>](cim-physicalpackage.md)
</dt> </dl>

 

