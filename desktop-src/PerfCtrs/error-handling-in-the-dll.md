---
description: Utilisez la journalisation des événements pour enregistrer les erreurs qui se produisent dans la DLL de performance.
ms.assetid: 61bc4fa1-8185-4e07-a3b5-4bd357f0f75a
title: Gestion des erreurs dans la DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd21f0b9338600012d65aa19801ee57794fac294
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103952012"
---
# <a name="error-handling-in-the-dll"></a><span data-ttu-id="9c256-103">Gestion des erreurs dans la DLL</span><span class="sxs-lookup"><span data-stu-id="9c256-103">Error Handling in the DLL</span></span>

<span data-ttu-id="9c256-104">Utilisez la journalisation des événements pour enregistrer les erreurs qui se produisent dans la DLL de performance.</span><span class="sxs-lookup"><span data-stu-id="9c256-104">Use event logging to record errors that occur in the performance DLL.</span></span> <span data-ttu-id="9c256-105">La journalisation des événements d’erreur facilite la résolution des problèmes liés aux applications qui fournissent des données de performances pendant le développement et après l’installation.</span><span class="sxs-lookup"><span data-stu-id="9c256-105">Logging error events aids in troubleshooting applications that provide performance data during development and after installation.</span></span> <span data-ttu-id="9c256-106">Vous devez limiter la quantité de journalisation des erreurs qui se produit dans la fonction [**CollectPerformanceData**](/windows/win32/api/winperf/nc-winperf-pm_collect_proc) , car la collecte de données peut être fréquente.</span><span class="sxs-lookup"><span data-stu-id="9c256-106">You should limit the amount of error logging that occurs in the [**CollectPerformanceData**](/windows/win32/api/winperf/nc-winperf-pm_collect_proc) function because data collection can be frequent.</span></span>

<span data-ttu-id="9c256-107">Le système enregistre les erreurs suivantes dans le journal des événements en cas de problème avec la fonction [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="9c256-107">The system logs the following errors to the event log if there are problems with the [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) function.</span></span> <span data-ttu-id="9c256-108">Si l’une des erreurs suivantes se produit, le système n’appelle pas à nouveau la DLL de performance.</span><span class="sxs-lookup"><span data-stu-id="9c256-108">If one of the following errors occurs, the system does not call the performance DLL again.</span></span> <span data-ttu-id="9c256-109">Au lieu de cela, la DLL est déchargée.</span><span class="sxs-lookup"><span data-stu-id="9c256-109">Instead, the DLL is unloaded.</span></span>

-   <span data-ttu-id="9c256-110">**PERFLIB \_ OPEN \_ Proc \_ \_ introuvable**: consigné lorsque le nom de la procédure défini dans le Registre est introuvable dans la dll en tant que fonction exportée.</span><span class="sxs-lookup"><span data-stu-id="9c256-110">**PERFLIB\_OPEN\_PROC\_NOT\_FOUND**—Logged when the procedure name defined in the registry could not be found in the DLL as an exported function.</span></span> <span data-ttu-id="9c256-111">Cela se produit généralement lorsque la DLL ou le service n’est pas installé correctement ou que le nom de la fonction a été renommé sans mettre à jour la procédure d’installation.</span><span class="sxs-lookup"><span data-stu-id="9c256-111">This usually occurs when the DLL or the service is not installed correctly or the function name has been renamed without updating the installation procedure.</span></span>
-   <span data-ttu-id="9c256-112">**PERFLIB \_ \_ \_ Échec** de l’ouverture de la procédure : consigné lorsque la procédure ouverte a retourné un état d’erreur autre que erreur de \_ réussite.</span><span class="sxs-lookup"><span data-stu-id="9c256-112">**PERFLIB\_OPEN\_PROC\_FAILURE**—Logged when the open procedure returned an error status other than ERROR\_SUCCESS.</span></span> <span data-ttu-id="9c256-113">Si cela se produit, la DLL doit également avoir entré une entrée du journal des événements décrivant les conditions qui ont provoqué l’échec.</span><span class="sxs-lookup"><span data-stu-id="9c256-113">Should this happen, the DLL should have also entered an event log entry describing the conditions that caused the failure.</span></span>
-   <span data-ttu-id="9c256-114">**PERFLIB \_ \_ \_ Exception Open proc**: consigné lorsque la procédure Open rencontre une exception non gérée.</span><span class="sxs-lookup"><span data-stu-id="9c256-114">**PERFLIB\_OPEN\_PROC\_EXCEPTION**—Logged when the open procedure encounters an unhandled exception.</span></span> <span data-ttu-id="9c256-115">Cela est généralement dû à une condition d’erreur inattendue rencontrée par la procédure Open.</span><span class="sxs-lookup"><span data-stu-id="9c256-115">This is usually due to an unexpected error condition encountered by the open procedure.</span></span>

 

 
