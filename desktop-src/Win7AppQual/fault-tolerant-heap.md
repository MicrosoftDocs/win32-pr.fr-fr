---
description: .
ms.assetid: f1ac375a-3f08-49cd-8752-6f55db24a60c
title: Segment de mémoire à tolérance de panne
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 349c8c3d6d066de3d563880c169c8dde2e062370
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106538181"
---
# <a name="fault-tolerant-heap"></a><span data-ttu-id="8b75f-103">Segment de mémoire à tolérance de panne</span><span class="sxs-lookup"><span data-stu-id="8b75f-103">Fault Tolerant Heap</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="8b75f-104">Plateformes affectées</span><span class="sxs-lookup"><span data-stu-id="8b75f-104">Affected Platforms</span></span>

<span data-ttu-id="8b75f-105">**Clients-** Windows 7</span><span class="sxs-lookup"><span data-stu-id="8b75f-105">**Clients -** Windows 7</span></span>  

## <a name="feature-impact"></a><span data-ttu-id="8b75f-106">Impact sur les fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="8b75f-106">Feature Impact</span></span>

 <span data-ttu-id="8b75f-107">**Gravité-** Médias</span><span class="sxs-lookup"><span data-stu-id="8b75f-107">**Severity -** Medium</span></span>  
<span data-ttu-id="8b75f-108">**Fréquence-** Entrée</span><span class="sxs-lookup"><span data-stu-id="8b75f-108">**Frequency -** Low</span></span>  


## <a name="description"></a><span data-ttu-id="8b75f-109">Description</span><span class="sxs-lookup"><span data-stu-id="8b75f-109">Description</span></span>

<span data-ttu-id="8b75f-110">Le segment de mémoire à tolérance de panne (FTH) est un sous-système de Windows 7 responsable de la surveillance des pannes d’application et de l’application de mesures d’atténuation de manière autonome afin d’éviter les pannes futures pour chaque application.</span><span class="sxs-lookup"><span data-stu-id="8b75f-110">The Fault Tolerant Heap (FTH) is a subsystem of Windows 7 responsible for monitoring application crashes and autonomously applying mitigations to prevent future crashes on a per application basis.</span></span> <span data-ttu-id="8b75f-111">Pour la grande majorité des utilisateurs, FTH ne nécessite aucune intervention ni modification de leur part.</span><span class="sxs-lookup"><span data-stu-id="8b75f-111">For the vast majority of users, FTH will function with no need for intervention or change on their part.</span></span> <span data-ttu-id="8b75f-112">Toutefois, dans certains cas, les développeurs d’applications et les testeurs de logiciels peuvent avoir besoin de remplacer le comportement par défaut de ce système.</span><span class="sxs-lookup"><span data-stu-id="8b75f-112">However, in some cases, application developers and software testers may need to override the default behavior of this system.</span></span>

## <a name="solution"></a><span data-ttu-id="8b75f-113">Solution</span><span class="sxs-lookup"><span data-stu-id="8b75f-113">Solution</span></span>

<span data-ttu-id="8b75f-114">**Affichage de l’activité du tas à tolérance de panne**</span><span class="sxs-lookup"><span data-stu-id="8b75f-114">**Viewing Fault Tolerant Heap activity**</span></span>

<span data-ttu-id="8b75f-115">Le segment de mémoire à tolérance de panne enregistre les informations lorsque le service démarre, s’arrête ou commence à atténuer les problèmes pour une nouvelle application.</span><span class="sxs-lookup"><span data-stu-id="8b75f-115">Fault Tolerant Heap logs information when the service starts, stops, or starts mitigating problems for a new application.</span></span> <span data-ttu-id="8b75f-116">Pour voir ces informations, effectuez les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="8b75f-116">To view this information, follow these steps:</span></span>

1.  <span data-ttu-id="8b75f-117">Cliquez sur le menu Démarrer.</span><span class="sxs-lookup"><span data-stu-id="8b75f-117">Click the Start menu.</span></span>
2.  <span data-ttu-id="8b75f-118">Cliquez avec le bouton droit sur **ordinateur** , puis cliquez sur **gérer**.</span><span class="sxs-lookup"><span data-stu-id="8b75f-118">Right-click **Computer** and click **Manage**.</span></span>
3.  <span data-ttu-id="8b75f-119">Cliquez sur **Observateur d’événements**  >  **les journaux des applications et des services**  >  **Microsoft**  >  **Windows > avec tolérance de pannes**</span><span class="sxs-lookup"><span data-stu-id="8b75f-119">Click **Event Viewer** > **Applications and Services Logs** > **Microsoft** > **Windows > Fault-Tolerant-Heap**</span></span>
4.  <span data-ttu-id="8b75f-120">Affichez les événements FTH.</span><span class="sxs-lookup"><span data-stu-id="8b75f-120">View FTH Events.</span></span>

