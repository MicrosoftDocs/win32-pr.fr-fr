---
title: ClosedCaption.SAMIStyle
description: La propriété SAMIStyle spécifie ou récupère le style de sous-titrage.
ms.assetid: 5535fb31-f1c0-49c4-b758-df74964b1e67
keywords:
- Lecteur Windows Media ClosedCaption. SAMIStyle
topic_type:
- apiref
api_name:
- ClosedCaption.SAMIStyle
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ebe81c2c2c4f4504d6167abe538c52ab769550a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532216"
---
# <a name="closedcaptionsamistyle"></a><span data-ttu-id="4add6-104">ClosedCaption.SAMIStyle</span><span class="sxs-lookup"><span data-stu-id="4add6-104">ClosedCaption.SAMIStyle</span></span>

<span data-ttu-id="4add6-105">La propriété **SAMIStyle** spécifie ou récupère le style de sous-titrage.</span><span class="sxs-lookup"><span data-stu-id="4add6-105">The **SAMIStyle** property specifies or retrieves the closed captioning style.</span></span>

``` syntax
player.closedCaption.SAMIStyle
```

## <a name="possible-values"></a><span data-ttu-id="4add6-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="4add6-106">Possible Values</span></span>

<span data-ttu-id="4add6-107">Cette propriété est une **chaîne** en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="4add6-107">This property is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="4add6-108">Notes</span><span class="sxs-lookup"><span data-stu-id="4add6-108">Remarks</span></span>

<span data-ttu-id="4add6-109">Un fichier SAMI peut contenir plusieurs définitions de style de format.</span><span class="sxs-lookup"><span data-stu-id="4add6-109">A SAMI file can contain several format style definitions.</span></span> <span data-ttu-id="4add6-110">Les styles SAMI sont définis entre les balises <STYLE> et </STYLE> dans le fichier sami.</span><span class="sxs-lookup"><span data-stu-id="4add6-110">SAMI styles are defined between the <STYLE> and </STYLE> tags in the SAMI file.</span></span> <span data-ttu-id="4add6-111">Un style est défini avec une chaîne de texte précédée d’un \# caractère.</span><span class="sxs-lookup"><span data-stu-id="4add6-111">A style is defined with a text string preceded by a \# character.</span></span> <span data-ttu-id="4add6-112">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="4add6-112">For example:</span></span>


```
#Emphasis1 {Name: Big Bold Italic; font-size: 14pt; text-align: center;
            color: blue; font-family: sans-serif; font-weight: bold;
            font-style: italic;}

```



<span data-ttu-id="4add6-113">Cela spécifie un style qui produit une police particulière.</span><span class="sxs-lookup"><span data-stu-id="4add6-113">This specifies a style that produces a particular font.</span></span>

<span data-ttu-id="4add6-114">Si aucun style SAMI n’est spécifié, le premier style défini dans le fichier SAMI est utilisé par défaut.</span><span class="sxs-lookup"><span data-stu-id="4add6-114">If no SAMI style is specified, the first style defined in the SAMI file is used by default.</span></span>

<span data-ttu-id="4add6-115">**Lecteur Windows Media 10 Mobile :** Cette propriété est en lecture seule et retourne toujours une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="4add6-115">**Windows Media Player 10 Mobile:** This property is read only, and always returns an empty string.</span></span>

## <a name="examples"></a><span data-ttu-id="4add6-116">Exemples</span><span class="sxs-lookup"><span data-stu-id="4add6-116">Examples</span></span>

<span data-ttu-id="4add6-117">L’exemple JScript suivant crée un élément SELECT HTML qui utilise *closedCaption*. **SAMIStyle** pour modifier l’apparence du texte de la légende fermée.</span><span class="sxs-lookup"><span data-stu-id="4add6-117">The following JScript example creates an HTML SELECT element that uses *closedCaption*.**SAMIStyle** to change the appearance of the closed caption text.</span></span> <span data-ttu-id="4add6-118">L’objet **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="4add6-118">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create the SELECT element. -->
<SELECT ID = CCMode  NAME = "CCMode"  LANGUAGE = "JScript"

       /* Change the text style when the SELECT element changes. */
        onChange = "Player.closedCaption.SAMIStyle = CCMode.value;
        ">

       /* Fill the SELECT list with options, set the default to Strong. */
        <OPTION VALUE = "Normal">Normal
        <OPTION VALUE = "Small">Small 
        <OPTION VALUE = "Big Bold Italic" SELECTED>Strong
</SELECT>

```



## <a name="requirements"></a><span data-ttu-id="4add6-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4add6-119">Requirements</span></span>



| <span data-ttu-id="4add6-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4add6-120">Requirement</span></span> | <span data-ttu-id="4add6-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="4add6-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4add6-122">Version</span><span class="sxs-lookup"><span data-stu-id="4add6-122">Version</span></span><br/> | <span data-ttu-id="4add6-123">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="4add6-123">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="4add6-124">DLL</span><span class="sxs-lookup"><span data-stu-id="4add6-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="4add6-125"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4add6-125"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4add6-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4add6-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4add6-127">**Ajout de sous-titres à des médias numériques**</span><span class="sxs-lookup"><span data-stu-id="4add6-127">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="4add6-128">**Objet ClosedCaption**</span><span class="sxs-lookup"><span data-stu-id="4add6-128">**ClosedCaption Object**</span></span>](closedcaption-object.md)
</dt> </dl>

 

 





