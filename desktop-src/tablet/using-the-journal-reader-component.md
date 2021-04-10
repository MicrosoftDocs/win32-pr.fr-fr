---
description: Le composant lecteur de note du journal Microsoft Windows fournit un accès par programmation aux fichiers au format journal.
ms.assetid: 85dcda59-2972-48e3-a9f5-5cce0b60a1f1
title: Utilisation du composant de lecture du journal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48fd098db4ce1c0c92a5ded76b0950e264aa2a73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951145"
---
# <a name="using-the-journal-reader-component"></a><span data-ttu-id="296b4-103">Utilisation du composant de lecture du journal</span><span class="sxs-lookup"><span data-stu-id="296b4-103">Using the Journal Reader Component</span></span>

<span data-ttu-id="296b4-104">Le composant lecteur de note du journal Microsoft Windows fournit un accès par programmation aux fichiers au format journal.</span><span class="sxs-lookup"><span data-stu-id="296b4-104">The Microsoft Windows Journal Note Reader component provides programmatic read access to files in the Journal format.</span></span>

## <a name="component-overview"></a><span data-ttu-id="296b4-105">Vue d’ensemble des composants</span><span class="sxs-lookup"><span data-stu-id="296b4-105">Component Overview</span></span>

<span data-ttu-id="296b4-106">Les fichiers journaux ont l’extension de fichier. jnt.</span><span class="sxs-lookup"><span data-stu-id="296b4-106">Journal files have the .jnt file extension.</span></span> <span data-ttu-id="296b4-107">Ce composant simple prend un flux contenant un fichier. jnt et retourne un flux contenant le contenu du fichier au format XML.</span><span class="sxs-lookup"><span data-stu-id="296b4-107">This simple component takes a stream containing a .jnt file and returns a stream containing the file's content in XML format.</span></span> <span data-ttu-id="296b4-108">Le code XML retourné par le composant est conforme au schéma du lecteur de note du journal.</span><span class="sxs-lookup"><span data-stu-id="296b4-108">The XML returned by the component conforms to the Journal Note Reader schema.</span></span> <span data-ttu-id="296b4-109">Ce schéma est documenté dans [Référence du schéma du lecteur du journal](journal-reader-schema-reference.md).</span><span class="sxs-lookup"><span data-stu-id="296b4-109">This schema is documented in [Journal Reader Schema Reference](journal-reader-schema-reference.md).</span></span>

<span data-ttu-id="296b4-110">Le composant ne permet pas d’écrire des fichiers. jnt.</span><span class="sxs-lookup"><span data-stu-id="296b4-110">The component does not provide the ability to write out .jnt files.</span></span>

<span data-ttu-id="296b4-111">Le composant est disponible dans les versions managées et non managées.</span><span class="sxs-lookup"><span data-stu-id="296b4-111">The component is available in unmanaged and managed versions.</span></span> <span data-ttu-id="296b4-112">Le composant non managé est disponible dans la bibliothèque de liens dynamiques (DLL) journal.dll.</span><span class="sxs-lookup"><span data-stu-id="296b4-112">The unmanaged component is available in the journal.dll dynamic link library (DLL).</span></span> <span data-ttu-id="296b4-113">La version managée se trouve dans l’assembly Microsoft.Ink.Journal.dll (pour la redistribution vers Windows XP Édition Tablet PC ou Windows Vista) ou Microsoft.Ink.dll.</span><span class="sxs-lookup"><span data-stu-id="296b4-113">The managed version is either in the Microsoft.Ink.Journal.dll assembly (for redistribution to Windows XP Tablet PC Edition or Windows Vista), or Microsoft.Ink.dll.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="296b4-114">À partir de Windows 10, version 1607, journal.dll n’est pas inclus dans le système d’exploitation Windows.</span><span class="sxs-lookup"><span data-stu-id="296b4-114">Beginning with Windows 10, version 1607, journal.dll is not included in the Windows operating system.</span></span> <span data-ttu-id="296b4-115">Cette bibliothèque doit être considérée comme dépréciée ou obsolète et ne doit pas être utilisée.</span><span class="sxs-lookup"><span data-stu-id="296b4-115">That library should be considered deprecated or obsolete and should not be used.</span></span>

 

### <a name="assembly-changes-of-note"></a><span data-ttu-id="296b4-116">Modifications de l’assembly de note</span><span class="sxs-lookup"><span data-stu-id="296b4-116">Assembly Changes of Note</span></span>

