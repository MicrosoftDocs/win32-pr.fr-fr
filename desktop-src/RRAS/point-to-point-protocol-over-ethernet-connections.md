---
title: protocole PPP des connexions Ethernet
description: Windows Server 2003, Windows XP et les systèmes d’exploitation ultérieurs fournissent une prise en charge de protocole PPP sur Ethernet (PPPoE). Pour une connexion PPPoE, définissez les valeurs suivantes dans la structure RASENTRY.
ms.assetid: abdbf22c-abeb-4363-bfa6-e0002d1637f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eed66d3a694896bdec9e0f53215a782d5896cd38
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941291"
---
# <a name="point-to-point-protocol-over-ethernet-connections"></a><span data-ttu-id="aac9a-104">protocole PPP des connexions Ethernet</span><span class="sxs-lookup"><span data-stu-id="aac9a-104">Point-to-Point Protocol over Ethernet Connections</span></span>

<span data-ttu-id="aac9a-105">Windows Server 2003, Windows XP et les systèmes d’exploitation ultérieurs fournissent une prise en charge de protocole PPP sur Ethernet (PPPoE).</span><span class="sxs-lookup"><span data-stu-id="aac9a-105">Windows Server 2003, Windows XP, and later operating systems provide support for Point-to-Point Protocol over Ethernet (PPPoE).</span></span> <span data-ttu-id="aac9a-106">Pour une connexion PPPoE, définissez les valeurs suivantes dans la structure [**RASENTRY**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="aac9a-106">For a PPPoE connection, set the following values in the [**RASENTRY**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)) structure.</span></span>



| <span data-ttu-id="aac9a-107">Membre</span><span class="sxs-lookup"><span data-stu-id="aac9a-107">Member</span></span>                      | <span data-ttu-id="aac9a-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="aac9a-108">Value</span></span>             |
|-----------------------------|-------------------|
| <span data-ttu-id="aac9a-109">RASENTRY.dwType</span><span class="sxs-lookup"><span data-stu-id="aac9a-109">RASENTRY.dwType</span></span>             | <span data-ttu-id="aac9a-110">\_Haut débit RASET</span><span class="sxs-lookup"><span data-stu-id="aac9a-110">RASET\_Broadband</span></span>  |
| <span data-ttu-id="aac9a-111">RAENTRY.szDeviceType</span><span class="sxs-lookup"><span data-stu-id="aac9a-111">RAENTRY.szDeviceType</span></span>        | <span data-ttu-id="aac9a-112">RASDT \_ PPPoE</span><span class="sxs-lookup"><span data-stu-id="aac9a-112">RASDT\_PPPoE</span></span>      |
| <span data-ttu-id="aac9a-113">RASENTRY.szLocalPhoneNumber</span><span class="sxs-lookup"><span data-stu-id="aac9a-113">RASENTRY.szLocalPhoneNumber</span></span> | <span data-ttu-id="aac9a-114">Nom du service.</span><span class="sxs-lookup"><span data-stu-id="aac9a-114">The service name.</span></span> |



 

<span data-ttu-id="aac9a-115">Utilisez la fonction [**RasSetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) pour définir ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="aac9a-115">Use the [**RasSetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) function to set these values.</span></span>

<span data-ttu-id="aac9a-116">Vous pouvez également utiliser [**RasEntryDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) et l' \_ indicateur RASEDFLAG NewBroadbandEntry pour [**RasEntryDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) pour afficher un Assistant pour la création d’une entrée d’annuaire PPPoE.</span><span class="sxs-lookup"><span data-stu-id="aac9a-116">You can also use [**RasEntryDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) and the RASEDFLAG\_NewBroadbandEntry flag for [**RASENTRYDLG**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) to display a wizard for creating a PPPoE phonebook entry.</span></span>

 

 