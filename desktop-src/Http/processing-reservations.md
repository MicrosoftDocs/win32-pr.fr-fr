---
title: Traitement des réservations
description: Les réservations pour des parties de l’espace de noms d’URL sont effectuées par l’administrateur système et placées dans le magasin de réservation persistant.
ms.assetid: deab6323-d114-463b-a0e7-acd173149b63
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a0a78fd6d374ede14e0eba7c1b22ad33ba50648
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/20/2020
ms.locfileid: "104383211"
---
# <a name="processing-reservations"></a><span data-ttu-id="a63ef-103">Traitement des réservations</span><span class="sxs-lookup"><span data-stu-id="a63ef-103">Processing Reservations</span></span>

<span data-ttu-id="a63ef-104">Les réservations pour des parties de l’espace de noms d’URL sont effectuées par l’administrateur système et placées dans le magasin de réservation persistant.</span><span class="sxs-lookup"><span data-stu-id="a63ef-104">Reservations for portions of the URL namespace are made by the system administrator and placed in the persistent reservation store.</span></span> <span data-ttu-id="a63ef-105">La racine de l’espace de noms URL pour HTTP appartient à l’administrateur système.</span><span class="sxs-lookup"><span data-stu-id="a63ef-105">The root of the URL namespace for HTTP is owned by the system administrator.</span></span> <span data-ttu-id="a63ef-106">Pour toutes les valeurs d’hôte et de port, les deux réservations suivantes sont toujours supposées à la racine de l’espace de noms **relativeUri** .</span><span class="sxs-lookup"><span data-stu-id="a63ef-106">For all host and port values, the following two reservations are always assumed at the root of the **relativeUri** namespace.</span></span>



| <span data-ttu-id="a63ef-107">Espace de noms réservé</span><span class="sxs-lookup"><span data-stu-id="a63ef-107">Namespace reserved</span></span>                 | <span data-ttu-id="a63ef-108">Réservé pour</span><span class="sxs-lookup"><span data-stu-id="a63ef-108">Reserved for</span></span>              |
|------------------------------------|---------------------------|
| <span data-ttu-id="a63ef-109"> https:// <host> :<port>/</span><span class="sxs-lookup"><span data-stu-id="a63ef-109">https://<host>:<port>/</span></span>  | <span data-ttu-id="a63ef-110">Administrateur LocalSystem</span><span class="sxs-lookup"><span data-stu-id="a63ef-110">LocalSystem Administrator</span></span> |
| <span data-ttu-id="a63ef-111"> https:// <host> :<port>/</span><span class="sxs-lookup"><span data-stu-id="a63ef-111">https://<host>:<port>/</span></span> | <span data-ttu-id="a63ef-112">Administrateur LocalSystem</span><span class="sxs-lookup"><span data-stu-id="a63ef-112">LocalSystem Administrator</span></span> |



 

<span data-ttu-id="a63ef-113">Ces réservations implicites ne peuvent pas être supprimées.</span><span class="sxs-lookup"><span data-stu-id="a63ef-113">These implicit reservations cannot be removed.</span></span> <span data-ttu-id="a63ef-114">Toutefois, il est possible de déléguer des réservations racines explicites à d’autres utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="a63ef-114">However, it is possible to delegate explicit root reservations to other users.</span></span> <span data-ttu-id="a63ef-115">Les réservations comme ci-dessous créent des délégations de ce type :</span><span class="sxs-lookup"><span data-stu-id="a63ef-115">Reservations such as the following would create such delegations:</span></span>



| <span data-ttu-id="a63ef-116">Espace de noms réservé</span><span class="sxs-lookup"><span data-stu-id="a63ef-116">Namespace reserved</span></span>        | <span data-ttu-id="a63ef-117">Réservé pour</span><span class="sxs-lookup"><span data-stu-id="a63ef-117">Reserved for</span></span> |
|---------------------------|--------------|
| `https://+:80/`           | <span data-ttu-id="a63ef-118">UtilisateurA, UtilisateurC reprennent</span><span class="sxs-lookup"><span data-stu-id="a63ef-118">UserA, UserC</span></span> |
| `https://adatum.com:443/` | <span data-ttu-id="a63ef-119">Login</span><span class="sxs-lookup"><span data-stu-id="a63ef-119">UserB</span></span>        |



 

<span data-ttu-id="a63ef-120">Si ces réservations déléguées sont supprimées par l’administrateur système, la propriété de l’espace de noms revient à la réservation implicite pour les valeurs d’hôte et de port correspondantes.</span><span class="sxs-lookup"><span data-stu-id="a63ef-120">If these delegated reservations are removed by the system administrator, ownership of the namespace reverts to the implicit reservation for the corresponding host and port values.</span></span>

 

 




