---
title: External. showPopup, méthode
description: Remarque Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. | External. showPopup, méthode
ms.assetid: 17958543-dbed-45a5-9b02-4800a07cb820
keywords:
- méthode showPopup lecteur Windows Media
- méthode showPopup lecteur Windows Media, classe externe
- Classe externe lecteur Windows Media, méthode showPopup
topic_type:
- apiref
api_name:
- External.showPopup
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acaecb559e7df60067e89ec754ec9432233500f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520841"
---
# <a name="externalshowpopup-method"></a><span data-ttu-id="d948f-107">External. showPopup, méthode</span><span class="sxs-lookup"><span data-stu-id="d948f-107">External.showPopup method</span></span>

> [!Note]  
> <span data-ttu-id="d948f-108">Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne.</span><span class="sxs-lookup"><span data-stu-id="d948f-108">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="d948f-109">L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="d948f-109">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="d948f-110">La méthode **ShowPopup** demande au lecteur Windows Media d’afficher une page contextuelle. autrement dit, une page Web qui s’affiche dans une fenêtre distincte.</span><span class="sxs-lookup"><span data-stu-id="d948f-110">The **showPopup** method instructs Windows Media Player to display a pop-up webpage; that is, a webpage that appears in a separate window.</span></span>

## <a name="syntax"></a><span data-ttu-id="d948f-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d948f-111">Syntax</span></span>


```JScript
External.showPopup(
  PopupIndex,
  Parameters
)
```



## <a name="parameters"></a><span data-ttu-id="d948f-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d948f-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d948f-113">*PopupIndex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d948f-113">*PopupIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d948f-114">**Nombre** (**long**) qui spécifie l’index de la page Web contextuelle.</span><span class="sxs-lookup"><span data-stu-id="d948f-114">**Number** (**long**) that specifies the index of the pop-up webpage.</span></span>

</dd> <dt>

<span data-ttu-id="d948f-115">*Paramètres* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d948f-115">*Parameters* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d948f-116">**Chaîne** que le lecteur Windows Media ajoute à l’URL de la page Web.</span><span class="sxs-lookup"><span data-stu-id="d948f-116">**String** that Windows Media Player appends to the URL of the webpage.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d948f-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d948f-117">Return value</span></span>

<span data-ttu-id="d948f-118">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="d948f-118">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d948f-119">Notes</span><span class="sxs-lookup"><span data-stu-id="d948f-119">Remarks</span></span>

<span data-ttu-id="d948f-120">L’index contextuel n’est pas interprété par le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="d948f-120">The pop-up index is not interpreted by Windows Media Player.</span></span> <span data-ttu-id="d948f-121">Les index qui identifient les pages Web contextuelles sont créés par le magasin en ligne et ont une signification uniquement pour le magasin en ligne.</span><span class="sxs-lookup"><span data-stu-id="d948f-121">Indexes that identify pop-up webpages are created by the online store, and have meaning only to the online store.</span></span>

<span data-ttu-id="d948f-122">Les étapes suivantes montrent comment le lecteur Windows Media utilise les paramètres de la méthode **ShowPopup** pour créer une URL pour la fenêtre contextuelle.</span><span class="sxs-lookup"><span data-stu-id="d948f-122">The following steps show how Windows Media Player uses the parameters of the **showPopup** method to create a URL for the popup window.</span></span>

1.  <span data-ttu-id="d948f-123">Un script sur une page de découverte appelle **ShowPopup**, en passant un entier dans *PopupIndex* et une chaîne dans les *paramètres*.</span><span class="sxs-lookup"><span data-stu-id="d948f-123">Script on a discovery page calls **showPopup**, passing an integer in *PopupIndex* and a string in *Parameters*.</span></span>

2.  <span data-ttu-id="d948f-124">Le lecteur Windows Media transmet l’index à [IWMPContentPartner :: GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo) pour récupérer l’URL de la page Web à afficher.</span><span class="sxs-lookup"><span data-stu-id="d948f-124">Windows Media Player passes the index to [IWMPContentPartner::GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo) to retrieve the URL of the webpage to be displayed.</span></span>

3.  <span data-ttu-id="d948f-125">Le lecteur Windows Media ajoute des *paramètres* à l’URL sous la forme d’une chaîne de requête.</span><span class="sxs-lookup"><span data-stu-id="d948f-125">Windows Media Player appends *Parameters* to the URL as a query string.</span></span> <span data-ttu-id="d948f-126">Par exemple, si **GetItemInfo** retourne « https://www.Proseware.com/Pages/Popup1.htm » et que les *paramètres* sont égaux à « DlgX = 800&DlgY = 400&Greeting = Hi », le lecteur Windows Media crée l’URL suivante :</span><span class="sxs-lookup"><span data-stu-id="d948f-126">For example, if **GetItemInfo** returns "https://www.Proseware.com/Pages/Popup1.htm" and *Parameters* is equal to "DlgX=800&DlgY=400&Greeting=Hi", Windows Media Player creates the following URL:</span></span>

    https://www.Proseware.com/Pages/Popup1.htm?DlgX=800&DlgY=400&Greeting=Hi

<span data-ttu-id="d948f-127">Vous pouvez utiliser des *paramètres* pour spécifier la taille de la fenêtre indépendante.</span><span class="sxs-lookup"><span data-stu-id="d948f-127">You can use *Parameters* to specify the size of the pop-up window.</span></span> <span data-ttu-id="d948f-128">Par exemple, si vous définissez les *paramètres* sur « DlgX = 800&DlgY = 400 », la fenêtre contextuelle aura une taille de 800 pixels par 400 pixels.</span><span class="sxs-lookup"><span data-stu-id="d948f-128">For example, if you set *Parameters* to "DlgX=800&DlgY=400", the pop-up window will have a size of 800 pixels by 400 pixels.</span></span>

## <a name="requirements"></a><span data-ttu-id="d948f-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d948f-129">Requirements</span></span>



| <span data-ttu-id="d948f-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d948f-130">Requirement</span></span> | <span data-ttu-id="d948f-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="d948f-131">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d948f-132">Version</span><span class="sxs-lookup"><span data-stu-id="d948f-132">Version</span></span><br/> | <span data-ttu-id="d948f-133">Lecteur Windows Media 11</span><span class="sxs-lookup"><span data-stu-id="d948f-133">Windows Media Player 11</span></span><br/>                                                 |
| <span data-ttu-id="d948f-134">DLL</span><span class="sxs-lookup"><span data-stu-id="d948f-134">DLL</span></span><br/>     | <dl> <span data-ttu-id="d948f-135"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d948f-135"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d948f-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d948f-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d948f-137">**Objet externe pour les magasins de type 1 en ligne**</span><span class="sxs-lookup"><span data-stu-id="d948f-137">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





