---
title: WM/GenreID
description: L’attribut WM/GenreID contient un identificateur de genre conforme au contenu de la balise TCON dans ID3v2.
ms.assetid: 2f2a87f7-ba2d-465a-a36b-a8f58b5dd2d0
keywords:
- Format Windows Media WM/GenreID
topic_type:
- apiref
api_name:
- WM/GenreID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a3b25dffe69471f47eaf20124af48141835540f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104380975"
---
# <a name="wmgenreid"></a><span data-ttu-id="c0c12-104">WM/GenreID</span><span class="sxs-lookup"><span data-stu-id="c0c12-104">WM/GenreID</span></span>

<span data-ttu-id="c0c12-105">L’attribut **WM/GenreID** contient un identificateur de genre conforme au contenu de la balise TCON dans ID3v2.</span><span class="sxs-lookup"><span data-stu-id="c0c12-105">The **WM/GenreID** attribute contains a genre identifier compliant with the contents of the TCON tag in ID3v2.</span></span> <span data-ttu-id="c0c12-106">Il doit contenir l’ID de genre entre parenthèses, éventuellement suivi d’un perfectionnement qui décrit plus en détail le genre.</span><span class="sxs-lookup"><span data-stu-id="c0c12-106">This should contain the genre ID in parentheses, optionally followed by a refinement further describing the genre.</span></span> <span data-ttu-id="c0c12-107">Pour plus d’informations, reportez-vous à la spécification ID3v2.</span><span class="sxs-lookup"><span data-stu-id="c0c12-107">For more information, refer to the ID3v2 specification.</span></span>

## <a name="global-constant"></a><span data-ttu-id="c0c12-108">Constante globale</span><span class="sxs-lookup"><span data-stu-id="c0c12-108">Global Constant</span></span>

<span data-ttu-id="c0c12-109">\_wszWMGenreID g</span><span class="sxs-lookup"><span data-stu-id="c0c12-109">g\_wszWMGenreID</span></span>

## <a name="data-type"></a><span data-ttu-id="c0c12-110">Type de données</span><span class="sxs-lookup"><span data-stu-id="c0c12-110">Data Type</span></span>

<span data-ttu-id="c0c12-111">**\_chaîne de type WMT \_**</span><span class="sxs-lookup"><span data-stu-id="c0c12-111">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="c0c12-112">Notes</span><span class="sxs-lookup"><span data-stu-id="c0c12-112">Remarks</span></span>

<span data-ttu-id="c0c12-113">L’attribut préféré pour la spécification d’un genre est [**WM/genre**](wm-genre.md).</span><span class="sxs-lookup"><span data-stu-id="c0c12-113">The preferred attribute for specifying a genre is [**WM/Genre**](wm-genre.md).</span></span> <span data-ttu-id="c0c12-114">Utilisez-le à la préférence pour cet attribut.</span><span class="sxs-lookup"><span data-stu-id="c0c12-114">Use it in preference to this attribute.</span></span>

<span data-ttu-id="c0c12-115">Si vous modifiez **WM/genre** ou **WM/GenreID** dans un fichier mp3, l’autre attribut sera modifié en correspondance.</span><span class="sxs-lookup"><span data-stu-id="c0c12-115">If you change either **WM/Genre** or **WM/GenreID** in an MP3 file, the other attribute will be changed to match.</span></span>

### <a name="example"></a><span data-ttu-id="c0c12-116">Exemple</span><span class="sxs-lookup"><span data-stu-id="c0c12-116">Example</span></span>



| <span data-ttu-id="c0c12-117">Type de fichier</span><span class="sxs-lookup"><span data-stu-id="c0c12-117">File type</span></span> | <span data-ttu-id="c0c12-118">Valeur d'exemple</span><span class="sxs-lookup"><span data-stu-id="c0c12-118">Example value</span></span>   |
|-----------|-----------------|
| <span data-ttu-id="c0c12-119">Audio</span><span class="sxs-lookup"><span data-stu-id="c0c12-119">Audio</span></span>     | <span data-ttu-id="c0c12-120">« (4) Eurodisco »</span><span class="sxs-lookup"><span data-stu-id="c0c12-120">"(4) Eurodisco"</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="c0c12-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c0c12-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0c12-122">**Liste d’attributs**</span><span class="sxs-lookup"><span data-stu-id="c0c12-122">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




