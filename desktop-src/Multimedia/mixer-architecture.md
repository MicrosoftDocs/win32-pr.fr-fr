---
title: Architecture du mélangeur
description: Architecture du mélangeur
ms.assetid: 11d650bf-c258-4818-88b7-9fdc71a8d859
keywords:
- audio multimédia, architecture de mixage
- audio, architecture de mixage
- mixages audio, architecture
- mixages audio, lignes audio
- lignes audio
- mixages audio, contrôles
- audio multimédia, contrôles de mixage
- audio, contrôles de mixage
- mixages, lignes audio
- mixages, architecture
- mélangeurs, contrôles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 447b0cdc44a33237aa7e0c726a5eb533b3bc7d0e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309933"
---
# <a name="mixer-architecture"></a><span data-ttu-id="8eace-114">Architecture du mélangeur</span><span class="sxs-lookup"><span data-stu-id="8eace-114">Mixer Architecture</span></span>

<span data-ttu-id="8eace-115">L’élément de base de l’architecture du mélangeur est une *ligne audio*.</span><span class="sxs-lookup"><span data-stu-id="8eace-115">The basic element of the mixer architecture is an *audio line*.</span></span> <span data-ttu-id="8eace-116">Une ligne audio se compose d’un ou de plusieurs canaux de données provenant d’une source unique ou d’une ressource système.</span><span class="sxs-lookup"><span data-stu-id="8eace-116">An audio line consists of one or more channels of data originating from a single source or a system resource.</span></span> <span data-ttu-id="8eace-117">Par exemple, une ligne audio stéréo a deux canaux de données, mais elle est considérée comme une seule ligne audio, car elle provient d’une source unique.</span><span class="sxs-lookup"><span data-stu-id="8eace-117">For example, a stereo audio line has two data channels, but it is considered a single audio line because it originates from a single source.</span></span>

<span data-ttu-id="8eace-118">L’architecture du mélangeur fournit des services de routage pour gérer les lignes audio sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="8eace-118">The mixer architecture provides routing services to manage audio lines on a computer.</span></span> <span data-ttu-id="8eace-119">Vous pouvez utiliser les services de routage si vous avez installé les périphériques matériels et les pilotes de logiciels appropriés.</span><span class="sxs-lookup"><span data-stu-id="8eace-119">You can use the routing services if you have adequate hardware devices and software drivers installed.</span></span> <span data-ttu-id="8eace-120">L’architecture du mélangeur permet de mapper plusieurs lignes de sources audio sur une seule ligne audio de destination.</span><span class="sxs-lookup"><span data-stu-id="8eace-120">The mixer architecture allows several audio source lines to map to a single destination audio line.</span></span>

<span data-ttu-id="8eace-121">Chaque ligne audio peut être associée à des contrôles de mixage.</span><span class="sxs-lookup"><span data-stu-id="8eace-121">Each audio line can have mixer controls associated with it.</span></span> <span data-ttu-id="8eace-122">Un contrôle de mixage peut exécuter un nombre quelconque de fonctions (telles que le volume de contrôle), en fonction des caractéristiques de la ligne audio associée.</span><span class="sxs-lookup"><span data-stu-id="8eace-122">A mixer control can perform any number of functions (such as control volume), depending on the characteristics of the associated audio line.</span></span>

 

 




