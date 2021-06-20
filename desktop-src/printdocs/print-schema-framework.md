---
description: Ces articles fournissent des informations plus détaillées sur la signification et l’utilisation des types d’éléments de schéma d’impression.
ms.assetid: 05c7fd07-1c32-409d-8ca5-820038af3440
title: Structure du schéma d’impression
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 570701df700954ad85fb724b9528b7e7912f3174
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407162"
---
# <a name="print-schema-framework"></a><span data-ttu-id="a5f93-103">Structure du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="a5f93-103">Print Schema Framework</span></span>

<span data-ttu-id="a5f93-104">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="a5f93-104">This topic is not current.</span></span> <span data-ttu-id="a5f93-105">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="a5f93-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="a5f93-106">Cette section fournit des informations plus détaillées sur la signification et l’utilisation des types d’éléments de schéma d’impression.</span><span class="sxs-lookup"><span data-stu-id="a5f93-106">This section provides more detailed information on the meaning and usage of the Print Schema element types.</span></span> <span data-ttu-id="a5f93-107">L’objectif principal de la version initiale de l’infrastructure du schéma d’impression est de représenter les configurations et les capacités des attributs des appareils.</span><span class="sxs-lookup"><span data-stu-id="a5f93-107">The main focus of the initial version of the Print Schema Framework is to represent configurations and capabilities of device attributes.</span></span> <span data-ttu-id="a5f93-108">À un niveau élevé, cette infrastructure offre deux styles différents de description d’un attribut d’appareil : en tant que construction fonctionnalité/option, ou en tant que construction de paramètre.</span><span class="sxs-lookup"><span data-stu-id="a5f93-108">At a high level, this framework offers two different styles of describing a device attribute: as a Feature/Option construct, or as a parameter construct.</span></span> <span data-ttu-id="a5f93-109">Si un attribut d’appareil a un petit nombre de valeurs ou d’États disponibles, l’attribut doit être caractérisé comme une fonctionnalité avec les valeurs ou les États autorisés appelés éléments d’option.</span><span class="sxs-lookup"><span data-stu-id="a5f93-109">If a device attribute has a small number of available values or states, then the attribute should be characterized as a Feature with the allowed values or states referred to as Option elements.</span></span> <span data-ttu-id="a5f93-110">À l’inverse, si un attribut d’appareil a un grand nombre de valeurs ou d’États disponibles et que l’ensemble de toutes les valeurs possibles est facilement défini sans avoir recours à une énumération explicite, l’attribut de l’appareil doit être caractérisé comme un paramètre.</span><span class="sxs-lookup"><span data-stu-id="a5f93-110">Conversely, if a device attribute has a large number of available values or states and the set of all possible values is easily defined without resorting to explicit enumeration, the device attribute should be characterized as a parameter.</span></span> <span data-ttu-id="a5f93-111">(Un paramètre est défini au moyen d’un élément ParameterDef, et une instance de paramètre est initialisée au moyen d’un élément ParameterInit.) Les éléments de propriété sont utilisés dans les constructions de fonctionnalités et d’options et de paramètres pour fournir un niveau de différenciation plus fin.</span><span class="sxs-lookup"><span data-stu-id="a5f93-111">(A parameter is defined by means of a ParameterDef element, and a parameter instance is initialized by means of a ParameterInit element.) Property elements are used within Feature/Option and parameter constructs to provide a finer level of differentiation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a5f93-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a5f93-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a5f93-113">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="a5f93-113">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



