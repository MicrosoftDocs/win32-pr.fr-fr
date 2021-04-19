---
title: Méthode playlist. getItemInfo
description: La méthode getItemInfo récupère la valeur d’un attribut playlist.
ms.assetid: 888c0ab7-c225-4246-b1a1-94da7e19fa1a
keywords:
- méthode getItemInfo lecteur Windows Media
- méthode getItemInfo lecteur Windows Media, classe de sélection
- Classe de sélection lecteur Windows Media, méthode getItemInfo
topic_type:
- apiref
api_name:
- Playlist.getItemInfo
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b1151528d6cf4e36aaed1cb4dc48a70f4083c4e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106527287"
---
# <a name="playlistgetiteminfo-method"></a><span data-ttu-id="32e0d-106">Méthode playlist. getItemInfo</span><span class="sxs-lookup"><span data-stu-id="32e0d-106">Playlist.getItemInfo method</span></span>

<span data-ttu-id="32e0d-107">La méthode **getItemInfo** récupère la valeur d’un attribut playlist.</span><span class="sxs-lookup"><span data-stu-id="32e0d-107">The **getItemInfo** method retrieves the value of a playlist attribute.</span></span>

## <a name="syntax"></a><span data-ttu-id="32e0d-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="32e0d-108">Syntax</span></span>


```JScript
strRetVal = Playlist.getItemInfo(
  name
)
```



## <a name="parameters"></a><span data-ttu-id="32e0d-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="32e0d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32e0d-110">*nom* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="32e0d-110">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32e0d-111">**Chaîne** contenant le nom de l’attribut à récupérer.</span><span class="sxs-lookup"><span data-stu-id="32e0d-111">**String** containing the name of the attribute to be retrieved.</span></span> <span data-ttu-id="32e0d-112">Pour plus d’informations sur les attributs pris en charge par le lecteur Windows Media, consultez la page [référence des attributs](attribute-reference.md)du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="32e0d-112">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32e0d-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="32e0d-113">Return value</span></span>

<span data-ttu-id="32e0d-114">Cette méthode retourne une **chaîne**.</span><span class="sxs-lookup"><span data-stu-id="32e0d-114">This method returns a **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="32e0d-115">Notes</span><span class="sxs-lookup"><span data-stu-id="32e0d-115">Remarks</span></span>

<span data-ttu-id="32e0d-116">Pour utiliser cette méthode, l’accès en lecture à la bibliothèque est requis.</span><span class="sxs-lookup"><span data-stu-id="32e0d-116">To use this method, read access to the library is required.</span></span> <span data-ttu-id="32e0d-117">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="32e0d-117">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="32e0d-118">Exemples</span><span class="sxs-lookup"><span data-stu-id="32e0d-118">Examples</span></span>

<span data-ttu-id="32e0d-119">Consultez la propriété [attributeCount](playlist-attributecount.md) pour obtenir un exemple de code qui utilise cette propriété.</span><span class="sxs-lookup"><span data-stu-id="32e0d-119">See the [attributeCount](playlist-attributecount.md) property for example code that uses this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="32e0d-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="32e0d-120">Requirements</span></span>



| <span data-ttu-id="32e0d-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="32e0d-121">Requirement</span></span> | <span data-ttu-id="32e0d-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="32e0d-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="32e0d-123">Version</span><span class="sxs-lookup"><span data-stu-id="32e0d-123">Version</span></span><br/> | <span data-ttu-id="32e0d-124">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="32e0d-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="32e0d-125">DLL</span><span class="sxs-lookup"><span data-stu-id="32e0d-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="32e0d-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="32e0d-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32e0d-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="32e0d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32e0d-128">**Objet playlist**</span><span class="sxs-lookup"><span data-stu-id="32e0d-128">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="32e0d-129">**Playlist. setItemInfo**</span><span class="sxs-lookup"><span data-stu-id="32e0d-129">**Playlist.setItemInfo**</span></span>](playlist-setiteminfo.md)
</dt> <dt>

[<span data-ttu-id="32e0d-130">**Paramètres. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="32e0d-130">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="32e0d-131">**Paramètres. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="32e0d-131">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





