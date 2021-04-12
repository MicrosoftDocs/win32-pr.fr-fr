---
description: 'En savoir plus sur : paramètres système du moteur de stockage extensible'
title: Paramètres système du moteur de stockage extensible
TOCTitle: Extensible Storage Engine System Parameters
ms:assetid: f95c2e87-b25e-4be5-8c17-8486ba37dad4
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294139(v=EXCHG.10)
ms:contentKeyID: 32765753
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 43473f1bf5f599ba8efd06bd31345485acc07061
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527988"
---
# <a name="extensible-storage-engine-system-parameters"></a><span data-ttu-id="7938d-103">Paramètres système du moteur de stockage extensible</span><span class="sxs-lookup"><span data-stu-id="7938d-103">Extensible Storage Engine System Parameters</span></span>


<span data-ttu-id="7938d-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="7938d-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="extensible-storage-engine-system-parameters"></a><span data-ttu-id="7938d-105">Paramètres système du moteur de stockage extensible</span><span class="sxs-lookup"><span data-stu-id="7938d-105">Extensible Storage Engine System Parameters</span></span>

<span data-ttu-id="7938d-106">Les constantes suivantes sont utilisées comme valeurs pour le paramètre *paramid* des fonctions [JetGetSystemParameter](./jetgetsystemparameter-function.md) et [JetSetSystemParameter](./jetsetsystemparameter-function.md) .</span><span class="sxs-lookup"><span data-stu-id="7938d-106">The following constants are used as values for the *paramid* parameter of the [JetGetSystemParameter](./jetgetsystemparameter-function.md) and [JetSetSystemParameter](./jetsetsystemparameter-function.md) functions.</span></span>

  - [<span data-ttu-id="7938d-107">Paramètres de sauvegarde et de restauration</span><span class="sxs-lookup"><span data-stu-id="7938d-107">Backup and Restore Parameters</span></span>](./backup-and-restore-parameters.md)

  - [<span data-ttu-id="7938d-108">Paramètres de rappel</span><span class="sxs-lookup"><span data-stu-id="7938d-108">Callback Parameters</span></span>](./callback-parameters.md)

  - [<span data-ttu-id="7938d-109">Paramètres de base de données</span><span class="sxs-lookup"><span data-stu-id="7938d-109">Database Parameters</span></span>](./database-parameters.md)

  - [<span data-ttu-id="7938d-110">Paramètres du cache de base de données</span><span class="sxs-lookup"><span data-stu-id="7938d-110">Database Cache Parameters</span></span>](./database-cache-parameters.md)

  - [<span data-ttu-id="7938d-111">Paramètres de gestion des erreurs</span><span class="sxs-lookup"><span data-stu-id="7938d-111">Error Handling Parameters</span></span>](./error-handling-parameters.md)

  - [<span data-ttu-id="7938d-112">Paramètres du journal des événements</span><span class="sxs-lookup"><span data-stu-id="7938d-112">Event Log Parameters</span></span>](./event-log-parameters.md)

  - [<span data-ttu-id="7938d-113">Paramètres d’e/s</span><span class="sxs-lookup"><span data-stu-id="7938d-113">I/O Parameters</span></span>](./i-o-parameters.md)

  - [<span data-ttu-id="7938d-114">Paramètres d’index</span><span class="sxs-lookup"><span data-stu-id="7938d-114">Index Parameters</span></span>](./index-parameters.md)

  - [<span data-ttu-id="7938d-115">Paramètres d’information</span><span class="sxs-lookup"><span data-stu-id="7938d-115">Informational Parameters</span></span>](./informational-parameters.md)

  - [<span data-ttu-id="7938d-116">Paramètres méta</span><span class="sxs-lookup"><span data-stu-id="7938d-116">Meta Parameters</span></span>](./meta-parameters.md)

  - [<span data-ttu-id="7938d-117">Paramètres de ressource</span><span class="sxs-lookup"><span data-stu-id="7938d-117">Resource Parameters</span></span>](./resource-parameters.md)

  - [<span data-ttu-id="7938d-118">Paramètres de base de données temporaires</span><span class="sxs-lookup"><span data-stu-id="7938d-118">Temporary Database Parameters</span></span>](./temporary-database-parameters.md)

  - [<span data-ttu-id="7938d-119">Paramètres du journal des transactions</span><span class="sxs-lookup"><span data-stu-id="7938d-119">Transaction Log Parameters</span></span>](./transaction-log-parameters.md)

