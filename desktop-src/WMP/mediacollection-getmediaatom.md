---
title: Méthode MediaCollection. getMediaAtom
description: La méthode getMediaAtom récupère l’index auquel un attribut spécifié réside dans le jeu d’attributs disponibles.
ms.assetid: 17501a95-1196-43ff-9a4e-a78cf28e7a2d
keywords:
- méthode getMediaAtom lecteur Windows Media
- méthode getMediaAtom lecteur Windows Media, classe MediaCollection
- Classe MediaCollection lecteur Windows Media, méthode getMediaAtom
topic_type:
- apiref
api_name:
- MediaCollection.getMediaAtom
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16728b20c26b90c10f144f278f7dec24195b536a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542558"
---
# <a name="mediacollectiongetmediaatom-method"></a><span data-ttu-id="424fb-106">Méthode MediaCollection. getMediaAtom</span><span class="sxs-lookup"><span data-stu-id="424fb-106">MediaCollection.getMediaAtom method</span></span>

<span data-ttu-id="424fb-107">La méthode **getMediaAtom** récupère l’index auquel un attribut spécifié réside dans le jeu d’attributs disponibles.</span><span class="sxs-lookup"><span data-stu-id="424fb-107">The **getMediaAtom** method retrieves the index at which a specified attribute resides within the set of available attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="424fb-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="424fb-108">Syntax</span></span>


```JScript
retVal = MediaCollection.getMediaAtom(
  attribute
)
```



## <a name="parameters"></a><span data-ttu-id="424fb-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="424fb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="424fb-110">*attribut* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="424fb-110">*attribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="424fb-111">**Chaîne** contenant le nom de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="424fb-111">**String** containing the attribute name.</span></span> <span data-ttu-id="424fb-112">Pour plus d’informations sur les attributs pris en charge par le lecteur Windows Media, consultez la page [référence des attributs](attribute-reference.md)du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="424fb-112">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="424fb-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="424fb-113">Return value</span></span>

<span data-ttu-id="424fb-114">Cette méthode retourne un **nombre** (**long**).</span><span class="sxs-lookup"><span data-stu-id="424fb-114">This method returns a **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="424fb-115">Notes</span><span class="sxs-lookup"><span data-stu-id="424fb-115">Remarks</span></span>

<span data-ttu-id="424fb-116">Le numéro d’index récupéré avec cette méthode peut être passé au *média*. méthode **getItemInfoByAtom** pour accéder aux valeurs d’attribut.</span><span class="sxs-lookup"><span data-stu-id="424fb-116">The index number retrieved with this method can be passed to the *Media*.**getItemInfoByAtom** method to access attribute values.</span></span> <span data-ttu-id="424fb-117">Cette technique est généralement plus efficace lorsque vous utilisez des sélections volumineuses que l’accès à une valeur d’attribut par son nom par le biais d’un *média*. **getItemInfo** ou *Media*. **getItemInfoByType**.</span><span class="sxs-lookup"><span data-stu-id="424fb-117">This technique is generally more efficient when working with large playlists than accessing an attribute value by name through *Media*.**getItemInfo** or *Media*.**getItemInfoByType**.</span></span>

<span data-ttu-id="424fb-118">Pour utiliser cette méthode, l’accès en lecture à la bibliothèque est requis.</span><span class="sxs-lookup"><span data-stu-id="424fb-118">To use this method, read access to the library is required.</span></span> <span data-ttu-id="424fb-119">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="424fb-119">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="424fb-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="424fb-120">Requirements</span></span>



| <span data-ttu-id="424fb-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="424fb-121">Requirement</span></span> | <span data-ttu-id="424fb-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="424fb-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="424fb-123">Version</span><span class="sxs-lookup"><span data-stu-id="424fb-123">Version</span></span><br/> | <span data-ttu-id="424fb-124">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="424fb-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="424fb-125">DLL</span><span class="sxs-lookup"><span data-stu-id="424fb-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="424fb-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="424fb-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="424fb-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="424fb-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="424fb-128">**Media. getItemInfo**</span><span class="sxs-lookup"><span data-stu-id="424fb-128">**Media.getItemInfo**</span></span>](media-getiteminfo.md)
</dt> <dt>

[<span data-ttu-id="424fb-129">**Media. getItemInfoByAtom**</span><span class="sxs-lookup"><span data-stu-id="424fb-129">**Media.getItemInfoByAtom**</span></span>](media-getiteminfobyatom.md)
</dt> <dt>

[<span data-ttu-id="424fb-130">**Media. getItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="424fb-130">**Media.getItemInfoByType**</span></span>](media-getiteminfobytype.md)
</dt> <dt>

[<span data-ttu-id="424fb-131">**Objet MediaCollection**</span><span class="sxs-lookup"><span data-stu-id="424fb-131">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="424fb-132">**Paramètres. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="424fb-132">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="424fb-133">**Paramètres. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="424fb-133">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





