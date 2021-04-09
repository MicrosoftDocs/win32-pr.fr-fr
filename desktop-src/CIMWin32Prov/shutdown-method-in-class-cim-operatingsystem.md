---
description: La méthode Shutdown demande l’arrêt du système d’exploitation.
ms.assetid: f2a2a98b-2f4f-4aa1-9f54-515660273c8d
ms.tgt_platform: multiple
title: Méthode Shutdown de la classe CIM_OperatingSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_OperatingSystem.Shutdown
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 78a11f325b8682b0024ff281a48989b837d3073a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860637"
---
# <a name="shutdown-method-of-the-cim_operatingsystem-class"></a><span data-ttu-id="e4473-103">Méthode Shutdown de la \_ classe CIM OperatingSystem</span><span class="sxs-lookup"><span data-stu-id="e4473-103">Shutdown method of the CIM\_OperatingSystem class</span></span>

<span data-ttu-id="e4473-104">La méthode **Shutdown** demande l’arrêt du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="e4473-104">The **Shutdown** method requests a shutdown of the operating system.</span></span> <span data-ttu-id="e4473-105">L’implémentation ou la sous-classe du système d’exploitation peut établir des dépendances entre les méthodes **Shutdown** et [**reboot**](reboot-method-in-class-cim-operatingsystem.md) .</span><span class="sxs-lookup"><span data-stu-id="e4473-105">The implementation or subclass of the operating system can establish dependencies between the **Shutdown** and [**Reboot**](reboot-method-in-class-cim-operatingsystem.md) methods.</span></span> <span data-ttu-id="e4473-106">Par exemple, des fonctionnalités plus sophistiquées peuvent être fournies, telles qu’un arrêt et un redémarrage planifiés.</span><span class="sxs-lookup"><span data-stu-id="e4473-106">For example, more sophisticated capabilities can be provided, such as a scheduled shutdown and reboot.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e4473-107">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="e4473-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="e4473-108">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="e4473-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="e4473-109">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="e4473-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="e4473-110">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="e4473-110">For more information about using this method see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="e4473-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e4473-111">Syntax</span></span>


```mof
uint32 Shutdown();
```



## <a name="parameters"></a><span data-ttu-id="e4473-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e4473-112">Parameters</span></span>

<span data-ttu-id="e4473-113">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="e4473-113">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e4473-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e4473-114">Return value</span></span>

<span data-ttu-id="e4473-115">Retourne la valeur 0 (zéro) en cas de réussite, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="e4473-115">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4473-116">Notes</span><span class="sxs-lookup"><span data-stu-id="e4473-116">Remarks</span></span>

<span data-ttu-id="e4473-117">Actuellement, cette méthode n’est pas implémentée par WMI.</span><span class="sxs-lookup"><span data-stu-id="e4473-117">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="e4473-118">Pour utiliser cette méthode, vous devez l’implémenter dans votre propre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="e4473-118">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="e4473-119">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="e4473-119">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="e4473-120">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="e4473-120">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4473-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e4473-121">Requirements</span></span>



| <span data-ttu-id="e4473-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e4473-122">Requirement</span></span> | <span data-ttu-id="e4473-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="e4473-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e4473-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e4473-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e4473-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e4473-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e4473-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e4473-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e4473-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e4473-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e4473-128">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e4473-128">Namespace</span></span><br/>                | <span data-ttu-id="e4473-129">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="e4473-129">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e4473-130">MOF</span><span class="sxs-lookup"><span data-stu-id="e4473-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e4473-131"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e4473-131"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e4473-132">DLL</span><span class="sxs-lookup"><span data-stu-id="e4473-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e4473-133"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e4473-133"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4473-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e4473-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4473-135">\_OPERATINGSYSTEM CIM</span><span class="sxs-lookup"><span data-stu-id="e4473-135">CIM\_OperatingSystem</span></span>](shutdown-method-in-class-cim-operatingsystem.md)
</dt> <dt>

[<span data-ttu-id="e4473-136">**\_OPERATINGSYSTEM CIM**</span><span class="sxs-lookup"><span data-stu-id="e4473-136">**CIM\_OperatingSystem**</span></span>](cim-operatingsystem.md)
</dt> </dl>

 

