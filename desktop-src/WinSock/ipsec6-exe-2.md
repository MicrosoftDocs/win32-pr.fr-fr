---
description: La configuration des stratégies IPSec et des associations de sécurité pour IPv6 s’effectue avec Ipsec6.exe.
ms.assetid: 9a0c8e48-bc57-461d-9ade-54b75f7aa56d
title: Ipsec6.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b373e8ab0dc54c3c8ee2fae8bc05722a9ac6aa64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515238"
---
# <a name="ipsec6exe"></a><span data-ttu-id="4fc12-103">Ipsec6.exe</span><span class="sxs-lookup"><span data-stu-id="4fc12-103">Ipsec6.exe</span></span>

<span data-ttu-id="4fc12-104">La configuration des stratégies IPSec et des associations de sécurité pour IPv6 s’effectue avec Ipsec6.exe.</span><span class="sxs-lookup"><span data-stu-id="4fc12-104">Configuration of IPSec policies and security associations for IPv6 is done with Ipsec6.exe.</span></span> <span data-ttu-id="4fc12-105">Les Ipsec6.exe sous-commandes sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="4fc12-105">The following are Ipsec6.exe subcommands:</span></span>

<dl> <dt>

<span data-ttu-id="4fc12-106"><span id="ipsec6_sp__Interface_"></span><span id="ipsec6_sp__interface_"></span><span id="IPSEC6_SP__INTERFACE_"></span>**Ipsec6 SP \[** _Interface_*_\]_*</span><span class="sxs-lookup"><span data-stu-id="4fc12-106"><span id="ipsec6_sp__Interface_"></span><span id="ipsec6_sp__interface_"></span><span id="IPSEC6_SP__INTERFACE_"></span>**ipsec6 sp \[**_Interface_*_\]_*</span></span>
</dt> <dd>

<span data-ttu-id="4fc12-107">Affiche les stratégies de sécurité actives.</span><span class="sxs-lookup"><span data-stu-id="4fc12-107">Displays active security policies.</span></span> <span data-ttu-id="4fc12-108">Vous pouvez également afficher des stratégies de sécurité actives pour une interface spécifique.</span><span class="sxs-lookup"><span data-stu-id="4fc12-108">Alternately, displays active security policies for a specific interface.</span></span>

</dd> <dt>

<span data-ttu-id="4fc12-109"><span id="ipsec6_sa"></span><span id="IPSEC6_SA"></span>**Ipsec6 sa**</span><span class="sxs-lookup"><span data-stu-id="4fc12-109"><span id="ipsec6_sa"></span><span id="IPSEC6_SA"></span>**ipsec6 sa**</span></span>
</dt> <dd>

<span data-ttu-id="4fc12-110">Affiche les associations de sécurité actives.</span><span class="sxs-lookup"><span data-stu-id="4fc12-110">Displays active security associations.</span></span>

</dd> <dt>

<span data-ttu-id="4fc12-111"><span id="ipsec6_c__FileName_without_extension__"></span><span id="ipsec6_c__filename_without_extension__"></span><span id="IPSEC6_C__FILENAME_WITHOUT_EXTENSION__"></span>**Ipsec6 c \[** _Nom de fichier (sans extension)_*_\]_*</span><span class="sxs-lookup"><span data-stu-id="4fc12-111"><span id="ipsec6_c__FileName_without_extension__"></span><span id="ipsec6_c__filename_without_extension__"></span><span id="IPSEC6_C__FILENAME_WITHOUT_EXTENSION__"></span>**ipsec6 c \[**_FileName(without extension)_*_\]_*</span></span>
</dt> <dd>

<span data-ttu-id="4fc12-112">Crée les fichiers utilisés pour configurer les associations de sécurité et de stratégie de sécurité.</span><span class="sxs-lookup"><span data-stu-id="4fc12-112">Creates files used to configure security policy and security associations.</span></span> <span data-ttu-id="4fc12-113">Crée *filename*. SPD pour les stratégies de sécurité et *nom de fichier*. sad pour les associations de sécurité.</span><span class="sxs-lookup"><span data-stu-id="4fc12-113">Creates *FileName*.spd for security policies and *FileName*.sad for security associations.</span></span> <span data-ttu-id="4fc12-114">Utilisez les fichiers créés en tant que modèles pour configurer des stratégies de sécurité ou des associations de sécurité.</span><span class="sxs-lookup"><span data-stu-id="4fc12-114">Use the created files as templates to configure security policies or security associations.</span></span> <span data-ttu-id="4fc12-115">Les fichiers peuvent être modifiés à l’aide d’un éditeur de texte.</span><span class="sxs-lookup"><span data-stu-id="4fc12-115">The files can be modified with a text editor.</span></span> <span data-ttu-id="4fc12-116">Pour appeler la configuration contenue dans les fichiers SPD et SAD, utilisez la commande **Ipsec6 a** .</span><span class="sxs-lookup"><span data-stu-id="4fc12-116">To invoke the configuration contained in the SPD and SAD files, use the **ipsec6 a** command.</span></span>

