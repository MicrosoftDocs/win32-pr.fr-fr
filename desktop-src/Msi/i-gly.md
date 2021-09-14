---
description: en savoir plus sur les concepts de Windows Installer qui commencent par la lettre I, tels que importer une table d’adresses et un niveau d’installation.
ms.assetid: b8e0a14f-ebdc-4b8f-a884-f6276dccda49
title: I (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e33b5cfb9c4545a5482b214e0413ab3e3d981109
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021654"
---
# <a name="i-windows-installer"></a>I (Windows Installer)

[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [e](e-gly.md) [F](f-gly.md) [G](g-gly.md) H I J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z

<dl> <dt>

<span id="_msi_.idt_file_gly"></span><span id="_MSI_.IDT_FILE_GLY"></span>**fichier. IDT**
</dt> <dd>

Table de base de données du programme d’installation exporté. pour plus d’informations, consultez [importation et exportation](importing-and-exporting.md) et [Windows Installer des Extensions de fichier](windows-installer-file-extensions.md).

</dd> <dt>

<span id="_msi_import_address_table_gly"></span><span id="_MSI_IMPORT_ADDRESS_TABLE_GLY"></span>**Table des adresses d’importation (IAT)**
</dt> <dd>

Où l’adresse virtuelle calculée est enregistrée à partir de chaque fonction importée à partir de toutes les dll.

</dd> <dt>

<span id="_msi_internal_user_interface_gly"></span><span id="_MSI_INTERNAL_USER_INTERFACE_GLY"></span>**interface utilisateur interne**
</dt> <dd>

Fonctionnalités intégrées du programme d’installation qui peuvent être utilisées pour créer une interface utilisateur graphique pour l’installation. Un auteur peut choisir une [*interface utilisateur externe*](e-gly.md). Pour plus d’informations, consultez [à propos de l’interface utilisateur](about-the-user-interface.md).

</dd> <dt>

<span id="_msi_install_level_gly"></span><span id="_MSI_INSTALL_LEVEL_GLY"></span>**niveau d’installation**
</dt> <dd>

Valeur d’installation spécifiée. Une application est installée uniquement si son propre niveau est inférieur ou égal au niveau d’installation. L’ensemble des applications choisies pour l’installation peut donc être modifié en modifiant le niveau d’installation. Pour plus d’informations, consultez [table des fonctionnalités](feature-table.md).

</dd> <dt>

<span id="_msi_install_on_demand_gly"></span><span id="_MSI_INSTALL_ON_DEMAND_GLY"></span>**installation à la demande**
</dt> <dd>

Service qui installe les applications ou les fonctionnalités demandées par l’utilisateur ou une autre application. La [*publicité*](a-gly.md) rend une fonctionnalité ou une application disponible pour une installation à la demande. Pour plus d’informations, consultez : [installation à la demande](installation-on-demand.md).

</dd> <dt>

<span id="_msi_installation_context_gly"></span><span id="_MSI_INSTALLATION_CONTEXT_GLY"></span>**contexte d’installation**
</dt> <dd>

La combinaison des droits d’installation et des types d’installation produit trois contextes d’installation différents : gérés par utilisateur, géré par utilisateur et par ordinateur. Ce n’est pas le cas par ordinateur non géré.

</dd> <dt>

<span id="_msi_installer_gly"></span><span id="_MSI_INSTALLER_GLY"></span>**d'**
</dt> <dd>

[*Windows Installer*](m-gly.md).

</dd> <dt>

<span id="_msi_installer_database_gly"></span><span id="_MSI_INSTALLER_DATABASE_GLY"></span>**base de données du programme d’installation**
</dt> <dd>

Base de données relationnelle contenant les instructions d’installation pour une installation. La base de données du programme d’installation est stockée dans le [*fichier.msi*](m-gly.md). Pour plus d’informations, consultez [base de données du programme d’installation](installer-database.md).

</dd> <dt>

<span id="_msi_installer_function_gly"></span><span id="_MSI_INSTALLER_FUNCTION_GLY"></span>**fonction installer**
</dt> <dd>

Appelée par un utilisateur ou une application pour obtenir les services et les fonctionnalités du programme d’installation. Il s’agit de l’interface de programmation d’applications du programme d’installation. Pour plus d’informations, consultez [référence des fonctions du programme d’installation](installer-function-reference.md).

</dd> <dt>

<span id="_msi_installer_package_authoring_tool_gly"></span><span id="_MSI_INSTALLER_PACKAGE_AUTHORING_TOOL_GLY"></span>**outil de création de packages d’installation**
</dt> <dd>

Logiciel qui permet à un développeur de créer et de modifier un [*fichier de.msi*](m-gly.md). Ainsi, tout [*fichier source externe*](e-gly.md) comprend un [*package*](p-gly.md) contenant toutes les informations requises pour une installation.

</dd> <dt>

<span id="_msi_internal_source_files_gly"></span><span id="_MSI_INTERNAL_SOURCE_FILES_GLY"></span>**fichiers sources internes**
</dt> <dd>

Stocké dans le [*fichier.msi*](m-gly.md). Plusieurs fichiers sources internes peuvent être compressés et stockés ensemble dans un [*fichier CAB*](c-gly.md) stocké dans un fichier de .msi.

</dd> </dl>

 

 



