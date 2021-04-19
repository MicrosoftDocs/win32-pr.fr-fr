---
title: Media. imageSourceWidth
description: La propriété imageSourceWidth récupère la largeur de l’élément multimédia actuel en pixels.
ms.assetid: 6559bd51-cec2-4fc6-aab8-f2fdd1d59bae
keywords:
- Media. imageSourceWidth Windows Media Player
topic_type:
- apiref
api_name:
- Media.imageSourceWidth
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff2a3fef7b74a3d033b058f0afd1f6eece007bd7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528810"
---
# <a name="mediaimagesourcewidth"></a><span data-ttu-id="1827f-104">Media. imageSourceWidth</span><span class="sxs-lookup"><span data-stu-id="1827f-104">Media.imageSourceWidth</span></span>

<span data-ttu-id="1827f-105">La propriété **imageSourceWidth** récupère la largeur de l’élément multimédia actuel en pixels.</span><span class="sxs-lookup"><span data-stu-id="1827f-105">The **imageSourceWidth** property retrieves the width of the current media item in pixels.</span></span>

## <a name="syntax"></a><span data-ttu-id="1827f-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1827f-106">Syntax</span></span>

<span data-ttu-id="1827f-107">*lecteur*. *currentMedia*. **imageSourceWidth**</span><span class="sxs-lookup"><span data-stu-id="1827f-107">*player*.*currentMedia*.**imageSourceWidth**</span></span>

## <a name="possible-values"></a><span data-ttu-id="1827f-108">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="1827f-108">Possible Values</span></span>

<span data-ttu-id="1827f-109">Cette propriété est un **nombre** en lecture seule (**long**).</span><span class="sxs-lookup"><span data-stu-id="1827f-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="1827f-110">Notes</span><span class="sxs-lookup"><span data-stu-id="1827f-110">Remarks</span></span>

<span data-ttu-id="1827f-111">Si l’élément multimédia n’est pas celui en cours, cette propriété retourne la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="1827f-111">If the media item is not the current one, this property returns zero.</span></span>

<span data-ttu-id="1827f-112">Pour récupérer la valeur de cette propriété, l’accès en lecture à la bibliothèque est requis.</span><span class="sxs-lookup"><span data-stu-id="1827f-112">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="1827f-113">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="1827f-113">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="1827f-114">Exemples</span><span class="sxs-lookup"><span data-stu-id="1827f-114">Examples</span></span>

<span data-ttu-id="1827f-115">L’exemple JScript suivant utilise un *média*. **imageSourceWidth** pour afficher la taille de l’image, en pixels, de l' **élément multimédia actuel. Les informations sont imprimées dans un élément TEXTAREA HTML nommé Videote. L’objet Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="1827f-115">The following JScript example uses *Media*.**imageSourceWidth** to display the image size, in pixels, of the **current media item. The information is printed to an HTML TEXTAREA element named VideoSize. The Player** object was created with ID = "player".</span></span>


```JScript
<!-- Create an event handler to refresh the information when the current media changes. -->
<SCRIPT LANGUAGE = "JScript"  FOR = "Player"  EVENT = OpenStateChange(NewState)>

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



## <a name="requirements"></a><span data-ttu-id="1827f-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1827f-116">Requirements</span></span>



| <span data-ttu-id="1827f-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1827f-117">Requirement</span></span> | <span data-ttu-id="1827f-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="1827f-118">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1827f-119">Version</span><span class="sxs-lookup"><span data-stu-id="1827f-119">Version</span></span><br/> | <span data-ttu-id="1827f-120">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="1827f-120">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="1827f-121">DLL</span><span class="sxs-lookup"><span data-stu-id="1827f-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="1827f-122"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1827f-122"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1827f-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1827f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1827f-124">**Objet Media**</span><span class="sxs-lookup"><span data-stu-id="1827f-124">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="1827f-125">**Player. currentMedia**</span><span class="sxs-lookup"><span data-stu-id="1827f-125">**Player.currentMedia**</span></span>](player-currentmedia.md)
</dt> <dt>

[<span data-ttu-id="1827f-126">**Paramètres. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="1827f-126">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="1827f-127">**Paramètres. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="1827f-127">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





