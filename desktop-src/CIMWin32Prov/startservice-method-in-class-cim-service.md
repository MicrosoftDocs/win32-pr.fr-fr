---
description: Méthode StartService de la classe CIM_Service (fournisseurs WMI CIMWin32)-la méthode StartService met le service dans un état Démarré.
ms.assetid: 0f2880ed-1643-4211-8684-12493711b1f8
ms.tgt_platform: multiple
title: Méthode StartService de la classe CIM_Service (fournisseurs WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Service.StartService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6027112323fc14abf4c4a8dc667b921025a5e652
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086167"
---
# <a name="startservice-method-of-the-cim_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="1f7a0-103">Méthode StartService de la classe CIM_Service (fournisseurs WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="1f7a0-103">StartService method of the CIM_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="1f7a0-104">La méthode **StartService** met le service dans un état Démarré.</span><span class="sxs-lookup"><span data-stu-id="1f7a0-104">The **StartService** method puts the service in a started state.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1f7a0-105">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="1f7a0-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="1f7a0-106">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="1f7a0-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="1f7a0-107">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="1f7a0-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="1f7a0-108">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="1f7a0-108">For more information about using this method see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="1f7a0-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1f7a0-109">Syntax</span></span>


```mof
uint32 StartService();
```



## <a name="parameters"></a><span data-ttu-id="1f7a0-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1f7a0-110">Parameters</span></span>

<span data-ttu-id="1f7a0-111">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="1f7a0-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1f7a0-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="1f7a0-112">Return value</span></span>

<span data-ttu-id="1f7a0-113">Retourne la valeur 0 (zéro) en cas de réussite, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="1f7a0-113">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span> <span data-ttu-id="1f7a0-114">Dans une sous-classe, l’ensemble des codes de retour possibles peut être spécifié à l’aide d’un qualificateur **ValueMap** sur la méthode.</span><span class="sxs-lookup"><span data-stu-id="1f7a0-114">In a subclass, the set of possible return codes can be specified by using a **ValueMap** qualifier on the method.</span></span> <span data-ttu-id="1f7a0-115">Les chaînes dans lesquelles le contenu **ValueMap** est traduit peuvent également être spécifiées dans la sous-classe en tant que qualificateur de tableau de **valeurs** .</span><span class="sxs-lookup"><span data-stu-id="1f7a0-115">The strings to which the **ValueMap** contents are translated can also be specified in the subclass as a **Values** array qualifier.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f7a0-116">Notes </span><span class="sxs-lookup"><span data-stu-id="1f7a0-116">Remarks</span></span>

<span data-ttu-id="1f7a0-117">Actuellement, cette méthode n’est pas implémentée par WMI.</span><span class="sxs-lookup"><span data-stu-id="1f7a0-117">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="1f7a0-118">Pour utiliser cette méthode, vous devez l’implémenter dans votre propre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="1f7a0-118">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="1f7a0-119">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="1f7a0-119">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="1f7a0-120">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="1f7a0-120">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f7a0-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1f7a0-121">Requirements</span></span>



| <span data-ttu-id="1f7a0-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1f7a0-122">Requirement</span></span> | <span data-ttu-id="1f7a0-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="1f7a0-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1f7a0-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1f7a0-124">Minimum supported client</span></span><br/> | <span data-ttu-id="1f7a0-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1f7a0-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1f7a0-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1f7a0-126">Minimum supported server</span></span><br/> | <span data-ttu-id="1f7a0-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1f7a0-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1f7a0-128">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="1f7a0-128">Namespace</span></span><br/>                | <span data-ttu-id="1f7a0-129">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="1f7a0-129">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1f7a0-130">MOF</span><span class="sxs-lookup"><span data-stu-id="1f7a0-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1f7a0-131"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1f7a0-131"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1f7a0-132">DLL</span><span class="sxs-lookup"><span data-stu-id="1f7a0-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1f7a0-133"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1f7a0-133"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f7a0-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1f7a0-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f7a0-135">\_Service CIM</span><span class="sxs-lookup"><span data-stu-id="1f7a0-135">CIM\_Service</span></span>](startservice-method-in-class-cim-service.md)
</dt> <dt>

[<span data-ttu-id="1f7a0-136">**\_Service CIM**</span><span class="sxs-lookup"><span data-stu-id="1f7a0-136">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

