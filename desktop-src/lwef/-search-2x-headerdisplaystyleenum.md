---
title: Énumération HeaderDisplayStyle
description: Utilisé par IResultsViewer HeaderStyle pour définir ou retourner le style d’en-tête actuel.
ms.assetid: 13ae6317-d990-4ccf-83b3-275caf953611
keywords:
- HeaderDisplayStyle, énumération des fonctionnalités d’environnement Windows héritées
topic_type:
- apiref
api_name:
- HeaderDisplayStyle
api_location:
- WdsView.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc65b17fa61b799fc9ab8ea7cc1b01380a5843c7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537091"
---
# <a name="headerdisplaystyle-enumeration"></a><span data-ttu-id="a8e61-104">Énumération HeaderDisplayStyle</span><span class="sxs-lookup"><span data-stu-id="a8e61-104">HeaderDisplayStyle enumeration</span></span>

> [!NOTE]
> <span data-ttu-id="a8e61-105">Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="a8e61-105">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="a8e61-106">Dans les versions ultérieures, utilisez plutôt l' [API Windows Search](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="a8e61-106">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="a8e61-107">Utilisé par [**IResultsViewer :: HeaderStyle**](-search-2x-iresultsviewer-headerstyle.md) pour définir ou retourner le style d’en-tête actuel.</span><span class="sxs-lookup"><span data-stu-id="a8e61-107">Used by [**IResultsViewer::HeaderStyle**](-search-2x-iresultsviewer-headerstyle.md) to set or return the current header style.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8e61-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a8e61-108">Syntax</span></span>


```C++
typedef enum HeaderDisplayStyleEnum { 
  FullHeader     = 0,
  CompactHeader  = 1,
  NoHeader       = 2
} HeaderDisplayStyle;
```



## <a name="constants"></a><span data-ttu-id="a8e61-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="a8e61-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="a8e61-110"><span id="FullHeader"></span><span id="fullheader"></span><span id="FULLHEADER"></span>**FullHeader**</span><span class="sxs-lookup"><span data-stu-id="a8e61-110"><span id="FullHeader"></span><span id="fullheader"></span><span id="FULLHEADER"></span>**FullHeader**</span></span>
</dt> <dd>

<span data-ttu-id="a8e61-111">Indique ou définit l’utilisation des en-têtes complets.</span><span class="sxs-lookup"><span data-stu-id="a8e61-111">Indicates or sets the use of full headers.</span></span>

</dd> <dt>

<span data-ttu-id="a8e61-112"><span id="CompactHeader"></span><span id="compactheader"></span><span id="COMPACTHEADER"></span>**CompactHeader**</span><span class="sxs-lookup"><span data-stu-id="a8e61-112"><span id="CompactHeader"></span><span id="compactheader"></span><span id="COMPACTHEADER"></span>**CompactHeader**</span></span>
</dt> <dd>

<span data-ttu-id="a8e61-113">Indique ou définit l’utilisation des en-têtes compacts.</span><span class="sxs-lookup"><span data-stu-id="a8e61-113">Indicates or sets the use of compact headers.</span></span>

</dd> <dt>

<span data-ttu-id="a8e61-114"><span id="NoHeader"></span><span id="noheader"></span><span id="NOHEADER"></span>**Noen-tête**</span><span class="sxs-lookup"><span data-stu-id="a8e61-114"><span id="NoHeader"></span><span id="noheader"></span><span id="NOHEADER"></span>**NoHeader**</span></span>
</dt> <dd>

<span data-ttu-id="a8e61-115">Indique ou définit l’utilisation d’aucun en-tête.</span><span class="sxs-lookup"><span data-stu-id="a8e61-115">Indicates or sets the use of no headers.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a8e61-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a8e61-116">Requirements</span></span>



| <span data-ttu-id="a8e61-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a8e61-117">Requirement</span></span> | <span data-ttu-id="a8e61-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="a8e61-118">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a8e61-119">MIDL</span><span class="sxs-lookup"><span data-stu-id="a8e61-119">IDL</span></span><br/> | <dl> <span data-ttu-id="a8e61-120"><dt>WdsView. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a8e61-120"><dt>WdsView.idl</dt></span></span> </dl> |



 

 





