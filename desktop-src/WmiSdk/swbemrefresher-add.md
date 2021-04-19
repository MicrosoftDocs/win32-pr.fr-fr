---
description: La méthode SWbemRefresher. Add ajoute un nouvel objet SWbemRefreshableItem à la collection dans l’objet SWbemRefresher. Objet SWbemRefreshableItem à la collection dans l’objet SWbemRefresher.
ms.assetid: 92d11a18-1eed-4958-b74a-2f9de4907dd0
ms.tgt_platform: multiple
title: Méthode SWbemRefresher. Add (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher.Add
- ISWbemRefresher.Add
- ISWbemRefresher.Add
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: ebe9da221314252b2b143bf674cd7bb7177329b5
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106524769"
---
# <a name="swbemrefresheradd-method"></a><span data-ttu-id="99064-103">SWbemRefresher. Add, méthode</span><span class="sxs-lookup"><span data-stu-id="99064-103">SWbemRefresher.Add method</span></span>

<span data-ttu-id="99064-104">La méthode **SWbemRefresher. Add** ajoute un nouvel objet [**SWbemRefreshableItem**](swbemrefreshableitem.md) à la collection dans l’objet [**SWbemRefresher**](swbemrefresher.md) .</span><span class="sxs-lookup"><span data-stu-id="99064-104">The **SWbemRefresher.Add** method adds a new [**SWbemRefreshableItem**](swbemrefreshableitem.md) object to the collection in the [**SWbemRefresher**](swbemrefresher.md) object.</span></span>

<span data-ttu-id="99064-105">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="99064-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="99064-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="99064-106">Syntax</span></span>


```VB
objRefreshItem = .Add( _
  ByVal objWbemService, _
  ByVal strInstancePath, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedvalueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="99064-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="99064-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99064-108">*objWbemService*</span><span class="sxs-lookup"><span data-stu-id="99064-108">*objWbemService*</span></span> 
</dt> <dd>

<span data-ttu-id="99064-109">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="99064-109">Required.</span></span> <span data-ttu-id="99064-110">Objet [**SWbemServices**](swbemservices.md) qui représente une connexion à l’espace de noms dans lequel réside l’objet ajouté à l’actualisateur.</span><span class="sxs-lookup"><span data-stu-id="99064-110">An [**SWbemServices**](swbemservices.md) object that represents a connection to the namespace in which the object that is being added to the refresher resides.</span></span>

</dd> <dt>

<span data-ttu-id="99064-111">*strInstancePath*</span><span class="sxs-lookup"><span data-stu-id="99064-111">*strInstancePath*</span></span> 
</dt> <dd>

<span data-ttu-id="99064-112">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="99064-112">Required.</span></span> <span data-ttu-id="99064-113">Chaîne qui contient le chemin d’accès relatif de l’objet dans l’espace de noms.</span><span class="sxs-lookup"><span data-stu-id="99064-113">String that contains the relative path of the object in the namespace.</span></span> <span data-ttu-id="99064-114">Le chemin d’accès doit contenir une instance.</span><span class="sxs-lookup"><span data-stu-id="99064-114">The path must contain an instance.</span></span> <span data-ttu-id="99064-115">La propriété d' [**index**](swbemrefreshableitem-index.md) de la [**SWbemRefreshableItem**](swbemrefreshableitem.md) retournée représente l’index de l’objet dans la collection d’actualisations.</span><span class="sxs-lookup"><span data-stu-id="99064-115">The [**Index**](swbemrefreshableitem-index.md) property of the returned [**SWbemRefreshableItem**](swbemrefreshableitem.md) represents the index of the object in the refresher collection.</span></span>

</dd> <dt>

<span data-ttu-id="99064-116">*IFlags* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="99064-116">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="99064-117">Chaîne qui contient le chemin d’accès de l’objet pour lequel la méthode est exécutée.</span><span class="sxs-lookup"><span data-stu-id="99064-117">String that contains the object path of the object for which the method is executed.</span></span>

</dd> <dt>

<span data-ttu-id="99064-118">*objWbemNamedvalueSet* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="99064-118">*objWbemNamedvalueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="99064-119">En général, ce n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="99064-119">Typically, this is undefined.</span></span> <span data-ttu-id="99064-120">Dans le cas contraire, il s’agit d’un objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) dont les éléments représentent les informations de contexte qui peuvent être utilisées par le fournisseur qui sert la demande.</span><span class="sxs-lookup"><span data-stu-id="99064-120">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that services the request.</span></span> <span data-ttu-id="99064-121">Un fournisseur qui prend en charge ou requiert ces informations doit documenter les noms de valeur reconnus, le type de données de la valeur, les valeurs autorisées et la sémantique.</span><span class="sxs-lookup"><span data-stu-id="99064-121">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99064-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="99064-122">Return value</span></span>

<span data-ttu-id="99064-123">Si l’appel réussit, un objet [**SWbemRefreshableItem**](swbemrefreshableitem.md) qui contient un objet actualisable unique est retourné.</span><span class="sxs-lookup"><span data-stu-id="99064-123">If the call is successful, an [**SWbemRefreshableItem**](swbemrefreshableitem.md) object that contains a single refreshable object is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="99064-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="99064-124">Requirements</span></span>



| <span data-ttu-id="99064-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="99064-125">Requirement</span></span> | <span data-ttu-id="99064-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="99064-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="99064-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="99064-127">Minimum supported client</span></span><br/> | <span data-ttu-id="99064-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="99064-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="99064-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="99064-129">Minimum supported server</span></span><br/> | <span data-ttu-id="99064-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="99064-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="99064-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="99064-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="99064-132"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="99064-132"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="99064-133">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="99064-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="99064-134"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="99064-134"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="99064-135">DLL</span><span class="sxs-lookup"><span data-stu-id="99064-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="99064-136"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="99064-136"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="99064-137">CLSID</span><span class="sxs-lookup"><span data-stu-id="99064-137">CLSID</span></span><br/>                    | <span data-ttu-id="99064-138">CLSID \_ SWbemRefresher</span><span class="sxs-lookup"><span data-stu-id="99064-138">CLSID\_SWbemRefresher</span></span><br/>                                                        |
| <span data-ttu-id="99064-139">IID</span><span class="sxs-lookup"><span data-stu-id="99064-139">IID</span></span><br/>                      | <span data-ttu-id="99064-140">IID \_ ISWbemRefresher</span><span class="sxs-lookup"><span data-stu-id="99064-140">IID\_ISWbemRefresher</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="99064-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="99064-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99064-142">**SWbemRefresher**</span><span class="sxs-lookup"><span data-stu-id="99064-142">**SWbemRefresher**</span></span>](swbemrefresher.md)
</dt> </dl>

 

 




