---
description: PNRP utilise la fonction WSANSPIoctl pour recevoir des notifications sur les modifications apportées aux éléments suivants.
ms.assetid: e5509be1-5294-4696-ab5b-fa2217ae0956
title: PNRP et WSANSPIoctl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c36dc53fb3d00eeaa2b74be643a7ea62af436e93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544864"
---
# <a name="pnrp-and-wsanspioctl"></a><span data-ttu-id="8fd62-103">PNRP et WSANSPIoctl</span><span class="sxs-lookup"><span data-stu-id="8fd62-103">PNRP and WSANSPIoctl</span></span>

<span data-ttu-id="8fd62-104">PNRP utilise la fonction [**WSANSPIoctl**](winsock-nsp-reference-links.md) pour recevoir des notifications sur les modifications apportées aux éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="8fd62-104">PNRP uses the [**WSANSPIoctl**](winsock-nsp-reference-links.md) function to receive notifications about changes to the following:</span></span>

-   <span data-ttu-id="8fd62-105">Liste de clouds réseau</span><span class="sxs-lookup"><span data-stu-id="8fd62-105">A network cloud list</span></span>
-   <span data-ttu-id="8fd62-106">Disponibilité des résultats d’une demande de résolution de noms</span><span class="sxs-lookup"><span data-stu-id="8fd62-106">Availability of results of a name resolution request</span></span>

<span data-ttu-id="8fd62-107">Le premier appel à [**WSALookupServiceBegin**](winsock-nsp-reference-links.md) définit le type d’informations sur lequel un client est averti.</span><span class="sxs-lookup"><span data-stu-id="8fd62-107">The first call to [**WSALookupServiceBegin**](winsock-nsp-reference-links.md) defines the type of information that a client is notified about.</span></span> <span data-ttu-id="8fd62-108">Un client peut être notifié à l’aide d’un message Windows, d’une routine de saisie semi-automatique, d’un handle vers un objet WSAEVENT ou d’un port.</span><span class="sxs-lookup"><span data-stu-id="8fd62-108">A client can be notified with a Windows message, a completion routine, a handle to a WSAEVENT object, or a port.</span></span> <span data-ttu-id="8fd62-109">Pour plus d’informations sur les options et la définition du paramètre *lpCompletion* , consultez **WSANSPIoctl**.</span><span class="sxs-lookup"><span data-stu-id="8fd62-109">For more information about options and setting the *lpCompletion* parameter, see **WSANSPIoctl**.</span></span>

<span data-ttu-id="8fd62-110">Pour continuer à recevoir des notifications après un appel à [**WSALookupServiceNext**](winsock-nsp-reference-links.md), une application doit à nouveau appeler **WSANSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="8fd62-110">To continue receiving notifications after a call to [**WSALookupServiceNext**](winsock-nsp-reference-links.md), an application must call **WSANSPIoctl** again.</span></span>

<span data-ttu-id="8fd62-111">La fonction [**WSALookupServiceNext**](winsock-nsp-reference-links.md) se bloque même si **WSANSPIoctl** est appelé.</span><span class="sxs-lookup"><span data-stu-id="8fd62-111">The [**WSALookupServiceNext**](winsock-nsp-reference-links.md) function blocks even if **WSANSPIoctl** is called.</span></span> <span data-ttu-id="8fd62-112">Avant d’appeler **WSALookupServiceNext**, une application doit attendre jusqu’à ce qu’elle reçoive une notification, si le blocage est un problème.</span><span class="sxs-lookup"><span data-stu-id="8fd62-112">Before calling **WSALookupServiceNext**, an application must wait until it receives a notification—if blocking is an issue.</span></span>

<span data-ttu-id="8fd62-113">Lors de l’appel de cette fonction, les paramètres doivent avoir les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="8fd62-113">When calling this function, the parameters must have the following values:</span></span>

<dl> <dt>

<span data-ttu-id="8fd62-114"><span id="hLookup"></span><span id="hlookup"></span><span id="HLOOKUP"></span>*Fonction*</span><span class="sxs-lookup"><span data-stu-id="8fd62-114"><span id="hLookup"></span><span id="hlookup"></span><span id="HLOOKUP"></span>*hLookup*</span></span>
</dt> <dd>

