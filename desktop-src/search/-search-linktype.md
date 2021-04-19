---
description: Spécifie le type de lien lors de l’analyse ou de l’indexation.
ms.assetid: 2a0ddb31-df35-4da5-9950-b091cd461556
title: Énumération LINKTYPE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LINKTYPE
api_type:
- NA
api_location: ''
ms.openlocfilehash: e5b2105e8d56a9c8042f341ffc3f24a4d7995f4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514793"
---
# <a name="linktype-enumeration"></a><span data-ttu-id="8dcba-103">Énumération LINKTYPE</span><span class="sxs-lookup"><span data-stu-id="8dcba-103">LINKTYPE enumeration</span></span>

<span data-ttu-id="8dcba-104">\[L’énumération **LinkType** est prise en charge uniquement sur Windows XP et windows Server 2003 et ne doit plus être utilisée.\]</span><span class="sxs-lookup"><span data-stu-id="8dcba-104">\[The **LINKTYPE** enumeration is supported only on Windows XP and Windows Server 2003, and should no longer be used.\]</span></span>

<span data-ttu-id="8dcba-105">Spécifie le type de lien lors de l’analyse ou de l’indexation.</span><span class="sxs-lookup"><span data-stu-id="8dcba-105">Specifies the type of link when crawling or indexing.</span></span>

## <a name="syntax"></a><span data-ttu-id="8dcba-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8dcba-106">Syntax</span></span>


```C++
typedef enum _LINKTYPE { 
  LINKTYPE_URL      = 0x00000000,
  LINKTYPE_CONTENT  = 0x00000001,
  LINKTYPE_RELATED  = 0x00000002
} LINKTYPE;
```



## <a name="constants"></a><span data-ttu-id="8dcba-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="8dcba-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="8dcba-108"><span id="LINKTYPE_URL"></span><span id="linktype_url"></span>**\_URL LinkType**</span><span class="sxs-lookup"><span data-stu-id="8dcba-108"><span id="LINKTYPE_URL"></span><span id="linktype_url"></span>**LINKTYPE\_URL**</span></span>
</dt> <dd>

<span data-ttu-id="8dcba-109">Spécifie si le type de lien des URL doit être indexé.</span><span class="sxs-lookup"><span data-stu-id="8dcba-109">Specifies whether the URLs link type should be indexed.</span></span>

</dd> <dt>

<span data-ttu-id="8dcba-110"><span id="LINKTYPE_CONTENT"></span><span id="linktype_content"></span>**\_contenu LinkType**</span><span class="sxs-lookup"><span data-stu-id="8dcba-110"><span id="LINKTYPE_CONTENT"></span><span id="linktype_content"></span>**LINKTYPE\_CONTENT**</span></span>
</dt> <dd>

<span data-ttu-id="8dcba-111">Spécifie si le contenu du lien doit être indexé.</span><span class="sxs-lookup"><span data-stu-id="8dcba-111">Specifies whether the link content should be indexed.</span></span>

</dd> <dt>

<span data-ttu-id="8dcba-112"><span id="LINKTYPE_RELATED"></span><span id="linktype_related"></span>**LINKTYPE \_ associées**</span><span class="sxs-lookup"><span data-stu-id="8dcba-112"><span id="LINKTYPE_RELATED"></span><span id="linktype_related"></span>**LINKTYPE\_RELATED**</span></span>
</dt> <dd>

<span data-ttu-id="8dcba-113">Spécifie un lien associé.</span><span class="sxs-lookup"><span data-stu-id="8dcba-113">Specifies a related link.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8dcba-114">Notes</span><span class="sxs-lookup"><span data-stu-id="8dcba-114">Remarks</span></span>

<span data-ttu-id="8dcba-115">Pour afficher un aperçu des pièces jointes avec un gestionnaire de protocole tiers sur les ordinateurs exécutant Windows XP ou Windows Server 2003, il peut être nécessaire d’utiliser les indicateurs **LinkType** et les autres API suivantes : les méthodes [**IItemPreviewerExt :: GetLinkedContent**](-search-iitempreviewerext-getlinkedcontent.md) et [**IItemPreviewerExt :: GetRelatedPart**](-search-iitempreviewerext-getrelatedpart.md) , et la structure [**LINKINFO**](-search-linkinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="8dcba-115">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the **LINKTYPE** flags, and the following other APIs: the [**IItemPreviewerExt::GetLinkedContent**](-search-iitempreviewerext-getlinkedcontent.md) and [**IItemPreviewerExt::GetRelatedPart**](-search-iitempreviewerext-getrelatedpart.md) methods, and the [**LINKINFO**](-search-linkinfo.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="8dcba-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8dcba-116">Requirements</span></span>



| <span data-ttu-id="8dcba-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8dcba-117">Requirement</span></span> | <span data-ttu-id="8dcba-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="8dcba-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8dcba-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8dcba-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8dcba-120">Windows XP avec les \[ applications de bureau SP2 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8dcba-120">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="8dcba-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8dcba-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8dcba-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8dcba-122">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



 

 




