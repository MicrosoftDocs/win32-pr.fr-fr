---
title: DRM_Rights
description: La \_ propriété droits DRM spécifie les droits requis par l’application lors de la prochaine tentative d’ouverture d’un fichier protégé.
ms.assetid: fbf62e8d-069e-427b-9093-6c579cdaa96a
keywords:
- Format Windows Media DRM_Rights
topic_type:
- apiref
api_name:
- DRM_Rights
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 542e511c11111bb2698d9c936a1f0973a2145c9b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104030784"
---
# <a name="drm_rights"></a><span data-ttu-id="cf6f7-104">\_Droits DRM</span><span class="sxs-lookup"><span data-stu-id="cf6f7-104">DRM\_Rights</span></span>

<span data-ttu-id="cf6f7-105">La **propriété \_ droits DRM** spécifie les droits requis par l’application lors de la prochaine tentative d’ouverture d’un fichier protégé.</span><span class="sxs-lookup"><span data-stu-id="cf6f7-105">The **DRM\_Rights** property specifies the rights that the application will require in the next attempt to open a protected file.</span></span>

## <a name="global-constant"></a><span data-ttu-id="cf6f7-106">Constante globale</span><span class="sxs-lookup"><span data-stu-id="cf6f7-106">Global Constant</span></span>

<span data-ttu-id="cf6f7-107">\_droits wszWMDRM \_ g</span><span class="sxs-lookup"><span data-stu-id="cf6f7-107">g\_wszWMDRM\_Rights</span></span>

## <a name="data-type"></a><span data-ttu-id="cf6f7-108">Type de données</span><span class="sxs-lookup"><span data-stu-id="cf6f7-108">Data Type</span></span>

<span data-ttu-id="cf6f7-109">**\_chaîne de type WMT \_**</span><span class="sxs-lookup"><span data-stu-id="cf6f7-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="cf6f7-110">Notes</span><span class="sxs-lookup"><span data-stu-id="cf6f7-110">Remarks</span></span>

<span data-ttu-id="cf6f7-111">Il s’agit d’une propriété en lecture-écriture qui est récupérée à l’aide de [**IWMDRMReader :: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty) et définie à l’aide de [**IWMDRMReader :: SetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-setdrmproperty) ou [**IWMDRMWriter :: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute).</span><span class="sxs-lookup"><span data-stu-id="cf6f7-111">This is a read-write property that is retrieved using [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty) and set using either [**IWMDRMReader::SetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-setdrmproperty) or [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute).</span></span>

<span data-ttu-id="cf6f7-112">Le tableau suivant répertorie les droits pris en charge.</span><span class="sxs-lookup"><span data-stu-id="cf6f7-112">The following table lists the supported rights.</span></span>



