---
title: Settings. muet
description: La propriété muet spécifie et récupère une valeur indiquant si l’audio est muet.
ms.assetid: d6d4b46d-5631-4af7-bd99-21674f067121
keywords:
- Settings. muet Windows Media Player
topic_type:
- apiref
api_name:
- Settings.mute
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7061439e9e091b2ad1cf6be49873d7e3895132b0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106538102"
---
# <a name="settingsmute"></a><span data-ttu-id="a7573-104">Settings. muet</span><span class="sxs-lookup"><span data-stu-id="a7573-104">Settings.mute</span></span>

<span data-ttu-id="a7573-105">La propriété **muet** spécifie et récupère une valeur indiquant si l’audio est muet.</span><span class="sxs-lookup"><span data-stu-id="a7573-105">The **mute** property specifies and retrieves a value indicating whether audio is muted.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7573-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a7573-106">Syntax</span></span>

<span data-ttu-id="a7573-107">Player. Settings. muet</span><span class="sxs-lookup"><span data-stu-id="a7573-107">player.settings.mute</span></span>

## <a name="possible-values"></a><span data-ttu-id="a7573-108">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="a7573-108">Possible Values</span></span>

<span data-ttu-id="a7573-109">Cette propriété est une **valeur booléenne** en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="a7573-109">This property is a read/write **Boolean**.</span></span>



| <span data-ttu-id="a7573-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="a7573-110">Value</span></span> | <span data-ttu-id="a7573-111">Description</span><span class="sxs-lookup"><span data-stu-id="a7573-111">Description</span></span>                  |
|-------|------------------------------|
| <span data-ttu-id="a7573-112">true</span><span class="sxs-lookup"><span data-stu-id="a7573-112">true</span></span>  | <span data-ttu-id="a7573-113">L’audio est muet.</span><span class="sxs-lookup"><span data-stu-id="a7573-113">Audio is muted.</span></span>              |
| <span data-ttu-id="a7573-114">false</span><span class="sxs-lookup"><span data-stu-id="a7573-114">false</span></span> | <span data-ttu-id="a7573-115">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="a7573-115">Default.</span></span> <span data-ttu-id="a7573-116">L’audio n’est pas muet.</span><span class="sxs-lookup"><span data-stu-id="a7573-116">Audio is not muted.</span></span> |



 

## <a name="examples"></a><span data-ttu-id="a7573-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="a7573-117">Examples</span></span>

<span data-ttu-id="a7573-118">L’exemple suivant crée un élément de case à cocher HTML qui permet à l’utilisateur d’activer ou de désactiver le son.</span><span class="sxs-lookup"><span data-stu-id="a7573-118">The following example creates an HTML CHECKBOX element that allows the user to mute and un-mute audio.</span></span> <span data-ttu-id="a7573-119">L’objet **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="a7573-119">The **Player** object was created with ID = "Player".</span></span>


```
<!-- Create an HTML CHECKBOX control. -->
<INPUT  TYPE = "CHECKBOX"  ID = MUTE  
             onClick = "
                        /* Use the CHECKBOX state to set 
                           the mute property. */
                        Player.settings.mute = MUTE.checked;
">
```



## <a name="requirements"></a><span data-ttu-id="a7573-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a7573-120">Requirements</span></span>



| <span data-ttu-id="a7573-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a7573-121">Requirement</span></span> | <span data-ttu-id="a7573-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="a7573-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a7573-123">Version</span><span class="sxs-lookup"><span data-stu-id="a7573-123">Version</span></span><br/> | <span data-ttu-id="a7573-124">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="a7573-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="a7573-125">DLL</span><span class="sxs-lookup"><span data-stu-id="a7573-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="a7573-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a7573-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7573-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a7573-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7573-128">**Settings (objet)**</span><span class="sxs-lookup"><span data-stu-id="a7573-128">**Settings Object**</span></span>](settings-object.md)
</dt> </dl>

 

 





