---
description: Le Windows Installer conserve toutes les informations relatives à l’installation dans une base de données relationnelle. Vous pouvez modifier cette base de données et, par conséquent, l’installation, à l’aide de transformations et de fusions.
ms.assetid: 32163e06-d03d-4b65-b744-62f306f2100d
title: Fusions et transformations
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aec6314e81afb5afa9d74346b64fe3129ba5ed30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518923"
---
# <a name="merges-and-transforms"></a><span data-ttu-id="bf2e0-104">Fusions et transformations</span><span class="sxs-lookup"><span data-stu-id="bf2e0-104">Merges and Transforms</span></span>

<span data-ttu-id="bf2e0-105">Le Windows Installer conserve toutes les informations relatives à l’installation dans une base de données relationnelle.</span><span class="sxs-lookup"><span data-stu-id="bf2e0-105">The Windows Installer keeps all information about the installation in a relational database.</span></span> <span data-ttu-id="bf2e0-106">Vous pouvez modifier cette base de données et, par conséquent, l’installation, à l’aide de transformations et de fusions.</span><span class="sxs-lookup"><span data-stu-id="bf2e0-106">You can modify this database, and therefore the installation, by using transforms and merges.</span></span>

## <a name="transforms"></a><span data-ttu-id="bf2e0-107">Transformations</span><span class="sxs-lookup"><span data-stu-id="bf2e0-107">Transforms</span></span>

<span data-ttu-id="bf2e0-108">Une [transformation de base de données](database-transforms.md) ajoute ou remplace des éléments dans la base de données d’origine.</span><span class="sxs-lookup"><span data-stu-id="bf2e0-108">A [database transform](database-transforms.md) adds or replaces elements in the original database.</span></span> <span data-ttu-id="bf2e0-109">Par exemple, une transformation peut modifier l’ensemble du texte de l’interface utilisateur de l’application, du français au français.</span><span class="sxs-lookup"><span data-stu-id="bf2e0-109">For example, a transform can change all of the text in an application's user interface from French to English.</span></span>

<span data-ttu-id="bf2e0-110">Les utilisations principales des transformations sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="bf2e0-110">Primary uses for transforms include:</span></span>

-   <span data-ttu-id="bf2e0-111">Personnalisation des packages d’installation de base pour des groupes d’utilisateurs particuliers.</span><span class="sxs-lookup"><span data-stu-id="bf2e0-111">Customization of base installation packages for particular groups of users.</span></span>

    <span data-ttu-id="bf2e0-112">Les transformations peuvent être utilisées pour encapsuler les différentes personnalisations d’un package de base qui sont requises par différents groupes d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="bf2e0-112">Transforms can be used to encapsulate the various customizations of a single base package that are required by different groups of users.</span></span> <span data-ttu-id="bf2e0-113">Par exemple, cela s’avère utile dans les organisations où les services de support technique et de personnel ont besoin de différentes installations d’un produit particulier.</span><span class="sxs-lookup"><span data-stu-id="bf2e0-113">For example, this is useful in organizations where the finance and staff support departments require different installations of a particular product.</span></span> <span data-ttu-id="bf2e0-114">Le package de base d’un produit peut être mis à la disposition de tous les utilisateurs d’un point d’installation administratif avec des personnalisations appropriées distribuées à chaque groupe d’utilisateurs séparément.</span><span class="sxs-lookup"><span data-stu-id="bf2e0-114">A product's base package can be available to everyone at one administrative installation point with appropriate customizations distributed to each group of users separately.</span></span>

-   <span data-ttu-id="bf2e0-115">Synchronisation des applications dans plusieurs langues.</span><span class="sxs-lookup"><span data-stu-id="bf2e0-115">Synchronization of applications across languages.</span></span>

    <span data-ttu-id="bf2e0-116">Les transformations sont utiles pour la conservation des packages créés à des emplacements largement séparés synchronisés au cours de la création.</span><span class="sxs-lookup"><span data-stu-id="bf2e0-116">Transforms are useful for keeping packages authored at widely separated locations synchronized during authoring.</span></span> <span data-ttu-id="bf2e0-117">Par exemple, si une mise à niveau est d’abord développée pour une version anglaise d’une application qui existe en anglais et en français, une transformation peut être appliquée à la version anglaise mise à niveau qui la convertit en version française mise à niveau.</span><span class="sxs-lookup"><span data-stu-id="bf2e0-117">For example, if an upgrade is first developed for an English version of an application that exists in English and French, a transform can be applied to the upgraded English version that converts it into an upgraded French version.</span></span>

    <span data-ttu-id="bf2e0-118">Plusieurs transformations peuvent être appliquées à un package de base, puis appliquées à la volée pendant l’installation.</span><span class="sxs-lookup"><span data-stu-id="bf2e0-118">Multiple transforms can be applied to a base package and then applied on-the-fly during installation.</span></span> <span data-ttu-id="bf2e0-119">Cela étend les fonctionnalités du programme d’installation pour créer des packages personnalisés et fournit un mécanisme permettant d’attribuer efficacement les installations les plus appropriées à différents groupes d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="bf2e0-119">This extends the capabilities of the installer to create custom packages and provides a mechanism for efficiently assigning the most appropriate installations to different groups of users.</span></span>

