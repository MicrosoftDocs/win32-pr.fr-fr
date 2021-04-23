---
description: Lorsque le filtre de navigateur DVD passe en mode karaoké, il informe le décodeur audio via la propriété AM \_ \_ DVDKARAOKE \_ Enable Property.
ms.assetid: 78b2998b-d8b3-424d-85bc-872e64eb4a4f
title: Jeu de propriétés Karaoké DVD (dvdmedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2918513de06a657436ed99e67f672fe74a113b78
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909067"
---
# <a name="dvd-karaoke-property-set"></a><span data-ttu-id="aa132-103">Jeu de propriétés Karaoké DVD</span><span class="sxs-lookup"><span data-stu-id="aa132-103">DVD Karaoke Property Set</span></span>

<span data-ttu-id="aa132-104">Lorsque le filtre de [navigateur DVD](dvd-navigator-filter.md) passe en mode karaoké, il informe le décodeur audio via la propriété **am \_ \_ DVDKARAOKE \_ Enable** Property.</span><span class="sxs-lookup"><span data-stu-id="aa132-104">When the [DVD Navigator](dvd-navigator-filter.md) filter goes into karaoke mode, it informs the audio decoder through the **AM\_PROPERTY\_DVDKARAOKE\_ENABLE** property.</span></span> <span data-ttu-id="aa132-105">Le décodeur doit ensuite désactiver les canaux audio de 2 à 5 jusqu’à ce qu’il reçoive du navigateur DVD une propriété de **\_ \_ \_ données DVDKARAOKE de la propriété am** avec un pointeur vers une structure de données [**am \_ DvdKaraokeData**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdkaraokedata) indiquant comment les canaux auxiliaires doivent être mélangés.</span><span class="sxs-lookup"><span data-stu-id="aa132-105">The decoder should then mute audio channels 2 through 5 until it receives from the DVD Navigator an **AM\_PROPERTY\_DVDKARAOKE\_DATA** property with a pointer to an [**AM\_DvdKaraokeData**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdkaraokedata) data structure indicating how the auxiliary channels are to be mixed.</span></span>



| <span data-ttu-id="aa132-106">Étiquette</span><span class="sxs-lookup"><span data-stu-id="aa132-106">Label</span></span> | <span data-ttu-id="aa132-107">Valeur</span><span class="sxs-lookup"><span data-stu-id="aa132-107">Value</span></span> |
|-------------------|-----------------------------|
| <span data-ttu-id="aa132-108">GUID de jeu de propriétés</span><span class="sxs-lookup"><span data-stu-id="aa132-108">Property Set GUID</span></span> | <span data-ttu-id="aa132-109">AM \_ KSPROPSETID \_ DvdKaraoke</span><span class="sxs-lookup"><span data-stu-id="aa132-109">AM\_KSPROPSETID\_DvdKaraoke</span></span> |



 



| <span data-ttu-id="aa132-110">ID de propriété</span><span class="sxs-lookup"><span data-stu-id="aa132-110">Property ID</span></span>                      | <span data-ttu-id="aa132-111">Description</span><span class="sxs-lookup"><span data-stu-id="aa132-111">Description</span></span>                                                                                                                                                                                                                                                                                                 |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa132-112">AM, \_ propriété \_ DVDKARAOKE \_ activer</span><span class="sxs-lookup"><span data-stu-id="aa132-112">AM\_PROPERTY\_DVDKARAOKE\_ENABLE</span></span> | <span data-ttu-id="aa132-113">Valeur BOOLÉENNE.</span><span class="sxs-lookup"><span data-stu-id="aa132-113">BOOLEAN value.</span></span> <span data-ttu-id="aa132-114">Le navigateur DVD envoie au décodeur une \_ propriété am \_ DVDKARAOKE \_ Enable avec la valeur **true** pour activer karaoké downmixing ou **false** pour le désactiver.</span><span class="sxs-lookup"><span data-stu-id="aa132-114">The DVD Navigator sends the decoder an AM\_PROPERTY\_DVDKARAOKE\_ENABLE with a value of **TRUE** to enable karaoke downmixing or **FALSE** to disable it.</span></span>                                                                                                                                    |
| <span data-ttu-id="aa132-115">AM, \_ propriété \_ DVDKARAOKE \_ données</span><span class="sxs-lookup"><span data-stu-id="aa132-115">AM\_PROPERTY\_DVDKARAOKE\_DATA</span></span>   | <span data-ttu-id="aa132-116">Le navigateur DVD envoie au décodeur une propriété \_ de \_ données DVDKARAOKE de propriété am \_ avec un pointeur vers une structure [**am \_ DvdKaraokeData**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdkaraokedata) pour modifier la configuration downmix ; autrement dit, pour activer ou désactiver certains canaux karaoké et les diriger vers le canal de sortie de droite ou de gauche.</span><span class="sxs-lookup"><span data-stu-id="aa132-116">The DVD Navigator sends the decoder an AM\_PROPERTY\_DVDKARAOKE\_DATA property with a pointer to an [**AM\_DvdKaraokeData**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdkaraokedata) structure to change the downmix configuration; that is, to turn certain karaoke channels on or off and direct them to the right or left output channel.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="aa132-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aa132-117">Requirements</span></span>



| <span data-ttu-id="aa132-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="aa132-118">Requirement</span></span> | <span data-ttu-id="aa132-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="aa132-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="aa132-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="aa132-120">Header</span></span><br/> | <dl> <span data-ttu-id="aa132-121"><dt>Dvdmedia. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa132-121"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa132-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aa132-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa132-123">Jeux de propriétés</span><span class="sxs-lookup"><span data-stu-id="aa132-123">Property Sets</span></span>](property-sets.md)
</dt> </dl>

 

 




