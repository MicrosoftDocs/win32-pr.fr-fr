---
description: La méthode SetSpeed demande que la vitesse du ventilateur soit définie sur la valeur spécifiée dans le paramètre d’entrée de la méthode.
ms.assetid: 7dd1cd57-66c5-4b50-9a73-31caf0b824e6
ms.tgt_platform: multiple
title: Méthode SetSpeed de la classe CIM_Fan
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Fan.SetSpeed
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 16d90dbef3a9318ad144303e5720cea0abbde03e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861729"
---
# <a name="setspeed-method-of-the-cim_fan-class"></a><span data-ttu-id="d72af-103">Méthode SetSpeed de la \_ classe de ventilateur CIM</span><span class="sxs-lookup"><span data-stu-id="d72af-103">SetSpeed method of the CIM\_Fan class</span></span>

<span data-ttu-id="d72af-104">La méthode **SetSpeed** demande que la vitesse du ventilateur soit définie sur la valeur spécifiée dans le paramètre d’entrée de la méthode.</span><span class="sxs-lookup"><span data-stu-id="d72af-104">The **SetSpeed** method requests that the fan speed be set to the value specified in the method's input parameter.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d72af-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="d72af-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="d72af-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="d72af-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="d72af-107">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="d72af-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="d72af-108">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="d72af-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="d72af-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d72af-109">Syntax</span></span>


```mof
uint32 SetSpeed(
  [in] uint64 DesiredSpeed
);
```



## <a name="parameters"></a><span data-ttu-id="d72af-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d72af-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d72af-111">*DesiredSpeed* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d72af-111">*DesiredSpeed* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d72af-112">Vitesse de ventilateur demandée, en tours par minute.</span><span class="sxs-lookup"><span data-stu-id="d72af-112">Requested fan speed, in revolutions per minute.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d72af-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d72af-113">Return value</span></span>

<span data-ttu-id="d72af-114">Retourne la valeur 0 (zéro) en cas de réussite, 1 (un) si la demande n’est pas prise en charge, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="d72af-114">Returns a value of 0 (zero) on success, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="d72af-115">Notes</span><span class="sxs-lookup"><span data-stu-id="d72af-115">Remarks</span></span>

<span data-ttu-id="d72af-116">Actuellement, cette méthode n’est pas implémentée par WMI.</span><span class="sxs-lookup"><span data-stu-id="d72af-116">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="d72af-117">Pour utiliser cette méthode, vous devez l’implémenter dans votre propre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="d72af-117">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="d72af-118">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="d72af-118">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="d72af-119">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="d72af-119">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="d72af-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d72af-120">Requirements</span></span>



| <span data-ttu-id="d72af-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d72af-121">Requirement</span></span> | <span data-ttu-id="d72af-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="d72af-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d72af-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d72af-123">Minimum supported client</span></span><br/> | <span data-ttu-id="d72af-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d72af-124">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d72af-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d72af-125">Minimum supported server</span></span><br/> | <span data-ttu-id="d72af-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d72af-126">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d72af-127">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d72af-127">Namespace</span></span><br/>                | <span data-ttu-id="d72af-128">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="d72af-128">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d72af-129">MOF</span><span class="sxs-lookup"><span data-stu-id="d72af-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d72af-130"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d72af-130"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d72af-131">DLL</span><span class="sxs-lookup"><span data-stu-id="d72af-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d72af-132"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d72af-132"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d72af-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d72af-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d72af-134">\_Ventilateur CIM</span><span class="sxs-lookup"><span data-stu-id="d72af-134">CIM\_Fan</span></span>](setspeed-method-in-class-cim-fan.md)
</dt> <dt>

[<span data-ttu-id="d72af-135">**\_Ventilateur CIM**</span><span class="sxs-lookup"><span data-stu-id="d72af-135">**CIM\_Fan**</span></span>](cim-fan.md)
</dt> </dl>

 

