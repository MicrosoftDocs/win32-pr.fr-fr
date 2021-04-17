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
# <a name="creating-an-object-using-vbscript"></a>Création d’un objet à l’aide de VBScript

Vous pouvez créer un objet pour WMI dans Visual Basic Scripting Edition (VBScript) en vous connectant à WMI, puis en appelant [CreateObject](/previous-versions//xzysf6hc(v=vs.85)). Le tableau suivant répertorie les méthodes de l’API de script pour WMI qui prennent en charge la création d’objets.



| Interface                                        | ProgID                             |
|--------------------------------------------------|------------------------------------|
| [**SWbemDateTime**](swbemdatetime.md)           | "WbemScripting.SwbemDateTime"      |
| [**SWbemLocator**](swbemlocator.md)             | « WbemScripting. SWbemLocator »       |
| [**SWbemLastError**](swbemlasterror.md)         | « WbemScripting. SWbem. LastError »    |
| [**SWbemObjectPath**](swbemobjectpath.md)       | "WbemScripting.SWbemObjectPath"    |
| [**SWbemNamedValueSet**](swbemnamedvalueset.md) | "WbemScripting.SWbemNamedValueSet" |
| [**SWbemRefresher**](swbemrefresher.md)         | "WbemScripting.SWbemRefresher"     |
| [**SWbemSink**](swbemsink.md)                   | "WbemScripting.SWbemSink"          |



 

La procédure suivante décrit comment créer un objet WMI à l’aide de VBScript.

**Pour créer un objet WMI à l’aide de VBScript**

1.  Connectez-vous à WMI à l’aide d’un moniker ou d’un objet [**SWbemLocator**](swbemlocator.md) .

    Pour plus d’informations, consultez [création d’un script WMI](creating-a-wmi-script.md).

2.  Effectuez un appel à la méthode VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) .

    L’exemple de code suivant montre comment créer un objet.

    ```VB
    Set locator = CreateObject("WbemScripting.SWbemLocator")
    ```

    

    Si vous utilisez un moniker à l’étape 1, vous n’avez pas besoin d’appeler [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) à nouveau.

 

 
