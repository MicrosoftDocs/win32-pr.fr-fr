---
description: La méthode reboot demande un redémarrage du système d’exploitation.
ms.assetid: 2ce766dd-51a4-4ffb-a45a-40399f1110f6
ms.tgt_platform: multiple
title: Méthode reboot de la classe CIM_OperatingSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_OperatingSystem.Reboot
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e498dd16372503b23aa56471224faf4d5d0ff012
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514515"
---
# <a name="reboot-method-of-the-cim_operatingsystem-class"></a><span data-ttu-id="a7f92-103">Méthode reboot de la \_ classe CIM OperatingSystem</span><span class="sxs-lookup"><span data-stu-id="a7f92-103">Reboot method of the CIM\_OperatingSystem class</span></span>

<span data-ttu-id="a7f92-104">La méthode **reboot** demande un redémarrage du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="a7f92-104">The **Reboot** method requests a reboot of the operating system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a7f92-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="a7f92-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="a7f92-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="a7f92-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="a7f92-107">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="a7f92-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="a7f92-108">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="a7f92-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="a7f92-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a7f92-109">Syntax</span></span>


```mof
uint32 Reboot();
```



## <a name="parameters"></a><span data-ttu-id="a7f92-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a7f92-110">Parameters</span></span>

<span data-ttu-id="a7f92-111">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="a7f92-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a7f92-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a7f92-112">Return value</span></span>

<span data-ttu-id="a7f92-113">Retourne la valeur 0 (zéro) en cas de réussite, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="a7f92-113">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="a7f92-114">Notes</span><span class="sxs-lookup"><span data-stu-id="a7f92-114">Remarks</span></span>

<span data-ttu-id="a7f92-115">Actuellement, cette méthode n’est pas implémentée par WMI.</span><span class="sxs-lookup"><span data-stu-id="a7f92-115">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="a7f92-116">Pour utiliser cette méthode, vous devez l’implémenter dans votre propre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="a7f92-116">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="a7f92-117">Pour les classes WMI dérivées de [**CIM \_ OperatingSystem**](cim-operatingsystem.md), consultez [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="a7f92-117">For WMI classes that are derived from [**CIM\_OperatingSystem**](cim-operatingsystem.md), see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="a7f92-118">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="a7f92-118">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="a7f92-119">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="a7f92-119">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

<span data-ttu-id="a7f92-120">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="a7f92-120">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="a7f92-121">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="a7f92-121">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7f92-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a7f92-122">Requirements</span></span>



| <span data-ttu-id="a7f92-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a7f92-123">Requirement</span></span> | <span data-ttu-id="a7f92-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="a7f92-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a7f92-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a7f92-125">Minimum supported client</span></span><br/> | <span data-ttu-id="a7f92-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a7f92-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a7f92-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a7f92-127">Minimum supported server</span></span><br/> | <span data-ttu-id="a7f92-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a7f92-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a7f92-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="a7f92-129">Namespace</span></span><br/>                | <span data-ttu-id="a7f92-130">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="a7f92-130">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a7f92-131">MOF</span><span class="sxs-lookup"><span data-stu-id="a7f92-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a7f92-132"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a7f92-132"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a7f92-133">DLL</span><span class="sxs-lookup"><span data-stu-id="a7f92-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a7f92-134"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a7f92-134"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7f92-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a7f92-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7f92-136">\_OPERATINGSYSTEM CIM</span><span class="sxs-lookup"><span data-stu-id="a7f92-136">CIM\_OperatingSystem</span></span>](reboot-method-in-class-cim-operatingsystem.md)
</dt> <dt>

[<span data-ttu-id="a7f92-137">**\_OPERATINGSYSTEM CIM**</span><span class="sxs-lookup"><span data-stu-id="a7f92-137">**CIM\_OperatingSystem**</span></span>](cim-operatingsystem.md)
</dt> </dl>

 

