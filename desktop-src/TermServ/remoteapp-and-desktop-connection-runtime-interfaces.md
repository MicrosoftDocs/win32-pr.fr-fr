---
title: Interfaces d’exécution Connexions aux programmes RemoteApp et aux services Bureau à distance
description: Prend en charge les interfaces qui permettent le développement de clients personnalisés dans Connexions aux programmes RemoteApp et aux services Bureau à distance.
ms.assetid: 4580df05-5e44-40d0-8765-5d9b4e1d339e
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance Services Bureau à distance, Connexions aux programmes RemoteApp et aux services Bureau à distance référence de l’API Runtime
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6b7c3c2fd3841cfe797fc559ba1aa30d3479436
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104100941"
---
# <a name="remoteapp-and-desktop-connection-runtime-interfaces"></a><span data-ttu-id="11145-104">Interfaces d’exécution Connexions aux programmes RemoteApp et aux services Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="11145-104">RemoteApp and Desktop Connection Runtime interfaces</span></span>

<span data-ttu-id="11145-105">L’API du runtime Connexions aux programmes RemoteApp et aux services Bureau à distance prend en charge les interfaces qui permettent le développement de clients personnalisés dans Connexions aux programmes RemoteApp et aux services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="11145-105">The RemoteApp and Desktop Connection Runtime API supports interfaces that allow the development of custom clients in RemoteApp and Desktop Connection.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="11145-106">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="11145-106">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="11145-107">**IWorkspace**</span><span class="sxs-lookup"><span data-stu-id="11145-107">**IWorkspace**</span></span>](/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspace)
</dt> <dd>

<span data-ttu-id="11145-108">Expose des méthodes qui fournissent des informations sur une connexion dans Connexions aux programmes RemoteApp et aux services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="11145-108">Exposes methods that provide information about a connection in RemoteApp and Desktop Connection.</span></span>

</dd> <dt>

[<span data-ttu-id="11145-109">**IWorkspace2**</span><span class="sxs-lookup"><span data-stu-id="11145-109">**IWorkspace2**</span></span>](/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspace2)
</dt> <dd>

<span data-ttu-id="11145-110">Expose des méthodes supplémentaires qui fournissent des informations sur une connexion dans Connexions aux programmes RemoteApp et aux services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="11145-110">Exposes additional methods that provide information about a connection in RemoteApp and Desktop Connection.</span></span>

</dd> <dt>

[<span data-ttu-id="11145-111">**IWorkspace3**</span><span class="sxs-lookup"><span data-stu-id="11145-111">**IWorkspace3**</span></span>](/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspace3)
</dt> <dd>

<span data-ttu-id="11145-112">Expose des méthodes qui fournissent des informations sur une connexion dans Connexions aux programmes RemoteApp et aux services Bureau à distance, et ajoute la possibilité de récupérer ou de définir un jeton de revendications.</span><span class="sxs-lookup"><span data-stu-id="11145-112">Exposes methods that provide information about a connection in RemoteApp and Desktop Connection, and adds the ability to retrieve or set a claims token.</span></span>

</dd> <dt>

[<span data-ttu-id="11145-113">**IWorkspaceClientExt**</span><span class="sxs-lookup"><span data-stu-id="11145-113">**IWorkspaceClientExt**</span></span>](/windows/desktop/api/Workspaceruntimeclientext/nn-workspaceruntimeclientext-iworkspaceclientext)
</dt> <dd>

<span data-ttu-id="11145-114">Expose des méthodes qui permettent au runtime de déconnecter un client personnalisé dans Connexions aux programmes RemoteApp et aux services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="11145-114">Exposes methods that allow the runtime to disconnect a custom client in RemoteApp and Desktop Connection.</span></span>

</dd> <dt>

[<span data-ttu-id="11145-115">**IWorkspaceRegistration**</span><span class="sxs-lookup"><span data-stu-id="11145-115">**IWorkspaceRegistration**</span></span>](/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspaceregistration)
</dt> <dd>

