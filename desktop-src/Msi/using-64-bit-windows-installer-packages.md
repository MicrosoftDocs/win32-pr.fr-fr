---
description: respectez les consignes suivantes lors de la création d’un package Windows Installer bits 64.
ms.assetid: e7dfd188-fd4d-49d6-8cf5-c17182b697ca
title: utilisation de Packages Windows Installers 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9c3bca5c666f7a6a0f1757efca40a26b1406d4241abf7d32a066c2d7fa01b92
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809089"
---
# <a name="using-64-bit-windows-installer-packages"></a>utilisation de Packages Windows Installers 64 bits

lorsque vous créez des [packages ou des applications Windows Installer bits 64](64-bit-windows-installer-packages.md) qui appellent Windows Installer pour installer des packages 64 bits, procédez comme suit :

-   utilisez un schéma de base de données Windows Installer de 200 ou une version ultérieure. Spécifiez que la version 2,0 est la version minimale du programme d’installation requis pour installer le package en affectant à la propriété [**Résumé du nombre de pages**](page-count-summary.md) la valeur de l’entier 200. les versions antérieures de Windows Installer rejettent les tentatives d’installation des packages 64 bits. pour les packages 64 bits sur la plateforme Arm64, le schéma de base de données Windows Installer doit être 500 ou version ultérieure.
-   Indiquez dans la propriété [**Résumé du modèle**](template-summary.md) du flux d’informations Résumé du package qu’il s’agit d’un package 64 bits. Entrez « Intel64 » dans le champ plateforme de la propriété **Résumé du modèle** si le package doit être exécuté sur un processeur Intel64. Entrez « x64 » si le package doit être exécuté sur un processeur étendu 64 bits. Entrez « Arm64 » si le package doit être exécuté sur un processeur Arm64. Un package ne peut pas être marqué comme prenant en charge les plateformes Intel64 et x64, la valeur de propriété de **Résumé de modèle** « Intel64, x64 » n’est pas valide. Un package ne peut pas être marqué comme prenant en charge les plateformes 32 bits et 64 bits, les valeurs de propriété de **Résumé de modèle** « Intel, x64 » ou « Intel, Intel64 » ne sont pas valides.
-   Identifiez chaque composant 64 bits en définissant **msidbComponentAttributes64bit** dans la colonne attributs de la table des [composants](component-table.md) .
-   Utilisez des instructions conditionnelles facultatives qui vérifient la version du système d’exploitation 64 bits en référençant la propriété [**VersionNT64**](versionnt64.md) . Windows le programme d’installation définit cette propriété sur la version 64 bits Windows et laisse VersionNT64 non défini si le système d’exploitation n’est pas Windows 64 bits. Pour plus d’informations, consultez [utilisation des propriétés dans des instructions conditionnelles](using-properties-in-conditional-statements.md).
-   Utilisez des instructions conditionnelles facultatives qui vérifient le niveau de processeur numérique de l’ordinateur en référençant la propriété [**Intel64**](intel64.md) ou [**Msix64**](msix64.md) . le Windows Installer définit ces propriétés au niveau du processeur numérique actuel de l’ordinateur et laisse la propriété **Intel64** non définie si ce n’est pas un processeur itanium. Pour plus d’informations, consultez [utilisation des propriétés dans des instructions conditionnelles](using-properties-in-conditional-statements.md).
-   Utilisez la [table AppSearch](appsearch-table.md) et l' [action AppSearch](appsearch-action.md) pour effectuer des recherches facultatives dans le registre pour les composants 64 bits existants. Pour rechercher des composants 64 bits existants, incluez le bit **msidbLocatorType64bit** dans la colonne type de la [table RegLocator](reglocator-table.md). Pour plus d’informations, consultez [recherche d’applications, de fichiers, d’entrées de registre ou de .ini propriété entrées de fichier existantes](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md)
-   Obtenez les chemins d’accès aux dossiers système en référençant la propriété [**System64Folder**](system64folder.md), la propriété [**ProgramFiles64Folder**](programfiles64folder.md) et la propriété [**CommonFiles64Folder**](commonfiles64folder.md) pour les dossiers 64 bits et la propriété [**SystemFolder**](systemfolder.md) , la propriété [**ProgramFilesFolder**](programfilesfolder.md) et la propriété [**CommonFilesFolder**](commonfilesfolder.md) pour les dossiers 32 bits.
-   Vérifiez que l’application utilise le GUID correct lors du référencement d’un composant 64 bits. S’il existe des versions 32 bits et 64 bits d’un composant spécifique, ceux-ci doivent avoir des GUID d’ID de composant différents.
-   Déterminez si de nouvelles variables d’environnement doivent être définies lors de l’installation d’applications 64 bits.
-   Si un gestionnaire de pilotes ODBC 64 bits doit être installé, le composant qui le contient doit être nommé ODBCDriverManager64. Le gestionnaire de pilotes ODBC doit être créé dans le package d’installation et un composant nommé ODBCDriverManager64 doit être inclus. Le gestionnaire sera installé si nécessaire.
-   Vérifiez que l’application appelle uniquement des services 32 bits qui s’exécutent en tant qu’exécutables. Les applications ne doivent pas appeler les services 32 bits qui s’exécutent dans des dll.
-   Si l’application installe les versions d’un composant coexistantes de 32 bits et 64 bits, vérifiez que l’application partage .ini informations de fichier correctement.
-   Vérifiez que l’application applique uniquement les correctifs 32 bits aux binaires 32 bits et les correctifs 64 bits aux fichiers binaires 64 bits.
-   Tenez compte des scénarios de mise à niveau futurs pour les versions 32 bits et 64 bits et tenez à jour les codes de mise à niveau. Pour plus d’informations, consultez [mise à jour corrective et mises à niveau](patching-and-upgrades.md).
-   quand vous utilisez une application d' [amorçage](bootstrapping.md) pour installer un [Package Windows Installer 64 bits](64-bit-windows-installer-packages.md), compilez l’application d’amorçage comme une application 64 bits.
-   Pour désactiver la [réflexion du Registre](../winprog64/registry-reflection.md) pour les clés de Registre qui sont affectées par un composant particulier, définissez le bit **msidbComponentAttributesDisableRegistryReflection** dans le champ attributs de la table des [composants](component-table.md) . Cela peut être nécessaire pour que les copies 32 bits et 64 bits de la même application coexistent. si ce bit est défini, le Windows Installer appelle la fonction [**RegDisableReflectionKey**](/windows/win32/api/winreg/nf-winreg-regdisablereflectionkey) sur chaque clé à laquelle le composant accède. ce bit est disponible avec la version 4,0 de Windows Installer. Ce bit est ignoré sur les systèmes 32 bits. ce bit est ignoré sur les versions 64 bits de Windows XP et Windows 2000.

> [!Note]  
> La valeur de la racine de Registre numérique retournée par le paramètre *lpPathBuf* de la fonction [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) distingue les composants sur les systèmes d’exploitation 32 bits et 64 bits. Pour plus d’informations, consultez fonction **MsiGetComponentPath** .

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Actions personnalisées 64 bits](64-bit-custom-actions.md)
</dt> </dl>

 

 
