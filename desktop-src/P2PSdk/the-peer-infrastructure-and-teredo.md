---
description: Un utilisateur peut vérifier l’état de l’interface Teredo à partir de l’invite de commandes en tapant netsh interface teredo show State et en examinant la sortie.
ms.assetid: b6ac1708-fb8a-449b-b30f-c889688a4bac
title: L’infrastructure homologue et Teredo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2550d8da46339205de60c4a537d03c10940da4b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104529121"
---
# <a name="the-peer-infrastructure-and-teredo"></a><span data-ttu-id="a8731-103">L’infrastructure homologue et Teredo</span><span class="sxs-lookup"><span data-stu-id="a8731-103">The Peer Infrastructure and Teredo</span></span>

<span data-ttu-id="a8731-104">Un utilisateur peut vérifier l’état de l’interface [Teredo](https://msdn.microsoft.com/library/ms819742.aspx) à partir de l’invite de commandes en tapant **netsh interface teredo show State** et en examinant la sortie.</span><span class="sxs-lookup"><span data-stu-id="a8731-104">A user can check the status of the [Teredo](https://msdn.microsoft.com/library/ms819742.aspx) interface from the command prompt by typing **netsh interface teredo show state** and examining the output.</span></span> <span data-ttu-id="a8731-105">Si l’État est « hors connexion », Teredo n’est pas actif, ce qui empêche l’utilisateur de se connecter à d’autres utilisateurs via leurs adresses Teredo.</span><span class="sxs-lookup"><span data-stu-id="a8731-105">If the state is "offline", Teredo is not active, which prevents the user from connecting to other users via their Teredo addresses.</span></span> <span data-ttu-id="a8731-106">Il est possible que Teredo soit hors connexion, car votre pare-feu est désactivé ou ne prend pas en charge [IPv6](/previous-versions/windows/embedded/ms898970(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="a8731-106">It is possible Teredo may be offline because your firewall is disabled or does not support [IPv6](/previous-versions/windows/embedded/ms898970(v=msdn.10)).</span></span>

 

 
