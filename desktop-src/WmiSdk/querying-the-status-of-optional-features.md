---
description: Dans Windows 7, WMI implémentait la \_ classe Win32 OptionalFeature. Cette classe récupère l’état des fonctionnalités facultatives présentes sur un ordinateur.
ms.assetid: d756b0c0-b9f4-4b71-9f07-963a0dd5e585
ms.tgt_platform: multiple
title: Interrogation de l’état des fonctionnalités facultatives
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c190b2a2143dae1e22c30b3e5e803908bcb4116
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755333"
---
# <a name="querying-the-status-of-optional-features"></a><span data-ttu-id="5ada0-104">Interrogation de l’état des fonctionnalités facultatives</span><span class="sxs-lookup"><span data-stu-id="5ada0-104">Querying the Status of Optional Features</span></span>

<span data-ttu-id="5ada0-105">Dans Windows 7, WMI implémentait la classe [**Win32 \_ OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) .</span><span class="sxs-lookup"><span data-stu-id="5ada0-105">In Windows 7, WMI implemented the [**Win32\_OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) class.</span></span> <span data-ttu-id="5ada0-106">Cette classe récupère l’état des fonctionnalités facultatives présentes sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="5ada0-106">This class retrieves the status of the optional features that are present on a computer.</span></span>

<span data-ttu-id="5ada0-107">Vous pouvez utiliser les applets de commande Windows PowerShell pour interroger l’état des fonctionnalités facultatives.</span><span class="sxs-lookup"><span data-stu-id="5ada0-107">You can use Windows PowerShell cmdlets to query the status of optional features.</span></span> <span data-ttu-id="5ada0-108">Tous les exemples de cette rubrique utilisent l’applet de commande Get-WmiObject.</span><span class="sxs-lookup"><span data-stu-id="5ada0-108">All of the examples in this topic use the Get-WmiObject cmdlet.</span></span> <span data-ttu-id="5ada0-109">Pour plus d’informations, consultez la rubrique [obtenir-WmiObject](/previous-versions//dd315295(v=technet.10)).</span><span class="sxs-lookup"><span data-stu-id="5ada0-109">For more information, see [Get-WmiObject](/previous-versions//dd315295(v=technet.10)).</span></span>

<span data-ttu-id="5ada0-110">**Pour récupérer toutes les instances de fonctionnalités facultatives présentes sur un ordinateur**</span><span class="sxs-lookup"><span data-stu-id="5ada0-110">**To retrieve all instances of optional features present on a computer**</span></span>

-   <span codelanguage="PowerShell"></span>
    <table>
    <colgroup>
    <col style="width: 100%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="5ada0-111">PowerShell</span><span class="sxs-lookup"><span data-stu-id="5ada0-111">PowerShell</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><pre><code>Get-WmiObject Win32_OptionalFeature</code></pre></td>
    </tr>
    </tbody>
    </table>

    

<span data-ttu-id="5ada0-112">**Pour rechercher une fonctionnalité facultative en spécifiant le nom de la fonctionnalité**</span><span class="sxs-lookup"><span data-stu-id="5ada0-112">**To query for an optional feature by specifying the feature name**</span></span>

-   <span codelanguage="PowerShell"></span>
    <table>
    <colgroup>
    <col style="width: 100%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="5ada0-113">PowerShell</span><span class="sxs-lookup"><span data-stu-id="5ada0-113">PowerShell</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><pre><code>Get-WmiObject -query &quot;select * from Win32_OptionalFeature where name = &#39;TelnetClient&#39;&quot;</code></pre></td>
    </tr>
    </tbody>
    </table>

    

    > [!Note]  
    > <span data-ttu-id="5ada0-114">La propriété **Name** respecte la casse.</span><span class="sxs-lookup"><span data-stu-id="5ada0-114">The **name** property is case-sensitive.</span></span>

     

<span data-ttu-id="5ada0-115">**Pour rechercher des fonctionnalités facultatives en spécifiant l’état d’installation**</span><span class="sxs-lookup"><span data-stu-id="5ada0-115">**To query for optional features by specifying the install state**</span></span>

-   <span codelanguage="PowerShell"></span>
    <table>
    <colgroup>
    <col style="width: 100%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="5ada0-116">PowerShell</span><span class="sxs-lookup"><span data-stu-id="5ada0-116">PowerShell</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><pre><code>Get-WmiObject -query &quot;select * from win32_optionalfeature where installstate= 1&quot;</code></pre></td>
    </tr>
    </tbody>
    </table>

    

    <span data-ttu-id="5ada0-117">Pour plus d’informations sur les valeurs possibles de la propriété **InstallState** , consultez [**Win32 \_ OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature).</span><span class="sxs-lookup"><span data-stu-id="5ada0-117">For more information about the possible values for the **InstallState** property, see [**Win32\_OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5ada0-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5ada0-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ada0-119">**\_OptionalFeature Win32**</span><span class="sxs-lookup"><span data-stu-id="5ada0-119">**Win32\_OptionalFeature**</span></span>](/windows/desktop/CIMWin32Prov/win32-optionalfeature)
</dt> </dl>

 

 