### <a name="system-parameter-description-format"></a><span data-ttu-id="7938d-120">Format de description de paramètre système</span><span class="sxs-lookup"><span data-stu-id="7938d-120">System Parameter Description Format</span></span>

<span data-ttu-id="7938d-121">Chaque paramètre système est décrit en utilisant le format suivant :</span><span class="sxs-lookup"><span data-stu-id="7938d-121">Each system parameter will be described using the following format:</span></span>

<span data-ttu-id="7938d-122">JET_paramX</span><span class="sxs-lookup"><span data-stu-id="7938d-122">JET_paramX</span></span>

<span data-ttu-id="7938d-123">Description du paramètre système JET_paramX.</span><span class="sxs-lookup"><span data-stu-id="7938d-123">Description of the JET_paramX system parameter.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7938d-124">Valeur par défaut :</span><span class="sxs-lookup"><span data-stu-id="7938d-124">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="7938d-125">Valeur par défaut du paramètre.</span><span class="sxs-lookup"><span data-stu-id="7938d-125">The default value of the parameter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7938d-126">Tapez :</span><span class="sxs-lookup"><span data-stu-id="7938d-126">Type:</span></span></p></td>
<td><p><span data-ttu-id="7938d-127">Type de données du paramètre.</span><span class="sxs-lookup"><span data-stu-id="7938d-127">The data type of the parameter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7938d-128">Plage valide :</span><span class="sxs-lookup"><span data-stu-id="7938d-128">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="7938d-129">Valeurs autorisées pour le paramètre.</span><span class="sxs-lookup"><span data-stu-id="7938d-129">The legal values for the parameter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7938d-130">Étendue :</span><span class="sxs-lookup"><span data-stu-id="7938d-130">Scope:</span></span></p></td>
<td><p><span data-ttu-id="7938d-131">Le paramètre est-il global ou par instance ?</span><span class="sxs-lookup"><span data-stu-id="7938d-131">Is the parameter Global or per Instance?</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7938d-132">Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="7938d-132">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="7938d-133">Le paramètre peut-il être défini si des instances existent ?</span><span class="sxs-lookup"><span data-stu-id="7938d-133">Can the parameter be set if any instances exist?</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7938d-134">Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="7938d-134">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="7938d-135">Le paramètre peut-il être défini lors de son initialisation ?</span><span class="sxs-lookup"><span data-stu-id="7938d-135">Can the parameter be set when initialized?</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7938d-136">Affecte la disposition physique :</span><span class="sxs-lookup"><span data-stu-id="7938d-136">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="7938d-137">Le paramètre affecte-t-il les fichiers sur le disque ?</span><span class="sxs-lookup"><span data-stu-id="7938d-137">Does the parameter affect the files on disk?</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7938d-138">Affecte la fiabilité :</span><span class="sxs-lookup"><span data-stu-id="7938d-138">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="7938d-139">Le paramètre affecte-t-il la fiabilité du moteur ?</span><span class="sxs-lookup"><span data-stu-id="7938d-139">Does the parameter affect engine reliability?</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7938d-140">Affecte les performances :</span><span class="sxs-lookup"><span data-stu-id="7938d-140">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="7938d-141">Le paramètre affecte-t-il les performances du moteur ?</span><span class="sxs-lookup"><span data-stu-id="7938d-141">Does the parameter affect engine performance?</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7938d-142">Affecte les ressources :</span><span class="sxs-lookup"><span data-stu-id="7938d-142">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="7938d-143">Le paramètre affecte-t-il les ressources du moteur ?</span><span class="sxs-lookup"><span data-stu-id="7938d-143">Does the parameter affect engine resources?</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7938d-144">Disponibilité :</span><span class="sxs-lookup"><span data-stu-id="7938d-144">Availability:</span></span></p></td>
<td><p><span data-ttu-id="7938d-145">Les versions de Windows qui prennent en charge le paramètre.</span><span class="sxs-lookup"><span data-stu-id="7938d-145">Releases of Windows that support the parameter.</span></span></p></td>
</tr>
</tbody>
</table>
