---
title: Limitations de l’authentification mutuelle avec Kerberos
description: Le compte du client et le compte du service doivent être dans des domaines Windows 2000 natifs ou en mode mixte, car les services Kerberos ne sont pas disponibles dans les domaines de niveau inférieur.
ms.assetid: 54685e88-b289-4db9-b4cb-f5c22a216a0d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 290bd93050c9cb4c89052ce644b4c588f638f312
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462015"
---
# <a name="limitations-of-mutual-authentication-with-kerberos"></a><span data-ttu-id="36943-103">Limitations de l’authentification mutuelle avec Kerberos</span><span class="sxs-lookup"><span data-stu-id="36943-103">Limitations of Mutual Authentication with Kerberos</span></span>

<span data-ttu-id="36943-104">Le compte du client et le compte du service doivent être dans des domaines Windows 2000 natifs ou en mode mixte, car les services Kerberos ne sont pas disponibles dans les domaines de niveau inférieur.</span><span class="sxs-lookup"><span data-stu-id="36943-104">Both the client's account and the service's account must be in Windows 2000 native or mixed-mode domains because Kerberos services are not available in downlevel domains.</span></span> <span data-ttu-id="36943-105">En outre, les comptes de service et de client doivent se trouver dans la même forêt, car le KDC du client utilise le catalogue global pour rechercher le nom de principal du service.</span><span class="sxs-lookup"><span data-stu-id="36943-105">In addition, both client and service accounts must be in the same forest because the client's KDC uses the global catalog to search for the service principal name.</span></span>

<span data-ttu-id="36943-106">Le service et le client doivent s’exécuter sur Windows 2000. dans le cas contraire, l’authentification mutuelle avec Kerberos échouera, car les versions antérieures de Windows ne prendront pas en charge Kerberos.</span><span class="sxs-lookup"><span data-stu-id="36943-106">Both service and client must be running on Windows 2000, otherwise mutual authentication with Kerberos will fail because earlier versions of Windows do not support Kerberos.</span></span>

<span data-ttu-id="36943-107">Les noms de principal du service doivent inclure le nom DNS du serveur hôte sur lequel le service s’exécute.</span><span class="sxs-lookup"><span data-stu-id="36943-107">Service principal names must include the DNS name of the host server on which the service is running.</span></span> <span data-ttu-id="36943-108">Vous devez utiliser le nom DNS.</span><span class="sxs-lookup"><span data-stu-id="36943-108">You must use the DNS name.</span></span>

 

 




