---
description: WMI utilise le suivi d’événements (ETW) et les événements peuvent être obtenus par le biais de l’interface utilisateur observateur d’événements ou de l’outil en ligne de commande Wevtutil. Pour plus d’informations, consultez suivi de l’activité WMI.
ms.assetid: 315b8355-03b9-40f9-a6c1-29a49f5a2cd8
ms.tgt_platform: multiple
title: Fichiers journaux WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a51dfe4efbec32e60812980511676f723fd5aee9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106520468"
---
# <a name="wmi-log-files"></a><span data-ttu-id="acc67-104">Fichiers journaux WMI</span><span class="sxs-lookup"><span data-stu-id="acc67-104">WMI Log Files</span></span>

<span data-ttu-id="acc67-105">WMI utilise le [suivi d’événements](/windows/desktop/ETW/event-tracing-portal) (ETW) et les événements peuvent être obtenus par le biais de l’interface utilisateur **Observateur d’événements** ou de l’outil en ligne de commande Wevtutil.</span><span class="sxs-lookup"><span data-stu-id="acc67-105">WMI uses [Event Tracing](/windows/desktop/ETW/event-tracing-portal) (ETW) and events can be obtained through the **Event Viewer** user interface or the Wevtutil command line tool.</span></span> <span data-ttu-id="acc67-106">Pour plus d’informations, consultez suivi de l' [activité WMI](tracing-wmi-activity.md).</span><span class="sxs-lookup"><span data-stu-id="acc67-106">For more information, see [Tracing WMI Activity](tracing-wmi-activity.md).</span></span>

-   [<span data-ttu-id="acc67-107">Suivi des événements au lieu des journaux texte</span><span class="sxs-lookup"><span data-stu-id="acc67-107">Event Tracing Instead of Text Logs</span></span>](#event-tracing-instead-of-text-logs)
-   [<span data-ttu-id="acc67-108">Fichiers journaux WMI</span><span class="sxs-lookup"><span data-stu-id="acc67-108">WMI Log Files</span></span>](#wmi-log-files)
-   [<span data-ttu-id="acc67-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="acc67-109">Related topics</span></span>](#related-topics)

## <a name="event-tracing-instead-of-text-logs"></a><span data-ttu-id="acc67-110">Suivi des événements au lieu des journaux texte</span><span class="sxs-lookup"><span data-stu-id="acc67-110">Event Tracing Instead of Text Logs</span></span>

<span data-ttu-id="acc67-111">L’activité du service WMI est enregistrée dans le fichier WMITracing. log.</span><span class="sxs-lookup"><span data-stu-id="acc67-111">WMI service activity is recorded in the WMITracing.log file.</span></span> <span data-ttu-id="acc67-112">Pour plus d’informations sur l’activation du suivi d’événements WMI et l’accès au fichier WMITracing. log, consultez suivi de l' [activité WMI](tracing-wmi-activity.md).</span><span class="sxs-lookup"><span data-stu-id="acc67-112">For more information about enabling WMI event tracing and accessing the WMITracing.log file, see [Tracing WMI Activity](tracing-wmi-activity.md).</span></span> <span data-ttu-id="acc67-113">Les fournisseurs de Windows Driver Model (WDM) continuent à se connecter au fichier wbemprov. log.</span><span class="sxs-lookup"><span data-stu-id="acc67-113">Windows Driver Model (WDM) providers continue to log in the Wbemprov.log file.</span></span>

## <a name="wmi-log-files"></a><span data-ttu-id="acc67-114">Fichiers journaux WMI</span><span class="sxs-lookup"><span data-stu-id="acc67-114">WMI Log Files</span></span>

<span data-ttu-id="acc67-115">Le service WMI et certains fournisseurs écrivent des fichiers journaux de texte pour enregistrer les événements.</span><span class="sxs-lookup"><span data-stu-id="acc67-115">The WMI service and some providers write text log files to record events.</span></span>

<dl> <dt>

<span data-ttu-id="acc67-116"><span id="WMI_Provider_Log_Files"></span><span id="wmi_provider_log_files"></span><span id="WMI_PROVIDER_LOG_FILES"></span>[Fichiers journaux du fournisseur WMI](wmi-provider-log-files.md)</span><span class="sxs-lookup"><span data-stu-id="acc67-116"><span id="WMI_Provider_Log_Files"></span><span id="wmi_provider_log_files"></span><span id="WMI_PROVIDER_LOG_FILES"></span>[WMI Provider Log Files](wmi-provider-log-files.md)</span></span>
</dt> <dd>

<span data-ttu-id="acc67-117">Les fournisseurs WMI peuvent également conserver les journaux.</span><span class="sxs-lookup"><span data-stu-id="acc67-117">WMI providers also may maintain logs.</span></span> <span data-ttu-id="acc67-118">Les fichiers journaux qui apparaissent sur un système dépendent des fournisseurs installés.</span><span class="sxs-lookup"><span data-stu-id="acc67-118">Which log files appear on a system depends on which providers are installed.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="acc67-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="acc67-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="acc67-120">Référence WMI</span><span class="sxs-lookup"><span data-stu-id="acc67-120">WMI Reference</span></span>](wmi-reference.md)
</dt> <dt>

[<span data-ttu-id="acc67-121">Suivi de l’activité WMI</span><span class="sxs-lookup"><span data-stu-id="acc67-121">Tracing WMI Activity</span></span>](tracing-wmi-activity.md)
</dt> <dt>

[<span data-ttu-id="acc67-122">Journalisation de l’activité WMI</span><span class="sxs-lookup"><span data-stu-id="acc67-122">Logging WMI Activity</span></span>](logging-wmi-activity.md)
</dt> </dl>

 

 
