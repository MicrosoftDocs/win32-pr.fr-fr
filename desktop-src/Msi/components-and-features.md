---
description: Le Windows Installer organise une installation autour des concepts des composants et des fonctionnalités.
ms.assetid: c560441e-89c5-4f82-837b-988c3f404d37
title: Composants et fonctionnalités
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7b21241c98fbb701bd6a3ef5869045ef8c46da1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114178"
---
# <a name="components-and-features"></a><span data-ttu-id="4360b-103">Composants et fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="4360b-103">Components and Features</span></span>

<span data-ttu-id="4360b-104">Le Windows Installer organise une installation autour des concepts des composants et des fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="4360b-104">The Windows Installer organizes an installation around the concepts of components and features.</span></span>

<span data-ttu-id="4360b-105">Une fonctionnalité fait partie de la fonctionnalité totale de l’application qu’un utilisateur peut décider d’installer de manière indépendante.</span><span class="sxs-lookup"><span data-stu-id="4360b-105">A feature is a part of the application's total functionality that a user may decide to install independently.</span></span> <span data-ttu-id="4360b-106">Pour plus d’informations, consultez [fonctionnalités de Windows Installer](windows-installer-features.md).</span><span class="sxs-lookup"><span data-stu-id="4360b-106">For more information, see [Windows Installer Features](windows-installer-features.md).</span></span>

<span data-ttu-id="4360b-107">Un composant est une partie de l’application ou du produit à installer.</span><span class="sxs-lookup"><span data-stu-id="4360b-107">A component is a piece of the application or product to be installed.</span></span> <span data-ttu-id="4360b-108">Le programme d’installation installe ou supprime toujours un composant de l’ordinateur d’un utilisateur comme élément cohérent.</span><span class="sxs-lookup"><span data-stu-id="4360b-108">The installer always installs or removes a component from a user's computer as a coherent piece.</span></span> <span data-ttu-id="4360b-109">Les composants sont généralement masqués par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4360b-109">Components are usually hidden from the user.</span></span> <span data-ttu-id="4360b-110">Quand un utilisateur sélectionne une fonctionnalité à installer, le programme d’installation détermine les composants qui doivent être installés pour fournir cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="4360b-110">When a user selects a feature for installation, the installer determines which components must be installed to provide that feature.</span></span> <span data-ttu-id="4360b-111">Pour plus d’informations, consultez [Windows Installer Components](windows-installer-components.md).</span><span class="sxs-lookup"><span data-stu-id="4360b-111">For more information, see [Windows Installer Components](windows-installer-components.md).</span></span>

<span data-ttu-id="4360b-112">Les auteurs des packages d’installation doivent décider comment diviser leur application en fonctionnalités et composants.</span><span class="sxs-lookup"><span data-stu-id="4360b-112">Authors of installation packages need to decide how to divide their application into features and components.</span></span> <span data-ttu-id="4360b-113">La sélection des fonctionnalités est principalement déterminée par les fonctionnalités de l’application du point de vue de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4360b-113">The selection of features is primarily determined by the application's functionality from the user's perspective.</span></span> <span data-ttu-id="4360b-114">Étant donné que les composants doivent être partagés entre les applications, voire entre les produits, il est recommandé que les auteurs suivent une méthode standard pour sélectionner les composants.</span><span class="sxs-lookup"><span data-stu-id="4360b-114">Because components commonly must be shared across applications, or even across products, it is recommended that authors follow a standard method for selecting components.</span></span> <span data-ttu-id="4360b-115">Pour plus d’informations, consultez [Organisation des applications dans des composants](organizing-applications-into-components.md).</span><span class="sxs-lookup"><span data-stu-id="4360b-115">For more information, see [Organizing Applications into Components](organizing-applications-into-components.md).</span></span>

 

 