<span data-ttu-id="8fd62-115">Spécifie le handle retourné par [**WSALookupServiceBegin**](winsock-nsp-reference-links.md) .</span><span class="sxs-lookup"><span data-stu-id="8fd62-115">Specifies the handle that [**WSALookupServiceBegin**](winsock-nsp-reference-links.md) returns.</span></span>

</dd> <dt>

<span data-ttu-id="8fd62-116"><span id="dwControlCode"></span><span id="dwcontrolcode"></span><span id="DWCONTROLCODE"></span>*dwControlCode*</span><span class="sxs-lookup"><span data-stu-id="8fd62-116"><span id="dwControlCode"></span><span id="dwcontrolcode"></span><span id="DWCONTROLCODE"></span>*dwControlCode*</span></span>
</dt> <dd>

<span data-ttu-id="8fd62-117">Doit être **SIO \_ NSP \_ notifier la \_ modification**.</span><span class="sxs-lookup"><span data-stu-id="8fd62-117">Must be **SIO\_NSP\_NOTIFY\_CHANGE**.</span></span>

</dd> <dt>

<span data-ttu-id="8fd62-118"><span id="lpvInBuffer"></span><span id="lpvinbuffer"></span><span id="LPVINBUFFER"></span>*lpvInBuffer*</span><span class="sxs-lookup"><span data-stu-id="8fd62-118"><span id="lpvInBuffer"></span><span id="lpvinbuffer"></span><span id="LPVINBUFFER"></span>*lpvInBuffer*</span></span>
</dt> <dd>

<span data-ttu-id="8fd62-119">Doit avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="8fd62-119">Must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="8fd62-120"><span id="cbInBuffer"></span><span id="cbinbuffer"></span><span id="CBINBUFFER"></span>*cbInBuffer*</span><span class="sxs-lookup"><span data-stu-id="8fd62-120"><span id="cbInBuffer"></span><span id="cbinbuffer"></span><span id="CBINBUFFER"></span>*cbInBuffer*</span></span>
</dt> <dd>

<span data-ttu-id="8fd62-121">Doit être égal à zéro (0).</span><span class="sxs-lookup"><span data-stu-id="8fd62-121">Must be zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="8fd62-122"><span id="lpvOutBuffer"></span><span id="lpvoutbuffer"></span><span id="LPVOUTBUFFER"></span>*lpvOutBuffer*</span><span class="sxs-lookup"><span data-stu-id="8fd62-122"><span id="lpvOutBuffer"></span><span id="lpvoutbuffer"></span><span id="LPVOUTBUFFER"></span>*lpvOutBuffer*</span></span>
</dt> <dd>

<span data-ttu-id="8fd62-123">Doit avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="8fd62-123">Must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="8fd62-124"><span id="cbOutBuffer"></span><span id="cboutbuffer"></span><span id="CBOUTBUFFER"></span>*cbOutBuffer*</span><span class="sxs-lookup"><span data-stu-id="8fd62-124"><span id="cbOutBuffer"></span><span id="cboutbuffer"></span><span id="CBOUTBUFFER"></span>*cbOutBuffer*</span></span>
</dt> <dd>

<span data-ttu-id="8fd62-125">Doit être égal à zéro (0).</span><span class="sxs-lookup"><span data-stu-id="8fd62-125">Must be zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="8fd62-126"><span id="lpcbBytesReturned"></span><span id="lpcbbytesreturned"></span><span id="LPCBBYTESRETURNED"></span>*lpcbBytesReturned*</span><span class="sxs-lookup"><span data-stu-id="8fd62-126"><span id="lpcbBytesReturned"></span><span id="lpcbbytesreturned"></span><span id="LPCBBYTESRETURNED"></span>*lpcbBytesReturned*</span></span>
</dt> <dd>

<span data-ttu-id="8fd62-127">Doit avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="8fd62-127">Must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="8fd62-128"><span id="lpCompletion"></span><span id="lpcompletion"></span><span id="LPCOMPLETION"></span>*lpCompletion*</span><span class="sxs-lookup"><span data-stu-id="8fd62-128"><span id="lpCompletion"></span><span id="lpcompletion"></span><span id="LPCOMPLETION"></span>*lpCompletion*</span></span>
</dt> <dd>

