---
title: Actualisation d’un objet dynamique
description: Un client peut actualiser la durée de vie (TTL, Time to Live) d’une entrée de répertoire donnée pour la maintenir active de l’une des deux façons d’effectuer une mise à jour LDAP sur la valeur de son attribut entryTTL avant que l’entrée ne soit récupérée par le garbage collector.
ms.assetid: 5f51013c-b278-4ef7-a235-b238eed79a35
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7866c423fcb715289793a7beefa564150954257
ms.sourcegitcommit: 4d6ff888fd5825e78bc8fd5cdb21d4b542205039
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/18/2020
ms.locfileid: "106509482"
---
# <a name="refreshing-a-dynamic-object"></a><span data-ttu-id="212a1-103">Actualisation d’un objet dynamique</span><span class="sxs-lookup"><span data-stu-id="212a1-103">Refreshing a Dynamic Object</span></span>

<span data-ttu-id="212a1-104">Un client peut actualiser la durée de vie (TTL) d’une entrée de répertoire donnée pour la garder active de deux manières :</span><span class="sxs-lookup"><span data-stu-id="212a1-104">A client can refresh the Time To Live (TTL) of a given directory entry to keep it alive in one of two ways:</span></span>

-   <span data-ttu-id="212a1-105">Exécution d’une mise à jour LDAP de la valeur de son attribut **entryTTL** avant que l’entrée ne soit récupérée par le garbage collector.</span><span class="sxs-lookup"><span data-stu-id="212a1-105">Performing an LDAP update to the value of its **entryTTL** attribute before the entry is garbage collected.</span></span> <span data-ttu-id="212a1-106">Cette méthode d’actualisation d’une entrée dynamique dans l’annuaire est une fonctionnalité supplémentaire (facultative) de Active Directory Domain Services qui n’est pas spécifiée par la RFC 2589.</span><span class="sxs-lookup"><span data-stu-id="212a1-106">This method of refreshing a dynamic entry in the directory is an additional (optional) feature of Active Directory Domain Services that is not specified by RFC 2589.</span></span>
-   <span data-ttu-id="212a1-107">Exécution d’une opération LDAP étendue avec un OID de 1.3.6.1.4.1.1466.101.119.1 pour l’actualisation de la durée de vie, comme stipulé dans le document RFC 2589.</span><span class="sxs-lookup"><span data-stu-id="212a1-107">Performing an LDAP extended operation with an OID of 1.3.6.1.4.1.1466.101.119.1 for TTL refresh, as stipulated in the RFC 2589.</span></span> <span data-ttu-id="212a1-108">Cet OID est défini comme **LDAP \_ TTL \_ Extended \_ op \_ OID** dans WINLDAP. H.</span><span class="sxs-lookup"><span data-stu-id="212a1-108">This OID is defined as **LDAP\_TTL\_EXTENDED\_OP\_OID** in WINLDAP.H.</span></span>

 
<span data-ttu-id="212a1-109">\* \* ReMark \* \* \* : les objets dynamiques sont supprimés par le garbage collector lorsqu’ils ont expiré, aucune phase de l’objet n’est un objet tombstone lorsqu’il a expiré.</span><span class="sxs-lookup"><span data-stu-id="212a1-109">\*\*Remark\*\*\*: Dynamic objects are removed by Garbage Collector when they have expired, there is no phase of the object being a tombstone when it has expired.</span></span> <span data-ttu-id="212a1-110">Vous devez faire attention à la latence de réplication Active Directory lorsque vous actualisez des objets.</span><span class="sxs-lookup"><span data-stu-id="212a1-110">You need to be careful with the AD replication latency when you refresh objects.</span></span> <span data-ttu-id="212a1-111">Vous devez vous assurer que la mise à jour pour actualiser la durée de vie arrive suffisamment tôt pour que tous les réplicas du contexte d’appellation (catalogue complet et catalogue global) voient la transaction d’actualisation avant l’expiration locale de l’objet.</span><span class="sxs-lookup"><span data-stu-id="212a1-111">You have to ensure that the update to refresh the TTL arrives early enough so all replicas of the naming context (full and global catalog) see the refresh transaction before the object expires locally.</span></span>

 




