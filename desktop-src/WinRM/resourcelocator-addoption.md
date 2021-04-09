---
title: Méthode ResourceLocator. AddOption (WSManDisp. h)
description: Ajoute les données supplémentaires requises pour traiter la demande. Par exemple, certains fournisseurs WMI peuvent nécessiter un objet IWbemContext ou SWbemNamedValueSet avec des informations spécifiques au fournisseur.
ms.assetid: c85949fc-41e7-47eb-8aab-9b456490bc81
ms.tgt_platform: multiple
keywords:
- Windows Remote Management de la méthode AddOption
- Méthode AddOption Windows Remote Management, objet ResourceLocator
- Windows Remote Management objet ResourceLocator, méthode AddOption
topic_type:
- apiref
api_name:
- ResourceLocator.AddOption
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 882f400dd2c59d2395dd2755846245f4e4ad385e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032509"
---
# <a name="resourcelocatoraddoption-method"></a><span data-ttu-id="32353-107">Méthode ResourceLocator. AddOption</span><span class="sxs-lookup"><span data-stu-id="32353-107">ResourceLocator.AddOption method</span></span>

<span data-ttu-id="32353-108">Ajoute les données supplémentaires requises pour traiter la demande.</span><span class="sxs-lookup"><span data-stu-id="32353-108">Adds additional data required to process the request.</span></span> <span data-ttu-id="32353-109">Par exemple, certains fournisseurs WMI peuvent nécessiter un objet [**IWbemContext**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcontext) ou [**SWbemNamedValueSet**](/windows/desktop/WmiSdk/swbemnamedvalueset) avec des informations spécifiques au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="32353-109">For example, some WMI providers may require an [**IWbemContext**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcontext) or [**SWbemNamedValueSet**](/windows/desktop/WmiSdk/swbemnamedvalueset) object with provider-specific information.</span></span> <span data-ttu-id="32353-110">Vous pouvez fournir un objet [**ResourceLocator**](resourcelocator.md) au lieu de spécifier un URI de ressource dans les opérations d’objet de [**session**](session.md) , telles que [**session. obtenir**](session-get.md), [**session. put**](session-put.md)ou [**session. Enumerate**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="32353-110">You can provide a [**ResourceLocator**](resourcelocator.md) object instead of specifying a resource URI in [**Session**](session.md) object operations such as [**Session.Get**](session-get.md), [**Session.Put**](session-put.md), or [**Session.Enumerate**](session-enumerate.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="32353-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="32353-111">Syntax</span></span>


```VB
ResourceLocator.AddOption( _
  ByVal OptionName, _
  ByVal OptionValue, _
  ByVal mustComply _
)
```



## <a name="parameters"></a><span data-ttu-id="32353-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="32353-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32353-113">*Nomoptist* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="32353-113">*OptionName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32353-114">Nom (clé) de l’objet de données facultatif.</span><span class="sxs-lookup"><span data-stu-id="32353-114">The name (key) of the optional data object.</span></span>

</dd> <dt>

<span data-ttu-id="32353-115">*ValeurContrôle* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="32353-115">*OptionValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32353-116">Valeur fournie pour l’objet de données facultatif.</span><span class="sxs-lookup"><span data-stu-id="32353-116">A value supplied for the optional data object.</span></span>

</dd> <dt>

<span data-ttu-id="32353-117">*mustComply* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="32353-117">*mustComply* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32353-118">Indicateur qui indique que l’option doit être traitée.</span><span class="sxs-lookup"><span data-stu-id="32353-118">A flag that indicates the option must be processed.</span></span> <span data-ttu-id="32353-119">La valeur par défaut est **false** (0).</span><span class="sxs-lookup"><span data-stu-id="32353-119">The default is **False** (0).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32353-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="32353-120">Return value</span></span>

<span data-ttu-id="32353-121">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="32353-121">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="32353-122">Notes</span><span class="sxs-lookup"><span data-stu-id="32353-122">Remarks</span></span>

<span data-ttu-id="32353-123">**IWSManResourceLocator :: AddOption** est la méthode C++ correspondante.</span><span class="sxs-lookup"><span data-stu-id="32353-123">**IWSManResourceLocator::AddOption** is the corresponding C++ method.</span></span>

## <a name="requirements"></a><span data-ttu-id="32353-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="32353-124">Requirements</span></span>



| <span data-ttu-id="32353-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="32353-125">Requirement</span></span> | <span data-ttu-id="32353-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="32353-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="32353-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="32353-127">Minimum supported client</span></span><br/> | <span data-ttu-id="32353-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="32353-128">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="32353-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="32353-129">Minimum supported server</span></span><br/> | <span data-ttu-id="32353-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="32353-130">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="32353-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="32353-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="32353-132"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="32353-132"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="32353-133">MIDL</span><span class="sxs-lookup"><span data-stu-id="32353-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="32353-134"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="32353-134"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="32353-135">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="32353-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="32353-136"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="32353-136"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="32353-137">DLL</span><span class="sxs-lookup"><span data-stu-id="32353-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="32353-138"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="32353-138"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="32353-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="32353-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32353-140">**ResourceLocator**</span><span class="sxs-lookup"><span data-stu-id="32353-140">**ResourceLocator**</span></span>](resourcelocator.md)
</dt> </dl>

 