<span data-ttu-id="8b75f-121">Les événements d’arrêt et de démarrage du service ne contiennent pas de données supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="8b75f-121">The service stop and start events contain no additional data.</span></span> <span data-ttu-id="8b75f-122">L’événement FTH activé contient l’ID de processus (PID), le nom de l’image de processus et l’heure de début de l’instance de processus.</span><span class="sxs-lookup"><span data-stu-id="8b75f-122">The FTH Enabled event contains the Process ID (PID), the process image name, and the process instance start time.</span></span>

<span data-ttu-id="8b75f-123">**Désactivation du tas à tolérance de panne**</span><span class="sxs-lookup"><span data-stu-id="8b75f-123">**Disabling Fault Tolerant Heap**</span></span>

<span data-ttu-id="8b75f-124">**Attention** Des problèmes sérieux peuvent survenir si vous modifiez le registre de manière incorrecte à l’aide de l’éditeur du registre ou en utilisant une autre méthode.</span><span class="sxs-lookup"><span data-stu-id="8b75f-124">**Caution** Serious problems may occur if you modify the registry incorrectly by using Registry Editor or by using another method.</span></span> <span data-ttu-id="8b75f-125">Ces problèmes peuvent nécessiter la réinstallation du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="8b75f-125">These problems may require you to reinstall the operating system.</span></span> <span data-ttu-id="8b75f-126">Microsoft ne peut pas garantir que ces problèmes puissent être résolus.</span><span class="sxs-lookup"><span data-stu-id="8b75f-126">Microsoft cannot guarantee that these problems can be solved.</span></span> <span data-ttu-id="8b75f-127">Toute modification du registre relève de votre propre responsabilité.</span><span class="sxs-lookup"><span data-stu-id="8b75f-127">Modify the registry at your own risk.</span></span>  
 <span data-ttu-id="8b75f-128">Pour désactiver entièrement le segment de mémoire à tolérance de panne sur un système, définissez la \_ valeur reg DWORD **HKLM \\ Software \\ Microsoft \\ FTH \\ Enabled** sur **0**.</span><span class="sxs-lookup"><span data-stu-id="8b75f-128">To disable Fault Tolerant Heap entirely on a system, set the REG\_DWORD value **HKLM\\Software\\Microsoft\\FTH\\Enabled** to **0**.</span></span>

<span data-ttu-id="8b75f-129">Après avoir modifié cette valeur, redémarrez le système.</span><span class="sxs-lookup"><span data-stu-id="8b75f-129">After changing this value, restart the system.</span></span> <span data-ttu-id="8b75f-130">FTH ne s’activera plus pour les nouvelles applications.</span><span class="sxs-lookup"><span data-stu-id="8b75f-130">FTH will no longer activate for new applications.</span></span>

<span data-ttu-id="8b75f-131">**Réinitialisation de la liste des applications suivies par FTH**</span><span class="sxs-lookup"><span data-stu-id="8b75f-131">**Resetting the list of applications tracked by FTH**</span></span>

<span data-ttu-id="8b75f-132">Le segment de mémoire à tolérance de panne est auto-géré et s’arrête de façon autonome dans le cas où les atténuations ne sont pas effectives pour une application donnée.</span><span class="sxs-lookup"><span data-stu-id="8b75f-132">Fault Tolerant heap is self-managing and will autonomously stop applying in the case that mitigations are not effective for a given application.</span></span> <span data-ttu-id="8b75f-133">Toutefois, si vous devez réinitialiser la liste des applications pour lesquelles FTH est en mesure d’atténuer les problèmes (par exemple, si vous testez une application et que vous devez reproduire un incident que FTH est en mesure d’atténuer), vous pouvez exécuter la commande suivante à partir d’une invite de commandes avec élévation de privilèges :  **Rundll32.exe fthsvc.dll, FthSysprepSpecialize**</span><span class="sxs-lookup"><span data-stu-id="8b75f-133">However, if you need to reset the list of applications for which FTH is mitigating problems (for example, if you are testing an application and need to reproduce a crash that FTH is mitigating), you can run the following command from an elevated command prompt:  **Rundll32.exe fthsvc.dll,FthSysprepSpecialize**</span></span>  
<span data-ttu-id="8b75f-134">**Attention** L’exécution de cette commande entraîne la suppression de toutes les applications FTH, de sorte que les applications qui fonctionnent correctement peuvent commencer à se bloquer après l’exécution de cette commande.</span><span class="sxs-lookup"><span data-stu-id="8b75f-134">**Caution** Running this command will clear all FTH applications, so applications that are currently functioning properly may begin to crash again after running this command.</span></span>  

 

 



