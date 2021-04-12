---
description: Installez un package de Windows Installer avec des privilèges élevés (système).
ms.assetid: 0bbec06a-0a2b-430a-a361-317a319da615
title: AlwaysInstallElevated a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c07e705e3e46a28049b6fb85eda96930d645a867
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528876"
---
# <a name="alwaysinstallelevated"></a><span data-ttu-id="8ef28-103">AlwaysInstallElevated a</span><span class="sxs-lookup"><span data-stu-id="8ef28-103">AlwaysInstallElevated</span></span>

<span data-ttu-id="8ef28-104">Vous pouvez utiliser la stratégie AlwaysInstallElevated a pour installer un package Windows Installer avec des privilèges élevés (système).</span><span class="sxs-lookup"><span data-stu-id="8ef28-104">You can use the AlwaysInstallElevated policy to install a Windows Installer package with elevated (system) privileges.</span></span>

<span data-ttu-id="8ef28-105">\* \* AVERTISSEMENT : \* \*</span><span class="sxs-lookup"><span data-stu-id="8ef28-105">\*\*Warning:  \*\*</span></span>

<span data-ttu-id="8ef28-106">Cette option équivaut à accorder des droits d’administration complets, ce qui peut poser un risque de sécurité massif.</span><span class="sxs-lookup"><span data-stu-id="8ef28-106">This option is equivalent to granting full administrative rights, which can pose a massive security risk.</span></span> <span data-ttu-id="8ef28-107">Microsoft déconseille fortement l’utilisation de ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="8ef28-107">Microsoft strongly discourages the use of this setting.</span></span>

<span data-ttu-id="8ef28-108">Pour installer un package avec des privilèges élevés (système), définissez la valeur AlwaysInstallElevated a sur « 1 » sous les deux clés de Registre suivantes :</span><span class="sxs-lookup"><span data-stu-id="8ef28-108">To install a package with elevated (system) privileges, set the AlwaysInstallElevated value to "1" under both of the following registry keys:</span></span>

<span data-ttu-id="8ef28-109">**HKEY \_ \_** \\ **Stratégies logicielles** de l’utilisateur actuel \\  \\ **Microsoft** \\ **Windows** \\ **installer**</span><span class="sxs-lookup"><span data-stu-id="8ef28-109">**HKEY\_CURRENT\_USER**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

<span data-ttu-id="8ef28-110">**HKEY \_ \_** \\ **Stratégies logicielles** de l’ordinateur local \\  \\ **Microsoft** \\ **Windows** \\ **installer**</span><span class="sxs-lookup"><span data-stu-id="8ef28-110">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

<span data-ttu-id="8ef28-111">Si la valeur AlwaysInstallElevated a n’est pas définie sur « 1 » sous les deux clés de Registre précédentes, le programme d’installation utilise des privilèges élevés pour installer les applications managées et utilise le niveau de privilège de l’utilisateur actuel pour les applications non gérées.</span><span class="sxs-lookup"><span data-stu-id="8ef28-111">If the AlwaysInstallElevated value is not set to "1" under both of the preceding registry keys, the installer uses elevated privileges to install managed applications and uses the current user's privilege level for unmanaged applications.</span></span>

<span data-ttu-id="8ef28-112">Étant donné que cette stratégie permet aux utilisateurs d’installer des applications qui requièrent l’accès aux répertoires et aux clés de Registre pour lesquels l’utilisateur n’a pas l’autorisation d’afficher ou de modifier, vous devez déterminer s’il fournit à vos utilisateurs un niveau de sécurité approprié.</span><span class="sxs-lookup"><span data-stu-id="8ef28-112">Because this policy permits users to install applications that require access to directories and registry keys for which the user may not have permission to view or change, you should consider whether it provides your users with an appropriate level of security.</span></span> <span data-ttu-id="8ef28-113">La définition de cette stratégie indique à Windows Installer d’utiliser des autorisations système lors de l’installation de l’application sur le système.</span><span class="sxs-lookup"><span data-stu-id="8ef28-113">Setting this policy directs Windows Installer to use system permissions when it installs the application on the system.</span></span> <span data-ttu-id="8ef28-114">Si cette stratégie n’est pas définie, les applications non distribuées par l’administrateur sont installées à l’aide des privilèges de l’utilisateur et seules les applications gérées obtiennent des privilèges élevés.</span><span class="sxs-lookup"><span data-stu-id="8ef28-114">If this policy is not set, applications not distributed by the administrator are installed using the user's privileges and only managed applications get elevated privileges.</span></span>

<span data-ttu-id="8ef28-115">Notez qu’une fois que la stratégie par ordinateur pour AlwaysInstallElevated a est activée, tout utilisateur peut définir son paramètre par utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8ef28-115">Note that once the per-machine policy for AlwaysInstallElevated is enabled, any user can set their per-user setting.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ef28-116">Notes</span><span class="sxs-lookup"><span data-stu-id="8ef28-116">Remarks</span></span>

<span data-ttu-id="8ef28-117">Pour plus d’informations sur l’interaction de cette stratégie avec les sources d’installation, consultez [gestion des sources d’installation](managing-installation-sources.md).</span><span class="sxs-lookup"><span data-stu-id="8ef28-117">For information about the interaction of this policy with installation sources, see [Managing Installation Sources](managing-installation-sources.md).</span></span>

## <a name="data-type"></a><span data-ttu-id="8ef28-118">Type de données</span><span class="sxs-lookup"><span data-stu-id="8ef28-118">Data Type</span></span>

<span data-ttu-id="8ef28-119">**\_valeur DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="8ef28-119">**REG\_DWORD**</span></span>

 

 



