---
description: Les ordinateurs personnels exécutant Microsoft Windows ont souvent de nombreuses connexions réseau, telles que plusieurs cartes d’interface réseau (NIC) connectées à différents réseaux, ou une connexion réseau physique et une connexion d’accès à distance.
ms.assetid: 73a1999d-0c19-4f9d-8e47-07f819874535
title: Fournisseur d’emplacement réseau (NLA)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91d3b5882b63539ce0299c9d4a2d93dc17ef2576
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113027"
---
# <a name="network-location-awareness-service-provider-nla"></a><span data-ttu-id="b046f-103">Fournisseur d’emplacement réseau (NLA)</span><span class="sxs-lookup"><span data-stu-id="b046f-103">Network Location Awareness Service Provider (NLA)</span></span>

<span data-ttu-id="b046f-104">Les ordinateurs personnels exécutant Microsoft Windows ont souvent de nombreuses connexions réseau, telles que plusieurs cartes d’interface réseau (NIC) connectées à différents réseaux, ou une connexion réseau physique et une connexion d’accès à distance.</span><span class="sxs-lookup"><span data-stu-id="b046f-104">Personal computers running Microsoft Windows often have numerous network connections, such as multiple network interface cards (NIC) connected to different networks, or a physical network connection and a dial-up connection.</span></span> <span data-ttu-id="b046f-105">Windows Sockets a été en capacité d’énumérer les interfaces réseau disponibles pendant un certain temps, mais certaines informations critiques sur les connexions réseau n’étaient pas disponibles auparavant.</span><span class="sxs-lookup"><span data-stu-id="b046f-105">Windows Sockets has been capable of enumerating available network interfaces for some time, but certain critical information about network connections was previously unavailable.</span></span> <span data-ttu-id="b046f-106">Cela comprend des informations telles que le réseau logique auquel un ordinateur Windows est attaché ou si plusieurs interfaces sont connectées au même réseau.</span><span class="sxs-lookup"><span data-stu-id="b046f-106">This includes information such as the logical network to which a Windows computer is attached or whether multiple interfaces are connected to the same network.</span></span>

<span data-ttu-id="b046f-107">Le fournisseur de service de reconnaissance d’emplacement réseau, communément appelé NLA, permet aux applications Windows Sockets 2 d’identifier le réseau logique auquel un ordinateur Windows est attaché.</span><span class="sxs-lookup"><span data-stu-id="b046f-107">The Network Location Awareness service provider, commonly referred to as NLA, enables Windows Sockets 2 applications to identify the logical network to which a Windows computer is attached.</span></span> <span data-ttu-id="b046f-108">En outre, NLA permet aux applications Windows Sockets d’identifier l’interface réseau physique à laquelle une application donnée a enregistré des informations spécifiques.</span><span class="sxs-lookup"><span data-stu-id="b046f-108">In addition, NLA enables Windows Sockets applications to identify to which physical network interface a given application has saved specific information.</span></span> <span data-ttu-id="b046f-109">NLA est implémentée en tant que fournisseur de services de résolution de noms Windows Sockets 2 générique.</span><span class="sxs-lookup"><span data-stu-id="b046f-109">NLA is implemented as a generic Windows Sockets 2 Name Resolution service provider.</span></span>

 

 



