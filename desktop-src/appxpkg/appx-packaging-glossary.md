---
title: Glossaire de l’empaquetage, du déploiement et de la requête
description: Fournit des définitions pour les termes liés à l’empaquetage, au déploiement et à la requête pour les applications Windows.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 15E35DCF-C6C1-446A-B09B-6428F9C8A677
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83a2112b593e2d2a5aaf4f06525160e2d799bad1
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104381774"
---
# <a name="packaging-deployment-and-query-glossary"></a><span data-ttu-id="54ca3-103">Glossaire de l’empaquetage, du déploiement et de la requête</span><span class="sxs-lookup"><span data-stu-id="54ca3-103">Packaging, deployment, and query glossary</span></span>

<dl> <dt>

<span data-ttu-id="54ca3-104"><span id="appxpkg.appx_packaging_glossary_application_user_model_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_APPLICATION_USER_MODEL_ID"></span>**ID de modèle d’utilisateur d’application**</span><span class="sxs-lookup"><span data-stu-id="54ca3-104"><span id="appxpkg.appx_packaging_glossary_application_user_model_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_APPLICATION_USER_MODEL_ID"></span>**application user model ID**</span></span>
</dt> <dd>

<span data-ttu-id="54ca3-105">L’ID de modèle utilisateur de l’application identifie de façon unique une application sur le système d’exploitation afin que le système d’exploitation puisse envoyer des notifications, et ainsi de suite, à l’application.</span><span class="sxs-lookup"><span data-stu-id="54ca3-105">The application user model ID uniquely identifies an app on the operating system so the operating system can send notifications and so on to the app.</span></span>

</dd> <dt>

<span data-ttu-id="54ca3-106"><span id="appxpkg.appx_packaging_glossary_block_map"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_BLOCK_MAP"></span>**mappage de bloc**</span><span class="sxs-lookup"><span data-stu-id="54ca3-106"><span id="appxpkg.appx_packaging_glossary_block_map"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_BLOCK_MAP"></span>**block map**</span></span>
</dt> <dd>

<span data-ttu-id="54ca3-107">Définit les index et les hachages de chiffrement pour les blocs de code exécutable et les données stockées dans les fichiers d’un package d’application.</span><span class="sxs-lookup"><span data-stu-id="54ca3-107">Defines the indices and cryptographic hashes for blocks of executable code and data that are stored in the files of an app package.</span></span> <span data-ttu-id="54ca3-108">Un fichier de BlockMap.xml est requis pour chaque package d’application.</span><span class="sxs-lookup"><span data-stu-id="54ca3-108">A BlockMap.xml file is required for every app package.</span></span>

</dd> <dt>

<span data-ttu-id="54ca3-109"><span id="appxpkg.appx_packaging_glossary_dependency_package"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_DEPENDENCY_PACKAGE"></span>**package de dépendance**</span><span class="sxs-lookup"><span data-stu-id="54ca3-109"><span id="appxpkg.appx_packaging_glossary_dependency_package"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_DEPENDENCY_PACKAGE"></span>**dependency package**</span></span>
</dt> <dd>

<span data-ttu-id="54ca3-110">Package dont dépend un autre package.</span><span class="sxs-lookup"><span data-stu-id="54ca3-110">A package on which another package depends.</span></span> <span data-ttu-id="54ca3-111">La dépendance est déclarée dans le manifeste du package dépendant et non dans le manifeste du package de dépendances.</span><span class="sxs-lookup"><span data-stu-id="54ca3-111">The dependency is declared in the dependent package's manifest and not in the dependency package's manifest.</span></span>

</dd> <dt>

<span data-ttu-id="54ca3-112"><span id="appxpkg.appx_packaging_glossary_dependent_package"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_DEPENDENT_PACKAGE"></span>**package dépendant**</span><span class="sxs-lookup"><span data-stu-id="54ca3-112"><span id="appxpkg.appx_packaging_glossary_dependent_package"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_DEPENDENT_PACKAGE"></span>**dependent package**</span></span>
</dt> <dd>

<span data-ttu-id="54ca3-113">Package qui prend une dépendance sur un autre package.</span><span class="sxs-lookup"><span data-stu-id="54ca3-113">A package that takes a dependency on another package.</span></span> <span data-ttu-id="54ca3-114">La dépendance est déclarée dans le manifeste du package dépendant.</span><span class="sxs-lookup"><span data-stu-id="54ca3-114">The dependency is declared in the dependent package's manifest.</span></span>

