---
title: THÈME. openDialog
description: La méthode openDialog ouvre une boîte de dialogue de fichier.
ms.assetid: d7f4549c-a5c3-4902-b13b-51f3d4444ea9
keywords:
- THEMe. openDialog Windows Media Player
topic_type:
- apiref
api_name:
- THEME.openDialog
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 79b9478b6b970b1d8d18b6f40975479e4755fa6d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543375"
---
# <a name="themeopendialog"></a><span data-ttu-id="178f6-104">THÈME. openDialog</span><span class="sxs-lookup"><span data-stu-id="178f6-104">THEME.openDialog</span></span>

<span data-ttu-id="178f6-105">La méthode **openDialog** ouvre une boîte de dialogue de fichier.</span><span class="sxs-lookup"><span data-stu-id="178f6-105">The **openDialog** method opens a file dialog box.</span></span>

``` syntax
        theme.openDialog(dialogType, parameters)
```

## <a name="parameters"></a><span data-ttu-id="178f6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="178f6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="178f6-107"><span id="dialogType"></span><span id="dialogtype"></span><span id="DIALOGTYPE"></span>*dialogType*</span><span class="sxs-lookup"><span data-stu-id="178f6-107"><span id="dialogType"></span><span id="dialogtype"></span><span id="DIALOGTYPE"></span>*dialogType*</span></span>
</dt> <dd>

<span data-ttu-id="178f6-108">**Chaîne** qui spécifie le type de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="178f6-108">A **String** that specifies the type of dialog box.</span></span> <span data-ttu-id="178f6-109">Doit être défini sur « fichier \_ ouvert ».</span><span class="sxs-lookup"><span data-stu-id="178f6-109">Must be set to "FILE\_OPEN".</span></span>

</dd> <dt>

<span data-ttu-id="178f6-110"><span id="parameters"></span><span id="PARAMETERS"></span>*paramètres*</span><span class="sxs-lookup"><span data-stu-id="178f6-110"><span id="parameters"></span><span id="PARAMETERS"></span>*parameters*</span></span>
</dt> <dd>

<span data-ttu-id="178f6-111">**Chaîne** qui peut être utilisée pour obtenir des informations supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="178f6-111">A **String** that can be used for additional information.</span></span> <span data-ttu-id="178f6-112">Doit être défini sur « FILES \_ ALLMEDIA ».</span><span class="sxs-lookup"><span data-stu-id="178f6-112">Must be set to "FILES\_ALLMEDIA".</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="178f6-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="178f6-113">Return Value</span></span>

<span data-ttu-id="178f6-114">Cette méthode retourne une **chaîne** contenant l’URL du fichier sélectionné ou «» (chaîne vide) si l’utilisateur clique sur Annuler.</span><span class="sxs-lookup"><span data-stu-id="178f6-114">This method returns a **String** containing the URL of the selected file or "" (empty string) if the user clicks cancel.</span></span>

## <a name="remarks"></a><span data-ttu-id="178f6-115">Notes</span><span class="sxs-lookup"><span data-stu-id="178f6-115">Remarks</span></span>

<span data-ttu-id="178f6-116">Cette méthode peut être utilisée pour les fichiers sur les disques durs locaux ou sur les lecteurs réseau.</span><span class="sxs-lookup"><span data-stu-id="178f6-116">This method can be used for files on the local hard drives or on network drives.</span></span>

## <a name="examples"></a><span data-ttu-id="178f6-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="178f6-117">Examples</span></span>


```JScript
<THEME>
  <VIEW id="View1" 
    backgroundImage="greenstone.bmp" 
    width=500 height=300 author="Microsoft Corp.">
    <BUTTON 
      id="Open" 
      image="Open.png" 
      onclick="jscript:
        player.URL = theme.openDialog('FILE_OPEN','FILES_ALLMEDIA')">
    </BUTTON>
  </VIEW>
</THEME>
```



## <a name="requirements"></a><span data-ttu-id="178f6-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="178f6-118">Requirements</span></span>



| <span data-ttu-id="178f6-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="178f6-119">Requirement</span></span> | <span data-ttu-id="178f6-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="178f6-120">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="178f6-121">Version</span><span class="sxs-lookup"><span data-stu-id="178f6-121">Version</span></span><br/> | <span data-ttu-id="178f6-122">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="178f6-122">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="178f6-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="178f6-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="178f6-124">**Élément THEMe**</span><span class="sxs-lookup"><span data-stu-id="178f6-124">**THEME Element**</span></span>](theme-element.md)
</dt> </dl>

 

 





