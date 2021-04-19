---
title: Settings. requestMediaAccessRights, méthode
description: La méthode requestMediaAccessRights demande un niveau d’accès spécifié à la bibliothèque. | Settings. requestMediaAccessRights, méthode
ms.assetid: 076b749b-9b25-483c-aa1f-60fc4367e4e0
keywords:
- méthode requestMediaAccessRights lecteur Windows Media
- méthode requestMediaAccessRights lecteur Windows Media, classe de paramètres
- Classe de paramètres lecteur Windows Media, méthode requestMediaAccessRights
topic_type:
- apiref
api_name:
- Settings.requestMediaAccessRights
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abfeed45666ee1f63bf995b211030b0b840c4279
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535961"
---
# <a name="settingsrequestmediaaccessrights-method"></a><span data-ttu-id="ce8ab-107">Settings. requestMediaAccessRights, méthode</span><span class="sxs-lookup"><span data-stu-id="ce8ab-107">Settings.requestMediaAccessRights method</span></span>

<span data-ttu-id="ce8ab-108">La méthode **requestMediaAccessRights** demande un niveau d’accès spécifié à la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="ce8ab-108">The **requestMediaAccessRights** method requests a specified level of access to the library.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce8ab-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ce8ab-109">Syntax</span></span>


```JScript
bRetVal = Settings.requestMediaAccessRights(
  access
)
```



## <a name="parameters"></a><span data-ttu-id="ce8ab-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ce8ab-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce8ab-111">*accès* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ce8ab-111">*access* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce8ab-112">**Chaîne** spécifiant le niveau de droits d’accès souhaité.</span><span class="sxs-lookup"><span data-stu-id="ce8ab-112">**String** specifying the desired access rights level.</span></span> <span data-ttu-id="ce8ab-113">Contient l'une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="ce8ab-113">Contains one of the following values.</span></span>



| <span data-ttu-id="ce8ab-114">String</span><span class="sxs-lookup"><span data-stu-id="ce8ab-114">String</span></span> | <span data-ttu-id="ce8ab-115">Description</span><span class="sxs-lookup"><span data-stu-id="ce8ab-115">Description</span></span>                      |
|--------|----------------------------------|
| <span data-ttu-id="ce8ab-116">aucun</span><span class="sxs-lookup"><span data-stu-id="ce8ab-116">none</span></span>   | <span data-ttu-id="ce8ab-117">Droits d’accès à l’élément actuel uniquement.</span><span class="sxs-lookup"><span data-stu-id="ce8ab-117">Current item access rights only.</span></span> |
| <span data-ttu-id="ce8ab-118">lire</span><span class="sxs-lookup"><span data-stu-id="ce8ab-118">read</span></span>   | <span data-ttu-id="ce8ab-119">Droits d’accès en lecture uniquement.</span><span class="sxs-lookup"><span data-stu-id="ce8ab-119">Read access rights only.</span></span>         |
| <span data-ttu-id="ce8ab-120">complet</span><span class="sxs-lookup"><span data-stu-id="ce8ab-120">full</span></span>   | <span data-ttu-id="ce8ab-121">Droits d’accès en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="ce8ab-121">Read/Write access rights.</span></span>        |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce8ab-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ce8ab-122">Return value</span></span>

<span data-ttu-id="ce8ab-123">Cette méthode retourne une valeur **booléenne** indiquant si les droits d’accès demandés ont été accordés.</span><span class="sxs-lookup"><span data-stu-id="ce8ab-123">This method returns a **Boolean** value indicating whether the requested access rights were granted.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce8ab-124">Notes</span><span class="sxs-lookup"><span data-stu-id="ce8ab-124">Remarks</span></span>

<span data-ttu-id="ce8ab-125">Une page Web doit tout d’abord demander l’autorisation à l’utilisateur de lire des informations ou d’écrire des données dans la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="ce8ab-125">A webpage must first request permission from the user to read information from or write data to the library.</span></span> <span data-ttu-id="ce8ab-126">L’appel de cette méthode invite l’utilisateur à utiliser une boîte de dialogue qui demande le niveau d’autorisation spécifié.</span><span class="sxs-lookup"><span data-stu-id="ce8ab-126">Invoking this method prompts the user with a dialog box that requests the specified permission level.</span></span> <span data-ttu-id="ce8ab-127">Cela signifie que certaines méthodes, propriétés et événements seront inaccessibles à partir du code si les droits d’accès appropriés n’ont pas été accordés.</span><span class="sxs-lookup"><span data-stu-id="ce8ab-127">This means that certain methods, properties, and events will be inaccessible from code if the appropriate access rights have not been granted.</span></span> <span data-ttu-id="ce8ab-128">Le niveau de droits d’accès actuel peut être récupéré à l’aide de *paramètres*. **mediaAccessRights**.</span><span class="sxs-lookup"><span data-stu-id="ce8ab-128">The current access rights level can be retrieved using *Settings*.**mediaAccessRights**.</span></span>

<span data-ttu-id="ce8ab-129">**Windows Media Player 10 Mobile**: cette méthode retourne toujours **true**.</span><span class="sxs-lookup"><span data-stu-id="ce8ab-129">**Windows Media Player 10 Mobile**: This method always returns **true**.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce8ab-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ce8ab-130">Requirements</span></span>



| <span data-ttu-id="ce8ab-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ce8ab-131">Requirement</span></span> | <span data-ttu-id="ce8ab-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="ce8ab-132">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ce8ab-133">Version</span><span class="sxs-lookup"><span data-stu-id="ce8ab-133">Version</span></span><br/> | <span data-ttu-id="ce8ab-134">Lecteur Windows Media série 9 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="ce8ab-134">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="ce8ab-135">DLL</span><span class="sxs-lookup"><span data-stu-id="ce8ab-135">DLL</span></span><br/>     | <dl> <span data-ttu-id="ce8ab-136"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ce8ab-136"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce8ab-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ce8ab-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce8ab-138">**Settings (objet)**</span><span class="sxs-lookup"><span data-stu-id="ce8ab-138">**Settings Object**</span></span>](settings-object.md)
</dt> <dt>

[<span data-ttu-id="ce8ab-139">**Paramètres. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="ce8ab-139">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> </dl>

 

 