<span data-ttu-id="8fd62-129">Spécifie une **valeur null** ou un pointeur vers une structure [**WSACOMPLETION**](winsock-nsp-reference-links.md) .</span><span class="sxs-lookup"><span data-stu-id="8fd62-129">Specifies either **NULL** or a pointer to a [**WSACOMPLETION**](winsock-nsp-reference-links.md) structure.</span></span>

</dd> </dl>

<span data-ttu-id="8fd62-130">Une fois la notification reçue, appelez [**WSALookupServiceNext**](winsock-nsp-reference-links.md) une fois pour obtenir les résultats.</span><span class="sxs-lookup"><span data-stu-id="8fd62-130">After a notification is received, call [**WSALookupServiceNext**](winsock-nsp-reference-links.md) one time to obtain the results.</span></span>

<span data-ttu-id="8fd62-131">Pour mettre fin à une recherche, appelez [**WSALookupServiceEnd**](winsock-nsp-reference-links.md).</span><span class="sxs-lookup"><span data-stu-id="8fd62-131">To end a search, call [**WSALookupServiceEnd**](winsock-nsp-reference-links.md).</span></span>

## <a name="resolution-notifications"></a><span data-ttu-id="8fd62-132">Notifications de résolution</span><span class="sxs-lookup"><span data-stu-id="8fd62-132">Resolution Notifications</span></span>

<span data-ttu-id="8fd62-133">Un client peut être notifié à chaque fois qu’une entrée de résolution de nom est ajoutée.</span><span class="sxs-lookup"><span data-stu-id="8fd62-133">A client can be notified any time that a name resolution entry is added.</span></span> <span data-ttu-id="8fd62-134">Le client appelle ensuite [**WSALookupServiceNext**](winsock-nsp-reference-links.md) pour obtenir les données de résolution.</span><span class="sxs-lookup"><span data-stu-id="8fd62-134">The client then calls [**WSALookupServiceNext**](winsock-nsp-reference-links.md) to obtain the resolution data.</span></span>

<span data-ttu-id="8fd62-135">Si le client n’utilise pas cette technique, un appel à [**WSALookupServiceNext**](winsock-nsp-reference-links.md) peut être bloqué jusqu’à ce que le délai d’attente spécifié se produise.</span><span class="sxs-lookup"><span data-stu-id="8fd62-135">If the client does not use this technique, a call to [**WSALookupServiceNext**](winsock-nsp-reference-links.md) can be blocked until the specified timeout occurs.</span></span>

## <a name="cloud-list-notifications"></a><span data-ttu-id="8fd62-136">Notifications de liste de clouds</span><span class="sxs-lookup"><span data-stu-id="8fd62-136">Cloud List Notifications</span></span>

<span data-ttu-id="8fd62-137">Un client peut être averti chaque fois qu’une modification est apportée à un ensemble de clouds.</span><span class="sxs-lookup"><span data-stu-id="8fd62-137">A client can be notified any time there is a change to a set of clouds.</span></span>

<span data-ttu-id="8fd62-138">La fonction [**WSALookupServiceNext**](winsock-nsp-reference-links.md) retourne le **WSA \_ E \_ \_** plus comme délimiteur défini.</span><span class="sxs-lookup"><span data-stu-id="8fd62-138">The [**WSALookupServiceNext**](winsock-nsp-reference-links.md) function returns **WSA\_E\_NO\_MORE** as a set delimiter.</span></span> <span data-ttu-id="8fd62-139">L’application cliente doit énumérer les clouds existants jusqu’à ce que ce message soit retourné, puis utiliser un schéma de notification pour récupérer les modifications ultérieures à mesure qu’elles se produisent.</span><span class="sxs-lookup"><span data-stu-id="8fd62-139">The client application must enumerate existing clouds until this message is returned, and then use a notification scheme to retrieve subsequent changes as they occur.</span></span> <span data-ttu-id="8fd62-140">Une application cliente peut également appeler **WSALookupServiceNext**, mais l’appel est bloqué jusqu’à ce qu’une modification se produise.</span><span class="sxs-lookup"><span data-stu-id="8fd62-140">A client application can also call **WSALookupServiceNext**, but the call is blocked until a change occurs.</span></span>

