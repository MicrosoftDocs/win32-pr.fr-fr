---
description: Si cette stratégie système par utilisateur est définie sur &\# 0034 ; 1&\# 0034 ;, les utilisateurs et les administrateurs exécutant une installation de maintenance d’un produit ne peuvent pas utiliser la boîte de dialogue Parcourir pour parcourir les sources de média, telles que les CD-ROM, pour les sources d’autres produits installables.
ms.assetid: 275a6d43-ecf8-4146-82eb-3b42b25b9a80
title: DisableMedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2ee50abf36225aa96e52332a53f0b2ab36f058c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103953340"
---
# <a name="disablemedia"></a><span data-ttu-id="e24c6-103">DisableMedia</span><span class="sxs-lookup"><span data-stu-id="e24c6-103">DisableMedia</span></span>

<span data-ttu-id="e24c6-104">Si cette [stratégie système](system-policy.md) par utilisateur est définie sur « 1 », les utilisateurs et les administrateurs exécutant une installation de maintenance d’un produit ne peuvent pas utiliser la boîte de dialogue Parcourir pour parcourir les sources de média, telles que les CD-ROM, pour les sources d’autres produits installables.</span><span class="sxs-lookup"><span data-stu-id="e24c6-104">If this per-user [system policy](system-policy.md) is set to "1", users and administrators running a maintenance installation of one product are prevented from using the Browse Dialog to browse media sources, such as CD-ROM, for the sources of other installable products.</span></span> <span data-ttu-id="e24c6-105">La recherche d’autres produits est empêchée, que l’installation soit effectuée avec des privilèges élevés.</span><span class="sxs-lookup"><span data-stu-id="e24c6-105">Browsing for other products is prevented regardless of whether the installation is done with elevated privileges.</span></span> <span data-ttu-id="e24c6-106">Il est toujours possible pour l’utilisateur de réinstaller le produit à partir d’un support si celui-ci possède une source de média correctement libellée.</span><span class="sxs-lookup"><span data-stu-id="e24c6-106">It is still possible for the user to reinstall the product from media if the user has a correctly labeled media source.</span></span>

## <a name="registry-key"></a><span data-ttu-id="e24c6-107">Clé de Registre</span><span class="sxs-lookup"><span data-stu-id="e24c6-107">Registry Key</span></span>

<span data-ttu-id="e24c6-108">**HKEY \_ \_** \\ **Stratégies logicielles** de l’utilisateur actuel \\  \\ **Microsoft** \\ **Windows** \\ **installer**</span><span class="sxs-lookup"><span data-stu-id="e24c6-108">**HKEY\_CURRENT\_USER**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="e24c6-109">Type de données</span><span class="sxs-lookup"><span data-stu-id="e24c6-109">Data Type</span></span>

<span data-ttu-id="e24c6-110">**\_valeur DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="e24c6-110">**REG\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="e24c6-111">Notes</span><span class="sxs-lookup"><span data-stu-id="e24c6-111">Remarks</span></span>

<span data-ttu-id="e24c6-112">Notez que la propriété [**DISABLEMEDIA**](-disablemedia.md) a un effet différent de la stratégie DISABLEMEDIA.</span><span class="sxs-lookup"><span data-stu-id="e24c6-112">Note that the [**DISABLEMEDIA**](-disablemedia.md) property has a different effect than the DisableMedia policy.</span></span> <span data-ttu-id="e24c6-113">La définition de la stratégie système DisableMedia désactive uniquement la navigation vers les sources multimédias.</span><span class="sxs-lookup"><span data-stu-id="e24c6-113">Setting the DisableMedia system policy, only disables browsing to media sources.</span></span> <span data-ttu-id="e24c6-114">La définition de la propriété **DISABLEMEDIA** empêche le programme d’installation d’inscrire toute source multimédia, telle qu’un CD-ROM, comme source valide pour le produit.</span><span class="sxs-lookup"><span data-stu-id="e24c6-114">Setting the **DISABLEMEDIA** property prevents the installer from registering any media source, such as a CD-ROM, as a valid source for the product.</span></span> <span data-ttu-id="e24c6-115">Toutefois, si la navigation est activée, un utilisateur peut toujours accéder à une source multimédia.</span><span class="sxs-lookup"><span data-stu-id="e24c6-115">If browsing is enabled however, a user may still browse to a media source.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e24c6-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e24c6-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e24c6-117">Résilience source</span><span class="sxs-lookup"><span data-stu-id="e24c6-117">Source Resiliency</span></span>](source-resiliency.md)
</dt> </dl>

 

 



