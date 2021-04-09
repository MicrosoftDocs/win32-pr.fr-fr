---
description: Arrête le service représenté par l’objet dérivé du \_ service CIM.
ms.assetid: f9eedde7-8d71-40a2-b1e9-7ba97e634f64
ms.tgt_platform: multiple
title: Méthode StopService de la classe CIM_Service (Sdoias. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Service.StopService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 14a7d378b514a93906c3be4f711bd6ab5b88bf17
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110734"
---
# <a name="stopservice-method-of-the-cim_service-class-sdoiash"></a><span data-ttu-id="03f63-103">Méthode StopService de la classe CIM_Service (Sdoias. h)</span><span class="sxs-lookup"><span data-stu-id="03f63-103">StopService method of the CIM_Service class (Sdoias.h)</span></span>

<span data-ttu-id="03f63-104">La méthode **StopService** arrête le service représenté par l’objet dérivé du [**\_ service CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="03f63-104">The **StopService** method stops the service represented by the object derived from [**CIM\_Service**](cim-service.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="03f63-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="03f63-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="03f63-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="03f63-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="03f63-107">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="03f63-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="03f63-108">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="03f63-108">For more information about using this method see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="03f63-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="03f63-109">Syntax</span></span>


```mof
uint32 StopService();
```



## <a name="parameters"></a><span data-ttu-id="03f63-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="03f63-110">Parameters</span></span>

<span data-ttu-id="03f63-111">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="03f63-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="03f63-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="03f63-112">Return value</span></span>

<span data-ttu-id="03f63-113">Retourne la valeur 0 (zéro) si le service a été arrêté avec succès, 1 (un) si la demande n’est pas prise en charge, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="03f63-113">Returns a value of 0 (zero) if the service was successfully stopped, 1 (one) if the request is not supported, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="03f63-114">Notes</span><span class="sxs-lookup"><span data-stu-id="03f63-114">Remarks</span></span>

<span data-ttu-id="03f63-115">Actuellement, cette méthode n’est pas implémentée par WMI.</span><span class="sxs-lookup"><span data-stu-id="03f63-115">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="03f63-116">Pour utiliser cette méthode, vous devez l’implémenter dans votre propre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="03f63-116">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="03f63-117">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="03f63-117">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="03f63-118">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="03f63-118">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="03f63-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="03f63-119">Requirements</span></span>



| <span data-ttu-id="03f63-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="03f63-120">Requirement</span></span> | <span data-ttu-id="03f63-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="03f63-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="03f63-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="03f63-122">Minimum supported client</span></span><br/> | <span data-ttu-id="03f63-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="03f63-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="03f63-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="03f63-124">Minimum supported server</span></span><br/> | <span data-ttu-id="03f63-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="03f63-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="03f63-126">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="03f63-126">Namespace</span></span><br/>                | <span data-ttu-id="03f63-127">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="03f63-127">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="03f63-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="03f63-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="03f63-129"><dt>Sdoias. h</dt></span><span class="sxs-lookup"><span data-stu-id="03f63-129"><dt>Sdoias.h</dt></span></span> </dl>     |
| <span data-ttu-id="03f63-130">MOF</span><span class="sxs-lookup"><span data-stu-id="03f63-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="03f63-131"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="03f63-131"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="03f63-132">DLL</span><span class="sxs-lookup"><span data-stu-id="03f63-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="03f63-133"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="03f63-133"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03f63-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="03f63-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03f63-135">\_Service CIM</span><span class="sxs-lookup"><span data-stu-id="03f63-135">CIM\_Service</span></span>](stopservice-method-in-class-cim-service.md)
</dt> <dt>

[<span data-ttu-id="03f63-136">**\_Service CIM**</span><span class="sxs-lookup"><span data-stu-id="03f63-136">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