</dd> <dt>

<span data-ttu-id="54ca3-115"><span id="appxpkg_packaging_glossary_footpint_files"></span><span id="APPXPKG_PACKAGING_GLOSSARY_FOOTPINT_FILES"></span>**fichiers d’encombrement**</span><span class="sxs-lookup"><span data-stu-id="54ca3-115"><span id="appxpkg_packaging_glossary_footpint_files"></span><span id="APPXPKG_PACKAGING_GLOSSARY_FOOTPINT_FILES"></span>**footprint files**</span></span>
</dt> <dd>

<span data-ttu-id="54ca3-116">Fichiers dans un package d’application qui ne font pas partie de l’application à déployer.</span><span class="sxs-lookup"><span data-stu-id="54ca3-116">Files within an app package that are not part of the app to be deployed.</span></span> <span data-ttu-id="54ca3-117">Ces fichiers fournissent des métadonnées relatives au package.</span><span class="sxs-lookup"><span data-stu-id="54ca3-117">These files provide metadata pertaining to the package.</span></span> <span data-ttu-id="54ca3-118">Les fichiers d’encombrement standard incluent le manifeste, le mappage de bloc, le mappage de flux et la signature numérique.</span><span class="sxs-lookup"><span data-stu-id="54ca3-118">Standard footprint files include the manifest, block map, stream map, and digital signature.</span></span> <span data-ttu-id="54ca3-119">Les fichiers d’encombrement sont créés dans le cadre du processus de génération du package.</span><span class="sxs-lookup"><span data-stu-id="54ca3-119">Footprint files are created as part of the package build process.</span></span> <span data-ttu-id="54ca3-120">En outre, conformément à la spécification OPC, \[ Content \_ types \] . xml et les fichiers dont les noms correspondent au \* \\ \_ modèle « rels \\ \* . rels » sont des fichiers d’encombrement.</span><span class="sxs-lookup"><span data-stu-id="54ca3-120">In addition per the OPC specification, \[Content\_Types\].xml and files whose names match the "\*\\\_rels\\\*.rels" pattern are footprint files.</span></span>

</dd> <dt>

<span data-ttu-id="54ca3-121"><span id="appxpkg_packaging_glossary_manifest"></span><span id="APPXPKG_PACKAGING_GLOSSARY_MANIFEST"></span>**du**</span><span class="sxs-lookup"><span data-stu-id="54ca3-121"><span id="appxpkg_packaging_glossary_manifest"></span><span id="APPXPKG_PACKAGING_GLOSSARY_MANIFEST"></span>**manifest**</span></span>
</dt> <dd>

<span data-ttu-id="54ca3-122">Fichier XML qui décrit le contenu et les métadonnées associés à un package, y compris l’ID de package.</span><span class="sxs-lookup"><span data-stu-id="54ca3-122">An XML file that describes the contents and metadata associated with a package including the package ID.</span></span> <span data-ttu-id="54ca3-123">Un fichier manifeste XML est requis pour chaque package d’application.</span><span class="sxs-lookup"><span data-stu-id="54ca3-123">A manifest XML file is required for every app package.</span></span>

</dd> <dt>

<span data-ttu-id="54ca3-124"><span id="appxpkg_packaging_glossary_opc"></span><span id="APPXPKG_PACKAGING_GLOSSARY_OPC"></span>**OPC**</span><span class="sxs-lookup"><span data-stu-id="54ca3-124"><span id="appxpkg_packaging_glossary_opc"></span><span id="APPXPKG_PACKAGING_GLOSSARY_OPC"></span>**OPC**</span></span>
</dt> <dd>

<span data-ttu-id="54ca3-125">Open Packaging Conventions (OPC) décrit une technologie de fichier conteneur qui est documentée dans les normes ISO/IEC 29500 et ECMA 376.</span><span class="sxs-lookup"><span data-stu-id="54ca3-125">Open Packaging Conventions (OPC) describes a container-file technology that is documented in the ISO/IEC 29500 and ECMA 376 standards.</span></span> <span data-ttu-id="54ca3-126">Les packages d’application sont conformes à OPC.</span><span class="sxs-lookup"><span data-stu-id="54ca3-126">App packages are OPC-compliant.</span></span>

</dd> <dt>

