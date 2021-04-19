---
description: Il existe plusieurs fonctions qui modifient l’installation des composants et fonctionnalités du produit. La rubrique suivante décrit comment modifier des fonctionnalités et des composants.
ms.assetid: 840656f9-ea85-49e7-8842-f779228c30d6
title: Utilisation des fonctionnalités et des composants
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d579b82dfb312c1588b500d8959fad8a09e44753
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106538687"
---
# <a name="working-with-features-and-components"></a><span data-ttu-id="e68a2-104">Utilisation des fonctionnalités et des composants</span><span class="sxs-lookup"><span data-stu-id="e68a2-104">Working with Features and Components</span></span>

<span data-ttu-id="e68a2-105">Il existe plusieurs fonctions qui modifient l’installation des [composants et fonctionnalités](components-and-features.md)du produit.</span><span class="sxs-lookup"><span data-stu-id="e68a2-105">There are several functions that change the installation of product [components and features](components-and-features.md).</span></span> <span data-ttu-id="e68a2-106">La rubrique suivante décrit comment modifier des fonctionnalités et des composants.</span><span class="sxs-lookup"><span data-stu-id="e68a2-106">The following describes how to change features and components.</span></span>

<span data-ttu-id="e68a2-107">**Pour modifier l’installation de fonctionnalités et de composants**</span><span class="sxs-lookup"><span data-stu-id="e68a2-107">**To change the installation of features and components**</span></span>

1.  <span data-ttu-id="e68a2-108">Définissez le niveau d’installation d’un composant ou d’une fonctionnalité en appelant la fonction [**MsiSetInstallLevel**](/windows/desktop/api/Msiquery/nf-msiquery-msisetinstalllevel) .</span><span class="sxs-lookup"><span data-stu-id="e68a2-108">Set the installation level for a component or feature by calling the [**MsiSetInstallLevel**](/windows/desktop/api/Msiquery/nf-msiquery-msisetinstalllevel) function.</span></span>

    <span data-ttu-id="e68a2-109">Chaque fonctionnalité d’un package se voit attribuer un niveau d’installation dans le [tableau des fonctionnalités](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="e68a2-109">Each feature in a package is assigned an installation level in the [Feature table](feature-table.md).</span></span> <span data-ttu-id="e68a2-110">Si le niveau d’installation d’une fonctionnalité est inférieur au niveau défini par [**MsiSetInstallLevel**](/windows/desktop/api/Msiquery/nf-msiquery-msisetinstalllevel), la fonctionnalité est sélectionnée pour l’installation.</span><span class="sxs-lookup"><span data-stu-id="e68a2-110">If the installation level of a feature is lower than the level set by [**MsiSetInstallLevel**](/windows/desktop/api/Msiquery/nf-msiquery-msisetinstalllevel), the feature is selected for installation.</span></span> <span data-ttu-id="e68a2-111">Une fois **MsiSetInstallLevel** appelé, vous pouvez définir explicitement si une fonctionnalité est installée.</span><span class="sxs-lookup"><span data-stu-id="e68a2-111">After **MsiSetInstallLevel** is called, you can explicitly change whether a feature is installed.</span></span>

2.  <span data-ttu-id="e68a2-112">Déterminez les États disponibles pour une fonctionnalité spécifiée en appelant la fonction [**MsiGetFeatureValidStates**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturevalidstatesa) .</span><span class="sxs-lookup"><span data-stu-id="e68a2-112">Determine which states are available for a specified feature by calling the [**MsiGetFeatureValidStates**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturevalidstatesa) function.</span></span>
3.  <span data-ttu-id="e68a2-113">Obtenez l’espace disque requis pour une fonctionnalité spécifiée et ses fonctionnalités enfants en appelant la fonction [**MsiGetFeatureCost**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturecosta) .</span><span class="sxs-lookup"><span data-stu-id="e68a2-113">Obtain the disk space requirements for a specified feature and its child features by calling the [**MsiGetFeatureCost**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturecosta) function.</span></span>
4.  <span data-ttu-id="e68a2-114">Obtenir l’état actuel d’une fonctionnalité ou d’un composant en appelant la fonction [**MsiGetFeatureState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea) ou la fonction [**MsiGetComponentState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea) .</span><span class="sxs-lookup"><span data-stu-id="e68a2-114">Obtain the current state of a feature or component by calling the [**MsiGetFeatureState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea) function or the [**MsiGetComponentState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea) function.</span></span>
5.  <span data-ttu-id="e68a2-115">Modifiez l’état de la fonctionnalité ou du composant avec la fonction [**MsiSetFeatureState**](/windows/desktop/api/Msiquery/nf-msiquery-msisetfeaturestatea) ou la fonction [**MsiSetComponentState**](/windows/desktop/api/Msiquery/nf-msiquery-msisetcomponentstatea) .</span><span class="sxs-lookup"><span data-stu-id="e68a2-115">Change the state of the feature or component with the [**MsiSetFeatureState**](/windows/desktop/api/Msiquery/nf-msiquery-msisetfeaturestatea) function or the [**MsiSetComponentState**](/windows/desktop/api/Msiquery/nf-msiquery-msisetcomponentstatea) function.</span></span>

 

 



