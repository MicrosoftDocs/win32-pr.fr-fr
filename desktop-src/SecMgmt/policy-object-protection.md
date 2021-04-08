---
description: Décrit comment l’objet de stratégie est protégé par défaut.
ms.assetid: e2d65ebf-5fbd-4e25-9862-a8188abb5492
title: Protection des objets de stratégie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 802fea6ce37a070c8230c3c9993df78a45f439bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750892"
---
# <a name="policy-object-protection"></a><span data-ttu-id="6966f-103">Protection des objets de stratégie</span><span class="sxs-lookup"><span data-stu-id="6966f-103">Policy Object Protection</span></span>

<span data-ttu-id="6966f-104">L’objet de [**stratégie**](policy-object.md) est protégé par défaut avec les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="6966f-104">The [**Policy**](policy-object.md) object is protected by default with the following settings:</span></span>

-   <span data-ttu-id="6966f-105">Le monde du groupe local dispose d’un \_ accès d’exécution générique.</span><span class="sxs-lookup"><span data-stu-id="6966f-105">The local group WORLD has GENERIC\_EXECUTE access.</span></span>
-   <span data-ttu-id="6966f-106">Le système d’ID connu reçoit la stratégie \_ tout \_ accès.</span><span class="sxs-lookup"><span data-stu-id="6966f-106">The well-known ID System is granted POLICY\_ALL\_ACCESS.</span></span>
-   <span data-ttu-id="6966f-107">L’administrateur LOCAL du groupe local dispose d’un \_ \_ accès générique en lecture, en \_ écriture générique et en \_ Exécution générique.</span><span class="sxs-lookup"><span data-stu-id="6966f-107">The local group LOCAL\_ADMIN has GENERIC\_READ, GENERIC\_WRITE, and GENERIC\_EXECUTE access.</span></span>
-   <span data-ttu-id="6966f-108">L’administrateur LOCAL du groupe \_ est affecté en tant que propriétaire et groupe principal de cet objet.</span><span class="sxs-lookup"><span data-stu-id="6966f-108">The group LOCAL\_ADMIN is assigned as owner and primary group of this object.</span></span>

<span data-ttu-id="6966f-109">Impossible de créer ou de détruire l’objet de [**stratégie**](policy-object.md) .</span><span class="sxs-lookup"><span data-stu-id="6966f-109">The [**Policy**](policy-object.md) object cannot be created or destroyed.</span></span>

 

 



