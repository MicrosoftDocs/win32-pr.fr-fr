---
title: Restauration du système
description: Définit des points de restauration système et surveille les modifications système principales d’un programme pour permettre une restauration du système à un état antérieur. Écrire du code de récupération automatique ou un script WMI pour restaurer l’état du système sur un point de restauration enregistré.
ms.assetid: 6861eedc-2bd9-49c7-8682-ea557fa29d28
keywords:
- Restauration du système
- Restauration du système, page de démarrage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e0bdc4555171ad867f6e6b925144d9ed673ffc3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101933"
---
# <a name="system-restore"></a><span data-ttu-id="49b86-106">Restauration du système</span><span class="sxs-lookup"><span data-stu-id="49b86-106">System Restore</span></span>

## <a name="purpose"></a><span data-ttu-id="49b86-107">Objectif</span><span class="sxs-lookup"><span data-stu-id="49b86-107">Purpose</span></span>

<span data-ttu-id="49b86-108">La restauration du système surveille et enregistre automatiquement les modifications système principales sur l’ordinateur d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="49b86-108">System Restore automatically monitors and records key system changes on a user's computer.</span></span> <span data-ttu-id="49b86-109">Il est conçu pour réduire les coûts de support et accroître la satisfaction des clients en permettant à un utilisateur d’annuler une modification susceptible d’être à l’origine d’un problème au niveau du système, ou de revenir à un jour lorsque le système était optimal.</span><span class="sxs-lookup"><span data-stu-id="49b86-109">It is designed to reduce support costs and increase customer satisfaction by enabling a user to undo a change that may have caused a problem with the system, or revert to a day when the system was performing optimally.</span></span>

> [!Note]  
> <span data-ttu-id="49b86-110">La documentation suivante est destinée aux développeurs.</span><span class="sxs-lookup"><span data-stu-id="49b86-110">The following documentation is targeted for developers.</span></span> <span data-ttu-id="49b86-111">Si vous êtes un utilisateur final à la recherche d’informations sur l’utilisation de la restauration du système, consultez [qu’est-ce que la restauration du système ?](https://windows.microsoft.com/windows/What-is-System-Restore#1TC=windows-7)</span><span class="sxs-lookup"><span data-stu-id="49b86-111">If you are an end-user looking for information on how to use System Restore, see [What Is System Restore?](https://windows.microsoft.com/windows/What-is-System-Restore#1TC=windows-7)</span></span>

 

## <a name="developer-audience"></a><span data-ttu-id="49b86-112">Développeurs concernés</span><span class="sxs-lookup"><span data-stu-id="49b86-112">Developer audience</span></span>

<span data-ttu-id="49b86-113">L’API de restauration du système est conçue pour être utilisée par les programmeurs C/C++.</span><span class="sxs-lookup"><span data-stu-id="49b86-113">The System Restore API is designed for use by C/C++ programmers.</span></span> <span data-ttu-id="49b86-114">Une bonne connaissance de Windows Management Instrumentation (WMI) est nécessaire pour utiliser l’interface de script.</span><span class="sxs-lookup"><span data-stu-id="49b86-114">A familiarity with Windows Management Instrumentation (WMI) is required to use the scripting interface.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="49b86-115">Conditions d’exécution</span><span class="sxs-lookup"><span data-stu-id="49b86-115">Run-time requirements</span></span>

<span data-ttu-id="49b86-116">L’API de restauration du système est prise en charge sur les systèmes d’exploitation clients à partir de Windows XP.</span><span class="sxs-lookup"><span data-stu-id="49b86-116">The System Restore API is supported on client operating systems starting with Windows XP.</span></span> <span data-ttu-id="49b86-117">Pour plus d’informations sur les systèmes d’exploitation requis pour utiliser un élément d’API particulier, consultez la section Configuration requise de sa documentation.</span><span class="sxs-lookup"><span data-stu-id="49b86-117">For information about which operating systems are required to use a particular API element, see the Requirements section of its documentation.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="49b86-118">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="49b86-118">In this section</span></span>



| <span data-ttu-id="49b86-119">Rubrique</span><span class="sxs-lookup"><span data-stu-id="49b86-119">Topic</span></span>                                                | <span data-ttu-id="49b86-120">Description</span><span class="sxs-lookup"><span data-stu-id="49b86-120">Description</span></span>                                                                    |
|------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="49b86-121">Vue d'ensemble</span><span class="sxs-lookup"><span data-stu-id="49b86-121">Overview</span></span>](about-system-restore.md)<br/>      | <span data-ttu-id="49b86-122">Vue d’ensemble du fonctionnement de la restauration du système.</span><span class="sxs-lookup"><span data-stu-id="49b86-122">An overview of how System Restore works.</span></span><br/>                            |
| [<span data-ttu-id="49b86-123">Référence</span><span class="sxs-lookup"><span data-stu-id="49b86-123">Reference</span></span>](system-restore-reference.md)<br/> | <span data-ttu-id="49b86-124">Documentation des fonctions, structures et classes de restauration du système.</span><span class="sxs-lookup"><span data-stu-id="49b86-124">Documentation of System Restore functions, structures, and classes.</span></span><br/> |
| [<span data-ttu-id="49b86-125">Exemples</span><span class="sxs-lookup"><span data-stu-id="49b86-125">Samples</span></span>](using-system-restore.md)<br/>       | <span data-ttu-id="49b86-126">Exemple de programme écrit en C.</span><span class="sxs-lookup"><span data-stu-id="49b86-126">A sample program written in C.</span></span><br/>                                      |



 

## <a name="related-topics"></a><span data-ttu-id="49b86-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="49b86-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="49b86-128">WMI</span><span class="sxs-lookup"><span data-stu-id="49b86-128">WMI</span></span>](/windows/desktop/WmiSdk/wmi-start-page)
</dt> </dl>

 

