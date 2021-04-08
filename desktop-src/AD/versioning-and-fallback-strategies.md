---
title: Contrôle de version et stratégies de secours
description: Quand une application détecte une mise à jour partielle à l’aide de l’une des techniques précédentes ou lit un ensemble d’objets dont la date d’effet n’a pas encore été atteinte, l’application doit gérer la situation de manière appropriée.
ms.assetid: 6a34a783-98fd-406e-a96d-8e2a09a51c2d
ms.tgt_platform: multiple
keywords:
- Contrôle de version et stratégies de secours AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45f6383ad06e73457e18dddfac53295a0c16389c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839262"
---
# <a name="versioning-and-fallback-strategies"></a><span data-ttu-id="ffdeb-104">Contrôle de version et stratégies de secours</span><span class="sxs-lookup"><span data-stu-id="ffdeb-104">Versioning and Fallback Strategies</span></span>

<span data-ttu-id="ffdeb-105">Quand une application détecte une mise à jour partielle à l’aide de l’une des techniques précédentes ou lit un ensemble d’objets dont la date d’effet n’a pas encore été atteinte, l’application doit gérer la situation de manière appropriée.</span><span class="sxs-lookup"><span data-stu-id="ffdeb-105">When an application detects a partial update using one of the preceding techniques or reads a set of objects whose effective date has not yet been reached, the application must deal with the situation gracefully.</span></span> <span data-ttu-id="ffdeb-106">Pour certaines applications, la réponse normale consiste à « revenir » à une version précédente des objets en question.</span><span class="sxs-lookup"><span data-stu-id="ffdeb-106">For some applications, the graceful response is to "fall back" to a previous version of the objects in question.</span></span> <span data-ttu-id="ffdeb-107">Active Directory Domain Services ne fournissez pas de fonctionnalité de contrôle de version, les applications qui souhaitent que cette fonctionnalité les fournisse eux-mêmes.</span><span class="sxs-lookup"><span data-stu-id="ffdeb-107">Active Directory Domain Services do not provide a versioning facility—applications that want this capability must provide it themselves.</span></span> <span data-ttu-id="ffdeb-108">Les approches de la gestion des versions incluent la conservation locale des valeurs « dernières bonnes connues » et le stockage de plusieurs ensembles d’objets dans l’annuaire, par exemple, dans les conteneurs « ancien », « actuel » et « nouveau ».</span><span class="sxs-lookup"><span data-stu-id="ffdeb-108">Approaches to versioning include keeping the "last known good" values cached locally and storing multiple sets of objects in the directory, for example, in "old," "current," and "new" containers.</span></span> <span data-ttu-id="ffdeb-109">De nombreux autres schémas sont possibles.</span><span class="sxs-lookup"><span data-stu-id="ffdeb-109">Many other schemes are possible.</span></span>

<span data-ttu-id="ffdeb-110">Les implémentations doivent veiller à éviter des conséquences inattendues.</span><span class="sxs-lookup"><span data-stu-id="ffdeb-110">Implementations must take care to avoid unintended consequences.</span></span> <span data-ttu-id="ffdeb-111">Une version antérieure d’objets doit être utilisée uniquement lorsqu’une mise à jour partielle est détectée ou que les nouveaux objets ne sont pas encore « effectifs ».</span><span class="sxs-lookup"><span data-stu-id="ffdeb-111">An earlier version of objects should be used only when a partial update is detected or the new objects are not yet "effective."</span></span> <span data-ttu-id="ffdeb-112">En arrière-plan, car un événement de l’application « ne fonctionne pas » peut contourner l’intention d’un administrateur.</span><span class="sxs-lookup"><span data-stu-id="ffdeb-112">Falling back because something in the application "does not work" might circumvent an administrator's intent.</span></span> <span data-ttu-id="ffdeb-113">Par exemple, deux ordinateurs qui pouvaient auparavant communiquer peuvent se trouver incapables de le faire en raison d’une modification de la stratégie IPsec (Internet Protocol Security).</span><span class="sxs-lookup"><span data-stu-id="ffdeb-113">For example, two computers that formerly could communicate might find themselves unable to do so because of a change in Internet Protocol security (IPsec) policy.</span></span> <span data-ttu-id="ffdeb-114">Si cela est intentionnel pour la part de l’administrateur, les systèmes affectés ne doivent pas revenir à la stratégie qui leur a permis de communiquer, car il s’agit d’une violation de la sécurité.</span><span class="sxs-lookup"><span data-stu-id="ffdeb-114">If this is intentional on the part of the administrator, the affected systems should not fall back to the policy that allowed them to communicate, as this would be a security breach.</span></span>

 

 




