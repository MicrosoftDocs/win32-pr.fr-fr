---
description: ICEM13 vérifie que le module de fusion ne contient pas d’assemblys de stratégie et de configuration d’éditeur.
ms.assetid: 1281ee21-a154-4275-a9e6-6e92fff548ed
title: ICEM13
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3286906cf162f24dce7105835544c3a387993ac6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864405"
---
# <a name="icem13"></a><span data-ttu-id="17d1f-103">ICEM13</span><span class="sxs-lookup"><span data-stu-id="17d1f-103">ICEM13</span></span>

<span data-ttu-id="17d1f-104">ICEM13 vérifie que le module de fusion ne contient pas d’assemblys de stratégie et de configuration d’éditeur.</span><span class="sxs-lookup"><span data-stu-id="17d1f-104">ICEM13 verifies that the merge module does not contain publisher policy and configuration assemblies.</span></span> <span data-ttu-id="17d1f-105">Les assemblys de stratégie et de configuration d’éditeur ne doivent pas être inclus dans les modules de fusion destinés à la redistribution, car cela peut affecter d’autres applications sur l’ordinateur d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="17d1f-105">Publisher policy and configuration assemblies should not be included in merge modules intended for redistribution because this can affect other applications on a user's computer.</span></span>

<span data-ttu-id="17d1f-106">Ce ICEM est disponible dans le fichier Mergemod. CUB fourni dans le kit de développement logiciel (SDK) Windows Installer 2,0 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="17d1f-106">This ICEM is available in the Mergemod.cub file provided in the Windows Installer 2.0 SDK and later.</span></span> <span data-ttu-id="17d1f-107">Pour plus d’informations, consultez [SDK Windows Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="17d1f-107">For details, see [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

## <a name="result"></a><span data-ttu-id="17d1f-108">Résultats</span><span class="sxs-lookup"><span data-stu-id="17d1f-108">Result</span></span>

<span data-ttu-id="17d1f-109">ICEM13 publie un message d’avertissement s’il trouve un composant spécifié dans le champ composant de la [table MsiAssembly](msiassembly-table.md) du module de fusion qui est une stratégie ou un assembly de configuration d’éditeur.</span><span class="sxs-lookup"><span data-stu-id="17d1f-109">ICEM13 posts a warning message if it finds a component specified in the Component field of the merge module's [MsiAssembly Table](msiassembly-table.md) that is a publisher policy or configuration assembly.</span></span>

## <a name="example"></a><span data-ttu-id="17d1f-110">Exemple</span><span class="sxs-lookup"><span data-stu-id="17d1f-110">Example</span></span>

<span data-ttu-id="17d1f-111">ICEM13 publie le message d’avertissement suivant s’il trouve une ligne de la [table MsiAssembly](msiassembly-table.md) avec le composant « \[ 1 \] » spécifié dans le champ de composant qui est une stratégie d’éditeur ou un assembly de configuration qui a été inclus dans le module de fusion.</span><span class="sxs-lookup"><span data-stu-id="17d1f-111">ICEM13 posts the following warning message if it finds a row in the [MsiAssembly Table](msiassembly-table.md) with a component '\[1\]' specified in the Component field that is a publisher policy or configuration assembly that has been included in the merge module.</span></span>

``` syntax
This entry Component_=`[1]` in MsiAssembly Table is a Policy/Configuration Assembly. A Publisher Policy/Configuration assembly should not be redistributed with a merge module. Policy/Configuration may impact other applications and should only be installed with products.
```

<span data-ttu-id="17d1f-112">Il est possible d’installer des assemblys de stratégie et de configuration d’éditeur à l’aide de la Windows Installer, il n’est pas recommandé de redistribuer ces assemblys dans des modules de fusion.</span><span class="sxs-lookup"><span data-stu-id="17d1f-112">It is possible to install publisher policy and configuration assemblies using the Windows Installer, it is not recommended that these assemblies be redistributed in merge modules.</span></span>

## <a name="related-topics"></a><span data-ttu-id="17d1f-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="17d1f-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="17d1f-114">Référence ICE du module de fusion</span><span class="sxs-lookup"><span data-stu-id="17d1f-114">Merge Module ICE Reference</span></span>](merge-module-ice-reference.md)
</dt> </dl>

 

 



