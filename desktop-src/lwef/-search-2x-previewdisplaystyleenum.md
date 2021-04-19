---
title: Énumération PreviewDisplayStyle
description: Utilisé par IResultsViewer PreviewStyle pour définir ou déterminer le style d’affichage en cours d’utilisation.
ms.assetid: ccbbfe38-0719-41e0-9331-cc0c1be651eb
keywords:
- PreviewDisplayStyle, énumération des fonctionnalités d’environnement Windows héritées
topic_type:
- apiref
api_name:
- PreviewDisplayStyle
api_location:
- WdsView.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11902821ec9fdbbaa9ab8d3fda8971f42fc28c1f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541503"
---
# <a name="previewdisplaystyle-enumeration"></a><span data-ttu-id="333e8-104">Énumération PreviewDisplayStyle</span><span class="sxs-lookup"><span data-stu-id="333e8-104">PreviewDisplayStyle enumeration</span></span>

> [!NOTE]
> <span data-ttu-id="333e8-105">Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="333e8-105">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="333e8-106">Dans les versions ultérieures, utilisez plutôt l' [API Windows Search](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="333e8-106">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="333e8-107">Utilisé par [**IResultsViewer ::P reviewstyle**](-search-2x-iresultsviewer-previewstyle.md) pour définir ou déterminer le style d’affichage en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="333e8-107">Used by [**IResultsViewer::PreviewStyle**](-search-2x-iresultsviewer-previewstyle.md) to set or determine the display style currently being used.</span></span>

## <a name="syntax"></a><span data-ttu-id="333e8-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="333e8-108">Syntax</span></span>


```C++
typedef enum PreviewDisplayStyleEnum { 
  AutoPreview    = 0,
  RightPreview   = 1,
  BottomPreview  = 2,
  NoPreview      = 3
} PreviewDisplayStyle;
```



## <a name="constants"></a><span data-ttu-id="333e8-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="333e8-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="333e8-110"><span id="AutoPreview"></span><span id="autopreview"></span><span id="AUTOPREVIEW"></span>**Aperçu partiel**</span><span class="sxs-lookup"><span data-stu-id="333e8-110"><span id="AutoPreview"></span><span id="autopreview"></span><span id="AUTOPREVIEW"></span>**AutoPreview**</span></span>
</dt> <dd>

<span data-ttu-id="333e8-111">Indique l’aperçu partiel.</span><span class="sxs-lookup"><span data-stu-id="333e8-111">Indicates AutoPreview.</span></span>

</dd> <dt>

<span data-ttu-id="333e8-112"><span id="RightPreview"></span><span id="rightpreview"></span><span id="RIGHTPREVIEW"></span>**RightPreview**</span><span class="sxs-lookup"><span data-stu-id="333e8-112"><span id="RightPreview"></span><span id="rightpreview"></span><span id="RIGHTPREVIEW"></span>**RightPreview**</span></span>
</dt> <dd>

<span data-ttu-id="333e8-113">Indique RightPreview.</span><span class="sxs-lookup"><span data-stu-id="333e8-113">Indicates RightPreview.</span></span>

</dd> <dt>

<span data-ttu-id="333e8-114"><span id="BottomPreview"></span><span id="bottompreview"></span><span id="BOTTOMPREVIEW"></span>**BottomPreview**</span><span class="sxs-lookup"><span data-stu-id="333e8-114"><span id="BottomPreview"></span><span id="bottompreview"></span><span id="BOTTOMPREVIEW"></span>**BottomPreview**</span></span>
</dt> <dd>

<span data-ttu-id="333e8-115">Indique BottomPreview.</span><span class="sxs-lookup"><span data-stu-id="333e8-115">Indicates BottomPreview.</span></span>

</dd> <dt>

<span data-ttu-id="333e8-116"><span id="NoPreview"></span><span id="nopreview"></span><span id="NOPREVIEW"></span>**Nopreview**</span><span class="sxs-lookup"><span data-stu-id="333e8-116"><span id="NoPreview"></span><span id="nopreview"></span><span id="NOPREVIEW"></span>**NoPreview**</span></span>
</dt> <dd>

<span data-ttu-id="333e8-117">Indique nopreview.</span><span class="sxs-lookup"><span data-stu-id="333e8-117">Indicates NoPreview.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="333e8-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="333e8-118">Requirements</span></span>



| <span data-ttu-id="333e8-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="333e8-119">Requirement</span></span> | <span data-ttu-id="333e8-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="333e8-120">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="333e8-121">MIDL</span><span class="sxs-lookup"><span data-stu-id="333e8-121">IDL</span></span><br/> | <dl> <span data-ttu-id="333e8-122"><dt>WdsView. idl</dt></span><span class="sxs-lookup"><span data-stu-id="333e8-122"><dt>WdsView.idl</dt></span></span> </dl> |



 

 





