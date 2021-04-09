---
description: Un profil 802.1 X contient les éléments de schéma suivants.
ms.assetid: be3f1986-d0c2-47f6-b4dd-8defb89bd03a
title: Éléments de schéma OneX
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7b7f3e7bac256b915d0e134720fc63b3519b21e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756459"
---
# <a name="onex-schema-elements"></a><span data-ttu-id="44b37-103">Éléments de schéma OneX</span><span class="sxs-lookup"><span data-stu-id="44b37-103">OneX Schema Elements</span></span>

<span data-ttu-id="44b37-104">Un profil 802.1 X contient les éléments de schéma suivants.</span><span class="sxs-lookup"><span data-stu-id="44b37-104">An 802.1X profile contains the following schema elements.</span></span> <span data-ttu-id="44b37-105">Tous les éléments de schéma OneX s’appliquent aux profils filaires et sans fil.</span><span class="sxs-lookup"><span data-stu-id="44b37-105">All OneX schema elements apply to both wired and wireless profiles.</span></span> <span data-ttu-id="44b37-106">La plupart des éléments nommés se trouvent dans l’espace de noms `https://www.microsoft.com/networking/OneX/v1` , à l’exception de [**EAPConfig (Onex)**](onexschema-eapconfig-onex-element.md) qui se trouve dans l’espace de noms `https://www.microsoft.com/provisioning/EapHostConfig` .</span><span class="sxs-lookup"><span data-stu-id="44b37-106">Most of the named elements are in the namespace `https://www.microsoft.com/networking/OneX/v1`, except for [**EAPConfig (OneX)**](onexschema-eapconfig-onex-element.md) which is in the namespace `https://www.microsoft.com/provisioning/EapHostConfig`.</span></span>

<span data-ttu-id="44b37-107">La liste suivante présente les éléments définis dans l’ordre dans lequel les éléments apparaissent dans un profil.</span><span class="sxs-lookup"><span data-stu-id="44b37-107">The following list shows the defined elements in the order in which the elements appear in a profile.</span></span> <span data-ttu-id="44b37-108">L’ordre des éléments est appliqué.</span><span class="sxs-lookup"><span data-stu-id="44b37-108">The ordering of elements is enforced.</span></span> <span data-ttu-id="44b37-109">Tous les éléments ne se trouvent pas dans chaque profil, car certains éléments sont facultatifs.</span><span class="sxs-lookup"><span data-stu-id="44b37-109">Not all elements are in every profile, as some elements are optional.</span></span>

<span data-ttu-id="44b37-110">Cette liste n’affiche pas tous les éléments possibles qui peuvent apparaître dans un profil, car des éléments peuvent être ajoutés dans **XS : n’importe quel** point d’insertion.</span><span class="sxs-lookup"><span data-stu-id="44b37-110">This list does not show all possible elements that can appear in a profile, as elements can be added in **xs:any** insertion points.</span></span>

-   [<span data-ttu-id="44b37-111">**802.1x**</span><span class="sxs-lookup"><span data-stu-id="44b37-111">**OneX**</span></span>](onexschema-onex-element.md)
    -   [<span data-ttu-id="44b37-112">**cacheUserData (OneX)**</span><span class="sxs-lookup"><span data-stu-id="44b37-112">**cacheUserData (OneX)**</span></span>](onexschema-cacheuserdata-onex-element.md)
    -   [<span data-ttu-id="44b37-113">**heldPeriod (OneX)**</span><span class="sxs-lookup"><span data-stu-id="44b37-113">**heldPeriod (OneX)**</span></span>](onexschema-heldperiod-onex-element.md)
    -   [<span data-ttu-id="44b37-114">**authPeriod (OneX)**</span><span class="sxs-lookup"><span data-stu-id="44b37-114">**authPeriod (OneX)**</span></span>](onexschema-authperiod-onex-element.md)
    -   [<span data-ttu-id="44b37-115">**startPeriod (OneX)**</span><span class="sxs-lookup"><span data-stu-id="44b37-115">**startPeriod (OneX)**</span></span>](onexschema-startperiod-onex-element.md)
    -   [<span data-ttu-id="44b37-116">**maxStart (OneX)**</span><span class="sxs-lookup"><span data-stu-id="44b37-116">**maxStart (OneX)**</span></span>](onexschema-maxstart-onex-element.md)
    -   [<span data-ttu-id="44b37-117">**maxAuthFailures (OneX)**</span><span class="sxs-lookup"><span data-stu-id="44b37-117">**maxAuthFailures (OneX)**</span></span>](onexschema-maxauthfailures-onex-element.md)
    -   [<span data-ttu-id="44b37-118">**supplicantMode (OneX)**</span><span class="sxs-lookup"><span data-stu-id="44b37-118">**supplicantMode (OneX)**</span></span>](onexschema-supplicantmode-onex-element.md)
    -   [<span data-ttu-id="44b37-119">**authMode (OneX)**</span><span class="sxs-lookup"><span data-stu-id="44b37-119">**authMode (OneX)**</span></span>](onexschema-authmode-onex-element.md)
    -   [<span data-ttu-id="44b37-120">**singleSignOn (OneX)**</span><span class="sxs-lookup"><span data-stu-id="44b37-120">**singleSignOn (OneX)**</span></span>](onexschema-singlesignon-onex-element.md)
        -   [<span data-ttu-id="44b37-121">**type (singleSignOn)**</span><span class="sxs-lookup"><span data-stu-id="44b37-121">**type (singleSignOn)**</span></span>](onexschema-type-singlesignon-element.md)
        -   [<span data-ttu-id="44b37-122">**maxDelay (singleSignOn)**</span><span class="sxs-lookup"><span data-stu-id="44b37-122">**maxDelay (singleSignOn)**</span></span>](onexschema-maxdelay-singlesignon-element.md)
        -   [<span data-ttu-id="44b37-123">**userBasedVirtualLan (singleSignOn)**</span><span class="sxs-lookup"><span data-stu-id="44b37-123">**userBasedVirtualLan (singleSignOn)**</span></span>](onexschema-userbasedvirtuallan-singlesignon-element.md)
    -   [<span data-ttu-id="44b37-124">**EAPConfig (OneX)**</span><span class="sxs-lookup"><span data-stu-id="44b37-124">**EAPConfig (OneX)**</span></span>](onexschema-eapconfig-onex-element.md)

 

 



