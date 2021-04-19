---
title: Méthode ClosedCaption. getSAMILangName
description: La méthode getSAMILangName récupère le nom d’une langue prise en charge par le fichier SAMI actuel.
ms.assetid: 20cf8faf-3a8c-4d7b-9bd1-2366672f0e67
keywords:
- méthode getSAMILangName lecteur Windows Media
- méthode getSAMILangName lecteur Windows Media, classe ClosedCaption
- Classe ClosedCaption lecteur Windows Media, méthode getSAMILangName
topic_type:
- apiref
api_name:
- ClosedCaption.getSAMILangName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccd4b481de808ac8814e596cfc038aec38c7f19b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528761"
---
# <a name="closedcaptiongetsamilangname-method"></a><span data-ttu-id="0e8b9-106">Méthode ClosedCaption. getSAMILangName</span><span class="sxs-lookup"><span data-stu-id="0e8b9-106">ClosedCaption.getSAMILangName method</span></span>

<span data-ttu-id="0e8b9-107">La méthode **getSAMILangName** récupère le nom d’une langue prise en charge par le fichier sami actuel.</span><span class="sxs-lookup"><span data-stu-id="0e8b9-107">The **getSAMILangName** method retrieves the name of a language supported by the current SAMI file.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e8b9-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0e8b9-108">Syntax</span></span>


```JScript
strRetVal = ClosedCaption.getSAMILangName(
  index
)
```



## <a name="parameters"></a><span data-ttu-id="0e8b9-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0e8b9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e8b9-110">*index* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0e8b9-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e8b9-111">**Nombre** (**long**) spécifiant l’index du nom de la langue à récupérer.</span><span class="sxs-lookup"><span data-stu-id="0e8b9-111">**Number** (**long**) specifying the index of the language name to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e8b9-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0e8b9-112">Return value</span></span>

<span data-ttu-id="0e8b9-113">Cette méthode retourne une **chaîne** contenant le nom de la langue tel que spécifié dans le fichier sami.</span><span class="sxs-lookup"><span data-stu-id="0e8b9-113">This method returns a **String** containing the name of the language as specified in the SAMI file.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e8b9-114">Notes</span><span class="sxs-lookup"><span data-stu-id="0e8b9-114">Remarks</span></span>

<span data-ttu-id="0e8b9-115">Les langues d’un fichier SAMI sont indexées dans l’ordre indiqué dans le fichier, à partir de zéro.</span><span class="sxs-lookup"><span data-stu-id="0e8b9-115">The languages in a SAMI file are indexed in the order shown in the file, starting with zero.</span></span>

<span data-ttu-id="0e8b9-116">Cette méthode ne peut pas être utilisée tant qu’un fichier multimédia numérique n’est pas ouvert (*lecteur*.**openState** est égal à 13).</span><span class="sxs-lookup"><span data-stu-id="0e8b9-116">This method cannot be used until a digital media file is open (*Player*.**openState** is equal to 13).</span></span>

<span data-ttu-id="0e8b9-117">**Lecteur Windows Media 10 Mobile :** Cette méthode n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="0e8b9-117">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e8b9-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0e8b9-118">Requirements</span></span>



| <span data-ttu-id="0e8b9-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0e8b9-119">Requirement</span></span> | <span data-ttu-id="0e8b9-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="0e8b9-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0e8b9-121">Version</span><span class="sxs-lookup"><span data-stu-id="0e8b9-121">Version</span></span><br/> | <span data-ttu-id="0e8b9-122">Lecteur Windows Media série 9 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="0e8b9-122">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="0e8b9-123">DLL</span><span class="sxs-lookup"><span data-stu-id="0e8b9-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="0e8b9-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0e8b9-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e8b9-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0e8b9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e8b9-126">**Ajout de sous-titres à des médias numériques**</span><span class="sxs-lookup"><span data-stu-id="0e8b9-126">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="0e8b9-127">**Objet ClosedCaption**</span><span class="sxs-lookup"><span data-stu-id="0e8b9-127">**ClosedCaption Object**</span></span>](closedcaption-object.md)
</dt> <dt>

[<span data-ttu-id="0e8b9-128">**ClosedCaption.SAMILang**</span><span class="sxs-lookup"><span data-stu-id="0e8b9-128">**ClosedCaption.SAMILang**</span></span>](closedcaption-samilang.md)
</dt> </dl>

 

 





