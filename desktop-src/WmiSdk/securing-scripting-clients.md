---
description: Les scripts et les applications de Visual Basic doivent définir la sécurité DCOM, en particulier pour l’accès à distance, et peuvent également avoir besoin d’activer des privilèges.
ms.assetid: 4816914d-a1cf-47d8-af20-2b22c53042d6
ms.tgt_platform: multiple
title: Sécurisation des clients de script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c58a3dbade78b1dd81b0bf89eb867d8cd5c2f265
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202166"
---
# <a name="securing-scripting-clients"></a><span data-ttu-id="e8dbd-103">Sécurisation des clients de script</span><span class="sxs-lookup"><span data-stu-id="e8dbd-103">Securing Scripting Clients</span></span>

<span data-ttu-id="e8dbd-104">Les scripts et les applications de Visual Basic doivent définir la sécurité DCOM, en particulier pour l’accès à distance, et peuvent également avoir besoin d’activer des privilèges.</span><span class="sxs-lookup"><span data-stu-id="e8dbd-104">Scripts and Visual Basic applications must set DCOM security, especially for remote access, and may also need to enable privileges.</span></span>

## <a name="default-access-permissions"></a><span data-ttu-id="e8dbd-105">Autorisations d’accès par défaut</span><span class="sxs-lookup"><span data-stu-id="e8dbd-105">Default Access Permissions</span></span>

<span data-ttu-id="e8dbd-106">L’accès WMI diffère entre les ordinateurs locaux et distants.</span><span class="sxs-lookup"><span data-stu-id="e8dbd-106">WMI access differs between local and remote computers.</span></span> <span data-ttu-id="e8dbd-107">Pour plus d’informations, consultez [connexion à WMI sur un ordinateur distant](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="e8dbd-107">For more information, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>

<span data-ttu-id="e8dbd-108">Voici les autorisations d’accès par défaut par compte :</span><span class="sxs-lookup"><span data-stu-id="e8dbd-108">The following are the default access permissions by account:</span></span>

-   <span data-ttu-id="e8dbd-109">Tout le monde, LocalService, NetworkService</span><span class="sxs-lookup"><span data-stu-id="e8dbd-109">Everyone, LocalService, NetworkService</span></span>

    <span data-ttu-id="e8dbd-110">Autorisation de lire ou d’écrire des données et d’exécuter des [*méthodes de fournisseur*](gloss-p.md) sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="e8dbd-110">Permission to read or write data and to run [*provider methods*](gloss-p.md) on the local computer.</span></span> <span data-ttu-id="e8dbd-111">Ces comptes ne peuvent pas créer de nouvelles classes ou installer de nouveaux fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="e8dbd-111">These accounts cannot create new classes or install new providers.</span></span>

-   <span data-ttu-id="e8dbd-112">Comptes d'administrateur</span><span class="sxs-lookup"><span data-stu-id="e8dbd-112">Administrator accounts</span></span>

    <span data-ttu-id="e8dbd-113">Contrôle total sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="e8dbd-113">Full control on local computer.</span></span> <span data-ttu-id="e8dbd-114">Lors de la connexion à un ordinateur distant, le compte doit également être un administrateur local sur l’ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="e8dbd-114">When connecting to a remote computer, the account must be a local administrator on the remote computer also.</span></span>

## <a name="securing-a-scripting-client"></a><span data-ttu-id="e8dbd-115">Sécurisation d’un client de script</span><span class="sxs-lookup"><span data-stu-id="e8dbd-115">Securing a Scripting Client</span></span>

<span data-ttu-id="e8dbd-116">Les applications de script et de Visual Basic WMI doivent définir les niveaux de sécurité DCOM de manière appropriée pour les systèmes d’exploitation ciblés.</span><span class="sxs-lookup"><span data-stu-id="e8dbd-116">WMI scripting and Visual Basic applications must set DCOM security levels appropriately for the operating systems they are targeting.</span></span> <span data-ttu-id="e8dbd-117">Pour plus d’informations, consultez [définition du niveau de sécurité de processus par défaut à l’aide de VBScript](setting-the-default-process-security-level-using-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="e8dbd-117">For more information, see [Setting the Default Process Security Level Using VBScript](setting-the-default-process-security-level-using-vbscript.md).</span></span>

<span data-ttu-id="e8dbd-118">Lorsque vous vous connectez à un ordinateur distant, vous devrez peut-être modifier le service (NTLM ou Kerberos) qui gère l’authentification.</span><span class="sxs-lookup"><span data-stu-id="e8dbd-118">When connecting to a remote computer, you may need to change the service (NTLM or Kerberos) that handles authentication.</span></span> <span data-ttu-id="e8dbd-119">Pour plus d’informations, consultez [définition du service d’authentification à l’aide de VBScript](setting-the-authentication-service-using-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="e8dbd-119">For more information, see [Setting the Authentication Service Using VBScript](setting-the-authentication-service-using-vbscript.md).</span></span>

<span data-ttu-id="e8dbd-120">L’accès à certaines classes ou données WMI peut nécessiter un privilège qui n’est pas activé.</span><span class="sxs-lookup"><span data-stu-id="e8dbd-120">Access to some WMI classes or data may require a privilege that is not enabled.</span></span> <span data-ttu-id="e8dbd-121">Par exemple, vous devez inclure le privilège de sécurité lors de la connexion à la classe [**Win32 \_ NTEventlogFile**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="e8dbd-121">For example, you must include the Security privilege when connecting to the [**Win32\_NTEventlogFile**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)) class.</span></span> <span data-ttu-id="e8dbd-122">Pour plus d’informations, consultez [exécution d’opérations privilégiées à l’aide de VBScript](executing-privileged-operations-using-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="e8dbd-122">For more information, see [Executing Privileged Operations Using VBScript](executing-privileged-operations-using-vbscript.md).</span></span>

<span data-ttu-id="e8dbd-123">Si vous accédez à WMI à partir d’une page de Active Server (ASP), une configuration IIS est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="e8dbd-123">If you are accessing WMI from an Active Server Page (ASP), then some IIS configuration is required.</span></span> <span data-ttu-id="e8dbd-124">Pour plus d’informations, consultez [configuration d’IIS 5,0 et versions ultérieures pour les scripts ASP WMI](configuring-iis-5-for-wmi-asp-scripting.md).</span><span class="sxs-lookup"><span data-stu-id="e8dbd-124">For more information, see [Configuring IIS 5.0 and Later for WMI ASP Scripting](configuring-iis-5-for-wmi-asp-scripting.md).</span></span>

<span data-ttu-id="e8dbd-125">Vous essayez peut-être de vous connecter à un espace de noms qui nécessite une connexion chiffrée, en d’autres termes, qui requiert un niveau d’authentification de pktPrivacy.</span><span class="sxs-lookup"><span data-stu-id="e8dbd-125">You may be trying to connect to a namespace which requires an encrypted connection, in other words, one that requires an authentication level of pktPrivacy.</span></span> <span data-ttu-id="e8dbd-126">Pour plus d’informations, consultez [définition du niveau de sécurité de processus par défaut à l’aide de VBScript](setting-the-default-process-security-level-using-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="e8dbd-126">For more information, see [Setting the Default Process Security Level Using VBScript](setting-the-default-process-security-level-using-vbscript.md).</span></span>

 

 
