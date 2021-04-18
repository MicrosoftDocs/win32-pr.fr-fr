---
title: Méthode playlist. setItemInfo
description: La méthode setItemInfo spécifie la valeur d’un attribut playlist.
ms.assetid: ffecb43f-343d-4a4f-9356-0e3cfa85ce77
keywords:
- méthode setItemInfo lecteur Windows Media
- méthode setItemInfo lecteur Windows Media, classe de sélection
- Classe de sélection lecteur Windows Media, méthode setItemInfo
topic_type:
- apiref
api_name:
- Playlist.setItemInfo
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ff42e56e549100044db0881bb38ade5f2f1711a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533328"
---
# <a name="playlistsetiteminfo-method"></a><span data-ttu-id="8be36-106">Méthode playlist. setItemInfo</span><span class="sxs-lookup"><span data-stu-id="8be36-106">Playlist.setItemInfo method</span></span>

<span data-ttu-id="8be36-107">La méthode **setItemInfo** spécifie la valeur d’un attribut playlist.</span><span class="sxs-lookup"><span data-stu-id="8be36-107">The **setItemInfo** method specifies the value of a playlist attribute.</span></span>

## <a name="syntax"></a><span data-ttu-id="8be36-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8be36-108">Syntax</span></span>


```JScript
Playlist.setItemInfo(
  name,
  value
)
```



## <a name="parameters"></a><span data-ttu-id="8be36-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8be36-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8be36-110">*nom* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8be36-110">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8be36-111">**Chaîne** contenant le nom de l’attribut à définir.</span><span class="sxs-lookup"><span data-stu-id="8be36-111">**String** containing the name of the attribute to be set.</span></span> <span data-ttu-id="8be36-112">Pour plus d’informations sur les attributs pris en charge par le lecteur Windows Media, consultez la page [référence des attributs](attribute-reference.md)du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="8be36-112">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

</dd> <dt>

<span data-ttu-id="8be36-113">*valeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8be36-113">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8be36-114">**Chaîne** contenant la nouvelle valeur de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="8be36-114">**String** containing the new value for the attribute.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8be36-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8be36-115">Return value</span></span>

<span data-ttu-id="8be36-116">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="8be36-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8be36-117">Notes</span><span class="sxs-lookup"><span data-stu-id="8be36-117">Remarks</span></span>

<span data-ttu-id="8be36-118">Une utilisation spéciale de la méthode **setItemInfo** consiste à trier les éléments de la sélection à l’aide de l’attribut SortAttribute.</span><span class="sxs-lookup"><span data-stu-id="8be36-118">A special use of the **setItemInfo** method is to sort the items in the playlist by using the SortAttribute attribute.</span></span> <span data-ttu-id="8be36-119">L’exemple JScript suivant trie une sélection selon les valeurs de l’attribut UserLastPlayedTime.</span><span class="sxs-lookup"><span data-stu-id="8be36-119">The following JScript example sorts a playlist by the values of the UserLastPlayedTime attribute.</span></span> <span data-ttu-id="8be36-120">La sélection de variable est une référence à un objet **playlist** .</span><span class="sxs-lookup"><span data-stu-id="8be36-120">The variable playlist is a reference to a **Playlist** object.</span></span>


```JScript
playlist.setItemInfo("SortAttribute", "UserLastPlayedTime")
```



<span data-ttu-id="8be36-121">Pour utiliser cette méthode, l’accès complet à la bibliothèque est requis.</span><span class="sxs-lookup"><span data-stu-id="8be36-121">To use this method, full access to the library is required.</span></span> <span data-ttu-id="8be36-122">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="8be36-122">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="8be36-123">**Lecteur Windows Media 10 Mobile :** Cette méthode n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="8be36-123">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="8be36-124">Exemples</span><span class="sxs-lookup"><span data-stu-id="8be36-124">Examples</span></span>

<span data-ttu-id="8be36-125">Consultez la propriété [attributeCount](playlist-attributecount.md) pour obtenir un exemple de code qui utilise cette propriété.</span><span class="sxs-lookup"><span data-stu-id="8be36-125">See the [attributeCount](playlist-attributecount.md) property for example code that uses this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="8be36-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8be36-126">Requirements</span></span>



| <span data-ttu-id="8be36-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8be36-127">Requirement</span></span> | <span data-ttu-id="8be36-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="8be36-128">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8be36-129">Version</span><span class="sxs-lookup"><span data-stu-id="8be36-129">Version</span></span><br/> | <span data-ttu-id="8be36-130">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="8be36-130">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="8be36-131">DLL</span><span class="sxs-lookup"><span data-stu-id="8be36-131">DLL</span></span><br/>     | <dl> <span data-ttu-id="8be36-132"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8be36-132"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8be36-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8be36-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8be36-134">**Objet playlist**</span><span class="sxs-lookup"><span data-stu-id="8be36-134">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="8be36-135">**Playlist. getItemInfo**</span><span class="sxs-lookup"><span data-stu-id="8be36-135">**Playlist.getItemInfo**</span></span>](playlist-getiteminfo.md)
</dt> <dt>

[<span data-ttu-id="8be36-136">**Paramètres. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="8be36-136">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="8be36-137">**Paramètres. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="8be36-137">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





