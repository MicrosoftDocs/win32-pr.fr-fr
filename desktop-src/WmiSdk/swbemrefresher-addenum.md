---
description: Ajoute un nouvel énumérateur à l’objet SWbemRefresher. Cet énumérateur concerne toutes les instances de la classe qui est spécifiée dans le paramètre strClass.
ms.assetid: 0fa22a47-4050-43ae-aad3-3a8ebbf5e9b2
ms.tgt_platform: multiple
title: Méthode SWbemRefresher. AddEnum (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher.AddEnum
- ISWbemRefresher.AddEnum
- ISWbemRefresher.AddEnum
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: cffa406a3a45869038f5e6fed12b23b6b84fde27
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103761401"
---
# <a name="swbemrefresheraddenum-method"></a><span data-ttu-id="599b1-104">Méthode SWbemRefresher. AddEnum</span><span class="sxs-lookup"><span data-stu-id="599b1-104">SWbemRefresher.AddEnum method</span></span>

<span data-ttu-id="599b1-105">La méthode **SWbemRefresher. AddEnum** ajoute un nouvel énumérateur à l’objet [**SWbemRefresher**](swbemrefresher.md) .</span><span class="sxs-lookup"><span data-stu-id="599b1-105">The **SWbemRefresher.AddEnum** method adds a new enumerator to the [**SWbemRefresher**](swbemrefresher.md) object.</span></span> <span data-ttu-id="599b1-106">Cet énumérateur concerne toutes les instances de la classe qui est spécifiée dans le paramètre *strClass* .</span><span class="sxs-lookup"><span data-stu-id="599b1-106">This enumerator is for all the instances of the class that is specified in the *strClass* parameter.</span></span>

<span data-ttu-id="599b1-107">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="599b1-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="599b1-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="599b1-108">Syntax</span></span>


```VB
objRefreshEnum = .AddEnum( _
  ByVal objWbemService, _
  ByVal strClass, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedvalueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="599b1-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="599b1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="599b1-110">*objWbemService*</span><span class="sxs-lookup"><span data-stu-id="599b1-110">*objWbemService*</span></span> 
</dt> <dd>

<span data-ttu-id="599b1-111">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="599b1-111">Required.</span></span> <span data-ttu-id="599b1-112">Objet [**SWbemServices**](swbemservices.md) qui représente une connexion à l’espace de noms dans lequel réside l’objet ajouté à l’actualisateur.</span><span class="sxs-lookup"><span data-stu-id="599b1-112">An [**SWbemServices**](swbemservices.md) object that represents a connection to the namespace in which the object that is being added to the refresher resides.</span></span>

</dd> <dt>

<span data-ttu-id="599b1-113">*strClass*</span><span class="sxs-lookup"><span data-stu-id="599b1-113">*strClass*</span></span> 
</dt> <dd>

<span data-ttu-id="599b1-114">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="599b1-114">Required.</span></span> <span data-ttu-id="599b1-115">Chaîne qui contient la classe ajoutée à l’actualisateur.</span><span class="sxs-lookup"><span data-stu-id="599b1-115">String that contains the class that is being added to the refresher.</span></span> <span data-ttu-id="599b1-116">Cette classe est utilisée comme un énumérateur des instances de la classe.</span><span class="sxs-lookup"><span data-stu-id="599b1-116">This class is used as an enumerator of the instances of the class.</span></span> <span data-ttu-id="599b1-117">La propriété d' [**index**](swbemrefreshableitem-index.md) de la [**SWbemRefreshableItem**](swbemrefreshableitem.md) retournée représente l’index de l’énumérateur dans la collection d’actualisations.</span><span class="sxs-lookup"><span data-stu-id="599b1-117">The [**Index**](swbemrefreshableitem-index.md) property of the returned [**SWbemRefreshableItem**](swbemrefreshableitem.md) represents the index of the enumerator in the refresher collection.</span></span>

</dd> <dt>

<span data-ttu-id="599b1-118">*IFlags* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="599b1-118">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="599b1-119">Chaîne qui contient le chemin d’accès de l’objet pour lequel la méthode est exécutée.</span><span class="sxs-lookup"><span data-stu-id="599b1-119">String that contains the object path of the object for which the method is executed.</span></span>

</dd> <dt>

<span data-ttu-id="599b1-120">*objWbemNamedvalueSet* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="599b1-120">*objWbemNamedvalueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="599b1-121">En général, ce n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="599b1-121">Typically, this is undefined.</span></span> <span data-ttu-id="599b1-122">Dans le cas contraire, il s’agit d’un objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) dont les éléments représentent les informations de contexte qui peuvent être utilisées par le fournisseur qui sert la demande.</span><span class="sxs-lookup"><span data-stu-id="599b1-122">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that services the request.</span></span> <span data-ttu-id="599b1-123">Un fournisseur qui prend en charge ou requiert ces informations doit documenter les noms de valeur reconnus, le type de données de la valeur, les valeurs autorisées et la sémantique.</span><span class="sxs-lookup"><span data-stu-id="599b1-123">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="599b1-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="599b1-124">Return value</span></span>

<span data-ttu-id="599b1-125">Si l’appel réussit, un objet [**SWbemRefreshableItem**](swbemrefreshableitem.md) qui contient un énumérateur pour toutes les instances de la classe spécifiée est retourné.</span><span class="sxs-lookup"><span data-stu-id="599b1-125">If the call is successful, an [**SWbemRefreshableItem**](swbemrefreshableitem.md) object that contains an enumerator for all the instances for the specified class is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="599b1-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="599b1-126">Requirements</span></span>



| <span data-ttu-id="599b1-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="599b1-127">Requirement</span></span> | <span data-ttu-id="599b1-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="599b1-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="599b1-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="599b1-129">Minimum supported client</span></span><br/> | <span data-ttu-id="599b1-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="599b1-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="599b1-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="599b1-131">Minimum supported server</span></span><br/> | <span data-ttu-id="599b1-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="599b1-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="599b1-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="599b1-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="599b1-134"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="599b1-134"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="599b1-135">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="599b1-135">Type library</span></span><br/>             | <dl> <span data-ttu-id="599b1-136"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="599b1-136"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="599b1-137">DLL</span><span class="sxs-lookup"><span data-stu-id="599b1-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="599b1-138"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="599b1-138"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="599b1-139">CLSID</span><span class="sxs-lookup"><span data-stu-id="599b1-139">CLSID</span></span><br/>                    | <span data-ttu-id="599b1-140">CLSID \_ SWbemRefresher</span><span class="sxs-lookup"><span data-stu-id="599b1-140">CLSID\_SWbemRefresher</span></span><br/>                                                        |
| <span data-ttu-id="599b1-141">IID</span><span class="sxs-lookup"><span data-stu-id="599b1-141">IID</span></span><br/>                      | <span data-ttu-id="599b1-142">IID \_ ISWbemRefresher</span><span class="sxs-lookup"><span data-stu-id="599b1-142">IID\_ISWbemRefresher</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="599b1-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="599b1-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="599b1-144">**SWbemRefresher**</span><span class="sxs-lookup"><span data-stu-id="599b1-144">**SWbemRefresher**</span></span>](swbemrefresher.md)
</dt> </dl>

 

 




