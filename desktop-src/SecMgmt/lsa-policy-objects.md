---
description: L’autorité LSA stocke les informations de stratégie de sécurité locale dans un ensemble d’objets. Votre application peut interroger ou modifier la stratégie de sécurité locale en accédant à ces objets.
ms.assetid: c8ed5cd8-55cf-43e7-92a3-9bd17a1147a9
title: Objets de stratégie LSA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1481b6a6f49e973ecc2a2e1b53830bf22c67a77f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952109"
---
# <a name="lsa-policy-objects"></a><span data-ttu-id="0d96b-104">Objets de stratégie LSA</span><span class="sxs-lookup"><span data-stu-id="0d96b-104">LSA Policy Objects</span></span>

<span data-ttu-id="0d96b-105">L’autorité LSA stocke les informations de stratégie de sécurité locale dans un ensemble d’objets.</span><span class="sxs-lookup"><span data-stu-id="0d96b-105">The LSA stores local security policy information in a set of objects.</span></span> <span data-ttu-id="0d96b-106">Votre application peut interroger ou modifier la stratégie de sécurité locale en accédant à ces objets.</span><span class="sxs-lookup"><span data-stu-id="0d96b-106">Your application can query or edit the local security policy by accessing these objects.</span></span>

<span data-ttu-id="0d96b-107">L’ensemble se compose des quatre objets suivants :</span><span class="sxs-lookup"><span data-stu-id="0d96b-107">The set consists of the following four objects:</span></span>

-   <span data-ttu-id="0d96b-108">La [stratégie](policy-object.md) contient des informations de stratégie globale.</span><span class="sxs-lookup"><span data-stu-id="0d96b-108">[Policy](policy-object.md) contains global policy information.</span></span>
-   <span data-ttu-id="0d96b-109">[TrustedDomain](trusteddomain-object.md) contient des informations sur un domaine approuvé.</span><span class="sxs-lookup"><span data-stu-id="0d96b-109">[TrustedDomain](trusteddomain-object.md) contains information about a trusted domain.</span></span>
-   <span data-ttu-id="0d96b-110">Le [compte](account-object.md) contient des informations sur un compte d’utilisateur, de groupe ou de groupe local.</span><span class="sxs-lookup"><span data-stu-id="0d96b-110">[Account](account-object.md) contains information about a user, group, or local group account.</span></span>
-   <span data-ttu-id="0d96b-111">Les [données privées](private-data-object.md) contiennent des informations protégées, telles que des mots de passe de compte de serveur.</span><span class="sxs-lookup"><span data-stu-id="0d96b-111">[Private Data](private-data-object.md) contains protected information, such as server account passwords.</span></span> <span data-ttu-id="0d96b-112">Ces informations sont stockées sous forme de chaînes chiffrées.</span><span class="sxs-lookup"><span data-stu-id="0d96b-112">This information is stored as encrypted strings.</span></span>

<span data-ttu-id="0d96b-113">Pour plus d’informations sur l’utilisation des fonctions de stratégie LSA pour gérer les informations stockées dans ces objets, consultez Utilisation de la [stratégie LSA](using-lsa-policy.md).</span><span class="sxs-lookup"><span data-stu-id="0d96b-113">For more information on how to use the LSA Policy functions to manage the information stored in these objects, see [Using LSA Policy](using-lsa-policy.md).</span></span>

 

 