</dd> <dt>

<span data-ttu-id="4fc12-117"><span id="ipsec6_a__FileName_without_extension__"></span><span id="ipsec6_a__filename_without_extension__"></span><span id="IPSEC6_A__FILENAME_WITHOUT_EXTENSION__"></span>**Ipsec6 a \[** _Nom de fichier (sans extension)_*_\]_*</span><span class="sxs-lookup"><span data-stu-id="4fc12-117"><span id="ipsec6_a__FileName_without_extension__"></span><span id="ipsec6_a__filename_without_extension__"></span><span id="IPSEC6_A__FILENAME_WITHOUT_EXTENSION__"></span>**ipsec6 a \[**_FileName(without extension)_*_\]_*</span></span>
</dt> <dd>

<span data-ttu-id="4fc12-118">Ajoute des stratégies de sécurité dans *filename*. SPD et des associations de sécurité dans *filename*. Sad à la liste des stratégies de sécurité et des associations de sécurité actives.</span><span class="sxs-lookup"><span data-stu-id="4fc12-118">Adds security policies in *FileName*.spd and security associations in *FileName*.sad to the list of active security policies and security associations.</span></span>

</dd> <dt>

<span data-ttu-id="4fc12-119"><span id="ipsec6_i__Policy___FileName_without_extension__"></span><span id="ipsec6_i__policy___filename_without_extension__"></span><span id="IPSEC6_I__POLICY___FILENAME_WITHOUT_EXTENSION__"></span>**Ipsec6 i \[**  *_\] \[_* _Nom de fichier de stratégie (sans extension)_*_\]_*</span><span class="sxs-lookup"><span data-stu-id="4fc12-119"><span id="ipsec6_i__Policy___FileName_without_extension__"></span><span id="ipsec6_i__policy___filename_without_extension__"></span><span id="IPSEC6_I__POLICY___FILENAME_WITHOUT_EXTENSION__"></span>**ipsec6 i \[**_Policy_*_\] \[_*_FileName(without extension)_*_\]_*</span></span>
</dt> <dd>

<span data-ttu-id="4fc12-120">Ajoute des stratégies de sécurité dans *filename*. SPD et des associations de sécurité dans *filename*. Sad à la liste des stratégies de sécurité actives et des associations de sécurité, telles qu’elles sont référencées par le numéro de stratégie.</span><span class="sxs-lookup"><span data-stu-id="4fc12-120">Adds security policies in *FileName*.spd and security associations in *FileName*.sad to the list of active security policies and security associations as referenced by policy number.</span></span>

</dd> <dt>

<span data-ttu-id="4fc12-121"><span id="ipsec6_d__type___sp_sa___IndexNumber_"></span><span id="ipsec6_d__type___sp_sa___indexnumber_"></span><span id="IPSEC6_D__TYPE___SP_SA___INDEXNUMBER_"></span>**Ipsec6 d \[ type = SP sa \] \[** _IndexNumber_*_\]_*</span><span class="sxs-lookup"><span data-stu-id="4fc12-121"><span id="ipsec6_d__type___sp_sa___IndexNumber_"></span><span id="ipsec6_d__type___sp_sa___indexnumber_"></span><span id="IPSEC6_D__TYPE___SP_SA___INDEXNUMBER_"></span>**ipsec6 d \[type = sp sa\] \[**_IndexNumber_*_\]_*</span></span>
</dt> <dd>

<span data-ttu-id="4fc12-122">Supprime les stratégies de sécurité ou les associations de sécurité de la liste des stratégies de sécurité actives et des associations de sécurité, telles qu’elles sont référencées par leur numéro d’index (affiché avec **Ipsec6 SP** ou **Ipsec6 sa**).</span><span class="sxs-lookup"><span data-stu-id="4fc12-122">Deletes security policies or security associations from the list of active security policies and security associations, as referenced by their index number (displayed with **ipsec6 sp** or **ipsec6 sa**).</span></span>

</dd> </dl>

 

 



