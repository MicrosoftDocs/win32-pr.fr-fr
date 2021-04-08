---
description: À compter de Windows 7, Windows Management Instrumentation (WMI) implémentait un mécanisme standard pour la découverte des profils à l’aide du schéma CIM.
ms.assetid: e748b623-5ff3-464d-ba09-96cf226de7b6
ms.tgt_platform: multiple
title: Traversée d’association entre espaces de noms
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fe2bbb408c4d89a7093adf45f3daf276df294ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864029"
---
# <a name="cross-namespace-association-traversal"></a><span data-ttu-id="20c1c-103">Traversée d’association entre espaces de noms</span><span class="sxs-lookup"><span data-stu-id="20c1c-103">Cross-Namespace Association Traversal</span></span>

<span data-ttu-id="20c1c-104">À compter de Windows 7, Windows Management Instrumentation (WMI) implémentait un mécanisme standard pour la découverte des profils à l’aide du schéma CIM.</span><span class="sxs-lookup"><span data-stu-id="20c1c-104">Starting in Windows 7, Windows Management Instrumentation (WMI) implemented a standard mechanism for discovering profiles by using the CIM schema.</span></span>

<span data-ttu-id="20c1c-105">WMI prend en charge l’inscription des profils d’association et de parcours d’association entre espaces de noms.</span><span class="sxs-lookup"><span data-stu-id="20c1c-105">WMI supports the cross-namespace association traversal and association profile registration.</span></span> <span data-ttu-id="20c1c-106">Pour plus d’informations sur l’inscription des profils et l’implémentation standard CIM de la traversée d’association, consultez DSP1033 ( [https://www.dmtf.org/standards/published\_documents/DSP1033.pdf](https://www.dmtf.org/sites/default/files/standards/documents/DSP1033_1.0.0.pdf) )</span><span class="sxs-lookup"><span data-stu-id="20c1c-106">For more information about profile registration and the CIM standard implementation of association traversal, see DSP1033 ([https://www.dmtf.org/standards/published\_documents/DSP1033.pdf](https://www.dmtf.org/sites/default/files/standards/documents/DSP1033_1.0.0.pdf))</span></span>

<span data-ttu-id="20c1c-107">Pour prendre en charge cette fonctionnalité, l’infrastructure WMI a effectué les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="20c1c-107">To support this feature, the WMI infrastructure did the following:</span></span>

-   <span data-ttu-id="20c1c-108">Création de l’espace de noms Interop : \\ \\ Interop racine.</span><span class="sxs-lookup"><span data-stu-id="20c1c-108">Created the interop namespace: \\root\\interop.</span></span>
-   <span data-ttu-id="20c1c-109">Traversée des associations entre espaces de noms autorisées.</span><span class="sxs-lookup"><span data-stu-id="20c1c-109">Allowed cross namespace association traversal.</span></span> <span data-ttu-id="20c1c-110">Les associations qui traversent des espaces de noms prennent en charge le filtrage au niveau de la classe d’association et au niveau de l’espace de noms implémenté.</span><span class="sxs-lookup"><span data-stu-id="20c1c-110">Associations that cross namespaces support filtering at the association class level and at the implemented namespace level.</span></span>
-   <span data-ttu-id="20c1c-111">Ajout des classes [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)), [**CIM \_ ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile)et [**CIM \_ ReferencedProfile**](cim-referencedprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="20c1c-111">Added the [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)), [**CIM\_ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile), and [**CIM\_ReferencedProfile**](cim-referencedprofile.md) classes.</span></span>
-   <span data-ttu-id="20c1c-112">Mise en œuvre de la version du schéma CIM compatibilité 2.17.1.</span><span class="sxs-lookup"><span data-stu-id="20c1c-112">Implemented CIM Schema version 2.17.1 compatibility.</span></span> <span data-ttu-id="20c1c-113">Pour plus d’informations, consultez [compatibilité du schéma CIM](cim-schema-compatibility.md).</span><span class="sxs-lookup"><span data-stu-id="20c1c-113">For more information, see [CIM Schema Compatibility](cim-schema-compatibility.md).</span></span>

## <a name="interop-namespace"></a><span data-ttu-id="20c1c-114">Espace de noms Interop</span><span class="sxs-lookup"><span data-stu-id="20c1c-114">Interop Namespace</span></span>

<span data-ttu-id="20c1c-115">L’espace de noms Interop fournit un emplacement commun pour qu’une application cliente Découvre tous les profils pris en charge sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="20c1c-115">The interop namespace provides a common location for a client application to discover all of the profiles that are supported on a computer.</span></span> <span data-ttu-id="20c1c-116">Les profils peuvent être utilisés pour gérer différents aspects d’un système d’exploitation, d’un groupe de stockage ou d’une base de données.</span><span class="sxs-lookup"><span data-stu-id="20c1c-116">Profiles can be used to manage various aspects of an operating system, storage array, or database.</span></span>

<span data-ttu-id="20c1c-117">Tous les objets et classes Interop doivent être définis dans l' \\ espace de noms Interop racine.</span><span class="sxs-lookup"><span data-stu-id="20c1c-117">All interop classes and objects must be defined in the root\\interop namespace.</span></span>

## <a name="cim-classes"></a><span data-ttu-id="20c1c-118">Classes CIM</span><span class="sxs-lookup"><span data-stu-id="20c1c-118">CIM Classes</span></span>

<span data-ttu-id="20c1c-119">Les classes CIM décrites dans la liste suivante prennent en charge la traversée d’association entre espaces de noms.</span><span class="sxs-lookup"><span data-stu-id="20c1c-119">The CIM classes described in the following list support cross-namespace association traversal.</span></span>

<dl> <dt>

<span data-ttu-id="20c1c-120"><span id="CIM_RegisteredProfile"></span><span id="cim_registeredprofile"></span><span id="CIM_REGISTEREDPROFILE"></span>[**\_REGISTEREDPROFILE CIM**](/previous-versions//ee309375(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="20c1c-120"><span id="CIM_RegisteredProfile"></span><span id="cim_registeredprofile"></span><span id="CIM_REGISTEREDPROFILE"></span>[**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="20c1c-121">Utilisé pour identifier la spécification de profil publiée comme étant implémentée.</span><span class="sxs-lookup"><span data-stu-id="20c1c-121">Used to identify the profile specification that is advertised as being implemented.</span></span> <span data-ttu-id="20c1c-122">Cette classe spécifie les informations qui incluent le nom du profil, l’organisation et la version avec lesquelles l’implémentation est conforme.</span><span class="sxs-lookup"><span data-stu-id="20c1c-122">This class specifies information that includes the profile name, organization, and version with which the implementation is compliant.</span></span>

</dd> <dt>

<span data-ttu-id="20c1c-123"><span id="CIM_ElementConformsToProfile"></span><span id="cim_elementconformstoprofile"></span><span id="CIM_ELEMENTCONFORMSTOPROFILE"></span>[**\_ELEMENTCONFORMSTOPROFILE CIM**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile)</span><span class="sxs-lookup"><span data-stu-id="20c1c-123"><span id="CIM_ElementConformsToProfile"></span><span id="cim_elementconformstoprofile"></span><span id="CIM_ELEMENTCONFORMSTOPROFILE"></span>[**CIM\_ElementConformsToProfile**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile)</span></span>
</dt> <dd>

<span data-ttu-id="20c1c-124">Utilisé pour associer des instances d’éléments de gestion définis dans des profils à la classe [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) qui identifie les spécifications de profil spécifiques qui sont implémentées.</span><span class="sxs-lookup"><span data-stu-id="20c1c-124">Used to associate instances of management elements that are defined in profiles with the [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) class that identifies the particular profile specifications that are implemented.</span></span>

</dd> <dt>

<span data-ttu-id="20c1c-125"><span id="CIM_ReferencedProfile"></span><span id="cim_referencedprofile"></span><span id="CIM_REFERENCEDPROFILE"></span>[**\_REFERENCEDPROFILE CIM**](cim-referencedprofile.md)</span><span class="sxs-lookup"><span data-stu-id="20c1c-125"><span id="CIM_ReferencedProfile"></span><span id="cim_referencedprofile"></span><span id="CIM_REFERENCEDPROFILE"></span>[**CIM\_ReferencedProfile**](cim-referencedprofile.md)</span></span>
</dt> <dd>

<span data-ttu-id="20c1c-126">Utilisé pour représenter la relation entre les profils.</span><span class="sxs-lookup"><span data-stu-id="20c1c-126">Used to represent the relationship between profiles.</span></span>

</dd> </dl>

## <a name="implementing-cross-namespace-association-traversal"></a><span data-ttu-id="20c1c-127">Implémentation du parcours des associations entre espaces de noms</span><span class="sxs-lookup"><span data-stu-id="20c1c-127">Implementing Cross-Namespace Association Traversal</span></span>

<span data-ttu-id="20c1c-128">Le service WMI autorise le parcours de l’association entre espaces de noms.</span><span class="sxs-lookup"><span data-stu-id="20c1c-128">The WMI service allows cross-namespace association traversal.</span></span> <span data-ttu-id="20c1c-129">WMI fournit l’espace de noms Interop pour inscrire des profils et les associer aux profils qui sont implémentés dans différents espaces de noms.</span><span class="sxs-lookup"><span data-stu-id="20c1c-129">WMI provides the interop namespace for registering profiles and associating them with profiles that are implemented in different namespaces.</span></span> <span data-ttu-id="20c1c-130">Toutefois, pour utiliser le parcours d’association, les implémenteurs doivent instancier les classes de profil dans l’interopérabilité et dans l’espace de noms implémenté.</span><span class="sxs-lookup"><span data-stu-id="20c1c-130">However, to use association traversal, implementers must instantiate the profile classes both in the interop and in the implemented namespace.</span></span> <span data-ttu-id="20c1c-131">Pour plus d’informations, consultez [écriture d’un fournisseur d’associations pour l’interopérabilité](writing-an-association-provider-for-interop.md).</span><span class="sxs-lookup"><span data-stu-id="20c1c-131">For more information, see [Writing an Association Provider for Interop](writing-an-association-provider-for-interop.md).</span></span>

<span data-ttu-id="20c1c-132">Les associations qui traversent des espaces de noms dans le même environnement de gestion doivent être instanciées à la fois dans les espaces de noms Interop et Implemented.</span><span class="sxs-lookup"><span data-stu-id="20c1c-132">Associations that cross namespaces within the same management environment must be instantiated in both the interop and implemented namespaces.</span></span> <span data-ttu-id="20c1c-133">Dans le cas contraire, la traversée d’association ne fonctionnera pas.</span><span class="sxs-lookup"><span data-stu-id="20c1c-133">Otherwise, association traversal will not work.</span></span> <span data-ttu-id="20c1c-134">Par exemple, le fournisseur d’associations Power profile doit être inscrit avec les espaces de noms root/Interop et root/cimv2/Power.</span><span class="sxs-lookup"><span data-stu-id="20c1c-134">For example, the power profile association provider must be registered with both root/interop and root/cimv2/power namespaces.</span></span> <span data-ttu-id="20c1c-135">La traversée d’association doit pouvoir se produire à partir de l’espace de noms vers l’autre.</span><span class="sxs-lookup"><span data-stu-id="20c1c-135">Association traversal should be able to occur from either namespace back to the other.</span></span> <span data-ttu-id="20c1c-136">Pour obtenir des exemples de parcours d’association, consultez [accès aux données dans l’espace de noms Interop](accessing-data-in-the-interop-namespace.md).</span><span class="sxs-lookup"><span data-stu-id="20c1c-136">For examples of association traversal, see [Accessing Data in the Interop Namespace](accessing-data-in-the-interop-namespace.md).</span></span>

<span data-ttu-id="20c1c-137">\* \* Windows Vista : \* \*</span><span class="sxs-lookup"><span data-stu-id="20c1c-137">\*\*Windows Vista:  \*\*</span></span>

<span data-ttu-id="20c1c-138">Après la mise à niveau vers Windows 7, si des profils d’appareils d’interopérabilité étaient précédemment installés dans l’espace de noms racine/Interop, aucun profil Windows 7 n’est installé.</span><span class="sxs-lookup"><span data-stu-id="20c1c-138">After upgrading to Windows 7, if there are interop device profiles that were previously installed in the root/interop namespace, no Windows 7 profiles will be installed.</span></span> <span data-ttu-id="20c1c-139">Ces objets de profil tiers remplacent le schéma d’interopérabilité de Windows 7 pour gérer les fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="20c1c-139">These third-party profile objects overwrite Windows 7 interop schema to maintain functionality.</span></span> <span data-ttu-id="20c1c-140">En outre, l’ID d’événement 5631 de l’application WMI est enregistré.</span><span class="sxs-lookup"><span data-stu-id="20c1c-140">Additionally, the WMI application event ID 5631 is recorded.</span></span>

<span data-ttu-id="20c1c-141">Pour récupérer les profils d’interopérabilité de Windows 7, la version Windows 7 du fichier Interop. mof et les fichiers MFL associés doivent être compilés.</span><span class="sxs-lookup"><span data-stu-id="20c1c-141">To get the Windows 7 interop profiles, the Windows 7 version of the Interop.mof file and the related MFL files must be compiled.</span></span> <span data-ttu-id="20c1c-142">Pour plus d’informations, consultez [compilation des fichiers MOF](compiling-mof-files.md).</span><span class="sxs-lookup"><span data-stu-id="20c1c-142">For more information, see [Compiling MOF Files](compiling-mof-files.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="20c1c-143">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="20c1c-143">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="20c1c-144">[**\_REGISTEREDPROFILE CIM**](/previous-versions//ee309375(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="20c1c-144">[**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="20c1c-145">**\_ELEMENTCONFORMSTOPROFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="20c1c-145">**CIM\_ElementConformsToProfile**</span></span>](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile)
</dt> <dt>

[<span data-ttu-id="20c1c-146">**\_REFERENCEDPROFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="20c1c-146">**CIM\_ReferencedProfile**</span></span>](cim-referencedprofile.md)
</dt> <dt>

[<span data-ttu-id="20c1c-147">Compatibilité du schéma CIM</span><span class="sxs-lookup"><span data-stu-id="20c1c-147">CIM Schema Compatibility</span></span>](cim-schema-compatibility.md)
</dt> <dt>

[<span data-ttu-id="20c1c-148">Écriture d’un fournisseur d’association pour l’interopérabilité</span><span class="sxs-lookup"><span data-stu-id="20c1c-148">Writing an Association Provider for Interop</span></span>](writing-an-association-provider-for-interop.md)
</dt> <dt>

[<span data-ttu-id="20c1c-149">Accès aux données dans l’espace de noms Interop</span><span class="sxs-lookup"><span data-stu-id="20c1c-149">Accessing Data in the Interop Namespace</span></span>](accessing-data-in-the-interop-namespace.md)
</dt> </dl>

 

 
