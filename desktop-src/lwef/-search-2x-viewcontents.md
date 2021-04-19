---
title: Énumération ViewContents
description: Utilisé par le contenu IResultsViewer pour indiquer ou définir le mode d’affichage du jeu de requêtes actuel.
ms.assetid: aebcbcac-4c45-4097-91a1-5e00611c152c
keywords:
- ViewContents, énumération des fonctionnalités d’environnement Windows héritées
topic_type:
- apiref
api_name:
- ViewContents
api_location:
- WdsView.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f465b16ef81dd71695f8de0b04b6d7567480f4c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106531144"
---
# <a name="viewcontents-enumeration"></a><span data-ttu-id="5d243-104">Énumération ViewContents</span><span class="sxs-lookup"><span data-stu-id="5d243-104">ViewContents enumeration</span></span>

> [!NOTE]
> <span data-ttu-id="5d243-105">Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="5d243-105">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="5d243-106">Dans les versions ultérieures, utilisez plutôt l' [API Windows Search](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="5d243-106">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="5d243-107">Utilisé par [**IResultsViewer :: content**](-search-2x-iresultsviewer-contents.md) pour indiquer ou définir le mode d’affichage du jeu de requêtes actuel.</span><span class="sxs-lookup"><span data-stu-id="5d243-107">Used by [**IResultsViewer::Contents**](-search-2x-iresultsviewer-contents.md) to indicate or set how the current query return set is displayed.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d243-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5d243-108">Syntax</span></span>


```C++
typedef enum ViewContentsEnum { 
  ResultsDisplayed     = 0,
  ShellViewDisplayed   = 1,
  WebBrowserDisplayed  = 2
} ViewContents;
```



## <a name="constants"></a><span data-ttu-id="5d243-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="5d243-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="5d243-110"><span id="ResultsDisplayed"></span><span id="resultsdisplayed"></span><span id="RESULTSDISPLAYED"></span>**ResultsDisplayed**</span><span class="sxs-lookup"><span data-stu-id="5d243-110"><span id="ResultsDisplayed"></span><span id="resultsdisplayed"></span><span id="RESULTSDISPLAYED"></span>**ResultsDisplayed**</span></span>
</dt> <dd>

<span data-ttu-id="5d243-111">Indique le type de contenu affiché dans l’affichage des résultats.</span><span class="sxs-lookup"><span data-stu-id="5d243-111">Indicates the type of contents being displayed in the results view.</span></span>

</dd> <dt>

<span data-ttu-id="5d243-112"><span id="ShellViewDisplayed"></span><span id="shellviewdisplayed"></span><span id="SHELLVIEWDISPLAYED"></span>**ShellViewDisplayed**</span><span class="sxs-lookup"><span data-stu-id="5d243-112"><span id="ShellViewDisplayed"></span><span id="shellviewdisplayed"></span><span id="SHELLVIEWDISPLAYED"></span>**ShellViewDisplayed**</span></span>
</dt> <dd>

<span data-ttu-id="5d243-113">Indique que le type de contenu affiché dans l’affichage des résultats est actuellement défini sur la vue de l’interpréteur de commandes.</span><span class="sxs-lookup"><span data-stu-id="5d243-113">Indicates the type of contents being displayed in the results view is currently set to the Shell view.</span></span>

</dd> <dt>

<span data-ttu-id="5d243-114"><span id="WebBrowserDisplayed"></span><span id="webbrowserdisplayed"></span><span id="WEBBROWSERDISPLAYED"></span>**WebBrowserDisplayed**</span><span class="sxs-lookup"><span data-stu-id="5d243-114"><span id="WebBrowserDisplayed"></span><span id="webbrowserdisplayed"></span><span id="WEBBROWSERDISPLAYED"></span>**WebBrowserDisplayed**</span></span>
</dt> <dd>

<span data-ttu-id="5d243-115">Indique que le type de contenu affiché dans l’affichage des résultats est actuellement défini sur la vue du navigateur.</span><span class="sxs-lookup"><span data-stu-id="5d243-115">Indicates the type of contents being displayed in the results view is currently set to the browser view.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5d243-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5d243-116">Requirements</span></span>



| <span data-ttu-id="5d243-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5d243-117">Requirement</span></span> | <span data-ttu-id="5d243-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="5d243-118">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5d243-119">MIDL</span><span class="sxs-lookup"><span data-stu-id="5d243-119">IDL</span></span><br/> | <dl> <span data-ttu-id="5d243-120"><dt>WdsView. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5d243-120"><dt>WdsView.idl</dt></span></span> </dl> |



 

 





