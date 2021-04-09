---
description: WSPGetSockName est utilisé pour récupérer l’adresse locale pour les sockets liés.
ms.assetid: 5f3c9aa8-97fe-48a1-a3f5-156c9bddb1b2
title: Détermination des noms locaux et distants
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 265cf8013dcadaedbef786ab78f48e63de81a992
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033984"
---
# <a name="determining-local-and-remote-names"></a><span data-ttu-id="17597-103">Détermination des noms locaux et distants</span><span class="sxs-lookup"><span data-stu-id="17597-103">Determining Local and Remote Names</span></span>

<span data-ttu-id="17597-104">[**WSPGetSockName**](/previous-versions/windows/desktop/legacy/ms742280(v=vs.85)) est utilisé pour récupérer l’adresse locale pour les sockets liés.</span><span class="sxs-lookup"><span data-stu-id="17597-104">[**WSPGetSockName**](/previous-versions/windows/desktop/legacy/ms742280(v=vs.85)) is used to retrieve the local address for bound sockets.</span></span> <span data-ttu-id="17597-105">Cela s’avère particulièrement utile lorsqu’un appel [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85)) a été effectué sans commencer par [**WSPBind**](/previous-versions/windows/hardware/network/ff566268(v=vs.85)) . **WSPGetSockName** fournit le seul moyen de déterminer l’association locale qui a été définie implicitement par le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="17597-105">This is especially useful when a [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85)) call has been made without doing a [**WSPBind**](/previous-versions/windows/hardware/network/ff566268(v=vs.85)) first; **WSPGetSockName** provides the only means to determine the local association which has been set implicitly by the provider.</span></span>

<span data-ttu-id="17597-106">Une fois la connexion configurée, [**WSPGetPeerName**](/previous-versions/windows/desktop/legacy/ms742278(v=vs.85)) peut être utilisé pour déterminer l’adresse de l’homologue auquel un socket est connecté.</span><span class="sxs-lookup"><span data-stu-id="17597-106">After a connection has been set up, [**WSPGetPeerName**](/previous-versions/windows/desktop/legacy/ms742278(v=vs.85)) can be used to determine the address of the peer to which a socket is connected.</span></span>

 

 
