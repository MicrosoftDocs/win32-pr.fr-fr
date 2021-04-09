---
title: Autres informations de connexion
description: Les membres de la structure RASDIALPARAMS peuvent également spécifier les informations de connexion suivantes.
ms.assetid: 95a8dd78-e424-4d0b-899a-69deb9e1b9cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea4d006cd3cb31d5dc7229043b2a8ef169c22d76
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941098"
---
# <a name="other-connection-information"></a><span data-ttu-id="af686-103">Autres informations de connexion</span><span class="sxs-lookup"><span data-stu-id="af686-103">Other Connection Information</span></span>

<span data-ttu-id="af686-104">Les membres de la structure [**RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) peuvent également spécifier les informations de connexion suivantes.</span><span class="sxs-lookup"><span data-stu-id="af686-104">The members of the [**RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) structure can also specify the following connection information.</span></span>

-   <span data-ttu-id="af686-105">Un numéro de téléphone pour remplacer le numéro dans l’entrée de l’annuaire téléphonique.</span><span class="sxs-lookup"><span data-stu-id="af686-105">A phone number to override the number in the phone-book entry.</span></span>
-   <span data-ttu-id="af686-106">Numéro de téléphone de [rappel](callback-connections.md) que le serveur distant peut rappeler pour établir la connexion.</span><span class="sxs-lookup"><span data-stu-id="af686-106">A [callback](callback-connections.md) phone number that the remote server can call back to establish the connection.</span></span>
-   <span data-ttu-id="af686-107">Nom du domaine de réseau distant sur lequel l’authentification doit se produire.</span><span class="sxs-lookup"><span data-stu-id="af686-107">The name of the remote network domain on which the authentication is to occur.</span></span>

<span data-ttu-id="af686-108">Pour le numéro de rappel et le domaine, les membres [**RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) peuvent indiquer que le service d’accès à distance doit utiliser les informations de l’entrée de l’annuaire téléphonique, ou il peut fournir des informations qui remplacent les données de l’annuaire téléphonique.</span><span class="sxs-lookup"><span data-stu-id="af686-108">For the callback number and the domain, the [**RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) members can either indicate that RAS should use the information in the phone-book entry, or it can provide information that overrides the phone-book data.</span></span>

<span data-ttu-id="af686-109">Un client RAS peut utiliser le paramètre *lpRasDialExtensions* de la fonction [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) pour déterminer si RAS utilise un préfixe ou un suffixe de numéro de téléphone spécifié dans une entrée d’annuaire téléphonique.</span><span class="sxs-lookup"><span data-stu-id="af686-109">A RAS client can use the *lpRasDialExtensions* parameter of the [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) function to control whether RAS uses a phone number prefix or suffix specified in a phone-book entry.</span></span>

 

 