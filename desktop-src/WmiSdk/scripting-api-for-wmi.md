---
description: La référence de script WMI contient des définitions pour l’API de script WMI.
ms.assetid: 83fc78fc-929d-4d32-940e-9147543a6324
ms.tgt_platform: multiple
title: API de script pour WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6c43587fd8f40c2524bcabd79fe80e3d00d74b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863798"
---
# <a name="scripting-api-for-wmi"></a><span data-ttu-id="8de91-103">API de script pour WMI</span><span class="sxs-lookup"><span data-stu-id="8de91-103">Scripting API for WMI</span></span>

<span data-ttu-id="8de91-104">La référence de script WMI contient des définitions pour l’API de script WMI.</span><span class="sxs-lookup"><span data-stu-id="8de91-104">The WMI scripting reference contains definitions for the WMI Scripting API.</span></span> <span data-ttu-id="8de91-105">Utilisez cette API si vous écrivez des applications avec Microsoft Visual Basic, Visual Basic pour Applications, Visual Basic Scripting Edition (VBScript) ou tout autre langage de script prenant en charge les technologies Active Scripting.</span><span class="sxs-lookup"><span data-stu-id="8de91-105">Use this API if writing applications with Microsoft Visual Basic, Visual Basic for Applications, Visual Basic Scripting Edition (VBScript), or any other scripting language that supports active scripting technologies.</span></span>

> [!Note]  
> <span data-ttu-id="8de91-106">PowerShell est également disponible pour l’écriture de scripts avec WMI.</span><span class="sxs-lookup"><span data-stu-id="8de91-106">PowerShell is also available for scripting with WMI.</span></span> <span data-ttu-id="8de91-107">L’applet de commande obtient-WMI et les trois accélérateurs de type ( \[ WMI \] , \[ WMIClass \] et \[ WmiSearcher \] ) permettent un accès administratif de base à WMI.</span><span class="sxs-lookup"><span data-stu-id="8de91-107">The Get-WMI cmdlet and the three type accelerators (\[wmi\], \[wmiclass\], and \[wmisearcher\]) enable basic administrative access to WMI.</span></span> <span data-ttu-id="8de91-108">Pour plus d’informations, consultez [écriture de scripts avec Windows PowerShell](https://TechNet.Microsoft.Com/library/bb978526.aspx).</span><span class="sxs-lookup"><span data-stu-id="8de91-108">For more information, see [Scripting with Windows PowerShell](https://TechNet.Microsoft.Com/library/bb978526.aspx).</span></span>

 

<span data-ttu-id="8de91-109">Les objets de script WMI, à l’exception de [**SWbemDateTime**](swbemdatetime.md) , ne sont pas marqués comme sécurisés pour l’écriture de scripts pour les scripts exécutés sur des pages HTML dans Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="8de91-109">WMI scripting objects, except for [**SWbemDateTime**](swbemdatetime.md) are not marked safe for scripting for scripts running on HTML pages in Internet Explorer.</span></span> <span data-ttu-id="8de91-110">Par conséquent, à moins que le niveau de sécurité dans Internet Explorer ne soit abaissé, le script échoue.</span><span class="sxs-lookup"><span data-stu-id="8de91-110">Therefore, unless the security level within Internet Explorer is lowered, the script will fail.</span></span> <span data-ttu-id="8de91-111">**SWbemDateTime** est marqué comme sécurisé pour l’initialisation et l’écriture de scripts.</span><span class="sxs-lookup"><span data-stu-id="8de91-111">**SWbemDateTime** is marked safe for initialization and scripting.</span></span> <span data-ttu-id="8de91-112">Toutefois, utilisez tous les objets de script WMI dans les appels **GetObject** et **CreateObject** sur le code côté serveur dans les pages de Active Server (ASP).</span><span class="sxs-lookup"><span data-stu-id="8de91-112">However, use all WMI scripting objects in **GetObject** and **CreateObject** calls on server-side code in Active Server Pages (ASP).</span></span>

-   [<span data-ttu-id="8de91-113">Modèle objet de l’API de script</span><span class="sxs-lookup"><span data-stu-id="8de91-113">Scripting API Object Model</span></span>](scripting-api-object-model.md)
-   [<span data-ttu-id="8de91-114">Conventions de document pour l’API de script</span><span class="sxs-lookup"><span data-stu-id="8de91-114">Document Conventions for the Scripting API</span></span>](document-conventions-for-the-scripting-api.md)
-   [<span data-ttu-id="8de91-115">Scripts d’objets d’API</span><span class="sxs-lookup"><span data-stu-id="8de91-115">Scripting API Objects</span></span>](scripting-api-objects.md)
-   [<span data-ttu-id="8de91-116">Constantes d’API de script</span><span class="sxs-lookup"><span data-stu-id="8de91-116">Scripting API Constants</span></span>](scripting-api-constants.md)

## <a name="related-topics"></a><span data-ttu-id="8de91-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8de91-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8de91-118">Référence WMI</span><span class="sxs-lookup"><span data-stu-id="8de91-118">WMI Reference</span></span>](wmi-reference.md)
</dt> <dt>

[<span data-ttu-id="8de91-119">Codes de retour WMI</span><span class="sxs-lookup"><span data-stu-id="8de91-119">WMI Return Codes</span></span>](wmi-return-codes.md)
</dt> </dl>

 

 



