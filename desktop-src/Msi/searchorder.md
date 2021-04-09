---
description: La définition de cette stratégie système par utilisateur spécifie l’ordre dans lequel le programme d’installation effectue une recherche dans trois types de sources.
ms.assetid: c16a5cbb-d530-4932-944b-af68d0a4018c
title: SearchOrder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8f486ee58eebd1a1bd1174f18e413785e5e3129
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869046"
---
# <a name="searchorder"></a><span data-ttu-id="79785-103">SearchOrder</span><span class="sxs-lookup"><span data-stu-id="79785-103">SearchOrder</span></span>

<span data-ttu-id="79785-104">La définition de cette [stratégie système](system-policy.md) par utilisateur spécifie l’ordre dans lequel le programme d’installation effectue une recherche dans trois types de sources.</span><span class="sxs-lookup"><span data-stu-id="79785-104">Setting this per-user [system policy](system-policy.md) specifies the order in which the installer searches three types of sources.</span></span> <span data-ttu-id="79785-105">Les types de sources sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="79785-105">The types of sources are:</span></span>

<span data-ttu-id="79785-106">« n » – réseau</span><span class="sxs-lookup"><span data-stu-id="79785-106">"n" – network</span></span>

<span data-ttu-id="79785-107">« m » – média (CD-ROM ou DVD)</span><span class="sxs-lookup"><span data-stu-id="79785-107">"m" – media (CD-ROM or DVD)</span></span>

<span data-ttu-id="79785-108">« u » – Uniform Resource Locator (URL)</span><span class="sxs-lookup"><span data-stu-id="79785-108">"u" – Uniform Resource Locator (URL)</span></span>

<span data-ttu-id="79785-109">Par exemple, pour effectuer une recherche dans les sources réseau en premier, les sources de média seconde et les sources d’URL, la valeur de cette stratégie est « NMU ».</span><span class="sxs-lookup"><span data-stu-id="79785-109">For example, to search network sources first, media sources second, and URL sources last set this policy to a value of "nmu".</span></span> <span data-ttu-id="79785-110">Pour omettre la recherche d’un type de source particulier, laissez la lettre correspondante de la valeur.</span><span class="sxs-lookup"><span data-stu-id="79785-110">To omit searching for a particular source type, leave out the corresponding letter from the value.</span></span>

<span data-ttu-id="79785-111">Si l’option SearchOrder n’est pas définie, l’ordre de recherche par défaut est Network, Media, puis URL.</span><span class="sxs-lookup"><span data-stu-id="79785-111">If SearchOrder is not set, the default search order is network, media, and then URL.</span></span>

## <a name="registry-key"></a><span data-ttu-id="79785-112">Clé de Registre</span><span class="sxs-lookup"><span data-stu-id="79785-112">Registry Key</span></span>

<span data-ttu-id="79785-113">**HKEY \_ \_** \\ **Stratégies logicielles** de l’utilisateur actuel \\  \\ **Microsoft** \\ **Windows** \\ **installer**</span><span class="sxs-lookup"><span data-stu-id="79785-113">**HKEY\_CURRENT\_USER**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="79785-114">Type de données</span><span class="sxs-lookup"><span data-stu-id="79785-114">Data Type</span></span>

<span data-ttu-id="79785-115">**SZ de REG \_**</span><span class="sxs-lookup"><span data-stu-id="79785-115">**REG\_SZ**</span></span>

## <a name="related-topics"></a><span data-ttu-id="79785-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="79785-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="79785-117">Résilience source</span><span class="sxs-lookup"><span data-stu-id="79785-117">Source Resiliency</span></span>](source-resiliency.md)
</dt> </dl>

 

 



