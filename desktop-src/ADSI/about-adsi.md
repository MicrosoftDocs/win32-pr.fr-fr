---
title: À propos des interfaces de service Active Directory
description: Active Directory interfaces de service (ADSI) abstraites les fonctionnalités des services d’annuaire de différents fournisseurs de réseau dans un environnement informatique distribué pour présenter un ensemble unique d’interfaces de service d’annuaire pour la gestion des ressources réseau.
ms.assetid: 6d601af5-7470-42c2-b99e-21174ea008b1
ms.tgt_platform: multiple
keywords:
- À propos des interfaces de service Active Directory ADSI
- ADSI ADSI, à propos de
- Interfaces ADSI (Active Directory Service Interfaces), à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc083b33a633335da12915257fcddff1174a6858
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100585"
---
# <a name="about-active-directory-service-interfaces"></a><span data-ttu-id="80256-106">À propos des interfaces de service Active Directory</span><span class="sxs-lookup"><span data-stu-id="80256-106">About Active Directory Service Interfaces</span></span>

<span data-ttu-id="80256-107">Active Directory interfaces de service (ADSI) abstraites les fonctionnalités des services d’annuaire de différents fournisseurs de réseau dans un environnement informatique distribué pour présenter un ensemble unique d’interfaces de service d’annuaire pour la gestion des ressources réseau.</span><span class="sxs-lookup"><span data-stu-id="80256-107">Active Directory Service Interfaces (ADSI) abstracts the capabilities of directory services from different network providers in a distributed computing environment to present a single set of directory service interfaces for managing network resources.</span></span> <span data-ttu-id="80256-108">Les administrateurs et les développeurs peuvent utiliser les services ADSI pour énumérer et gérer les ressources dans un service d’annuaire, quel que soit l’environnement réseau qui contient la ressource.</span><span class="sxs-lookup"><span data-stu-id="80256-108">Administrators and developers can use ADSI services to enumerate and manage the resources in a directory service, no matter which network environment contains the resource.</span></span>

<span data-ttu-id="80256-109">ADSI facilite l’exécution de tâches d’administration courantes, telles que l’ajout de nouveaux utilisateurs, la gestion des imprimantes et la localisation des ressources dans l’environnement informatique distribué.</span><span class="sxs-lookup"><span data-stu-id="80256-109">ADSI makes it easier to perform common administrative tasks, such as adding new users, managing printers, and locating resources throughout the distributed computing environment.</span></span>

<span data-ttu-id="80256-110">Grâce à ADSI, les développeurs peuvent facilement « activer l’annuaire » pour les applications.</span><span class="sxs-lookup"><span data-stu-id="80256-110">ADSI makes it easy for developers to "directory enable" their applications.</span></span> <span data-ttu-id="80256-111">Les administrateurs et les développeurs gèrent un ensemble unique d’interfaces de service d’annuaire, quels que soient les services d’annuaire installés.</span><span class="sxs-lookup"><span data-stu-id="80256-111">Administrators and developers handle a single set of directory service interfaces, regardless of which directory services are installed.</span></span>

<span data-ttu-id="80256-112">Les rubriques suivantes sont traitées dans cette introduction :</span><span class="sxs-lookup"><span data-stu-id="80256-112">The following topics are discussed in this introduction:</span></span>

-   [<span data-ttu-id="80256-113">Plusieurs services d’annuaire</span><span class="sxs-lookup"><span data-stu-id="80256-113">Multiple Directory Services</span></span>](multiple-directory-services.md)
-   [<span data-ttu-id="80256-114">Qui utilisera Active Directory interfaces de service ?</span><span class="sxs-lookup"><span data-stu-id="80256-114">Who Will Use Active Directory Service Interfaces?</span></span>](who-will-use-active-directory-service-interfaces.md)
-   [<span data-ttu-id="80256-115">Services d’annuaire aujourd’hui</span><span class="sxs-lookup"><span data-stu-id="80256-115">Directory Services Today</span></span>](directory-services-today.md)
-   [<span data-ttu-id="80256-116">Avantages de l’utilisation des interfaces de service Active Directory</span><span class="sxs-lookup"><span data-stu-id="80256-116">Benefits of Using Active Directory Service Interfaces</span></span>](benefits-of-using-active-directory-service-interfaces.md)
-   [<span data-ttu-id="80256-117">Architecture des interfaces de service Active Directory</span><span class="sxs-lookup"><span data-stu-id="80256-117">Active Directory Service Interfaces Architecture</span></span>](active-directory-service-interfaces-architecture.md)
-   [<span data-ttu-id="80256-118">Prise en charge des langages de programmation</span><span class="sxs-lookup"><span data-stu-id="80256-118">Programming Language Support</span></span>](programming-language-support.md)
-   [<span data-ttu-id="80256-119">Propriétés et attributs ADSI</span><span class="sxs-lookup"><span data-stu-id="80256-119">ADSI Properties and Attributes</span></span>](adsi-properties-and-attributes.md)

## <a name="what-you-should-know-before-reading-this-guide"></a><span data-ttu-id="80256-120">Ce que vous devez savoir avant de lire ce guide</span><span class="sxs-lookup"><span data-stu-id="80256-120">What You Should Know Before Reading This Guide</span></span>

<span data-ttu-id="80256-121">Ce guide part du principe que vous êtes familiarisé avec le modèle COM (Component Object Model) et l’automatisation, et que vous savez comment programmer en Visual Basic ou en C/C++.</span><span class="sxs-lookup"><span data-stu-id="80256-121">This guide assumes that you are familiar with the Component Object Model (COM) and Automation, and that you know how to program in either Visual Basic or C/C++.</span></span>

