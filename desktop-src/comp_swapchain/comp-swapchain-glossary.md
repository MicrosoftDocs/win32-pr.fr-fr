---
title: Glossaire utilise permutation de la composition
description: Glossaire des termes de la composition utilise permutation.
ms.topic: article
ms.date: 09/10/2021
ms.openlocfilehash: 04450f5107a9c06cc231336449e8ed9563212ad4
ms.sourcegitcommit: 2c13d0f1620f7c089687ef1d97e8c1d22e5d537a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "128523847"
---
# <a name="composition-swapchain-glossary"></a>Glossaire utilise permutation de la composition

> [!NOTE]
> **Certaines informations portent sur la préversion du produit, qui est susceptible d’être en grande partie modifié avant sa commercialisation. Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.**

|Terme|Signification|
|-|-|
|**Disponible (mémoire tampon de présentation)**|Mémoire tampon qui est sécurisée pour le rendu de votre application sans altérer les cadeaux précédents. Pour être disponible, une mémoire tampon ne doit pas avoir de présentation précédente qui la référence qui n’a pas été entrée dans le retrait ou le retrait. Un présent peut référencer implicitement une mémoire tampon à partir d’un présent présent si votre application n’a pas mis à jour une surface, comme indiqué dans l’exemple du [diagramme de mémoires tampons, de surfaces et de cadeaux](comp-swapchain.md#diagram-of-buffers-surfaces-and-presents).|
|**Composition (mode de présentation)**|Forme de présentation dans laquelle la mémoire tampon présentée par votre application est copiée dans le cache en mémoire tampon que DWM affiche et envoie pour afficher le matériel. Cette forme de présentation a une configuration système inférieure à scanout directe ou iflip, mais elle est également moins efficace.|
|**Poignée de surface de la composition**|**Handle** qui peut lier un visuel d’arborescence visuelle à un utilise permutation donné ou à une surface de présentation.|
|**Retournement direct**|Forme de présentation dans laquelle la présentation de la mémoire tampon par votre application est envoyée directement pour afficher le matériel sur les systèmes qui ne prennent pas en charge la superposition Multiplan.|
|**Scanout directe**|Forme de présentation dans laquelle la mémoire tampon présentée par votre application n’est pas restituée à nouveau dans la mémoire tampon que le DWM envoie à l’écran, mais est envoyée directement au matériel scanout GPU. Cela peut impliquer le DWM en affectant la mémoire tampon à un plan de recouvrement Multiplan, ou il peut s’agir d’un mode dans lequel la mémoire tampon est envoyée directement au matériel scanout via le *retournement direct*. Dans un mode de présentation direct scanout, DWM peut être impliqué dans la programmation du matériel pour afficher le présent, ou il peut être contourné entièrement lorsque le système est en mode *iflip* .|
|**Rendu de la mémoire tampon avant**|Travail de dessin émis pour une mémoire tampon actuellement affichée par le système. En fonction de la façon dont la mémoire tampon est affichée, cela peut entraîner une altération ou un blocage de l’application, car Direct3D protège contre l’émission du travail de rendu dans des mémoires tampons affichées par le matériel scanout.|
|**File d’attente de basculement matériel**|Fonctionnalité du système d’exploitation prise en charge par un matériel GPU qui permet aux GPU de s’afficher indépendamment, sans implication de l’UC, ce qui réduit la consommation d’énergie, mais peut retarder les mises à jour de l’état du processeur telles que les événements disponibles dans la mémoire tampon, présenter la clôture de mise hors service et présenter les statistiques.|
|**Retournement indépendant (iflip)**|Une méthode plus efficace de présentation scanout directe dans laquelle les cadeaux sont envoyés directement au matériel scanout GPU, ignorant complètement le DWM. Cette forme de présentation présente une configuration système plus élevée, mais permet de réduire les latences et les économies d’énergie du système.|
|**Superposition Multiplan (MPO)**|Type de matériel d’affichage qui est capable d’afficher plusieurs plans affichés au-dessus des autres. Les éléments présentés dans le gestionnaire de présentation peuvent être affichés dans le cadre d’un plan dans une configuration MPO pour éviter de devoir copier la mémoire tampon de présentation dans la mémoire tampon que DWM envoie au matériel d’affichage.|
|**Trouver**|Une seule instance de Presentation. Présent qui est destiné à afficher les résultats d’une opération de dessin dans une mémoire tampon unique à l’écran.|
|**Identificateur présent (ID)**|Identificateur d’incrémentation, unique au sein d’un gestionnaire de présentation donné, associé à chaque présent pour lui permettre d’être référencé par des éléments tels que des statistiques de présentation et des délimiteurs de présence.|
|**File d’attente actuelle**|Une file d’attente de présente qu’un gestionnaire de présentation a émis, mais qu’il n’a pas encore été traité par le système. Tous les cadeaux émis sont traités dans l’ordre de la file d’attente, même si leurs heures cibles ne s’améliorent pas. Autrement dit, avant que le présent *n* ne puisse être traité, la présentation *n-1* doit également être traitée. par conséquent, si les versions suivantes ont une heure cible antérieure à celle d’un présent, elles remplacent immédiatement cette présence particulière.|
|**(Présent) heure cible**|Heure à laquelle un présent particulier doit s’afficher à l’écran. Le système tentera d’afficher la présentation comme à l’heure la plus proche possible.|
|**Statistiques de présentation**|informations retournées à votre application qui décrivent comment un présent particulier a été traité. Les statistiques sont mises en file d’attente dans le gestionnaire de présentation pour être lues par votre application.|
|**Surface de présentation**|espace réservé de contenu qui peut être lié à un visuel dans une arborescence d’éléments visuels. Une surface de présentation peut avoir une seule mémoire tampon affichée à la fois. Présentation Manager met à jour les mémoires tampons pour une ou plusieurs surfaces de présentation.|
|**Présentation**|Concept de l’affichage des résultats des opérations de dessin sur l’écran.|
|**Mémoire tampon de présentation**|Texture Direct3D qui a été associée à un gestionnaire de présentation et qui peut donc être présentée par ce gestionnaire de présentation à l’écran.|
|**Arborescence d’éléments visuels**|Arborescence d’éléments visuels qui décrit la disposition d’une application. Les problèmes de l’API utilise permutation de composition présentent un ou plusieurs visuels dans une arborescence d’éléments visuels. pour plus d’informations, consultez [**Windows. UI. Composition**](/uwp/api/windows.ui.composition) et documentation de l’API [**DirectComposition**](/windows/win32/directcomp/directcomposition-portal) .|
|**Interruption VSync**|Lorsqu’un GPU affiche un présent, il émet une interruption VSync pour réveiller le processeur afin de l’informer qu’il a eu lieu. Cela permet à l’UC de mettre à jour l’État, par exemple les événements de mémoire tampon disponibles, la clôture de mise hors service présente et les statistiques actuelles. Si le GPU prend en charge la file d’attente de basculement matériel, votre application peut explicitement contrôler les cadeaux qui doivent forcer une interruption VSync et mettre immédiatement à jour l’État, et ce qui n’est pas le cas, ce qui permet d’améliorer l’efficacité énergétique au détriment des commentaires retardés.|

## <a name="related-topics"></a>Rubriques connexes

* [Utilise permutation de la composition](comp-swapchain-portal.md)
