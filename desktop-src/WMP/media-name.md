---
title: Media.name
description: La propriété Name spécifie ou récupère le nom de l’élément multimédia.
ms.assetid: 68aba78a-86fd-4411-9ac4-58f38d915e2c
keywords:
- Lecteur Windows Media Media.name
topic_type:
- apiref
api_name:
- Media.name
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9de8095d88c3ddec9049e0b43461adcf5553ec74
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542629"
---
# <a name="medianame"></a><span data-ttu-id="36930-104">Media.name</span><span class="sxs-lookup"><span data-stu-id="36930-104">Media.name</span></span>

<span data-ttu-id="36930-105">La propriété **Name** spécifie ou récupère le nom de l’élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="36930-105">The **name** property specifies or retrieves the name of the media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="36930-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="36930-106">Syntax</span></span>

<span data-ttu-id="36930-107">*lecteur*. *currentMedia*. **nom**</span><span class="sxs-lookup"><span data-stu-id="36930-107">*player*.*currentMedia*.**name**</span></span>

## <a name="possible-values"></a><span data-ttu-id="36930-108">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="36930-108">Possible Values</span></span>

<span data-ttu-id="36930-109">Cette propriété est une **chaîne** en lecture/écriture contenant le nom de l’élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="36930-109">This property is a read/write **String** containing the name of the media item.</span></span>

## <a name="remarks"></a><span data-ttu-id="36930-110">Notes</span><span class="sxs-lookup"><span data-stu-id="36930-110">Remarks</span></span>

<span data-ttu-id="36930-111">Pour récupérer la valeur de cette propriété, l’accès en lecture à la bibliothèque est requis.</span><span class="sxs-lookup"><span data-stu-id="36930-111">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="36930-112">Pour spécifier la valeur de cette propriété, l’accès complet à la bibliothèque est requis.</span><span class="sxs-lookup"><span data-stu-id="36930-112">To specify the value of this property, full access to the library is required.</span></span> <span data-ttu-id="36930-113">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="36930-113">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="36930-114">Avant d’utiliser cette méthode pour spécifier le nom d’un élément multimédia, utilisez **isReadOnlyItem** pour déterminer si le nom peut être défini.</span><span class="sxs-lookup"><span data-stu-id="36930-114">Before using this method to specify the name of a media item, use **isReadOnlyItem** to determine whether the name can be set.</span></span>

<span data-ttu-id="36930-115">**Lecteur Windows Media 10 Mobile :** Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="36930-115">**Windows Media Player 10 Mobile:** This property is read-only.</span></span>

## <a name="examples"></a><span data-ttu-id="36930-116">Exemples</span><span class="sxs-lookup"><span data-stu-id="36930-116">Examples</span></span>

<span data-ttu-id="36930-117">L’exemple JScript suivant utilise un *média*. **nom** pour modifier le nom de l’élément multimédia actuel.</span><span class="sxs-lookup"><span data-stu-id="36930-117">The following JScript example uses *Media*.**name** to change the name of the current media item.</span></span> <span data-ttu-id="36930-118">Un élément d’entrée de texte HTML nommé NameText permet à l’utilisateur d’entrer une chaîne de texte pour le nouveau nom.</span><span class="sxs-lookup"><span data-stu-id="36930-118">An HTML TEXT input element named NameText allows the user to enter a text string for the new name.</span></span> <span data-ttu-id="36930-119">L’objet **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="36930-119">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!<entity type="mdash"/>-Create an HTML BUTTON element to execute the name change. -->
<INPUT type = "BUTTON"  id = "NewName"  name = "NewName"  value = "Change Name" 
    onClick = "

        /* Store the current media item. */
        var cm = Player.currentMedia;

        /* Change the name. */
        cm.name = NameText.value;
">

```



## <a name="requirements"></a><span data-ttu-id="36930-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="36930-120">Requirements</span></span>



| <span data-ttu-id="36930-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="36930-121">Requirement</span></span> | <span data-ttu-id="36930-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="36930-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="36930-123">Version</span><span class="sxs-lookup"><span data-stu-id="36930-123">Version</span></span><br/> | <span data-ttu-id="36930-124">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="36930-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="36930-125">DLL</span><span class="sxs-lookup"><span data-stu-id="36930-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="36930-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="36930-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36930-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="36930-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36930-128">**Objet Media**</span><span class="sxs-lookup"><span data-stu-id="36930-128">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="36930-129">**Paramètres. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="36930-129">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="36930-130">**Paramètres. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="36930-130">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





