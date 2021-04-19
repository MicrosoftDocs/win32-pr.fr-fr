---
title: Media. imageSourceHeight
description: La propriété ImageSourceHeight récupère la hauteur de l’élément multimédia actuel en pixels.
ms.assetid: fa98ec62-4c58-46ab-98f3-8017096d46d8
keywords:
- Media. imageSourceHeight Windows Media Player
topic_type:
- apiref
api_name:
- Media.imageSourceHeight
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0de364243e71c6653085b4c9c9ff81f148dc299d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106529900"
---
# <a name="mediaimagesourceheight"></a><span data-ttu-id="62c3d-104">Media. imageSourceHeight</span><span class="sxs-lookup"><span data-stu-id="62c3d-104">Media.imageSourceHeight</span></span>

<span data-ttu-id="62c3d-105">La propriété **ImageSourceHeight** récupère la hauteur de l’élément multimédia actuel en pixels.</span><span class="sxs-lookup"><span data-stu-id="62c3d-105">The **ImageSourceHeight** property retrieves the height of the current media item in pixels.</span></span>

## <a name="syntax"></a><span data-ttu-id="62c3d-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="62c3d-106">Syntax</span></span>

<span data-ttu-id="62c3d-107">*lecteur*. *currentMedia*. **imageSourceHeight**</span><span class="sxs-lookup"><span data-stu-id="62c3d-107">*player*.*currentMedia*.**imageSourceHeight**</span></span>

## <a name="possible-values"></a><span data-ttu-id="62c3d-108">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="62c3d-108">Possible Values</span></span>

<span data-ttu-id="62c3d-109">Cette propriété est un **nombre** en lecture seule (**long**).</span><span class="sxs-lookup"><span data-stu-id="62c3d-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="62c3d-110">Notes</span><span class="sxs-lookup"><span data-stu-id="62c3d-110">Remarks</span></span>

<span data-ttu-id="62c3d-111">Si l’élément multimédia n’est pas celui en cours, cette propriété retourne la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="62c3d-111">If the media item is not the current one, this property returns zero.</span></span>

<span data-ttu-id="62c3d-112">Pour récupérer la valeur de cette propriété, l’accès en lecture à la bibliothèque est requis.</span><span class="sxs-lookup"><span data-stu-id="62c3d-112">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="62c3d-113">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="62c3d-113">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="62c3d-114">Exemples</span><span class="sxs-lookup"><span data-stu-id="62c3d-114">Examples</span></span>

<span data-ttu-id="62c3d-115">L’exemple JScript suivant utilise *Media*. imageSourceHeight pour afficher la taille de l’image, en pixels, de l’élément multimédia actuel.</span><span class="sxs-lookup"><span data-stu-id="62c3d-115">The following JScript example uses *Media*.imageSourceHeight to display the image size, in pixels, of the current media item.</span></span> <span data-ttu-id="62c3d-116">Les informations sont imprimées dans un élément TEXTAREA HTML nommé Videote.</span><span class="sxs-lookup"><span data-stu-id="62c3d-116">The information is printed to an HTML TEXTAREA element named VideoSize.</span></span> <span data-ttu-id="62c3d-117">L’objet **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="62c3d-117">The **Player** object was created with ID = "player".</span></span>


```JScript
<!-- Create an event handler to refresh the information when the current media changes. -->
<SCRIPT LANGUAGE = "JScript"  FOR = Player  EVENT = OpenStateChange(NewState)>

// Test whether the new media item is open.
if (NewState == 13){

   // Store the height and width of the new media item.
   var Height = Player.currentMedia.imageSourceHeight;
   var Width =  Player.currentMedia.imageSourceWidth;

   // Erase the information in the text area.
   VideoSize.value = "";

   // Test whether an image is visible.
   if (Height != 0 && Width != 0)

      // Display the image size information.
      VideoSize.value = Width + " x " + Height;
}
</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="62c3d-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="62c3d-118">Requirements</span></span>



| <span data-ttu-id="62c3d-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="62c3d-119">Requirement</span></span> | <span data-ttu-id="62c3d-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="62c3d-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="62c3d-121">Version</span><span class="sxs-lookup"><span data-stu-id="62c3d-121">Version</span></span><br/> | <span data-ttu-id="62c3d-122">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="62c3d-122">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="62c3d-123">DLL</span><span class="sxs-lookup"><span data-stu-id="62c3d-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="62c3d-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="62c3d-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62c3d-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="62c3d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62c3d-126">**Objet Media**</span><span class="sxs-lookup"><span data-stu-id="62c3d-126">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="62c3d-127">**Player. currentMedia**</span><span class="sxs-lookup"><span data-stu-id="62c3d-127">**Player.currentMedia**</span></span>](player-currentmedia.md)
</dt> <dt>

[<span data-ttu-id="62c3d-128">**Paramètres. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="62c3d-128">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="62c3d-129">**Paramètres. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="62c3d-129">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





