---
title: Méthode Media. isIdentical
description: La méthode isIdentical récupère une valeur indiquant si l’objet fourni est le même que celui actuel. | Méthode Media. isIdentical
ms.assetid: af3266d5-4ac2-4e8c-a9f6-44f7938e9c9d
keywords:
- méthode isIdentical lecteur Windows Media
- méthode isIdentical lecteur Windows Media, classe multimédia
- Classe multimédia lecteur Windows Media, méthode isIdentical
topic_type:
- apiref
api_name:
- Media.isIdentical
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 196487889c075938e763c2b2305b614cffb5f09f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530563"
---
# <a name="mediaisidentical-method"></a><span data-ttu-id="9be90-107">Méthode Media. isIdentical</span><span class="sxs-lookup"><span data-stu-id="9be90-107">Media.isIdentical method</span></span>

<span data-ttu-id="9be90-108">La méthode **isIdentical** récupère une valeur indiquant si l’objet fourni est le même que celui actuel.</span><span class="sxs-lookup"><span data-stu-id="9be90-108">The **isIdentical** method retrieves a value indicating whether the supplied object is the same as the current one.</span></span>

## <a name="syntax"></a><span data-ttu-id="9be90-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9be90-109">Syntax</span></span>


```JScript
bRetVal = Media.isIdentical(
  media
)
```



## <a name="parameters"></a><span data-ttu-id="9be90-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9be90-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9be90-111">*éléments multimédias* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9be90-111">*media* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9be90-112">Objet **multimédia** à comparer avec l’objet **multimédia** actuel.</span><span class="sxs-lookup"><span data-stu-id="9be90-112">**Media** object to compare with the current **Media** object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9be90-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9be90-113">Return value</span></span>

<span data-ttu-id="9be90-114">Cette méthode retourne une **valeur booléenne**.</span><span class="sxs-lookup"><span data-stu-id="9be90-114">This method returns a **Boolean**.</span></span>

## <a name="examples"></a><span data-ttu-id="9be90-115">Exemples</span><span class="sxs-lookup"><span data-stu-id="9be90-115">Examples</span></span>

<span data-ttu-id="9be90-116">L’exemple JScript suivant utilise un *média*. **isIdentical** pour vérifier si un élément multimédia nommé newMedia est le même que l’élément multimédia en cours.</span><span class="sxs-lookup"><span data-stu-id="9be90-116">The following JScript example uses *Media*.**isIdentical** to check whether a media item named newMedia is the same as the current media item.</span></span> <span data-ttu-id="9be90-117">Si ce n’est pas le cas, le nouvel élément multimédia est lu.</span><span class="sxs-lookup"><span data-stu-id="9be90-117">If they are not the same, the new media item is played.</span></span> <span data-ttu-id="9be90-118">Dans le cas contraire, le média actuel continue de s’exécuter sans interruption.</span><span class="sxs-lookup"><span data-stu-id="9be90-118">Otherwise, the current media continues to play uninterrupted.</span></span> <span data-ttu-id="9be90-119">L’objet **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="9be90-119">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Check the new media item to see if it matches the current one.
if (newMedia.isIdentical(Player.currentMedia) != true){

   // Change the current media to the new media item.
   Player.currentMedia = newMedia;

   // Play the new media item.
   Player.controls.play();
}

```



## <a name="requirements"></a><span data-ttu-id="9be90-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9be90-120">Requirements</span></span>



| <span data-ttu-id="9be90-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9be90-121">Requirement</span></span> | <span data-ttu-id="9be90-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="9be90-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9be90-123">Version</span><span class="sxs-lookup"><span data-stu-id="9be90-123">Version</span></span><br/> | <span data-ttu-id="9be90-124">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="9be90-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="9be90-125">DLL</span><span class="sxs-lookup"><span data-stu-id="9be90-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="9be90-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9be90-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9be90-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9be90-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9be90-128">**Objet Media**</span><span class="sxs-lookup"><span data-stu-id="9be90-128">**Media Object**</span></span>](media-object.md)
</dt> </dl>

 

 





