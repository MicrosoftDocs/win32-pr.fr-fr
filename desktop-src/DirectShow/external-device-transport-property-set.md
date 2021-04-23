---
description: Ensemble de propriétés de transport d’appareil externe
ms.assetid: 9c80cf59-054f-49b6-9456-ed5e091cbfaf
title: Ensemble de propriétés de transport d’appareil externe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85e38217af21ea1839d7c9207a4922bcff00d63a
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909217"
---
# <a name="external-device-transport-property-set"></a><span data-ttu-id="dffd0-103">Ensemble de propriétés de transport d’appareil externe</span><span class="sxs-lookup"><span data-stu-id="dffd0-103">External Device Transport Property Set</span></span>

<span data-ttu-id="dffd0-104">Ce jeu de propriétés contrôle le transport des données vers et à partir d’un périphérique externe.</span><span class="sxs-lookup"><span data-stu-id="dffd0-104">This property set controls the transport of data to and from an external device.</span></span> <span data-ttu-id="dffd0-105">Dans la plupart des cas, les applications ne doivent pas utiliser cette propriété directement définie.</span><span class="sxs-lookup"><span data-stu-id="dffd0-105">In most cases, applications should not use this property set directly.</span></span> <span data-ttu-id="dffd0-106">Utilisez plutôt l’interface [**IAMExtTransport**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport) .</span><span class="sxs-lookup"><span data-stu-id="dffd0-106">Use the [**IAMExtTransport**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport) interface instead.</span></span>

<span data-ttu-id="dffd0-107">Le tableau suivant répertorie les propriétés qui sont pertinentes pour les applications en mode utilisateur.</span><span class="sxs-lookup"><span data-stu-id="dffd0-107">The following table lists the properties that are relevant to user-mode applications.</span></span> <span data-ttu-id="dffd0-108">Pour obtenir une description complète de ce jeu de propriétés, reportez-vous au kit de développement de pilotes Microsoft Windows Driver kit DDK.</span><span class="sxs-lookup"><span data-stu-id="dffd0-108">For a complete description of this property set, refer to the Microsoft Windows Driver Development Kit DDK.</span></span>



| <span data-ttu-id="dffd0-109">Étiquette</span><span class="sxs-lookup"><span data-stu-id="dffd0-109">Label</span></span> | <span data-ttu-id="dffd0-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="dffd0-110">Value</span></span> |
|-------------------|---------------------------|
| <span data-ttu-id="dffd0-111">GUID de jeu de propriétés</span><span class="sxs-lookup"><span data-stu-id="dffd0-111">Property Set GUID</span></span> | <span data-ttu-id="dffd0-112">\_transport PROPSETID ext \_</span><span class="sxs-lookup"><span data-stu-id="dffd0-112">PROPSETID\_EXT\_TRANSPORT</span></span> |



 



| <span data-ttu-id="dffd0-113">ID de propriété</span><span class="sxs-lookup"><span data-stu-id="dffd0-113">Property ID</span></span>                                                                           | <span data-ttu-id="dffd0-114">Description</span><span class="sxs-lookup"><span data-stu-id="dffd0-114">Description</span></span>                                  |
|---------------------------------------------------------------------------------------|----------------------------------------------|
| [<span data-ttu-id="dffd0-115">**\_recherche KSPROPERTY EXTXPORT \_ ATN \_**</span><span class="sxs-lookup"><span data-stu-id="dffd0-115">**KSPROPERTY\_EXTXPORT\_ATN\_SEARCH**</span></span>](ksproperty-extxport-atn-search.md)           | <span data-ttu-id="dffd0-116">Recherche un numéro de piste absolu (ATN).</span><span class="sxs-lookup"><span data-stu-id="dffd0-116">Searches for an absolute track number (ATN).</span></span> |
| [<span data-ttu-id="dffd0-117">**\_recherche de \_ code temporel KSPROPERTY EXTXPORT \_**</span><span class="sxs-lookup"><span data-stu-id="dffd0-117">**KSPROPERTY\_EXTXPORT\_TIMECODE\_SEARCH**</span></span>](ksproperty-extxport-timecode-search.md) | <span data-ttu-id="dffd0-118">Recherche un code d’heure.</span><span class="sxs-lookup"><span data-stu-id="dffd0-118">Searches for a time code.</span></span>                    |



 

## <a name="related-topics"></a><span data-ttu-id="dffd0-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="dffd0-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dffd0-120">Jeux de propriétés</span><span class="sxs-lookup"><span data-stu-id="dffd0-120">Property Sets</span></span>](property-sets.md)
</dt> </dl>

 

 



