---
description: La capacité des Windows Installer à définir des autorisations d’accès sur les services, les fichiers, les dossiers créés et les entrées de Registre peut aider à renforcer la sécurité des applications d’installation.
ms.assetid: a25fcecf-f15f-4772-8f41-d03864484cc9
title: Sécurisation des ressources
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 415fe7b2df343a54aa0819031f4fd22b05857618
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534312"
---
# <a name="securing-resources"></a>Sécurisation des ressources

La capacité des Windows Installer à définir des autorisations d’accès sur les services, les fichiers, les dossiers créés et les entrées de Registre peut aider à renforcer la sécurité des applications d’installation. L’utilisation des tables [MsiLockPermissionsEx](msilockpermissionsex-table.md) ou [LockPermissions](lockpermissions-table.md) pour sécuriser les ressources est l’une des [recommandations recommandées pour la création d’installations sécurisées](guidelines-for-authoring-secure-installations.md). La table MsiLockPermissionsEx peut permettre à un auteur de package de sécuriser une ressource sans avoir à écrire une [action personnalisée](custom-actions.md).

À partir de packages développés pour Windows Installer 5,0, la table [MsiLockPermissionsEx](msilockpermissionsex-table.md) doit remplacer l’utilisation de la table [LockPermissions](lockpermissions-table.md) . Les fonctionnalités étendues fournies par la table MsiLockPermissionsEx permettent à un package de sécuriser les [services](../services/services.md)Windows, les fichiers, les dossiers et les clés de registre. Un package ne doit pas contenir à la fois les tables MsiLockPermissionsEx et LockPermissions.

Windows Installer 4,5 et les versions antérieures ignorent la [table MsiLockPermissionsEx](msilockpermissionsex-table.md). À partir de Windows Installer 5,0, l’installation échoue avec un message d’erreur 1941 si le package contient à la fois une [table LockPermissions](lockpermissions-table.md) et une table MsiLockPermissionsEx. Les packages d’installation existants qui contiennent uniquement la table LockPermissions peuvent toujours être installés à l’aide de Windows Installer 5,0.

Windows Installer 5,0 traite les informations dans la table [MsiLockPermissionsEx](msilockpermissionsex-table.md) lorsqu’il exécute les actions standard [InstallFiles](installfiles-action.md), [InstallServices](installservices-action.md), [WriteRegistryValues](writeregistryvalues-action.md) et [CreateFolders](createfolders-action.md) . Un objet sécurisable doit être installé ou réinstallé pour être sécurisé et il n’est pas possible d’ajouter une [liste de Access Control](../secauthz/access-control-lists.md) (ACL) à un objet existant sans réinstaller cet objet.

Pour spécifier le service, le fichier, le répertoire ou la clé de Registre à sécuriser, entrez les informations d’identification dans les champs LockObject et table de la table [MsiLockPermissionsEx](msilockpermissionsex-table.md) . Un objet est identifié par sa clé primaire dans la table [ServiceInstall](serviceinstall-table.md), la table de [fichiers](file-table.md), la table de [Registre](registry-table.md)ou la [table CreateFolder](createfolder-table.md).

Pour demander que les autorisations spécifiées s’appliquent à un objet, entrez une chaîne de descripteur de sécurité valide dans le champ *SDDLText* de la table [MsiLockPermissionsEx](msilockpermissionsex-table.md) à l’aide du langage SDDL ( [Security Descriptor Definition Language](../secauthz/security-descriptor-definition-language.md) ) valide. La table **MsiLockPermissionsEx** peut spécifier un descripteur de sécurité qui refuse des autorisations, spécifie l’héritage des autorisations d’une ressource parent ou spécifie les autorisations d’un nouveau compte. Pour obtenir la liste de toutes les autorisations qui peuvent être accordées, refusées ou héritées, consultez [chaînes ACE](../secauthz/ace-strings.md). Windows Installer 5,0 étend l’ensemble des identificateurs de sécurité (SID) disponibles. Pour obtenir la liste des SID valides, consultez [sid Strings](../secauthz/sid-strings.md).

> [!NOTE]
> Si vous souhaitez configurer le descripteur de sécurité d’une ressource parente pour spécifier que ses autorisations doivent être héritées par les objets enfants, votre programme d’installation doit appliquer des autorisations à la ressource parente avant de créer les objets enfants. Si votre programme d’installation crée les objets enfants avant d’appliquer les autorisations pouvant être héritées à la ressource parente, les autorisations de la ressource parent ne seront pas propagées aux objets enfants.

À partir de Windows Installer 5,0, le type de données [FormattedSDDLText](formattedsddltext.md) étend le type de données [mis en forme](formatted.md) . Le Windows Installer valide que la chaîne FormattedSDDLText entrée dans la colonne SDDLText de la table [MsiLockPermissionsEx](msilockpermissionsex-table.md) est conforme au [format de chaîne du descripteur de sécurité](../secauthz/security-descriptor-string-format.md).

**[Windows Installer 4,5 ou version antérieure](not-supported-in-windows-installer-4-5.md):** Non pris en charge. La table [MsiLockPermissionsEx](msilockpermissionsex-table.md) et le type de données [FormattedSDDLText](formattedsddltext.md) sont disponibles à partir de Windows Installer 5,0.

 

 