| <span data-ttu-id="cf6f7-113">Right</span><span class="sxs-lookup"><span data-stu-id="cf6f7-113">Right</span></span>                                           | <span data-ttu-id="cf6f7-114">Littéral de chaîne</span><span class="sxs-lookup"><span data-stu-id="cf6f7-114">String literal</span></span>      | <span data-ttu-id="cf6f7-115">Description</span><span class="sxs-lookup"><span data-stu-id="cf6f7-115">Description</span></span>                                                                                                                                                                                                          |
|-------------------------------------------------|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf6f7-116">\_wszWMDRM la \_ sauvegarde à droite g \_</span><span class="sxs-lookup"><span data-stu-id="cf6f7-116">g\_wszWMDRM\_RIGHT\_BACKUP</span></span>                      | <span data-ttu-id="cf6f7-117">« Backup »</span><span class="sxs-lookup"><span data-stu-id="cf6f7-117">"Backup"</span></span>            | <span data-ttu-id="cf6f7-118">Droit de sauvegarder la licence.</span><span class="sxs-lookup"><span data-stu-id="cf6f7-118">Right to back up the license.</span></span>                                                                                                                                                                                        |
| <span data-ttu-id="cf6f7-119">wszWMDRM de la \_ \_ bonne \_ \_ lecture collaborative</span><span class="sxs-lookup"><span data-stu-id="cf6f7-119">g\_wszWMDRM\_RIGHT\_COLLABORATIVE\_PLAY</span></span>         | <span data-ttu-id="cf6f7-120">"CollaborativePlay"</span><span class="sxs-lookup"><span data-stu-id="cf6f7-120">"CollaborativePlay"</span></span> | <span data-ttu-id="cf6f7-121">Droit de lire le fichier dans le cadre d’une sélection collaborative.</span><span class="sxs-lookup"><span data-stu-id="cf6f7-121">Right to play the file as part of a collaborative playlist.</span></span>                                                                                                                                                          |
| <span data-ttu-id="cf6f7-122">\_wszWMDRM g \_ droit de \_ copie</span><span class="sxs-lookup"><span data-stu-id="cf6f7-122">g\_wszWMDRM\_RIGHT\_COPY</span></span>                        | <span data-ttu-id="cf6f7-123">"Copy"</span><span class="sxs-lookup"><span data-stu-id="cf6f7-123">"Copy"</span></span>              | <span data-ttu-id="cf6f7-124">Droit de copier le fichier sur un appareil.</span><span class="sxs-lookup"><span data-stu-id="cf6f7-124">Right to copy the file to a device.</span></span> <span data-ttu-id="cf6f7-125">Ce droit remplace les droits de copie plus anciens (g \_ wszWMDRM \_ droit Copy \_ \_ sur \_ CD, g \_ wszWMDRM \_ Right \_ Copy \_ to \_ non \_ SDMI \_ Device et g \_ wszWMDRM \_ Right \_ Copy \_ to \_ SDMI \_ Device).</span><span class="sxs-lookup"><span data-stu-id="cf6f7-125">This right supersedes the older copy rights (g\_wszWMDRM\_RIGHT\_COPY\_TO\_CD, g\_wszWMDRM\_RIGHT\_COPY\_TO\_NON\_SDMI\_DEVICE, and g\_wszWMDRM\_RIGHT\_COPY\_TO\_SDMI\_DEVICE).</span></span> |
| <span data-ttu-id="cf6f7-126">\_wszWMDRM g \_ droit \_ \_ de copie sur le \_ CD</span><span class="sxs-lookup"><span data-stu-id="cf6f7-126">g\_wszWMDRM\_RIGHT\_COPY\_TO\_CD</span></span>                | <span data-ttu-id="cf6f7-127">« Print. Redbook »</span><span class="sxs-lookup"><span data-stu-id="cf6f7-127">"Print.redbook"</span></span>     | <span data-ttu-id="cf6f7-128">Droit de copier le fichier sur un CD (format de livre rouge). Dans Windows Media DRM 10, ce droit est remplacé par g \_ wszWMDRM \_ Right \_ Copy.</span><span class="sxs-lookup"><span data-stu-id="cf6f7-128">Right to copy the file to a CD (Red Book format).In Windows Media DRM 10, this right is replaced by g\_wszWMDRM\_RIGHT\_COPY.</span></span><br/>                                                                             |
| <span data-ttu-id="cf6f7-129">g \_ wszWMDRM \_ droit \_ \_ de copie sur un \_ \_ appareil non SDMI \_</span><span class="sxs-lookup"><span data-stu-id="cf6f7-129">g\_wszWMDRM\_RIGHT\_COPY\_TO\_NON\_SDMI\_DEVICE</span></span> | <span data-ttu-id="cf6f7-130">« Transfer. NONSDMI »</span><span class="sxs-lookup"><span data-stu-id="cf6f7-130">"Transfer.NONSDMI"</span></span>  | <span data-ttu-id="cf6f7-131">Droit de copier le fichier sur un appareil non-SDMI. Dans Windows Media DRM 10, ce droit est remplacé par g \_ wszWMDRM \_ Right \_ Copy.</span><span class="sxs-lookup"><span data-stu-id="cf6f7-131">Right to copy the file to a non-SDMI device.In Windows Media DRM 10, this right is replaced by g\_wszWMDRM\_RIGHT\_COPY.</span></span><br/>                                                                                  |
| <span data-ttu-id="cf6f7-132">g \_ wszWMDRM \_ droit \_ \_ de copie sur l' \_ \_ appareil SDMI</span><span class="sxs-lookup"><span data-stu-id="cf6f7-132">g\_wszWMDRM\_RIGHT\_COPY\_TO\_SDMI\_DEVICE</span></span>      | <span data-ttu-id="cf6f7-133">« Transfer. SDMI »</span><span class="sxs-lookup"><span data-stu-id="cf6f7-133">"Transfer.SDMI"</span></span>     | <span data-ttu-id="cf6f7-134">Droit de copier le fichier sur un appareil compatible SDMI. Dans Windows Media DRM 10, ce droit est remplacé par g \_ wszWMDRM \_ Right \_ Copy.</span><span class="sxs-lookup"><span data-stu-id="cf6f7-134">Right to copy the file to an SDMI-compliant device.In Windows Media DRM 10, this right is replaced by g\_wszWMDRM\_RIGHT\_COPY.</span></span><br/>                                                                           |
| <span data-ttu-id="cf6f7-135">\_ \_ lecture droite g \_ wszWMDRM</span><span class="sxs-lookup"><span data-stu-id="cf6f7-135">g\_wszWMDRM\_RIGHT\_PLAYBACK</span></span>                    | <span data-ttu-id="cf6f7-136">Répétition</span><span class="sxs-lookup"><span data-stu-id="cf6f7-136">"Play"</span></span>              | <span data-ttu-id="cf6f7-137">Droit de lire le fichier multimédia.</span><span class="sxs-lookup"><span data-stu-id="cf6f7-137">Right to play the media file.</span></span>                                                                                                                                                                                        |



 

<span data-ttu-id="cf6f7-138">Cette propriété contient une chaîne de caractères larges d’un ou plusieurs droits séparés par des points-virgules, par exemple : L "lecture ; Reprographie CollaborativePlay".</span><span class="sxs-lookup"><span data-stu-id="cf6f7-138">This property contains a wide-character string of one or more rights separated by semicolons, for example: L"Playback;Copy;CollaborativePlay".</span></span>

## <a name="see-also"></a><span data-ttu-id="cf6f7-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cf6f7-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf6f7-140">**Propriétés DRM**</span><span class="sxs-lookup"><span data-stu-id="cf6f7-140">**DRM Properties**</span></span>](drm-properties.md)
</dt> </dl>

 

 





