---
description: ATM s’applique aux environnements LAN et WAN.
ms.assetid: 532a876c-9b31-410e-9331-5e8aa98ccaee
title: Annexe Winsock ATM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63ec056cc2b84c9449ed466a60a15683df29744b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106520415"
---
# <a name="winsock-atm-annex"></a><span data-ttu-id="29ae8-103">Annexe Winsock ATM</span><span class="sxs-lookup"><span data-stu-id="29ae8-103">Winsock ATM Annex</span></span>

<span data-ttu-id="29ae8-104">ATM s’applique aux environnements LAN et WAN.</span><span class="sxs-lookup"><span data-stu-id="29ae8-104">ATM is applicable to both LAN and WAN environments.</span></span> <span data-ttu-id="29ae8-105">Un réseau ATM transporte simultanément un large éventail de trafic réseau (voix, données, image et vidéo).</span><span class="sxs-lookup"><span data-stu-id="29ae8-105">An ATM network simultaneously transports a wide variety of network traffic — voice, data, image, and video.</span></span> <span data-ttu-id="29ae8-106">Il fournit aux utilisateurs une qualité de service garantie sur la base d’un canal virtuel (VC).</span><span class="sxs-lookup"><span data-stu-id="29ae8-106">It provides users with a guaranteed quality of service on a per-virtual channel (VC) basis.</span></span>



| <span data-ttu-id="29ae8-107">Élément</span><span class="sxs-lookup"><span data-stu-id="29ae8-107">Element</span></span>          | <span data-ttu-id="29ae8-108">Description</span><span class="sxs-lookup"><span data-stu-id="29ae8-108">Description</span></span>                                                                                                                                                 |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29ae8-109">Nom (s) de protocole</span><span class="sxs-lookup"><span data-stu-id="29ae8-109">Protocol name(s)</span></span> | <span data-ttu-id="29ae8-110">ATMPROTO \_ AAL5, ATMPROTO \_ AALUSER</span><span class="sxs-lookup"><span data-stu-id="29ae8-110">ATMPROTO\_AAL5, ATMPROTO\_AALUSER</span></span>                                                                                                                           |
| <span data-ttu-id="29ae8-111">Description</span><span class="sxs-lookup"><span data-stu-id="29ae8-111">Description</span></span>      | <span data-ttu-id="29ae8-112">La couche AAL5 ATM fournit un service de transport qui est orienté connexion, limite de message conservée et QOS garantie.</span><span class="sxs-lookup"><span data-stu-id="29ae8-112">ATM AAL5 provides a transport service that is connection oriented, message-boundary preserved, and QOS guaranteed.</span></span> <span data-ttu-id="29ae8-113">ATMPROTO \_ AALUSER est une AAL définie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="29ae8-113">ATMPROTO\_AALUSER is a user-defined AAL.</span></span> |
| <span data-ttu-id="29ae8-114">Famille d’adresses</span><span class="sxs-lookup"><span data-stu-id="29ae8-114">Address family</span></span>   | <span data-ttu-id="29ae8-115">\_ATM AF</span><span class="sxs-lookup"><span data-stu-id="29ae8-115">AF\_ATM</span></span>                                                                                                                                                     |
| <span data-ttu-id="29ae8-116">Fichier d’en-tête</span><span class="sxs-lookup"><span data-stu-id="29ae8-116">Header file</span></span>      | <span data-ttu-id="29ae8-117">Ws2atm. h</span><span class="sxs-lookup"><span data-stu-id="29ae8-117">Ws2atm.h</span></span>                                                                                                                                                    |



 

<span data-ttu-id="29ae8-118">Cette section décrit les extensions spécifiques au mode de transfert asynchrone (ATM) nécessaires pour prendre en charge les services ATM natifs tels qu’ils sont exposés et spécifiés dans la spécification de l’interface réseau utilisateur du Forum ATM version 3. x (3,0 et 3,1).</span><span class="sxs-lookup"><span data-stu-id="29ae8-118">This section describes the Asynchronous Transfer Mode (ATM)-specific extensions needed to support the native ATM services as exposed and specified in the ATM Forum User Network Interface (UNI) specification version 3.x (3.0 and 3.1).</span></span> <span data-ttu-id="29ae8-119">Ce document prend en charge AAL type 5 (mode message) et AAL défini par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="29ae8-119">This document supports AAL type 5 (message mode) and user-defined AAL.</span></span> <span data-ttu-id="29ae8-120">Les versions ultérieures de ce document prendront en charge d’autres types de AAL et UNI 4,0.</span><span class="sxs-lookup"><span data-stu-id="29ae8-120">Future versions of this document will support other types of AAL as well as UNI 4.0.</span></span>

 

 



