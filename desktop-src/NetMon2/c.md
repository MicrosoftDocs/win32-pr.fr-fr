---
description: Glossaire des termes de Moniteur réseau qui commencent par la lettre C.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 9e0b9f77-8a47-4724-b08c-fac3b6e23afc
title: C (Moniteur réseau)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b06dd8ccd4d4c3382e7f7f7bb4426320bfcd8d4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519685"
---
# <a name="c-network-monitor"></a><span data-ttu-id="20ea0-103">C (Moniteur réseau)</span><span class="sxs-lookup"><span data-stu-id="20ea0-103">C (Network Monitor)</span></span>

<dl> <dt>

<span data-ttu-id="20ea0-104"><span id="_netmon_capture_gly"></span><span id="_NETMON_CAPTURE_GLY"></span>**attire**</span><span class="sxs-lookup"><span data-stu-id="20ea0-104"><span id="_netmon_capture_gly"></span><span id="_NETMON_CAPTURE_GLY"></span>**capture**</span></span>
</dt> <dd>

<span data-ttu-id="20ea0-105">Données de trafic réseau collectées dans des frames.</span><span class="sxs-lookup"><span data-stu-id="20ea0-105">Network traffic data that is collected in frames.</span></span> <span data-ttu-id="20ea0-106">Un fournisseur de paquets réseau (NPP) effectue une capture.</span><span class="sxs-lookup"><span data-stu-id="20ea0-106">A network packet provider (NPP) performs a capture.</span></span> <span data-ttu-id="20ea0-107">Voir aussi [*capture différée*](d.md)et *capture en temps réel*</span><span class="sxs-lookup"><span data-stu-id="20ea0-107">See also [*delayed capture*](d.md), and *real-time capture*</span></span>

</dd> <dt>

<span data-ttu-id="20ea0-108"><span id="_netmon_capture_file_gly"></span><span id="_NETMON_CAPTURE_FILE_GLY"></span>**fichier de capture**</span><span class="sxs-lookup"><span data-stu-id="20ea0-108"><span id="_netmon_capture_file_gly"></span><span id="_NETMON_CAPTURE_FILE_GLY"></span>**capture file**</span></span>
</dt> <dd>

<span data-ttu-id="20ea0-109">Fichier créé par Moniteur réseau pour stocker les données capturées.</span><span class="sxs-lookup"><span data-stu-id="20ea0-109">A file that Network Monitor creates to store captured data.</span></span> <span data-ttu-id="20ea0-110">L’extension de nom de fichier. Cap identifie un fichier de capture.</span><span class="sxs-lookup"><span data-stu-id="20ea0-110">The .cap file name extension identifies a capture file.</span></span> <span data-ttu-id="20ea0-111">Moniteur réseau génère un nom de fichier de capture de manière aléatoire, mais vous pouvez modifier le nom du fichier lorsque vous enregistrez le fichier de capture.</span><span class="sxs-lookup"><span data-stu-id="20ea0-111">Network Monitor randomly generates a capture file name, but you can change the file name when you save the capture file.</span></span>

<span data-ttu-id="20ea0-112">Moniteur réseau crée un fichier de capture chaque fois que le processus de capture démarre, puis laisse le fichier ouvert pendant le processus de capture.</span><span class="sxs-lookup"><span data-stu-id="20ea0-112">Network Monitor creates a capture file each time the capture process starts, and then keeps the file open during the capture process.</span></span> <span data-ttu-id="20ea0-113">Vous ne pouvez pas accéder au contenu d’un fichier de capture tant que le processus de capture n’est pas arrêté et que le fichier de capture n’est pas fermé.</span><span class="sxs-lookup"><span data-stu-id="20ea0-113">You cannot access the contents of a capture file until the capture process is stopped and the capture file is closed.</span></span>

</dd> <dt>

<span data-ttu-id="20ea0-114"><span id="_netmon_capture_filter_gly"></span><span id="_NETMON_CAPTURE_FILTER_GLY"></span>**filtre de capture**</span><span class="sxs-lookup"><span data-stu-id="20ea0-114"><span id="_netmon_capture_filter_gly"></span><span id="_NETMON_CAPTURE_FILTER_GLY"></span>**capture filter**</span></span>
</dt> <dd>

