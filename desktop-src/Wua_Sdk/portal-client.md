---
description: L’API Windows Update Agent (WUA) est un ensemble d’interfaces COM qui permettent aux administrateurs système et aux programmeurs d’accéder à Windows Update et Windows Server Update Services (WSUS).
ms.assetid: 611dc759-e0fc-472e-bdc2-fb952ba74999
title: API de l’agent de Windows Update
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19c34cb76619c9739c84e650a32590fdc4f61022
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749997"
---
# <a name="windows-update-agent-api"></a><span data-ttu-id="d9298-103">API de l’agent de Windows Update</span><span class="sxs-lookup"><span data-stu-id="d9298-103">Windows Update Agent API</span></span>

## <a name="purpose"></a><span data-ttu-id="d9298-104">Objectif</span><span class="sxs-lookup"><span data-stu-id="d9298-104">Purpose</span></span>

<span data-ttu-id="d9298-105">L’API Windows Update Agent (WUA) est un ensemble d’interfaces COM qui permettent aux administrateurs système et aux programmeurs d’accéder à Windows Update et [Windows Server Update Services (WSUS)](/previous-versions/windows/desktop/ms744624(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d9298-105">The Windows Update Agent (WUA) API is a set of COM interfaces that enable system administrators and programmers to access Windows Update and [Windows Server Update Services (WSUS)](/previous-versions/windows/desktop/ms744624(v=vs.85)).</span></span> <span data-ttu-id="d9298-106">Les scripts et les programmes peuvent être écrits pour examiner les mises à jour actuellement disponibles pour un ordinateur, puis vous pouvez installer ou désinstaller des mises à jour.</span><span class="sxs-lookup"><span data-stu-id="d9298-106">Scripts and programs can be written to examine which updates are currently available for a computer, and then you can install or uninstall updates.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="d9298-107">Le cas échéant</span><span class="sxs-lookup"><span data-stu-id="d9298-107">Where applicable</span></span>

<span data-ttu-id="d9298-108">Les administrateurs système peuvent utiliser WUA pour déterminer par programmation les mises à jour à appliquer à un ordinateur, télécharger ces mises à jour, puis les installer avec peu ou pas d’intervention de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d9298-108">System administrators can use WUA to programmatically determine which updates should be applied to a computer, download those updates, and then install them with little or no user intervention.</span></span>

<span data-ttu-id="d9298-109">Les éditeurs de logiciels indépendants (ISV) et les développeurs d’utilisateurs finaux peuvent intégrer les fonctionnalités de WUA dans le logiciel de gestion d’ordinateur ou de gestion des mises à jour pour fournir un environnement d’exploitation transparent.</span><span class="sxs-lookup"><span data-stu-id="d9298-109">Independent software vendors (ISV) and end-user developers can integrate WUA features into computer management or update management software to provide a seamless operating environment.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="d9298-110">Développeurs concernés</span><span class="sxs-lookup"><span data-stu-id="d9298-110">Developer audience</span></span>

<span data-ttu-id="d9298-111">Vous pouvez écrire des applications WUA dans plusieurs langages de programmation.</span><span class="sxs-lookup"><span data-stu-id="d9298-111">You can write WUA applications in several programming languages.</span></span> <span data-ttu-id="d9298-112">WUA définit des interfaces et des objets accessibles à partir de Visual Basic, Visual Basic Scripting Edition (VBScript), JScript et à partir de C et C++.</span><span class="sxs-lookup"><span data-stu-id="d9298-112">WUA defines interfaces and objects that are accessible from Visual Basic, Visual Basic Scripting Edition (VBScript), JScript, and from C and C++.</span></span> <span data-ttu-id="d9298-113">Une bonne connaissance de la programmation COM est utile pour le programmeur WUA.</span><span class="sxs-lookup"><span data-stu-id="d9298-113">A familiarity with COM programming is useful to the WUA programmer.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="d9298-114">Conditions d’exécution</span><span class="sxs-lookup"><span data-stu-id="d9298-114">Run-time requirements</span></span>

<span data-ttu-id="d9298-115">WUA est pris en charge à partir de Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d9298-115">WUA is supported starting with Windows XP.</span></span> <span data-ttu-id="d9298-116">WUA est pris en charge sur le serveur à partir de Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="d9298-116">WUA is supported on the server starting with Windows Server 2003.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="d9298-117">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="d9298-117">In this section</span></span>

-   [<span data-ttu-id="d9298-118">Utilisation de l’API Windows Update Agent</span><span class="sxs-lookup"><span data-stu-id="d9298-118">Using the Windows Update Agent API</span></span>](using-the-windows-update-agent-api.md)
-   [<span data-ttu-id="d9298-119">Informations de référence sur l’API WUA</span><span class="sxs-lookup"><span data-stu-id="d9298-119">WUA API Reference</span></span>](windows-update-agent--wua--api-reference.md)

 

 