<span data-ttu-id="296b4-117">Il est important de tenir compte de certaines modifications apportées à l’assembly contenant le composant lecteur de note de journal qui s’est produit entre la version publiée avec la version 1,7 du kit de développement de Tablet PC et la version fournie avec le système d’exploitation Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="296b4-117">It is important to be aware of some changes to the assembly containing the Journal Note Reader component that occurred between the version released in conjunction with version 1.7 of the Tablet Developers Kit and the version that ships in the Windows Vista operating system.</span></span>

<span data-ttu-id="296b4-118">La version 1,7 du composant lecteur, qui peut être redistribuée vers Windows XP ou Windows Vista, est contenue dans un assembly appelé Microsoft.Ink.Journal.dll.</span><span class="sxs-lookup"><span data-stu-id="296b4-118">The 1.7 version of the reader component, which can be redistributed to either Windows XP or Windows Vista, is contained in an assembly called Microsoft.Ink.Journal.dll.</span></span> <span data-ttu-id="296b4-119">Le composant lecteur est fourni avec Windows Vista, mais il a été intégré à l’assembly principal Microsoft.Ink.dll.</span><span class="sxs-lookup"><span data-stu-id="296b4-119">The reader component ships in Windows Vista, but has been integrated into the core Microsoft.Ink.dll assembly.</span></span> <span data-ttu-id="296b4-120">Cela signifie que les applications qui utilisent l’assembly 1,7 doivent redistribuer cet assembly avec leur installation.</span><span class="sxs-lookup"><span data-stu-id="296b4-120">This means that applications that make use of the 1.7 assembly need to redistribute that assembly with their setup.</span></span>

## <a name="using-the-component"></a><span data-ttu-id="296b4-121">Utilisation du composant</span><span class="sxs-lookup"><span data-stu-id="296b4-121">Using the Component</span></span>

<span data-ttu-id="296b4-122">Le composant lecteur de note de journal est utile pour extraire les données d’entrée manuscrite et d’autres informations sur le fichier à partir d’un fichier journal.</span><span class="sxs-lookup"><span data-stu-id="296b4-122">The Journal Note Reader component is useful for extracting the ink data and other information about the file from a Journal file.</span></span>

### <a name="com"></a><span data-ttu-id="296b4-123">COM</span><span class="sxs-lookup"><span data-stu-id="296b4-123">COM</span></span>

<span data-ttu-id="296b4-124">Le composant COM lecteur de note de journal se trouve dans le fichier Journal.dll, qui est installé et inscrit lorsque vous téléchargez et exécutez le fichier d’installation du lecteur de note de journal.</span><span class="sxs-lookup"><span data-stu-id="296b4-124">The Journal Note Reader COM component is in the file Journal.dll, which is installed and registered when you download and run the Journal Note Reader installation file.</span></span>

<span data-ttu-id="296b4-125">Le composant COM ne prend pas en charge l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="296b4-125">The COM component does not support the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span>

### <a name="managed"></a><span data-ttu-id="296b4-126">Adresses IP gérées</span><span class="sxs-lookup"><span data-stu-id="296b4-126">Managed</span></span>

<span data-ttu-id="296b4-127">Le composant géré du lecteur de note de journal se trouve dans l’assembly de Microsoft.Ink.JournalReader.dll.</span><span class="sxs-lookup"><span data-stu-id="296b4-127">The Journal Note Reader managed component is in the Microsoft.Ink.JournalReader.dll assembly.</span></span> <span data-ttu-id="296b4-128">Cet assembly est installé et inscrit dans le Global Assembly Cache lorsque vous exécutez le fichier d’installation du lecteur de note de journal.</span><span class="sxs-lookup"><span data-stu-id="296b4-128">This assembly is installed and registered in the global assembly cache when you run the Journal Note Reader installation file.</span></span>

<span data-ttu-id="296b4-129">Ajoutez une référence à l’assembly pour l’utiliser dans votre projet managé.</span><span class="sxs-lookup"><span data-stu-id="296b4-129">Add a reference to the assembly to use it in your managed project.</span></span>

## <a name="related-topics"></a><span data-ttu-id="296b4-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="296b4-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="296b4-131">**Interface IJournalReader**</span><span class="sxs-lookup"><span data-stu-id="296b4-131">**IJournalReader Interface**</span></span>](ijournalreader.md)
</dt> <dt>

[<span data-ttu-id="296b4-132">Référence du schéma du lecteur de journal</span><span class="sxs-lookup"><span data-stu-id="296b4-132">Journal Reader Schema Reference</span></span>](journal-reader-schema-reference.md)
</dt> </dl>

 

 
