---
description: Les applications peuvent déclarer l’isolement du pilote d’imprimante dans leur manifeste d’application pour isoler l’application du pilote d’imprimante et améliorer la fiabilité des applications.
ms.assetid: 80650C46-AC96-46FD-894A-4F34B056AB79
ms.topic: article
title: 'Comment : utiliser l’isolation d’application'
ms.date: 05/31/2018
ms.openlocfilehash: 28c2a143406e9501662e0ddf7294abfb25e362b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202803"
---
# <a name="how-to-use-application-isolation"></a><span data-ttu-id="3e5ef-103">Comment : utiliser l’isolation d’application</span><span class="sxs-lookup"><span data-stu-id="3e5ef-103">How To: Use Application Isolation</span></span>

<span data-ttu-id="3e5ef-104">Les applications peuvent déclarer l’isolement du pilote d’imprimante dans leur manifeste d’application pour isoler l’application du pilote d’imprimante et améliorer la fiabilité de l’application.</span><span class="sxs-lookup"><span data-stu-id="3e5ef-104">Apps can declare printer-driver isolation in their app manifest to isolate the app from the printer driver and improve the app's reliability.</span></span> <span data-ttu-id="3e5ef-105">Le service d’impression Windows permet aux pilotes d’imprimante de s’exécuter dans des processus distincts du processus dans lequel le spouleur d’impression s’exécute.</span><span class="sxs-lookup"><span data-stu-id="3e5ef-105">The Windows print service allows printer drivers to run in processes that are separate from the process in which the print spooler runs.</span></span> <span data-ttu-id="3e5ef-106">À l’aide de cette fonctionnalité, votre application l’empêche de se bloquer en cas d’erreur du pilote d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="3e5ef-106">Using this feature your app prevents it from crashing in the event the printer driver has an error.</span></span>

<span data-ttu-id="3e5ef-107">L’isolation du pilote d’imprimante est implémentée dans Windows 7 et Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="3e5ef-107">Printer-driver isolation is implemented in Windows 7 and Windows Server 2008 R2.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="3e5ef-108">Prérequis</span><span class="sxs-lookup"><span data-stu-id="3e5ef-108">Prerequisites</span></span>

-   <span data-ttu-id="3e5ef-109">Application de code managé ou Windows Store qui utilise l’impression Windows.</span><span class="sxs-lookup"><span data-stu-id="3e5ef-109">A managed-code or Windows Store app that uses Windows printing.</span></span>

## <a name="instructions"></a><span data-ttu-id="3e5ef-110">Instructions</span><span class="sxs-lookup"><span data-stu-id="3e5ef-110">Instructions</span></span>

### <a name="update-the-app-manifest"></a><span data-ttu-id="3e5ef-111">Mettre à jour le manifeste d’application</span><span class="sxs-lookup"><span data-stu-id="3e5ef-111">Update the app manifest</span></span>

<span data-ttu-id="3e5ef-112">Pour activer l’isolation des pilotes d’imprimantes, vous devez ajouter l’élément **printerDriverIsolation** au manifeste de l’application.</span><span class="sxs-lookup"><span data-stu-id="3e5ef-112">Enabling printer-driver isolation requires you to add the **printerDriverIsolation** element to the app's manifest.</span></span> <span data-ttu-id="3e5ef-113">Voici comment faire :</span><span class="sxs-lookup"><span data-stu-id="3e5ef-113">Here's how:</span></span>

1.  <span data-ttu-id="3e5ef-114">Modifiez le manifeste de l’application, en ajoutant l’élément **printerDriverIsolation** avec la valeur **true** à l’élément **windowsSettings** de l’élément **application** , comme indiqué dans cet exemple.</span><span class="sxs-lookup"><span data-stu-id="3e5ef-114">Edit the app manifest, adding the **printerDriverIsolation** element with a value of **true** to the **windowsSettings** element of the **application** element, as shown in this example.</span></span>
    ```XML
    <application xmlns="urn:schemas-microsoft-com:asm.v3">
        <windowsSettings>
            <printerDriverIsolation xmlns="http://schemas.microsoft.com/SMI/2011/WindowsSettings">true</printerDriverIsolation>
        </windowsSettings>
    </application>
    ```

    

2.  <span data-ttu-id="3e5ef-115">Régénérez votre application.</span><span class="sxs-lookup"><span data-stu-id="3e5ef-115">Rebuild your app.</span></span>

 

 



