---
title: Méthode IWMPClosedCaption2 getSAMILangID
description: La méthode getSAMILangID retourne l’identificateur de paramètres régionaux (LCID) d’une langue prise en charge par le fichier SAMI actuel.
ms.assetid: 41aca317-6182-47c3-8bd9-ba42b92b10f4
keywords:
- méthode getSAMILangID lecteur Windows Media
- méthode getSAMILangID lecteur Windows Media, interface IWMPClosedCaption2
- Interface IWMPClosedCaption2 lecteur Windows Media, méthode getSAMILangID
topic_type:
- apiref
api_name:
- IWMPClosedCaption2.getSAMILangID
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb9aaebecf8e86c056fa9c91141042facc6bcc18
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543921"
---
# <a name="iwmpclosedcaption2getsamilangid-method"></a><span data-ttu-id="36aca-106">IWMPClosedCaption2 :: getSAMILangID, méthode</span><span class="sxs-lookup"><span data-stu-id="36aca-106">IWMPClosedCaption2::getSAMILangID method</span></span>

<span data-ttu-id="36aca-107">La méthode **getSAMILangID** retourne l’identificateur de paramètres régionaux (LCID) d’une langue prise en charge par le fichier sami actuel.</span><span class="sxs-lookup"><span data-stu-id="36aca-107">The **getSAMILangID** method returns the locale identifier (LCID) of a language supported by the current SAMI file.</span></span>

## <a name="syntax"></a><span data-ttu-id="36aca-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="36aca-108">Syntax</span></span>


```CSharp
public System.Int32 getSAMILangID(
  System.Int32 nIndex
);
```


```VB

Public Function getSAMILangID( _
  ByVal nIndex As System.Int32 _
) As System.Int32
Implements IWMPClosedCaption2.getSAMILangID
```





## <a name="parameters"></a><span data-ttu-id="36aca-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="36aca-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36aca-110">*nIndex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="36aca-110">*nIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36aca-111">**System. Int32** qui correspond à l’index de base zéro du LCID à récupérer.</span><span class="sxs-lookup"><span data-stu-id="36aca-111">A **System.Int32** that is the zero-based index of the LCID to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36aca-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="36aca-112">Return value</span></span>

<span data-ttu-id="36aca-113">**System. Int32** qui est le LCID de la langue avec l’index spécifié.</span><span class="sxs-lookup"><span data-stu-id="36aca-113">A **System.Int32** that is the LCID of the language with the specified index.</span></span>

## <a name="remarks"></a><span data-ttu-id="36aca-114">Notes</span><span class="sxs-lookup"><span data-stu-id="36aca-114">Remarks</span></span>

<span data-ttu-id="36aca-115">Les langues d’un fichier SAMI sont indexées dans l’ordre indiqué dans le fichier, à partir de zéro.</span><span class="sxs-lookup"><span data-stu-id="36aca-115">The languages in a SAMI file are indexed in the order shown in the file, starting with zero.</span></span>

<span data-ttu-id="36aca-116">Cette méthode retourne la valeur 0, sauf si un fichier multimédia numérique est ouvert (AxWindowsMediaPlayer. openState est égal à 13).</span><span class="sxs-lookup"><span data-stu-id="36aca-116">This method returns 0 unless a digital media file is open (AxWindowsMediaPlayer.openState is equal to 13).</span></span>

## <a name="requirements"></a><span data-ttu-id="36aca-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="36aca-117">Requirements</span></span>



| <span data-ttu-id="36aca-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="36aca-118">Requirement</span></span> | <span data-ttu-id="36aca-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="36aca-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36aca-120">Version</span><span class="sxs-lookup"><span data-stu-id="36aca-120">Version</span></span><br/>   | <span data-ttu-id="36aca-121">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="36aca-121">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="36aca-122">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="36aca-122">Namespace</span></span><br/> | <span data-ttu-id="36aca-123">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="36aca-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="36aca-124">Assembly</span><span class="sxs-lookup"><span data-stu-id="36aca-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="36aca-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="36aca-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36aca-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="36aca-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36aca-127">**Ajout de sous-titres à des médias numériques**</span><span class="sxs-lookup"><span data-stu-id="36aca-127">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="36aca-128">**Interface IWMPClosedCaption (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="36aca-128">**IWMPClosedCaption Interface (VB and C#)**</span></span>](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="36aca-129">**Interface IWMPClosedCaption2 (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="36aca-129">**IWMPClosedCaption2 Interface (VB and C#)**</span></span>](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





