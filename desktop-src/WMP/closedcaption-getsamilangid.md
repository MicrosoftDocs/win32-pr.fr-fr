---
title: Méthode ClosedCaption. getSAMILangID
description: La méthode getSAMILangID récupère l’identificateur de paramètres régionaux (LCID) d’une langue prise en charge par le fichier SAMI actuel.
ms.assetid: 35f8379a-a2f5-4b22-b1ad-3c5cc5bc5e3d
keywords:
- méthode getSAMILangID lecteur Windows Media
- méthode getSAMILangID lecteur Windows Media, classe ClosedCaption
- Classe ClosedCaption lecteur Windows Media, méthode getSAMILangID
topic_type:
- apiref
api_name:
- ClosedCaption.getSAMILangID
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cd543c9cb9d884022d78a875a2f8de078c479b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533502"
---
# <a name="closedcaptiongetsamilangid-method"></a><span data-ttu-id="f7b41-106">Méthode ClosedCaption. getSAMILangID</span><span class="sxs-lookup"><span data-stu-id="f7b41-106">ClosedCaption.getSAMILangID method</span></span>

<span data-ttu-id="f7b41-107">La méthode **getSAMILangID** récupère l’identificateur de paramètres régionaux (LCID) d’une langue prise en charge par le fichier sami actuel.</span><span class="sxs-lookup"><span data-stu-id="f7b41-107">The **getSAMILangID** method retrieves the locale identifier (LCID) of a language supported by the current SAMI file.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7b41-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f7b41-108">Syntax</span></span>


```JScript
retVal = ClosedCaption.getSAMILangID(
  index
)
```



## <a name="parameters"></a><span data-ttu-id="f7b41-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f7b41-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7b41-110">*index* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f7b41-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7b41-111">**Nombre** (**long**) spécifiant l’index du LCID à récupérer.</span><span class="sxs-lookup"><span data-stu-id="f7b41-111">**Number** (**long**) specifying the index of the LCID to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7b41-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f7b41-112">Return value</span></span>

<span data-ttu-id="f7b41-113">Cette méthode retourne un **nombre** (**long**) contenant le LCID de la langue avec l’index spécifié.</span><span class="sxs-lookup"><span data-stu-id="f7b41-113">This method returns a **Number** (**long**) containing the LCID of the language with the specified index.</span></span>

## <a name="remarks"></a><span data-ttu-id="f7b41-114">Notes</span><span class="sxs-lookup"><span data-stu-id="f7b41-114">Remarks</span></span>

<span data-ttu-id="f7b41-115">Les langues d’un fichier SAMI sont indexées dans l’ordre indiqué dans le fichier, à partir de zéro.</span><span class="sxs-lookup"><span data-stu-id="f7b41-115">The languages in a SAMI file are indexed in the order shown in the file, starting with zero.</span></span>

<span data-ttu-id="f7b41-116">Cette méthode ne peut pas être utilisée tant qu’un fichier multimédia numérique n’est pas ouvert (*lecteur*.**openState** est égal à 13).</span><span class="sxs-lookup"><span data-stu-id="f7b41-116">This method cannot be used until a digital media file is open (*Player*.**openState** is equal to 13).</span></span>

<span data-ttu-id="f7b41-117">**Lecteur Windows Media 10 Mobile :** Cette méthode n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="f7b41-117">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7b41-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f7b41-118">Requirements</span></span>



| <span data-ttu-id="f7b41-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f7b41-119">Requirement</span></span> | <span data-ttu-id="f7b41-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="f7b41-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f7b41-121">Version</span><span class="sxs-lookup"><span data-stu-id="f7b41-121">Version</span></span><br/> | <span data-ttu-id="f7b41-122">Lecteur Windows Media série 9 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="f7b41-122">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="f7b41-123">DLL</span><span class="sxs-lookup"><span data-stu-id="f7b41-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="f7b41-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f7b41-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7b41-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f7b41-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7b41-126">**Ajout de sous-titres à des médias numériques**</span><span class="sxs-lookup"><span data-stu-id="f7b41-126">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="f7b41-127">**Objet ClosedCaption**</span><span class="sxs-lookup"><span data-stu-id="f7b41-127">**ClosedCaption Object**</span></span>](closedcaption-object.md)
</dt> </dl>

 

 





