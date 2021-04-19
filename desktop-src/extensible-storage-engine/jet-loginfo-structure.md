---
description: 'En savoir plus sur : structure JET_LOGINFO'
title: Structure JET_LOGINFO
TOCTitle: JET_LOGINFO Structure
ms:assetid: b34b3f24-5d19-4e11-a657-a0e59204d628
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294063(v=EXCHG.10)
ms:contentKeyID: 32765678
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b7e643d775d1fb8e0c19286bfb7a50d887644e99
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "106527968"
---
# <a name="jet_loginfo-structure"></a><span data-ttu-id="c7013-103">Structure JET_LOGINFO</span><span class="sxs-lookup"><span data-stu-id="c7013-103">JET_LOGINFO Structure</span></span>


<span data-ttu-id="c7013-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="c7013-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_loginfo-structure"></a><span data-ttu-id="c7013-105">Structure JET_LOGINFO</span><span class="sxs-lookup"><span data-stu-id="c7013-105">JET_LOGINFO Structure</span></span>

<span data-ttu-id="c7013-106">La structure **JET_LOGINFO** retourne des informations structurées sur l’ensemble des fichiers du journal des transactions qui doit faire partie d’un jeu de fichiers de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="c7013-106">The **JET_LOGINFO** structure returns structured information about the set of transaction log files that should be a part of a backup file set.</span></span> <span data-ttu-id="c7013-107">La structure **JET_LOGINFO** est l’ensemble minimal d’informations nécessaires pour représenter une plage de journaux récupérés avec [JetGetLogInfoInstance2](./jetgetloginfoinstance2-function.md) ou spécifiés pour une récupération matérielle avec [JetExternalRestore2](./jetexternalrestore2-function.md).</span><span class="sxs-lookup"><span data-stu-id="c7013-107">The **JET_LOGINFO** structure is the minimal set of information needed to represent a range of logs that is retrieved with [JetGetLogInfoInstance2](./jetgetloginfoinstance2-function.md) or specified for a hard recovery with [JetExternalRestore2](./jetexternalrestore2-function.md).</span></span>

```cpp
typedef struct {
  unsigned long cbSize;
  unsigned long ulGenLow;
  unsigned long ulGenHigh;
  tchar szBaseName[JET_BASE_NAME_LENGTH + 1];
} JET_LOGINFO;
```

### <a name="members"></a><span data-ttu-id="c7013-108">Membres</span><span class="sxs-lookup"><span data-stu-id="c7013-108">Members</span></span>

<span data-ttu-id="c7013-109">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="c7013-109">**cbSize**</span></span>

<span data-ttu-id="c7013-110">Taille de la structure en octets.</span><span class="sxs-lookup"><span data-stu-id="c7013-110">The size of the structure, in bytes.</span></span>

<span data-ttu-id="c7013-111">Ce membre permet l’expansion future de cette structure tout en activant la compatibilité descendante.</span><span class="sxs-lookup"><span data-stu-id="c7013-111">This member enables future expansion of this structure while enabling backwards compatibility.</span></span> <span data-ttu-id="c7013-112">Il doit toujours être défini sur sizeof (JET_LOGINFO).</span><span class="sxs-lookup"><span data-stu-id="c7013-112">It should always be set to sizeof( JET_LOGINFO ).</span></span>

<span data-ttu-id="c7013-113">**ulGenLow**</span><span class="sxs-lookup"><span data-stu-id="c7013-113">**ulGenLow**</span></span>

<span data-ttu-id="c7013-114">Numéro de fichier journal le plus bas (ou le plus ancien) qui est restauré.</span><span class="sxs-lookup"><span data-stu-id="c7013-114">The lowest (or oldest) log file number that is restored.</span></span> <span data-ttu-id="c7013-115">La fidélité complète d’un long non signé doit être conservée, mais dans les versions actuelles du moteur, ce nombre est un nombre hexadécimal compris entre 0x00000 et 0xFFFFF.</span><span class="sxs-lookup"><span data-stu-id="c7013-115">The full fidelity of an unsigned long should be preserved, but in current versions of the engine this number is a hexadecimal number in the range from 0x00000 to 0xFFFFF.</span></span> <span data-ttu-id="c7013-116">Cela peut changer dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="c7013-116">This might change in future versions.</span></span>

<span data-ttu-id="c7013-117">**ulGenHigh**</span><span class="sxs-lookup"><span data-stu-id="c7013-117">**ulGenHigh**</span></span>

<span data-ttu-id="c7013-118">Numéro de fichier journal le plus élevé (ou le plus récent) qui est restauré.</span><span class="sxs-lookup"><span data-stu-id="c7013-118">The highest (or most recent) log file number that is restored.</span></span> <span data-ttu-id="c7013-119">La fidélité complète d’un long non signé doit être conservée, mais dans les versions actuelles du moteur, ce nombre est un nombre hexadécimal compris entre 0x00000 et 0xFFFFF.</span><span class="sxs-lookup"><span data-stu-id="c7013-119">The full fidelity of a unsigned long should be preserved, but in current versions of the engine this number is a hexadecimal number in the range from 0x00000 to 0xFFFFF.</span></span> <span data-ttu-id="c7013-120">Cela peut changer dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="c7013-120">This might change in future versions.</span></span>

