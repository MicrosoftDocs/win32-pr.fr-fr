---
title: /commutateur metadata_dir (MIDLRT)
description: Le \_ commutateur/Metadata dir spécifie un ou plusieurs répertoires qui contiennent des fichiers de métadonnées de plateforme.
ms.assetid: 578b9d3f-3ee6-4978-9d2a-0c5aee561a30
keywords:
- /commutateur metadata_dir MIDL
topic_type:
- apiref
api_name:
- /metadata_dir
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72781641323aa61ae75da256f84f8c1debfd6556
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528974"
---
# <a name="metadata_dir-switch-midlrt"></a><span data-ttu-id="a1d47-104">/commutateur metadata_dir (MIDLRT)</span><span class="sxs-lookup"><span data-stu-id="a1d47-104">/metadata_dir switch (MIDLRT)</span></span>

<span data-ttu-id="a1d47-105">Le commutateur **/Metadata \_ dir** spécifie un ou plusieurs répertoires qui contiennent des fichiers de métadonnées de plateforme.</span><span class="sxs-lookup"><span data-stu-id="a1d47-105">The **/metadata\_dir** switch specifies one or more directories that contain platform metadata files.</span></span>

``` syntax
midlrt /metadata_dir metadata_directory
```

## <a name="switch-options"></a><span data-ttu-id="a1d47-106">Options de commutateur</span><span class="sxs-lookup"><span data-stu-id="a1d47-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="a1d47-107">*Répertoire de métadonnées \_*</span><span class="sxs-lookup"><span data-stu-id="a1d47-107">*metadata\_directory*</span></span> 
</dt> <dd>

<span data-ttu-id="a1d47-108">Spécifie un ou plusieurs répertoires qui contiennent des fichiers de métadonnées de plateforme.</span><span class="sxs-lookup"><span data-stu-id="a1d47-108">Specifies one or more directories that contain platform metadata files.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a1d47-109">Notes</span><span class="sxs-lookup"><span data-stu-id="a1d47-109">Remarks</span></span>

<span data-ttu-id="a1d47-110">Utilisez ce commutateur pour spécifier l’emplacement du fichier de métadonnées principal pour Windows, nommé Windows. winmd.</span><span class="sxs-lookup"><span data-stu-id="a1d47-110">Use this switch to specify the location of the main metadata file for Windows, which is named windows.winmd.</span></span>

## <a name="examples"></a><span data-ttu-id="a1d47-111">Exemples</span><span class="sxs-lookup"><span data-stu-id="a1d47-111">Examples</span></span>

<span data-ttu-id="a1d47-112">**midlrt/Metadata \_ dir dir1 dir2**</span><span class="sxs-lookup"><span data-stu-id="a1d47-112">**midlrt /metadata\_dir dir1 dir2**</span></span>

## <a name="requirements"></a><span data-ttu-id="a1d47-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a1d47-113">Requirements</span></span>



| <span data-ttu-id="a1d47-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a1d47-114">Requirement</span></span> | <span data-ttu-id="a1d47-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="a1d47-115">Value</span></span> |
|-------------------|--------------------------------|
| <span data-ttu-id="a1d47-116">Client</span><span class="sxs-lookup"><span data-stu-id="a1d47-116">Client</span></span><br/> | <span data-ttu-id="a1d47-117">Windows 8</span><span class="sxs-lookup"><span data-stu-id="a1d47-117">Windows 8</span></span><br/>           |
| <span data-ttu-id="a1d47-118">Serveur</span><span class="sxs-lookup"><span data-stu-id="a1d47-118">Server</span></span><br/> | <span data-ttu-id="a1d47-119">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a1d47-119">Windows Server 2012</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a1d47-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a1d47-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1d47-121">Syntaxe générale de la ligne de commande MIDL</span><span class="sxs-lookup"><span data-stu-id="a1d47-121">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> </dl>

 

 





