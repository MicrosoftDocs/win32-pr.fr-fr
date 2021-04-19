---
title: Playlist. attributeName
description: La propriété attributeName récupère le nom d’un attribut au niveau d’un index spécifié.
ms.assetid: 3ff68e78-5fa1-4ca6-aa59-4752dbaee52a
keywords:
- Lecteur Windows Media playlist. attributeName
topic_type:
- apiref
api_name:
- Playlist.attributeName
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4560a7ca2766ee0bbadc582af878bca87e0834e2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542591"
---
# <a name="playlistattributename"></a><span data-ttu-id="b4d58-104">Playlist. attributeName</span><span class="sxs-lookup"><span data-stu-id="b4d58-104">Playlist.attributeName</span></span>

<span data-ttu-id="b4d58-105">La propriété **AttributeName** récupère le nom d’un attribut au niveau d’un index spécifié.</span><span class="sxs-lookup"><span data-stu-id="b4d58-105">The **attributeName** property retrieves the name of an attribute at a specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4d58-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b4d58-106">Syntax</span></span>

<span data-ttu-id="b4d58-107">*lecteur*. *currentPlaylist*. **AttributeName**( *index* )</span><span class="sxs-lookup"><span data-stu-id="b4d58-107">*player*.*currentPlaylist*.**attributeName**( *index* )</span></span>

## <a name="parameters"></a><span data-ttu-id="b4d58-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b4d58-108">Parameters</span></span>

<span data-ttu-id="b4d58-109">*index*</span><span class="sxs-lookup"><span data-stu-id="b4d58-109">*index*</span></span>

<span data-ttu-id="b4d58-110">**Nombre** (**long**) contenant l’index.</span><span class="sxs-lookup"><span data-stu-id="b4d58-110">**Number** (**long**) containing the index.</span></span>

## <a name="possible-values"></a><span data-ttu-id="b4d58-111">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="b4d58-111">Possible Values</span></span>

<span data-ttu-id="b4d58-112">Cette propriété est une **chaîne** en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="b4d58-112">This property is a read-only **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4d58-113">Notes</span><span class="sxs-lookup"><span data-stu-id="b4d58-113">Remarks</span></span>

<span data-ttu-id="b4d58-114">Le nombre d’attributs est récupéré par la propriété **attributeCount** .</span><span class="sxs-lookup"><span data-stu-id="b4d58-114">The number of attributes is retrieved by the **attributeCount** property.</span></span> <span data-ttu-id="b4d58-115">Avec un index donné, **AttributeName** retourne une **chaîne** qui peut être utilisée conjointement avec **setItemInfo** ou **getItemInfo** pour spécifier ou récupérer une valeur pour l’attribut.</span><span class="sxs-lookup"><span data-stu-id="b4d58-115">Given an index, **attributeName** returns a **String** that can be used in conjunction with **setItemInfo** or **getItemInfo** to specify or retrieve a value for the attribute.</span></span>

<span data-ttu-id="b4d58-116">Pour récupérer la valeur de cette propriété, l’accès en lecture à la bibliothèque est requis.</span><span class="sxs-lookup"><span data-stu-id="b4d58-116">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="b4d58-117">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="b4d58-117">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="b4d58-118">Pour plus d’informations sur les attributs pris en charge par le lecteur Windows Media, consultez la page [référence des attributs](attribute-reference.md)du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="b4d58-118">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

<span data-ttu-id="b4d58-119">Consultez la propriété [attributeCount](playlist-attributecount.md) pour obtenir un exemple de code qui utilise cette propriété.</span><span class="sxs-lookup"><span data-stu-id="b4d58-119">See the [attributeCount](playlist-attributecount.md) property for example code that uses this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4d58-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b4d58-120">Requirements</span></span>



| <span data-ttu-id="b4d58-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b4d58-121">Requirement</span></span> | <span data-ttu-id="b4d58-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="b4d58-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b4d58-123">Version</span><span class="sxs-lookup"><span data-stu-id="b4d58-123">Version</span></span><br/> | <span data-ttu-id="b4d58-124">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="b4d58-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="b4d58-125">DLL</span><span class="sxs-lookup"><span data-stu-id="b4d58-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="b4d58-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b4d58-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4d58-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b4d58-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4d58-128">**Objet playlist**</span><span class="sxs-lookup"><span data-stu-id="b4d58-128">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="b4d58-129">**Playlist. attributeCount**</span><span class="sxs-lookup"><span data-stu-id="b4d58-129">**Playlist.attributeCount**</span></span>](playlist-attributecount.md)
</dt> <dt>

[<span data-ttu-id="b4d58-130">**Playlist. getItemInfo**</span><span class="sxs-lookup"><span data-stu-id="b4d58-130">**Playlist.getItemInfo**</span></span>](playlist-getiteminfo.md)
</dt> <dt>

[<span data-ttu-id="b4d58-131">**Playlist. setItemInfo**</span><span class="sxs-lookup"><span data-stu-id="b4d58-131">**Playlist.setItemInfo**</span></span>](playlist-setiteminfo.md)
</dt> <dt>

[<span data-ttu-id="b4d58-132">**Paramètres. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="b4d58-132">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="b4d58-133">**Paramètres. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="b4d58-133">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





