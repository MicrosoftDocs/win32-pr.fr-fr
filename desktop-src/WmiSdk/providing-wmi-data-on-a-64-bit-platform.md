---
description: Les scripts et les applications écrits pour les systèmes d’exploitation 32 bits doivent continuer à fonctionner correctement.
ms.assetid: b437b9ed-b9e4-4fc5-9b86-0eb77bb41b8e
ms.tgt_platform: multiple
title: Fourniture de données WMI sur une plateforme 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec1d6b348c16765014c4eb6988b64976ba3f11a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527747"
---
# <a name="providing-wmi-data-on-a-64-bit-platform"></a><span data-ttu-id="4b4d6-103">Fourniture de données WMI sur une plateforme 64 bits</span><span class="sxs-lookup"><span data-stu-id="4b4d6-103">Providing WMI Data on a 64-bit Platform</span></span>

<span data-ttu-id="4b4d6-104">Les scripts et les applications écrits pour les systèmes d’exploitation 32 bits doivent continuer à fonctionner correctement.</span><span class="sxs-lookup"><span data-stu-id="4b4d6-104">Scripts and applications written for 32-bit operating systems should continue to run properly.</span></span> <span data-ttu-id="4b4d6-105">Si vous disposez déjà d’un fournisseur 32 bits, vous pouvez évaluer si vous devez écrire une version 64 bits pour une opération côte à côte.</span><span class="sxs-lookup"><span data-stu-id="4b4d6-105">If you have an existing 32-bit provider, you can evaluate whether you need to write a 64-bit version for side-by-side operation.</span></span> <span data-ttu-id="4b4d6-106">En règle générale, les deux versions ne sont pas nécessaires et la version 64 bits peut traiter à la fois les clients locaux et distants 32 bits et 64 bits.</span><span class="sxs-lookup"><span data-stu-id="4b4d6-106">Generally, both versions are not necessary and the 64-bit version can service both 32-bit and 64-bit local or remote clients.</span></span> <span data-ttu-id="4b4d6-107">Toutefois, pour le mode de compatibilité des applications 32 bits, utilisez votre fournisseur WMI 32 bits existant sur un système 64 bits qui s’exécute en mode WOW64 32 bits.</span><span class="sxs-lookup"><span data-stu-id="4b4d6-107">However, for 32-bit application compatibility mode, use your existing 32-bit WMI provider on a 64-bit system that runs in the 32-bit WOW64 mode.</span></span>

<span data-ttu-id="4b4d6-108">Dans de rares cas, les fournisseurs 32 bits et 64 bits doivent s’exécuter côte à côte sur des systèmes 64 bits.</span><span class="sxs-lookup"><span data-stu-id="4b4d6-108">In rare situations, both the 32-bit and 64-bit providers must run side-by-side on 64-bit systems.</span></span> <span data-ttu-id="4b4d6-109">Dans ce cas, la version appropriée du fournisseur qui est chargée varie selon que l’appelant est 32-bit ou 64 bits et local ou distant.</span><span class="sxs-lookup"><span data-stu-id="4b4d6-109">In this case, the appropriate version of provider that is loaded depends on whether the caller is 32-bit or 64-bit and local or remote.</span></span> <span data-ttu-id="4b4d6-110">Un appelant qui utilise les indicateurs de contexte de l’objet de connexion, **\_ \_ ProviderArchitecture** et **\_ \_ RequiredArchitecture**, peut demander à ce que WMI charge un fournisseur non défini par défaut.</span><span class="sxs-lookup"><span data-stu-id="4b4d6-110">A caller using the connection object context flags, **\_\_ProviderArchitecture** and **\_\_RequiredArchitecture**, can request that WMI load a nondefault provider.</span></span> <span data-ttu-id="4b4d6-111">Pour plus d’informations, consultez [obtention et fourniture de données sur un ordinateur 64 bits](getting-and-providing-data-on-a-64-bit-computer.md).</span><span class="sxs-lookup"><span data-stu-id="4b4d6-111">For more information, see [Getting and Providing Data on a 64-bit Computer](getting-and-providing-data-on-a-64-bit-computer.md).</span></span>

<span data-ttu-id="4b4d6-112">Dans le cas rare où vous devez exécuter les fournisseurs 32 bits et 64 bits côte à côte, vous devez vous assurer que les scénarios d’installation et de désinstallation sont gérés avec précaution.</span><span class="sxs-lookup"><span data-stu-id="4b4d6-112">In the unusual case that you must run both the 32-bit and 64-bit providers side-by-side, then you must ensure that install and uninstall scenarios are handled carefully.</span></span> <span data-ttu-id="4b4d6-113">Cela est dû au fait que WMI n’a qu’un seul [*référentiel*](gloss-w.md) et que les versions 32 bits et 64 bits de [**mofcomp.exe**](mofcomp.md) placent les données dans le même référentiel ; Il n’existe aucune distinction entre un fichier. mof 32 bits ou 64.</span><span class="sxs-lookup"><span data-stu-id="4b4d6-113">This is because WMI has only one [*repository*](gloss-w.md) and both the 32-bit and 64-bit versions of [**mofcomp.exe**](mofcomp.md) put the data in the same repository; there is no distinction between a 32-bit or a 64-bit .mof file.</span></span> <span data-ttu-id="4b4d6-114">La réinstallation d’une version du fournisseur n’a pas d’impact : les fichiers. mof seront compilés et les classes stockées dans le référentiel.</span><span class="sxs-lookup"><span data-stu-id="4b4d6-114">Reinstalling one version of the provider will not hurt: the .mof files will be compiled and the classes stored in the repository.</span></span> <span data-ttu-id="4b4d6-115">Toutefois, une deuxième désinstallation qui supprime un espace de noms peut interférer avec le fonctionnement de l’autre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="4b4d6-115">However, a second uninstall that deletes a namespace can interfere with the operation of the other provider.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4b4d6-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4b4d6-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4b4d6-117">Obtention et fourniture de données sur un ordinateur 64 bits</span><span class="sxs-lookup"><span data-stu-id="4b4d6-117">Getting and Providing Data on a 64-bit Computer</span></span>](getting-and-providing-data-on-a-64-bit-computer.md)
</dt> <dt>

[<span data-ttu-id="4b4d6-118">Demande de données WMI sur une plateforme 64 bits</span><span class="sxs-lookup"><span data-stu-id="4b4d6-118">Requesting WMI Data on a 64-bit Platform</span></span>](requesting-wmi-data-on-a-64-bit-platform.md)
</dt> <dt>

[<span data-ttu-id="4b4d6-119">Fourniture de données à WMI</span><span class="sxs-lookup"><span data-stu-id="4b4d6-119">Providing Data to WMI</span></span>](providing-data-to-wmi.md)
</dt> </dl>

 

 



