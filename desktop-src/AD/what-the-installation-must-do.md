---
title: Ce que l’installation doit faire
description: Les nouveaux attributs référencés à l’étape 3 doivent être référencés par son OID, car le nouveau nom d’attribut n’est pas présent dans le cache de schéma à ce stade.
ms.assetid: 57da8740-7646-4ca9-ba8d-832e4f520b13
ms.tgt_platform: multiple
keywords:
- Ce que l’installation doit faire d’AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5724a7acbb4d0bf8ef3008fa48e2f10fcc04a324
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939619"
---
# <a name="what-the-installation-must-do"></a><span data-ttu-id="e9655-104">Ce que l’installation doit faire</span><span class="sxs-lookup"><span data-stu-id="e9655-104">What the Installation Must Do</span></span>

<span data-ttu-id="e9655-105">Les applications qui étendent le schéma doivent appliquer les mises à jour comme décrit dans la procédure suivante.</span><span class="sxs-lookup"><span data-stu-id="e9655-105">Applications that extend the schema, must apply updates as described in the following procedure.</span></span>

<span data-ttu-id="e9655-106">**Pour appliquer des mises à jour lors de l’extension du schéma**</span><span class="sxs-lookup"><span data-stu-id="e9655-106">**To apply updates when extending the schema**</span></span>

1.  <span data-ttu-id="e9655-107">Ajoutez les nouveaux attributs.</span><span class="sxs-lookup"><span data-stu-id="e9655-107">Add the new attributes.</span></span>
2.  <span data-ttu-id="e9655-108">Ajoutez les nouvelles classes.</span><span class="sxs-lookup"><span data-stu-id="e9655-108">Add the new classes.</span></span>
3.  <span data-ttu-id="e9655-109">Ajoutez les nouveaux attributs aux classes.</span><span class="sxs-lookup"><span data-stu-id="e9655-109">Add the new attributes to classes.</span></span>
4.  <span data-ttu-id="e9655-110">Déclenchez un rechargement du cache.</span><span class="sxs-lookup"><span data-stu-id="e9655-110">Trigger a cache reload.</span></span>

<span data-ttu-id="e9655-111">Les nouveaux attributs référencés à l’étape 3 doivent être référencés par son OID, car le nouveau nom d’attribut n’est pas présent dans le cache de schéma à ce stade.</span><span class="sxs-lookup"><span data-stu-id="e9655-111">New attributes referenced in Step 3 must be referred to by its OID because the new attribute name is not present in the schema cache at this point.</span></span>

<span data-ttu-id="e9655-112">L’étape 4 n’est pas nécessaire si les extensions ne seront pas utilisées immédiatement ; les extensions s’affichent dans le cache de schéma en 5 minutes environ, en fonction de la charge du système.</span><span class="sxs-lookup"><span data-stu-id="e9655-112">Step 4 is unnecessary if the extensions will not be used immediately; the extensions will appear in the schema cache in approximately 5 minutes, depending on system load.</span></span> <span data-ttu-id="e9655-113">Pour plus d’informations sur le cache de schéma et sur la façon de déclencher un rechargement de cache, consultez [mise à jour du cache de schéma](updating-the-schema-cache.md).</span><span class="sxs-lookup"><span data-stu-id="e9655-113">For more information about the schema cache and how to trigger a cache reload, see [Updating the Schema Cache](updating-the-schema-cache.md).</span></span>

 

 




