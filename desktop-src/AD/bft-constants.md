---
title: Constantes BFT (ntdsbcli. h)
description: Les constantes BFT sont utilisées comme indicateurs binaires pour identifier les différents types de fichiers dans une sauvegarde Active Directory Domain Services.
ms.assetid: 3658a657-d9e3-4fbf-9120-4b0205b81a36
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- BFT_LOG_DIRECTORY
- BFT_DATABASE_DIRECTORY
- BFT_DIRECTORY
- BFT_LOG
- BFT_LOG_DIR
- BFT_CHECKPOINT_DIR
- BFT_NTDS_DATABASE
- BFT_PATCH_FILE
- BFT_UNKNOWN
api_location:
- Ntdsbcli.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9607b5e61e5689d8895b39a11aa7e813fc7fcbe6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941972"
---
# <a name="bft-constants"></a><span data-ttu-id="dde17-103">Constantes BFT</span><span class="sxs-lookup"><span data-stu-id="dde17-103">BFT Constants</span></span>

<span data-ttu-id="dde17-104">Les constantes BFT sont utilisées comme indicateurs binaires pour identifier les différents types de fichiers dans une sauvegarde Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="dde17-104">The BFT constants are used as bit flags to identify different file types in an Active Directory Domain Services backup.</span></span>

<dl> <dt>

<span data-ttu-id="dde17-105"><span id="BFT_LOG_DIRECTORY"></span><span id="bft_log_directory"></span>**\_répertoire du journal BFT \_**</span><span class="sxs-lookup"><span data-stu-id="dde17-105"><span id="BFT_LOG_DIRECTORY"></span><span id="bft_log_directory"></span>**BFT\_LOG\_DIRECTORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dde17-106">0x20</span><span class="sxs-lookup"><span data-stu-id="dde17-106">0x20</span></span>
</dt> <dt>



<span data-ttu-id="dde17-107">Le fichier appartient au répertoire des journaux.</span><span class="sxs-lookup"><span data-stu-id="dde17-107">The file belongs in the log directory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dde17-108"><span id="BFT_DATABASE_DIRECTORY"></span><span id="bft_database_directory"></span>**\_Répertoire de base de données BFT \_**</span><span class="sxs-lookup"><span data-stu-id="dde17-108"><span id="BFT_DATABASE_DIRECTORY"></span><span id="bft_database_directory"></span>**BFT\_DATABASE\_DIRECTORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dde17-109">0x40</span><span class="sxs-lookup"><span data-stu-id="dde17-109">0x40</span></span>
</dt> <dt>



<span data-ttu-id="dde17-110">Le fichier appartient au répertoire de la base de données.</span><span class="sxs-lookup"><span data-stu-id="dde17-110">The file belongs in the database directory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dde17-111"><span id="BFT_DIRECTORY"></span><span id="bft_directory"></span>**\_répertoire BFT**</span><span class="sxs-lookup"><span data-stu-id="dde17-111"><span id="BFT_DIRECTORY"></span><span id="bft_directory"></span>**BFT\_DIRECTORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dde17-112">0x80</span><span class="sxs-lookup"><span data-stu-id="dde17-112">0x80</span></span>
</dt> <dt>



<span data-ttu-id="dde17-113">Le chemin d’accès spécifié est un répertoire et non un nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="dde17-113">The path specified is a directory and not a file name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dde17-114"><span id="BFT_LOG"></span><span id="bft_log"></span>**\_Journal BFT**</span><span class="sxs-lookup"><span data-stu-id="dde17-114"><span id="BFT_LOG"></span><span id="bft_log"></span>**BFT\_LOG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dde17-115">0x21</span><span class="sxs-lookup"><span data-stu-id="dde17-115">0x21</span></span>
</dt> <dt>



