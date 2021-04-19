---
description: Démarrage et récupération COM+ CRM
ms.assetid: dee1f2df-dfe0-44c3-830b-871690e513e9
title: Démarrage et récupération COM+ CRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a0e631e2e5ecef1621705c9af74aa48898d733b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514951"
---
# <a name="com-crm-startup-and-recovery"></a><span data-ttu-id="c4f3c-103">Démarrage et récupération COM+ CRM</span><span class="sxs-lookup"><span data-stu-id="c4f3c-103">COM+ CRM Startup and Recovery</span></span>

<span data-ttu-id="c4f3c-104">Si la case à cocher **activer les gestionnaires de ressources de compensation** est activée pour une application serveur (à l’aide de l’outil d’administration Services de composants, sous l’onglet **avancé** de la page de propriétés de l’application com+), la première fois qu’elle démarre, elle crée un fichier journal CRM qui sera utilisé par tous les composants CRM dans ce processus d’application serveur.</span><span class="sxs-lookup"><span data-stu-id="c4f3c-104">If a server application has the **Enable compensating resource managers** checkbox selected (using the Component Services administrative tool, on the **Advanced** tab of the COM+ application's property page), the first time it starts up it creates a CRM log file to be used by all CRMs in that server application process.</span></span> <span data-ttu-id="c4f3c-105">(Pour obtenir des instructions détaillées sur la configuration de CRM, consultez [Configuration des composants CRM de com+](configuring-com--crm-components.md).)</span><span class="sxs-lookup"><span data-stu-id="c4f3c-105">(For detailed instructions about configuring the CRM, see [Configuring COM+ CRM Components](configuring-com--crm-components.md).)</span></span>

<span data-ttu-id="c4f3c-106">Le nom du fichier journal CRM créé pour l’application serveur est basé sur l’AppId (un GUID) de l’application serveur, et le fichier journal CRM est placé dans le même répertoire que le fichier journal DTC (normalement, votre répertoire% SystemRoot% \\ winnt \\ system32 \\ DtcLog).</span><span class="sxs-lookup"><span data-stu-id="c4f3c-106">The name of the CRM log file created for the server application is based on the AppId (a GUID) of the server application, and the CRM log file is placed in the same directory as the DTC log file (normally your %SystemRoot%\\winnt\\system32\\DtcLog directory).</span></span> <span data-ttu-id="c4f3c-107">Les fichiers journaux CRM portent l’extension. crmlog.</span><span class="sxs-lookup"><span data-stu-id="c4f3c-107">CRM log files have the extension .crmlog.</span></span>

> [!Note]  
> <span data-ttu-id="c4f3c-108">Il peut être nécessaire de modifier l’emplacement par défaut d’un fichier journal CRM pour des raisons de performances (pour que le fichier journal DTC soit situé sur un disque différent de celui du fichier journal CRM) ou peut-être en raison de l’utilisation du CRM dans un environnement de cluster.</span><span class="sxs-lookup"><span data-stu-id="c4f3c-108">It may be necessary to change the default location of a CRM log file due to performance reasons (to have the DTC log file on a different disk than the CRM log file) or perhaps due to use of the CRM in a cluster environment.</span></span> <span data-ttu-id="c4f3c-109">L’emplacement des fichiers journaux CRM peut être modifié à l’aide du kit de développement logiciel (SDK) d’administration COM+.</span><span class="sxs-lookup"><span data-stu-id="c4f3c-109">The location of the CRM log files can be changed using the COM+ administration SDK.</span></span> <span data-ttu-id="c4f3c-110">Le nom de la propriété est CRMLogFile, et il existe sur l’objet de collection d' [**applications**](applications.md) .</span><span class="sxs-lookup"><span data-stu-id="c4f3c-110">The property name is CRMLogFile, and it exists on the [**Applications**](applications.md) collection object.</span></span>

 

<span data-ttu-id="c4f3c-111">Lorsqu’une application serveur (compatible CRM) démarre et détecte qu’un fichier journal CRM existe déjà pour cette application serveur, elle effectue la récupération sur ce fichier journal CRM.</span><span class="sxs-lookup"><span data-stu-id="c4f3c-111">When a server application (that is CRM-enabled) starts up and finds that a CRM log file already exists for that server application, it performs recovery on that CRM log file.</span></span> <span data-ttu-id="c4f3c-112">La *récupération* est le processus qui consiste à effectuer toutes les transactions qui ont été interrompues par une défaillance et qui implique que l’infrastructure CRM lit le fichier journal CRM pour toutes les transactions qui n’ont pas été entièrement terminées.</span><span class="sxs-lookup"><span data-stu-id="c4f3c-112">*Recovery* is the process of completing any transactions that were interrupted by a failure and involves the CRM infrastructure reading the CRM log file for any transactions that were not fully completed.</span></span> <span data-ttu-id="c4f3c-113">S’il en trouve, il contacte le DTC pour déterminer le résultat de la transaction.</span><span class="sxs-lookup"><span data-stu-id="c4f3c-113">If it finds any, it contacts the DTC to determine the transaction outcome.</span></span> <span data-ttu-id="c4f3c-114">Il crée ensuite le compensateur CRM et transmet les notifications de validation ou d’abandon comme requis, ainsi que les enregistrements de journal associés.</span><span class="sxs-lookup"><span data-stu-id="c4f3c-114">It then creates the CRM Compensator and passes on the commit or abort notifications as required, together with the associated log records.</span></span>

<span data-ttu-id="c4f3c-115">Les notifications de préparation ne sont pas reçues par le compensateur CRM pendant la récupération.</span><span class="sxs-lookup"><span data-stu-id="c4f3c-115">Prepare notifications are not received by the CRM Compensator during recovery.</span></span> <span data-ttu-id="c4f3c-116">Le compensateur CRM a un indicateur pour déterminer s’il est appelé pendant un fonctionnement normal ou pendant la récupération.</span><span class="sxs-lookup"><span data-stu-id="c4f3c-116">The CRM Compensator has a flag to distinguish whether it is being called during normal operation or during recovery.</span></span>

<span data-ttu-id="c4f3c-117">La récupération trouvera normalement des transactions non terminées uniquement si l’application serveur a été arrêtée anormalement, en raison d’un blocage de processus d’application serveur ou d’un incident d’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c4f3c-117">Recovery will normally find uncompleted transactions only if the server application has been shutdown abnormally, due to either a server application process crash or a computer crash.</span></span> <span data-ttu-id="c4f3c-118">Si l’application serveur est autorisée à s’arrêter normalement, en raison de l’expiration du délai d’inactivité ou de l’arrêt manuel via l’outil d’administration Services de composants, le fichier journal est nettoyé.</span><span class="sxs-lookup"><span data-stu-id="c4f3c-118">If the server application is allowed to shut down normally, due either to the idle time-out or to manual shutdown via the Component Services administrative tool, the log file will be clean.</span></span>

<span data-ttu-id="c4f3c-119">Le démarrage d’une application de serveur CRM pour la récupération n’est pas initié automatiquement.</span><span class="sxs-lookup"><span data-stu-id="c4f3c-119">Starting of a CRM server application for recovery is not automatically initiated.</span></span> <span data-ttu-id="c4f3c-120">Certaines actions externes doivent être effectuées pour démarrer l’application CRM Server où la récupération est requise.</span><span class="sxs-lookup"><span data-stu-id="c4f3c-120">Some external action must be taken to start the CRM server application where recovery is required.</span></span> <span data-ttu-id="c4f3c-121">En général, cela crée un composant dans cette application serveur.</span><span class="sxs-lookup"><span data-stu-id="c4f3c-121">Typically this would be creating a component in that server application.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c4f3c-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c4f3c-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4f3c-123">Concepts de Gestionnaire des ressources de compensation COM+</span><span class="sxs-lookup"><span data-stu-id="c4f3c-123">COM+ Compensating Resource Manager Concepts</span></span>](com--compensating-resource-manager-concepts.md)
</dt> <dt>

[<span data-ttu-id="c4f3c-124">Processus de fonctionnement COM+ CRM</span><span class="sxs-lookup"><span data-stu-id="c4f3c-124">COM+ CRM Operating Process</span></span>](com--crm-operating-process.md)
</dt> </dl>

 

 



