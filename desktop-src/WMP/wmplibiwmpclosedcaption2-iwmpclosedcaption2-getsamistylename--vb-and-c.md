---
title: Méthode IWMPClosedCaption2 getSAMIStyleName
description: La méthode getSAMIStyleName retourne le nom d’un style pris en charge par le fichier SAMI actuel.
ms.assetid: e7678ca6-f52f-45f4-bd1c-7fbcdf1cc47c
keywords:
- méthode getSAMIStyleName lecteur Windows Media
- méthode getSAMIStyleName lecteur Windows Media, interface IWMPClosedCaption2
- Interface IWMPClosedCaption2 lecteur Windows Media, méthode getSAMIStyleName
topic_type:
- apiref
api_name:
- IWMPClosedCaption2.getSAMIStyleName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34ceb3f598ae603d478af5cad9c78333952530a2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533450"
---
# <a name="iwmpclosedcaption2getsamistylename-method"></a><span data-ttu-id="b0262-106">IWMPClosedCaption2 :: getSAMIStyleName, méthode</span><span class="sxs-lookup"><span data-stu-id="b0262-106">IWMPClosedCaption2::getSAMIStyleName method</span></span>

<span data-ttu-id="b0262-107">La méthode **getSAMIStyleName** retourne le nom d’un style pris en charge par le fichier sami actuel.</span><span class="sxs-lookup"><span data-stu-id="b0262-107">The **getSAMIStyleName** method returns the name of a style supported by the current SAMI file.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0262-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b0262-108">Syntax</span></span>


```CSharp
public System.String getSAMIStyleName(
  System.Int32 nIndex
);
```


```VB

Public Function getSAMIStyleName( _
  ByVal nIndex As System.Int32 _
) As System.String
Implements IWMPClosedCaption2.getSAMIStyleName
```





## <a name="parameters"></a><span data-ttu-id="b0262-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b0262-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0262-110">*nIndex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b0262-110">*nIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0262-111">**System. Int32** qui est l’index de base zéro du nom de style à récupérer</span><span class="sxs-lookup"><span data-stu-id="b0262-111">A **System.Int32** that is the zero-based index of the style name to retrieve</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0262-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b0262-112">Return value</span></span>

<span data-ttu-id="b0262-113">**System. String** qui est le nom du style tel que spécifié dans le fichier sami.</span><span class="sxs-lookup"><span data-stu-id="b0262-113">A **System.String** that is the name of the style as specified in the SAMI file.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0262-114">Notes</span><span class="sxs-lookup"><span data-stu-id="b0262-114">Remarks</span></span>

<span data-ttu-id="b0262-115">Les styles d’un fichier SAMI sont indexés dans l’ordre indiqué dans le fichier, à partir de zéro.</span><span class="sxs-lookup"><span data-stu-id="b0262-115">The styles in a SAMI file are indexed in the order shown in the file, starting with zero.</span></span>

<span data-ttu-id="b0262-116">Cette méthode retourne une chaîne de longueur nulle (""), à moins qu’un fichier multimédia numérique soit ouvert (AxWindowsMediaPlayer. openState est égal à 13).</span><span class="sxs-lookup"><span data-stu-id="b0262-116">This method returns a zero-length string ("") unless a digital media file is open (AxWindowsMediaPlayer.openState is equal to 13).</span></span>

## <a name="requirements"></a><span data-ttu-id="b0262-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b0262-117">Requirements</span></span>



| <span data-ttu-id="b0262-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b0262-118">Requirement</span></span> | <span data-ttu-id="b0262-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="b0262-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0262-120">Version</span><span class="sxs-lookup"><span data-stu-id="b0262-120">Version</span></span><br/>   | <span data-ttu-id="b0262-121">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="b0262-121">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="b0262-122">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="b0262-122">Namespace</span></span><br/> | <span data-ttu-id="b0262-123">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="b0262-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="b0262-124">Assembly</span><span class="sxs-lookup"><span data-stu-id="b0262-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="b0262-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="b0262-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0262-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b0262-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0262-127">**Ajout de sous-titres à des médias numériques**</span><span class="sxs-lookup"><span data-stu-id="b0262-127">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="b0262-128">**Interface IWMPClosedCaption (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="b0262-128">**IWMPClosedCaption Interface (VB and C#)**</span></span>](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b0262-129">**IWMPClosedCaption. SAMIStyle (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="b0262-129">**IWMPClosedCaption.SAMIStyle (VB and C#)**</span></span>](wmplibiwmpclosedcaption-iwmpclosedcaption-samistyle--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b0262-130">**Interface IWMPClosedCaption2 (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="b0262-130">**IWMPClosedCaption2 Interface (VB and C#)**</span></span>](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





