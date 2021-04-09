---
description: La méthode Invoke de la \_ classe CIM VersionCompatibilityCheck évalue une vérification particulière.
ms.assetid: d1ccc248-340e-4277-9696-063e1e2bf915
ms.tgt_platform: multiple
title: Méthode Invoke de la classe CIM_VersionCompatibilityCheck
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VersionCompatibilityCheck.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: bccbb6072ae84a238b60247daf6b81cfaa74e608
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860929"
---
# <a name="invoke-method-of-the-cim_versioncompatibilitycheck-class"></a><span data-ttu-id="5b10c-103">Méthode Invoke de la \_ classe CIM VersionCompatibilityCheck</span><span class="sxs-lookup"><span data-stu-id="5b10c-103">Invoke method of the CIM\_VersionCompatibilityCheck class</span></span>

<span data-ttu-id="5b10c-104">La méthode **Invoke** de la classe [**CIM \_ VersionCompatibilityCheck**](cim-versioncompatibilitycheck.md) évalue une vérification particulière.</span><span class="sxs-lookup"><span data-stu-id="5b10c-104">The **Invoke** method of the [**CIM\_VersionCompatibilityCheck**](cim-versioncompatibilitycheck.md) class evaluates a particular check.</span></span> <span data-ttu-id="5b10c-105">Les détails de la façon dont la méthode évalue un contrôle particulier dans un contexte CIM sont décrits par les sous-classes de [**\_ vérification CIM**](cim-check.md) non abstraites.</span><span class="sxs-lookup"><span data-stu-id="5b10c-105">The details of how the method evaluates a particular check in a CIM context are described by the non-abstract [**CIM\_Check**](cim-check.md) subclasses.</span></span> <span data-ttu-id="5b10c-106">Cette méthode est héritée de la **\_ vérification CIM**.</span><span class="sxs-lookup"><span data-stu-id="5b10c-106">This method is inherited from **CIM\_Check**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5b10c-107">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="5b10c-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="5b10c-108">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="5b10c-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="5b10c-109">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="5b10c-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="5b10c-110">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="5b10c-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="5b10c-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5b10c-111">Syntax</span></span>


```mof
uint32 Invoke();
```



## <a name="parameters"></a><span data-ttu-id="5b10c-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5b10c-112">Parameters</span></span>

<span data-ttu-id="5b10c-113">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="5b10c-113">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5b10c-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5b10c-114">Return value</span></span>

<span data-ttu-id="5b10c-115">Retourne la valeur 0 (zéro) en cas de réussite, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="5b10c-115">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b10c-116">Notes</span><span class="sxs-lookup"><span data-stu-id="5b10c-116">Remarks</span></span>

<span data-ttu-id="5b10c-117">Actuellement, cette méthode n’est pas implémentée par WMI.</span><span class="sxs-lookup"><span data-stu-id="5b10c-117">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="5b10c-118">Pour utiliser cette méthode, vous devez l’implémenter dans votre propre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="5b10c-118">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="5b10c-119">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="5b10c-119">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="5b10c-120">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="5b10c-120">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b10c-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5b10c-121">Requirements</span></span>



| <span data-ttu-id="5b10c-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5b10c-122">Requirement</span></span> | <span data-ttu-id="5b10c-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="5b10c-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5b10c-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5b10c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="5b10c-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5b10c-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5b10c-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5b10c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="5b10c-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5b10c-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5b10c-128">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="5b10c-128">Namespace</span></span><br/>                | <span data-ttu-id="5b10c-129">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="5b10c-129">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5b10c-130">MOF</span><span class="sxs-lookup"><span data-stu-id="5b10c-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5b10c-131"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5b10c-131"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5b10c-132">DLL</span><span class="sxs-lookup"><span data-stu-id="5b10c-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5b10c-133"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5b10c-133"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b10c-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5b10c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b10c-135">\_VERSIONCOMPATIBILITYCHECK CIM</span><span class="sxs-lookup"><span data-stu-id="5b10c-135">CIM\_VersionCompatibilityCheck</span></span>](invoke-method-in-class-cim-versioncompatibilitycheck.md)
</dt> <dt>

[<span data-ttu-id="5b10c-136">**\_VERSIONCOMPATIBILITYCHECK CIM**</span><span class="sxs-lookup"><span data-stu-id="5b10c-136">**CIM\_VersionCompatibilityCheck**</span></span>](cim-versioncompatibilitycheck.md)
</dt> </dl>

 

