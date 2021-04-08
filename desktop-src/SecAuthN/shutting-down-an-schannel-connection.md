---
description: Arrêt d’une connexion Schannel
ms.assetid: 7081ba1f-df3c-41b4-96da-24d44e74d714
title: Arrêt d’une connexion Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc61b67083ceee65da714069c2b30ba1bfd5c89b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749604"
---
# <a name="shutting-down-an-schannel-connection"></a><span data-ttu-id="80a5c-103">Arrêt d’une connexion Schannel</span><span class="sxs-lookup"><span data-stu-id="80a5c-103">Shutting Down an Schannel Connection</span></span>

<span data-ttu-id="80a5c-104">Lorsqu’un client ou un serveur se termine avec une connexion, il doit l’arrêter.</span><span class="sxs-lookup"><span data-stu-id="80a5c-104">When a client or server is finished with a connection, it must shut it down.</span></span> <span data-ttu-id="80a5c-105">L’autre partie doit, à son tour, reconnaître l’arrêt et supprimer la connexion.</span><span class="sxs-lookup"><span data-stu-id="80a5c-105">The other party, in turn, must recognize the shutdown and delete the connection.</span></span>

<span data-ttu-id="80a5c-106">**Pour arrêter une connexion Schannel**</span><span class="sxs-lookup"><span data-stu-id="80a5c-106">**To shut down an Schannel connection**</span></span>

1.  <span data-ttu-id="80a5c-107">Appelez la fonction [**ApplyControlToken**](/windows/desktop/api/Sspi/nf-sspi-applycontroltoken) , en spécifiant le \_ jeton de contrôle d’arrêt Schannel.</span><span class="sxs-lookup"><span data-stu-id="80a5c-107">Call the [**ApplyControlToken**](/windows/desktop/api/Sspi/nf-sspi-applycontroltoken) function, specifying the SCHANNEL\_SHUTDOWN control token.</span></span>
2.  <span data-ttu-id="80a5c-108">Après avoir reçu une \_ \_ valeur de retour s E OK de [**ApplyControlToken**](/windows/desktop/api/Sspi/nf-sspi-applycontroltoken), appelez la fonction [**InitializeSecurityContext (SChannel)**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) (clients) ou [**AcceptSecurityContext (SChannel)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) (serveurs), en passant dans des mémoires tampons vides.</span><span class="sxs-lookup"><span data-stu-id="80a5c-108">After receiving an SEC\_E\_OK return value from [**ApplyControlToken**](/windows/desktop/api/Sspi/nf-sspi-applycontroltoken), call the [**InitializeSecurityContext (Schannel)**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) (clients) or [**AcceptSecurityContext (Schannel)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) (servers) function, passing in empty buffers.</span></span>
3.  <span data-ttu-id="80a5c-109">Procédez comme si votre application était en train de créer une nouvelle connexion jusqu’à ce que la fonction retourne SEC \_ I \_ Context \_ expiré ou sec \_ e \_ OK pour indiquer que la connexion est arrêtée.</span><span class="sxs-lookup"><span data-stu-id="80a5c-109">Proceed as though your application were creating a new connection until the function returns SEC\_I\_CONTEXT\_EXPIRED or SEC\_E\_OK to indicate that the connection is shut down.</span></span>
4.  <span data-ttu-id="80a5c-110">Envoyer les informations de sortie finales, le cas échéant, au tiers distant.</span><span class="sxs-lookup"><span data-stu-id="80a5c-110">Send the final output information, if any, to the remote party.</span></span>
5.  <span data-ttu-id="80a5c-111">Appelez [**DeleteSecurityContext**](/windows/desktop/api/Sspi/nf-sspi-deletesecuritycontext) pour libérer les ressources détenues par la connexion.</span><span class="sxs-lookup"><span data-stu-id="80a5c-111">Call [**DeleteSecurityContext**](/windows/desktop/api/Sspi/nf-sspi-deletesecuritycontext) to free resources held by the connection.</span></span>

## <a name="recognizing-a-shutdown"></a><span data-ttu-id="80a5c-112">Reconnaissance d’un arrêt</span><span class="sxs-lookup"><span data-stu-id="80a5c-112">Recognizing a Shutdown</span></span>

<span data-ttu-id="80a5c-113">La fonction [**DecryptMessage (SChannel)**](/windows/win32/api/sspi/nf-sspi-decryptmessage) retourne le \_ contexte sec I \_ \_ expiré lorsque l’expéditeur du message a arrêté la connexion.</span><span class="sxs-lookup"><span data-stu-id="80a5c-113">The [**DecryptMessage (Schannel)**](/windows/win32/api/sspi/nf-sspi-decryptmessage) function returns SEC\_I\_CONTEXT\_EXPIRED when the message sender has shut down the connection.</span></span> <span data-ttu-id="80a5c-114">Après avoir reçu cette valeur de retour, suivez la procédure pour arrêter une connexion Schannel, plus haut dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="80a5c-114">After receiving this return value, follow the procedure To shut down an Schannel connection, earlier in this topic.</span></span>

 

 
