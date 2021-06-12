---
description: En savoir plus sur les concepts de Windows Installer qui commencent par la lettre D, tels que la fonction de base de données et le correctif Delta.
ms.assetid: d6dd73e7-657f-4f71-8e9b-70369cb21972
title: D (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d76378d636c8ae14acdc9cb882c31840e3f1550f
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010932"
---
# <a name="d-windows-installer"></a><span data-ttu-id="fbafa-103">D (Windows Installer)</span><span class="sxs-lookup"><span data-stu-id="fbafa-103">D (Windows Installer)</span></span>

<span data-ttu-id="fbafa-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) D [e](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span><span class="sxs-lookup"><span data-stu-id="fbafa-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) D [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="fbafa-105"><span id="_msi_database_function_gly"></span><span id="_MSI_DATABASE_FUNCTION_GLY"></span>**fonction de base de données**</span><span class="sxs-lookup"><span data-stu-id="fbafa-105"><span id="_msi_database_function_gly"></span><span id="_MSI_DATABASE_FUNCTION_GLY"></span>**database function**</span></span>
</dt> <dd>

<span data-ttu-id="fbafa-106">Accède à la base de données du programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="fbafa-106">Accesses the installer database.</span></span> <span data-ttu-id="fbafa-107">Ces fonctions sont fournies principalement pour une utilisation par les [*outils de création de packages d’installation*](i-gly.md) et ne sont pas destinées à être utilisées pour appeler des services de programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="fbafa-107">These functions are provided primarily for use by [*installer package authoring tools*](i-gly.md) and they are not intended to be used to call installer services.</span></span> <span data-ttu-id="fbafa-108">Pour plus d’informations, consultez [fonctions de base de données](database-functions.md) et référence des fonctions du [programme d’installation](installer-function-reference.md).</span><span class="sxs-lookup"><span data-stu-id="fbafa-108">For more information, see [Database Functions](database-functions.md) and the [Installer Function Reference](installer-function-reference.md).</span></span>

</dd> <dt>

<span data-ttu-id="fbafa-109"><span id="_msi_database_handle_gly"></span><span id="_MSI_DATABASE_HANDLE_GLY"></span>**descripteur de base de données**</span><span class="sxs-lookup"><span data-stu-id="fbafa-109"><span id="_msi_database_handle_gly"></span><span id="_MSI_DATABASE_HANDLE_GLY"></span>**database handle**</span></span>
</dt> <dd>

<span data-ttu-id="fbafa-110">Requis pour l’utilisation d’une base de données.</span><span class="sxs-lookup"><span data-stu-id="fbafa-110">Required for working with a database.</span></span> <span data-ttu-id="fbafa-111">Pour plus d’informations, consultez [obtention d’un descripteur de base de données](obtaining-a-database-handle.md).</span><span class="sxs-lookup"><span data-stu-id="fbafa-111">For more information, see [Obtaining a Database Handle](obtaining-a-database-handle.md).</span></span>

</dd> <dt>

<span data-ttu-id="fbafa-112"><span id="setup.delta_patch_gly"></span><span id="SETUP.DELTA_PATCH_GLY"></span>**correctif Delta**</span><span class="sxs-lookup"><span data-stu-id="fbafa-112"><span id="setup.delta_patch_gly"></span><span id="SETUP.DELTA_PATCH_GLY"></span>**delta patch**</span></span>
</dt> <dd>

<span data-ttu-id="fbafa-113">Un correctif Delta est un correctif Windows Installer compressé par Delta, créé à l’aide d’un outil, tel que Patchwiz.dll, qui prend en charge la compression Delta.</span><span class="sxs-lookup"><span data-stu-id="fbafa-113">A delta patch is a delta-compressed Windows Installer patch created using a tool, such as Patchwiz.dll, that supports delta compression.</span></span> <span data-ttu-id="fbafa-114">Les correctifs qui utilisent la compression Delta peuvent réduire la taille d’une mise à jour en fournissant uniquement les différences (deltas) entre les fichiers existants sur un ordinateur cible et les nouveaux fichiers souhaités.</span><span class="sxs-lookup"><span data-stu-id="fbafa-114">Patches that use delta compression can reduce the size of an update by providing only the differences (deltas) between existing files on a target computer and the desired new files.</span></span> <span data-ttu-id="fbafa-115">Les nouveaux fichiers souhaités sont ensuite synthétisés à partir des fichiers existants et des deltas téléchargés.</span><span class="sxs-lookup"><span data-stu-id="fbafa-115">The desired new files are then synthesized from the existing files and the downloaded deltas.</span></span> <span data-ttu-id="fbafa-116">Pour plus d’informations sur la technologie de compression Delta, consultez l' [interface de programmation d’applications de compression Delta](https://msdn.microsoft.com/library/ms811406.aspx).</span><span class="sxs-lookup"><span data-stu-id="fbafa-116">For more information about delta compression technology, see the [Delta Compression Application Programming Interface](https://msdn.microsoft.com/library/ms811406.aspx).</span></span>

</dd> </dl>

 

 