<span data-ttu-id="c7013-121">**szBaseName**</span><span class="sxs-lookup"><span data-stu-id="c7013-121">**szBaseName**</span></span>

<span data-ttu-id="c7013-122">Préfixe utilisé pour nommer les fichiers du journal des transactions.</span><span class="sxs-lookup"><span data-stu-id="c7013-122">The prefix used to name the transaction log files.</span></span>

<span data-ttu-id="c7013-123">La valeur retournée dans ce membre est toujours égale au paramètre de [JET_paramBaseName](./transaction-log-parameters.md) pour l’instance qui a généré ces informations.</span><span class="sxs-lookup"><span data-stu-id="c7013-123">The value that is returned in this member is always equal to the setting for [JET_paramBaseName](./transaction-log-parameters.md) for the instance that generated this information.</span></span>

### <a name="remarks"></a><span data-ttu-id="c7013-124">Notes</span><span class="sxs-lookup"><span data-stu-id="c7013-124">Remarks</span></span>

<span data-ttu-id="c7013-125">Les fichiers journaux de transactions sont nommés en fonction du nom de base de l’instance et du numéro de génération du fichier journal.</span><span class="sxs-lookup"><span data-stu-id="c7013-125">Transaction log files are named according to the instance base name and the generation number of the log file.</span></span> <span data-ttu-id="c7013-126">Le nom est au format BBBXXXXX. Sign.</span><span class="sxs-lookup"><span data-stu-id="c7013-126">The name is of the format BBBXXXXX.LOG.</span></span> <span data-ttu-id="c7013-127">BBB correspond au nom de base du fichier journal et sa longueur est toujours de trois caractères.</span><span class="sxs-lookup"><span data-stu-id="c7013-127">BBB corresponds to the base name for the log file and is always three characters in length.</span></span> <span data-ttu-id="c7013-128">XXXXX correspond au numéro de génération du fichier journal en valeur hexadécimale de zéro et est toujours de cinq caractères.</span><span class="sxs-lookup"><span data-stu-id="c7013-128">XXXXX corresponds to the generation number of the log file in zero padded hexadecimal and is always five characters in length.</span></span> <span data-ttu-id="c7013-129">LOG est l’extension de fichier qui est toujours donnée aux fichiers journaux des transactions par le moteur.</span><span class="sxs-lookup"><span data-stu-id="c7013-129">LOG is the file extension that is always given to transaction log files by the engine.</span></span>

<span data-ttu-id="c7013-130">L’utilisation de ces informations structurées est déconseillée, car elle permet à l’application d’avoir une connaissance approfondie de ce schéma de nommage pour les fichiers journaux des transactions.</span><span class="sxs-lookup"><span data-stu-id="c7013-130">Use of this structured information is discouraged because it causes the application to have intimate knowledge of this naming scheme for transaction log files.</span></span> <span data-ttu-id="c7013-131">Si le schéma de nommage change à l’avenir, une telle application ne fonctionnera plus correctement.</span><span class="sxs-lookup"><span data-stu-id="c7013-131">If the naming scheme ever changes in the future then such an application will no longer function properly.</span></span> <span data-ttu-id="c7013-132">Il est concevable que le format de journal change pour incorporer 8 chiffres hexadécimaux à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="c7013-132">It is conceivable that the log format will change to incorporate 8 hex digits in the future.</span></span> <span data-ttu-id="c7013-133">Les applications doivent utiliser la liste explicite des noms de fichiers retournés par [JetGetLogInfo](./jetgetloginfo-function.md) à la place.</span><span class="sxs-lookup"><span data-stu-id="c7013-133">Applications should use the explicit list of file names returned by [JetGetLogInfo](./jetgetloginfo-function.md) instead.</span></span>

### <a name="requirements"></a><span data-ttu-id="c7013-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c7013-134">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c7013-135"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="c7013-135"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="c7013-136">Nécessite Windows Vista ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c7013-136">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7013-137"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="c7013-137"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="c7013-138">Requiert Windows Server 2008 ou Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="c7013-138">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c7013-139"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="c7013-139"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="c7013-140">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="c7013-140">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7013-141"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="c7013-141"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="c7013-142">Implémenté comme <strong>JET_LOGINFO_W</strong> (Unicode) et <strong>JET_LOGINFO_A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="c7013-142">Implemented as <strong>JET_LOGINFO_W</strong> (Unicode) and <strong>JET_LOGINFO_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="c7013-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c7013-143">See Also</span></span>

[<span data-ttu-id="c7013-144">JetExternalRestore2</span><span class="sxs-lookup"><span data-stu-id="c7013-144">JetExternalRestore2</span></span>](./jetexternalrestore2-function.md)  
[<span data-ttu-id="c7013-145">JetGetLogInfo</span><span class="sxs-lookup"><span data-stu-id="c7013-145">JetGetLogInfo</span></span>](./jetgetloginfo-function.md)  
[<span data-ttu-id="c7013-146">JetGetLogInfoInstance2</span><span class="sxs-lookup"><span data-stu-id="c7013-146">JetGetLogInfoInstance2</span></span>](./jetgetloginfoinstance2-function.md)  
[<span data-ttu-id="c7013-147">Paramètres système</span><span class="sxs-lookup"><span data-stu-id="c7013-147">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
