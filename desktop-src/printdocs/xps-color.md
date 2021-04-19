---
description: Structure qui décrit une seule valeur de couleur.
ms.assetid: 710f3ef1-bbc3-416d-9faf-aa4a716007c2
title: XPS_COLOR (Xpsobjectmodel. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34c148c2a5452154bfe33b0c74d695fe78f0cdad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521928"
---
# <a name="xps_color"></a><span data-ttu-id="912e3-103">\_couleur XPS</span><span class="sxs-lookup"><span data-stu-id="912e3-103">XPS\_COLOR</span></span>

<span data-ttu-id="912e3-104">Structure qui décrit une seule valeur de couleur.</span><span class="sxs-lookup"><span data-stu-id="912e3-104">A structure that describes a single color value.</span></span>

``` syntax
typedef union switch (XPS_COLOR_TYPE colorType) value
{
    case XPS_COLOR_TYPE_SRGB:
        struct {
            byte alpha, red, green, blue;
        } sRGB;
    case XPS_COLOR_TYPE_SCRGB:
        struct {
            FLOAT alpha, red, green, blue;
        } scRGB;
    case XPS_COLOR_TYPE_CONTEXT:
        struct {
            byte channelCount;
            FLOAT channels[9];
        } context;
} XPS_COLOR;
```

## <a name="remarks"></a><span data-ttu-id="912e3-105">Notes</span><span class="sxs-lookup"><span data-stu-id="912e3-105">Remarks</span></span>

<span data-ttu-id="912e3-106">Le format de la structure dépend de la valeur de *colorType*.</span><span class="sxs-lookup"><span data-stu-id="912e3-106">The structure's format depends on the value of *colorType*.</span></span>

<dl>

<span data-ttu-id="912e3-107">[**\_type de couleur XPS \_ \_ sRVB**](/previous-versions/windows/desktop/dd372944(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="912e3-107">[**XPS\_COLOR\_TYPE\_SRGB**](/previous-versions/windows/desktop/dd372944(v=vs.85))</span></span>  
<span data-ttu-id="912e3-108">[**\_type de couleur XPS \_ \_ ScRVB**](/previous-versions/windows/desktop/dd372943(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="912e3-108">[**XPS\_COLOR\_TYPE\_SCRGB**](/previous-versions/windows/desktop/dd372943(v=vs.85))</span></span>  
[<span data-ttu-id="912e3-109">**\_contexte du \_ type de couleur XPS \_**</span><span class="sxs-lookup"><span data-stu-id="912e3-109">**XPS\_COLOR\_TYPE\_CONTEXT**</span></span>](/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_color)  
</dl>

## <a name="requirements"></a><span data-ttu-id="912e3-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="912e3-110">Requirements</span></span>



| <span data-ttu-id="912e3-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="912e3-111">Requirement</span></span> | <span data-ttu-id="912e3-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="912e3-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="912e3-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="912e3-113">Minimum supported client</span></span><br/> | <span data-ttu-id="912e3-114">Windows 7, Windows Vista avec SP2 et mise à jour de la plateforme pour les applications de bureau Windows Vista, applications \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="912e3-114">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="912e3-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="912e3-115">Minimum supported server</span></span><br/> | <span data-ttu-id="912e3-116">Windows Server 2008 R2, Windows Server 2008 avec SP2 et mise à jour de la plateforme pour les applications de bureau Windows Server 2008 pour applications \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="912e3-116">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="912e3-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="912e3-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="912e3-118"><dt>Xpsobjectmodel. h</dt></span><span class="sxs-lookup"><span data-stu-id="912e3-118"><dt>Xpsobjectmodel.h</dt></span></span> </dl>                                              |
| <span data-ttu-id="912e3-119">MIDL</span><span class="sxs-lookup"><span data-stu-id="912e3-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="912e3-120"><dt>XpsObjectModel. idl</dt></span><span class="sxs-lookup"><span data-stu-id="912e3-120"><dt>XpsObjectModel.idl</dt></span></span> </dl>                                            |



## <a name="see-also"></a><span data-ttu-id="912e3-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="912e3-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="912e3-122">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="912e3-122">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

