---
title: Paramètre de registre d’acquisition en mode silencieux
description: Paramètre de registre d’acquisition en mode silencieux
ms.assetid: 50e0b27e-ddf8-441f-adcd-d88d36f3edaf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a00bbb6d930cb137ed12ffbcb05af31cee3c99c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106510218"
---
# <a name="silent-acquisition-registry-setting"></a><span data-ttu-id="78146-103">Paramètre de registre d’acquisition en mode silencieux</span><span class="sxs-lookup"><span data-stu-id="78146-103">Silent Acquisition Registry Setting</span></span>

<span data-ttu-id="78146-104">Le lecteur Microsoft Windows Media utilise la valeur de Registre suivante pour déterminer s’il faut activer l’acquisition en mode silencieux, un État dans lequel le lecteur télécharge automatiquement les droits d’utilisation lorsque l’utilisateur lit ou synchronise le contenu protégé.</span><span class="sxs-lookup"><span data-stu-id="78146-104">Microsoft Windows Media Player uses the following registry value to determine whether to enable silent acquisition, a state in which the player downloads usage rights automatically when the user plays or syncs protected content.</span></span>

<span data-ttu-id="78146-105">**HKEY \_ Logiciel de l' \_ ordinateur local** \\  \\ **Microsoft** \\ **MediaPlayer** \\ **Préférences** \\ **SilentAcquisition**</span><span class="sxs-lookup"><span data-stu-id="78146-105">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**MediaPlayer**\\**Preferences**\\**SilentAcquisition**</span></span>

<span data-ttu-id="78146-106">La valeur SilentAcquisition se présente sous la forme suivante :</span><span class="sxs-lookup"><span data-stu-id="78146-106">The SilentAcquisition value has the following form:</span></span>



| <span data-ttu-id="78146-107">Nom</span><span class="sxs-lookup"><span data-stu-id="78146-107">Name</span></span>              | <span data-ttu-id="78146-108">Type</span><span class="sxs-lookup"><span data-stu-id="78146-108">Type</span></span>           | <span data-ttu-id="78146-109">Description</span><span class="sxs-lookup"><span data-stu-id="78146-109">Description</span></span>                                                                                                       |
|-------------------|----------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78146-110">SilentAcquisition</span><span class="sxs-lookup"><span data-stu-id="78146-110">SilentAcquisition</span></span> | <span data-ttu-id="78146-111">**\_valeur DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="78146-111">**REG\_DWORD**</span></span> | <span data-ttu-id="78146-112">Définissez cette valeur sur 1 pour activer l’acquisition en mode silencieux ou sur 0 pour désactiver l’acquisition en mode silencieux.</span><span class="sxs-lookup"><span data-stu-id="78146-112">Set this value to 1 to enable silent acquisition, or set it to 0 to disable silent acquisition.</span></span> <span data-ttu-id="78146-113">La valeur par défaut est 1.</span><span class="sxs-lookup"><span data-stu-id="78146-113">The default is 1.</span></span> |



 

<span data-ttu-id="78146-114">Pour spécifier une valeur, l’utilisateur peut démarrer le lecteur Windows Media, ouvrir la boîte de dialogue **options** , cliquer sur l’onglet **confidentialité** , puis activer ou désactiver la case à cocher **Télécharger automatiquement les droits d’utilisation lors de la lecture ou de la synchronisation d’un fichier** .</span><span class="sxs-lookup"><span data-stu-id="78146-114">To specify a value, the user can start Windows Media Player, open the **Options** dialog box, click the **Privacy** tab, and then select or clear the **Download usage rights automatically when I play or sync a file** check box.</span></span> <span data-ttu-id="78146-115">La sélection de cette case à cocher affecte la valeur 1 à SilentAcquisition. la désactivation de la case à cocher lui affecte la valeur 0.</span><span class="sxs-lookup"><span data-stu-id="78146-115">Selecting this check box sets SilentAcquisition to 1; clearing the check box sets it to 0.</span></span>

## <a name="related-topics"></a><span data-ttu-id="78146-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="78146-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="78146-117">**Paramètres du Registre**</span><span class="sxs-lookup"><span data-stu-id="78146-117">**Registry Settings**</span></span>](registry-settings.md)
</dt> </dl>

 

 




