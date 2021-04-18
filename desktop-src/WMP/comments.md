---
title: Commentaires (msfeeds. h)
description: Ajoutez des commentaires aux fichiers de données en suivant la syntaxe Extensible Markup Language (XML). Les commentaires commencent par \ 0034 ; --\ 0034 ; et se terminent par \ 0034 ;--\ 0034 ;.
ms.assetid: 3d8dbf13-bd48-4405-804f-57e0f5eff642
keywords:
- Commentaires sur le lecteur Windows Media
topic_type:
- apiref
api_name:
- Comments
api_location:
- msfeeds.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 701f456cae9f1432ed42235a3a6e13af555b2b8d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106529029"
---
# <a name="comments-msfeedsh"></a><span data-ttu-id="65b6e-105">Commentaires (msfeeds. h)</span><span class="sxs-lookup"><span data-stu-id="65b6e-105">Comments (Msfeeds.h)</span></span>

<span data-ttu-id="65b6e-106">Ajoutez des commentaires aux fichiers de données en suivant la syntaxe Extensible Markup Language (XML).</span><span class="sxs-lookup"><span data-stu-id="65b6e-106">Add comments to metafiles by following Extensible Markup Language (XML) syntax.</span></span> <span data-ttu-id="65b6e-107">Les commentaires commencent par « &lt; !-- » et se terminent par « -- &gt; ».</span><span class="sxs-lookup"><span data-stu-id="65b6e-107">Comments begin with "&lt;!--" and end with "--&gt;".</span></span>

``` syntax

<!--Enter your comment text here.-->
```

## <a name="remarks"></a><span data-ttu-id="65b6e-108">Notes</span><span class="sxs-lookup"><span data-stu-id="65b6e-108">Remarks</span></span>

<span data-ttu-id="65b6e-109">Les commentaires peuvent apparaître n’importe où, à l’exception du contenu de l’élément (entre les balises d’ouverture et de fermeture d’élément,  < >).</span><span class="sxs-lookup"><span data-stu-id="65b6e-109">Comments can appear anywhere except within element content (between element open and close tags, < >).</span></span> <span data-ttu-id="65b6e-110">Elles ne font pas partie des données caractères du document et sont ignorées lorsque le métafichier est analysé.</span><span class="sxs-lookup"><span data-stu-id="65b6e-110">They are not part of the document's character data and are ignored when the metafile is parsed.</span></span>

## <a name="examples"></a><span data-ttu-id="65b6e-111">Exemples</span><span class="sxs-lookup"><span data-stu-id="65b6e-111">Examples</span></span>


```XML
<ASX version = "3.0">
<!-- This information is only visible when editing a metafile file. -->
<!--<BANNER HREF="c:\wmsdk\wmssdk\samples\dhtml\asfbutton3.gif">
    </BANNER>-->
    <ENTRY>
        <REF HREF = "mms://proseware.com/pubpt/filename.asf" />
    </ENTRY>

    <ENTRY>
        <TITLE>WMA Port na Pucai</TITLE>
        <!--<DURATION VALUE="00:00:15"/>-->
        <REF href="c:\asfroot\Port na Pucai.wma"/>
    </ENTRY></ASX>

```



## <a name="requirements"></a><span data-ttu-id="65b6e-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="65b6e-112">Requirements</span></span>



| <span data-ttu-id="65b6e-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="65b6e-113">Requirement</span></span> | <span data-ttu-id="65b6e-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="65b6e-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="65b6e-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="65b6e-115">Header</span></span><br/> | <dl> <span data-ttu-id="65b6e-116"><dt>Msfeeds. h</dt></span><span class="sxs-lookup"><span data-stu-id="65b6e-116"><dt>Msfeeds.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65b6e-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="65b6e-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65b6e-118">**Informations de référence sur les éléments de métafichier Windows Media**</span><span class="sxs-lookup"><span data-stu-id="65b6e-118">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> </dl>

 

 