<span data-ttu-id="20ea0-115">Ensemble de fonctions de Moniteur réseau utilisées pour restreindre les trames entrantes utilisées par une application de fournisseur de paquets réseau (NPP).</span><span class="sxs-lookup"><span data-stu-id="20ea0-115">A set of Network Monitor functions used to restrict incoming frames that a network packet provider (NPP) application uses.</span></span>

</dd> <dt>

<span data-ttu-id="20ea0-116"><span id="_netmon_capture_trigger_gly"></span><span id="_NETMON_CAPTURE_TRIGGER_GLY"></span>**déclencheur de capture**</span><span class="sxs-lookup"><span data-stu-id="20ea0-116"><span id="_netmon_capture_trigger_gly"></span><span id="_NETMON_CAPTURE_TRIGGER_GLY"></span>**capture trigger**</span></span>
</dt> <dd>

<span data-ttu-id="20ea0-117">Événement de déclencheur qui est défini pour arrêter le processus de capture.</span><span class="sxs-lookup"><span data-stu-id="20ea0-117">A trigger event that is set to stop the capture process.</span></span> <span data-ttu-id="20ea0-118">L’événement de déclencheur de capture peut être un fichier de capture temporaire qui est dirigé vers un niveau spécifique ou un modèle de données qui se produit dans un frame capturé.</span><span class="sxs-lookup"><span data-stu-id="20ea0-118">The capture trigger event can be a temporary capture file that is directed to a specific level or data pattern that occurs in a captured frame.</span></span>

</dd> <dt>

<span data-ttu-id="20ea0-119"><span id="_netmon_captured_data_gly"></span><span id="_NETMON_CAPTURED_DATA_GLY"></span>**données capturées**</span><span class="sxs-lookup"><span data-stu-id="20ea0-119"><span id="_netmon_captured_data_gly"></span><span id="_NETMON_CAPTURED_DATA_GLY"></span>**captured data**</span></span>
</dt> <dd>

<span data-ttu-id="20ea0-120">Frames ayant un ensemble défini de critères.</span><span class="sxs-lookup"><span data-stu-id="20ea0-120">Frames that have a defined set of criteria.</span></span> <span data-ttu-id="20ea0-121">Les trames de données sont contenues dans un fichier de capture temporaire.</span><span class="sxs-lookup"><span data-stu-id="20ea0-121">The data frames are contained in a temporary capture file.</span></span>

</dd> <dt>

<span data-ttu-id="20ea0-122"><span id="_netmon_conversation_statistics_gly"></span><span id="_NETMON_CONVERSATION_STATISTICS_GLY"></span>**statistiques de conversation**</span><span class="sxs-lookup"><span data-stu-id="20ea0-122"><span id="_netmon_conversation_statistics_gly"></span><span id="_NETMON_CONVERSATION_STATISTICS_GLY"></span>**conversation statistics**</span></span>
</dt> <dd>

<span data-ttu-id="20ea0-123">Statistiques du trafic réseau enregistrées pendant une capture.</span><span class="sxs-lookup"><span data-stu-id="20ea0-123">Statistics of network traffic saved during a capture.</span></span> <span data-ttu-id="20ea0-124">Ces statistiques incluent les informations de station et de session qui commencent au démarrage du processus de capture et se terminent à l’arrêt de la capture.</span><span class="sxs-lookup"><span data-stu-id="20ea0-124">These statistics include station and session information beginning when the capture process starts, and ending when the capture stops.</span></span> <span data-ttu-id="20ea0-125">Si vous suspendez le processus de capture, Moniteur réseau continue à ajouter des statistiques lorsque vous reprenez le processus.</span><span class="sxs-lookup"><span data-stu-id="20ea0-125">If you pause the capture process, Network Monitor continues to add statistics when you resume the process.</span></span> <span data-ttu-id="20ea0-126">Pour récupérer des statistiques de conversation, appelez la méthode **GetConversationStatistics** pour l’interface que vous utilisez.</span><span class="sxs-lookup"><span data-stu-id="20ea0-126">To retrieve conversation statistics, call the **GetConversationStatistics** method for the interface you are using.</span></span>

</dd> </dl>

 

 



