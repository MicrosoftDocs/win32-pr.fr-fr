---
title: Media. erreur
description: La propriété Error récupère un objet ErrorItem si l’élément multimédia a une condition d’erreur.
ms.assetid: cd572688-12f9-4615-8f22-9442d615a2b6
keywords:
- Media. erreur dans le lecteur Windows Media
topic_type:
- apiref
api_name:
- Media.error
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5845252c817a424b0cbe414612fde47ed8b57328
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540402"
---
# <a name="mediaerror"></a><span data-ttu-id="1ad83-104">Media. erreur</span><span class="sxs-lookup"><span data-stu-id="1ad83-104">Media.error</span></span>

<span data-ttu-id="1ad83-105">La propriété **Error** récupère un objet **ErrorItem** si l’élément multimédia a une condition d’erreur.</span><span class="sxs-lookup"><span data-stu-id="1ad83-105">The **error** property retrieves an **ErrorItem** object if the media item has an error condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ad83-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1ad83-106">Syntax</span></span>

<span data-ttu-id="1ad83-107">*lecteur*. *currentMedia*. **erreur**</span><span class="sxs-lookup"><span data-stu-id="1ad83-107">*player*.*currentMedia*.**error**</span></span>

## <a name="possible-values"></a><span data-ttu-id="1ad83-108">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="1ad83-108">Possible Values</span></span>

<span data-ttu-id="1ad83-109">Cette propriété est un objet **ErrorItem** en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="1ad83-109">This property is a read-only **ErrorItem** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ad83-110">Notes</span><span class="sxs-lookup"><span data-stu-id="1ad83-110">Remarks</span></span>

<span data-ttu-id="1ad83-111">Si l’élément multimédia ne peut pas être lu, cette propriété récupère un objet **ErrorItem** qui contient des informations sur le problème rencontré.</span><span class="sxs-lookup"><span data-stu-id="1ad83-111">If the media item cannot be played, this property retrieves an **ErrorItem** object that contains information about the problem encountered.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ad83-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1ad83-112">Requirements</span></span>



| <span data-ttu-id="1ad83-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1ad83-113">Requirement</span></span> | <span data-ttu-id="1ad83-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="1ad83-114">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1ad83-115">Version</span><span class="sxs-lookup"><span data-stu-id="1ad83-115">Version</span></span><br/> | <span data-ttu-id="1ad83-116">Lecteur Windows Media pour Windows XP ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="1ad83-116">Windows Media Player for Windows XP or later.</span></span><br/>                           |
| <span data-ttu-id="1ad83-117">DLL</span><span class="sxs-lookup"><span data-stu-id="1ad83-117">DLL</span></span><br/>     | <dl> <span data-ttu-id="1ad83-118"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1ad83-118"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ad83-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1ad83-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ad83-120">**Objet ErrorItem**</span><span class="sxs-lookup"><span data-stu-id="1ad83-120">**ErrorItem Object**</span></span>](erroritem-object.md)
</dt> <dt>

[<span data-ttu-id="1ad83-121">**Objet Media**</span><span class="sxs-lookup"><span data-stu-id="1ad83-121">**Media Object**</span></span>](media-object.md)
</dt> </dl>

 

 





