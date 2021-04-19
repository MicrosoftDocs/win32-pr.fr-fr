---
title: Playlist. attributeCount
description: La propriété attributeCount récupère le nombre d’attributs associés à la sélection.
ms.assetid: 92063131-0118-4458-9122-0539628a9821
keywords:
- Lecteur Windows Media playlist. attributeCount
topic_type:
- apiref
api_name:
- Playlist.attributeCount
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e42d72e029f232bb6dabc074b412406a1bb64c7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528860"
---
# <a name="playlistattributecount"></a><span data-ttu-id="09a72-104">Playlist. attributeCount</span><span class="sxs-lookup"><span data-stu-id="09a72-104">Playlist.attributeCount</span></span>

<span data-ttu-id="09a72-105">La propriété **attributeCount** récupère le nombre d’attributs associés à la sélection.</span><span class="sxs-lookup"><span data-stu-id="09a72-105">The **attributeCount** property retrieves the number of attributes associated with the playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="09a72-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="09a72-106">Syntax</span></span>

<span data-ttu-id="09a72-107">*lecteur*. *currentPlaylist*. **attributeCount**</span><span class="sxs-lookup"><span data-stu-id="09a72-107">*player*.*currentPlaylist*.**attributeCount**</span></span>

## <a name="possible-values"></a><span data-ttu-id="09a72-108">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="09a72-108">Possible Values</span></span>

<span data-ttu-id="09a72-109">Cette propriété est un **nombre** en lecture seule (**long**).</span><span class="sxs-lookup"><span data-stu-id="09a72-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="09a72-110">Notes</span><span class="sxs-lookup"><span data-stu-id="09a72-110">Remarks</span></span>

<span data-ttu-id="09a72-111">Étant donné que les sélections peuvent provenir de nombreuses sources différentes, elles peuvent avoir plusieurs jeux de propriétés différents.</span><span class="sxs-lookup"><span data-stu-id="09a72-111">Because playlists can come from many different sources, they can have several different sets of properties.</span></span> <span data-ttu-id="09a72-112">Cette méthode récupère le nombre total de propriétés disponibles afin que les autres méthodes de l’objet **playlist** puissent y accéder.</span><span class="sxs-lookup"><span data-stu-id="09a72-112">This method retrieves the total number of properties available so that the other methods of the **Playlist** object can access them.</span></span>

<span data-ttu-id="09a72-113">Pour récupérer la valeur de cette propriété, l’accès en lecture à la bibliothèque est requis.</span><span class="sxs-lookup"><span data-stu-id="09a72-113">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="09a72-114">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="09a72-114">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="09a72-115">Pour plus d’informations sur les attributs pris en charge par le lecteur Windows Media, consultez la page [référence des attributs](attribute-reference.md)du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="09a72-115">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

## <a name="examples"></a><span data-ttu-id="09a72-116">Exemples</span><span class="sxs-lookup"><span data-stu-id="09a72-116">Examples</span></span>

<span data-ttu-id="09a72-117">L’exemple JScript suivant illustre l’utilisation de différentes propriétés et méthodes de la **sélection** et des objets **multimédias** .</span><span class="sxs-lookup"><span data-stu-id="09a72-117">The following JScript example illustrates how various properties and methods of the **Playlist** and **Media** objects are used.</span></span>


```JScript
function onLoad() {
    var display;
    var pl = player.currentPlaylist;

    pl.setItemInfo("custom playlist attribute", "changed");
    pl.item(0).setItemInfo("new custom attribute", "5");

    display = pl.attributeCount + " Playlist Attributes:\r\r";

    for (var i = 0; i < pl.attributeCount; ++i) {
        display = display + pl.attributeName(i) + ": ";
        display = display + pl.getItemInfo(pl.attributeName(i)) + "\r";
    }

    for (var j = 0; j < pl.count; ++j) {
        display = display + "\rTrack " + j + "\r"
        display = display + pl.item(j).attributeCount + " Attributes:\r\r";

        for (var k = 0; k < pl.item(j).attributeCount; ++k) {
            var it = pl.item(j);  // Media object
            display = display + it.getAttributeName(k) + ": ";
            display = display + it.getItemInfo(it.getAttributeName(k)) + "\r";
        }
    }

    myText.value = display;
}

```



## <a name="requirements"></a><span data-ttu-id="09a72-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="09a72-118">Requirements</span></span>



| <span data-ttu-id="09a72-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="09a72-119">Requirement</span></span> | <span data-ttu-id="09a72-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="09a72-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="09a72-121">Version</span><span class="sxs-lookup"><span data-stu-id="09a72-121">Version</span></span><br/> | <span data-ttu-id="09a72-122">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="09a72-122">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="09a72-123">DLL</span><span class="sxs-lookup"><span data-stu-id="09a72-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="09a72-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="09a72-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09a72-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="09a72-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09a72-126">**Objet playlist**</span><span class="sxs-lookup"><span data-stu-id="09a72-126">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="09a72-127">**Playlist. attributeName**</span><span class="sxs-lookup"><span data-stu-id="09a72-127">**Playlist.attributeName**</span></span>](playlist-attributename.md)
</dt> <dt>

[<span data-ttu-id="09a72-128">**Playlist. getItemInfo**</span><span class="sxs-lookup"><span data-stu-id="09a72-128">**Playlist.getItemInfo**</span></span>](playlist-getiteminfo.md)
</dt> <dt>

[<span data-ttu-id="09a72-129">**Playlist. setItemInfo**</span><span class="sxs-lookup"><span data-stu-id="09a72-129">**Playlist.setItemInfo**</span></span>](playlist-setiteminfo.md)
</dt> <dt>

[<span data-ttu-id="09a72-130">**Paramètres. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="09a72-130">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="09a72-131">**Paramètres. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="09a72-131">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





