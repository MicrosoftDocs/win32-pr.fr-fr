---
title: Compatibilité du client et du serveur-Windows 8
description: Compatibilité entre le client et le serveur Windows 8 et Windows Server 2012
ms.assetid: 5067219A-EBA2-4FAF-8C17-7AB22C5EADD0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca5b685ae10b97a7b8197737944ea7231d226514
ms.sourcegitcommit: 477b1efe7d9c2f91d5f2ac588a20edf348b1c734
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2019
ms.locfileid: "104313969"
---
# <a name="windows-8-and-windows-server-2012-client-and-server-compatibility"></a><span data-ttu-id="84b2f-103">Compatibilité entre le client et le serveur Windows 8 et Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="84b2f-103">Windows 8 and Windows Server 2012 client and server compatibility</span></span>

<span data-ttu-id="84b2f-104">Cette section décrit les modifications apportées au système d’exploitation dont vous devez prêter une attention particulière en raison des impacts potentiels sur les applications existantes et de la façon dont les nouvelles applications doivent être conçues sur les clients, sur les serveurs, ou sur les clients et les serveurs.</span><span class="sxs-lookup"><span data-stu-id="84b2f-104">This section describes changes in the operating system that you should pay special attention to due to the potential impacts on existing apps and how new apps should be designed on clients, on servers, or on both clients and servers.</span></span> <span data-ttu-id="84b2f-105">Voici la liste des rubriques traitées dans cette section, regroupées par domaine de fonctionnalité :</span><span class="sxs-lookup"><span data-stu-id="84b2f-105">Following is the list of topics covered in this section, grouped by feature area:</span></span>

<span data-ttu-id="84b2f-106">**AppCompat**</span><span class="sxs-lookup"><span data-stu-id="84b2f-106">**AppCompat**</span></span>

-   <span data-ttu-id="84b2f-107">Mise à jour des règles de détection des applications de sécurité</span><span class="sxs-lookup"><span data-stu-id="84b2f-107">Security app detection rules update</span></span>
-   <span data-ttu-id="84b2f-108">Détermination de l’état des shims</span><span class="sxs-lookup"><span data-stu-id="84b2f-108">Determining shim status</span></span>
-   <span data-ttu-id="84b2f-109">Les applications serveur doivent pouvoir s’exécuter sans l’interpréteur de commandes graphique de serveur</span><span class="sxs-lookup"><span data-stu-id="84b2f-109">Server apps must be able to run without the Server Graphical Shell</span></span>
-   <span data-ttu-id="84b2f-110">Les composants serveur RDS sont supprimés de Windows 8</span><span class="sxs-lookup"><span data-stu-id="84b2f-110">RDS server components are removed from Windows 8</span></span>
-   <span data-ttu-id="84b2f-111">Type de fichier et modèle d’association de protocole</span><span class="sxs-lookup"><span data-stu-id="84b2f-111">File type and protocol associations model</span></span>
-   <span data-ttu-id="84b2f-112">Modérateur de l’activité du Bureau</span><span class="sxs-lookup"><span data-stu-id="84b2f-112">Desktop Activity Moderator</span></span>
-   <span data-ttu-id="84b2f-113">.NET Framework 4,5 est la valeur par défaut et .NET Framework 3,5 est facultatif</span><span class="sxs-lookup"><span data-stu-id="84b2f-113">.NET Framework 4.5 is default and .NET Framework 3.5 is optional</span></span>
-   <span data-ttu-id="84b2f-114">Les applications de bureau peuvent ne pas être visibles après le lancement du navigateur Web par défaut</span><span class="sxs-lookup"><span data-stu-id="84b2f-114">Desktop apps may not be visible after launching the default web browser</span></span>
-   <span data-ttu-id="84b2f-115">Mode de contraste élevé</span><span class="sxs-lookup"><span data-stu-id="84b2f-115">High-contrast mode</span></span>
-   <span data-ttu-id="84b2f-116">Manifeste de l’application (exécutable)</span><span class="sxs-lookup"><span data-stu-id="84b2f-116">App (executable) manifest</span></span>
-   <span data-ttu-id="84b2f-117">Le modèle actuel mis en file d’attente est déconseillé</span><span class="sxs-lookup"><span data-stu-id="84b2f-117">Queued present model is being deprecated</span></span>
-   <span data-ttu-id="84b2f-118">Scénarios de l’Assistant Compatibilité des programmes pour Windows 8</span><span class="sxs-lookup"><span data-stu-id="84b2f-118">Program Compatibility Assistant scenarios for Windows 8</span></span>
-   <span data-ttu-id="84b2f-119">Gadgets du Bureau supprimés</span><span class="sxs-lookup"><span data-stu-id="84b2f-119">Desktop gadgets removed</span></span>

