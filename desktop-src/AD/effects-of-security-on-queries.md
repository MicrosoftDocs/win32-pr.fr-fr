---
title: Effets de la sécurité sur la recherche
description: La sécurité est un filtre implicite lors de l’exécution de recherches, de l’énumération des conteneurs ou de la lecture des propriétés.
ms.assetid: 4a027069-8c3d-4a95-a04b-c9c59200a9ed
ms.tgt_platform: multiple
keywords:
- effets de la sécurité sur la recherche Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26feee840c0668b2ea9412932a27927bb1c00012
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671333"
---
# <a name="effects-of-security-on-searching"></a><span data-ttu-id="73a70-104">Effets de la sécurité sur la recherche</span><span class="sxs-lookup"><span data-stu-id="73a70-104">Effects of Security on Searching</span></span>

<span data-ttu-id="73a70-105">La sécurité est un filtre implicite lors de l’exécution de recherches, de l’énumération des conteneurs ou de la lecture des propriétés.</span><span class="sxs-lookup"><span data-stu-id="73a70-105">Security is an implicit filter when performing searches, enumerating containers, or reading properties.</span></span>

<span data-ttu-id="73a70-106">ADSI ne peut retourner \_ aucune \_ propriété de ce type ou aucune \_ \_ erreur d’objet, même lorsque l’objet existe si vous n’avez pas accès à des attributs de lecture sur l’objet.</span><span class="sxs-lookup"><span data-stu-id="73a70-106">ADSI can return NO\_SUCH\_PROPERTY or NO\_SUCH\_OBJECT errors even when the object exists if you do not have access to read attributes on the object.</span></span>

<span data-ttu-id="73a70-107">Par exemple, un appelant peut être en mesure d’énumérer les objets enfants dans un conteneur, car l’appelant a \_ des droits de liste de contenu sur le conteneur.</span><span class="sxs-lookup"><span data-stu-id="73a70-107">For example, a caller may be able to enumerate the child objects in a container because the caller has LIST\_CONTENTS rights on the container.</span></span> <span data-ttu-id="73a70-108">Toutefois, il se peut que le même appelant ne puisse pas accéder aux objets énumérés si l’appelant n’a pas d’accès en lecture aux objets enfants.</span><span class="sxs-lookup"><span data-stu-id="73a70-108">But the same caller may not be able to access the enumerated objects if the caller does not have read access to the child objects.</span></span> <span data-ttu-id="73a70-109">Dans ce cas, une requête pour un objet enfant peut retourner un \_ objet de ce type, \_ même si l’appelant a énuméré correctement l’objet.</span><span class="sxs-lookup"><span data-stu-id="73a70-109">In this case, a query for a child object may return NO\_SUCH\_OBJECT even though the caller successfully enumerated the object.</span></span>

<span data-ttu-id="73a70-110">Si l’appelant ne dispose pas de droits suffisants, les codes de retour suivants peuvent être retournés :</span><span class="sxs-lookup"><span data-stu-id="73a70-110">If the caller does not have sufficient rights, the following return codes may be returned:</span></span>

<span data-ttu-id="73a70-111">\_objet domaine E ADS \_ non valide \_ \_</span><span class="sxs-lookup"><span data-stu-id="73a70-111">E\_ADS\_INVALID\_DOMAIN\_OBJECT</span></span>

<span data-ttu-id="73a70-112">\_propriété E \_ ADS \_ non \_ prise en charge</span><span class="sxs-lookup"><span data-stu-id="73a70-112">E\_ADS\_PROPERTY\_NOT\_SUPPORTED</span></span>

<span data-ttu-id="73a70-113">\_propriété ADS \_ E \_ \_ introuvable</span><span class="sxs-lookup"><span data-stu-id="73a70-113">E\_ADS\_PROPERTY\_NOT\_FOUND</span></span>

 

 




