---
description: Lors de l’installation d’un correctif et d’une ou de plusieurs transformations de personnalisation à une application, le correctif est généralement installé en premier, suivi des transformations de personnalisation.
ms.assetid: 39a58174-fa62-42e3-a0aa-4cc541c2e36b
title: Mise à jour corrective des applications personnalisées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 289685ebc390de750ea9c47ddfae6ef58ec87116
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104319197"
---
# <a name="patching-customized-applications"></a><span data-ttu-id="200dd-103">Mise à jour corrective des applications personnalisées</span><span class="sxs-lookup"><span data-stu-id="200dd-103">Patching Customized Applications</span></span>

<span data-ttu-id="200dd-104">Lors de l’installation d’un correctif et d’une ou de plusieurs transformations de personnalisation à une application, le correctif est généralement installé en premier, suivi des transformations de personnalisation.</span><span class="sxs-lookup"><span data-stu-id="200dd-104">When installing a patch and one or more customization transforms to an application, the patch is typically installed first, followed by the customization transforms.</span></span> <span data-ttu-id="200dd-105">Par défaut, le correctif n’est pas interrompu par l’installation suivante de la personnalisation.</span><span class="sxs-lookup"><span data-stu-id="200dd-105">By design, the patch is not broken by the subsequent installation of the customization.</span></span> <span data-ttu-id="200dd-106">Toutefois, l’installation préalable des transformations, puis du correctif, risque de perturber la personnalisation.</span><span class="sxs-lookup"><span data-stu-id="200dd-106">However, installing the transforms first, and then the patch, may break the customization.</span></span>

<span data-ttu-id="200dd-107">Par exemple, une interruption dans la personnalisation peut se produire lorsqu’un correctif est utilisé pour mettre à jour un produit de la version 1 à la version 2 et qu’une transformation de personnalisation qui fonctionne pour la version 1 ne fonctionne pas pour la version 2.</span><span class="sxs-lookup"><span data-stu-id="200dd-107">For example, a break in the customization could occur when a patch is used to update a product from version 1 to version 2 and a customization transform that works for version 1 does not work for version 2.</span></span> <span data-ttu-id="200dd-108">Dans ce cas, le correctif de mise à jour de version ne peut pas être appliqué à un produit personnalisé sans avoir préalablement désinstallé, puis réinstallé le produit d’origine.</span><span class="sxs-lookup"><span data-stu-id="200dd-108">In this case, the version update patch cannot be applied to a customized product without first uninstalling and then reinstalling the original product.</span></span>

 

 



