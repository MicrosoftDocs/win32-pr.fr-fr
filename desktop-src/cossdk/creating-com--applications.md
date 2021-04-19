---
description: Création d’applications COM+
ms.assetid: 32828d4d-aa98-4e6a-b7de-2ec832024517
title: Création d’applications COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e42a4b7ad18dab3f7163f527626322e05671e7be
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515382"
---
# <a name="creating-com-applications"></a><span data-ttu-id="46a5b-103">Création d’applications COM+</span><span class="sxs-lookup"><span data-stu-id="46a5b-103">Creating COM+ Applications</span></span>

<span data-ttu-id="46a5b-104">Cette section décrit comment créer une application COM+ (vide), puis ajouter des composants à cette application.</span><span class="sxs-lookup"><span data-stu-id="46a5b-104">This section describes how to create a new (empty) COM+ application and then add components to that application.</span></span> <span data-ttu-id="46a5b-105">Elle explique également comment ajouter et supprimer des composants COM, et comment déplacer et copier des composants d’une application COM+ à une autre...</span><span class="sxs-lookup"><span data-stu-id="46a5b-105">It also describes how to add COM components to, and remove them from, existing COM+ applications, and how to move and copy components from one COM+ application to another.</span></span>



| <span data-ttu-id="46a5b-106">Rubrique</span><span class="sxs-lookup"><span data-stu-id="46a5b-106">Topic</span></span>                                                                                                       | <span data-ttu-id="46a5b-107">Description</span><span class="sxs-lookup"><span data-stu-id="46a5b-107">Description</span></span>                                                                        |
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="46a5b-108">Création d’une application COM+</span><span class="sxs-lookup"><span data-stu-id="46a5b-108">Creating a New COM+ Application</span></span>](creating-a-new-com--application.md)<br/>                           | <span data-ttu-id="46a5b-109">Décrit comment créer une application COM+.</span><span class="sxs-lookup"><span data-stu-id="46a5b-109">Describes how to create a new COM+ application.</span></span><br/>                         |
| [<span data-ttu-id="46a5b-110">Installation de nouveaux composants</span><span class="sxs-lookup"><span data-stu-id="46a5b-110">Installing New Components</span></span>](installing-new-components.md)<br/>                                       | <span data-ttu-id="46a5b-111">Décrit comment installer de nouveaux composants.</span><span class="sxs-lookup"><span data-stu-id="46a5b-111">Describes how to install new components.</span></span><br/>                                |
| [<span data-ttu-id="46a5b-112">Importation de composants</span><span class="sxs-lookup"><span data-stu-id="46a5b-112">Importing Components</span></span>](importing-components.md)<br/>                                                 | <span data-ttu-id="46a5b-113">Décrit comment importer des composants.</span><span class="sxs-lookup"><span data-stu-id="46a5b-113">Describes how to import components.</span></span><br/>                                     |
| [<span data-ttu-id="46a5b-114">Suppression d’un composant d’une application COM+</span><span class="sxs-lookup"><span data-stu-id="46a5b-114">Removing a Component from a COM+ Application</span></span>](removing-a-component-from-a-com--application.md)<br/> | <span data-ttu-id="46a5b-115">Décrit comment supprimer un composant d’une application COM+.</span><span class="sxs-lookup"><span data-stu-id="46a5b-115">Describes how to delete a component from a COM+ application.</span></span><br/>            |
| [<span data-ttu-id="46a5b-116">Déplacement des composants</span><span class="sxs-lookup"><span data-stu-id="46a5b-116">Moving Components</span></span>](moving-components.md)<br/>                                                       | <span data-ttu-id="46a5b-117">Décrit comment déplacer un composant d’une application COM+ à une autre.</span><span class="sxs-lookup"><span data-stu-id="46a5b-117">Describes how to move a component from one COM+ application to another.</span></span><br/> |
| [<span data-ttu-id="46a5b-118">Copier des composants</span><span class="sxs-lookup"><span data-stu-id="46a5b-118">Copying Components</span></span>](copying-components.md)<br/>                                                     | <span data-ttu-id="46a5b-119">Décrit comment copier un composant d’une application COM+ vers une autre.</span><span class="sxs-lookup"><span data-stu-id="46a5b-119">Describes how to copy a component from one COM+ application to another.</span></span><br/> |
| [<span data-ttu-id="46a5b-120">Suppression d’une application COM+</span><span class="sxs-lookup"><span data-stu-id="46a5b-120">Deleting a COM+ Application</span></span>](deleting-a-com--application.md)<br/>                                   | <span data-ttu-id="46a5b-121">Décrit comment supprimer une application COM+.</span><span class="sxs-lookup"><span data-stu-id="46a5b-121">Describes how to delete a COM+ application.</span></span><br/>                             |



 

<span data-ttu-id="46a5b-122">Pour obtenir des informations conceptuelles sur les procédures décrites dans cette section, consultez [vue d’ensemble de l’application com+](com--application-overview.md) et [déploiement d’applications com+](deploying-com--applications.md).</span><span class="sxs-lookup"><span data-stu-id="46a5b-122">For conceptual information on the procedures described in this section, see [COM+ Application Overview](com--application-overview.md) and [Deploying COM+ Applications](deploying-com--applications.md).</span></span>

<span data-ttu-id="46a5b-123">Pour obtenir des informations procédurales sur les tâches d’administration impliquées dans l’exportation et l’installation d’applications COM+, consultez « Installation d’applications COM+ » dans le Guide de l’administrateur des services de composants.</span><span class="sxs-lookup"><span data-stu-id="46a5b-123">For procedural information on the administrative tasks involved in exporting and installing COM+ applications, see "Installing COM+ Applications" in the Component Services Administrator's Guide.</span></span>

## <a name="related-topics"></a><span data-ttu-id="46a5b-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="46a5b-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="46a5b-125">Automatisation de l’administration COM+</span><span class="sxs-lookup"><span data-stu-id="46a5b-125">Automating COM+ Administration</span></span>](automating-com--administration.md)
</dt> <dt>

[<span data-ttu-id="46a5b-126">Configuration des applications COM+</span><span class="sxs-lookup"><span data-stu-id="46a5b-126">Configuring COM+ Applications</span></span>](configuring-com--applications.md)
</dt> <dt>

[<span data-ttu-id="46a5b-127">Conversion de packages MTS en applications COM+</span><span class="sxs-lookup"><span data-stu-id="46a5b-127">Conversion of MTS Packages to COM+ Applications</span></span>](conversion-of-mts-packages-to-com--applications.md)
</dt> </dl>

 

 