-   <span data-ttu-id="bf2e0-120">Application de correctifs aux applications.</span><span class="sxs-lookup"><span data-stu-id="bf2e0-120">Patching applications.</span></span>

    <span data-ttu-id="bf2e0-121">Les transformations peuvent être utilisées pour appliquer un correctif mineur à une application qui ne garantit pas une mise à niveau majeure.</span><span class="sxs-lookup"><span data-stu-id="bf2e0-121">Transforms can be used to apply a minor fix to an application that does not warrant a major upgrade.</span></span> <span data-ttu-id="bf2e0-122">Pour plus d’informations sur les correctifs, consultez [packages de correctifs](patch-packages.md).</span><span class="sxs-lookup"><span data-stu-id="bf2e0-122">For more information about patches, see [Patch Packages](patch-packages.md).</span></span>

## <a name="merges"></a><span data-ttu-id="bf2e0-123">Fusions</span><span class="sxs-lookup"><span data-stu-id="bf2e0-123">Merges</span></span>

<span data-ttu-id="bf2e0-124">Une fusion combine deux bases de données dans une base de données et ajoute des informations au lieu de les remplacer.</span><span class="sxs-lookup"><span data-stu-id="bf2e0-124">A merge combines two databases into one database, and adds, rather than replaces, information.</span></span> <span data-ttu-id="bf2e0-125">Si les deux bases de données comportent des informations identiques, un conflit de fusion se produit.</span><span class="sxs-lookup"><span data-stu-id="bf2e0-125">If the same information exists in both databases, a merge conflict occurs.</span></span> <span data-ttu-id="bf2e0-126">Les fusions sont utiles pour les équipes de développement, car elles permettent de diviser une application volumineuse en parties pouvant être recombinées ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="bf2e0-126">Merges are useful to development teams because they allow a large application to be divided into parts that can be recombined later.</span></span> <span data-ttu-id="bf2e0-127">Par exemple, les éléments de base de données pour l’installation d’un nouveau composant peuvent être développés séparément et par la suite fusionnés dans la base de données d’installation principale.</span><span class="sxs-lookup"><span data-stu-id="bf2e0-127">For example, the database elements for the installation of a new component can be developed separately and later merged into the main installation database.</span></span> <span data-ttu-id="bf2e0-128">Pour plus d’informations, consultez [fusionner des modules](merge-modules.md).</span><span class="sxs-lookup"><span data-stu-id="bf2e0-128">For more information, see [Merge Modules](merge-modules.md).</span></span>

<span data-ttu-id="bf2e0-129">Une équipe de développement peut appliquer une opération de fusion de la façon suivante :</span><span class="sxs-lookup"><span data-stu-id="bf2e0-129">A development team might apply a merge operation in the following way:</span></span>

1.  <span data-ttu-id="bf2e0-130">Séparer en groupes et travailler simultanément sur différents composants d’une grande application.</span><span class="sxs-lookup"><span data-stu-id="bf2e0-130">Separate into groups and work simultaneously on different components of a large application.</span></span>
2.  <span data-ttu-id="bf2e0-131">Chaque groupe de développement remplit ensuite une base de données avec les informations d’installation de son propre composant, sans se préoccuper des autres composants de l’application.</span><span class="sxs-lookup"><span data-stu-id="bf2e0-131">Each development group then populates a database with installation information for its own component, without being concerned with the other components of the application.</span></span>
3.  <span data-ttu-id="bf2e0-132">Une fois le développement d’un composant terminé, la base de données de ce composant peut être fusionnée dans la base de données d’installation principale pour l’application entière.</span><span class="sxs-lookup"><span data-stu-id="bf2e0-132">After the development of a component is complete, that component's database can be merged into the main installation database for the entire application.</span></span>

 

 



