---
description: Si cette stratégie système par ordinateur est définie sur une valeur supérieure à 0, Windows Installer enregistre les anciennes versions des fichiers dans un cache lorsqu’un correctif est appliqué à une application.
ms.assetid: 986cd521-6907-420d-a2e9-5e0da0069834
title: MaxPatchCacheSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8d9930f4a52d3ea0126a19d4dfadae359321f56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485264"
---
# <a name="maxpatchcachesize"></a><span data-ttu-id="673df-103">MaxPatchCacheSize</span><span class="sxs-lookup"><span data-stu-id="673df-103">MaxPatchCacheSize</span></span>

<span data-ttu-id="673df-104">Si cette [stratégie système](system-policy.md) par ordinateur est définie sur une valeur supérieure à 0, Windows Installer enregistre les anciennes versions des fichiers dans un cache lorsqu’un correctif est appliqué à une application.</span><span class="sxs-lookup"><span data-stu-id="673df-104">If this per-machine [system policy](system-policy.md) is set to a value greater than 0, Windows Installer saves older versions of files in a cache when a patch is applied to an application.</span></span> <span data-ttu-id="673df-105">La mise en cache peut augmenter les performances des installations futures qui, sinon, doivent obtenir les anciens fichiers à partir d’une source d’application d’origine.</span><span class="sxs-lookup"><span data-stu-id="673df-105">Caching can increase the performance of future installations that otherwise need to obtain the old files from a original application source.</span></span>

<span data-ttu-id="673df-106">La valeur de la stratégie MaxPatchCacheSize est le pourcentage maximal d’espace disque que le programme d’installation peut utiliser pour le cache des anciens fichiers.</span><span class="sxs-lookup"><span data-stu-id="673df-106">The value of the MaxPatchCacheSize policy is the maximum percentage of disk space that the installer can use for the cache of old files.</span></span> <span data-ttu-id="673df-107">Par exemple, la valeur 20 ne spécifie pas plus de 20% d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="673df-107">For example, a value of 20 specifies no more than 20% be used.</span></span> <span data-ttu-id="673df-108">Si la taille totale du cache atteint le pourcentage d’espace disque spécifié, aucun fichier supplémentaire n’est enregistré dans le cache.</span><span class="sxs-lookup"><span data-stu-id="673df-108">If the total size of the cache reaches the specified percentage of disk space, no additional files are saved to the cache.</span></span> <span data-ttu-id="673df-109">La stratégie n’affecte pas les fichiers qui ont déjà été enregistrés.</span><span class="sxs-lookup"><span data-stu-id="673df-109">The policy does not affect files that have already been saved.</span></span>

<span data-ttu-id="673df-110">Si la valeur de la stratégie MaxPatchCacheSize est définie sur 0, aucun fichier supplémentaire n’est enregistré.</span><span class="sxs-lookup"><span data-stu-id="673df-110">If the value of the MaxPatchCacheSize policy is set to 0, no additional files are saved.</span></span>

<span data-ttu-id="673df-111">Si la stratégie MaxPatchCacheSize n’est pas définie, la valeur par défaut est 10 et un maximum de 10% de l’espace disque peut être utilisé pour enregistrer les anciens fichiers.</span><span class="sxs-lookup"><span data-stu-id="673df-111">If the MaxPatchCacheSize policy is not set, the default value is 10 and a maximum of 10% of the disk space can be used to save old files.</span></span>

## <a name="registry-key"></a><span data-ttu-id="673df-112">Clé de Registre</span><span class="sxs-lookup"><span data-stu-id="673df-112">Registry Key</span></span>

<span data-ttu-id="673df-113">**HKEY \_ \_** \\ **Stratégies logicielles** de l’ordinateur local \\  \\ **Microsoft** \\ **Windows** \\ **installer**</span><span class="sxs-lookup"><span data-stu-id="673df-113">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="673df-114">Type de données</span><span class="sxs-lookup"><span data-stu-id="673df-114">Data Type</span></span>

<span data-ttu-id="673df-115">**\_valeur DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="673df-115">**REG\_DWORD**</span></span>

## <a name="related-topics"></a><span data-ttu-id="673df-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="673df-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="673df-117">Non pris en charge dans Windows Installer 2,0 et versions antérieures</span><span class="sxs-lookup"><span data-stu-id="673df-117">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



