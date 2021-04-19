---
title: ClosedCaption.SAMILang
description: La propriété SAMILang spécifie ou récupère la langue affichée pour le sous-titrage.
ms.assetid: 990fb180-cb37-4022-b236-03f5acfd3ad3
keywords:
- Lecteur Windows Media ClosedCaption. SAMILang
topic_type:
- apiref
api_name:
- ClosedCaption.SAMILang
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae99b9a164e29b4adeb2fd7b23a1b79945dcb26e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537970"
---
# <a name="closedcaptionsamilang"></a><span data-ttu-id="f23e0-104">ClosedCaption.SAMILang</span><span class="sxs-lookup"><span data-stu-id="f23e0-104">ClosedCaption.SAMILang</span></span>

<span data-ttu-id="f23e0-105">La propriété **SAMILang** spécifie ou récupère la langue affichée pour le sous-titrage.</span><span class="sxs-lookup"><span data-stu-id="f23e0-105">The **SAMILang** property specifies or retrieves the language displayed for closed captioning.</span></span>

``` syntax
player.closedCaption.SAMILang
```

## <a name="possible-values"></a><span data-ttu-id="f23e0-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="f23e0-106">Possible Values</span></span>

<span data-ttu-id="f23e0-107">Cette propriété est une **chaîne** en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="f23e0-107">This property is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="f23e0-108">Notes</span><span class="sxs-lookup"><span data-stu-id="f23e0-108">Remarks</span></span>

<span data-ttu-id="f23e0-109">Un fichier SAMI peut contenir du texte pour une ou plusieurs langues.</span><span class="sxs-lookup"><span data-stu-id="f23e0-109">A SAMI file can contain text for one or many languages.</span></span> <span data-ttu-id="f23e0-110">Les langues disponibles pour le sous-titrage sont définies entre les balises <STYLE> et </STYLE> dans le fichier sami.</span><span class="sxs-lookup"><span data-stu-id="f23e0-110">The languages available for closed captioning are defined between the <STYLE> and </STYLE> tags in the SAMI file.</span></span> <span data-ttu-id="f23e0-111">Un identificateur de langue est spécifié avec une chaîne alphanumérique unique précédée d’un point (.).</span><span class="sxs-lookup"><span data-stu-id="f23e0-111">A language identifier is specified with a unique alphanumeric string that is preceded by a period (.).</span></span> <span data-ttu-id="f23e0-112">Le nom spécifié pour une langue peut être n’importe quelle chaîne.</span><span class="sxs-lookup"><span data-stu-id="f23e0-112">The name specified for a language can be any string.</span></span> <span data-ttu-id="f23e0-113">Par exemple, les éléments suivants peuvent être utilisés pour définir l’anglais des États-Unis :</span><span class="sxs-lookup"><span data-stu-id="f23e0-113">For example, the following could be used to define US English:</span></span>


```
.ENUSCC {Name:'English Captions' lang: en-US; SAMIType:CC;}

```



<span data-ttu-id="f23e0-114">Si aucune langue SAMI n’est spécifiée, la première langue définie dans le fichier SAMI est utilisée par défaut.</span><span class="sxs-lookup"><span data-stu-id="f23e0-114">If no SAMI language is specified, the first language defined in the SAMI file is used by default.</span></span>

<span data-ttu-id="f23e0-115">Valeur que vous transmettez à l’aide de *ClosedCaption*. **SAMILang** doit correspondre à l’attribut **Name** dans le spécificateur de langage.</span><span class="sxs-lookup"><span data-stu-id="f23e0-115">The value you pass using *ClosedCaption*.**SAMILang** must match the **Name** attribute in the language specifier.</span></span>

<span data-ttu-id="f23e0-116">**Lecteur Windows Media 10 Mobile :** Cette propriété est en lecture seule et retourne toujours une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="f23e0-116">**Windows Media Player 10 Mobile:** This property is read only, and always returns an empty string.</span></span>

## <a name="examples"></a><span data-ttu-id="f23e0-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="f23e0-117">Examples</span></span>

<span data-ttu-id="f23e0-118">L’exemple JScript suivant utilise *ClosedCaption*. **SAMILang** dans un élément Select HTML pour spécifier la langue de la légende fermée.</span><span class="sxs-lookup"><span data-stu-id="f23e0-118">The following JScript example uses *ClosedCaption*.**SAMILang** in an HTML SELECT element to specify the closed caption language.</span></span> <span data-ttu-id="f23e0-119">L’objet **Player** a été créé avec ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="f23e0-119">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create the SELECT element. -->
<SELECT ID = CCLANG  NAME = "CCLANG"  LANGUAGE = "JScript"

     /* Set the closed caption language when the SELECT element changes. */
        onChange = "Player.closedCaption.SAMILang = CCLANG.value;
        ">

        /* Fill in the SELECT element options. */
           <OPTION VALUE = "'Spanish Captions'">Spanish
           <OPTION VALUE = "'Japanese Captions'">Japanese
           <OPTION VALUE = "'English Captions'">English
           <OPTION VALUE = "'French Captions'">French
           <OPTION VALUE = "'German Captions'" SELECTED>German
</SELECT>

```



## <a name="requirements"></a><span data-ttu-id="f23e0-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f23e0-120">Requirements</span></span>



| <span data-ttu-id="f23e0-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f23e0-121">Requirement</span></span> | <span data-ttu-id="f23e0-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="f23e0-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f23e0-123">Version</span><span class="sxs-lookup"><span data-stu-id="f23e0-123">Version</span></span><br/> | <span data-ttu-id="f23e0-124">Lecteur Windows Media version 7,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="f23e0-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="f23e0-125">DLL</span><span class="sxs-lookup"><span data-stu-id="f23e0-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="f23e0-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f23e0-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f23e0-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f23e0-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f23e0-128">**Ajout de sous-titres à des médias numériques**</span><span class="sxs-lookup"><span data-stu-id="f23e0-128">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="f23e0-129">**Objet ClosedCaption**</span><span class="sxs-lookup"><span data-stu-id="f23e0-129">**ClosedCaption Object**</span></span>](closedcaption-object.md)
</dt> </dl>

 

 





