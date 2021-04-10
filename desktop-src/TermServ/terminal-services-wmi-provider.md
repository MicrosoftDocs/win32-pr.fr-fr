---
title: Fournisseur WMI Services Bureau à distance
description: Le fournisseur WMI Services Bureau à distance fournit un accès par programmation aux informations et aux paramètres qui sont exposés par le composant logiciel enfichable MMC (Microsoft Management Console) configuration/connections Services Bureau à distance.
ms.assetid: d205a3da-3f9a-4ee1-9c99-a39e9cce0a11
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance Services Bureau à distance, fournisseur WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25d947db18c0cde63bcb6c4c3954fc9811e0f0f1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031403"
---
# <a name="remote-desktop-services-wmi-provider"></a><span data-ttu-id="903cd-104">Fournisseur WMI Services Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="903cd-104">Remote Desktop Services WMI provider</span></span>

<span data-ttu-id="903cd-105">Le fournisseur WMI Services Bureau à distance fournit un accès par programmation aux informations et aux paramètres qui sont exposés par le composant logiciel enfichable MMC (Microsoft Management Console) configuration/connections Services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="903cd-105">The Remote Desktop Services WMI provider provides programmatic access to the information and settings that are exposed by the Remote Desktop Services Configuration/Connections Microsoft Management Console (MMC) snap-in.</span></span>

<span data-ttu-id="903cd-106">La DLL du fournisseur est chargée par le processus de gestion Windows (Winmgmt.exe) lorsqu’un client envoie une demande au serveur.</span><span class="sxs-lookup"><span data-stu-id="903cd-106">The provider DLL is loaded by the Windows Management process (Winmgmt.exe) when a client makes a request to the server.</span></span> <span data-ttu-id="903cd-107">L’administration est possible à l’aide des méthodes du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="903cd-107">Administration is possible by using the provider methods.</span></span> <span data-ttu-id="903cd-108">Le fournisseur est inscrit à la fois comme instance et comme fournisseur de méthode.</span><span class="sxs-lookup"><span data-stu-id="903cd-108">The provider is registered as both an instance and a method provider.</span></span>

<span data-ttu-id="903cd-109">Le fournisseur WMI Services Bureau à distance a été implémenté en tant que fournisseur dynamique dérivé de la classe de base du [**\_ service Win32**](/windows/desktop/CIMWin32Prov/win32-service) , en héritant de toutes ses propriétés et méthodes, et d’une bibliothèque de liens dynamiques in-process.</span><span class="sxs-lookup"><span data-stu-id="903cd-109">The Remote Desktop Services WMI provider has been implemented as a dynamic provider derived from the [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) base class, inheriting all of its properties and methods, and an in-process dynamic link library.</span></span>

<span data-ttu-id="903cd-110">Pour plus d’informations, consultez la [services Bureau à distance référence du fournisseur WMI](terminal-services-wmi-provider-reference.md).</span><span class="sxs-lookup"><span data-stu-id="903cd-110">For more information, see the [Remote Desktop Services WMI Provider reference](terminal-services-wmi-provider-reference.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="903cd-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="903cd-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="903cd-112">Référence du fournisseur WMI Services Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="903cd-112">Remote Desktop Services WMI Provider Reference</span></span>](terminal-services-wmi-provider-reference.md)
</dt> </dl>

 

 