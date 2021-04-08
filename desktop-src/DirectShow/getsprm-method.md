---
description: La méthode GetSPRM récupère le registre de paramètres système spécifié.
ms.assetid: c6177f43-2809-4ef2-bc94-ac9a28f94621
title: Méthode GetSPRM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc8b6898902eda55e0e877878343a25d82d03660
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103949970"
---
# <a name="getsprm-method"></a><span data-ttu-id="bbb83-103">Méthode GetSPRM</span><span class="sxs-lookup"><span data-stu-id="bbb83-103">GetSPRM Method</span></span>

> [!Note]  
> <span data-ttu-id="bbb83-104">Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="bbb83-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="bbb83-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="bbb83-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="bbb83-106">La `GetSPRM` méthode récupère le registre de paramètres système spécifié.</span><span class="sxs-lookup"><span data-stu-id="bbb83-106">The `GetSPRM` method retrieves the specified system parameter register.</span></span>

``` syntax
[ iSPRM = ] MSWebDVD.GetSPRM(iIndex)
```

## <a name="parameters"></a><span data-ttu-id="bbb83-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bbb83-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bbb83-108"><span id="iIndex"></span><span id="iindex"></span><span id="IINDEX"></span>*iIndex*</span><span class="sxs-lookup"><span data-stu-id="bbb83-108"><span id="iIndex"></span><span id="iindex"></span><span id="IINDEX"></span>*iIndex*</span></span>
</dt> <dd>

<span data-ttu-id="bbb83-109">Spécifie l’enregistrement dont vous souhaitez récupérer la valeur sous la forme d’un entier.</span><span class="sxs-lookup"><span data-stu-id="bbb83-109">Specifies the register whose value you want to retrieve as an Integer.</span></span> <span data-ttu-id="bbb83-110">L’entier doit être compris entre 0 et 23.</span><span class="sxs-lookup"><span data-stu-id="bbb83-110">The Integer must range from 0 through 23.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bbb83-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="bbb83-111">Return Value</span></span>

<span data-ttu-id="bbb83-112">Retourne une valeur entière représentant le contenu du Registre spécifié.</span><span class="sxs-lookup"><span data-stu-id="bbb83-112">Returns an integer value representing the contents of the specified register.</span></span>

## <a name="remarks"></a><span data-ttu-id="bbb83-113">Notes</span><span class="sxs-lookup"><span data-stu-id="bbb83-113">Remarks</span></span>

<span data-ttu-id="bbb83-114">Le disque contrôle les registres des paramètres système (SPRMs).</span><span class="sxs-lookup"><span data-stu-id="bbb83-114">The disc controls system parameter registers (SPRMs).</span></span> <span data-ttu-id="bbb83-115">Une application de lecteur n’A pas besoin d’accéder à ces registres pour les fonctionnalités de navigation standard.</span><span class="sxs-lookup"><span data-stu-id="bbb83-115">A player application doesn't need to access these registers for any standard navigation functionality.</span></span> <span data-ttu-id="bbb83-116">SPRMs représente l’état du joueur.</span><span class="sxs-lookup"><span data-stu-id="bbb83-116">SPRMs represent the status of the player.</span></span> <span data-ttu-id="bbb83-117">Chacune d’elles a une signification, définie par les préférences de l’utilisateur, les commandes de disque et d’autres occurrences qu’une application n’a pas de contrôle direct.</span><span class="sxs-lookup"><span data-stu-id="bbb83-117">Each one has a meaning, set by user preferences, disc commands, and other occurrences that an application has no direct control over.</span></span> <span data-ttu-id="bbb83-118">Une application peut lire ces registres, mais ne peut pas y écrire.</span><span class="sxs-lookup"><span data-stu-id="bbb83-118">An application can read these registers but cannot write to them.</span></span> <span data-ttu-id="bbb83-119">Pour utiliser ces registres efficacement, vous aurez probablement besoin d’une connaissance plus détaillée des commandes de navigation de DVD que celles fournies dans cette documentation.</span><span class="sxs-lookup"><span data-stu-id="bbb83-119">To use these registers effectively, you will probably need a more detailed knowledge of the DVD navigation commands than is provided in this documentation.</span></span> <span data-ttu-id="bbb83-120">Le tableau suivant présente le contenu de chaque registre.</span><span class="sxs-lookup"><span data-stu-id="bbb83-120">The following table shows the contents of each register.</span></span> <span data-ttu-id="bbb83-121">Pour plus d’informations sur le contenu du Registre, consultez [ **IDvdInfo2 :: GetAllSPRMs**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getallsprms)</span><span class="sxs-lookup"><span data-stu-id="bbb83-121">For more detailed information on the register contents, see [**IDvdInfo2::GetAllSPRMs**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getallsprms)</span></span>



