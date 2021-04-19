---
description: Les composants indiquent le type de données qu’ils représentent par le biais d’un type.
ms.assetid: 19d785d5-09a7-48b9-a0a2-eca3049d67fe
title: Types de composants
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1f89355b4b26090b7d43f9753c086b4ccc79df0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106531393"
---
# <a name="component-types"></a><span data-ttu-id="6b31c-103">Types de composants</span><span class="sxs-lookup"><span data-stu-id="6b31c-103">Component Types</span></span>

<span data-ttu-id="6b31c-104">Les composants indiquent le type de données qu’ils représentent par le biais d’un type.</span><span class="sxs-lookup"><span data-stu-id="6b31c-104">Components indicate the sort of data they represent through a type.</span></span>

<span data-ttu-id="6b31c-105">Actuellement, les types de composant (consultez [**\_ \_ type de composant VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_component_type)) sont limités à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="6b31c-105">Currently, component types (see [**VSS\_COMPONENT\_TYPE**](/windows/desktop/api/VsWriter/ne-vswriter-vss_component_type)) are limited to the following:</span></span>

-   <span data-ttu-id="6b31c-106">Composants de base de données</span><span class="sxs-lookup"><span data-stu-id="6b31c-106">Database components</span></span>
-   <span data-ttu-id="6b31c-107">Groupes de fichiers</span><span class="sxs-lookup"><span data-stu-id="6b31c-107">File groups</span></span>

<span data-ttu-id="6b31c-108">Pour plus d’informations sur la définition des types de composants, consultez [définition des composants par les Writers](definition-of-components-by-writers.md).</span><span class="sxs-lookup"><span data-stu-id="6b31c-108">For implementation information about setting component types, see [Definition of Components by Writers](definition-of-components-by-writers.md).</span></span>

<span data-ttu-id="6b31c-109">Les enregistreurs ont une saisie de données qui indique leur utilisation (consultez [**\_ \_ type de source VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_source_type)), qui peut être la suivante :</span><span class="sxs-lookup"><span data-stu-id="6b31c-109">Writers have a data typing that indicates their usage (see [**VSS\_SOURCE\_TYPE**](/windows/desktop/api/VsWriter/ne-vswriter-vss_source_type)), which can be the following:</span></span>

-   <span data-ttu-id="6b31c-110">Une base de données transactionnelle (par exemple, un serveur SQL Server)</span><span class="sxs-lookup"><span data-stu-id="6b31c-110">A transactional database (such as an SQL server)</span></span>
-   <span data-ttu-id="6b31c-111">Une base de données non transactionnelle (comme un client de feuille de calcul)</span><span class="sxs-lookup"><span data-stu-id="6b31c-111">A nontransactional database (such as a spreadsheet client)</span></span>
-   <span data-ttu-id="6b31c-112">Groupe de fichiers (autre)</span><span class="sxs-lookup"><span data-stu-id="6b31c-112">File group (other)</span></span>

<span data-ttu-id="6b31c-113">La spécification d’un type de composant en tant que base de données permet d’identifier plus facilement son contenu, permet de gérer séparément les fichiers journaux et de données (consultez [**IVssCreateWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata) et [**IVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) pour plus d’informations) et applique une plus grande rigueur dans la sélection de fichiers en n’autorisant pas la sélection de fichier récursive ou en utilisant un [*autre chemin d’accès*](vssgloss-a.md) (voir [**IVssCreateWriterMetadata :: AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles) et [**IVssCreateWriterMetadata :**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles)</span><span class="sxs-lookup"><span data-stu-id="6b31c-113">Specifying a component type as database allows for easier identification of its content, allows for separate handling of log and data files (see [**IVssCreateWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata) and [**IVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) for details), and enforces greater rigor in file selection by not allowing either recursive file selection or using an [*alternate path*](vssgloss-a.md) (see [**IVssCreateWriterMetadata::AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles) and [**IVssCreateWriterMetadata::AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles)).</span></span>

<span data-ttu-id="6b31c-114">Avec un composant de groupe de fichiers, en revanche, au prix de ne pas connaître les données qu’il contient, vous avez une plus grande liberté quant à la façon dont les fichiers sont insérés, car vous pouvez utiliser la spécification récursive et d’autres chemins d’accès.</span><span class="sxs-lookup"><span data-stu-id="6b31c-114">With a file group component, on the other hand, at the price of not knowing what data it contains, you have greater freedom about how files are inserted, because you can use recursive specification and alternate paths.</span></span>

<span data-ttu-id="6b31c-115">D’autres types de composants peuvent être ajoutés à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="6b31c-115">Additional component types may be added in the future.</span></span>

 

 



