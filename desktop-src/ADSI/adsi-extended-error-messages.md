---
title: Messages d’erreur étendus ADSI
description: Cette rubrique contient une liste de rubriques qui expliquent comment utiliser les messages d’erreur ADSI retournés par IADs, IADsContainer, IDirectoryObject et IDirectorySearch.
ms.assetid: cfec86cb-fe90-4e2b-8c9d-06e175253fa4
ms.tgt_platform: multiple
keywords:
- Messages d’erreur étendus ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab374f18892c0ff336ef588dce477db60405ab19
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028577"
---
# <a name="adsi-extended-error-messages"></a><span data-ttu-id="4254e-104">Messages d’erreur étendus ADSI</span><span class="sxs-lookup"><span data-stu-id="4254e-104">ADSI Extended Error Messages</span></span>

<span data-ttu-id="4254e-105">Outre les valeurs **HRESULT** , plusieurs fournisseurs de système ADSI (principalement LDAP) renvoient des données d’erreur supplémentaires pour les opérations effectuées par les interfaces suivantes :</span><span class="sxs-lookup"><span data-stu-id="4254e-105">Apart from the **HRESULT** values, several ADSI system providers (mostly LDAP) return additional error data for operations performed by the following interfaces:</span></span>

-   [<span data-ttu-id="4254e-106">**IADs**</span><span class="sxs-lookup"><span data-stu-id="4254e-106">**IADs**</span></span>](/windows/desktop/api/Iads/nn-iads-iads)
-   [<span data-ttu-id="4254e-107">**IADsContainer**</span><span class="sxs-lookup"><span data-stu-id="4254e-107">**IADsContainer**</span></span>](/windows/desktop/api/Iads/nn-iads-iadscontainer)
-   [<span data-ttu-id="4254e-108">**IDirectoryObject**</span><span class="sxs-lookup"><span data-stu-id="4254e-108">**IDirectoryObject**</span></span>](/windows/desktop/api/Iads/nn-iads-idirectoryobject)
-   [<span data-ttu-id="4254e-109">**Rubrique IDirectorySearch**</span><span class="sxs-lookup"><span data-stu-id="4254e-109">**IDirectorySearch**</span></span>](/windows/desktop/api/Iads/nn-iads-idirectorysearch)

<span data-ttu-id="4254e-110">Une partie de ces données d’erreur étendues est la chaîne envoyée par le serveur dans le cadre du résultat du message.</span><span class="sxs-lookup"><span data-stu-id="4254e-110">A part of such extended error data is the string sent by the server as a part of the message result.</span></span>

<span data-ttu-id="4254e-111">Appelez [**ADsGetLastError**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetlasterror) pour récupérer ces messages d’erreur étendus.</span><span class="sxs-lookup"><span data-stu-id="4254e-111">Call [**ADsGetLastError**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetlasterror) to retrieve such extended error messages.</span></span> <span data-ttu-id="4254e-112">Le premier paramètre de cette fonction, *lpError*, est une valeur **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="4254e-112">The first parameter of this function, *lpError*, is a **DWORD** value.</span></span> <span data-ttu-id="4254e-113">Pour un serveur Active Directory, ADSI tente de mapper un message d’erreur LDAP à un code d’erreur Win32 approprié et attribue la valeur de code d’erreur Win32 à *lpError*.</span><span class="sxs-lookup"><span data-stu-id="4254e-113">For an Active Directory server, ADSI attempts to map an LDAP error message to an appropriate Win32 error code and assigns the Win32 error code value to *lpError*.</span></span> <span data-ttu-id="4254e-114">Si le mappage n’est pas résolu, ADSI affecte des **\_ \_ données non valides** à *lpError*, comme c’est le cas pour tout autre serveur d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="4254e-114">Failing to resolve the mapping, ADSI assigns **ERROR\_INVALID\_DATA** to *lpError*, as it does for any other directory server.</span></span> <span data-ttu-id="4254e-115">Dans tous les cas, ADSI relaie fidèlement la chaîne de la description d’erreur du serveur au client par le biais de *lpErrorBuf*, le deuxième paramètre de la fonction **ADsGetLastError** .</span><span class="sxs-lookup"><span data-stu-id="4254e-115">In all cases, ADSI faithfully relays the string of the error description from the server to the client through *lpErrorBuf*, the second parameter of the **ADsGetLastError** function.</span></span>

 

 




