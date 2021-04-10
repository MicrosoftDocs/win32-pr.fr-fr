---
description: Ajoute un fichier MOF à la liste des fichiers compilés au cours de la récupération du référentiel.
ms.assetid: 8901c04e-f8c1-45b0-b69d-e2ebc948f088
ms.tgt_platform: multiple
title: pragma AutoRecover
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pragma
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9bb1cfca44e0bc5437d05d721ffcd57203e5aa9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952684"
---
# <a name="pragma-autorecover"></a><span data-ttu-id="7a2a7-103">pragma AutoRecover</span><span class="sxs-lookup"><span data-stu-id="7a2a7-103">pragma autorecover</span></span>

<span data-ttu-id="7a2a7-104">La commande de préprocesseur **pragma AutoRecover** ajoute un fichier MOF à la liste des fichiers compilés au cours de la récupération du référentiel.</span><span class="sxs-lookup"><span data-stu-id="7a2a7-104">The **pragma autorecover** preprocessor command adds a MOF file to the list of files compiled during repository recovery.</span></span> <span data-ttu-id="7a2a7-105">La liste des fichiers MOF de **récupération automatique** est stockée dans cette clé de Registre :</span><span class="sxs-lookup"><span data-stu-id="7a2a7-105">The list of **autorecover** MOF files is stored in this registry key:</span></span>

<span data-ttu-id="7a2a7-106">**HKEY \_ Logiciel de l' \_ ordinateur local** \\  \\ **Microsoft** \\ **WBEM** \\ **CIMOM**- \\ **récupération automatique (MOF** )</span><span class="sxs-lookup"><span data-stu-id="7a2a7-106">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM**\\**autorecover mofs**</span></span>

<span data-ttu-id="7a2a7-107">WMI vérifie l’intégrité de l’espace de stockage WMI lorsque le système d’exploitation démarre WMI.</span><span class="sxs-lookup"><span data-stu-id="7a2a7-107">WMI checks the integrity of the WMI repository when the operating system starts WMI.</span></span> <span data-ttu-id="7a2a7-108">Si le référentiel est endommagé, WMI reconstruit automatiquement le référentiel et RECOMPILE tous les fichiers MOF listés dans cette clé dans le registre.</span><span class="sxs-lookup"><span data-stu-id="7a2a7-108">If the repository is damaged, WMI automatically rebuilds the repository and recompiles any MOF files listed in this key in the registry.</span></span>

<span data-ttu-id="7a2a7-109">La syntaxe de la commande pragma autoautorecover est décrite ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="7a2a7-109">The following describes the syntax for the pragma autorecover command:</span></span>


```mof
#pragma autorecover
```



<span data-ttu-id="7a2a7-110">Toutefois, vous devez respecter les restrictions suivantes lors de l’utilisation de cette commande :</span><span class="sxs-lookup"><span data-stu-id="7a2a7-110">However, you must observe the following restrictions when using this command:</span></span>

-   <span data-ttu-id="7a2a7-111">WMI ne peut pas récupérer les fichiers MOF situés sur un ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="7a2a7-111">WMI cannot recover MOF files located on a remote computer.</span></span>

    <span data-ttu-id="7a2a7-112">Par conséquent, les fichiers MOF listés dans cette clé de Registre doivent résider sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="7a2a7-112">Therefore, the MOF files listed in this registry key must reside on the local computer.</span></span>

-   <span data-ttu-id="7a2a7-113">Vous ne pouvez pas spécifier les commutateurs de ligne de commande que le compilateur MOF utilise lorsque WMI récupère un fichier MOF.</span><span class="sxs-lookup"><span data-stu-id="7a2a7-113">You cannot specify the command-line switches that the MOF compiler uses when WMI recovers a MOF file.</span></span>

    <span data-ttu-id="7a2a7-114">Par conséquent, vous devez inclure dans votre fichier MOF des commandes [pragma](-pragma.md) qui rendent les commutateurs de ligne de commande inutiles.</span><span class="sxs-lookup"><span data-stu-id="7a2a7-114">Therefore, you should include [pragma](-pragma.md) commands in your MOF file that make command-line switches unnecessary.</span></span> <span data-ttu-id="7a2a7-115">L’exemple suivant décrit un commutateur de ligne de commande courant que WMI n’utilise pas lors de la récupération d’un fichier MOF à partir de cette clé de Registre : **mofcomp-N :root \\ test mymof. mof**</span><span class="sxs-lookup"><span data-stu-id="7a2a7-115">The following example describes a common command-line switch that WMI does not use when recovering a MOF file from this registry key: **mofcomp -N:Root\\Test mymof.mof**</span></span>

    <span data-ttu-id="7a2a7-116">Toutefois, vous pouvez spécifier l’espace de noms à l’aide d’une commande [pragma](-pragma.md) dans le fichier MOF.</span><span class="sxs-lookup"><span data-stu-id="7a2a7-116">However, you can specify the namespace using a [pragma](-pragma.md) command in the MOF file.</span></span>

    ```mof
    #pragma namespace ("\\\\.\\Root\\test")
    ```

    

## <a name="requirements"></a><span data-ttu-id="7a2a7-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7a2a7-117">Requirements</span></span>



| <span data-ttu-id="7a2a7-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7a2a7-118">Requirement</span></span> | <span data-ttu-id="7a2a7-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="7a2a7-119">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="7a2a7-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7a2a7-120">Minimum supported client</span></span><br/> | <span data-ttu-id="7a2a7-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7a2a7-121">Windows Vista</span></span><br/>       |
| <span data-ttu-id="7a2a7-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7a2a7-122">Minimum supported server</span></span><br/> | <span data-ttu-id="7a2a7-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7a2a7-123">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7a2a7-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7a2a7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a2a7-125">Commandes de préprocesseur</span><span class="sxs-lookup"><span data-stu-id="7a2a7-125">Preprocessor Commands</span></span>](preprocessor-commands.md)
</dt> </dl>

 

 




