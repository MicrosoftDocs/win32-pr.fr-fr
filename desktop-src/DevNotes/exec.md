---
description: HKLM \\ Software \\ Microsoft \\ Internet Explorer \\ extensions \\ {e2e2dd38-d088-4134-82b7-f2ba38496583}.
ms.assetid: a0d9e959-d8fd-4546-9529-1dc42fa0bdd6
title: Exec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2711b2c8882f9af12de2f060810ccd4219faa5ec
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748757"
---
# <a name="exec"></a><span data-ttu-id="28c81-103">Exec</span><span class="sxs-lookup"><span data-stu-id="28c81-103">Exec</span></span>

<span data-ttu-id="28c81-104">**HKLM \\ Software \\ Microsoft \\ Internet Explorer \\ extensions \\ {e2e2dd38-d088-4134-82b7-f2ba38496583}**</span><span class="sxs-lookup"><span data-stu-id="28c81-104">**HKLM\\Software\\Microsoft\\Internet Explorer\\Extensions\\{e2e2dd38-d088-4134-82b7-f2ba38496583}**</span></span>



| <span data-ttu-id="28c81-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="28c81-105">Data type</span></span> | <span data-ttu-id="28c81-106">Plage</span><span class="sxs-lookup"><span data-stu-id="28c81-106">Range</span></span>                    | <span data-ttu-id="28c81-107">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="28c81-107">Default value</span></span> |
|-----------|--------------------------|---------------|
| <span data-ttu-id="28c81-108">SZ de REG \_</span><span class="sxs-lookup"><span data-stu-id="28c81-108">REG\_SZ</span></span>   | <span data-ttu-id="28c81-109">*Chemin de l’exécutable*</span><span class="sxs-lookup"><span data-stu-id="28c81-109">*Path to the executable*</span></span> |               |



 

## <a name="browser-integration-steps"></a><span data-ttu-id="28c81-110">Étapes d’intégration du navigateur</span><span class="sxs-lookup"><span data-stu-id="28c81-110">Browser Integration Steps</span></span>

1.  <span data-ttu-id="28c81-111">Utilisez la fonction [**RegOpenKeyEx**](/windows/win32/api/winreg/nf-winreg-regopenkeyexa) pour déterminer si le diagnostic réseau est installé.</span><span class="sxs-lookup"><span data-stu-id="28c81-111">Use the [**RegOpenKeyEx**](/windows/win32/api/winreg/nf-winreg-regopenkeyexa) function to determine whether the Network Diagnostic is installed.</span></span> <span data-ttu-id="28c81-112">S’il est installé, la clé **{e2e2dd38-d088-4134-82b7-f2ba38496583}** est présente.</span><span class="sxs-lookup"><span data-stu-id="28c81-112">If it is installed, the **{e2e2dd38-d088-4134-82b7-f2ba38496583}** key is present.</span></span>
2.  <span data-ttu-id="28c81-113">Utilisez la fonction [**RegQueryValueEx**](/windows/win32/api/winreg/nf-winreg-regqueryvalueexa) pour récupérer le chemin d’accès du fichier exécutable de diagnostics du réseau à partir de l’entrée **Exec** .</span><span class="sxs-lookup"><span data-stu-id="28c81-113">Use the [**RegQueryValueEx**](/windows/win32/api/winreg/nf-winreg-regqueryvalueexa) function to retrieve the path of the Network Diagnostic executable file from the **Exec** entry.</span></span>
3.  <span data-ttu-id="28c81-114">Affichez la page nouvelle erreur si le diagnostic est installé sur le système.</span><span class="sxs-lookup"><span data-stu-id="28c81-114">Display the new error page if the diagnostic is installed on the system.</span></span>
4.  <span data-ttu-id="28c81-115">Créez une extension de navigateur qui crée un élément de barre d’outils standard si le diagnostic est installé sur le système.</span><span class="sxs-lookup"><span data-stu-id="28c81-115">Create a browser extension that creates a standard toolbar item if the diagnostic is installed on the system.</span></span>
5.  <span data-ttu-id="28c81-116">Exécutez l’exécutable Diagnostics du réseau à l’aide du chemin d’accès récupéré à l’étape 2.</span><span class="sxs-lookup"><span data-stu-id="28c81-116">Execute the Network Diagnostic executable using the path retrieved in step 2.</span></span>

## <a name="related-topics"></a><span data-ttu-id="28c81-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="28c81-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28c81-118">Vue d’ensemble des fonctionnalités des outils de diagnostic réseau</span><span class="sxs-lookup"><span data-stu-id="28c81-118">Network Diagnostics Tools Feature Overview</span></span>](https://www.microsoft.com/technet/prodtechnol/winxppro/maintain/netdiag.mspx)
</dt> </dl>

 

 
