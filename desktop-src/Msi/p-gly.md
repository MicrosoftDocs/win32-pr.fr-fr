---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ms.assetid: 868f5ed3-b179-404b-9462-1d3a179103f8
title: P (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a4e6b8f1343fdd68f4a6ce042852cff1e28e05c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115359"
---
# <a name="p-windows-installer"></a>P (Windows Installer)

[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [e](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) P [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z

<dl> <dt>

<span id="_msi_package_using_windows_installer_gly"></span><span id="_MSI_PACKAGE_USING_WINDOWS_INSTALLER_GLY"></span>**Packages**
</dt> <dd>

[*fichier. msi*](m-gly.md) et tout fichier [*source externe*](e-gly.md) pouvant être désigné par ce fichier. Un package contient donc toutes les informations dont le Windows Installer a besoin pour exécuter l’interface utilisateur et installer ou désinstaller l’application. Pour plus d’informations, consultez également [*installer la base de données*](i-gly.md).

</dd> <dt>

<span id="_msi_package_code_gly"></span><span id="_MSI_PACKAGE_CODE_GLY"></span>**Code du package**
</dt> <dd>

GUID qui identifie un package particulier. Un code de package unique est nécessaire, car certains transformations ou packages de correctifs peuvent être appliqués à plusieurs applications ou peuvent mettre à niveau une application vers une autre application ou version. Pour plus d’informations, consultez [codes de package](package-codes.md).

</dd> <dt>

<span id="_msi_patching_gly"></span><span id="_MSI_PATCHING_GLY"></span>**correctifs**
</dt> <dd>

Méthode de mise à jour d’un fichier qui remplace uniquement les bits en cours de modification, plutôt que le fichier entier. Cela signifie que les utilisateurs peuvent télécharger un correctif de mise à niveau pour un produit qui est plus petit que l’intégralité du produit. Pour plus d’informations, consultez [packages de correctifs](patch-packages.md).

</dd> <dt>

<span id="_msi_patch_file_gly"></span><span id="_MSI_PATCH_FILE_GLY"></span>**fichier correctif**
</dt> <dd>

[Package P atch](patch-packages.md) utilisé pour la mise à jour corrective. Pour plus d’informations, consultez [mise à jour corrective et mises à niveau](patching-and-upgrades.md).

</dd> <dt>

<span id="_msi_preview_mode_using_windows_installer_gly"></span><span id="_MSI_PREVIEW_MODE_USING_WINDOWS_INSTALLER_GLY"></span>**mode aperçu**
</dt> <dd>

Mode d’affichage de la conception de l’interface utilisateur. Pour plus d’informations, consultez [aperçu de l’interface utilisateur](previewing-the-user-interface.md).

</dd> <dt>

<span id="_msi_progress_bar_gly"></span><span id="_MSI_PROGRESS_BAR_GLY"></span>**barre de progression**
</dt> <dd>

Contrôle que le programme d’installation peut afficher pendant l’exécution du script représentant la progression de l’installation. Pour plus d’informations, consultez [création d’un contrôle ProgressBar](authoring-a-progressbar-control.md).

</dd> <dt>

<span id="_msi_property_gly"></span><span id="_MSI_PROPERTY_GLY"></span>**propriété**
</dt> <dd>

Variables globales utilisées durant une installation. (Consultez [à propos des propriétés](about-properties.md).)

Le terme « propriété » fait également référence à un attribut d’un objet Automation. (Voir [interface Automation](automation-interface.md).)

</dd> <dt>

<span id="_msi_publishing_gly"></span><span id="_MSI_PUBLISHING_GLY"></span>**publiée**
</dt> <dd>

Méthode de [*publication*](a-gly.md) d’une fonctionnalité ou d’une application. La publication ne remplit pas l’interface utilisateur. Toutefois, si une autre application tente d’ouvrir une application publiée, il y a suffisamment d’informations pour que le programme d’installation affecte l’application publiée. Pour plus d’informations, consultez [*Assigning*](a-gly.md) and [Components and features](components-and-features.md).

</dd> </dl>

 

 



