---
description: Le moniteur d’événements de mise hors tension permet à l’utilisateur ou à l’application de documenter la raison de l’arrêt ou du redémarrage du système.
ms.assetid: 860c014e-1fde-45d1-b366-c279bfcf4079
title: Moniteur d’événements de mise hors tension
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4208914149bb84df34e67cca71b40cde66363211
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319258"
---
# <a name="shutdown-event-tracker"></a><span data-ttu-id="10f39-103">Moniteur d’événements de mise hors tension</span><span class="sxs-lookup"><span data-stu-id="10f39-103">Shutdown Event Tracker</span></span>

<span data-ttu-id="10f39-104">Le *moniteur d’événements de mise hors tension* permet à l’utilisateur ou à l’application de documenter la raison de l’arrêt ou du redémarrage du système.</span><span class="sxs-lookup"><span data-stu-id="10f39-104">The *Shutdown Event Tracker* enables the user or application to document the reason for shutting down or restarting the system.</span></span> <span data-ttu-id="10f39-105">L’utilisateur est invité à renseigner les informations lors de la sélection de l’option **arrêter** dans le menu **Démarrer** , ou lors de l’utilisation de Shutdown.exe.</span><span class="sxs-lookup"><span data-stu-id="10f39-105">The user is prompted to fill in information when selecting **Shut Down** from the **Start** menu, or when using Shutdown.exe.</span></span> <span data-ttu-id="10f39-106">Les développeurs peuvent inclure un code de raison lors de l’appel des fonctions [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) et [**InitiateSystemShutdownEx**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa) .</span><span class="sxs-lookup"><span data-stu-id="10f39-106">Developers can include a reason code when calling the [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) and [**InitiateSystemShutdownEx**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa) functions.</span></span> <span data-ttu-id="10f39-107">Les informations sont stockées dans le journal des événements.</span><span class="sxs-lookup"><span data-stu-id="10f39-107">The information is stored in the event log.</span></span>

<span data-ttu-id="10f39-108">**Windows XP :** Si cette fonctionnalité est activée par défaut à partir de Windows Server 2003, vous devez l’activer sur Windows XP.</span><span class="sxs-lookup"><span data-stu-id="10f39-108">**Windows XP:** While this feature is enabled by default starting with Windows Server 2003, you must enable it on Windows XP.</span></span> <span data-ttu-id="10f39-109">Pour plus d’informations, consultez la documentation du moniteur d’événements de mise hors tension inclus dans le système ou sur TechNet.</span><span class="sxs-lookup"><span data-stu-id="10f39-109">For more information, see the documentation for the Shutdown Event Tracker included in the system or on TechNet.</span></span>

<span data-ttu-id="10f39-110">Les fonctions [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) et [**InitiateSystemShutdownEx**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa) ont été mises à jour pour prendre en charge les codes de raison de l’arrêt dans le paramètre *dwReason* .</span><span class="sxs-lookup"><span data-stu-id="10f39-110">The [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) and [**InitiateSystemShutdownEx**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa) functions have been updated to support shutdown reason codes in the *dwReason* parameter.</span></span> <span data-ttu-id="10f39-111">Utilisez les valeurs définies dans Reason. h pour construire un code de raison d’arrêt ou définir un code de raison personnalisé.</span><span class="sxs-lookup"><span data-stu-id="10f39-111">Use the values defined in Reason.h to construct a shutdown reason code, or define a custom reason code.</span></span> <span data-ttu-id="10f39-112">Un code de raison d’arrêt est construit à partir d’un indicateur majeur, d’un drapeau mineur et de deux indicateurs facultatifs.</span><span class="sxs-lookup"><span data-stu-id="10f39-112">A shutdown reason code is constructed from a major flag, a minor flag, and two optional flags.</span></span> <span data-ttu-id="10f39-113">Pour plus d’informations, consultez codes de raison de l' [arrêt du système](system-shutdown-reason-codes.md).</span><span class="sxs-lookup"><span data-stu-id="10f39-113">For more information, see [System Shutdown Reason Codes](system-shutdown-reason-codes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="10f39-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="10f39-114">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="10f39-115">[Moniteur d’événements de mise hors tension (TechNet)](/previous-versions/windows/it-pro/windows-server-2003/cc783475(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="10f39-115">[Shutdown Event Tracker (TechNet)](/previous-versions/windows/it-pro/windows-server-2003/cc783475(v=ws.10))</span></span>
</dt> </dl>

 

 