<span data-ttu-id="54ca3-127"><span id="appxpkg.appx_packaging_glossary_package"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE"></span>**Packages**</span><span class="sxs-lookup"><span data-stu-id="54ca3-127"><span id="appxpkg.appx_packaging_glossary_package"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE"></span>**package**</span></span>
</dt> <dd>

<span data-ttu-id="54ca3-128">Unité de déploiement, de gestion et de maintenance du logiciel associée au modèle d’empaquetage d’applications.</span><span class="sxs-lookup"><span data-stu-id="54ca3-128">The unit of deployment, management, and servicing software associated with the app packaging model.</span></span> <span data-ttu-id="54ca3-129">Un package contient les fichiers qui constituent l’application, ainsi qu’un fichier manifeste décrivant le logiciel à Windows.</span><span class="sxs-lookup"><span data-stu-id="54ca3-129">A package contains the files that constitute the app, along with a manifest file that describes the software to Windows.</span></span>

</dd> <dt>

<span data-ttu-id="54ca3-130"><span id="appxpkg.appx_packaging_glossary_package_family_moniker"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_FAMILY_MONIKER"></span>**nom de la famille de packages**</span><span class="sxs-lookup"><span data-stu-id="54ca3-130"><span id="appxpkg.appx_packaging_glossary_package_family_moniker"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_FAMILY_MONIKER"></span>**package family name**</span></span>
</dt> <dd>

<span data-ttu-id="54ca3-131">Forme sérialisée de l’ID de package qui représente de façon unique la famille de packages sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="54ca3-131">A serialized form of the package ID that uniquely represents the package family on the computer.</span></span> <span data-ttu-id="54ca3-132">Il convient pour nommer des objets tels que des fichiers et des dossiers.</span><span class="sxs-lookup"><span data-stu-id="54ca3-132">It is suitable for naming objects such as files and folders.</span></span> <span data-ttu-id="54ca3-133">Le nom de la famille de packages est semblable au nom complet du package, mais il n’y a que le nom et le serveur de publication.</span><span class="sxs-lookup"><span data-stu-id="54ca3-133">The package family name is similar to the package full name, but includes only the name and publisher.</span></span> <span data-ttu-id="54ca3-134">Étant donné qu’elle exclut les informations qui changent avec la maintenance (version, architecture et informations sur les ressources), elle est utile pour les références indépendantes de la version du package.</span><span class="sxs-lookup"><span data-stu-id="54ca3-134">Because it excludes info that changes with servicing (version, architecture, and resource info), it is useful for version-independent references to the package.</span></span>

</dd> <dt>

<span data-ttu-id="54ca3-135"><span id="appxpkg.appx_packaging_glossary_package_moniker"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_MONIKER"></span>**nom complet du package**</span><span class="sxs-lookup"><span data-stu-id="54ca3-135"><span id="appxpkg.appx_packaging_glossary_package_moniker"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_MONIKER"></span>**package full name**</span></span>
</dt> <dd>

<span data-ttu-id="54ca3-136">Forme sérialisée de l’ID de package qui représente de façon unique cette version du package sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="54ca3-136">A serialized form of the package ID that uniquely represents this version of the package on the computer.</span></span> <span data-ttu-id="54ca3-137">Il convient pour nommer des objets tels que des fichiers et des dossiers.</span><span class="sxs-lookup"><span data-stu-id="54ca3-137">It is suitable for naming objects such as files and folders.</span></span>

</dd> <dt>

<span data-ttu-id="54ca3-138"><span id="appxpkg.appx_packaging_glossary_package_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_ID"></span>**ID du package**</span><span class="sxs-lookup"><span data-stu-id="54ca3-138"><span id="appxpkg.appx_packaging_glossary_package_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_ID"></span>**package ID**</span></span>
</dt> <dd>

<span data-ttu-id="54ca3-139">Identificateur global unique d’un package.</span><span class="sxs-lookup"><span data-stu-id="54ca3-139">A globally unique identifier for a package.</span></span> <span data-ttu-id="54ca3-140">Il se compose d’un tuple d’attributs pour le package, notamment le nom, l’éditeur, l’architecture prise en charge, les informations sur les ressources et la version.</span><span class="sxs-lookup"><span data-stu-id="54ca3-140">It is composed of a tuple of attributes for the package including name, publisher, supported architecture, resource info, and version.</span></span> <span data-ttu-id="54ca3-141">Consultez nom complet du package et nom de la famille de packages pour les formes sérialisées de l’ID de package.</span><span class="sxs-lookup"><span data-stu-id="54ca3-141">See package full name and package family name for serialized forms of the package ID.</span></span>

