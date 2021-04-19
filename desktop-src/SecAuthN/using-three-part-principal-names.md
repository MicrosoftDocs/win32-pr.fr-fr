---
description: Lorsque vous créez un package de sécurité SSP (Security Support Provider), vous ne devez pas autoriser le client joint à un domaine à s’authentifier auprès d’un contrôleur de domaine à l’aide d’un nom de fournisseur de services (SPN) en deux parties sous la forme suivante.
ms.assetid: 6CD3BC5E-F9B2-4E8E-9DEE-064AE8837DFB
title: Utilisation de trois noms principaux de parties
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8760ba740843c62c39a98e7e4683d25410a94ec4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515834"
---
# <a name="using-three-part-principal-names"></a><span data-ttu-id="96aff-103">Utilisation de trois noms principaux de parties</span><span class="sxs-lookup"><span data-stu-id="96aff-103">Using Three Part Principal Names</span></span>

<span data-ttu-id="96aff-104">Lorsque vous créez un package de sécurité SSP (Security Support Provider), vous ne devez pas autoriser le client joint à un domaine à s’authentifier auprès d’un contrôleur de domaine à l’aide d’un nom de fournisseur de services (SPN) en deux parties sous la forme suivante.</span><span class="sxs-lookup"><span data-stu-id="96aff-104">When creating a security support provider (SSP) security package, you should not allow the domain joined client to authenticate to a domain controller by using a two part service provider name (SPN) of the following form.</span></span>

-   <span data-ttu-id="96aff-105"><*protocole* >/< *nom d’hôte*></span><span class="sxs-lookup"><span data-stu-id="96aff-105"><*protocol*>/<*host name*></span></span>

<span data-ttu-id="96aff-106">Un client doit toujours s’authentifier en spécifiant le domaine.</span><span class="sxs-lookup"><span data-stu-id="96aff-106">A client should always authenticate by specifying the domain.</span></span>

-   <span data-ttu-id="96aff-107"><*protocole* >/< *nom* >/< d’hôte *nom de domaine*></span><span class="sxs-lookup"><span data-stu-id="96aff-107"><*protocol*>/<*host name*>/<*domain name*></span></span>

<span data-ttu-id="96aff-108">Un client joint à un domaine qui se connecte avec un SPN en deux parties peut être en mesure d’emprunter l’identité du contrôleur de domaine.</span><span class="sxs-lookup"><span data-stu-id="96aff-108">A domain joined client that logs on with a two part SPN may be able to impersonate the domain controller.</span></span> <span data-ttu-id="96aff-109">Si vous autorisez deux noms de principal du service (SPN), vous devez créer une entrée de journal qui contient suffisamment d’informations pour permettre à l’administrateur d’identifier l’appelant.</span><span class="sxs-lookup"><span data-stu-id="96aff-109">If you allow two part SPNs, you should create a log entry that contains enough information to enable the administrator to identify the caller.</span></span>

 

 



