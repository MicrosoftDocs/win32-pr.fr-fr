---
description: Explique comment les objets de compte sont protégés.
ms.assetid: a07ef46e-f4b6-4e21-bdd7-72d03e1c88b3
title: Protection des objets de compte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f495a3dc943ef73eef5074e0edc73247ceb02d09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521293"
---
# <a name="account-object-protection"></a><span data-ttu-id="bc606-103">Protection des objets de compte</span><span class="sxs-lookup"><span data-stu-id="bc606-103">Account Object Protection</span></span>

<span data-ttu-id="bc606-104">Les objets de [**compte**](account-object.md) sont protégés de la manière suivante :</span><span class="sxs-lookup"><span data-stu-id="bc606-104">[**Account**](account-object.md) objects are protected in the following fashion:</span></span>

-   <span data-ttu-id="bc606-105">Le **monde** du groupe a une \_ Exécution générique.</span><span class="sxs-lookup"><span data-stu-id="bc606-105">The group **WORLD** has GENERIC\_EXECUTE.</span></span>
-   <span data-ttu-id="bc606-106">L' **\_ administrateur local** du groupe a \_ accès en suppression, en lecture générique, en écriture générique, en \_ \_ Exécution générique et en écriture \_ DACL.</span><span class="sxs-lookup"><span data-stu-id="bc606-106">The group **LOCAL\_ADMIN** has DELETE, GENERIC\_READ, GENERIC\_WRITE, GENERIC\_EXECUTE, and WRITE\_DACL access.</span></span>
-   <span data-ttu-id="bc606-107">L' **\_ administrateur local** du groupe est affecté en tant que propriétaire et groupe principal d’objets de compte.</span><span class="sxs-lookup"><span data-stu-id="bc606-107">The group **LOCAL\_ADMIN** is assigned as owner and primary group of Account objects.</span></span>

 

 



