---
title: Méthode IWMPClosedCaption2 getSAMILangName
description: La méthode getSAMILangName retourne le nom d’une langue prise en charge par le fichier SAMI actuel.
ms.assetid: 52aaf1cc-89ef-4c4c-af43-3f88dc4a9539
keywords:
- méthode getSAMILangName lecteur Windows Media
- méthode getSAMILangName lecteur Windows Media, interface IWMPClosedCaption2
- Interface IWMPClosedCaption2 lecteur Windows Media, méthode getSAMILangName
topic_type:
- apiref
api_name:
- IWMPClosedCaption2.getSAMILangName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e50df643fdd6b665de1275873fb8de9d5d094a42
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543920"
---
# <a name="iwmpclosedcaption2getsamilangname-method"></a><span data-ttu-id="0d8d6-106">IWMPClosedCaption2 :: getSAMILangName, méthode</span><span class="sxs-lookup"><span data-stu-id="0d8d6-106">IWMPClosedCaption2::getSAMILangName method</span></span>

<span data-ttu-id="0d8d6-107">La méthode **getSAMILangName** retourne le nom d’une langue prise en charge par le fichier sami actuel.</span><span class="sxs-lookup"><span data-stu-id="0d8d6-107">The **getSAMILangName** method returns the name of a language supported by the current SAMI file.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d8d6-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0d8d6-108">Syntax</span></span>


```CSharp
public System.String getSAMILangName(
  System.Int32 nIndex
);
```


```VB

Public Function getSAMILangName( _
  ByVal nIndex As System.Int32 _
) As System.String
Implements IWMPClosedCaption2.getSAMILangName
```





## <a name="parameters"></a><span data-ttu-id="0d8d6-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0d8d6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d8d6-110">*nIndex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0d8d6-110">*nIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d8d6-111">**System. Int32** qui correspond à l’index de base zéro du nom de langage à récupérer.</span><span class="sxs-lookup"><span data-stu-id="0d8d6-111">**A System.Int32** that is the zero-based index of the language name to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d8d6-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0d8d6-112">Return value</span></span>

<span data-ttu-id="0d8d6-113">**System. String** qui est le nom de la langue tel que spécifié dans le fichier sami.</span><span class="sxs-lookup"><span data-stu-id="0d8d6-113">A **System.String** that is the name of the language as specified in the SAMI file.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d8d6-114">Notes</span><span class="sxs-lookup"><span data-stu-id="0d8d6-114">Remarks</span></span>

<span data-ttu-id="0d8d6-115">Les langues d’un fichier SAMI sont indexées dans l’ordre indiqué dans le fichier, à partir de zéro.</span><span class="sxs-lookup"><span data-stu-id="0d8d6-115">The languages in a SAMI file are indexed in the order shown in the file, starting with zero.</span></span>

<span data-ttu-id="0d8d6-116">Cette méthode retourne une chaîne de longueur nulle (""), à moins qu’un fichier multimédia numérique soit ouvert (AxWindowsMediaPlayer. openState est égal à 13).</span><span class="sxs-lookup"><span data-stu-id="0d8d6-116">This method returns a zero-length string ("") unless a digital media file is open (AxWindowsMediaPlayer.openState is equal to 13).</span></span>

## <a name="requirements"></a><span data-ttu-id="0d8d6-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0d8d6-117">Requirements</span></span>



| <span data-ttu-id="0d8d6-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0d8d6-118">Requirement</span></span> | <span data-ttu-id="0d8d6-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="0d8d6-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d8d6-120">Version</span><span class="sxs-lookup"><span data-stu-id="0d8d6-120">Version</span></span><br/>   | <span data-ttu-id="0d8d6-121">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="0d8d6-121">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="0d8d6-122">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="0d8d6-122">Namespace</span></span><br/> | <span data-ttu-id="0d8d6-123">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="0d8d6-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="0d8d6-124">Assembly</span><span class="sxs-lookup"><span data-stu-id="0d8d6-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="0d8d6-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="0d8d6-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d8d6-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0d8d6-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d8d6-127">**Ajout de sous-titres à des médias numériques**</span><span class="sxs-lookup"><span data-stu-id="0d8d6-127">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="0d8d6-128">**Interface IWMPClosedCaption (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="0d8d6-128">**IWMPClosedCaption Interface (VB and C#)**</span></span>](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="0d8d6-129">**IWMPClosedCaption. SAMILang (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="0d8d6-129">**IWMPClosedCaption.SAMILang (VB and C#)**</span></span>](wmplibiwmpclosedcaption-iwmpclosedcaption-samilang--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="0d8d6-130">**Interface IWMPClosedCaption2 (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="0d8d6-130">**IWMPClosedCaption2 Interface (VB and C#)**</span></span>](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





