---
description: Si le compilateur MOF ne peut pas terminer la compilation d’un fichier MOF, l’espace de stockage WMI peut être laissé dans un État indéfini.
ms.assetid: 13adc666-6588-4cfd-a5eb-17da93434468
ms.tgt_platform: multiple
title: Gestion des erreurs avec le compilateur MOF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 905b406020787de894a2821b501ee465ab63ea5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485817"
---
# <a name="handling-errors-with-the-mof-compiler"></a><span data-ttu-id="b5166-103">Gestion des erreurs avec le compilateur MOF</span><span class="sxs-lookup"><span data-stu-id="b5166-103">Handling Errors with the MOF Compiler</span></span>

<span data-ttu-id="b5166-104">Si le compilateur MOF ne peut pas terminer la compilation d’un fichier MOF, l’espace de stockage WMI peut être laissé dans un État indéfini.</span><span class="sxs-lookup"><span data-stu-id="b5166-104">If the MOF compiler cannot finish compiling a MOF file, the WMI repository may be left in an undefined state.</span></span> <span data-ttu-id="b5166-105">Par exemple, si vous compilez un fichier MOF et que vous utilisez le commutateur de ligne de commande **-Class : CreateOnly** , la compilation se termine si une classe spécifiée dans le fichier MOF existe déjà.</span><span class="sxs-lookup"><span data-stu-id="b5166-105">For example, if you are compiling a MOF file and you use the **-class:createonly** command-line switch, the compilation terminates if a class specified in the MOF file already exists.</span></span> <span data-ttu-id="b5166-106">Le compilateur MOF stocke dans le référentiel toutes les classes ou instances qui ont été définies jusqu’au point où le compilateur s’arrête.</span><span class="sxs-lookup"><span data-stu-id="b5166-106">The MOF compiler stores in the repository any classes or instances that were defined up to the point where the compiler stops.</span></span> <span data-ttu-id="b5166-107">Dans certains cas, cela peut rendre le référentiel WMI dans une condition non définie.</span><span class="sxs-lookup"><span data-stu-id="b5166-107">In some cases, this can leave the WMI repository in an undefined condition.</span></span>

<span data-ttu-id="b5166-108">Dans ce cas, vous devrez peut-être arrêter WMI, supprimer le référentiel WMI et le faire régénérer par WMI.</span><span class="sxs-lookup"><span data-stu-id="b5166-108">In this situation, you may need to stop WMI, delete the WMI repository, and have WMI rebuild it.</span></span> <span data-ttu-id="b5166-109">Tous les fichiers MOF contenant la [commande de préprocesseur](preprocessor-commands.md) [**pragma AutoRecover**](pragma-autorecover.md) sont reconstruits lors du redémarrage de WMI.</span><span class="sxs-lookup"><span data-stu-id="b5166-109">All MOF files that contain the [**pragma autorecover**](pragma-autorecover.md) [preprocessor command](preprocessor-commands.md) are rebuilt when WMI is restarted.</span></span> <span data-ttu-id="b5166-110">Vous devez recompiler manuellement tous les fichiers MOF qui n’incluent pas d' `#pragma autorecover` instruction.</span><span class="sxs-lookup"><span data-stu-id="b5166-110">You must manually recompile any MOF files that do not include a `#pragma autorecover` statement.</span></span>

<span data-ttu-id="b5166-111">Pour plus d’informations sur la façon de déclarer des classes et des instances à l’aide de la syntaxe MOF, consultez [conception de classes format MOF (MOF)](designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="b5166-111">For more information about how to declare classes and instances using the MOF syntax, see [Designing Managed Object Format (MOF) Classes](designing-managed-object-format--mof--classes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b5166-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b5166-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b5166-113">Compilation des fichiers MOF</span><span class="sxs-lookup"><span data-stu-id="b5166-113">Compiling MOF Files</span></span>](compiling-mof-files.md)
</dt> <dt>

[<span data-ttu-id="b5166-114">**mofcomp**</span><span class="sxs-lookup"><span data-stu-id="b5166-114">**mofcomp**</span></span>](mofcomp.md)
</dt> <dt>

[<span data-ttu-id="b5166-115">Commandes de préprocesseur</span><span class="sxs-lookup"><span data-stu-id="b5166-115">Preprocessor Commands</span></span>](preprocessor-commands.md)
</dt> </dl>

 

 



