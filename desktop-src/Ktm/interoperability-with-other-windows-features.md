---
description: Le Distributed Transaction Coordinator (DTC) active les transactions distribuées ou les transactions qui sont sous le contrôle de plusieurs gestionnaires de ressources sur un ou plusieurs systèmes. KTM et DTC fonctionnent étroitement ensemble pour y parvenir.
ms.assetid: 468379e2-c5f6-479f-9d5d-42afb395ec9b
title: Interopérabilité avec d’autres fonctionnalités Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa3aeac3d920b408a9a18c32eab83cf747525e82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529287"
---
# <a name="interoperability-with-other-windows-features"></a><span data-ttu-id="239c3-104">Interopérabilité avec d’autres fonctionnalités Windows</span><span class="sxs-lookup"><span data-stu-id="239c3-104">Interoperability With Other Windows Features</span></span>

<span data-ttu-id="239c3-105">Le [Distributed Transaction Coordinator](/previous-versions/windows/desktop/ms684146(v=vs.85)) (DTC) active les *transactions distribuées* ou les transactions qui sont sous le contrôle de plusieurs gestionnaires de ressources sur un ou plusieurs systèmes.</span><span class="sxs-lookup"><span data-stu-id="239c3-105">The [Distributed Transaction Coordinator](/previous-versions/windows/desktop/ms684146(v=vs.85)) (DTC) enables *distributed transactions*, or transactions that are under the control of multiple resource managers on one or more systems.</span></span> <span data-ttu-id="239c3-106">KTM et DTC fonctionnent étroitement ensemble pour y parvenir.</span><span class="sxs-lookup"><span data-stu-id="239c3-106">KTM and DTC work closely together to accomplish this.</span></span>

<span data-ttu-id="239c3-107">COM+ expose un modèle déclaratif pour la programmation transactionnelle.</span><span class="sxs-lookup"><span data-stu-id="239c3-107">COM+ exposes a declarative model for transactional programming.</span></span> <span data-ttu-id="239c3-108">En d’autres termes, le programmeur déclare dans quelle mesure un objet peut tirer parti des transactions et le runtime COM+ gère les transactions au nom de l’objet.</span><span class="sxs-lookup"><span data-stu-id="239c3-108">In other words, the programmer declares the extent to which an object can take advantage of transactions, and the COM+ runtime manages the transactions on the object's behalf.</span></span> <span data-ttu-id="239c3-109">Par exemple, un objet peut être déclaré pour participer à une transaction uniquement s’il en existe déjà un, pour exiger une transaction (une transaction est créée si elle n’existe pas déjà), pour exiger une nouvelle transaction (créée, qu’il en existe déjà une) ou non transactionnelle.</span><span class="sxs-lookup"><span data-stu-id="239c3-109">For example, an object can be declared to participate in a transaction only if one already exists, to require a transaction (one is created if it does not already exist), to require a new transaction (one is created regardless of whether one already exists), or is not transactional.</span></span> <span data-ttu-id="239c3-110">Ces transactions gérées de façon déclarative sont automatiquement utilisées sur les connexions de base de données créées par des objets COM+ qui s’exécutent dans le contexte d’une transaction.</span><span class="sxs-lookup"><span data-stu-id="239c3-110">These declaratively-managed transactions are automatically used on database connections created by COM+ objects that are executing in the context of a transaction.</span></span>

 

 
