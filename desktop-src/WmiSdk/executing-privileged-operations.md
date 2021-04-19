---
description: Les opérations privilégiées requièrent des privilèges de sécurité tels que SeLoadDriverPrivilege (wbemPrivilegeLoadDriver dans les constantes de l’API de script), un privilège qui doit être activé pour un compte qui charge un pilote de périphérique.
ms.assetid: 11bb8723-f329-4083-8219-2256ce44a5e3
ms.tgt_platform: multiple
title: Exécution des opérations privilégiées
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 37abba9d774025825611e311f08414b50e660f65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106521506"
---
# <a name="executing-privileged-operations"></a><span data-ttu-id="f49a3-103">Exécution des opérations privilégiées</span><span class="sxs-lookup"><span data-stu-id="f49a3-103">Executing Privileged Operations</span></span>

<span data-ttu-id="f49a3-104">Les opérations privilégiées requièrent des privilèges de sécurité tels que **SeLoadDriverPrivilege** (**WbemPrivilegeLoadDriver** dans les [constantes](scripting-api-constants.md)de l’API de script), un privilège qui doit être activé pour un compte qui charge un pilote de périphérique.</span><span class="sxs-lookup"><span data-stu-id="f49a3-104">Privileged operations require security privileges such as **SeLoadDriverPrivilege** (**wbemPrivilegeLoadDriver** in the [Scripting API Constants](scripting-api-constants.md)), a privilege that must be enabled for an account that is loading a device driver.</span></span> <span data-ttu-id="f49a3-105">Vous ne pouvez pas ajouter de privilèges à un administrateur ou à un utilisateur par le biais de WMI. vous pouvez uniquement activer les privilèges que le compte possède déjà.</span><span class="sxs-lookup"><span data-stu-id="f49a3-105">You cannot add privileges to an administrator or user through WMI, you can only enable privileges that the account already has.</span></span> <span data-ttu-id="f49a3-106">Pour obtenir la liste des privilèges, [**consultez \_ constantes de privilège**](privilege-constants.md).</span><span class="sxs-lookup"><span data-stu-id="f49a3-106">For a list of privileges, see [**Privilege\_Constants**](privilege-constants.md).</span></span>

<span data-ttu-id="f49a3-107">Par défaut, un utilisateur local sur un ordinateur peut lire des données statiques à partir de l' [*espace de stockage WMI*](gloss-w.md), écrire dans des instances fournies par des fournisseurs et exécuter des méthodes de fournisseur, sauf si le fournisseur applique des exigences de sécurité spécifiques.</span><span class="sxs-lookup"><span data-stu-id="f49a3-107">By default, a local user on a computer can read static data from the [*WMI repository*](gloss-w.md), write to instances supplied by providers, and execute provider methods, unless the provider enforces special security requirements of its own.</span></span> <span data-ttu-id="f49a3-108">Seuls les administrateurs peuvent [se connecter à un ordinateur distant](connecting-to-wmi-on-a-remote-computer.md), modifier les descripteurs de sécurité ou modifier les données de référentiel WMI statiques, telles qu’une définition de classe WMI.</span><span class="sxs-lookup"><span data-stu-id="f49a3-108">Only administrators can [connect to a remote computer](connecting-to-wmi-on-a-remote-computer.md), change security descriptors, or change static WMI repository data, such as a WMI class definition.</span></span> <span data-ttu-id="f49a3-109">Tous les privilèges sont activés pour une connexion à distance.</span><span class="sxs-lookup"><span data-stu-id="f49a3-109">All privileges are enabled for a remote connection.</span></span> <span data-ttu-id="f49a3-110">Pour plus d’informations, consultez [sécurisation d’une connexion WMI à distance](securing-a-remote-wmi-connection.md).</span><span class="sxs-lookup"><span data-stu-id="f49a3-110">For more information, see [Securing a Remote WMI Connection](securing-a-remote-wmi-connection.md).</span></span>

<span data-ttu-id="f49a3-111">Les constantes de privilège pour C++ diffèrent de celles utilisées par les langages Automation tels que Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="f49a3-111">The privilege constants for C++ differ from those that are used by automation languages such as Visual Basic.</span></span> <span data-ttu-id="f49a3-112">Les scripts doivent utiliser la valeur de la constante plutôt que le nom.</span><span class="sxs-lookup"><span data-stu-id="f49a3-112">Scripts must use the value of the constant rather than the name.</span></span> <span data-ttu-id="f49a3-113">Pour plus d’informations, consultez [exécution d’opérations privilégiées à l’aide de C++](executing-privileged-operations-using-c-.md) ou exécution d' [opérations privilégiées à l’aide de VBScript](executing-privileged-operations-using-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="f49a3-113">For more information, see [Executing Privileged Operations Using C++](executing-privileged-operations-using-c-.md) or [Executing Privileged Operations Using VBScript](executing-privileged-operations-using-vbscript.md).</span></span>

<span data-ttu-id="f49a3-114">La cause courante des erreurs de refus d’accès lors de l’utilisation de WMI est l’absence de privilège activé pour les opérations, comme l’obtention de toutes les instances de [**Win32 \_ NTEventlogFile**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f49a3-114">A common cause of access denied errors when using WMI is the lack of an enabled privilege for operations, such as getting all instances of [**Win32\_NTEventlogFile**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)).</span></span> <span data-ttu-id="f49a3-115">Si vous n’activez pas le privilège de **sécurité** , vous ne pouvez pas accéder au fichier journal de sécurité.</span><span class="sxs-lookup"><span data-stu-id="f49a3-115">Without enabling the **SeSecurity** privilege, you cannot access the Security log file.</span></span>

<span data-ttu-id="f49a3-116">L’exemple de code VBScript suivant montre comment définir le privilège **sesecurity** dans la chaîne de moniker.</span><span class="sxs-lookup"><span data-stu-id="f49a3-116">The following VBScript code example shows how to set the **SeSecurity** privilege in the moniker string.</span></span> <span data-ttu-id="f49a3-117">En cas d’utilisation dans le moniker, le nom de privilège entre parenthèses supprime le « se » initial.</span><span class="sxs-lookup"><span data-stu-id="f49a3-117">When used in the moniker, the privilege name in parentheses drops the initial "Se".</span></span> <span data-ttu-id="f49a3-118">Pour plus d’informations, consultez [construction d’une chaîne de moniker](constructing-a-moniker-string.md).</span><span class="sxs-lookup"><span data-stu-id="f49a3-118">For more information, see [Constructing a Moniker String](constructing-a-moniker-string.md).</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate,(Security)}!\\" _
    & strComputer & "\root\cimv2")
Set colFiles = objWMIService.ExecQuery _
    ("Select * from Win32_NTEventLogFile " _
    & "Where LogFileName='Security'")
For Each LogFile in colFiles
Wscript.Echo LogFile.NumberOfRecords
Next
```



## <a name="related-topics"></a><span data-ttu-id="f49a3-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f49a3-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f49a3-120">**Constantes de privilège**</span><span class="sxs-lookup"><span data-stu-id="f49a3-120">**Privilege Constants**</span></span>](privilege-constants.md)
</dt> </dl>

 

 
