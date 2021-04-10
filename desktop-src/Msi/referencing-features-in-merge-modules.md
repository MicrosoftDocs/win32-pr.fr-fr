---
description: Les modules de fusion fonctionnent uniquement avec les composants et non avec les fonctionnalités. Toutefois, certaines tables dans les modules de fusion, telles que la table PublishComponent, contiennent des champs qui font référence à des fonctionnalités.
ms.assetid: f2891457-efef-4319-bd09-5de7fcf32d21
title: Référencement des fonctionnalités dans les modules de fusion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01640902912aae7d2ca3c6519c92bbdb563a9473
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951906"
---
# <a name="referencing-features-in-merge-modules"></a><span data-ttu-id="0d34f-104">Référencement des fonctionnalités dans les modules de fusion</span><span class="sxs-lookup"><span data-stu-id="0d34f-104">Referencing Features in Merge Modules</span></span>

<span data-ttu-id="0d34f-105">Les modules de fusion fonctionnent uniquement avec les composants et non avec les fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="0d34f-105">Merge modules only operate with components and not with features.</span></span> <span data-ttu-id="0d34f-106">Toutefois, certaines tables dans les modules de fusion, telles que la [table PublishComponent](publishcomponent-table.md), contiennent des champs qui font référence à des fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="0d34f-106">However, some tables in merge modules, such as the [PublishComponent table](publishcomponent-table.md), contain fields that refer to features.</span></span>

<span data-ttu-id="0d34f-107">Un GUID NULL : {00000000-0000-0000-0000-000000000000} doit être créé dans n’importe quel champ d’une base de données de module de fusion qui fait référence à une fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="0d34f-107">A null GUID: {00000000-0000-0000-0000-000000000000} must be authored into any field of a merge module database that references a feature.</span></span> <span data-ttu-id="0d34f-108">Lorsque le module de fusion est fusionné dans un package d’installation, l’outil de fusion remplace le GUID NULL par la fonctionnalité spécifiée dans le package d’installation, à l’exception des tables qui nécessitent un traitement spécial, par exemple la [table ModuleSignature](modulesignature-table.md) et les tables ModuleSequence.</span><span class="sxs-lookup"><span data-stu-id="0d34f-108">When the merge module is merged into an installation package, the merge tool replaces the null GUID with the feature specified in the installation package, except for tables that require special handling, such as the [ModuleSignature table](modulesignature-table.md) and the ModuleSequence tables.</span></span>

<span data-ttu-id="0d34f-109">Notez que si un GUID null est utilisé comme clé primaire, il n’est pas garanti que la valeur substituée par l’outil de fusion est unique.</span><span class="sxs-lookup"><span data-stu-id="0d34f-109">Note that if a null GUID is used as a primary key, it is not guaranteed that the value substituted by the merge tool is unique.</span></span> <span data-ttu-id="0d34f-110">Les auteurs de modules de fusion sont chargés de s’assurer qu’aucune clé primaire existante dans l’interface de l’utilisateur n’est dupliquée lorsque l’outil de fusion remplace des GUID null avec des fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="0d34f-110">Authors of merge modules are responsible for ensuring that no existing primary key in the user's interface is duplicated when the merge tool replaces null GUIDs with features.</span></span>

 

 



