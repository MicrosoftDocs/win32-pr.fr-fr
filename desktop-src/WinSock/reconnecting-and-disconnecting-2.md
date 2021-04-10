---
description: La destination par défaut peut être modifiée en rappelant simplement WSPConnect, même si le socket est déjà connecté. Les datagrammes mis en file d’attente pour la réception sont ignorés si la nouvelle adresse est différente de l’adresse spécifiée dans un WSPConnect précédent.
ms.assetid: b5f5ab97-03bd-4f5c-8808-d14ad5a56a5a
title: Reconnexion et déconnexion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7babefe03be44f942ee60a840aa210ee3c0e25da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864042"
---
# <a name="reconnecting-and-disconnecting"></a><span data-ttu-id="aa62a-104">Reconnexion et déconnexion</span><span class="sxs-lookup"><span data-stu-id="aa62a-104">Reconnecting and Disconnecting</span></span>

<span data-ttu-id="aa62a-105">La destination par défaut peut être modifiée en rappelant simplement [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85)) , même si le socket est déjà connecté.</span><span class="sxs-lookup"><span data-stu-id="aa62a-105">The default destination may be changed by simply calling [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85)) again, even if the socket is already connected.</span></span> <span data-ttu-id="aa62a-106">Les datagrammes mis en file d’attente pour la réception sont ignorés si la nouvelle adresse est différente de l’adresse spécifiée dans un **WSPConnect** précédent.</span><span class="sxs-lookup"><span data-stu-id="aa62a-106">Any datagrams queued for receipt are discarded if the new address is different from the address specified in a previous **WSPConnect**.</span></span>

<span data-ttu-id="aa62a-107">Si l’adresse fournie pour le socket n’est que des zéros, le socket est déconnecté. l’adresse distante par défaut est indéterminée, de sorte que les appels [**WSPSend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85)) et [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) retournent le code d’erreur WSAENOTCONN, bien que [**WSPSendTo**](/previous-versions/windows/desktop/legacy/ms742291(v=vs.85)) et [**WSPRecvFrom**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85)) puissent toujours être utilisés.</span><span class="sxs-lookup"><span data-stu-id="aa62a-107">If the address supplied for the socket is all zeros, the socket will be disconnected — the default remote address will be indeterminate, so [**WSPSend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85)) and [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) calls will return the error code WSAENOTCONN, although [**WSPSendTo**](/previous-versions/windows/desktop/legacy/ms742291(v=vs.85)) and [**WSPRecvFrom**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85)) may still be used.</span></span>

 

 
