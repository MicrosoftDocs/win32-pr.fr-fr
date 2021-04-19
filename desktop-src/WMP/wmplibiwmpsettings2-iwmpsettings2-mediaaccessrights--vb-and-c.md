---
title: IWMPSettings2 propriété mediaAccessRights
description: La propriété mediaAccessRights obtient une valeur indiquant les autorisations actuellement accordées pour l’accès à la bibliothèque.
ms.assetid: c4289a2c-e343-405d-9bf5-0e97f6617916
keywords:
- propriété mediaAccessRights lecteur Windows Media
- propriété mediaAccessRights lecteur Windows Media, interface IWMPSettings2
- Interface IWMPSettings2 lecteur Windows Media, propriété mediaAccessRights
topic_type:
- apiref
api_name:
- IWMPSettings2.mediaAccessRights
- IWMPSettings2.get_mediaAccessRights
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96cca06b9618767e7748b4b1308ed97860c7c80b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532704"
---
# <a name="iwmpsettings2mediaaccessrights-property"></a><span data-ttu-id="2ab28-106">IWMPSettings2 :: mediaAccessRights, propriété</span><span class="sxs-lookup"><span data-stu-id="2ab28-106">IWMPSettings2::mediaAccessRights property</span></span>

<span data-ttu-id="2ab28-107">La propriété **mediaAccessRights** obtient une valeur indiquant les autorisations actuellement accordées pour l’accès à la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="2ab28-107">The **mediaAccessRights** property gets a value indicating the permissions currently granted for library access.</span></span>

<span data-ttu-id="2ab28-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="2ab28-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ab28-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2ab28-109">Syntax</span></span>


```CSharp
public System.String mediaAccessRights {get;}
```


```VB

Public ReadOnly Property mediaAccessRights As System.String
```





## <a name="property-value"></a><span data-ttu-id="2ab28-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="2ab28-110">Property value</span></span>

<span data-ttu-id="2ab28-111">**System. String** qui est l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="2ab28-111">A **System.String** that is one of the following values.</span></span>



| <span data-ttu-id="2ab28-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="2ab28-112">Value</span></span> | <span data-ttu-id="2ab28-113">Description</span><span class="sxs-lookup"><span data-stu-id="2ab28-113">Description</span></span>                      |
|-------|----------------------------------|
| <span data-ttu-id="2ab28-114">aucun</span><span class="sxs-lookup"><span data-stu-id="2ab28-114">none</span></span>  | <span data-ttu-id="2ab28-115">Droits d’accès à l’élément actuel uniquement.</span><span class="sxs-lookup"><span data-stu-id="2ab28-115">Current item access rights only.</span></span> |
| <span data-ttu-id="2ab28-116">lire</span><span class="sxs-lookup"><span data-stu-id="2ab28-116">read</span></span>  | <span data-ttu-id="2ab28-117">Droits d’accès en lecture uniquement.</span><span class="sxs-lookup"><span data-stu-id="2ab28-117">Read access rights only.</span></span>         |
| <span data-ttu-id="2ab28-118">complet</span><span class="sxs-lookup"><span data-stu-id="2ab28-118">full</span></span>  | <span data-ttu-id="2ab28-119">Droits d’accès en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="2ab28-119">Read/Write access rights.</span></span>        |



 

## <a name="remarks"></a><span data-ttu-id="2ab28-120">Notes</span><span class="sxs-lookup"><span data-stu-id="2ab28-120">Remarks</span></span>

<span data-ttu-id="2ab28-121">Une page Web doit tout d’abord demander l’autorisation à l’utilisateur de lire des informations ou d’écrire des données dans la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="2ab28-121">A webpage must first request permission from the user to read information from or write data to the library.</span></span> <span data-ttu-id="2ab28-122">Cela signifie que certaines méthodes, propriétés et événements seront inaccessibles à partir du code si les droits d’accès appropriés n’ont pas été accordés.</span><span class="sxs-lookup"><span data-stu-id="2ab28-122">This means that certain methods, properties, and events will be inaccessible from code if the appropriate access rights have not been granted.</span></span> <span data-ttu-id="2ab28-123">Pour obtenir les droits d’accès, l’application appelle **IWMPSettings2. obtenir \_ requestMediaAccessRights**, en passant un paramètre qui spécifie le niveau de droits d’accès souhaité.</span><span class="sxs-lookup"><span data-stu-id="2ab28-123">To obtain access rights, the application calls **IWMPSettings2.get\_requestMediaAccessRights**, passing a parameter that specifies the desired access rights level.</span></span>

<span data-ttu-id="2ab28-124">Les applications qui s’exécutent sur l’ordinateur de l’utilisateur disposent toujours de droits d’accès complets.</span><span class="sxs-lookup"><span data-stu-id="2ab28-124">Applications running on the user's computer always have full access rights.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ab28-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2ab28-125">Requirements</span></span>



| <span data-ttu-id="2ab28-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2ab28-126">Requirement</span></span> | <span data-ttu-id="2ab28-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="2ab28-127">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ab28-128">Version</span><span class="sxs-lookup"><span data-stu-id="2ab28-128">Version</span></span><br/>   | <span data-ttu-id="2ab28-129">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="2ab28-129">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="2ab28-130">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="2ab28-130">Namespace</span></span><br/> | <span data-ttu-id="2ab28-131">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="2ab28-131">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="2ab28-132">Assembly</span><span class="sxs-lookup"><span data-stu-id="2ab28-132">Assembly</span></span><br/>  | <dl> <span data-ttu-id="2ab28-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="2ab28-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ab28-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2ab28-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ab28-135">**Interface IWMPSettings2 (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="2ab28-135">**IWMPSettings2 Interface (VB and C#)**</span></span>](iwmpsettings2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2ab28-136">**IWMPSettings2. requestMediaAccessRights (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="2ab28-136">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