</dd> <dt>

<span data-ttu-id="54ca3-142"><span id="appxpkg.appx_packaging_glossary_package_relative_application_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_RELATIVE_APPLICATION_ID"></span>**ID d’application relative du package**</span><span class="sxs-lookup"><span data-stu-id="54ca3-142"><span id="appxpkg.appx_packaging_glossary_package_relative_application_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_RELATIVE_APPLICATION_ID"></span>**package relative application ID**</span></span>
</dt> <dd>

<span data-ttu-id="54ca3-143">L’attribut **ID** de l’élément [**application**](/uwp/schemas/appxpackage/appxmanifestschema2010-v2/element-application) dans le manifeste du package, également appelé Praid.</span><span class="sxs-lookup"><span data-stu-id="54ca3-143">The **Id** attribute on the [**Application**](/uwp/schemas/appxpackage/appxmanifestschema2010-v2/element-application) element within the package manifest, which is also known as PRAID.</span></span> <span data-ttu-id="54ca3-144">Cette chaîne identifie de façon unique une application dans un package.</span><span class="sxs-lookup"><span data-stu-id="54ca3-144">This string uniquely identifies an app within a package.</span></span> <span data-ttu-id="54ca3-145">Cet attribut est obligatoire pour l’élément **application** .</span><span class="sxs-lookup"><span data-stu-id="54ca3-145">This attribute is required for the **Application** element.</span></span>

</dd> <dt>

<span data-ttu-id="54ca3-146"><span id="appxpkg.appx_packaging_glossary_payload_file"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PAYLOAD_FILE"></span>**fichiers de charge utile**</span><span class="sxs-lookup"><span data-stu-id="54ca3-146"><span id="appxpkg.appx_packaging_glossary_payload_file"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PAYLOAD_FILE"></span>**payload files**</span></span>
</dt> <dd>

<span data-ttu-id="54ca3-147">Fichiers dans un package d’application qui font partie de l’application à déployer.</span><span class="sxs-lookup"><span data-stu-id="54ca3-147">The files within an app package that are part of the app to be deployed.</span></span> <span data-ttu-id="54ca3-148">Ces fichiers sont extraits et placés dans le dossier d’installation de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="54ca3-148">These files are extracted and placed in the user's installation folder.</span></span>

</dd> <dt>

<span data-ttu-id="54ca3-149"><span id="appxpkg.appx_packaging_glossary_resource_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_RESOURCE_ID"></span>**ID de ressource**</span><span class="sxs-lookup"><span data-stu-id="54ca3-149"><span id="appxpkg.appx_packaging_glossary_resource_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_RESOURCE_ID"></span>**resource ID**</span></span>
</dt> <dd>

<span data-ttu-id="54ca3-150">Partie facultative d’un ID de package utilisée pour différencier les ressources dans le package.</span><span class="sxs-lookup"><span data-stu-id="54ca3-150">An optional part of a package ID that is used to differentiate the resources in the package.</span></span> <span data-ttu-id="54ca3-151">Par exemple, un ID de ressource peut être utilisé pour spécifier la langue ou les paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="54ca3-151">For example, a resource ID can be used to specify the language or locale.</span></span>

</dd> <dt>

<span data-ttu-id="54ca3-152"><span id="appxpkg.appx_packaging_glossary_zip_central_directory"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_ZIP_CENTRAL_DIRECTORY"></span>**Répertoire ZIP central**</span><span class="sxs-lookup"><span data-stu-id="54ca3-152"><span id="appxpkg.appx_packaging_glossary_zip_central_directory"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_ZIP_CENTRAL_DIRECTORY"></span>**ZIP central directory**</span></span>
</dt> <dd>

<span data-ttu-id="54ca3-153">Séquences d’octets dans un fichier ZIP qui stockent les métadonnées relatives à l’archive ZIP et son contenu, y compris le nom, la taille, les paramètres de compression et l’emplacement au sein de l’archive.</span><span class="sxs-lookup"><span data-stu-id="54ca3-153">The byte sequences in a ZIP file that store metadata about the ZIP archive and its contents including name, size, compression settings, and location within the archive.</span></span>

</dd> </dl>

 

 