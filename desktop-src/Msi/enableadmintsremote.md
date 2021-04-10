---
description: À partir de Windows Server 2008 et Windows Vista, cette stratégie n’a plus aucun effet.
ms.assetid: 27a4192e-0574-414d-993e-6c715577f0ba
title: EnableAdminTSRemote
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 383339ab5c2a592f3d6ab2cd81b4d6a446780411
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201966"
---
# <a name="enableadmintsremote"></a><span data-ttu-id="fbe38-103">EnableAdminTSRemote</span><span class="sxs-lookup"><span data-stu-id="fbe38-103">EnableAdminTSRemote</span></span>

<span data-ttu-id="fbe38-104">À partir de Windows Server 2008 et Windows Vista, cette stratégie n’a plus aucun effet.</span><span class="sxs-lookup"><span data-stu-id="fbe38-104">Beginning with Windows Server 2008 and Windows Vista, this policy no longer has any effect.</span></span> <span data-ttu-id="fbe38-105">Un administrateur peut effectuer une installation à partir de la session de console d’un serveur Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="fbe38-105">An administrator can perform an installation from the console session of a terminal server.</span></span> <span data-ttu-id="fbe38-106">Un administrateur peut également effectuer une installation à partir d’une session client du serveur Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="fbe38-106">An administrator can also perform an installation from a client session of the terminal server.</span></span>

<span data-ttu-id="fbe38-107">Pour plus d’informations, consultez [services Terminal Server](/windows/desktop/TermServ/terminal-services-portal) dans le kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="fbe38-107">For more information, see [Terminal Services](/windows/desktop/TermServ/terminal-services-portal) in the Microsoft Windows Software Development Kit (SDK).</span></span>

<span data-ttu-id="fbe38-108">\* \* Systèmes d’exploitation antérieurs à Windows Server 2008 et Windows Vista : \* \*</span><span class="sxs-lookup"><span data-stu-id="fbe38-108">\*\*Operating systems earlier than Windows Server 2008 and Windows Vista:  \*\*</span></span>

<span data-ttu-id="fbe38-109">La définition de cette [stratégie système](system-policy.md) par ordinateur permet aux administrateurs d’effectuer des installations à partir d’une session client du serveur Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="fbe38-109">Setting this per-machine [system policy](system-policy.md) enables administrators to perform installations from a client session of the terminal server.</span></span> <span data-ttu-id="fbe38-110">Si cette stratégie n’est pas définie, les administrateurs peuvent uniquement effectuer des installations à partir de la session de la console.</span><span class="sxs-lookup"><span data-stu-id="fbe38-110">If this policy is not set, administrators can only perform installations from the console session.</span></span> <span data-ttu-id="fbe38-111">Les utilisateurs non administratifs ne peuvent jamais effectuer des installations à partir d’une session client.</span><span class="sxs-lookup"><span data-stu-id="fbe38-111">Nonadministrative users can never perform installations from a client session.</span></span> <span data-ttu-id="fbe38-112">La valeur par défaut de cette stratégie permet uniquement aux administrateurs d’effectuer des installations à partir de la session de la console.</span><span class="sxs-lookup"><span data-stu-id="fbe38-112">The default value for this policy allows only administrators to perform installations from the console session.</span></span> <span data-ttu-id="fbe38-113">Les administrateurs peuvent toujours effectuer des [installations d’administration](administrative-installation.md) à partir d’une session cliente du serveur Terminal Server, ou à partir de la session de la console, que cette stratégie soit définie ou non.</span><span class="sxs-lookup"><span data-stu-id="fbe38-113">Administrators can always do [Administrative installations](administrative-installation.md) from a client session of the terminal server, or from the console session, regardless of whether this policy is set.</span></span>

## <a name="registry-key"></a><span data-ttu-id="fbe38-114">Clé de Registre</span><span class="sxs-lookup"><span data-stu-id="fbe38-114">Registry Key</span></span>

<span data-ttu-id="fbe38-115">**HKEY \_ \_** \\ **Stratégies logicielles** de l’ordinateur local \\  \\ **Microsoft** \\ **Windows** \\ **installer**</span><span class="sxs-lookup"><span data-stu-id="fbe38-115">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="fbe38-116">Type de données</span><span class="sxs-lookup"><span data-stu-id="fbe38-116">Data Type</span></span>

<span data-ttu-id="fbe38-117">**\_valeur DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="fbe38-117">**REG\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="fbe38-118">Notes</span><span class="sxs-lookup"><span data-stu-id="fbe38-118">Remarks</span></span>

<span data-ttu-id="fbe38-119">Pour plus d’informations, voir aussi [utilisation de Windows Installer avec une Terminal Server](using-windows-installer-with-a-terminal-server.md).</span><span class="sxs-lookup"><span data-stu-id="fbe38-119">For more information see also, [Using Windows Installer with a Terminal Server](using-windows-installer-with-a-terminal-server.md).</span></span>

 

 
