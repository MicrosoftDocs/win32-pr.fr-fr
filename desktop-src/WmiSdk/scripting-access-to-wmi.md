---
description: Les scripts peuvent accéder à toutes les classes WMI pour les objets matériels et logiciels.
ms.assetid: dbb29bc8-a675-4538-99f4-00613c83eeaa
ms.tgt_platform: multiple
title: Écriture de scripts pour l’accès à WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd487c127c670f9ddee9596e44c4b2b9691ed880
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202173"
---
# <a name="scripting-access-to-wmi"></a><span data-ttu-id="0b4a6-103">Écriture de scripts pour l’accès à WMI</span><span class="sxs-lookup"><span data-stu-id="0b4a6-103">Scripting Access to WMI</span></span>

<span data-ttu-id="0b4a6-104">Les scripts peuvent accéder à toutes les classes WMI pour les objets matériels et logiciels.</span><span class="sxs-lookup"><span data-stu-id="0b4a6-104">Scripts can access all WMI classes for hardware and software objects.</span></span> <span data-ttu-id="0b4a6-105">Les scripts Windows Script Host (WSH) peuvent effectuer des opérations sur les objets du système de fichiers, manipuler des imprimantes réseau ou modifier les variables d’environnement.</span><span class="sxs-lookup"><span data-stu-id="0b4a6-105">Windows Script Host (WSH) scripts can perform operations on file system objects, manipulate network printers, or change environment variables.</span></span> <span data-ttu-id="0b4a6-106">Vous pouvez trouver une variété de tâches d’administration et des conseils sur la façon de les accomplir dans WMI à l’aide [des tâches WMI pour les scripts et les applications](wmi-tasks-for-scripts-and-applications.md).</span><span class="sxs-lookup"><span data-stu-id="0b4a6-106">You can find a variety of administrator tasks and brief guidance on how to accomplish them in WMI at [WMI Tasks for Scripts and Applications](wmi-tasks-for-scripts-and-applications.md).</span></span> <span data-ttu-id="0b4a6-107">Pour plus d’informations et d’exemples, consultez le [référentiel de scripts](https://www.microsoft.com/technet/scriptcenter/scripts/default.mspx)technet scriptcenter.</span><span class="sxs-lookup"><span data-stu-id="0b4a6-107">For more information and examples, see the TechNet ScriptCenter [Script Repository](https://www.microsoft.com/technet/scriptcenter/scripts/default.mspx).</span></span>

<span data-ttu-id="0b4a6-108">Si vous débutez avec des scripts ou des scripts spécifiques à WMI, consultez la section TechNet ScriptCenter [prise en main](https://www.microsoft.com/technet/scriptcenter/hubs/start.mspx).</span><span class="sxs-lookup"><span data-stu-id="0b4a6-108">If you are new to scripting or to WMI-specific scripting, see the TechNet ScriptCenter section [Getting Started](https://www.microsoft.com/technet/scriptcenter/hubs/start.mspx).</span></span>

<span data-ttu-id="0b4a6-109">Avec l' [API de script pour WMI](scripting-api-for-wmi.md), vous pouvez développer des scripts rapides, simples ou des applications complexes.</span><span class="sxs-lookup"><span data-stu-id="0b4a6-109">With the [Scripting API for WMI](scripting-api-for-wmi.md), you can develop quick, simple scripts or complex applications.</span></span> <span data-ttu-id="0b4a6-110">Les scripts vous permettent d’obtenir des informations ou de configurer la plupart des objets d’une entreprise, comme vous le feriez par le biais d’une application C++ ou C#.</span><span class="sxs-lookup"><span data-stu-id="0b4a6-110">Scripting gives you the same capability of getting information or of configuring most objects in an enterprise as you would have through a C++ or C# application.</span></span> <span data-ttu-id="0b4a6-111">Pour plus d’informations, consultez [scripts dans WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="0b4a6-111">For more information, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="0b4a6-112">Vous ne pouvez pas écrire de [*fournisseur WMI*](gloss-p.md) dans un script.</span><span class="sxs-lookup"><span data-stu-id="0b4a6-112">You cannot write a [*WMI provider*](gloss-p.md) in script.</span></span> <span data-ttu-id="0b4a6-113">Pour plus d’informations, consultez [fourniture de données à WMI](providing-data-to-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="0b4a6-113">For more information, see [Providing Data to WMI](providing-data-to-wmi.md).</span></span>

<span data-ttu-id="0b4a6-114">Les scripts WMI peuvent être écrits dans n’importe quel langage de script pouvant interagir avec les objets ActiveX.</span><span class="sxs-lookup"><span data-stu-id="0b4a6-114">WMI scripts can be written in any scripting language that can interact with ActiveX objects.</span></span>

<span data-ttu-id="0b4a6-115">Windows PowerShell fournit un environnement simple pour l’administration et l’écriture de scripts WMI.</span><span class="sxs-lookup"><span data-stu-id="0b4a6-115">Windows PowerShell provides a simple environment for WMI administration and scripting.</span></span> <span data-ttu-id="0b4a6-116">Pour plus d’informations sur PowerShell, consultez [prise en main avec Windows PowerShell](/powershell/scripting/getting-started/getting-started-with-windows-powershell?view=powershell-7&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="0b4a6-116">For more information about PowerShell, see [Getting Started with Windows PowerShell](/powershell/scripting/getting-started/getting-started-with-windows-powershell?view=powershell-7&preserve-view=true).</span></span>

<span data-ttu-id="0b4a6-117">Les scripts ADSI (Active Directory Service Interfaces) fournissent l’accès aux objets Active Directory Domain Services (AD DS).</span><span class="sxs-lookup"><span data-stu-id="0b4a6-117">Active Directory Service Interfaces (ADSI) scripts provides access to Active Directory Domain Services (AD DS) objects.</span></span> <span data-ttu-id="0b4a6-118">Les scripts WSH et ADSI accèdent aux objets et autorisent les procédures non disponibles par le biais de fichiers de commandes.</span><span class="sxs-lookup"><span data-stu-id="0b4a6-118">Both WSH and ADSI scripts access objects and allow procedures not available through batch files.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0b4a6-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0b4a6-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0b4a6-120">À propos de WMI</span><span class="sxs-lookup"><span data-stu-id="0b4a6-120">About WMI</span></span>](about-wmi.md)
</dt> <dt>

[<span data-ttu-id="0b4a6-121">API de script pour WMI</span><span class="sxs-lookup"><span data-stu-id="0b4a6-121">Scripting API for WMI</span></span>](scripting-api-for-wmi.md)
</dt> </dl>

 

 
