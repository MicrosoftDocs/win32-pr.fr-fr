---
description: Les fournisseurs de composants partagés doivent envisager de rendre leur composant disponible en tant qu’assembly côte à côte si un ou plusieurs des cas suivants sont vrais.
ms.assetid: 543451cd-0608-4302-a85b-ddce79a5cfd6
title: Devez-vous fournir un composant partagé comme assembly côte à côte ?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 733adf400ba9ce019d9f749fcd79a1a71380c9e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867882"
---
# <a name="should-you-provide-a-shared-component-as-a-side-by-side-assembly"></a><span data-ttu-id="7f5ca-103">Devez-vous fournir un composant partagé comme assembly côte à côte ?</span><span class="sxs-lookup"><span data-stu-id="7f5ca-103">Should you provide a shared component as a side-by-side assembly?</span></span>

<span data-ttu-id="7f5ca-104">Les fournisseurs de composants partagés doivent envisager de rendre leur composant disponible en tant qu’assembly côte à côte si une ou plusieurs des conditions suivantes sont vraies :</span><span class="sxs-lookup"><span data-stu-id="7f5ca-104">Providers of shared components should consider making their component available as a side-by-side assembly if one or more of the following are true:</span></span>

-   <span data-ttu-id="7f5ca-105">Le composant expose une interface de programmation d’applications riche qui est utilisée par de nombreuses applications.</span><span class="sxs-lookup"><span data-stu-id="7f5ca-105">The component exposes a rich application programming interface that is used by many applications.</span></span> <span data-ttu-id="7f5ca-106">Par exemple, un composant tel que MSHTML, qui permet aux applications C et C++ d’accéder au modèle objet DHTML (Dynamic HTML).</span><span class="sxs-lookup"><span data-stu-id="7f5ca-106">For example, a component such as MSHTML, which enables C and C++ applications to access the Dynamic HTML (DHTML) Object Model.</span></span>
-   <span data-ttu-id="7f5ca-107">Le composant est déjà partagé par plusieurs applications.</span><span class="sxs-lookup"><span data-stu-id="7f5ca-107">The component is already being shared by multiple applications.</span></span> <span data-ttu-id="7f5ca-108">Par exemple, un composant tel que COMCTL32, qui fournit aux applications un accès aux contrôles communs.</span><span class="sxs-lookup"><span data-stu-id="7f5ca-108">For example, a component such as COMCTL32, which provides applications access to the common controls.</span></span>
-   <span data-ttu-id="7f5ca-109">Le composant est un nouveau composant.</span><span class="sxs-lookup"><span data-stu-id="7f5ca-109">The component is a new component.</span></span>
-   <span data-ttu-id="7f5ca-110">Le composant est un composant en mode utilisateur et non un pilote de périphérique.</span><span class="sxs-lookup"><span data-stu-id="7f5ca-110">The component is a user-mode component and not a device driver.</span></span>

<span data-ttu-id="7f5ca-111">Tous les composants ne sont pas un candidat approprié pour un assembly côte à côte.</span><span class="sxs-lookup"><span data-stu-id="7f5ca-111">Not every component is a suitable candidate for a side-by-side assembly.</span></span> <span data-ttu-id="7f5ca-112">Un composant n’est pas un candidat approprié pour un assembly côte à côte si l’une des conditions suivantes est vraie :</span><span class="sxs-lookup"><span data-stu-id="7f5ca-112">A component is not a suitable candidate for a side-by-side assembly if any of the following are true:</span></span>

-   <span data-ttu-id="7f5ca-113">Le composant gère la communication entre les applications.</span><span class="sxs-lookup"><span data-stu-id="7f5ca-113">The component handles communication between applications.</span></span> <span data-ttu-id="7f5ca-114">Par exemple, certaines parties de OLE32 ne constituent pas un bon assembly côte à côte, car vous ne souhaitez pas avoir deux versions différentes des parties qui coordonnent la communication entre les applications exécutées sur votre système.</span><span class="sxs-lookup"><span data-stu-id="7f5ca-114">For example, parts of OLE32 would not make a good side-by-side assembly because you would not want to have two different versions of the parts that coordinate communication between applications run on your system.</span></span>
-   <span data-ttu-id="7f5ca-115">Le composant gère un appareil physique ou virtuel pour le système.</span><span class="sxs-lookup"><span data-stu-id="7f5ca-115">The component manages a physical or virtual device for the system.</span></span> <span data-ttu-id="7f5ca-116">Par exemple, un pilote de périphérique pour un spouleur d’impression.</span><span class="sxs-lookup"><span data-stu-id="7f5ca-116">For example a device driver for a print spooler.</span></span>

<span data-ttu-id="7f5ca-117">Dans certains cas, il est possible pour le développeur du composant de reconcevoir un composant existant afin de le rendre adapté à la publication en tant qu’assembly côte à côte.</span><span class="sxs-lookup"><span data-stu-id="7f5ca-117">In some cases it may be possible for the developer of the component to redesign an existing component in order to make it suitable for publication as a side-by-side assembly.</span></span> <span data-ttu-id="7f5ca-118">Pour plus d’informations, consultez [instructions relatives à la création d’assemblys côte à côte](guidelines-for-creating-side-by-side-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="7f5ca-118">For more information see [Guidelines for Creating Side-by-side Assemblies](guidelines-for-creating-side-by-side-assemblies.md).</span></span>

 

 



