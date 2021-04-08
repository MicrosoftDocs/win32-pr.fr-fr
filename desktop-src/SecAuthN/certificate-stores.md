---
description: Les certificats client et serveur doivent être stockés dans un magasin de certificats accessible par le processus d’application.
ms.assetid: 3be91b9b-ecc0-4cf2-88ca-77fd25d2dafc
title: Magasin de certificats
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ba46318f095c78e7813ed962e066fd7e4650126
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034265"
---
# <a name="certificate-stores"></a><span data-ttu-id="07d58-103">Magasin de certificats</span><span class="sxs-lookup"><span data-stu-id="07d58-103">Certificate Stores</span></span>

<span data-ttu-id="07d58-104">Les certificats [*client*](/windows/desktop/SecGloss/c-gly) et [*serveur*](/windows/desktop/SecGloss/s-gly) doivent être stockés dans un [*magasin de certificats*](/windows/desktop/SecGloss/c-gly) accessible par le processus d’application.</span><span class="sxs-lookup"><span data-stu-id="07d58-104">Both [*client*](/windows/desktop/SecGloss/c-gly) and [*server certificates*](/windows/desktop/SecGloss/s-gly) must be stored in a [*certificate store*](/windows/desktop/SecGloss/c-gly) accessible by the application process.</span></span> <span data-ttu-id="07d58-105">En règle générale, il s’agit du magasin mon magasin, également appelé magasin personnel.</span><span class="sxs-lookup"><span data-stu-id="07d58-105">Typically, this is the My store, also known as the personal store.</span></span> <span data-ttu-id="07d58-106">Les applications clientes telles qu’Internet Explorer utilisent normalement le magasin mon magasin de l’utilisateur actuel, tandis que les serveurs tels que Internet Information Services (IIS) utilisent le magasin mon magasin de l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="07d58-106">Client applications such as Internet Explorer normally use the My store of the current user while servers such as Internet Information Services (IIS) use the system My store of the local computer.</span></span>

<span data-ttu-id="07d58-107">Le magasin racine et le magasin de l' [*autorité de certification*](/windows/desktop/SecGloss/c-gly) sont utilisés lorsque Schannel ou une application génère une chaîne de certificats à envoyer à l’ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="07d58-107">The Root store and the [*certification authority*](/windows/desktop/SecGloss/c-gly) (CA) store are used when Schannel or an application builds a certificate chain to be sent to the remote computer.</span></span> <span data-ttu-id="07d58-108">Ces magasins sont utilisés pour valider une chaîne de certificats reçue.</span><span class="sxs-lookup"><span data-stu-id="07d58-108">These stores are used to validate a received certificate chain.</span></span> <span data-ttu-id="07d58-109">Pour plus d’informations, consultez [exécution de l’authentification à l’aide de Schannel](performing-authentication-using-schannel.md).</span><span class="sxs-lookup"><span data-stu-id="07d58-109">For more information, see [Performing Authentication Using Schannel](performing-authentication-using-schannel.md).</span></span>

 

 
