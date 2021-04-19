---
description: La fonction DisplayType envoie des informations sur un type de média à l’emplacement de sortie de débogage. Ignoré dans les builds de vente au détail.
ms.assetid: 63a88508-dff8-4869-97e5-0f75f4a9dca0
title: Fonction DisplayType (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DisplayType
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4f3d83bbe7a24463fc4cfaed4ace3adec9d6fcf7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530967"
---
# <a name="displaytype-function"></a><span data-ttu-id="00e3f-104">DisplayType, fonction</span><span class="sxs-lookup"><span data-stu-id="00e3f-104">DisplayType function</span></span>

<span data-ttu-id="00e3f-105">La `DisplayType` fonction envoie des informations sur un type de média à l’emplacement de sortie de débogage.</span><span class="sxs-lookup"><span data-stu-id="00e3f-105">The `DisplayType` function sends information about a media type to the debug output location.</span></span> <span data-ttu-id="00e3f-106">Ignoré dans les builds de vente au détail.</span><span class="sxs-lookup"><span data-stu-id="00e3f-106">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="00e3f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="00e3f-107">Syntax</span></span>


```C++
void DisplayType(
         LPTSTR        label,
   const AM_MEDIA_TYPE *pmtIn
);
```



## <a name="parameters"></a><span data-ttu-id="00e3f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="00e3f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00e3f-109">*label*</span><span class="sxs-lookup"><span data-stu-id="00e3f-109">*label*</span></span> 
</dt> <dd>

<span data-ttu-id="00e3f-110">Chaîne qui contient un message à afficher avec les informations sur le type de média.</span><span class="sxs-lookup"><span data-stu-id="00e3f-110">String that contains a message to display with the media type information.</span></span>

</dd> <dt>

<span data-ttu-id="00e3f-111">*pmtIn*</span><span class="sxs-lookup"><span data-stu-id="00e3f-111">*pmtIn*</span></span> 
</dt> <dd>

<span data-ttu-id="00e3f-112">ointer à la structure du [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) qui contient le type de média.</span><span class="sxs-lookup"><span data-stu-id="00e3f-112">ointer to the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that contains the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00e3f-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="00e3f-113">Return value</span></span>

<span data-ttu-id="00e3f-114">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="00e3f-114">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="00e3f-115">Notes</span><span class="sxs-lookup"><span data-stu-id="00e3f-115">Remarks</span></span>

<span data-ttu-id="00e3f-116">Cette fonction génère plusieurs messages de trace des journaux \_ .</span><span class="sxs-lookup"><span data-stu-id="00e3f-116">This function generates several LOG\_TRACE messages.</span></span> <span data-ttu-id="00e3f-117">Au niveau de la journalisation 2 ou supérieur, la fonction affiche le type, le sous-type et le type de format principaux, ainsi que les données du bloc de format.</span><span class="sxs-lookup"><span data-stu-id="00e3f-117">At logging level 2 or higher, the function displays the major type, subtype, and format type, and data from the format block.</span></span> <span data-ttu-id="00e3f-118">Au niveau de la journalisation 5 ou supérieur, la fonction affiche des informations supplémentaires, telles que les rectangles source et cible pour les types vidéo.</span><span class="sxs-lookup"><span data-stu-id="00e3f-118">At logging level 5 or higher, the function displays additional information, such as the source and target rectangles for video types.</span></span>

## <a name="requirements"></a><span data-ttu-id="00e3f-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="00e3f-119">Requirements</span></span>



| <span data-ttu-id="00e3f-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="00e3f-120">Requirement</span></span> | <span data-ttu-id="00e3f-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="00e3f-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00e3f-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="00e3f-122">Header</span></span><br/>  | <dl> <span data-ttu-id="00e3f-123"><dt>Wxdebug. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="00e3f-123"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="00e3f-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="00e3f-124">Library</span></span><br/> | <dl> <span data-ttu-id="00e3f-125"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="00e3f-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00e3f-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="00e3f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00e3f-127">Fonctions de sortie de débogage</span><span class="sxs-lookup"><span data-stu-id="00e3f-127">Debug Output Functions</span></span>](debug-output-functions.md)
</dt> </dl>

 

 




