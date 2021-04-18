---
title: Attribut DTCPIPPort
description: L’attribut DTCPIPPort est le numéro de port TCP (Transmission Control Protocol) de l’ordinateur ou du périphérique qui doit être contacté pour la transmission numérique protection du contenu via l’échange de clés authentifiées DTCP-IP (ACÉ) pour l’élément multimédia.
ms.assetid: 63767ec1-dd01-40c2-bf9a-6e9b8a7db7f8
keywords:
- Attribut DTCPIPPort lecteur Windows Media
topic_type:
- apiref
api_name:
- DTCPIPPort Attribute
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16c1c6117425211c0015d218412c8a9ac0971d7b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540719"
---
# <a name="dtcpipport-attribute"></a><span data-ttu-id="559aa-104">Attribut DTCPIPPort</span><span class="sxs-lookup"><span data-stu-id="559aa-104">DTCPIPPort Attribute</span></span>

<span data-ttu-id="559aa-105">L’attribut **DTCPIPPort** est le numéro de port TCP (Transmission Control Protocol) de l’ordinateur ou du périphérique qui doit être contacté pour la Transmission numérique protection du contenu via l’échange de clés authentifiées DTCP-IP (ACÉ) pour l’élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="559aa-105">The **DTCPIPPort** attribute is the Transmission Control Protocol (TCP) port number of the computer or device that must be contacted for the Digital Transmission Content Protection over Internet Protocol (DTCP-IP) Authenticated Key Exchange (AKE) for the media item.</span></span>

## <a name="applies-to"></a><span data-ttu-id="559aa-106">S'applique à</span><span class="sxs-lookup"><span data-stu-id="559aa-106">Applies To</span></span>

-   [<span data-ttu-id="559aa-107">**Éléments audio**</span><span class="sxs-lookup"><span data-stu-id="559aa-107">**Audio Items**</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="559aa-108">**Éléments de photo**</span><span class="sxs-lookup"><span data-stu-id="559aa-108">**Photo Items**</span></span>](photo-item-attributes.md)
-   [<span data-ttu-id="559aa-109">**Éléments de sélection**</span><span class="sxs-lookup"><span data-stu-id="559aa-109">**Playlist Items**</span></span>](playlist-attributes-ref.md)
-   [<span data-ttu-id="559aa-110">**Éléments vidéo**</span><span class="sxs-lookup"><span data-stu-id="559aa-110">**Video Items**</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="559aa-111">Notes</span><span class="sxs-lookup"><span data-stu-id="559aa-111">Remarks</span></span>

<span data-ttu-id="559aa-112">Si cet attribut est disponible, l’élément multimédia est protégé à l’aide de DTCP-IP.</span><span class="sxs-lookup"><span data-stu-id="559aa-112">If this attribute is available, the media item is protected using DTCP-IP.</span></span>

<span data-ttu-id="559aa-113">Cet attribut n’est pas disponible pour les éléments multimédias dans la bibliothèque locale de l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="559aa-113">This attribute is not available for media items in the current user's local library.</span></span> <span data-ttu-id="559aa-114">Elle est disponible uniquement pour les éléments multimédias appartenant à une bibliothèque distante ; autrement dit, une bibliothèque qui a été mise à la disposition d’un autre utilisateur sur le réseau privé.</span><span class="sxs-lookup"><span data-stu-id="559aa-114">It is available only for media items that belong to a remote library; that is, a library that has been made available by another user on the home network.</span></span> <span data-ttu-id="559aa-115">Pour déterminer si une bibliothèque multimédia est distante, appelez [**IWMPLibrary :: obtenir le \_ type**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type).</span><span class="sxs-lookup"><span data-stu-id="559aa-115">To determine whether a media library is remote, call [**IWMPLibrary::get\_type**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type).</span></span>

## <a name="requirements"></a><span data-ttu-id="559aa-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="559aa-116">Requirements</span></span>



| <span data-ttu-id="559aa-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="559aa-117">Requirement</span></span> | <span data-ttu-id="559aa-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="559aa-118">Value</span></span> |
|--------------------|------------------------------------|
| <span data-ttu-id="559aa-119">Version</span><span class="sxs-lookup"><span data-stu-id="559aa-119">Version</span></span><br/> | <span data-ttu-id="559aa-120">Lecteur Windows Media 12</span><span class="sxs-lookup"><span data-stu-id="559aa-120">Windows Media Player 12</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="559aa-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="559aa-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="559aa-122">**Référence d’attribut**</span><span class="sxs-lookup"><span data-stu-id="559aa-122">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





