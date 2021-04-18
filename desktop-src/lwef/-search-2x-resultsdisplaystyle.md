---
title: Énumération ResultsDisplayStyle
description: Utilisé par IResultsViewer ResultsStyle pour définir ou déterminer le mode d’affichage des résultats.
ms.assetid: 24b474f2-1aca-4556-ba9a-3b8139e80bf0
keywords:
- ResultsDisplayStyle, énumération des fonctionnalités d’environnement Windows héritées
topic_type:
- apiref
api_name:
- ResultsDisplayStyle
api_location:
- WdsView.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26d564e0a7bb8a10b44e2957f26aa20a07afa535
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533187"
---
# <a name="resultsdisplaystyle-enumeration"></a><span data-ttu-id="115cd-104">Énumération ResultsDisplayStyle</span><span class="sxs-lookup"><span data-stu-id="115cd-104">ResultsDisplayStyle enumeration</span></span>

> [!NOTE]
> <span data-ttu-id="115cd-105">Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="115cd-105">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="115cd-106">Dans les versions ultérieures, utilisez plutôt l' [API Windows Search](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="115cd-106">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="115cd-107">Utilisé par [**IResultsViewer :: ResultsStyle**](-search-2x-iresultsviewer-resultsstyle.md) pour définir ou déterminer le mode d’affichage des résultats.</span><span class="sxs-lookup"><span data-stu-id="115cd-107">Used by [**IResultsViewer::ResultsStyle**](-search-2x-iresultsviewer-resultsstyle.md) to set or determine how results are displayed.</span></span>

## <a name="syntax"></a><span data-ttu-id="115cd-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="115cd-108">Syntax</span></span>


```C++
typedef enum ResultsDisplayStyleEnum { 
  SmallIconResults  = 0,
  LargeIconResults  = 1
} ResultsDisplayStyle;
```



## <a name="constants"></a><span data-ttu-id="115cd-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="115cd-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="115cd-110"><span id="SmallIconResults"></span><span id="smalliconresults"></span><span id="SMALLICONRESULTS"></span>**SmallIconResults**</span><span class="sxs-lookup"><span data-stu-id="115cd-110"><span id="SmallIconResults"></span><span id="smalliconresults"></span><span id="SMALLICONRESULTS"></span>**SmallIconResults**</span></span>
</dt> <dd>

<span data-ttu-id="115cd-111">Indique que les résultats sont affichés sous forme de petites icônes.</span><span class="sxs-lookup"><span data-stu-id="115cd-111">Indicates Results are displayed as small icons.</span></span>

</dd> <dt>

<span data-ttu-id="115cd-112"><span id="LargeIconResults"></span><span id="largeiconresults"></span><span id="LARGEICONRESULTS"></span>**LargeIconResults**</span><span class="sxs-lookup"><span data-stu-id="115cd-112"><span id="LargeIconResults"></span><span id="largeiconresults"></span><span id="LARGEICONRESULTS"></span>**LargeIconResults**</span></span>
</dt> <dd>

<span data-ttu-id="115cd-113">Indique que les résultats sont affichés sous forme de grandes icônes.</span><span class="sxs-lookup"><span data-stu-id="115cd-113">Indicates Results are displayed as large icons.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="115cd-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="115cd-114">Requirements</span></span>



| <span data-ttu-id="115cd-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="115cd-115">Requirement</span></span> | <span data-ttu-id="115cd-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="115cd-116">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="115cd-117">MIDL</span><span class="sxs-lookup"><span data-stu-id="115cd-117">IDL</span></span><br/> | <dl> <span data-ttu-id="115cd-118"><dt>WdsView. idl</dt></span><span class="sxs-lookup"><span data-stu-id="115cd-118"><dt>WdsView.idl</dt></span></span> </dl> |



 

 





