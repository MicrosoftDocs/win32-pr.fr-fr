---
description: En savoir plus sur les concepts de Windows Installer qui commencent par la lettre C, tels que fichier CAB et somme de contrôle.
ms.assetid: f98d19c5-5187-4718-b241-3ec69454c2d6
title: C (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47e7af99ad32d8dff7f4e8509976b0004045477b
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010922"
---
# <a name="c-windows-installer"></a>C (Windows Installer)

[A](a-gly.md) [B](b-gly.md) C [D](d-gly.md) [e](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z

<dl> <dt>

<span id="_msi_cabinet_file_using_windows_installer_gly"></span><span id="_MSI_CABINET_FILE_USING_WINDOWS_INSTALLER_GLY"></span>**fichier CAB**
</dt> <dd>

Fichier unique, généralement avec une extension de .cab, qui stocke les fichiers compressés dans une bibliothèque de fichiers. Le format cab est un moyen efficace d’empaqueter plusieurs fichiers, car la compression est effectuée à travers les limites de fichiers, ce qui améliore considérablement le taux de compression. Pour plus d’informations sur la création d’armoires, consultez [fichiers CAB](cabinet-files.md).

</dd> <dt>

<span id="_msi_checksum_gly"></span><span id="_MSI_CHECKSUM_GLY"></span>**EEPROM**
</dt> <dd>

Valeur calculée qui dépend du contenu d’un fichier. Il est stocké avec les données pour détecter les fichiers endommagés. Le système vérifie cette valeur pour s’assurer que les données ne sont pas endommagées.

</dd> <dt>

<span id="_msi_component_using_windows_installer_gly"></span><span id="_MSI_COMPONENT_USING_WINDOWS_INSTALLER_GLY"></span>**-**
</dt> <dd>

Plus petite partie d’une installation gérée par le programme d’installation, également un bloc de construction d’une application ou d’une fonctionnalité du point de vue du programmeur. Les exemples de composants sont un groupe de fichiers associés, un objet COM ou une bibliothèque. Pour plus d’informations, consultez [composants et fonctionnalités](components-and-features.md).

</dd> <dt>

<span id="_msi_committing_databases_using_windows_installer_gly"></span><span id="_MSI_COMMITTING_DATABASES_USING_WINDOWS_INSTALLER_GLY"></span>**validation des bases de données**
</dt> <dd>

Modifications accumulées effectuées dans une base de données. Les modifications ne sont pas reflétées dans la base de données réelle tant que la base de données n’est pas validée. Pour plus d’informations, consultez [validation des bases de données](committing-databases.md).

</dd> <dt>

<span id="_msi_controlevent_gly"></span><span id="_MSI_CONTROLEVENT_GLY"></span>**ControlEvent,**
</dt> <dd>

Aspect des fonctionnalités de l’interface utilisateur du programme d’installation. Un ControlEvent, classique déclenche une action par le programme d’installation lors de l’activation d’un contrôle de boîte de dialogue ou d’un autre événement. Pour plus d’informations, consultez [vue d’ensemble de ControlEvent,](controlevent-overview.md).

</dd> <dt>

<span id="_msi_costing_gly"></span><span id="_MSI_COSTING_GLY"></span>**coûts**
</dt> <dd>

Méthode utilisée par le programme d’installation pour déterminer l’espace disque requis pour l’installation. Le coût prend en compte des facteurs tels que la nécessité ou non de remplacer les fichiers existants. Pour plus d’informations, consultez [coûts des fichiers](file-costing.md).

</dd> <dt>

<span id="_msi_.cub_file_gly"></span><span id="_MSI_.CUB_FILE_GLY"></span>**fichier. CUB**
</dt> <dd>

Module de validation qui stocke et fournit l’accès aux actions personnalisées ICE. Pour plus d’informations, consultez [exemple de fichier. CUB](sample--cub-file.md). Pour plus d’informations, consultez également [Windows Installer extensions de fichier](windows-installer-file-extensions.md).

</dd> <dt>

<span id="_msi_custom_action_using_windows_installer_gly"></span><span id="_MSI_CUSTOM_ACTION_USING_WINDOWS_INSTALLER_GLY"></span>**action personnalisée**
</dt> <dd>

Écrit par l’auteur du [*package*](p-gly.md) , mais n’est pas intégré au programme d’installation comme action standard. Pour plus d’informations, consultez [actions personnalisées](custom-actions.md).

</dd> </dl>

 

 



