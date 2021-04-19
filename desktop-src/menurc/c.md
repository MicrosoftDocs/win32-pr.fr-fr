---
title: C (menus et autres ressources)
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 2323bc5f-ace6-475f-8059-95392f8b61a4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20c8851e0ac59308b5c20c47e8d45cd4539ec19d
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "106509494"
---
# <a name="c-menus-and-other-resources"></a><span data-ttu-id="ea681-103">C (menus et autres ressources)</span><span class="sxs-lookup"><span data-stu-id="ea681-103">C (Menus and Other Resources)</span></span>

<span data-ttu-id="ea681-104">[A](a.md) [B](b.md) C D [e](e.md) [F](f.md) G H [I](i.md) J K L M [N](n.md) [O](o.md) P Q [R](r.md) S [T](t.md) [U](u.md) [V](v.md) [W](w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="ea681-104">[A](a.md) [B](b.md) C D [E](e.md) [F](f.md) G H [I](i.md) J K L M [N](n.md) [O](o.md) P Q [R](r.md) S [T](t.md) [U](u.md) [V](v.md) [W](w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="ea681-105"><span id="tools.c_1_gly"></span><span id="TOOLS.C_1_GLY"></span>**Impossible de réutiliser les constantes de chaîne**</span><span class="sxs-lookup"><span data-stu-id="ea681-105"><span id="tools.c_1_gly"></span><span id="TOOLS.C_1_GLY"></span>**Cannot Re-use String Constants**</span></span>
</dt> <dd>

<span data-ttu-id="ea681-106">Vous utilisez la même valeur deux fois dans une instruction [**STRINGTABLE**](stringtable-resource.md) .</span><span class="sxs-lookup"><span data-stu-id="ea681-106">You are using the same value twice in a [**STRINGTABLE**](stringtable-resource.md) statement.</span></span> <span data-ttu-id="ea681-107">Assurez-vous que vous n’avez pas mélangé des valeurs décimales et hexadécimales qui se chevauchent.</span><span class="sxs-lookup"><span data-stu-id="ea681-107">Make sure that you have not mixed overlapping decimal and hexadecimal values.</span></span>

</dd> <dt>

<span data-ttu-id="ea681-108"><span id="tools.c_2_gly"></span><span id="TOOLS.C_2_GLY"></span>**Caractère de contrôle hors de \[ la plage A ? Lettre\]**</span><span class="sxs-lookup"><span data-stu-id="ea681-108"><span id="tools.c_2_gly"></span><span id="TOOLS.C_2_GLY"></span>**Control Character out of range \[A?Z\]**</span></span>
</dt> <dd>

<span data-ttu-id="ea681-109">Un caractère de contrôle dans l’instruction [**Accelerators**](accelerators-resource.md) n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="ea681-109">A control character in the [**ACCELERATORS**](accelerators-resource.md) statement is invalid.</span></span> <span data-ttu-id="ea681-110">Le caractère qui suit le signe insertion (^) doit être compris entre A et Z.</span><span class="sxs-lookup"><span data-stu-id="ea681-110">The character following the caret (^) must be in the range A through Z.</span></span>

</dd> <dt>

<span data-ttu-id="ea681-111"><span id="tools.c_3_gly"></span><span id="TOOLS.C_3_GLY"></span>**Impossible d’ouvrir-fichier-nom**</span><span class="sxs-lookup"><span data-stu-id="ea681-111"><span id="tools.c_3_gly"></span><span id="TOOLS.C_3_GLY"></span>**Could not openin-file-name**</span></span>
</dt> <dd>

<span data-ttu-id="ea681-112">Le compilateur de ressources Microsoft Windows (RC) n’a pas pu ouvrir le fichier spécifié.</span><span class="sxs-lookup"><span data-stu-id="ea681-112">Microsoft Windows Resource Compiler (RC) could not open the specified file.</span></span> <span data-ttu-id="ea681-113">Assurez-vous que le fichier existe et que vous avez correctement tapé le nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="ea681-113">Make sure that the file exists and that you typed the filename correctly.</span></span>

</dd> <dt>

<span data-ttu-id="ea681-114"><span id="tools.c_4_gly"></span><span id="TOOLS.C_4_GLY"></span>**Openresource-nom introuvable**</span><span class="sxs-lookup"><span data-stu-id="ea681-114"><span id="tools.c_4_gly"></span><span id="TOOLS.C_4_GLY"></span>**Couldn't openresource-name**</span></span>
</dt> <dd>

<span data-ttu-id="ea681-115">Le compilateur de ressources Microsoft Windows (RC) n’a pas pu ouvrir le fichier spécifié.</span><span class="sxs-lookup"><span data-stu-id="ea681-115">Microsoft Windows Resource Compiler (RC) could not open the specified file.</span></span> <span data-ttu-id="ea681-116">Assurez-vous que le fichier existe et que vous avez correctement tapé le nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="ea681-116">Make sure that the file exists and that you typed the filename correctly.</span></span>

</dd> <dt>

<span data-ttu-id="ea681-117"><span id="tools.c_5_gly"></span><span id="TOOLS.C_5_GLY"></span>**Creatingresource-nom**</span><span class="sxs-lookup"><span data-stu-id="ea681-117"><span id="tools.c_5_gly"></span><span id="TOOLS.C_5_GLY"></span>**Creatingresource-name**</span></span>
</dt> <dd>

<span data-ttu-id="ea681-118">(V) le compilateur de ressources Microsoft Windows (RC) crée un fichier de ressources binaires (. res).</span><span class="sxs-lookup"><span data-stu-id="ea681-118">(V) Microsoft Windows Resource Compiler (RC) is creating a new binary resource (.res) file.</span></span>

</dd> </dl>

 

 




