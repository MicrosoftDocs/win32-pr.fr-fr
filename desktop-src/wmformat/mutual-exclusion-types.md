---
title: Types d’exclusion mutuelle
description: Types d’exclusion mutuelle
ms.assetid: bfe6cfe6-3df4-49c4-8015-fe4479b693c1
keywords:
- Windows Media Format SDK, exclusion mutuelle
- ASF (Advanced Systems Format), exclusion mutuelle
- ASF (format des systèmes avancés), exclusion mutuelle
- exclusion mutuelle, types
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c425e69c2aa3eac012874837a6970dbc26d1a51
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104030764"
---
# <a name="mutual-exclusion-types"></a><span data-ttu-id="7b3cf-107">Types d’exclusion mutuelle</span><span class="sxs-lookup"><span data-stu-id="7b3cf-107">Mutual Exclusion Types</span></span>

<span data-ttu-id="7b3cf-108">Vous pouvez utiliser des types d’exclusion mutuelle pour identifier la nature d’un objet d’exclusion mutuelle dans un profil.</span><span class="sxs-lookup"><span data-stu-id="7b3cf-108">You can use mutual exclusion types to identify the nature of a mutual exclusion object in a profile.</span></span> <span data-ttu-id="7b3cf-109">Les types d’exclusion mutuelle sont utilisés comme paramètres pour [**IWMMutualExclusion :: GetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-gettype) et [**IWMMutualExclusion :: setType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype).</span><span class="sxs-lookup"><span data-stu-id="7b3cf-109">Mutual exclusion types are used as parameters for [**IWMMutualExclusion::GetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-gettype) and [**IWMMutualExclusion::SetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype).</span></span>

<span data-ttu-id="7b3cf-110">Le tableau suivant répertorie les identificateurs pour les types d’exclusion mutuelle.</span><span class="sxs-lookup"><span data-stu-id="7b3cf-110">The following table lists the identifiers for mutual exclusion types.</span></span>



| <span data-ttu-id="7b3cf-111">Constante de type d’exclusion mutuelle</span><span class="sxs-lookup"><span data-stu-id="7b3cf-111">Mutual exclusion type constant</span></span> | <span data-ttu-id="7b3cf-112">GUID</span><span class="sxs-lookup"><span data-stu-id="7b3cf-112">GUID</span></span>                                 |
|--------------------------------|--------------------------------------|
| <span data-ttu-id="7b3cf-113">\_Langue WMMUTEX \_ CLSID</span><span class="sxs-lookup"><span data-stu-id="7b3cf-113">CLSID\_WMMUTEX\_Language</span></span>       | <span data-ttu-id="7b3cf-114">D6E22A00-35DA-11D1-9034-00A0C90349BE</span><span class="sxs-lookup"><span data-stu-id="7b3cf-114">D6E22A00-35DA-11D1-9034-00A0C90349BE</span></span> |
| <span data-ttu-id="7b3cf-115">\_Débit binaire WMMUTEX du CLSID \_</span><span class="sxs-lookup"><span data-stu-id="7b3cf-115">CLSID\_WMMUTEX\_Bitrate</span></span>        | <span data-ttu-id="7b3cf-116">D6E22A01-35DA-11D1-9034-00A0C90349BE</span><span class="sxs-lookup"><span data-stu-id="7b3cf-116">D6E22A01-35DA-11D1-9034-00A0C90349BE</span></span> |
| <span data-ttu-id="7b3cf-117">Présentation du CLSID \_ WMMUTEX \_</span><span class="sxs-lookup"><span data-stu-id="7b3cf-117">CLSID\_WMMUTEX\_Presentation</span></span>   | <span data-ttu-id="7b3cf-118">D6E22A02-35DA-11D1-9034-00A0C90349BE</span><span class="sxs-lookup"><span data-stu-id="7b3cf-118">D6E22A02-35DA-11D1-9034-00A0C90349BE</span></span> |
| <span data-ttu-id="7b3cf-119">CLSID \_ WMMUTEX \_ inconnu</span><span class="sxs-lookup"><span data-stu-id="7b3cf-119">CLSID\_WMMUTEX\_Unknown</span></span>        | <span data-ttu-id="7b3cf-120">D6E22A03-35DA-11D1-9034-00A0C90349BE</span><span class="sxs-lookup"><span data-stu-id="7b3cf-120">D6E22A03-35DA-11D1-9034-00A0C90349BE</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="7b3cf-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7b3cf-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b3cf-122">**Valeurs GUID**</span><span class="sxs-lookup"><span data-stu-id="7b3cf-122">**GUID Values**</span></span>](guid-values.md)
</dt> </dl>

 

 




