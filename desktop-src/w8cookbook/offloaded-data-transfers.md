---
title: Transferts de données déchargées
description: Transferts de données déchargées
ms.assetid: 91EBE6D6-2DA7-48DA-AEB7-3FAFCA8341F5
keywords:
- ODX
- déchargement de copie
- déchargement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1057ed27347fefc7ebc6a171eb7273da4341b024
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2020
ms.locfileid: "106509884"
---
# <a name="offloaded-data-transfers"></a><span data-ttu-id="68d27-106">Transferts de données déchargées</span><span class="sxs-lookup"><span data-stu-id="68d27-106">Offloaded data transfers</span></span>

## <a name="platforms"></a><span data-ttu-id="68d27-107">Plateformes</span><span class="sxs-lookup"><span data-stu-id="68d27-107">Platforms</span></span>

<span data-ttu-id="68d27-108">**Clients** – Windows 8</span><span class="sxs-lookup"><span data-stu-id="68d27-108">**Clients** – Windows 8</span></span>  
<span data-ttu-id="68d27-109">**Serveurs** – Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="68d27-109">**Servers** – Windows Server 2012</span></span>  


## <a name="description"></a><span data-ttu-id="68d27-110">Description</span><span class="sxs-lookup"><span data-stu-id="68d27-110">Description</span></span>

<span data-ttu-id="68d27-111">Pour accélérer le déplacement des données de stockage, Microsoft a développé une nouvelle technologie de transfert de données : le transfert de données déchargées (ODX).</span><span class="sxs-lookup"><span data-stu-id="68d27-111">To advance the storage data movement, Microsoft has developed a new data transfer technology – offloaded data transfer (ODX).</span></span> <span data-ttu-id="68d27-112">Au lieu d’utiliser des opérations d’écriture de lecture et de mise en mémoire tampon, Windows ODX démarre l’opération de copie avec une lecture de déchargement et récupère un jeton représentant les données du dispositif de stockage, puis utilise une commande d’écriture de déchargement avec le jeton pour demander le déplacement des données du disque source vers le disque de destination.</span><span class="sxs-lookup"><span data-stu-id="68d27-112">Instead of using buffered read and buffered write operations, Windows ODX starts the copy operation with an offload read and retrieves a token representing the data from the storage device, then uses an offload write command with the token to request data movement from the source disk to the destination disk.</span></span> <span data-ttu-id="68d27-113">Le gestionnaire de copie des périphériques de stockage effectue le déplacement des données en fonction du jeton.</span><span class="sxs-lookup"><span data-stu-id="68d27-113">The copy manager of the storage devices performs the data movement according to the token.</span></span> <span data-ttu-id="68d27-114">Dans Windows 8, le responsable informatique et l’administrateur du stockage sont en mesure d’utiliser la fonctionnalité ODX de Windows pour interagir avec le périphérique de stockage afin de déplacer des fichiers ou des données volumineux via le réseau de stockage à grande vitesse.</span><span class="sxs-lookup"><span data-stu-id="68d27-114">In the Windows 8, the IT manager and storage administrator are able to use the Windows ODX feature to interact with the storage device to move large files or data through the high-speed storage network.</span></span> <span data-ttu-id="68d27-115">Windows ODX réduit considérablement le trafic réseau client-serveur et l’utilisation du temps processeur pendant les transferts de données volumineux, car tous les déplacements de données se trouvent sur le réseau de stockage principal.</span><span class="sxs-lookup"><span data-stu-id="68d27-115">Windows ODX will significantly reduce client-server network traffic and CPU time usage during large data transfers because all the data movement is at the backend storage network.</span></span> <span data-ttu-id="68d27-116">ODX peut être utilisé dans le cadre du déploiement d’ordinateurs virtuels, de la migration massive des données et de la prise en charge des périphériques de stockage hiérarchisé, et peut réduire le coût du déploiement du matériel physique via les fonctionnalités de stockage ODX et de l’allocation dynamique.</span><span class="sxs-lookup"><span data-stu-id="68d27-116">ODX can be used in virtual machine deployment, massive data migration, and tiered storage device support, and can lower the cost of physical hardware deployment through the ODX and thin provisioning storage features.</span></span>

