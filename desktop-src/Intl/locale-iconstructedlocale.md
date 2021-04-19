---
description: Paramètres régionaux \_ ICONSTRUCTEDLOCALE Description de la constante
ms.assetid: 5557ee1e-09bf-0d0b-8e73-df32d9a406dd
title: LOCALE_ICONSTRUCTEDLOCALE
ms.topic: article
ms.date: 09/01/2020
ms.openlocfilehash: 120c206a14030a182378977c9e68fb7dcd77200d
ms.sourcegitcommit: 4af3e9ec3142ba499d20ed8b174c2b219c5eacd2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/30/2021
ms.locfileid: "106541569"
---
# <a name="locale_iconstructedlocale"></a><span data-ttu-id="f77bb-103">paramètres régionaux \_ ICONSTRUCTEDLOCALE</span><span class="sxs-lookup"><span data-stu-id="f77bb-103">LOCALE\_ICONSTRUCTEDLOCALE</span></span>

<span data-ttu-id="f77bb-104">Identificateur à demander si les paramètres régionaux sont des paramètres régionaux « construits ».</span><span class="sxs-lookup"><span data-stu-id="f77bb-104">Identifier to request if the locale is a "constructed" locale.</span></span> <span data-ttu-id="f77bb-105">L’utilisation de ce LCTYPE est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="f77bb-105">Use of this LCTYPE is discouraged.</span></span>

<span data-ttu-id="f77bb-106">Cela identifie les paramètres régionaux pour lesquels Windows n’ont pas d’informations complètes et qui doivent « construire » des informations au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="f77bb-106">This identifies a locale for which Windows many not have complete information and has to "construct" information at runtime.</span></span> <span data-ttu-id="f77bb-107">En général, les informations fournies par LOCALE_ICONSTRUCTEDLOCALE sont limitées, car Windows fournira autant de données que possible pour chaque paramètre régional.</span><span class="sxs-lookup"><span data-stu-id="f77bb-107">Typically the information provided by LOCALE_ICONSTRUCTEDLOCALE is of limited use as Windows will provide as much data as is available for every locale.</span></span> <span data-ttu-id="f77bb-108">Par conséquent, l’utilisation de ce LCTYPE est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="f77bb-108">Therefore, use of this LCTYPE is discouraged.</span></span>


| <span data-ttu-id="f77bb-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="f77bb-109">Value</span></span> | <span data-ttu-id="f77bb-110">Signification</span><span class="sxs-lookup"><span data-stu-id="f77bb-110">Meaning</span></span>                 |
|-------|-------------------------|
| <span data-ttu-id="f77bb-111">0</span><span class="sxs-lookup"><span data-stu-id="f77bb-111">0</span></span>     | <span data-ttu-id="f77bb-112">Non construit</span><span class="sxs-lookup"><span data-stu-id="f77bb-112">Not constructed</span></span>         |
| <span data-ttu-id="f77bb-113">1</span><span class="sxs-lookup"><span data-stu-id="f77bb-113">1</span></span>     | <span data-ttu-id="f77bb-114">Est un paramètre régional construit</span><span class="sxs-lookup"><span data-stu-id="f77bb-114">Is a constructed locale</span></span> |


<span data-ttu-id="f77bb-115">Par exemple, une demande pour « fr-fr » ou l’allemand dans le États-Unis.</span><span class="sxs-lookup"><span data-stu-id="f77bb-115">An example would be a request for "de-US", or German in the United States.</span></span> <span data-ttu-id="f77bb-116">NLS utilise les données en langue allemande qu’il peut trouver et les données de la région États-Unis qu’il peut trouver.</span><span class="sxs-lookup"><span data-stu-id="f77bb-116">NLS will use the German language data that it can find and the United States region data that it can find.</span></span> 

<span data-ttu-id="f77bb-117">Cela peut ne pas être parfait, par exemple, le système n’aura probablement pas d’informations sur le nom de États-Unis en allemand.</span><span class="sxs-lookup"><span data-stu-id="f77bb-117">This may not be perfect as, for example, the system will likely not have information about the name of United States in German.</span></span> <span data-ttu-id="f77bb-118">Toutefois, si l’application ou l’utilisateur désire un contexte de « -US », les données retournées sont les meilleures disponibles.</span><span class="sxs-lookup"><span data-stu-id="f77bb-118">However, if the application or user desires a "de-US" context, then the returned data is the best available.</span></span> 

<span data-ttu-id="f77bb-119">Les applications qui utilisent LOCALE_ICONSTRUCTEDLOCALE pour refuser des paramètres régionaux et revenir à des paramètres régionaux différents finissent par être moins expérimentés, comme le débarquement de-fr ou fr-US dans cet exemple.</span><span class="sxs-lookup"><span data-stu-id="f77bb-119">Apps that use LOCALE_ICONSTRUCTEDLOCALE to reject locales and fall back to a different locale typically end up with a worse experience, such as landing on de-DE or en-US in this example.</span></span> <span data-ttu-id="f77bb-120">Aucun de ces n’est proche de la demande d’origine de la langue allemande avec une région de États-Unis.</span><span class="sxs-lookup"><span data-stu-id="f77bb-120">Neither of those are close to the original request for German language with a United States region.</span></span>

