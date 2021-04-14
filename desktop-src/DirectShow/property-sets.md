---
description: Jeux de propriétés
ms.assetid: 4b8a917f-7a6c-4433-83f4-b83ef6d26115
title: Jeux de propriétés (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcdc65efbc99eeed3a5f94ab33ce5ec982975852
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392560"
---
# <a name="property-sets-directshow"></a><span data-ttu-id="fc36f-103">Jeux de propriétés (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="fc36f-103">Property Sets (DirectShow)</span></span>

<span data-ttu-id="fc36f-104">Microsoft DirectShow utilise des jeux de propriétés pour prendre en charge les services étendus offerts par le matériel et les pilotes et filtres associés.</span><span class="sxs-lookup"><span data-stu-id="fc36f-104">Microsoft DirectShow uses property sets to support extended services offered by hardware and its associated drivers and filters.</span></span> <span data-ttu-id="fc36f-105">Les fournisseurs de matériel et de filtre peuvent définir de nouvelles fonctionnalités en tant que propriétés, les réorganiser dans les jeux de propriétés et publier la spécification pour ces jeux de propriétés.</span><span class="sxs-lookup"><span data-stu-id="fc36f-105">Hardware and filter vendors can define new capabilities as properties, arrange them in property sets, and publish the specification for these property sets.</span></span> <span data-ttu-id="fc36f-106">En tant que développeur d’applications, vous pouvez utiliser les méthodes de l’interface [**IKsPropertySet**](ikspropertyset.md) pour déterminer si un pilote ou un filtre prend en charge un ensemble de propriétés particulier, et récupérer ou définir ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="fc36f-106">As the application developer, you can use the methods of the [**IKsPropertySet**](ikspropertyset.md) interface to determine whether a driver or filter supports a particular set of properties, and retrieve or set those properties.</span></span>

<span data-ttu-id="fc36f-107">Toutes les méthodes exposées par **IKsPropertySet** requièrent un **GUID** qui identifie le jeu de propriétés (le paramètre *GuidPropSet* ) et une valeur **DWORD** qui identifie la propriété dans le jeu de propriétés (le paramètre *dwPropID* ).</span><span class="sxs-lookup"><span data-stu-id="fc36f-107">All the methods exposed by **IKsPropertySet** require a **GUID** that identifies the property set (the *guidPropSet* parameter) and a **DWORD** that identifies the property within the property set (the *dwPropID* parameter).</span></span> <span data-ttu-id="fc36f-108">Le paramètre *dwPropID* est généralement un membre d’un type de données énuméré.</span><span class="sxs-lookup"><span data-stu-id="fc36f-108">The *dwPropID* parameter is typically a member of an enumerated data type.</span></span>

<span data-ttu-id="fc36f-109">Les propriétés individuelles peuvent avoir des données associées que vous spécifiez dans le paramètre *pPropData* dans les méthodes [**IKsPropertySet :: Set**](ikspropertyset-set.md) et [**IKsPropertySet :: obtenir**](ikspropertyset-get.md) .</span><span class="sxs-lookup"><span data-stu-id="fc36f-109">Individual properties can have associated data that you specify in the *pPropData* parameter in the [**IKsPropertySet::Set**](ikspropertyset-set.md) and [**IKsPropertySet::Get**](ikspropertyset-get.md) methods.</span></span> <span data-ttu-id="fc36f-110">Dans ces méthodes, les données de propriété sont typées comme un pointeur vers `void` .</span><span class="sxs-lookup"><span data-stu-id="fc36f-110">In these methods, the property data is typed as a pointer to `void`.</span></span> <span data-ttu-id="fc36f-111">Le type de données et la signification des données sont spécifiés dans la définition du jeu de propriétés.</span><span class="sxs-lookup"><span data-stu-id="fc36f-111">The data type and the meaning of the data are specified in the definition of the property set.</span></span>

<span data-ttu-id="fc36f-112">Les sections suivantes fournissent des informations sur les jeux de propriétés pris en charge dans DirectShow :</span><span class="sxs-lookup"><span data-stu-id="fc36f-112">The following sections provide information about the property sets supported in DirectShow:</span></span>

-   [<span data-ttu-id="fc36f-113">**Jeu de propriétés protection de copie de DVD**</span><span class="sxs-lookup"><span data-stu-id="fc36f-113">**DVD Copy Protection Property Set**</span></span>](dvd-copy-protection-property-set.md)
-   [<span data-ttu-id="fc36f-114">**Jeu de propriétés Karaoké DVD**</span><span class="sxs-lookup"><span data-stu-id="fc36f-114">**DVD Karaoke Property Set**</span></span>](dvd-karaoke-property-set.md)
-   [<span data-ttu-id="fc36f-115">**Jeu de propriétés de sous-image de DVD**</span><span class="sxs-lookup"><span data-stu-id="fc36f-115">**DVD Subpicture Property Set**</span></span>](dvd-subpicture-property-set.md)
-   [<span data-ttu-id="fc36f-116">Ensemble de propriétés de transport d’appareil externe</span><span class="sxs-lookup"><span data-stu-id="fc36f-116">External Device Transport Property Set</span></span>](external-device-transport-property-set.md)
-   [<span data-ttu-id="fc36f-117">Jeu de propriétés du pas à pas de frame</span><span class="sxs-lookup"><span data-stu-id="fc36f-117">Frame Stepping Property Set</span></span>](frame-stepping-property-set.md)
-   [<span data-ttu-id="fc36f-118">Épingler le jeu de propriétés</span><span class="sxs-lookup"><span data-stu-id="fc36f-118">Pin Property Set</span></span>](pin-property-set.md)
-   [<span data-ttu-id="fc36f-119">**Définition de la propriété change rate**</span><span class="sxs-lookup"><span data-stu-id="fc36f-119">**Rate Change Property Set**</span></span>](rate-change-property-set.md)

 

 