> [!Note]  
> <span data-ttu-id="68d27-117">Cette fonctionnalité fonctionne uniquement sur les périphériques de stockage avec l’implémentation de la spécification SPC4 et SBC3.</span><span class="sxs-lookup"><span data-stu-id="68d27-117">This feature will only work on storage devices with SPC4 and SBC3 specification implementation.</span></span>

 

## <a name="functional-details"></a><span data-ttu-id="68d27-118">Détails fonctionnels</span><span class="sxs-lookup"><span data-stu-id="68d27-118">Functional details</span></span>

-   <span data-ttu-id="68d27-119">La fonctionnalité ODX de Windows est incorporée dans le moteur de copie du système d’exploitation Windows. pendant l’énumération du stockage, Windows interroge la fonctionnalité ODX du dispositif de stockage</span><span class="sxs-lookup"><span data-stu-id="68d27-119">The Windows ODX feature is embedded in the copy engine of the Windows operating system; during storage enumeration, Windows will query the ODX capability of the storage device</span></span>
-   <span data-ttu-id="68d27-120">La copie du dispositif de stockage source et du périphérique de stockage de destination de copie doit être gérée sous le même gestionnaire de copie pour la prise en charge du déchargement</span><span class="sxs-lookup"><span data-stu-id="68d27-120">Copy source storage device and copy destination storage device should be managed under the same copy manager for copy offload support</span></span>
-   <span data-ttu-id="68d27-121">Si une opération de déchargement de copie échoue, le gestionnaire de copie du dispositif de stockage doit retourner les données de sens supplémentaires appropriées pour la gestion des erreurs des applications</span><span class="sxs-lookup"><span data-stu-id="68d27-121">If a copy offload operation fails, the storage device’s copy manager must return the proper additional sense data for the apps’ error handling</span></span>
-   <span data-ttu-id="68d27-122">Le moteur de copie Windows revient à l’opération de copie traditionnelle en cas d’échec de l’opération de déchargement de copie</span><span class="sxs-lookup"><span data-stu-id="68d27-122">The Windows copy engine will fall back to the traditional copy operation if the copy offload operation fails</span></span>

## <a name="using-odx"></a><span data-ttu-id="68d27-123">Utilisation de ODX</span><span class="sxs-lookup"><span data-stu-id="68d27-123">Using ODX</span></span>

-   <span data-ttu-id="68d27-124">L’application de transfert de données doit s’assurer que le LUN source de copie et le numéro d’unité logique de destination de copie sont bien basés sur ODX avant d’appeler les routines d’API ODX</span><span class="sxs-lookup"><span data-stu-id="68d27-124">The data transfer app must ensure both copy source LUN and copy destination LUN are ODX capable before calling the ODX API routines</span></span>
-   <span data-ttu-id="68d27-125">Dans l’Explorateur Windows, les utilisateurs peuvent utiliser « faire glisser » ou « copier et coller » pour effectuer un déchargement de copie</span><span class="sxs-lookup"><span data-stu-id="68d27-125">In Windows explorer, users could use “drag” or “copy and paste” to perform copy offload</span></span>
-   <span data-ttu-id="68d27-126">Lorsque le numéro d’unité logique source et le numéro d’unité logique de destination sont montés avec le système de fichiers, l’application ne doit appeler que le \_ déchargement FSCTL \_ et l' \_ écriture de déchargement FSCTL \_ pour effectuer le transfert de données du LUN source vers le LUN de destination.</span><span class="sxs-lookup"><span data-stu-id="68d27-126">When the source LUN and destination LUN are mounted with the file system, the app must only call FSCTL\_Offload\_Read and FSCTL\_Offload\_Write to perform data transfer from the source LUN to the destination LUN</span></span>
-   <span data-ttu-id="68d27-127">Si une opération de déchargement de copie échoue, le gestionnaire de copie du dispositif de stockage doit retourner les données de sens supplémentaires appropriées pour la gestion des erreurs des applications</span><span class="sxs-lookup"><span data-stu-id="68d27-127">If a copy offload operation fails, the storage device’s copy manager must return the proper additional sense data for apps’ error handling</span></span>
-   <span data-ttu-id="68d27-128">Lorsque le numéro d’unité logique source ou le numéro d’unité logique de destination n’est pas monté avec le système de fichiers et verrouillé, l’application doit appeler le \_ stockage IOCTL \_ gérer les \_ \_ \_ attributs du jeu de données avec DeviceDsmAction \_ OffloadRead ou DeviceDsmAction \_ OffloadWrite action pour effectuer le déchargement de copie</span><span class="sxs-lookup"><span data-stu-id="68d27-128">When the source LUN or destination LUN is not mounted with the file system and locked, the app must call IOCTL\_STORAGE\_MANAGE\_DATA\_SET\_ATTRIBUTES with DeviceDsmAction\_OffloadRead or DeviceDsmAction\_OffloadWrite action to perform copy offload</span></span>
-   <span data-ttu-id="68d27-129">Les applications de gestion du stockage peuvent utiliser \_ \_ l’API Pass via SCSI pour effectuer des transferts de données déchargées lorsque les numéros d’unité logique source et de destination ne sont pas montés avec un système de fichiers et verrouillés</span><span class="sxs-lookup"><span data-stu-id="68d27-129">Storage management apps may use SCSI\_PASS\_THROUGH API to perform offloaded data transfers when both source and destination LUNs are not mounted with any file system and locked</span></span>

