---
title: Paramètres. mediaAccessRights
description: La propriété mediaAccessRights récupère une valeur indiquant les droits actuellement octroyés pour l’accès à la bibliothèque.
ms.assetid: 744e696d-29d2-44b1-a296-5b5d007b689f
keywords:
- Settings. mediaAccessRights Windows Media Player
topic_type:
- apiref
api_name:
- Settings.mediaAccessRights
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36bcfb667a1aa09e84ae90324736291d421a3941
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528492"
---
# <a name="settingsmediaaccessrights"></a><span data-ttu-id="316d7-104">Paramètres. mediaAccessRights</span><span class="sxs-lookup"><span data-stu-id="316d7-104">Settings.mediaAccessRights</span></span>

<span data-ttu-id="316d7-105">La propriété **mediaAccessRights** récupère une valeur indiquant les droits actuellement octroyés pour l’accès à la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="316d7-105">The **mediaAccessRights** property retrieves a value indicating the rights currently granted for library access.</span></span>

## <a name="syntax"></a><span data-ttu-id="316d7-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="316d7-106">Syntax</span></span>

<span data-ttu-id="316d7-107">Player. Settings. mediaAccessRights</span><span class="sxs-lookup"><span data-stu-id="316d7-107">player.settings.mediaAccessRights</span></span>

## <a name="possible-values"></a><span data-ttu-id="316d7-108">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="316d7-108">Possible Values</span></span>

<span data-ttu-id="316d7-109">Cette propriété est une **chaîne** en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="316d7-109">This property is a read-only **String**.</span></span>



| <span data-ttu-id="316d7-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="316d7-110">Value</span></span> | <span data-ttu-id="316d7-111">Description</span><span class="sxs-lookup"><span data-stu-id="316d7-111">Description</span></span>                      |
|-------|----------------------------------|
| <span data-ttu-id="316d7-112">aucun</span><span class="sxs-lookup"><span data-stu-id="316d7-112">none</span></span>  | <span data-ttu-id="316d7-113">Droits d’accès à l’élément actuel uniquement.</span><span class="sxs-lookup"><span data-stu-id="316d7-113">Current item access rights only.</span></span> |
| <span data-ttu-id="316d7-114">lire</span><span class="sxs-lookup"><span data-stu-id="316d7-114">read</span></span>  | <span data-ttu-id="316d7-115">Droits d’accès en lecture uniquement.</span><span class="sxs-lookup"><span data-stu-id="316d7-115">Read access rights only.</span></span>         |
| <span data-ttu-id="316d7-116">complet</span><span class="sxs-lookup"><span data-stu-id="316d7-116">full</span></span>  | <span data-ttu-id="316d7-117">Droits d’accès en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="316d7-117">Read/Write access rights.</span></span>        |



 

## <a name="remarks"></a><span data-ttu-id="316d7-118">Notes</span><span class="sxs-lookup"><span data-stu-id="316d7-118">Remarks</span></span>

<span data-ttu-id="316d7-119">Une page Web doit tout d’abord demander l’autorisation à l’utilisateur de lire des informations ou d’écrire des données dans la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="316d7-119">A webpage must first request permission from the user to read information from or write data to the library.</span></span> <span data-ttu-id="316d7-120">Cela signifie que certaines méthodes, propriétés et événements seront inaccessibles à partir du code si les droits d’accès appropriés n’ont pas été accordés.</span><span class="sxs-lookup"><span data-stu-id="316d7-120">This means that certain methods, properties, and events will be inaccessible from code if the appropriate access rights have not been granted.</span></span> <span data-ttu-id="316d7-121">Pour obtenir les droits d’accès, l’application appelle des *paramètres*. **requestMediaAccessRights**, en passant un paramètre qui spécifie le niveau de droits d’accès souhaité.</span><span class="sxs-lookup"><span data-stu-id="316d7-121">To obtain access rights, the application calls *Settings*.**requestMediaAccessRights**, passing a parameter that specifies the desired access rights level.</span></span>

<span data-ttu-id="316d7-122">**Windows Media Player 10 Mobile**: cette propriété retourne toujours **Full**.</span><span class="sxs-lookup"><span data-stu-id="316d7-122">**Windows Media Player 10 Mobile**: This property always returns **full**.</span></span>

## <a name="requirements"></a><span data-ttu-id="316d7-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="316d7-123">Requirements</span></span>



| <span data-ttu-id="316d7-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="316d7-124">Requirement</span></span> | <span data-ttu-id="316d7-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="316d7-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="316d7-126">Version</span><span class="sxs-lookup"><span data-stu-id="316d7-126">Version</span></span><br/> | <span data-ttu-id="316d7-127">Lecteur Windows Media série 9 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="316d7-127">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="316d7-128">DLL</span><span class="sxs-lookup"><span data-stu-id="316d7-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="316d7-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="316d7-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="316d7-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="316d7-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="316d7-131">**Settings (objet)**</span><span class="sxs-lookup"><span data-stu-id="316d7-131">**Settings Object**</span></span>](settings-object.md)
</dt> <dt>

[<span data-ttu-id="316d7-132">**Paramètres. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="316d7-132">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





