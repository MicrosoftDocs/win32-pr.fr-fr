---
description: Pour établir une connexion entre un client et un serveur à l’aide du protocole SMB Microsoft, vous devez d’abord déterminer le dialecte avec le plus haut niveau de fonctionnalité pris en charge par le client et le serveur.
ms.assetid: ad48391b-fcc7-4e58-83bb-6084503c8d61
title: Dialectes du protocole SMB Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f35d3fbcaa3345e2981df797f115e88064e38f04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484729"
---
# <a name="microsoft-smb-protocol-dialects"></a><span data-ttu-id="dc0fe-103">Dialectes du protocole SMB Microsoft</span><span class="sxs-lookup"><span data-stu-id="dc0fe-103">Microsoft SMB Protocol Dialects</span></span>

<span data-ttu-id="dc0fe-104">La liste des paquets de messages du protocole SMB Microsoft a augmenté au fil des années pour s’adapter aux fonctionnalités croissantes du protocole SMB de Microsoft, ainsi qu’aux centaines.</span><span class="sxs-lookup"><span data-stu-id="dc0fe-104">The list of Microsoft SMB Protocol message packets has grown over the years to accommodate the increasing functionality of Microsoft SMB Protocol, and now numbers in the hundreds.</span></span> <span data-ttu-id="dc0fe-105">Chaque étape de sa croissance est marquée par un ensemble de paquets standard ou un dialecte.</span><span class="sxs-lookup"><span data-stu-id="dc0fe-105">Each stage of its growth is marked by a standard packet set, or dialect.</span></span> <span data-ttu-id="dc0fe-106">Chaque dialecte est identifié par une chaîne standard telle que « PC NETWORK PROGRAM 1,0 », « MICROSOFT NETWORKs 3,0 », « DOS LANMAN 2,1 » ou « NT LM 0,12 ».</span><span class="sxs-lookup"><span data-stu-id="dc0fe-106">Each dialect is identified by a standard string such as "PC NETWORK PROGRAM 1.0", "MICROSOFT NETWORKS 3.0", "DOS LANMAN 2.1", or "NT LM 0.12".</span></span> <span data-ttu-id="dc0fe-107">La première chaîne identifie le premier dialecte de SMB, et la dernière chaîne identifie CIFS, le premier dialecte du protocole SMB Microsoft.</span><span class="sxs-lookup"><span data-stu-id="dc0fe-107">The first string identifies the first dialect of SMB, and the last string identifies CIFS, the first dialect of Microsoft SMB Protocol.</span></span>

<span data-ttu-id="dc0fe-108">La plupart des clients Windows prennent en charge au moins six dialectes différents du protocole SMB de Microsoft. par conséquent, l’une des premières étapes de l’établissement d’une connexion entre un client et un serveur à l’aide du protocole SMB Microsoft consiste à déterminer le dialecte avec le plus haut niveau de fonctionnalité pris en charge par le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="dc0fe-108">Most Windows clients support at least six different dialects of Microsoft SMB Protocol, so one of the first steps in establishing a connection between a client and a server using Microsoft SMB Protocol is to determine the dialect with the highest level of functionality that both the client and server support.</span></span> <span data-ttu-id="dc0fe-109">Ce processus est appelé « négociation du dialecte ».</span><span class="sxs-lookup"><span data-stu-id="dc0fe-109">This process is known as "negotiating the dialect."</span></span> <span data-ttu-id="dc0fe-110">Les chaînes de dialectes mentionnées ci-dessus sont incluses dans les paquets de demande et de réponse de négociation de dialecte à cet effet.</span><span class="sxs-lookup"><span data-stu-id="dc0fe-110">The dialect strings mentioned above are included in the dialect negotiation request and response packets for this purpose.</span></span>

 

 