<span data-ttu-id="8fd62-141">La fonction [**WSALookupServiceNext**](winsock-nsp-reference-links.md) retourne un Cloud dans une structure **WSAQUERYSET** .</span><span class="sxs-lookup"><span data-stu-id="8fd62-141">The [**WSALookupServiceNext**](winsock-nsp-reference-links.md) function returns a cloud in a **WSAQUERYSET** structure.</span></span> <span data-ttu-id="8fd62-142">L’un des indicateurs suivants est retourné dans le membre **dwOutputFlags** .</span><span class="sxs-lookup"><span data-stu-id="8fd62-142">One of the following flags is returned in the **dwOutputFlags** member.</span></span>



| <span data-ttu-id="8fd62-143">Valeur</span><span class="sxs-lookup"><span data-stu-id="8fd62-143">Value</span></span>               | <span data-ttu-id="8fd62-144">Description</span><span class="sxs-lookup"><span data-stu-id="8fd62-144">Description</span></span>                                             |
|---------------------|---------------------------------------------------------|
| <span data-ttu-id="8fd62-145">le résultat \_ est \_ ajouté</span><span class="sxs-lookup"><span data-stu-id="8fd62-145">RESULT\_IS\_ADDED</span></span>   | <span data-ttu-id="8fd62-146">Le Cloud retourné est ajouté.</span><span class="sxs-lookup"><span data-stu-id="8fd62-146">The cloud that is returned is added.</span></span>                    |
| <span data-ttu-id="8fd62-147">RÉSULTAT \_ \_ modifié</span><span class="sxs-lookup"><span data-stu-id="8fd62-147">RESULT\_IS\_CHANGED</span></span> | <span data-ttu-id="8fd62-148">Le Cloud retourné est modifié.</span><span class="sxs-lookup"><span data-stu-id="8fd62-148">The cloud that is returned is changed.</span></span>                  |
| <span data-ttu-id="8fd62-149">le résultat \_ est \_ supprimé</span><span class="sxs-lookup"><span data-stu-id="8fd62-149">RESULT\_IS\_DELETED</span></span> | <span data-ttu-id="8fd62-150">Le Cloud retourné est supprimé et n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="8fd62-150">The cloud that is returned is deleted and is not valid.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="8fd62-151">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8fd62-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8fd62-152">PNRP et WSALookupServiceBegin</span><span class="sxs-lookup"><span data-stu-id="8fd62-152">PNRP and WSALookupServiceBegin</span></span>](pnrp-and-wsalookupservicebegin.md)
</dt> <dt>

[<span data-ttu-id="8fd62-153">PNRP et WSALookupServiceEnd</span><span class="sxs-lookup"><span data-stu-id="8fd62-153">PNRP and WSALookupServiceEnd</span></span>](pnrp-and-wsalookupserviceend.md)
</dt> <dt>

[<span data-ttu-id="8fd62-154">PNRP et WSAQUERYSET</span><span class="sxs-lookup"><span data-stu-id="8fd62-154">PNRP and WSAQUERYSET</span></span>](pnrp-and-wsaqueryset.md)
</dt> <dt>

[<span data-ttu-id="8fd62-155">Codes d’erreur du NSP PNRP</span><span class="sxs-lookup"><span data-stu-id="8fd62-155">PNRP NSP Error Codes</span></span>](pnrp-nsp-error-codes.md)
</dt> <dt>

[<span data-ttu-id="8fd62-156">**WSANSPIoctl**</span><span class="sxs-lookup"><span data-stu-id="8fd62-156">**WSANSPIoctl**</span></span>](winsock-nsp-reference-links.md)
</dt> <dt>

<span data-ttu-id="8fd62-157">**WSALookupServiceBegin**</span><span class="sxs-lookup"><span data-stu-id="8fd62-157">**WSALookupServiceBegin**</span></span>
</dt> <dt>

<span data-ttu-id="8fd62-158">**WSALookupServiceEnd**</span><span class="sxs-lookup"><span data-stu-id="8fd62-158">**WSALookupServiceEnd**</span></span>
</dt> <dt>

<span data-ttu-id="8fd62-159">**WSAQUERYSET**</span><span class="sxs-lookup"><span data-stu-id="8fd62-159">**WSAQUERYSET**</span></span>
</dt> </dl>

 

 



