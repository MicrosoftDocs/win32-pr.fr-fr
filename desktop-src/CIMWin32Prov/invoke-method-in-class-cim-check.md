---
description: La méthode Invoke de la \_ classe de vérification CIM évalue une vérification particulière.
ms.assetid: cf1adeb2-f8a2-4f84-978f-e801bce104ac
ms.tgt_platform: multiple
title: Méthode Invoke de la classe CIM_Check
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Check.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7774fcd1b3ef451fffb34ce9ad10d404e8ea95b3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516371"
---
# <a name="invoke-method-of-the-cim_check-class"></a><span data-ttu-id="81507-103">Méthode Invoke de la \_ classe de vérification CIM</span><span class="sxs-lookup"><span data-stu-id="81507-103">Invoke method of the CIM\_Check class</span></span>

<span data-ttu-id="81507-104">La méthode **Invoke** de la classe de [**\_ vérification CIM**](cim-check.md) évalue une vérification particulière.</span><span class="sxs-lookup"><span data-stu-id="81507-104">The **Invoke** method of the [**CIM\_Check**](cim-check.md) class evaluates a particular check.</span></span>

<span data-ttu-id="81507-105">Pour plus d’informations sur la façon dont la méthode évalue un contrôle particulier dans un contexte CIM, consultez les sous-classes de [**\_ vérification CIM**](cim-check.md) non abstraites.</span><span class="sxs-lookup"><span data-stu-id="81507-105">For more information about how the method evaluates a particular check in a CIM context, see the non-abstract [**CIM\_Check**](cim-check.md) subclasses.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="81507-106">Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées.</span><span class="sxs-lookup"><span data-stu-id="81507-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="81507-107">WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="81507-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="81507-108">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="81507-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="81507-109">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="81507-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="81507-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="81507-110">Syntax</span></span>


```mof
uint32 Invoke();
```



## <a name="parameters"></a><span data-ttu-id="81507-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="81507-111">Parameters</span></span>

<span data-ttu-id="81507-112">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="81507-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="81507-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="81507-113">Return value</span></span>

<span data-ttu-id="81507-114">Retourne la valeur 0 (zéro) en cas de réussite, 1 (un) si la méthode n’est pas prise en charge, et tout autre nombre pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="81507-114">Returns a value of 0 (zero) on success, 1 (one) if the method is not supported, and any other number to indicate an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="81507-115">Notes</span><span class="sxs-lookup"><span data-stu-id="81507-115">Remarks</span></span>

<span data-ttu-id="81507-116">Actuellement, cette méthode n’est pas implémentée par WMI.</span><span class="sxs-lookup"><span data-stu-id="81507-116">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="81507-117">Pour utiliser cette méthode, vous devez l’implémenter dans votre propre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="81507-117">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="81507-118">Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF.</span><span class="sxs-lookup"><span data-stu-id="81507-118">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="81507-119">Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="81507-119">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="81507-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="81507-120">Requirements</span></span>



| <span data-ttu-id="81507-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="81507-121">Requirement</span></span> | <span data-ttu-id="81507-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="81507-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="81507-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="81507-123">Minimum supported client</span></span><br/> | <span data-ttu-id="81507-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="81507-124">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="81507-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="81507-125">Minimum supported server</span></span><br/> | <span data-ttu-id="81507-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="81507-126">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="81507-127">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="81507-127">Namespace</span></span><br/>                | <span data-ttu-id="81507-128">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="81507-128">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="81507-129">MOF</span><span class="sxs-lookup"><span data-stu-id="81507-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="81507-130"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="81507-130"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="81507-131">DLL</span><span class="sxs-lookup"><span data-stu-id="81507-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="81507-132"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="81507-132"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81507-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="81507-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81507-134">**\_Vérification CIM**</span><span class="sxs-lookup"><span data-stu-id="81507-134">**CIM\_Check**</span></span>](invoke-method-in-class-cim-check.md)
</dt> <dt>

[<span data-ttu-id="81507-135">**\_Vérification CIM**</span><span class="sxs-lookup"><span data-stu-id="81507-135">**CIM\_Check**</span></span>](cim-check.md)
</dt> </dl>

 

