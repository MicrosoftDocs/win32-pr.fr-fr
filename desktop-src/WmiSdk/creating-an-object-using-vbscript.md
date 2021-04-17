---
description: Vous pouvez créer un objet pour WMI dans Visual Basic Scripting Edition (VBScript) en vous connectant à WMI, puis en appelant CreateObject. Le tableau suivant répertorie les méthodes de l’API de script pour WMI qui prennent en charge la création d’objets.
ms.assetid: 3acbce31-6d56-4a7a-af03-fa37b2b868be
ms.tgt_platform: multiple
title: Création d’un objet à l’aide de VBScript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6bfbb4753f19f8ed6f7a61d94ab1d9f03b57e091
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485353"
---
# <a name="creating-an-object-using-vbscript"></a><span data-ttu-id="7de73-104">Création d’un objet à l’aide de VBScript</span><span class="sxs-lookup"><span data-stu-id="7de73-104">Creating an Object Using VBScript</span></span>

<span data-ttu-id="7de73-105">Vous pouvez créer un objet pour WMI dans Visual Basic Scripting Edition (VBScript) en vous connectant à WMI, puis en appelant [CreateObject](/previous-versions//xzysf6hc(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7de73-105">You can create an object for WMI in Visual Basic Scripting Edition (VBScript) by connecting to WMI and then calling [CreateObject](/previous-versions//xzysf6hc(v=vs.85)).</span></span> <span data-ttu-id="7de73-106">Le tableau suivant répertorie les méthodes de l’API de script pour WMI qui prennent en charge la création d’objets.</span><span class="sxs-lookup"><span data-stu-id="7de73-106">The following table lists the methods in the Scripting API for WMI that support object creation.</span></span>



| <span data-ttu-id="7de73-107">Interface</span><span class="sxs-lookup"><span data-stu-id="7de73-107">Interface</span></span>                                        | <span data-ttu-id="7de73-108">ProgID</span><span class="sxs-lookup"><span data-stu-id="7de73-108">ProgID</span></span>                             |
|--------------------------------------------------|------------------------------------|
| [<span data-ttu-id="7de73-109">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="7de73-109">**SWbemDateTime**</span></span>](swbemdatetime.md)           | <span data-ttu-id="7de73-110">"WbemScripting.SwbemDateTime"</span><span class="sxs-lookup"><span data-stu-id="7de73-110">"WbemScripting.SwbemDateTime"</span></span>      |
| [<span data-ttu-id="7de73-111">**SWbemLocator**</span><span class="sxs-lookup"><span data-stu-id="7de73-111">**SWbemLocator**</span></span>](swbemlocator.md)             | <span data-ttu-id="7de73-112">« WbemScripting. SWbemLocator »</span><span class="sxs-lookup"><span data-stu-id="7de73-112">"WbemScripting.SWbemLocator"</span></span>       |
| [<span data-ttu-id="7de73-113">**SWbemLastError**</span><span class="sxs-lookup"><span data-stu-id="7de73-113">**SWbemLastError**</span></span>](swbemlasterror.md)         | <span data-ttu-id="7de73-114">« WbemScripting. SWbem. LastError »</span><span class="sxs-lookup"><span data-stu-id="7de73-114">"WbemScripting.SWbem.LastError"</span></span>    |
| [<span data-ttu-id="7de73-115">**SWbemObjectPath**</span><span class="sxs-lookup"><span data-stu-id="7de73-115">**SWbemObjectPath**</span></span>](swbemobjectpath.md)       | <span data-ttu-id="7de73-116">"WbemScripting.SWbemObjectPath"</span><span class="sxs-lookup"><span data-stu-id="7de73-116">"WbemScripting.SWbemObjectPath"</span></span>    |
| [<span data-ttu-id="7de73-117">**SWbemNamedValueSet**</span><span class="sxs-lookup"><span data-stu-id="7de73-117">**SWbemNamedValueSet**</span></span>](swbemnamedvalueset.md) | <span data-ttu-id="7de73-118">"WbemScripting.SWbemNamedValueSet"</span><span class="sxs-lookup"><span data-stu-id="7de73-118">"WbemScripting.SWbemNamedValueSet"</span></span> |
| [<span data-ttu-id="7de73-119">**SWbemRefresher**</span><span class="sxs-lookup"><span data-stu-id="7de73-119">**SWbemRefresher**</span></span>](swbemrefresher.md)         | <span data-ttu-id="7de73-120">"WbemScripting.SWbemRefresher"</span><span class="sxs-lookup"><span data-stu-id="7de73-120">"WbemScripting.SWbemRefresher"</span></span>     |
| [<span data-ttu-id="7de73-121">**SWbemSink**</span><span class="sxs-lookup"><span data-stu-id="7de73-121">**SWbemSink**</span></span>](swbemsink.md)                   | <span data-ttu-id="7de73-122">"WbemScripting.SWbemSink"</span><span class="sxs-lookup"><span data-stu-id="7de73-122">"WbemScripting.SWbemSink"</span></span>          |



 

<span data-ttu-id="7de73-123">La procédure suivante décrit comment créer un objet WMI à l’aide de VBScript.</span><span class="sxs-lookup"><span data-stu-id="7de73-123">The following procedure describes how to create a WMI object using VBScript.</span></span>

<span data-ttu-id="7de73-124">**Pour créer un objet WMI à l’aide de VBScript**</span><span class="sxs-lookup"><span data-stu-id="7de73-124">**To create a WMI object using VBScript**</span></span>

1.  <span data-ttu-id="7de73-125">Connectez-vous à WMI à l’aide d’un moniker ou d’un objet [**SWbemLocator**](swbemlocator.md) .</span><span class="sxs-lookup"><span data-stu-id="7de73-125">Connect to WMI using either a moniker or an [**SWbemLocator**](swbemlocator.md) object.</span></span>

    <span data-ttu-id="7de73-126">Pour plus d’informations, consultez [création d’un script WMI](creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="7de73-126">For more information, see [Creating a WMI Script](creating-a-wmi-script.md).</span></span>

2.  <span data-ttu-id="7de73-127">Effectuez un appel à la méthode VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="7de73-127">Make a call to the VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) method.</span></span>

    <span data-ttu-id="7de73-128">L’exemple de code suivant montre comment créer un objet.</span><span class="sxs-lookup"><span data-stu-id="7de73-128">The following code example shows how to create an object.</span></span>

    ```VB
    Set locator = CreateObject("WbemScripting.SWbemLocator")
    ```

    

    <span data-ttu-id="7de73-129">Si vous utilisez un moniker à l’étape 1, vous n’avez pas besoin d’appeler [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) à nouveau.</span><span class="sxs-lookup"><span data-stu-id="7de73-129">If you use a moniker in Step 1, you do not need to call [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) again.</span></span>

 

 
