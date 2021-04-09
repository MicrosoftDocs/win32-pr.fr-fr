---
description: Une installation d’administration crée une image source d’une application ou d’un produit sur un réseau.
ms.assetid: 40755461-317f-4764-aaa2-6b8471d52f55
title: Application de petites mises à jour en corrigeant une image administrative
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dad22d91e101d79d2bf6ecc0efc8ea9358eda2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951782"
---
# <a name="applying-small-updates-by-patching-an-administrative-image"></a><span data-ttu-id="d3776-103">Application de petites mises à jour en corrigeant une image administrative</span><span class="sxs-lookup"><span data-stu-id="d3776-103">Applying Small Updates by Patching an Administrative Image</span></span>

<span data-ttu-id="d3776-104">Une [installation d’administration](administrative-installation.md) crée une image source d’une application ou d’un produit sur un réseau.</span><span class="sxs-lookup"><span data-stu-id="d3776-104">An [administrative installation](administrative-installation.md) creates a source image of an application or product on a network.</span></span> <span data-ttu-id="d3776-105">Les utilisateurs d’un groupe de travail qui ont accès à cette image administrative peuvent installer le produit à partir de cette source.</span><span class="sxs-lookup"><span data-stu-id="d3776-105">Users in a workgroup who have access to this administrative image can install the product from this source.</span></span> <span data-ttu-id="d3776-106">La mise à jour de l’application pour ce groupe de travail s’effectue en deux étapes :</span><span class="sxs-lookup"><span data-stu-id="d3776-106">Updating the application for this workgroup is done in two steps:</span></span>

-   <span data-ttu-id="d3776-107">Tout d’abord, le correctif de mise à jour de petite taille peut être appliqué à l’image administrative.</span><span class="sxs-lookup"><span data-stu-id="d3776-107">First, the small update patch can be applied to the administrative image.</span></span>
-   <span data-ttu-id="d3776-108">Deuxièmement, les modifications apportées à la petite mise à jour doivent être propagées aux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="d3776-108">Second, the changes in the small update need to be propagated to the users.</span></span>

<span data-ttu-id="d3776-109">**Pour appliquer un correctif de mise à jour de petite taille à une image administrative**</span><span class="sxs-lookup"><span data-stu-id="d3776-109">**To apply a small update patch to an administrative image**</span></span>

1.  <span data-ttu-id="d3776-110">Obtenez la petite mise à jour sous la forme d’un [package de correctifs](patch-packages.md).</span><span class="sxs-lookup"><span data-stu-id="d3776-110">Obtain the small update in the form of a [patch package](patch-packages.md).</span></span> <span data-ttu-id="d3776-111">Par exemple, la petite mise à jour nommée patch. msp.</span><span class="sxs-lookup"><span data-stu-id="d3776-111">For example, the small update named Patch.msp.</span></span>
2.  <span data-ttu-id="d3776-112">Obtenez le chemin d’accès à l’image administrative.</span><span class="sxs-lookup"><span data-stu-id="d3776-112">Obtain the path to the administrative image.</span></span>
3.  <span data-ttu-id="d3776-113">À partir de la ligne de commande, utilisez :</span><span class="sxs-lookup"><span data-stu-id="d3776-113">From the command line use:</span></span>

    <span data-ttu-id="d3776-114">chemin d’accès **msiexec/a** *\[ au fichier \] image d’administration. msi* **/p** *patch. msp*</span><span class="sxs-lookup"><span data-stu-id="d3776-114">**msiexec /a** *\[path to administrative image .msi file\]* **/p** *patch.msp*</span></span>

4.  <span data-ttu-id="d3776-115">Cela met à jour les fichiers d’application et le fichier. msi de l’image administrative.</span><span class="sxs-lookup"><span data-stu-id="d3776-115">This updates the application files and the .msi file of the administrative image.</span></span> <span data-ttu-id="d3776-116">Pour obtenir la liste des options qui peuvent être utilisées avec Msiexec.exe, consultez [options de ligne de commande](command-line-options.md).</span><span class="sxs-lookup"><span data-stu-id="d3776-116">For a list of the options that can be used with Msiexec.exe, see [Command Line Options](command-line-options.md).</span></span> <span data-ttu-id="d3776-117">Windows Installer détermine automatiquement si l’image administrative utilise des noms de fichiers courts et définit la propriété [**SHORTFILENAMES**](shortfilenames.md) .</span><span class="sxs-lookup"><span data-stu-id="d3776-117">Windows Installer automatically determines whether the administrative image is using short file names and sets the [**SHORTFILENAMES**](shortfilenames.md) property.</span></span>
5.  <span data-ttu-id="d3776-118">L’image administrative résultante est la même que celle produite par une installation d’administration à l’aide d’un CD-ROM du produit complet qui comprend la mise à jour.</span><span class="sxs-lookup"><span data-stu-id="d3776-118">The resulting administrative image is the same as that produced by an administrative installation using a full product CD-ROM that includes the update.</span></span> <span data-ttu-id="d3776-119">Lorsque de nouveaux utilisateurs installent l’application à partir de cette source, ils reçoivent l’application mise à jour.</span><span class="sxs-lookup"><span data-stu-id="d3776-119">When new users install the application from this source they receive the updated application.</span></span>

<span data-ttu-id="d3776-120">**Pour propager la petite mise à jour au groupe de travail**</span><span class="sxs-lookup"><span data-stu-id="d3776-120">**To propagate the small update to the workgroup**</span></span>

-   <span data-ttu-id="d3776-121">Les membres du groupe de travail obtiennent les modifications en réinstallant l’application à partir de l’image administrative à l’aide de la procédure décrite dans [application de petites mises à jour en réinstallant le produit](applying-small-updates-by-reinstalling-the-product.md).</span><span class="sxs-lookup"><span data-stu-id="d3776-121">Members of the workgroup obtain the changes by reinstalling the application from the administrative image using the procedure described in [Applying Small Updates by Reinstalling the Product](applying-small-updates-by-reinstalling-the-product.md).</span></span>

 

 



