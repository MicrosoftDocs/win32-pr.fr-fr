---
title: Modes d’accès de stockage structuré
description: Les mécanismes de contrôle de l’accès simultané à un objet, par plusieurs processus et utilisateurs, sont essentiels.
ms.assetid: 2d524c2b-f2b4-49f2-9be8-2037846eb9e9
keywords:
- Stockage structuré Strctd STG, notions de base, fonctions API, indicateurs pour l’accès
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2e46a231cb5168d15564f0b86b064c8bfd19e38
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106521801"
---
# <a name="structured-storage-access-modes"></a><span data-ttu-id="f0d75-104">Modes d’accès de stockage structuré</span><span class="sxs-lookup"><span data-stu-id="f0d75-104">Structured Storage Access Modes</span></span>

<span data-ttu-id="f0d75-105">Les mécanismes de contrôle de l’accès simultané à un objet, par plusieurs processus et utilisateurs, sont essentiels.</span><span class="sxs-lookup"><span data-stu-id="f0d75-105">Mechanisms for controlling simultaneous access to an object, by multiple processes and users, are essential.</span></span> <span data-ttu-id="f0d75-106">COM fournit ces mécanismes en définissant les modes d’accès pour les objets de stockage et de flux.</span><span class="sxs-lookup"><span data-stu-id="f0d75-106">COM provides these mechanisms by defining access modes for both storage and stream objects.</span></span> <span data-ttu-id="f0d75-107">Le mode d’accès spécifié pour un objet de stockage parent est hérité par ses enfants, bien que vous puissiez placer des restrictions supplémentaires sur le flux ou le stockage enfant.</span><span class="sxs-lookup"><span data-stu-id="f0d75-107">The access mode specified for a parent storage object is inherited by its children, though you can place additional restrictions on the child storage or stream.</span></span> <span data-ttu-id="f0d75-108">Un objet de flux ou de stockage imbriqué peut être ouvert dans le même mode ou dans un mode plus restreint que celui de son parent, mais il ne peut pas être ouvert en mode moins restreint que celui de son parent.</span><span class="sxs-lookup"><span data-stu-id="f0d75-108">A nested storage or stream object can be opened in the same mode or in a more restricted mode than that of its parent, but it cannot be opened in a less restricted mode than that of its parent.</span></span>

<span data-ttu-id="f0d75-109">Vous spécifiez les modes d’accès à l’aide des valeurs indiquées dans [**constantes STGM**](stgm-constants.md).</span><span class="sxs-lookup"><span data-stu-id="f0d75-109">You specify access modes by using the values listed in [**STGM Constants**](stgm-constants.md).</span></span> <span data-ttu-id="f0d75-110">Ces valeurs servent d’indicateurs à passer comme arguments aux méthodes de l’interface [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) et aux fonctions API associées.</span><span class="sxs-lookup"><span data-stu-id="f0d75-110">These values serve as flags to be passed as arguments to methods in the [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) interface and associated API functions.</span></span> <span data-ttu-id="f0d75-111">En règle générale, plusieurs indicateurs sont combinés dans le paramètre *grfMode*, à l’aide d’une opération **or** booléenne.</span><span class="sxs-lookup"><span data-stu-id="f0d75-111">Typically, several flags are combined in the parameter *grfMode*, using a Boolean **OR** operation.</span></span>

<span data-ttu-id="f0d75-112">Les indicateurs sont répartis en six groupes.</span><span class="sxs-lookup"><span data-stu-id="f0d75-112">The flags fall into six groups.</span></span> <span data-ttu-id="f0d75-113">Un seul indicateur de chaque groupe peut être spécifié à la fois :</span><span class="sxs-lookup"><span data-stu-id="f0d75-113">Only one flag from each group can be specified at a time:</span></span>

-   [<span data-ttu-id="f0d75-114">Indicateurs de transaction</span><span class="sxs-lookup"><span data-stu-id="f0d75-114">Transaction Flags</span></span>](transaction-flags.md)
-   [<span data-ttu-id="f0d75-115">Indicateurs de création de stockage</span><span class="sxs-lookup"><span data-stu-id="f0d75-115">Storage Creation Flags</span></span>](storage-creation-flags.md)
-   [<span data-ttu-id="f0d75-116">Indicateurs de création temporaires</span><span class="sxs-lookup"><span data-stu-id="f0d75-116">Temporary Creation Flags</span></span>](temporary-creation-flags.md)
-   [<span data-ttu-id="f0d75-117">Indicateurs de priorité</span><span class="sxs-lookup"><span data-stu-id="f0d75-117">Priority Flags</span></span>](priority-flags.md)
-   [<span data-ttu-id="f0d75-118">Indicateurs d’autorisation d’accès</span><span class="sxs-lookup"><span data-stu-id="f0d75-118">Access Permission Flags</span></span>](access-permission-flags.md)
-   [<span data-ttu-id="f0d75-119">Indicateurs d’accès partagé</span><span class="sxs-lookup"><span data-stu-id="f0d75-119">Shared Access Flags</span></span>](shared-access-flags.md)

 

 