<span data-ttu-id="11145-116">Expose des méthodes qui ajoutent et suppriment des références à des clients personnalisés dans Connexions aux programmes RemoteApp et aux services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="11145-116">Exposes methods that add and remove references to custom clients in RemoteApp and Desktop Connection.</span></span>

</dd> <dt>

[<span data-ttu-id="11145-117">**IWorkspaceRegistration2**</span><span class="sxs-lookup"><span data-stu-id="11145-117">**IWorkspaceRegistration2**</span></span>](/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspaceregistration2)
</dt> <dd>

<span data-ttu-id="11145-118">Expose des méthodes qui ajoutent et suppriment des références à des clients personnalisés dans Connexions aux programmes RemoteApp et aux services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="11145-118">Exposes methods that add and remove references to custom clients in RemoteApp and Desktop Connection.</span></span>

</dd> <dt>

[<span data-ttu-id="11145-119">**IWorkspaceReportMessage**</span><span class="sxs-lookup"><span data-stu-id="11145-119">**IWorkspaceReportMessage**</span></span>](/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspacereportmessage)
</dt> <dd>

<span data-ttu-id="11145-120">Expose des méthodes qui prennent en charge la gestion des messages d’erreur pour les espaces de travail distants.</span><span class="sxs-lookup"><span data-stu-id="11145-120">Exposes methods that support error message handling for remote workspaces.</span></span>

</dd> <dt>

[<span data-ttu-id="11145-121">**IWorkspaceResTypeRegistry**</span><span class="sxs-lookup"><span data-stu-id="11145-121">**IWorkspaceResTypeRegistry**</span></span>](/windows/desktop/api/Workspaceax/nn-workspaceax-iworkspacerestyperegistry)
</dt> <dd>

<span data-ttu-id="11145-122">Expose des méthodes qui permettent à un plug-in de gérer des extensions de nom de fichier tierces dans Connexions aux programmes RemoteApp et aux services Bureau à distance Runtime.</span><span class="sxs-lookup"><span data-stu-id="11145-122">Exposes methods that allow a plug-in to manage third-party file name extensions in RemoteApp and Desktop Connection runtime.</span></span>

</dd> <dt>

[<span data-ttu-id="11145-123">**IWorkspaceScriptable**</span><span class="sxs-lookup"><span data-stu-id="11145-123">**IWorkspaceScriptable**</span></span>](/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspacescriptable)
</dt> <dd>

<span data-ttu-id="11145-124">Expose des méthodes qui gèrent les informations d’identification et les connexions de Connexions aux programmes RemoteApp et aux services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="11145-124">Exposes methods that manage RemoteApp and Desktop Connection credentials and connections.</span></span>

</dd> <dt>

[<span data-ttu-id="11145-125">**IWorkspaceScriptable2**</span><span class="sxs-lookup"><span data-stu-id="11145-125">**IWorkspaceScriptable2**</span></span>](/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspacescriptable2)
</dt> <dd>

<span data-ttu-id="11145-126">Expose des méthodes qui gèrent les informations d’identification et les connexions de Connexions aux programmes RemoteApp et aux services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="11145-126">Exposes methods that manage RemoteApp and Desktop Connection credentials and connections.</span></span>

</dd> <dt>

[<span data-ttu-id="11145-127">**IWorkspaceScriptable3**</span><span class="sxs-lookup"><span data-stu-id="11145-127">**IWorkspaceScriptable3**</span></span>](/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspacescriptable3)
</dt> <dd>

<span data-ttu-id="11145-128">Expose des méthodes qui gèrent les informations d’identification et les connexions de Connexions aux programmes RemoteApp et aux services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="11145-128">Exposes methods that manage RemoteApp and Desktop Connection credentials and connections.</span></span>

</dd> </dl>

 

 




