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
# <a name="packaging-deployment-and-query-glossary"></a>Glossaire de l’empaquetage, du déploiement et de la requête

<dl> <dt>

<span id="appxpkg.appx_packaging_glossary_application_user_model_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_APPLICATION_USER_MODEL_ID"></span>**ID de modèle d’utilisateur d’application**
</dt> <dd>

L’ID de modèle utilisateur de l’application identifie de façon unique une application sur le système d’exploitation afin que le système d’exploitation puisse envoyer des notifications, et ainsi de suite, à l’application.

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_block_map"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_BLOCK_MAP"></span>**mappage de bloc**
</dt> <dd>

Définit les index et les hachages de chiffrement pour les blocs de code exécutable et les données stockées dans les fichiers d’un package d’application. Un fichier de BlockMap.xml est requis pour chaque package d’application.

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_dependency_package"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_DEPENDENCY_PACKAGE"></span>**package de dépendance**
</dt> <dd>

Package dont dépend un autre package. La dépendance est déclarée dans le manifeste du package dépendant et non dans le manifeste du package de dépendances.

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_dependent_package"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_DEPENDENT_PACKAGE"></span>**package dépendant**
</dt> <dd>

Package qui prend une dépendance sur un autre package. La dépendance est déclarée dans le manifeste du package dépendant.

</dd> <dt>

<span id="appxpkg_packaging_glossary_footpint_files"></span><span id="APPXPKG_PACKAGING_GLOSSARY_FOOTPINT_FILES"></span>**fichiers d’encombrement**
</dt> <dd>

Fichiers dans un package d’application qui ne font pas partie de l’application à déployer. Ces fichiers fournissent des métadonnées relatives au package. Les fichiers d’encombrement standard incluent le manifeste, le mappage de bloc, le mappage de flux et la signature numérique. Les fichiers d’encombrement sont créés dans le cadre du processus de génération du package. En outre, conformément à la spécification OPC, \[ Content \_ types \] . xml et les fichiers dont les noms correspondent au \* \\ \_ modèle « rels \\ \* . rels » sont des fichiers d’encombrement.

</dd> <dt>

<span id="appxpkg_packaging_glossary_manifest"></span><span id="APPXPKG_PACKAGING_GLOSSARY_MANIFEST"></span>**du**
</dt> <dd>

Fichier XML qui décrit le contenu et les métadonnées associés à un package, y compris l’ID de package. Un fichier manifeste XML est requis pour chaque package d’application.

</dd> <dt>

<span id="appxpkg_packaging_glossary_opc"></span><span id="APPXPKG_PACKAGING_GLOSSARY_OPC"></span>**OPC**
</dt> <dd>

Open Packaging Conventions (OPC) décrit une technologie de fichier conteneur qui est documentée dans les normes ISO/IEC 29500 et ECMA 376. Les packages d’application sont conformes à OPC.

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_package"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE"></span>**Packages**
</dt> <dd>

Unité de déploiement, de gestion et de maintenance du logiciel associée au modèle d’empaquetage d’applications. Un package contient les fichiers qui constituent l’application, ainsi qu’un fichier manifeste décrivant le logiciel à Windows.

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_package_family_moniker"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_FAMILY_MONIKER"></span>**nom de la famille de packages**
</dt> <dd>

Forme sérialisée de l’ID de package qui représente de façon unique la famille de packages sur l’ordinateur. Il convient pour nommer des objets tels que des fichiers et des dossiers. Le nom de la famille de packages est semblable au nom complet du package, mais il n’y a que le nom et le serveur de publication. Étant donné qu’elle exclut les informations qui changent avec la maintenance (version, architecture et informations sur les ressources), elle est utile pour les références indépendantes de la version du package.

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_package_moniker"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_MONIKER"></span>**nom complet du package**
</dt> <dd>

Forme sérialisée de l’ID de package qui représente de façon unique cette version du package sur l’ordinateur. Il convient pour nommer des objets tels que des fichiers et des dossiers.

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_package_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_ID"></span>**ID du package**
</dt> <dd>

Identificateur global unique d’un package. Il se compose d’un tuple d’attributs pour le package, notamment le nom, l’éditeur, l’architecture prise en charge, les informations sur les ressources et la version. Consultez nom complet du package et nom de la famille de packages pour les formes sérialisées de l’ID de package.

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_package_relative_application_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_RELATIVE_APPLICATION_ID"></span>**ID d’application relative du package**
</dt> <dd>

L’attribut **ID** de l’élément [**application**](/uwp/schemas/appxpackage/appxmanifestschema2010-v2/element-application) dans le manifeste du package, également appelé Praid. Cette chaîne identifie de façon unique une application dans un package. Cet attribut est obligatoire pour l’élément **application** .

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_payload_file"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PAYLOAD_FILE"></span>**fichiers de charge utile**
</dt> <dd>

Fichiers dans un package d’application qui font partie de l’application à déployer. Ces fichiers sont extraits et placés dans le dossier d’installation de l’utilisateur.

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_resource_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_RESOURCE_ID"></span>**ID de ressource**
</dt> <dd>

Partie facultative d’un ID de package utilisée pour différencier les ressources dans le package. Par exemple, un ID de ressource peut être utilisé pour spécifier la langue ou les paramètres régionaux.

</dd> <dt>

<span id="appxpkg.appx_packaging_glossary_zip_central_directory"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_ZIP_CENTRAL_DIRECTORY"></span>**Répertoire ZIP central**
</dt> <dd>

Séquences d’octets dans un fichier ZIP qui stockent les métadonnées relatives à l’archive ZIP et son contenu, y compris le nom, la taille, les paramètres de compression et l’emplacement au sein de l’archive.

</dd> </dl>

 

 