---
description: Les systèmes Windows peuvent avoir plusieurs instances du type d’objet TrustedDomain.
ms.assetid: 13efedb5-ebb6-459b-8c4f-06774226278c
title: Type d’objet TrustedDomain
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70f0a4e6eca0790d877a9a23e4d83725d4e80798
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750860"
---
# <a name="the-trusteddomain-object-type"></a><span data-ttu-id="1e44b-103">Type d’objet TrustedDomain</span><span class="sxs-lookup"><span data-stu-id="1e44b-103">The TrustedDomain Object Type</span></span>

<span data-ttu-id="1e44b-104">Les systèmes Windows peuvent avoir plusieurs instances du type d’objet [**trustedDomain**](trusteddomain-object.md) .</span><span class="sxs-lookup"><span data-stu-id="1e44b-104">Windows-based systems can have multiple instances of the [**TrustedDomain**](trusteddomain-object.md) object type.</span></span> <span data-ttu-id="1e44b-105">Les objets **trustedDomain** ont deux champs qui doivent être uniques parmi tous les objets **trustedDomain** :</span><span class="sxs-lookup"><span data-stu-id="1e44b-105">**TrustedDomain** objects have two fields that must be unique among all **TrustedDomain** objects:</span></span>

-   <span data-ttu-id="1e44b-106">Nom du [ **trustedDomain**](trusteddomain-object.md)</span><span class="sxs-lookup"><span data-stu-id="1e44b-106">The name of the [**TrustedDomain**](trusteddomain-object.md)</span></span>
-   <span data-ttu-id="1e44b-107">[*Identificateur de sécurité*](/windows/desktop/SecGloss/s-gly) (SID) du [**trustedDomain**](trusteddomain-object.md).</span><span class="sxs-lookup"><span data-stu-id="1e44b-107">The [*security identifier*](/windows/desktop/SecGloss/s-gly) (SID) of the [**TrustedDomain**](trusteddomain-object.md).</span></span>

<span data-ttu-id="1e44b-108">Une tentative de création d’un nouvel objet **trustedDomain** avec un nom ou un SID qui est déjà utilisé par un autre objet **trustedDomain** est rejetée.</span><span class="sxs-lookup"><span data-stu-id="1e44b-108">An attempt to create a new **TrustedDomain** object with either a name or SID that is already in use by another **TrustedDomain** object will be rejected.</span></span>

 

 
