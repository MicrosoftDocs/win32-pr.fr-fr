---
description: Profil en mode restreint et établissement de la configuration
ms.assetid: 550f5413-eaa4-4530-867e-fd9b1907cadf
title: Profil en mode restreint et établissement de la configuration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17a424505b3934131527f249176f9fe0984b320a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392532"
---
# <a name="restricted-mode-profile-and-configuration-establishment"></a><span data-ttu-id="f0d7f-103">Profil en mode restreint et établissement de la configuration</span><span class="sxs-lookup"><span data-stu-id="f0d7f-103">Restricted Mode Profile and Configuration Establishment</span></span>

<span data-ttu-id="f0d7f-104">En raison de la variété des types de données qui peuvent être décodées par DirectX VA et des configurations de décodage multiples prises en charge dans DirectX VA pour chacun de ces types de données (par exemple, à l’aide des tampons de flux binaire par rapport au décodage des différences résiduelles de l’hôte par rapport aux IDCT basés sur des accélérateurs avec et sans chiffrement de chaque type de mémoire tampon, etc.), nous pensons qu’il serait un peu plus simple de spécifier un GUID unique pour chaque type de données et configuration de décodage uniques.</span><span class="sxs-lookup"><span data-stu-id="f0d7f-104">Due to the variety of types of data that can be decoded by DirectX VA, and the multiple decoding configurations supported within DirectX VA for each of these types of data (for example, using bitstream buffers versus host residual difference decoding versus accelerator-based IDCT with and without encryption of each relevant type of buffer, and so on), we believe it would be somewhat ungainly to simply specify a unique GUID for every unique data type and decoding configuration.</span></span> <span data-ttu-id="f0d7f-105">Cela créerait un grand nombre de GUID (par exemple, s’il existait 16 profils de DirectX VA et 16 configurations possibles pour chacun d’entre eux), il faudrait 256 GUID définis, ce qui nécessite 4 kilo-octets de mémoire tout simplement pour les conserver.</span><span class="sxs-lookup"><span data-stu-id="f0d7f-105">This would create a large number of GUIDs (for example, hypothetically if there were 16 profiles of DirectX VA and 16 configurations possible for each, there would need to be 256 defined GUIDs—requiring 4 kilobytes of memory just to hold them all.</span></span> <span data-ttu-id="f0d7f-106">Ce problème est la partie la plus difficile pour déterminer comment mapper DirectX VA dans **IAMVideoAccelerator**, avec le reste de la définition opérationnelle qui est généralement assez simple.</span><span class="sxs-lookup"><span data-stu-id="f0d7f-106">This issue is the most difficult part of determining how to map DirectX VA into **IAMVideoAccelerator**, with the remainder of the operational definition mostly being quite straightforward.</span></span> <span data-ttu-id="f0d7f-107">Par conséquent, nous spécifions un GUID unique pour chaque type de données (pour chaque profil en mode restreint) et vous autorisez l’Association d’un GUID supplémentaire à chaque type de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="f0d7f-107">As a result, we specify a unique GUID only for each type of data (for each restricted mode profile) and allow an additional GUID to be associated with each type of encryption.</span></span> <span data-ttu-id="f0d7f-108">La configuration du décodage est ensuite établie entre le décodeur et l’accélérateur par une négociation subordonnée de niveau inférieur à l’aide d’opérations de détection et de verrouillage pour établir des configurations pour chaque type de fonction DirectX VA.</span><span class="sxs-lookup"><span data-stu-id="f0d7f-108">The decoding configuration is then established between the decoder and accelerator by a lower-level subordinate negotiation using probing and locking operations to establish configurations for each type of DirectX VA function.</span></span>

 

 



