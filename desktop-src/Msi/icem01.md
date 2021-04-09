---
description: ICEM01 valide le fonctionnement du mécanisme ICE. Cette glace utilise la propriété Time pour connaître l’heure et retourne l’heure système ou aucune.
ms.assetid: f3b7677d-6b2e-4aa0-92eb-1b1e62cdf0a6
title: ICEM01
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bca7f2ffb3fcf5e3d50a3937a1f17fddd3a912f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113843"
---
# <a name="icem01"></a><span data-ttu-id="8fade-104">ICEM01</span><span class="sxs-lookup"><span data-stu-id="8fade-104">ICEM01</span></span>

<span data-ttu-id="8fade-105">ICEM01 valide le fonctionnement du mécanisme ICE.</span><span class="sxs-lookup"><span data-stu-id="8fade-105">ICEM01 validates that the ICE mechanism is working.</span></span> <span data-ttu-id="8fade-106">Cette glace utilise la propriété [**Time**](time.md) pour connaître l’heure et retourne l’heure système ou aucune.</span><span class="sxs-lookup"><span data-stu-id="8fade-106">This ICE uses the [**Time**](time.md) property to get the time and returns either the system time or None.</span></span>

<span data-ttu-id="8fade-107">Le module de fusion CIEM est stocké dans un fichier de module de fusion. CUB appelé Mergemod. CUB et non dans le fichier. CUB contenant le CIEM utilisé pour la validation du package.</span><span class="sxs-lookup"><span data-stu-id="8fade-107">Merge module ICEs are stored in a merge module .cub file called Mergemod.cub and not in the .cub file containing the ICEs used for package validation.</span></span>

## <a name="result"></a><span data-ttu-id="8fade-108">Résultats</span><span class="sxs-lookup"><span data-stu-id="8fade-108">Result</span></span>

<span data-ttu-id="8fade-109">ICEM01 publie un message indiquant l’heure à laquelle le programme d’installation a appelé ICEM01.</span><span class="sxs-lookup"><span data-stu-id="8fade-109">ICEM01 posts a message giving the time the installer called ICEM01.</span></span> <span data-ttu-id="8fade-110">Cette glace ne doit jamais retourner une erreur.</span><span class="sxs-lookup"><span data-stu-id="8fade-110">This ICE should never return an error.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8fade-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8fade-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8fade-112">Référence ICE du module de fusion</span><span class="sxs-lookup"><span data-stu-id="8fade-112">Merge Module ICE Reference</span></span>](merge-module-ice-reference.md)
</dt> </dl>

 

 



