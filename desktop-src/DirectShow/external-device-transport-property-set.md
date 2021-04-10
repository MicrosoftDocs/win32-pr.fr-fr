---
description: Ensemble de propriétés de transport d’appareil externe
ms.assetid: 9c80cf59-054f-49b6-9456-ed5e091cbfaf
title: Ensemble de propriétés de transport d’appareil externe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e77942157b7cf5f75b883e6953f3a115d1fa9f6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109902"
---
# <a name="external-device-transport-property-set"></a><span data-ttu-id="408ef-103">Ensemble de propriétés de transport d’appareil externe</span><span class="sxs-lookup"><span data-stu-id="408ef-103">External Device Transport Property Set</span></span>

<span data-ttu-id="408ef-104">Ce jeu de propriétés contrôle le transport des données vers et à partir d’un périphérique externe.</span><span class="sxs-lookup"><span data-stu-id="408ef-104">This property set controls the transport of data to and from an external device.</span></span> <span data-ttu-id="408ef-105">Dans la plupart des cas, les applications ne doivent pas utiliser cette propriété directement définie.</span><span class="sxs-lookup"><span data-stu-id="408ef-105">In most cases, applications should not use this property set directly.</span></span> <span data-ttu-id="408ef-106">Utilisez plutôt l’interface [**IAMExtTransport**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport) .</span><span class="sxs-lookup"><span data-stu-id="408ef-106">Use the [**IAMExtTransport**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport) interface instead.</span></span>

<span data-ttu-id="408ef-107">Le tableau suivant répertorie les propriétés qui sont pertinentes pour les applications en mode utilisateur.</span><span class="sxs-lookup"><span data-stu-id="408ef-107">The following table lists the properties that are relevant to user-mode applications.</span></span> <span data-ttu-id="408ef-108">Pour obtenir une description complète de ce jeu de propriétés, reportez-vous au kit de développement de pilotes Microsoft Windows Driver kit DDK.</span><span class="sxs-lookup"><span data-stu-id="408ef-108">For a complete description of this property set, refer to the Microsoft Windows Driver Development Kit DDK.</span></span>



|                   |                           |
|-------------------|---------------------------|
| <span data-ttu-id="408ef-109">GUID de jeu de propriétés</span><span class="sxs-lookup"><span data-stu-id="408ef-109">Property Set GUID</span></span> | <span data-ttu-id="408ef-110">\_transport PROPSETID ext \_</span><span class="sxs-lookup"><span data-stu-id="408ef-110">PROPSETID\_EXT\_TRANSPORT</span></span> |



 



| <span data-ttu-id="408ef-111">ID de propriété</span><span class="sxs-lookup"><span data-stu-id="408ef-111">Property ID</span></span>                                                                           | <span data-ttu-id="408ef-112">Description</span><span class="sxs-lookup"><span data-stu-id="408ef-112">Description</span></span>                                  |
|---------------------------------------------------------------------------------------|----------------------------------------------|
| [<span data-ttu-id="408ef-113">**\_recherche KSPROPERTY EXTXPORT \_ ATN \_**</span><span class="sxs-lookup"><span data-stu-id="408ef-113">**KSPROPERTY\_EXTXPORT\_ATN\_SEARCH**</span></span>](ksproperty-extxport-atn-search.md)           | <span data-ttu-id="408ef-114">Recherche un numéro de piste absolu (ATN).</span><span class="sxs-lookup"><span data-stu-id="408ef-114">Searches for an absolute track number (ATN).</span></span> |
| [<span data-ttu-id="408ef-115">**\_recherche de \_ code temporel KSPROPERTY EXTXPORT \_**</span><span class="sxs-lookup"><span data-stu-id="408ef-115">**KSPROPERTY\_EXTXPORT\_TIMECODE\_SEARCH**</span></span>](ksproperty-extxport-timecode-search.md) | <span data-ttu-id="408ef-116">Recherche un code d’heure.</span><span class="sxs-lookup"><span data-stu-id="408ef-116">Searches for a time code.</span></span>                    |



 

## <a name="related-topics"></a><span data-ttu-id="408ef-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="408ef-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="408ef-118">Jeux de propriétés</span><span class="sxs-lookup"><span data-stu-id="408ef-118">Property Sets</span></span>](property-sets.md)
</dt> </dl>

 

 



