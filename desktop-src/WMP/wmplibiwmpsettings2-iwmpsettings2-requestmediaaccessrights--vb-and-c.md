---
title: Méthode IWMPSettings2 requestMediaAccessRights
description: La méthode requestMediaAccessRights demande un niveau d’accès spécifié à la bibliothèque. | Méthode IWMPSettings2 requestMediaAccessRights
ms.assetid: ea33852c-d1e0-45cf-8954-2a1e2fe51910
keywords:
- méthode requestMediaAccessRights lecteur Windows Media
- méthode requestMediaAccessRights lecteur Windows Media, interface IWMPSettings2
- Interface IWMPSettings2 lecteur Windows Media, méthode requestMediaAccessRights
topic_type:
- apiref
api_name:
- IWMPSettings2.requestMediaAccessRights
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c609afffc1d9b228d908d905e0eb1a6ef8741032
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533075"
---
# <a name="iwmpsettings2requestmediaaccessrights-method"></a><span data-ttu-id="c3f24-107">IWMPSettings2 :: requestMediaAccessRights, méthode</span><span class="sxs-lookup"><span data-stu-id="c3f24-107">IWMPSettings2::requestMediaAccessRights method</span></span>

<span data-ttu-id="c3f24-108">La méthode **requestMediaAccessRights** demande un niveau d’accès spécifié à la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="c3f24-108">The **requestMediaAccessRights** method requests a specified level of access to the library.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3f24-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c3f24-109">Syntax</span></span>


```CSharp
public System.Boolean requestMediaAccessRights(
  System.String bstrDesiredAccess
);
```


```VB

Public Function requestMediaAccessRights( _
  ByVal bstrDesiredAccess As System.String _
) As System.Boolean
Implements IWMPSettings2.requestMediaAccessRights
```





## <a name="parameters"></a><span data-ttu-id="c3f24-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c3f24-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3f24-111">*bstrDesiredAccess* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c3f24-111">*bstrDesiredAccess* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3f24-112">**System. String** qui est l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="c3f24-112">A **System.String** that is one of the following values.</span></span>



| <span data-ttu-id="c3f24-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="c3f24-113">Value</span></span> | <span data-ttu-id="c3f24-114">Description</span><span class="sxs-lookup"><span data-stu-id="c3f24-114">Description</span></span>                      |
|-------|----------------------------------|
| <span data-ttu-id="c3f24-115">aucun</span><span class="sxs-lookup"><span data-stu-id="c3f24-115">none</span></span>  | <span data-ttu-id="c3f24-116">Droits d’accès à l’élément actuel uniquement.</span><span class="sxs-lookup"><span data-stu-id="c3f24-116">Current item access rights only.</span></span> |
| <span data-ttu-id="c3f24-117">lire</span><span class="sxs-lookup"><span data-stu-id="c3f24-117">read</span></span>  | <span data-ttu-id="c3f24-118">Droits d’accès en lecture uniquement.</span><span class="sxs-lookup"><span data-stu-id="c3f24-118">Read access rights only.</span></span>         |
| <span data-ttu-id="c3f24-119">complet</span><span class="sxs-lookup"><span data-stu-id="c3f24-119">full</span></span>  | <span data-ttu-id="c3f24-120">Droits d’accès en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="c3f24-120">Read/Write access rights.</span></span>        |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3f24-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c3f24-121">Return value</span></span>

<span data-ttu-id="c3f24-122">**System. Boolean** qui indique si les droits d’accès demandés ont été accordés.</span><span class="sxs-lookup"><span data-stu-id="c3f24-122">A **System.Boolean** that indicates whether the requested access rights were granted.</span></span>

## <a name="remarks"></a><span data-ttu-id="c3f24-123">Notes</span><span class="sxs-lookup"><span data-stu-id="c3f24-123">Remarks</span></span>

<span data-ttu-id="c3f24-124">Une page Web doit tout d’abord demander l’autorisation à l’utilisateur de lire des informations ou d’écrire des données dans la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="c3f24-124">A webpage must first request permission from the user to read information from or write data to the library.</span></span> <span data-ttu-id="c3f24-125">L’appel de cette méthode invite l’utilisateur à utiliser une boîte de dialogue qui demande le niveau d’autorisation spécifié.</span><span class="sxs-lookup"><span data-stu-id="c3f24-125">Invoking this method prompts the user with a dialog box that requests the specified permission level.</span></span> <span data-ttu-id="c3f24-126">Cela signifie que certaines méthodes, propriétés et événements seront inaccessibles à partir du code si les droits d’accès appropriés n’ont pas été accordés.</span><span class="sxs-lookup"><span data-stu-id="c3f24-126">This means that certain methods, properties, and events will be inaccessible from code if the appropriate access rights have not been granted.</span></span> <span data-ttu-id="c3f24-127">Le niveau de droits d’accès actuel peut être récupéré à l’aide de **IWMPSettings2. mediaAccessRights**.</span><span class="sxs-lookup"><span data-stu-id="c3f24-127">The current access rights level can be retrieved by using **IWMPSettings2.mediaAccessRights**.</span></span>

<span data-ttu-id="c3f24-128">Les applications qui s’exécutent sur l’ordinateur de l’utilisateur ne sont pas tenues d’utiliser cette méthode.</span><span class="sxs-lookup"><span data-stu-id="c3f24-128">Applications running on the user's computer are not required to use this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3f24-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c3f24-129">Requirements</span></span>



| <span data-ttu-id="c3f24-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c3f24-130">Requirement</span></span> | <span data-ttu-id="c3f24-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="c3f24-131">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3f24-132">Version</span><span class="sxs-lookup"><span data-stu-id="c3f24-132">Version</span></span><br/>   | <span data-ttu-id="c3f24-133">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="c3f24-133">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="c3f24-134">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c3f24-134">Namespace</span></span><br/> | <span data-ttu-id="c3f24-135">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="c3f24-135">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="c3f24-136">Assembly</span><span class="sxs-lookup"><span data-stu-id="c3f24-136">Assembly</span></span><br/>  | <dl> <span data-ttu-id="c3f24-137"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="c3f24-137"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3f24-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c3f24-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3f24-139">**Interface IWMPSettings2 (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="c3f24-139">**IWMPSettings2 Interface (VB and C#)**</span></span>](iwmpsettings2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c3f24-140">**IWMPSettings2. mediaAccessRights (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="c3f24-140">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





