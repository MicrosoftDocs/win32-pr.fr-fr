---
description: Glossaire des termes de Moniteur réseau qui commencent par la lettre F.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 6e6b85cc-83bc-4468-b1cf-3480022a8f12
title: F (Moniteur réseau)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 605eb27b95526fa2f3839c06e6f259a2afec55c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514150"
---
# <a name="f-network-monitor"></a><span data-ttu-id="4ba34-103">F (Moniteur réseau)</span><span class="sxs-lookup"><span data-stu-id="4ba34-103">F (Network Monitor)</span></span>

<dl> <dt>

<span data-ttu-id="4ba34-104"><span id="_netmon_filter_blob_gly"></span><span id="_NETMON_FILTER_BLOB_GLY"></span>**filtrer l’objet BLOB**</span><span class="sxs-lookup"><span data-stu-id="4ba34-104"><span id="_netmon_filter_blob_gly"></span><span id="_NETMON_FILTER_BLOB_GLY"></span>**filter BLOB**</span></span>
</dt> <dd>

<span data-ttu-id="4ba34-105">Objet BLOB (Binary Large Object) utilisé pour limiter la recherche d’une carte d’interface réseau (NIC).</span><span class="sxs-lookup"><span data-stu-id="4ba34-105">Binary large object (BLOB) used to restrict the search for a network interface card (NIC).</span></span> <span data-ttu-id="4ba34-106">Chaque entrée de l’objet BLOB de filtre doit correspondre à une entrée équivalente dans l’objet BLOB du fournisseur de paquets réseau (NPP) qui représente la carte réseau.</span><span class="sxs-lookup"><span data-stu-id="4ba34-106">Each entry in the filter BLOB must match an equivalent entry in the network packet provider (NPP) BLOB that represents the NIC.</span></span> <span data-ttu-id="4ba34-107">Par exemple, une application peut demander uniquement des cartes Ethernet ou des cartes qui prennent en charge une fréquence d’images spécifique.</span><span class="sxs-lookup"><span data-stu-id="4ba34-107">For example, an application can request only Ethernet cards, or cards that support a specific frame rate.</span></span> <span data-ttu-id="4ba34-108">Vous pouvez utiliser un objet BLOB de filtre pour appeler les fonctions **GetNPPBlobFromUI** et **GetNPPBlobTable** .</span><span class="sxs-lookup"><span data-stu-id="4ba34-108">You can use a filter BLOB to call the **GetNPPBlobFromUI** and **GetNPPBlobTable** functions.</span></span>

</dd> <dt>

<span data-ttu-id="4ba34-109"><span id="_netmon_follow_set_gly"></span><span id="_NETMON_FOLLOW_SET_GLY"></span>**ensemble suivant**</span><span class="sxs-lookup"><span data-stu-id="4ba34-109"><span id="_netmon_follow_set_gly"></span><span id="_NETMON_FOLLOW_SET_GLY"></span>**follow set**</span></span>
</dt> <dd>

<span data-ttu-id="4ba34-110">Ensemble de protocoles qui suit un protocole.</span><span class="sxs-lookup"><span data-stu-id="4ba34-110">A protocol set that follows a protocol.</span></span> <span data-ttu-id="4ba34-111">Moniteur réseau utilise le jeu suivant d’un protocole si l’analyseur ne parvient pas à détecter le protocole suivant à partir des données de la capture.</span><span class="sxs-lookup"><span data-stu-id="4ba34-111">Network Monitor uses the follow set of a protocol if the parser cannot detect the next protocol from the data in the capture.</span></span> <span data-ttu-id="4ba34-112">Voir aussi [ *jeu de remise*](h.md)</span><span class="sxs-lookup"><span data-stu-id="4ba34-112">See also [*handoff set*](h.md)</span></span>

</dd> <dt>

<span data-ttu-id="4ba34-113"><span id="_netmon_frame_gly"></span><span id="_NETMON_FRAME_GLY"></span>**Frame**</span><span class="sxs-lookup"><span data-stu-id="4ba34-113"><span id="_netmon_frame_gly"></span><span id="_NETMON_FRAME_GLY"></span>**frame**</span></span>
</dt> <dd>

<span data-ttu-id="4ba34-114">Paquet de données transmis sous la forme d’une unité sur un réseau.</span><span class="sxs-lookup"><span data-stu-id="4ba34-114">A packet of data that is transmitted as one unit over a network.</span></span> <span data-ttu-id="4ba34-115">Chaque frame suit la même organisation de base et contient des informations de contrôle telles que la synchronisation des caractères, des adresses de station, une valeur de vérification des erreurs et une quantité variable de données.</span><span class="sxs-lookup"><span data-stu-id="4ba34-115">Each frame follows the same basic organization, and contains control information such as synchronizing characters, station addresses, an error-checking value, and a variable amount of data.</span></span> <span data-ttu-id="4ba34-116">Également appelé paquet.</span><span class="sxs-lookup"><span data-stu-id="4ba34-116">Also called a packet.</span></span>

</dd> <dt>

<span data-ttu-id="4ba34-117"><span id="_netmon_frame_viewer_window_gly"></span><span id="_NETMON_FRAME_VIEWER_WINDOW_GLY"></span>**fenêtre de l’observateur de frames**</span><span class="sxs-lookup"><span data-stu-id="4ba34-117"><span id="_netmon_frame_viewer_window_gly"></span><span id="_NETMON_FRAME_VIEWER_WINDOW_GLY"></span>**frame viewer window**</span></span>
</dt> <dd>

<span data-ttu-id="4ba34-118">Fenêtre Moniteur réseau qui affiche des informations détaillées sur des frames individuels.</span><span class="sxs-lookup"><span data-stu-id="4ba34-118">A Network Monitor window that displays detailed information about individual frames.</span></span> <span data-ttu-id="4ba34-119">Vous pouvez ouvrir plusieurs fenêtres de visionneuse de frames à la fois.</span><span class="sxs-lookup"><span data-stu-id="4ba34-119">You can open several frame viewer windows at one time.</span></span>

</dd> </dl>

 

 



