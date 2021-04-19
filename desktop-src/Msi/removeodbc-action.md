---
description: L’action RemoveODBC supprime les sources de données, les traducteurs et les pilotes qui sont indiqués pour la suppression au cours de l’installation.
ms.assetid: 548984fd-e4f7-4db8-a625-87b4a0a4bdb2
title: Action RemoveODBC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1234ed736a8cb8258bccf3085de92bfb1b324cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524661"
---
# <a name="removeodbc-action"></a><span data-ttu-id="334f5-103">Action RemoveODBC</span><span class="sxs-lookup"><span data-stu-id="334f5-103">RemoveODBC Action</span></span>

<span data-ttu-id="334f5-104">L’action RemoveODBC supprime les sources de données, les traducteurs et les pilotes qui sont indiqués pour la suppression au cours de l’installation.</span><span class="sxs-lookup"><span data-stu-id="334f5-104">The RemoveODBC action removes the data sources, translators, and drivers listed for removal during the installation.</span></span> <span data-ttu-id="334f5-105">Cette action interroge la table [ODBCDataSource](odbcdatasource-table.md), la table [ODBCTranslator](odbctranslator-table.md)et la [table ODBCDriver](odbcdriver-table.md) pour chaque source de données, traducteur ou pilote dont la suppression est planifiée.</span><span class="sxs-lookup"><span data-stu-id="334f5-105">This action queries the [ODBCDataSource table](odbcdatasource-table.md), [ODBCTranslator table](odbctranslator-table.md), and [ODBCDriver table](odbcdriver-table.md) for each data source, translator, or driver scheduled for removal.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="334f5-106">Restrictions de séquence</span><span class="sxs-lookup"><span data-stu-id="334f5-106">Sequence Restrictions</span></span>

<span data-ttu-id="334f5-107">Il n’existe aucune restriction de séquence.</span><span class="sxs-lookup"><span data-stu-id="334f5-107">There are no sequence restrictions.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="334f5-108">Messages ActionData</span><span class="sxs-lookup"><span data-stu-id="334f5-108">ActionData Messages</span></span>

<span data-ttu-id="334f5-109">Pour chaque pilote installé.</span><span class="sxs-lookup"><span data-stu-id="334f5-109">For each driver installed.</span></span>



| <span data-ttu-id="334f5-110">Champ</span><span class="sxs-lookup"><span data-stu-id="334f5-110">Field</span></span> | <span data-ttu-id="334f5-111">Description des données d’action</span><span class="sxs-lookup"><span data-stu-id="334f5-111">Description of action data</span></span>               |
|-------|------------------------------------------|
| <span data-ttu-id="334f5-112">\[1\]</span><span class="sxs-lookup"><span data-stu-id="334f5-112">\[1\]</span></span> | <span data-ttu-id="334f5-113">Description du pilote.</span><span class="sxs-lookup"><span data-stu-id="334f5-113">Driver description.</span></span> <span data-ttu-id="334f5-114">Clé du pilote ODBC.</span><span class="sxs-lookup"><span data-stu-id="334f5-114">The ODBC driver key.</span></span> |
| <span data-ttu-id="334f5-115">\[2\]</span><span class="sxs-lookup"><span data-stu-id="334f5-115">\[2\]</span></span> | <span data-ttu-id="334f5-116">ComponentId</span><span class="sxs-lookup"><span data-stu-id="334f5-116">ComponentId</span></span>                              |



 

<span data-ttu-id="334f5-117">Pour chaque traducteur installé.</span><span class="sxs-lookup"><span data-stu-id="334f5-117">For each translator installed.</span></span>



| <span data-ttu-id="334f5-118">Champ</span><span class="sxs-lookup"><span data-stu-id="334f5-118">Field</span></span> | <span data-ttu-id="334f5-119">Description des données d’action</span><span class="sxs-lookup"><span data-stu-id="334f5-119">Description of action data</span></span>               |
|-------|------------------------------------------|
| <span data-ttu-id="334f5-120">\[1\]</span><span class="sxs-lookup"><span data-stu-id="334f5-120">\[1\]</span></span> | <span data-ttu-id="334f5-121">Description du pilote.</span><span class="sxs-lookup"><span data-stu-id="334f5-121">Driver description.</span></span> <span data-ttu-id="334f5-122">Clé du pilote ODBC.</span><span class="sxs-lookup"><span data-stu-id="334f5-122">The ODBC driver key.</span></span> |
| <span data-ttu-id="334f5-123">\[2\]</span><span class="sxs-lookup"><span data-stu-id="334f5-123">\[2\]</span></span> | <span data-ttu-id="334f5-124">ComponentId</span><span class="sxs-lookup"><span data-stu-id="334f5-124">ComponentId</span></span>                              |



 

<span data-ttu-id="334f5-125">Pour chaque source de données installée.</span><span class="sxs-lookup"><span data-stu-id="334f5-125">For each data source installed.</span></span>



| <span data-ttu-id="334f5-126">Champ</span><span class="sxs-lookup"><span data-stu-id="334f5-126">Field</span></span> | <span data-ttu-id="334f5-127">Description des données d’action</span><span class="sxs-lookup"><span data-stu-id="334f5-127">Description of action data</span></span>                              |
|-------|---------------------------------------------------------|
| <span data-ttu-id="334f5-128">\[1\]</span><span class="sxs-lookup"><span data-stu-id="334f5-128">\[1\]</span></span> | <span data-ttu-id="334f5-129">Description du pilote.</span><span class="sxs-lookup"><span data-stu-id="334f5-129">Driver description.</span></span> <span data-ttu-id="334f5-130">Clé du pilote ODBC.</span><span class="sxs-lookup"><span data-stu-id="334f5-130">The ODBC driver key.</span></span>                |
| <span data-ttu-id="334f5-131">\[2\]</span><span class="sxs-lookup"><span data-stu-id="334f5-131">\[2\]</span></span> | <span data-ttu-id="334f5-132">ComponentId</span><span class="sxs-lookup"><span data-stu-id="334f5-132">ComponentId</span></span>                                             |
| <span data-ttu-id="334f5-133">\[3\]</span><span class="sxs-lookup"><span data-stu-id="334f5-133">\[3\]</span></span> | <span data-ttu-id="334f5-134">Inscription : SQL \_ Remove \_ DSN ou SQL \_ Remove \_ sys \_ DSN</span><span class="sxs-lookup"><span data-stu-id="334f5-134">Registration: SQL\_REMOVE\_DSN or SQL\_REMOVE\_SYS\_DSN</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="334f5-135">Notes</span><span class="sxs-lookup"><span data-stu-id="334f5-135">Remarks</span></span>

<span data-ttu-id="334f5-136">Si le nombre d’utilisations ODBC et le nombre d’utilisations de fichiers deviennent nuls, le fichier est supprimé.</span><span class="sxs-lookup"><span data-stu-id="334f5-136">If both the ODBC usage count and the file usage count become zero, the file is removed.</span></span> <span data-ttu-id="334f5-137">L’inscription dépend du nombre d’utilisations ODBC et la suppression des fichiers est basée sur les nombres de références de clé dll partagés.</span><span class="sxs-lookup"><span data-stu-id="334f5-137">Registration is dependent on ODBC usage counts and file removal is based on shared DLLs key reference counts.</span></span>

 

 