<span data-ttu-id="dde17-116">Spécifie un fichier journal qui appartient au répertoire des journaux.</span><span class="sxs-lookup"><span data-stu-id="dde17-116">Specifies a log file that belongs in the log directory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dde17-117"><span id="BFT_LOG_DIR"></span><span id="bft_log_dir"></span>**\_répertoire du journal BFT \_**</span><span class="sxs-lookup"><span data-stu-id="dde17-117"><span id="BFT_LOG_DIR"></span><span id="bft_log_dir"></span>**BFT\_LOG\_DIR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dde17-118">0x22</span><span class="sxs-lookup"><span data-stu-id="dde17-118">0x22</span></span>
</dt> <dt>



<span data-ttu-id="dde17-119">Le fichier est le chemin d’accès du répertoire des journaux.</span><span class="sxs-lookup"><span data-stu-id="dde17-119">The file is the path of the log directory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dde17-120"><span id="BFT_CHECKPOINT_DIR"></span><span id="bft_checkpoint_dir"></span>**BFT \_ Répertoire de point de contrôle \_**</span><span class="sxs-lookup"><span data-stu-id="dde17-120"><span id="BFT_CHECKPOINT_DIR"></span><span id="bft_checkpoint_dir"></span>**BFT\_CHECKPOINT\_DIR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dde17-121">0x23</span><span class="sxs-lookup"><span data-stu-id="dde17-121">0x23</span></span>
</dt> <dt>



<span data-ttu-id="dde17-122">Le fichier est le chemin d’accès du répertoire de point de contrôle.</span><span class="sxs-lookup"><span data-stu-id="dde17-122">The file is the path of the checkpoint directory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dde17-123"><span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>**\_ \_ base de données BFT NTDS**</span><span class="sxs-lookup"><span data-stu-id="dde17-123"><span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>**BFT\_NTDS\_DATABASE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dde17-124">0x44</span><span class="sxs-lookup"><span data-stu-id="dde17-124">0x44</span></span>
</dt> <dt>



<span data-ttu-id="dde17-125">Le fichier est une base de données de service d’annuaire qui appartient au répertoire de base de données.</span><span class="sxs-lookup"><span data-stu-id="dde17-125">The file is a directory service database that belongs in the database directory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dde17-126"><span id="BFT_PATCH_FILE"></span><span id="bft_patch_file"></span>**\_fichier correctif \_ BFT**</span><span class="sxs-lookup"><span data-stu-id="dde17-126"><span id="BFT_PATCH_FILE"></span><span id="bft_patch_file"></span>**BFT\_PATCH\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dde17-127">0x25</span><span class="sxs-lookup"><span data-stu-id="dde17-127">0x25</span></span>
</dt> <dt>



<span data-ttu-id="dde17-128">Le fichier est un fichier correctif qui appartient au répertoire des journaux.</span><span class="sxs-lookup"><span data-stu-id="dde17-128">The file is a patch file that belongs in the log directory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dde17-129"><span id="BFT_UNKNOWN"></span><span id="bft_unknown"></span>**BFT \_ inconnu**</span><span class="sxs-lookup"><span data-stu-id="dde17-129"><span id="BFT_UNKNOWN"></span><span id="bft_unknown"></span>**BFT\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dde17-130">0x0F</span><span class="sxs-lookup"><span data-stu-id="dde17-130">0x0F</span></span>
</dt> <dt>



<span data-ttu-id="dde17-131">Le fichier ne peut pas être reconnu.</span><span class="sxs-lookup"><span data-stu-id="dde17-131">The file cannot be recognized.</span></span> <span data-ttu-id="dde17-132">Le fichier ne coïncide pas avec les noms de fichiers et les types de fichiers connus.</span><span class="sxs-lookup"><span data-stu-id="dde17-132">The file does not coincide with the known file names and file types.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dde17-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dde17-133">Requirements</span></span>



| <span data-ttu-id="dde17-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dde17-134">Requirement</span></span> | <span data-ttu-id="dde17-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="dde17-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dde17-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dde17-136">Minimum supported client</span></span><br/> | <span data-ttu-id="dde17-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dde17-137">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="dde17-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dde17-138">Minimum supported server</span></span><br/> | <span data-ttu-id="dde17-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dde17-139">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="dde17-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="dde17-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="dde17-141"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="dde17-141"><dt>Ntdsbcli.h</dt></span></span> </dl> |



 

 





