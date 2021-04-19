---
title: Méthode ClosedCaption. getSAMIStyleName
description: La méthode getSAMIStyleName récupère le nom d’un style pris en charge par le fichier SAMI actuel.
ms.assetid: c2ffedf8-4622-44fe-9d92-b52ed3bf3b9a
keywords:
- méthode getSAMIStyleName lecteur Windows Media
- méthode getSAMIStyleName lecteur Windows Media, classe ClosedCaption
- Classe ClosedCaption lecteur Windows Media, méthode getSAMIStyleName
topic_type:
- apiref
api_name:
- ClosedCaption.getSAMIStyleName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96480e28e0341b822aaf6726e63a6038681a577f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533014"
---
# <a name="closedcaptiongetsamistylename-method"></a><span data-ttu-id="1c177-106">Méthode ClosedCaption. getSAMIStyleName</span><span class="sxs-lookup"><span data-stu-id="1c177-106">ClosedCaption.getSAMIStyleName method</span></span>

<span data-ttu-id="1c177-107">La méthode **getSAMIStyleName** récupère le nom d’un style pris en charge par le fichier sami actuel.</span><span class="sxs-lookup"><span data-stu-id="1c177-107">The **getSAMIStyleName** method retrieves the name of a style supported by the current SAMI file.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c177-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1c177-108">Syntax</span></span>


```JScript
strRetVal = ClosedCaption.getSAMIStyleName(
  index
)
```



## <a name="parameters"></a><span data-ttu-id="1c177-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1c177-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c177-110">*index* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1c177-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c177-111">**Number** (**long**) spécifiant l’index du nom de style à récupérer.</span><span class="sxs-lookup"><span data-stu-id="1c177-111">**Number** (**long**) specifying the index of the style name to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c177-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1c177-112">Return value</span></span>

<span data-ttu-id="1c177-113">Cette méthode retourne une **chaîne** contenant le nom du style tel que spécifié dans le fichier sami.</span><span class="sxs-lookup"><span data-stu-id="1c177-113">This method returns a **String** containing the name of the style as specified in the SAMI file.</span></span>

## <a name="remarks"></a><span data-ttu-id="1c177-114">Notes</span><span class="sxs-lookup"><span data-stu-id="1c177-114">Remarks</span></span>

<span data-ttu-id="1c177-115">Les styles d’un fichier SAMI sont indexés dans l’ordre indiqué dans le fichier, à partir de zéro.</span><span class="sxs-lookup"><span data-stu-id="1c177-115">The styles in a SAMI file are indexed in the order shown in the file, starting with zero.</span></span>

<span data-ttu-id="1c177-116">Cette méthode ne peut pas être utilisée tant qu’un fichier multimédia numérique n’est pas ouvert (*lecteur*.**openState** est égal à 13).</span><span class="sxs-lookup"><span data-stu-id="1c177-116">This method cannot be used until a digital media file is open (*Player*.**openState** is equal to 13).</span></span>

<span data-ttu-id="1c177-117">**Lecteur Windows Media 10 Mobile :** Cette méthode n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="1c177-117">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c177-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1c177-118">Requirements</span></span>



| <span data-ttu-id="1c177-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1c177-119">Requirement</span></span> | <span data-ttu-id="1c177-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="1c177-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1c177-121">Version</span><span class="sxs-lookup"><span data-stu-id="1c177-121">Version</span></span><br/> | <span data-ttu-id="1c177-122">Lecteur Windows Media série 9 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="1c177-122">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="1c177-123">DLL</span><span class="sxs-lookup"><span data-stu-id="1c177-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="1c177-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1c177-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c177-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1c177-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c177-126">**Ajout de sous-titres à des médias numériques**</span><span class="sxs-lookup"><span data-stu-id="1c177-126">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="1c177-127">**Objet ClosedCaption**</span><span class="sxs-lookup"><span data-stu-id="1c177-127">**ClosedCaption Object**</span></span>](closedcaption-object.md)
</dt> <dt>

[<span data-ttu-id="1c177-128">**ClosedCaption.SAMIStyle**</span><span class="sxs-lookup"><span data-stu-id="1c177-128">**ClosedCaption.SAMIStyle**</span></span>](closedcaption-samistyle.md)
</dt> </dl>

 

 





