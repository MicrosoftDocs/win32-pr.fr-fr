---
description: À compter de Windows Server 2008, le fournisseur de fonctionnalités serveur fournit des informations sur les composants serveur installés sur le serveur. Cette classe permet aux administrateurs d’inventorier et de gérer leurs rôles serveur et leurs fonctionnalités.
ms.assetid: f7932eaa-6730-4301-9809-32de9c1a20de
ms.tgt_platform: multiple
title: Fournisseur de fonctionnalités serveur
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 73666dc810a40f33e3d35acb1b9d7ade5d2b021a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534307"
---
# <a name="server-feature-provider"></a><span data-ttu-id="3d874-104">Fournisseur de fonctionnalités serveur</span><span class="sxs-lookup"><span data-stu-id="3d874-104">Server Feature Provider</span></span>

<span data-ttu-id="3d874-105">À compter de Windows Server 2008, le fournisseur de fonctionnalités serveur fournit des informations sur les composants serveur installés sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="3d874-105">Starting with Windows Server 2008, the Server Feature Provider supplies information on what server features are installed on the server.</span></span> <span data-ttu-id="3d874-106">Cette classe permet aux administrateurs d’inventorier et de gérer leurs rôles serveur et leurs fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="3d874-106">This class allows administrators to inventory and manage their server roles and features.</span></span>

<span data-ttu-id="3d874-107">Un rôle de serveur est défini comme un groupe de composants qui fournissent des fonctions pour une zone de fonctionnalités spécifique, telles que l’impression, les fichiers, le contrôle de domaine, etc.</span><span class="sxs-lookup"><span data-stu-id="3d874-107">A server role is defined as a group of components that provide functions for a specific area of functionality, such as printing, files, domain control, and so on.</span></span> <span data-ttu-id="3d874-108">Les rôles de serveur classiques sont serveur de fichiers, serveur de messagerie, serveur DNS, contrôleur de domaine, serveur d’applications, etc.</span><span class="sxs-lookup"><span data-stu-id="3d874-108">Typical server roles are File Server, Mail Server, DNS Server, Domain Controller, Application Server, and so on.</span></span>

<span data-ttu-id="3d874-109">Si une entreprise n’exécute pas de logiciel de gestion qui signale des rôles de serveur, par exemple Microsoft Operations Manager avec les packs d’administration installés, vous pouvez obtenir ces informations en interrogeant la classe [**Win32 \_ ServerFeature**](win32-serverfeature.md) .</span><span class="sxs-lookup"><span data-stu-id="3d874-109">If an enterprise is not running management software that reports server roles, such as Microsoft Operations Manager with management packs installed, then you can obtain that information by querying the [**Win32\_ServerFeature**](win32-serverfeature.md) class.</span></span> <span data-ttu-id="3d874-110">Les informations sur les fonctionnalités et les rôles serveur des ordinateurs distants sont disponibles via des connexions à distance WMI normales ou à l’aide du service Windows Remote Management (WinRM).</span><span class="sxs-lookup"><span data-stu-id="3d874-110">Server role and feature information from remote computers is available through normal WMI remote connections or by using the Windows Remote Management (WinRM) service.</span></span> <span data-ttu-id="3d874-111">Pour plus d’informations sur les connexions WMI DCOM à distance, consultez [connexion à WMI sur un ordinateur distant](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="3d874-111">For more information about remote WMI DCOM connections, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span> <span data-ttu-id="3d874-112">Pour plus d’informations sur les connexions utilisant le protocole [*WS-Management*](/windows/desktop/WinRM/windows-remote-management-glossary) , consultez [Windows Remote Management](/windows/desktop/WinRM/portal).</span><span class="sxs-lookup"><span data-stu-id="3d874-112">For more information about connections using the [*WS-Management*](/windows/desktop/WinRM/windows-remote-management-glossary) protocol, see [Windows Remote Management](/windows/desktop/WinRM/portal).</span></span>

<span data-ttu-id="3d874-113">Le fournisseur de fonctionnalités serveur prend en charge les classes WMI suivantes :</span><span class="sxs-lookup"><span data-stu-id="3d874-113">The Server Feature Provider supports the following WMI classes:</span></span>

-   [<span data-ttu-id="3d874-114">**\_ServerFeature Win32**</span><span class="sxs-lookup"><span data-stu-id="3d874-114">**Win32\_ServerFeature**</span></span>](win32-serverfeature.md)

## <a name="related-topics"></a><span data-ttu-id="3d874-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3d874-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3d874-116">Fournisseurs WMI</span><span class="sxs-lookup"><span data-stu-id="3d874-116">WMI Providers</span></span>](wmi-providers.md)
</dt> </dl>

 

 