<span data-ttu-id="84b2f-120">**Stockage et système de fichiers**</span><span class="sxs-lookup"><span data-stu-id="84b2f-120">**Storage and File System**</span></span>

-   <span data-ttu-id="84b2f-121">Mise à jour de compatibilité des disques au format avancé (4K)</span><span class="sxs-lookup"><span data-stu-id="84b2f-121">Advanced format (4K) disk compatibility update</span></span>
-   <span data-ttu-id="84b2f-122">Allocation dynamique d’unités logiques</span><span class="sxs-lookup"><span data-stu-id="84b2f-122">Thin provisioning of logical units</span></span>
-   <span data-ttu-id="84b2f-123">Le stockage étendu est désormais facultatif pour environnement de préinstallation Windows (WinPE) (WinPE) et référence de serveur</span><span class="sxs-lookup"><span data-stu-id="84b2f-123">Enhanced storage is now optional for Windows Preinstallation Environment (WinPE) and server SKU</span></span>
-   <span data-ttu-id="84b2f-124">Le service de disque virtuel passe à l’API de gestion du stockage Windows basé sur le Windows Management Instrumentation (WMI)</span><span class="sxs-lookup"><span data-stu-id="84b2f-124">Virtual Disk Service is transitioning to the Windows Management Instrumentation (WMI)-based Windows Storage Management API</span></span>
-   <span data-ttu-id="84b2f-125">Interface utilisateur des versions précédentes supprimées pour les volumes locaux</span><span class="sxs-lookup"><span data-stu-id="84b2f-125">Previous versions UI removed for local volumes</span></span>
-   <span data-ttu-id="84b2f-126">StorAHCI remplace MSAHCI</span><span class="sxs-lookup"><span data-stu-id="84b2f-126">StorAHCI replaces MSAHCI</span></span>
-   <span data-ttu-id="84b2f-127">Sauvegarde et restauration de Windows 7 déconseillées</span><span class="sxs-lookup"><span data-stu-id="84b2f-127">Windows 7 backup and restore deprecated</span></span>
-   <span data-ttu-id="84b2f-128">Transferts de données déchargées</span><span class="sxs-lookup"><span data-stu-id="84b2f-128">Offloaded data transfers</span></span>

<span data-ttu-id="84b2f-129">**Autres**</span><span class="sxs-lookup"><span data-stu-id="84b2f-129">**Other**</span></span>

-   <span data-ttu-id="84b2f-130">Gestionnaire de fenêtrage est toujours activé</span><span class="sxs-lookup"><span data-stu-id="84b2f-130">Desktop Window Manager is always on</span></span>
-   <span data-ttu-id="84b2f-131">Direct2D ne prend pas en charge le rendu des sous-fichiers « enrichis » dans Internet Explorer 9</span><span class="sxs-lookup"><span data-stu-id="84b2f-131">Direct2D does not support rendering to "rich" metafiles in Internet Explorer 9</span></span>
-   <span data-ttu-id="84b2f-132">Modifications apportées à la prise en charge matérielle héritée virtuel DX9</span><span class="sxs-lookup"><span data-stu-id="84b2f-132">Changes in DX9 legacy hardware support</span></span>
-   <span data-ttu-id="84b2f-133">MSAA n’est pas disponible pour les applications du Windows Store</span><span class="sxs-lookup"><span data-stu-id="84b2f-133">MSAA is not available to Windows Store apps</span></span>
-   <span data-ttu-id="84b2f-134">Le port 3 est déconseillé pour les pilotes NDIS 6,30</span><span class="sxs-lookup"><span data-stu-id="84b2f-134">Port 3 is deprecated for NDIS 6.30 drivers</span></span>

 

 
