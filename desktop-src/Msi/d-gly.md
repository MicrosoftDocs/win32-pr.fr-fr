---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ms.assetid: d6dd73e7-657f-4f71-8e9b-70369cb21972
title: D (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4e2673f845d85db88d55cbcd53838f7e682dbe3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752317"
---
# <a name="d-windows-installer"></a>D (Windows Installer)

[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) D [e](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z

<dl> <dt>

<span id="_msi_database_function_gly"></span><span id="_MSI_DATABASE_FUNCTION_GLY"></span>**fonction de base de données**
</dt> <dd>

Accède à la base de données du programme d’installation. Ces fonctions sont fournies principalement pour une utilisation par les [*outils de création de packages d’installation*](i-gly.md) et ne sont pas destinées à être utilisées pour appeler des services de programme d’installation. Pour plus d’informations, consultez [fonctions de base de données](database-functions.md) et référence des fonctions du [programme d’installation](installer-function-reference.md).

</dd> <dt>

<span id="_msi_database_handle_gly"></span><span id="_MSI_DATABASE_HANDLE_GLY"></span>**descripteur de base de données**
</dt> <dd>

Requis pour l’utilisation d’une base de données. Pour plus d’informations, consultez [obtention d’un descripteur de base de données](obtaining-a-database-handle.md).

</dd> <dt>

<span id="setup.delta_patch_gly"></span><span id="SETUP.DELTA_PATCH_GLY"></span>**correctif Delta**
</dt> <dd>

Un correctif Delta est un correctif Windows Installer compressé par Delta, créé à l’aide d’un outil, tel que Patchwiz.dll, qui prend en charge la compression Delta. Les correctifs qui utilisent la compression Delta peuvent réduire la taille d’une mise à jour en fournissant uniquement les différences (deltas) entre les fichiers existants sur un ordinateur cible et les nouveaux fichiers souhaités. Les nouveaux fichiers souhaités sont ensuite synthétisés à partir des fichiers existants et des deltas téléchargés. Pour plus d’informations sur la technologie de compression Delta, consultez l' [interface de programmation d’applications de compression Delta](https://msdn.microsoft.com/library/ms811406.aspx).

</dd> </dl>

 

 