<span data-ttu-id="80256-122">Certains termes utilisés dans ce guide sont propres à ADSI ou à l’environnement des services d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="80256-122">Some of the terms used in this guide are unique to either ADSI or the directory services environment.</span></span> <span data-ttu-id="80256-123">D’autres termes sont familiers, mais ils peuvent avoir une signification légèrement différente dans ces environnements.</span><span class="sxs-lookup"><span data-stu-id="80256-123">Other terms will be familiar but may have slightly different meanings in these environments.</span></span>

## <a name="further-reading-about-adsi-and-related-topics"></a><span data-ttu-id="80256-124">En savoir plus sur ADSI et les rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="80256-124">Further Reading about ADSI and Related Topics</span></span>

<span data-ttu-id="80256-125">Pour plus d’informations sur les interfaces de service Active Directory et sur les technologies sur lesquelles elles sont basées, vous pouvez trouver les sources suivantes utiles.</span><span class="sxs-lookup"><span data-stu-id="80256-125">For more information about Active Directory Service Interfaces and the technologies on which they are based, you may find the following sources helpful.</span></span>

<span data-ttu-id="80256-126">Brockschmidt, Kraig.</span><span class="sxs-lookup"><span data-stu-id="80256-126">Brockschmidt, Kraig.</span></span> <span data-ttu-id="80256-127">*Dans OLE*, 2e édition.</span><span class="sxs-lookup"><span data-stu-id="80256-127">*Inside OLE*, 2nd edition.</span></span> <span data-ttu-id="80256-128">Redmond, WA : Microsoft Press, 1995.</span><span class="sxs-lookup"><span data-stu-id="80256-128">Redmond, WA: Microsoft Press, 1995.</span></span>

<span data-ttu-id="80256-129">Chappell, David.</span><span class="sxs-lookup"><span data-stu-id="80256-129">Chappell, David.</span></span> <span data-ttu-id="80256-130">*Fonctionnement d’ActiveX et d’OLE*.</span><span class="sxs-lookup"><span data-stu-id="80256-130">*Understanding ActiveX and OLE*.</span></span> <span data-ttu-id="80256-131">Redmond, WA : Microsoft Press, 1996.</span><span class="sxs-lookup"><span data-stu-id="80256-131">Redmond, WA: Microsoft Press, 1996.</span></span>

<span data-ttu-id="80256-132">Hahn, Steven.</span><span class="sxs-lookup"><span data-stu-id="80256-132">Hahn, Steven.</span></span> <span data-ttu-id="80256-133">*Guide de référence du programmeur ASP ADSI*.</span><span class="sxs-lookup"><span data-stu-id="80256-133">*ADSI ASP Programmer's Reference*.</span></span> <span data-ttu-id="80256-134">Wrox Appuyez sur Ltd., 1998.</span><span class="sxs-lookup"><span data-stu-id="80256-134">Wrox Press Ltd., 1998.</span></span>

<span data-ttu-id="80256-135">Harrison, Richard.</span><span class="sxs-lookup"><span data-stu-id="80256-135">Harrison, Richard.</span></span> <span data-ttu-id="80256-136">*Sécurité Web ASP/MTS/ADSI*.</span><span class="sxs-lookup"><span data-stu-id="80256-136">*ASP/MTS/ADSI Web Security*.</span></span> <span data-ttu-id="80256-137">Prentice Hall, 1999.</span><span class="sxs-lookup"><span data-stu-id="80256-137">Prentice Hall, 1999.</span></span>

<span data-ttu-id="80256-138">Version de référence du programmeur OLE DB de Microsoft, version 1,0, 1996.</span><span class="sxs-lookup"><span data-stu-id="80256-138">Microsoft's OLE DB Programmer's Reference Version 1.0, 1996.</span></span>

<span data-ttu-id="80256-139">*OLE 2 Programmer’s Reference, Volume Two*.</span><span class="sxs-lookup"><span data-stu-id="80256-139">*OLE 2 Programmer's Reference, Volume Two*.</span></span> <span data-ttu-id="80256-140">Redmond, WA : Microsoft Press, 1994.</span><span class="sxs-lookup"><span data-stu-id="80256-140">Redmond, WA: Microsoft Press, 1994.</span></span>

<span data-ttu-id="80256-141">Rogerson’s, Dale.</span><span class="sxs-lookup"><span data-stu-id="80256-141">Rogerson, Dale.</span></span> <span data-ttu-id="80256-142">*Dans com*.</span><span class="sxs-lookup"><span data-stu-id="80256-142">*Inside COM*.</span></span> <span data-ttu-id="80256-143">Redmond, WA : Microsoft Press, 1997.</span><span class="sxs-lookup"><span data-stu-id="80256-143">Redmond, WA: Microsoft Press, 1997.</span></span>

<span data-ttu-id="80256-144">*La Version 2,0 de la spécification de conception de Service Active Directory*.</span><span class="sxs-lookup"><span data-stu-id="80256-144">*The Active Directory Service Design Specification Version 2.0*.</span></span>

<span data-ttu-id="80256-145">*Spécification du modèle d’objet de composant*.</span><span class="sxs-lookup"><span data-stu-id="80256-145">*The Component Object Model Specification*.</span></span>

<span data-ttu-id="80256-146">(Ces ressources peuvent ne pas être disponibles dans certaines langues et pays/régions.)</span><span class="sxs-lookup"><span data-stu-id="80256-146">(These resources may not be available in some languages and countries/regions.)</span></span>

 

 