| <span data-ttu-id="bbb83-122">S’inscrire</span><span class="sxs-lookup"><span data-stu-id="bbb83-122">Register</span></span> | <span data-ttu-id="bbb83-123">Contenu</span><span class="sxs-lookup"><span data-stu-id="bbb83-123">Contents</span></span>                        |
|----------|---------------------------------|
| <span data-ttu-id="bbb83-124">0</span><span class="sxs-lookup"><span data-stu-id="bbb83-124">0</span></span>        | <span data-ttu-id="bbb83-125">Code de la langue du menu</span><span class="sxs-lookup"><span data-stu-id="bbb83-125">Menu language code</span></span>              |
| <span data-ttu-id="bbb83-126">1</span><span class="sxs-lookup"><span data-stu-id="bbb83-126">1</span></span>        | <span data-ttu-id="bbb83-127">Numéro de flux audio</span><span class="sxs-lookup"><span data-stu-id="bbb83-127">Audio stream number</span></span>             |
| <span data-ttu-id="bbb83-128">2</span><span class="sxs-lookup"><span data-stu-id="bbb83-128">2</span></span>        | <span data-ttu-id="bbb83-129">Numéro de flux de sous-image</span><span class="sxs-lookup"><span data-stu-id="bbb83-129">Subpicture stream number</span></span>        |
| <span data-ttu-id="bbb83-130">3</span><span class="sxs-lookup"><span data-stu-id="bbb83-130">3</span></span>        | <span data-ttu-id="bbb83-131">Nombre actuel d’angles</span><span class="sxs-lookup"><span data-stu-id="bbb83-131">Current angle number</span></span>            |
| <span data-ttu-id="bbb83-132">4</span><span class="sxs-lookup"><span data-stu-id="bbb83-132">4</span></span>        | <span data-ttu-id="bbb83-133">Numéro de titre actuel</span><span class="sxs-lookup"><span data-stu-id="bbb83-133">Current title number</span></span>            |
| <span data-ttu-id="bbb83-134">5</span><span class="sxs-lookup"><span data-stu-id="bbb83-134">5</span></span>        | <span data-ttu-id="bbb83-135">Numéro de titre</span><span class="sxs-lookup"><span data-stu-id="bbb83-135">Title number</span></span>                    |
| <span data-ttu-id="bbb83-136">6</span><span class="sxs-lookup"><span data-stu-id="bbb83-136">6</span></span>        | <span data-ttu-id="bbb83-137">Nombre de PGC</span><span class="sxs-lookup"><span data-stu-id="bbb83-137">PGC number</span></span>                      |
| <span data-ttu-id="bbb83-138">7</span><span class="sxs-lookup"><span data-stu-id="bbb83-138">7</span></span>        | <span data-ttu-id="bbb83-139">Numéro du chapitre actuel (PTT)</span><span class="sxs-lookup"><span data-stu-id="bbb83-139">Current chapter number (PTT)</span></span>    |
| <span data-ttu-id="bbb83-140">8</span><span class="sxs-lookup"><span data-stu-id="bbb83-140">8</span></span>        | <span data-ttu-id="bbb83-141">Numéro du bouton mis en surbrillance</span><span class="sxs-lookup"><span data-stu-id="bbb83-141">Highlighted button number</span></span>       |
| <span data-ttu-id="bbb83-142">9</span><span class="sxs-lookup"><span data-stu-id="bbb83-142">9</span></span>        | <span data-ttu-id="bbb83-143">Minuteur de navigation</span><span class="sxs-lookup"><span data-stu-id="bbb83-143">Navigation timer</span></span>                |
| <span data-ttu-id="bbb83-144">10</span><span class="sxs-lookup"><span data-stu-id="bbb83-144">10</span></span>       | <span data-ttu-id="bbb83-145">Jump pour le point de vue de la navigation.</span><span class="sxs-lookup"><span data-stu-id="bbb83-145">PGC jump for nav.</span></span> <span data-ttu-id="bbb83-146">minuterie (Timer)</span><span class="sxs-lookup"><span data-stu-id="bbb83-146">timer</span></span>         |
| <span data-ttu-id="bbb83-147">11</span><span class="sxs-lookup"><span data-stu-id="bbb83-147">11</span></span>       | <span data-ttu-id="bbb83-148">Mode de présentation audio karaoké</span><span class="sxs-lookup"><span data-stu-id="bbb83-148">Karaoke audio presentation mode</span></span> |
| <span data-ttu-id="bbb83-149">12</span><span class="sxs-lookup"><span data-stu-id="bbb83-149">12</span></span>       | <span data-ttu-id="bbb83-150">Code pays/région PML</span><span class="sxs-lookup"><span data-stu-id="bbb83-150">PML country/region code</span></span>         |
| <span data-ttu-id="bbb83-151">13</span><span class="sxs-lookup"><span data-stu-id="bbb83-151">13</span></span>       | <span data-ttu-id="bbb83-152">PML</span><span class="sxs-lookup"><span data-stu-id="bbb83-152">PML</span></span>                             |
| <span data-ttu-id="bbb83-153">14</span><span class="sxs-lookup"><span data-stu-id="bbb83-153">14</span></span>       | <span data-ttu-id="bbb83-154">Paramètre vidéo</span><span class="sxs-lookup"><span data-stu-id="bbb83-154">Video setting</span></span>                   |
| <span data-ttu-id="bbb83-155">15</span><span class="sxs-lookup"><span data-stu-id="bbb83-155">15</span></span>       | <span data-ttu-id="bbb83-156">Fonctionnalité audio</span><span class="sxs-lookup"><span data-stu-id="bbb83-156">Audio capability</span></span>                |
| <span data-ttu-id="bbb83-157">16</span><span class="sxs-lookup"><span data-stu-id="bbb83-157">16</span></span>       | <span data-ttu-id="bbb83-158">Langue audio</span><span class="sxs-lookup"><span data-stu-id="bbb83-158">Audio language</span></span>                  |
| <span data-ttu-id="bbb83-159">17</span><span class="sxs-lookup"><span data-stu-id="bbb83-159">17</span></span>       | <span data-ttu-id="bbb83-160">Extension de langage audio</span><span class="sxs-lookup"><span data-stu-id="bbb83-160">Audio language extension</span></span>        |
| <span data-ttu-id="bbb83-161">18</span><span class="sxs-lookup"><span data-stu-id="bbb83-161">18</span></span>       | <span data-ttu-id="bbb83-162">Langue de la sous-image</span><span class="sxs-lookup"><span data-stu-id="bbb83-162">Subpicture language</span></span>             |
| <span data-ttu-id="bbb83-163">19</span><span class="sxs-lookup"><span data-stu-id="bbb83-163">19</span></span>       | <span data-ttu-id="bbb83-164">Extension du langage de sous-image</span><span class="sxs-lookup"><span data-stu-id="bbb83-164">Subpicture language extension</span></span>   |
| <span data-ttu-id="bbb83-165">20</span><span class="sxs-lookup"><span data-stu-id="bbb83-165">20</span></span>       | <span data-ttu-id="bbb83-166">Code de la région du joueur</span><span class="sxs-lookup"><span data-stu-id="bbb83-166">Player region code</span></span>              |
| <span data-ttu-id="bbb83-167">21</span><span class="sxs-lookup"><span data-stu-id="bbb83-167">21</span></span>       | <span data-ttu-id="bbb83-168">Réservé</span><span class="sxs-lookup"><span data-stu-id="bbb83-168">Reserved</span></span>                        |
| <span data-ttu-id="bbb83-169">22</span><span class="sxs-lookup"><span data-stu-id="bbb83-169">22</span></span>       | <span data-ttu-id="bbb83-170">Réservé</span><span class="sxs-lookup"><span data-stu-id="bbb83-170">Reserved</span></span>                        |
| <span data-ttu-id="bbb83-171">23</span><span class="sxs-lookup"><span data-stu-id="bbb83-171">23</span></span>       | <span data-ttu-id="bbb83-172">Réservé</span><span class="sxs-lookup"><span data-stu-id="bbb83-172">Reserved</span></span>                        |



 

## <a name="see-also"></a><span data-ttu-id="bbb83-173">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bbb83-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbb83-174">**GetGPRM**</span><span class="sxs-lookup"><span data-stu-id="bbb83-174">**GetGPRM**</span></span>](getgprm-method.md)
</dt> <dt>

[<span data-ttu-id="bbb83-175">**SetGPRM**</span><span class="sxs-lookup"><span data-stu-id="bbb83-175">**SetGPRM**</span></span>](setgprm-method.md)
</dt> </dl>

 

 