## <a name="tests"></a><span data-ttu-id="68d27-130">Tests</span><span class="sxs-lookup"><span data-stu-id="68d27-130">Tests</span></span>

-   <span data-ttu-id="68d27-131">Pour garantir une expérience utilisateur robuste, vérifiez la certification ODX Windows du groupe de stockage.</span><span class="sxs-lookup"><span data-stu-id="68d27-131">To ensure a robust user experience, verify the Windows ODX certification of the storage array</span></span>
-   <span data-ttu-id="68d27-132">Le dispositif de stockage doit respecter les exigences de certification des transferts de données déchargées Windows (utilisées pour être logo) pour prendre en charge la fonctionnalité ODX</span><span class="sxs-lookup"><span data-stu-id="68d27-132">The storage device must comply with Windows Offloaded Data Transfers certification (used to be Logo) requirements to support ODX feature</span></span>
-   <span data-ttu-id="68d27-133">Utiliser le kit de certification du matériel des transferts de données déchargées Windows pour vérifier la prise en charge des fonctionnalités ODX des dispositifs de stockage</span><span class="sxs-lookup"><span data-stu-id="68d27-133">Use the Windows Offloaded Data Transfers Hardware Certification Kit to verify the ODX feature support of the storage devices</span></span>

## <a name="resources"></a><span data-ttu-id="68d27-134">Ressources</span><span class="sxs-lookup"><span data-stu-id="68d27-134">Resources</span></span>

-   <span data-ttu-id="68d27-135">Spécification de la spécification XCOPY pour XCOPY Lite (11-059r8)</span><span class="sxs-lookup"><span data-stu-id="68d27-135">T10 XCOPY Lite Spec (11-059r8)</span></span>
    -   [https://www.t10.org/cgi-bin/ac.pl?t=f&f=spc4r35b.pdf](https://www.t10.org/cgi-bin/ac.pl?t=f&f=spc4r35b.pdf)
    -   [https://www.t10.org/cgi-bin/ac.pl?t=f&f=sbc3r30.pdf](https://www.t10.org/cgi-bin/ac.pl?t=f&f=sbc3r30.pdf)
-   [<span data-ttu-id="68d27-136">Services du tableau de bord matériel</span><span class="sxs-lookup"><span data-stu-id="68d27-136">Hardware Dashboard Services</span></span>](/windows-hardware/drivers/dashboard/)
-   [<span data-ttu-id="68d27-137">\_Structure de transfert SCSI \_</span><span class="sxs-lookup"><span data-stu-id="68d27-137">SCSI\_PASS\_THROUGH Structure</span></span>](/windows-hardware/drivers/ddi/ntddscsi/ns-ntddscsi-_scsi_pass_through)

 

 