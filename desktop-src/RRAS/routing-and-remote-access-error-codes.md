---
title: Codes d’erreur de routage et d’accès distant
description: Les codes d’erreur de l’API de routage et d’accès à distance (RRAS) suivants sont définis dans raserror. h.
ms.assetid: 1fa41438-7c93-4e9c-851c-652fba23da4f
topic_type:
- apiref
api_name:
- Routing and Remote Access Error Codes
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 15966d009f0690a1db24c21460da5b9e08a38347
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032541"
---
# <a name="routing-and-remote-access-error-codes"></a><span data-ttu-id="346a3-103">Codes d’erreur de routage et d’accès distant</span><span class="sxs-lookup"><span data-stu-id="346a3-103">Routing and Remote Access Error Codes</span></span>

<span data-ttu-id="346a3-104">Les codes d’erreur de l’API de routage et d’accès à distance (RRAS) suivants sont définis dans raserror. h.</span><span class="sxs-lookup"><span data-stu-id="346a3-104">The following Routing and Remote Access (RRAS) API error codes are defined in raserror.h.</span></span> <span data-ttu-id="346a3-105">Tous les codes d’erreur sont pris en charge dans Windows 2000 ou les versions ultérieures de Windows, sauf indication contraire.</span><span class="sxs-lookup"><span data-stu-id="346a3-105">All error codes are supported in Windows 2000 or later versions of Windows unless specified otherwise.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="346a3-106">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="346a3-106">Return code/value</span></span></th>
<th><span data-ttu-id="346a3-107">Description</span><span class="sxs-lookup"><span data-stu-id="346a3-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="PENDING"></span><span id="pending"></span><dl> <span data-ttu-id="346a3-108"><dt><strong>En attente</strong></dt> <dt>600</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-108"><dt><strong>PENDING</strong></dt> <dt>600</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-109">Une opération est en attente.</span><span class="sxs-lookup"><span data-stu-id="346a3-109">An operation is pending.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_PORT_HANDLE"></span><span id="error_invalid_port_handle"></span><dl> <span data-ttu-id="346a3-110"><dt><strong>ERROR_INVALID_PORT_HANDLE</strong></dt> <dt>601</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-110"><dt><strong>ERROR_INVALID_PORT_HANDLE</strong></dt> <dt>601</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-111">Le descripteur de port fourni n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="346a3-111">The port handle supplied is not valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PORT_ALREADY_OPEN"></span><span id="error_port_already_open"></span><dl> <span data-ttu-id="346a3-112"><dt><strong>ERROR_PORT_ALREADY_OPEN</strong></dt> <dt>602</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-112"><dt><strong>ERROR_PORT_ALREADY_OPEN</strong></dt> <dt>602</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-113">Le port spécifié est déjà ouvert.</span><span class="sxs-lookup"><span data-stu-id="346a3-113">The specified port is already open.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_BUFFER_TOO_SMALL"></span><span id="error_buffer_too_small"></span><dl> <span data-ttu-id="346a3-114"><dt><strong>ERROR_BUFFER_TOO_SMALL</strong></dt> <dt>603</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-114"><dt><strong>ERROR_BUFFER_TOO_SMALL</strong></dt> <dt>603</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-115">La mémoire tampon fournie est trop petite.</span><span class="sxs-lookup"><span data-stu-id="346a3-115">The buffer supplied is too small.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_WRONG_INFO_SPECIFIED"></span><span id="error_wrong_info_specified"></span><dl> <span data-ttu-id="346a3-116"><dt><strong>ERROR_WRONG_INFO_SPECIFIED</strong></dt> <dt>604</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-116"><dt><strong>ERROR_WRONG_INFO_SPECIFIED</strong></dt> <dt>604</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-117">Les informations de port spécifiées sont incorrectes.</span><span class="sxs-lookup"><span data-stu-id="346a3-117">The port information specified is incorrect.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CANNOT_SET_PORT_INFO"></span><span id="error_cannot_set_port_info"></span><dl> <span data-ttu-id="346a3-118"><dt><strong>ERROR_CANNOT_SET_PORT_INFO</strong></dt> <dt>605</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-118"><dt><strong>ERROR_CANNOT_SET_PORT_INFO</strong></dt> <dt>605</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-119">Impossible de définir les informations de port spécifiées.</span><span class="sxs-lookup"><span data-stu-id="346a3-119">The port information specified cannot be set.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-120">Déconseillé dans Windows Vista et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-120">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PORT_NOT_CONNECTED"></span><span id="error_port_not_connected"></span><dl> <span data-ttu-id="346a3-121"><dt><strong>ERROR_PORT_NOT_CONNECTED</strong></dt> <dt>606</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-121"><dt><strong>ERROR_PORT_NOT_CONNECTED</strong></dt> <dt>606</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-122">Le port spécifié n’est pas connecté.</span><span class="sxs-lookup"><span data-stu-id="346a3-122">The port specified is not connected.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EVENT_INVALID"></span><span id="error_event_invalid"></span><dl> <span data-ttu-id="346a3-123"><dt><strong>ERROR_EVENT_INVALID</strong></dt> <dt>607</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-123"><dt><strong>ERROR_EVENT_INVALID</strong></dt> <dt>607</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-124">Un événement qui n’est pas valide a été détecté.</span><span class="sxs-lookup"><span data-stu-id="346a3-124">An event that is not valid was detected.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-125">Déconseillé dans Windows Vista et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-125">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DEVICE_DOES_NOT_EXIST"></span><span id="error_device_does_not_exist"></span><dl> <span data-ttu-id="346a3-126"><dt><strong>ERROR_DEVICE_DOES_NOT_EXIST</strong></dt> <dt>608</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-126"><dt><strong>ERROR_DEVICE_DOES_NOT_EXIST</strong></dt> <dt>608</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-127">L’appareil spécifié n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="346a3-127">The specified device does not exist.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_DEVICETYPE_DOES_NOT_EXIST"></span><span id="error_devicetype_does_not_exist"></span><dl> <span data-ttu-id="346a3-128"><dt><strong>ERROR_DEVICETYPE_DOES_NOT_EXIST</strong></dt> <dt>609</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-128"><dt><strong>ERROR_DEVICETYPE_DOES_NOT_EXIST</strong></dt> <dt>609</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-129">Le type d’appareil spécifié n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="346a3-129">The specified device type does not exist.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_BUFFER_INVALID"></span><span id="error_buffer_invalid"></span><dl> <span data-ttu-id="346a3-130"><dt><strong>ERROR_BUFFER_INVALID</strong></dt> <dt>610</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-130"><dt><strong>ERROR_BUFFER_INVALID</strong></dt> <dt>610</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-131">La mémoire tampon fournie n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="346a3-131">The buffer supplied is not valid.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_ROUTE_NOT_AVAILABLE"></span><span id="error_route_not_available"></span><dl> <span data-ttu-id="346a3-132"><dt><strong>ERROR_ROUTE_NOT_AVAILABLE</strong></dt> <dt>611</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-132"><dt><strong>ERROR_ROUTE_NOT_AVAILABLE</strong></dt> <dt>611</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-133">Un itinéraire spécifié n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="346a3-133">A route was specified that is not available.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-134">Déconseillé dans Windows Vista et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-134">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_ROUTE_NOT_ALLOCATED"></span><span id="error_route_not_allocated"></span><dl> <span data-ttu-id="346a3-135"><dt><strong>ERROR_ROUTE_NOT_ALLOCATED</strong></dt> <dt>612</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-135"><dt><strong>ERROR_ROUTE_NOT_ALLOCATED</strong></dt> <dt>612</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-136">L’itinéraire spécifié n’est pas alloué.</span><span class="sxs-lookup"><span data-stu-id="346a3-136">The specified route is not allocated.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERRERROR_INVALID_COMPRESSION_SPECIFIED"></span><span id="errerror_invalid_compression_specified"></span><dl> <span data-ttu-id="346a3-137"><dt><strong>ERRERROR_INVALID_COMPRESSION_SPECIFIED</strong></dt> <dt>613</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-137"><dt><strong>ERRERROR_INVALID_COMPRESSION_SPECIFIED</strong></dt> <dt>613</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-138">La compression spécifiée n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="346a3-138">The specified compression is not valid.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-139">Déconseillé dans Windows Vista et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-139">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_OUT_OF_BUFFERS"></span><span id="error_out_of_buffers"></span><dl> <span data-ttu-id="346a3-140"><dt><strong>ERROR_OUT_OF_BUFFERS</strong></dt> <dt>614</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-140"><dt><strong>ERROR_OUT_OF_BUFFERS</strong></dt> <dt>614</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-141">Les mémoires tampons sont insuffisantes.</span><span class="sxs-lookup"><span data-stu-id="346a3-141">There were insufficient buffers available.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PORT_NOT_FOUND_"></span><span id="error_port_not_found_"></span><dl> <span data-ttu-id="346a3-142"><dt> <strong>ERROR_PORT_NOT_FOUND</strong> </dt> <dt>615</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-142"><dt><strong>ERROR_PORT_NOT_FOUND</strong> </dt> <dt>615</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-143">Le port spécifié est introuvable.</span><span class="sxs-lookup"><span data-stu-id="346a3-143">The specified port was not found.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_ASYNC_REQUEST_PENDING"></span><span id="error_async_request_pending"></span><dl> <span data-ttu-id="346a3-144"><dt><strong>ERROR_ASYNC_REQUEST_PENDING</strong></dt> <dt>616</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-144"><dt><strong>ERROR_ASYNC_REQUEST_PENDING</strong></dt> <dt>616</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-145">Une demande asynchrone est en attente.</span><span class="sxs-lookup"><span data-stu-id="346a3-145">An asynchronous request is pending.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_ALREADY_DISCONNECTING"></span><span id="error_already_disconnecting"></span><dl> <span data-ttu-id="346a3-146"><dt><strong>ERROR_ALREADY_DISCONNECTING</strong></dt> <dt>617</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-146"><dt><strong>ERROR_ALREADY_DISCONNECTING</strong></dt> <dt>617</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-147">Le port ou l’appareil spécifié est déjà en cours de déconnexion.</span><span class="sxs-lookup"><span data-stu-id="346a3-147">The specified port or device is already disconnecting.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PORT_NOT_OPEN"></span><span id="error_port_not_open"></span><dl> <span data-ttu-id="346a3-148"><dt><strong>ERROR_PORT_NOT_OPEN</strong></dt> <dt>618</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-148"><dt><strong>ERROR_PORT_NOT_OPEN</strong></dt> <dt>618</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-149">Le port spécifié n'est pas ouvert.</span><span class="sxs-lookup"><span data-stu-id="346a3-149">The specified port is not open.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PORT_DISCONNECTED"></span><span id="error_port_disconnected"></span><dl> <span data-ttu-id="346a3-150"><dt><strong>ERROR_PORT_DISCONNECTED</strong></dt> <dt>619</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-150"><dt><strong>ERROR_PORT_DISCONNECTED</strong></dt> <dt>619</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-151">Le port spécifié est déconnecté.</span><span class="sxs-lookup"><span data-stu-id="346a3-151">The specified port is disconnected.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_ENDPOINTS"></span><span id="error_no_endpoints"></span><dl> <span data-ttu-id="346a3-152"><dt><strong>ERROR_NO_ENDPOINTS</strong></dt> <dt>620</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-152"><dt><strong>ERROR_NO_ENDPOINTS</strong></dt> <dt>620</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-153">Aucun point de terminaison n’a pu être déterminé.</span><span class="sxs-lookup"><span data-stu-id="346a3-153">No endpoints could be determined.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-154">Déconseillé dans Windows Vista et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-154">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CANNOT_OPEN_PHONEBOOK"></span><span id="error_cannot_open_phonebook"></span><dl> <span data-ttu-id="346a3-155"><dt><strong>ERROR_CANNOT_OPEN_PHONEBOOK</strong></dt> <dt>621</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-155"><dt><strong>ERROR_CANNOT_OPEN_PHONEBOOK</strong></dt> <dt>621</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-156">Impossible d’ouvrir le fichier de l’annuaire téléphonique spécifié.</span><span class="sxs-lookup"><span data-stu-id="346a3-156">Cannot open the specified phone book file.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_CANNOT_LOAD_PHONEBOOK"></span><span id="error_cannot_load_phonebook"></span><dl> <span data-ttu-id="346a3-157"><dt><strong>ERROR_CANNOT_LOAD_PHONEBOOK</strong></dt> <dt>622</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-157"><dt><strong>ERROR_CANNOT_LOAD_PHONEBOOK</strong></dt> <dt>622</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-158">Impossible de charger le fichier d’annuaire téléphonique spécifié.</span><span class="sxs-lookup"><span data-stu-id="346a3-158">Cannot load the specified phone book file.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CANNOT_FIND_PHONEBOOK_ENTRY"></span><span id="error_cannot_find_phonebook_entry"></span><dl> <span data-ttu-id="346a3-159"><dt><strong>ERROR_CANNOT_FIND_PHONEBOOK_ENTRY</strong></dt> <dt>623</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-159"><dt><strong>ERROR_CANNOT_FIND_PHONEBOOK_ENTRY</strong></dt> <dt>623</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-160">Impossible de trouver l’entrée de l’annuaire téléphonique spécifiée.</span><span class="sxs-lookup"><span data-stu-id="346a3-160">Cannot find the specified phone book entry.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_CANNOT_WRITE_PHONEBOOK"></span><span id="error_cannot_write_phonebook"></span><dl> <span data-ttu-id="346a3-161"><dt><strong>ERROR_CANNOT_WRITE_PHONEBOOK</strong></dt> <dt>624</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-161"><dt><strong>ERROR_CANNOT_WRITE_PHONEBOOK</strong></dt> <dt>624</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-162">Impossible d’écrire dans le fichier de l’annuaire téléphonique spécifié.</span><span class="sxs-lookup"><span data-stu-id="346a3-162">Cannot write to the specified phone book file.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CORRUPT_PHONEBOOK"></span><span id="error_corrupt_phonebook"></span><dl> <span data-ttu-id="346a3-163"><dt><strong>ERROR_CORRUPT_PHONEBOOK</strong></dt> <dt>625</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-163"><dt><strong>ERROR_CORRUPT_PHONEBOOK</strong></dt> <dt>625</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-164">Les informations trouvées dans l’annuaire téléphonique spécifié ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="346a3-164">Information found in the specified phone book is not valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_CANNOT_LOAD_STRING"></span><span id="error_cannot_load_string"></span><dl> <span data-ttu-id="346a3-165"><dt><strong>ERROR_CANNOT_LOAD_STRING</strong></dt> <dt>626</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-165"><dt><strong>ERROR_CANNOT_LOAD_STRING</strong></dt> <dt>626</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-166">Une chaîne n’a pas pu être chargée.</span><span class="sxs-lookup"><span data-stu-id="346a3-166">A string could not be loaded.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-167">Déconseillé dans Windows Vista et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-167">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_KEY_NOT_FOUND"></span><span id="error_key_not_found"></span><dl> <span data-ttu-id="346a3-168"><dt><strong>ERROR_KEY_NOT_FOUND</strong></dt> <dt>627</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-168"><dt><strong>ERROR_KEY_NOT_FOUND</strong></dt> <dt>627</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-169">Impossible de trouver la clé spécifiée.</span><span class="sxs-lookup"><span data-stu-id="346a3-169">Cannot find the specified key.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DISCONNECTION"></span><span id="error_disconnection"></span><dl> <span data-ttu-id="346a3-170"><dt><strong>ERROR_DISCONNECTION</strong></dt> <dt>628</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-170"><dt><strong>ERROR_DISCONNECTION</strong></dt> <dt>628</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-171">Le port spécifié a été déconnecté.</span><span class="sxs-lookup"><span data-stu-id="346a3-171">The specified port was disconnected.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_REMOTE_DISCONNECTION"></span><span id="error_remote_disconnection"></span><dl> <span data-ttu-id="346a3-172"><dt><strong>ERROR_REMOTE_DISCONNECTION</strong></dt> <dt>629</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-172"><dt><strong>ERROR_REMOTE_DISCONNECTION</strong></dt> <dt>629</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-173">Le port spécifié a été déconnecté par l’ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="346a3-173">The specified port was disconnected by the remote computer.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_HARDWARE_FAILURE"></span><span id="error_hardware_failure"></span><dl> <span data-ttu-id="346a3-174"><dt><strong>ERROR_HARDWARE_FAILURE</strong></dt> <dt>630</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-174"><dt><strong>ERROR_HARDWARE_FAILURE</strong></dt> <dt>630</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-175">Le port spécifié a été déconnecté en raison d’une défaillance matérielle.</span><span class="sxs-lookup"><span data-stu-id="346a3-175">The specified port was disconnected due to hardware failure.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_USER_DISCONNECTION"></span><span id="error_user_disconnection"></span><dl> <span data-ttu-id="346a3-176"><dt><strong>ERROR_USER_DISCONNECTION</strong></dt> <dt>631</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-176"><dt><strong>ERROR_USER_DISCONNECTION</strong></dt> <dt>631</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-177">Le port spécifié a été déconnecté par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="346a3-177">The specified port was disconnected by the user.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INVALID_SIZE"></span><span id="error_invalid_size"></span><dl> <span data-ttu-id="346a3-178"><dt><strong>ERROR_INVALID_SIZE</strong></dt> <dt>632</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-178"><dt><strong>ERROR_INVALID_SIZE</strong></dt> <dt>632</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-179">Taille de structure incorrecte.</span><span class="sxs-lookup"><span data-stu-id="346a3-179">Incorrect structure size.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PORT_NOT_AVAILABLE"></span><span id="error_port_not_available"></span><dl> <span data-ttu-id="346a3-180"><dt><strong>ERROR_PORT_NOT_AVAILABLE</strong></dt> <dt>633</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-180"><dt><strong>ERROR_PORT_NOT_AVAILABLE</strong></dt> <dt>633</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-181">Le port spécifié est déjà utilisé ou n’est pas configuré pour la connexion d’accès à distance.</span><span class="sxs-lookup"><span data-stu-id="346a3-181">The specified port is already in use or is not configured for remote access dial-out.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_CANNOT_PROJECT_CLIENT"></span><span id="error_cannot_project_client"></span><dl> <span data-ttu-id="346a3-182"><dt><strong>ERROR_CANNOT_PROJECT_CLIENT</strong></dt> <dt>634</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-182"><dt><strong>ERROR_CANNOT_PROJECT_CLIENT</strong></dt> <dt>634</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-183">Votre ordinateur n’a pas pu être enregistré sur le réseau distant.</span><span class="sxs-lookup"><span data-stu-id="346a3-183">Your computer could not be registered on the remote network.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-184">Déconseillé dans Windows Vista et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-184">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_UNKNOWN"></span><span id="error_unknown"></span><dl> <span data-ttu-id="346a3-185"><dt><strong>ERROR_UNKNOWN</strong></dt> <dt>635</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-185"><dt><strong>ERROR_UNKNOWN</strong></dt> <dt>635</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-186">Une erreur inconnue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="346a3-186">An unknown error has occurred.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_WRONG_DEVICE_ATTACHED"></span><span id="error_wrong_device_attached"></span><dl> <span data-ttu-id="346a3-187"><dt><strong>ERROR_WRONG_DEVICE_ATTACHED</strong></dt> <dt>636</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-187"><dt><strong>ERROR_WRONG_DEVICE_ATTACHED</strong></dt> <dt>636</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-188">Le mauvais appareil est attaché au port spécifié.</span><span class="sxs-lookup"><span data-stu-id="346a3-188">The wrong device is attached to the specified port.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_BAD_STRING"></span><span id="error_bad_string"></span><dl> <span data-ttu-id="346a3-189"><dt><strong>ERROR_BAD_STRING</strong></dt> <dt>637</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-189"><dt><strong>ERROR_BAD_STRING</strong></dt> <dt>637</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-190">Une chaîne qui n’a pas pu être convertie a été détectée.</span><span class="sxs-lookup"><span data-stu-id="346a3-190">A string was detected that could not be converted.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-191">Déconseillé dans Windows Vista et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-191">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_REQUEST_TIMEOUT"></span><span id="error_request_timeout"></span><dl> <span data-ttu-id="346a3-192"><dt><strong>ERROR_REQUEST_TIMEOUT</strong></dt> <dt>638</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-192"><dt><strong>ERROR_REQUEST_TIMEOUT</strong></dt> <dt>638</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-193">Le délai d'attente de la requête a expiré.</span><span class="sxs-lookup"><span data-stu-id="346a3-193">The request has timed out.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CANNOT_GET_LANA"></span><span id="error_cannot_get_lana"></span><dl> <span data-ttu-id="346a3-194"><dt><strong>ERROR_CANNOT_GET_LANA</strong></dt> <dt>639</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-194"><dt><strong>ERROR_CANNOT_GET_LANA</strong></dt> <dt>639</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-195">Aucun réseau asynchrone n’est disponible.</span><span class="sxs-lookup"><span data-stu-id="346a3-195">No asynchronous net is available.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-196">Déconseillé dans Windows Vista et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-196">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NETBIOS_ERROR"></span><span id="error_netbios_error"></span><dl> <span data-ttu-id="346a3-197"><dt><strong>ERROR_NETBIOS_ERROR</strong></dt> <dt>640</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-197"><dt><strong>ERROR_NETBIOS_ERROR</strong></dt> <dt>640</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-198">Une erreur s’est produite lors de l’appel de NetBIOS.</span><span class="sxs-lookup"><span data-stu-id="346a3-198">An error has occurred involving NetBIOS.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-199">Déconseillé dans Windows Vista et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-199">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SERVER_OUT_OF_RESOURCES"></span><span id="error_server_out_of_resources"></span><dl> <span data-ttu-id="346a3-200"><dt><strong>ERROR_SERVER_OUT_OF_RESOURCES</strong></dt> <dt>641</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-200"><dt><strong>ERROR_SERVER_OUT_OF_RESOURCES</strong></dt> <dt>641</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-201">le serveur ne peut pas allouer les ressources NetBIOS nécessaires à la prise en charge du client.</span><span class="sxs-lookup"><span data-stu-id="346a3-201">he server cannot allocate NetBIOS resources needed to support the client.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-202">Déconseillé dans Windows Vista et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-202">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NAME_EXISTS_ON_NET"></span><span id="error_name_exists_on_net"></span><dl> <span data-ttu-id="346a3-203"><dt><strong>ERROR_NAME_EXISTS_ON_NET</strong></dt> <dt>642</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-203"><dt><strong>ERROR_NAME_EXISTS_ON_NET</strong></dt> <dt>642</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-204">L’un des noms NetBIOS de votre ordinateur est déjà inscrit sur le réseau distant.</span><span class="sxs-lookup"><span data-stu-id="346a3-204">One of your computer's NetBIOS names is already registered on the remote network.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-205">Déconseillé dans Windows Vista et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-205">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SERVER_GENERAL_NET_FAILURE"></span><span id="error_server_general_net_failure"></span><dl> <span data-ttu-id="346a3-206"><dt><strong>ERROR_SERVER_GENERAL_NET_FAILURE</strong></dt> <dt>643</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-206"><dt><strong>ERROR_SERVER_GENERAL_NET_FAILURE</strong></dt> <dt>643</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-207">Échec d’une carte réseau sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="346a3-207">A network adapter at the server failed.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-208">Déconseillé dans Windows Vista et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-208">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="WARNING_MSG_ALIAS_NOT_ADDED"></span><span id="warning_msg_alias_not_added"></span><dl> <span data-ttu-id="346a3-209"><dt><strong>WARNING_MSG_ALIAS_NOT_ADDED</strong></dt> <dt>644</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-209"><dt><strong>WARNING_MSG_ALIAS_NOT_ADDED</strong></dt> <dt>644</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-210">Vous ne recevrez pas de message sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="346a3-210">You will not receive network message popups.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-211">Déconseillé dans Windows Vista et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-211">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_AUTH_INTERNAL"></span><span id="error_auth_internal"></span><dl> <span data-ttu-id="346a3-212"><dt><strong>ERROR_AUTH_INTERNAL</strong></dt> <dt>645</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-212"><dt><strong>ERROR_AUTH_INTERNAL</strong></dt> <dt>645</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-213">Une erreur d’authentification interne s’est produite.</span><span class="sxs-lookup"><span data-stu-id="346a3-213">An internal authentication error has occurred.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_RESTRICTED_LOGON_HOURS"></span><span id="error_restricted_logon_hours"></span><dl> <span data-ttu-id="346a3-214"><dt><strong>ERROR_RESTRICTED_LOGON_HOURS</strong></dt> <dt>646</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-214"><dt><strong>ERROR_RESTRICTED_LOGON_HOURS</strong></dt> <dt>646</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-215">Le compte spécifié n’est pas autorisé à se connecter à cette heure de la journée.</span><span class="sxs-lookup"><span data-stu-id="346a3-215">The specified account is not permitted to log in at this time of day.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_ACCT_DISABLED"></span><span id="error_acct_disabled"></span><dl> <span data-ttu-id="346a3-216"><dt><strong>ERROR_ACCT_DISABLED</strong></dt> <dt>647</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-216"><dt><strong>ERROR_ACCT_DISABLED</strong></dt> <dt>647</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-217">Le compte spécifié est désactivé.</span><span class="sxs-lookup"><span data-stu-id="346a3-217">The specified account is disabled.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PASSWD_EXPIRED"></span><span id="error_passwd_expired"></span><dl> <span data-ttu-id="346a3-218"><dt><strong>ERROR_PASSWD_EXPIRED</strong></dt> <dt>648</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-218"><dt><strong>ERROR_PASSWD_EXPIRED</strong></dt> <dt>648</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-219">Le mot de passe spécifié a expiré.</span><span class="sxs-lookup"><span data-stu-id="346a3-219">The specified password has expired.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NO_DIALIN_PERMISSION"></span><span id="error_no_dialin_permission"></span><dl> <span data-ttu-id="346a3-220"><dt><strong>ERROR_NO_DIALIN_PERMISSION</strong></dt> <dt>649</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-220"><dt><strong>ERROR_NO_DIALIN_PERMISSION</strong></dt> <dt>649</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-221">Le compte spécifié ne dispose pas des autorisations d’accès à distance.</span><span class="sxs-lookup"><span data-stu-id="346a3-221">The specified account does not have remote access permissions.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_SERVER_NOT_RESPONDING"></span><span id="error_server_not_responding"></span><dl> <span data-ttu-id="346a3-222"><dt><strong>ERROR_SERVER_NOT_RESPONDING</strong></dt> <dt>650</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-222"><dt><strong>ERROR_SERVER_NOT_RESPONDING</strong></dt> <dt>650</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-223">Le serveur d’accès à distance ne répond pas.</span><span class="sxs-lookup"><span data-stu-id="346a3-223">The remote access server is not responding.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-224">Déconseillé dans Windows Vista et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-224">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_FROM_DEVICE"></span><span id="error_from_device"></span><dl> <span data-ttu-id="346a3-225"><dt><strong>ERROR_FROM_DEVICE</strong></dt> <dt>651</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-225"><dt><strong>ERROR_FROM_DEVICE</strong></dt> <dt>651</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-226">Votre modem ou autre périphérique de connexion a signalé une erreur.</span><span class="sxs-lookup"><span data-stu-id="346a3-226">Your modem or other connection device has reported an error.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_UNRECOGNIZED_RESPONSE"></span><span id="error_unrecognized_response"></span><dl> <span data-ttu-id="346a3-227"><dt><strong>ERROR_UNRECOGNIZED_RESPONSE</strong></dt> <dt>652</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-227"><dt><strong>ERROR_UNRECOGNIZED_RESPONSE</strong></dt> <dt>652</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-228">Une réponse non reconnue a été retournée par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="346a3-228">An unrecognized response was returned by the device.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_MACRO_NOT_FOUND"></span><span id="error_macro_not_found"></span><dl> <span data-ttu-id="346a3-229"><dt><strong>ERROR_MACRO_NOT_FOUND</strong></dt> <dt>653</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-229"><dt><strong>ERROR_MACRO_NOT_FOUND</strong></dt> <dt>653</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-230">Une macro requise par l’appareil est introuvable dans l’appareil. Section du fichier INF.</span><span class="sxs-lookup"><span data-stu-id="346a3-230">A macro required by the device was not found in the device .INF file section.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_MACRO_NOT_DEFINED"></span><span id="error_macro_not_defined"></span><dl> <span data-ttu-id="346a3-231"><dt><strong>ERROR_MACRO_NOT_DEFINED</strong></dt> <dt>654</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-231"><dt><strong>ERROR_MACRO_NOT_DEFINED</strong></dt> <dt>654</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-232">Commande ou réponse dans l’appareil. La section du fichier INF fait référence à une macro non définie.</span><span class="sxs-lookup"><span data-stu-id="346a3-232">A command or response in the device .INF file section refers to an undefined macro.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_MESSAGE_MACRO_NOT_FOUND"></span><span id="error_message_macro_not_found"></span><dl> <span data-ttu-id="346a3-233"><dt><strong>ERROR_MESSAGE_MACRO_NOT_FOUND</strong></dt> <dt>655</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-233"><dt><strong>ERROR_MESSAGE_MACRO_NOT_FOUND</strong></dt> <dt>655</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-234">La <message> macro est introuvable dans l’appareil. Section du fichier INF.</span><span class="sxs-lookup"><span data-stu-id="346a3-234">The <message> macro was not found in the device .INF file section.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DEFAULTOFF_MACRO_NOT_FOUND"></span><span id="error_defaultoff_macro_not_found"></span><dl> <span data-ttu-id="346a3-235"><dt><strong>ERROR_DEFAULTOFF_MACRO_NOT_FOUND</strong></dt> <dt>656</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-235"><dt><strong>ERROR_DEFAULTOFF_MACRO_NOT_FOUND</strong></dt> <dt>656</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-236"><defaultoff>Macro dans l’appareil. La section du fichier INF contient une macro non définie.</span><span class="sxs-lookup"><span data-stu-id="346a3-236">The <defaultoff> macro in the device .INF file section contains an undefined macro.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_FILE_COULD_NOT_BE_OPENED"></span><span id="error_file_could_not_be_opened"></span><dl> <span data-ttu-id="346a3-237"><dt><strong>ERROR_FILE_COULD_NOT_BE_OPENED</strong></dt> <dt>657</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-237"><dt><strong>ERROR_FILE_COULD_NOT_BE_OPENED</strong></dt> <dt>657</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-238">L’appareil. Impossible d’ouvrir le fichier INF.</span><span class="sxs-lookup"><span data-stu-id="346a3-238">The device .INF file could not be opened.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DEVICENAME_TOO_LONG"></span><span id="error_devicename_too_long"></span><dl> <span data-ttu-id="346a3-239"><dt><strong>ERROR_DEVICENAME_TOO_LONG</strong></dt> <dt>658</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-239"><dt><strong>ERROR_DEVICENAME_TOO_LONG</strong></dt> <dt>658</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-240">Nom de l’appareil dans l’appareil. Fichier INF ou média. Le fichier INI est trop long.</span><span class="sxs-lookup"><span data-stu-id="346a3-240">The device name in the device .INF or media .INI file is too long.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_DEVICENAME_NOT_FOUND"></span><span id="error_devicename_not_found"></span><dl> <span data-ttu-id="346a3-241"><dt><strong>ERROR_DEVICENAME_NOT_FOUND</strong></dt> <dt>659</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-241"><dt><strong>ERROR_DEVICENAME_NOT_FOUND</strong></dt> <dt>659</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-242">Média. Le fichier INI fait référence à un nom de périphérique inconnu.</span><span class="sxs-lookup"><span data-stu-id="346a3-242">The media .INI file refers to an unknown device name.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_RESPONSES"></span><span id="error_no_responses"></span><dl> <span data-ttu-id="346a3-243"><dt><strong>ERROR_NO_RESPONSES</strong></dt> <dt>660</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-243"><dt><strong>ERROR_NO_RESPONSES</strong></dt> <dt>660</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-244">L’appareil. Le fichier INF ne contient aucune réponse pour la commande.</span><span class="sxs-lookup"><span data-stu-id="346a3-244">The device .INF file contains no responses for the command.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NO_COMMAND_FOUND"></span><span id="error_no_command_found"></span><dl> <span data-ttu-id="346a3-245"><dt><strong>ERROR_NO_COMMAND_FOUND</strong></dt> <dt>661</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-245"><dt><strong>ERROR_NO_COMMAND_FOUND</strong></dt> <dt>661</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-246">L’appareil. Une commande est manquante dans le fichier INF.</span><span class="sxs-lookup"><span data-stu-id="346a3-246">The device .INF file is missing a command.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_WRONG_KEY_SPECIFIED"></span><span id="error_wrong_key_specified"></span><dl> <span data-ttu-id="346a3-247"><dt><strong>ERROR_WRONG_KEY_SPECIFIED</strong></dt> <dt>662</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-247"><dt><strong>ERROR_WRONG_KEY_SPECIFIED</strong></dt> <dt>662</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-248">Tentative de définition d’une macro non listée dans le périphérique. Section du fichier INF.</span><span class="sxs-lookup"><span data-stu-id="346a3-248">Attempted to set a macro not listed in device .INF file section.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_UNKNOWN_DEVICE_TYPE"></span><span id="error_unknown_device_type"></span><dl> <span data-ttu-id="346a3-249"><dt><strong>ERROR_UNKNOWN_DEVICE_TYPE</strong></dt> <dt>663</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-249"><dt><strong>ERROR_UNKNOWN_DEVICE_TYPE</strong></dt> <dt>663</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-250">Média. Le fichier INI fait référence à un type de périphérique inconnu.</span><span class="sxs-lookup"><span data-stu-id="346a3-250">The media .INI file refers to an unknown device type.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_ALLOCATING_MEMORY"></span><span id="error_allocating_memory"></span><dl> <span data-ttu-id="346a3-251"><dt><strong>ERROR_ALLOCATING_MEMORY</strong></dt> <dt>664</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-251"><dt><strong>ERROR_ALLOCATING_MEMORY</strong></dt> <dt>664</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-252">Impossible d’allouer de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="346a3-252">Cannot allocate memory.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PORT_NOT_CONFIGURED"></span><span id="error_port_not_configured"></span><dl> <span data-ttu-id="346a3-253"><dt><strong>ERROR_PORT_NOT_CONFIGURED</strong></dt> <dt>665</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-253"><dt><strong>ERROR_PORT_NOT_CONFIGURED</strong></dt> <dt>665</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-254">Le port n’est pas configuré pour l’accès à distance.</span><span class="sxs-lookup"><span data-stu-id="346a3-254">The port is not configured for remote access.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DEVICE_NOT_READY"></span><span id="error_device_not_ready"></span><dl> <span data-ttu-id="346a3-255"><dt><strong>ERROR_DEVICE_NOT_READY</strong></dt> <dt>666</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-255"><dt><strong>ERROR_DEVICE_NOT_READY</strong></dt> <dt>666</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-256">Votre modem ou autre périphérique de connexion ne fonctionne pas.</span><span class="sxs-lookup"><span data-stu-id="346a3-256">Your modem or other connection device is not functioning.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_READING_INI_FILE"></span><span id="error_reading_ini_file"></span><dl> <span data-ttu-id="346a3-257"><dt><strong>ERROR_READING_INI_FILE</strong></dt> <dt>667</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-257"><dt><strong>ERROR_READING_INI_FILE</strong></dt> <dt>667</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-258">Impossible de lire le média. Fichier INI.</span><span class="sxs-lookup"><span data-stu-id="346a3-258">Cannot read the media .INI file.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_CONNECTION"></span><span id="error_no_connection"></span><dl> <span data-ttu-id="346a3-259"><dt><strong>ERROR_NO_CONNECTION</strong></dt> <dt>668</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-259"><dt><strong>ERROR_NO_CONNECTION</strong></dt> <dt>668</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-260">La connexion a été abandonnée.</span><span class="sxs-lookup"><span data-stu-id="346a3-260">The connection was dropped.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_BAD_USAGE_IN_INI_FILE"></span><span id="error_bad_usage_in_ini_file"></span><dl> <span data-ttu-id="346a3-261"><dt><strong>ERROR_BAD_USAGE_IN_INI_FILE</strong></dt> <dt>669</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-261"><dt><strong>ERROR_BAD_USAGE_IN_INI_FILE</strong></dt> <dt>669</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-262">Le paramètre d’utilisation du fichier Media. ini n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="346a3-262">The usage parameter in the media .ini file is not valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_READING_SECTIONNAME"></span><span id="error_reading_sectionname"></span><dl> <span data-ttu-id="346a3-263"><dt><strong>ERROR_READING_SECTIONNAME</strong></dt> <dt>670</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-263"><dt><strong>ERROR_READING_SECTIONNAME</strong></dt> <dt>670</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-264">Impossible de lire le nom de la section à partir du média. Fichier INI.</span><span class="sxs-lookup"><span data-stu-id="346a3-264">Cannot read the section name from the media .INI file.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_READING_DEVICETYPE"></span><span id="error_reading_devicetype"></span><dl> <span data-ttu-id="346a3-265"><dt><strong>ERROR_READING_DEVICETYPE</strong></dt> <dt>671</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-265"><dt><strong>ERROR_READING_DEVICETYPE</strong></dt> <dt>671</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-266">Impossible de lire le type d’appareil à partir du média. Fichier INI.</span><span class="sxs-lookup"><span data-stu-id="346a3-266">Cannot read the device type from the media .INI file.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_READING_DEVICENAME"></span><span id="error_reading_devicename"></span><dl> <span data-ttu-id="346a3-267"><dt><strong>ERROR_READING_DEVICENAME</strong></dt> <dt>672</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-267"><dt><strong>ERROR_READING_DEVICENAME</strong></dt> <dt>672</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-268">Impossible de lire le nom de l’appareil à partir du média. Fichier INI.</span><span class="sxs-lookup"><span data-stu-id="346a3-268">Cannot read the device name from the media .INI file.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_READING_USAGE"></span><span id="error_reading_usage"></span><dl> <span data-ttu-id="346a3-269"><dt><strong>ERROR_READING_USAGE</strong></dt> <dt>673</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-269"><dt><strong>ERROR_READING_USAGE</strong></dt> <dt>673</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-270">Impossible de lire l’utilisation à partir du média. Fichier INI.</span><span class="sxs-lookup"><span data-stu-id="346a3-270">Cannot read the usage from the media .INI file.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_READING_MAXCONNECTBPS"></span><span id="error_reading_maxconnectbps"></span><dl> <span data-ttu-id="346a3-271"><dt><strong>ERROR_READING_MAXCONNECTBPS</strong></dt> <dt>674</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-271"><dt><strong>ERROR_READING_MAXCONNECTBPS</strong></dt> <dt>674</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-272">Le système n’a pas pu lire la vitesse maximale de connexion du transporteur à partir du média. Fichier INI.</span><span class="sxs-lookup"><span data-stu-id="346a3-272">The system was unable to read the maximum carrier connection speed from the media .INI file.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-273">Déconseillé dans Windows Vista et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-273">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_READING_MAXCARRIERBPS"></span><span id="error_reading_maxcarrierbps"></span><dl> <span data-ttu-id="346a3-274"><dt><strong>ERROR_READING_MAXCARRIERBPS</strong></dt> <dt>675</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-274"><dt><strong>ERROR_READING_MAXCARRIERBPS</strong></dt> <dt>675</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-275">Impossible de lire l’utilisation à partir du média. Fichier INI.</span><span class="sxs-lookup"><span data-stu-id="346a3-275">Cannot read the usage from the media .INI file.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_LINE_BUSY"></span><span id="error_line_busy"></span><dl> <span data-ttu-id="346a3-276"><dt><strong>ERROR_LINE_BUSY</strong></dt> <dt>676</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-276"><dt><strong>ERROR_LINE_BUSY</strong></dt> <dt>676</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-277">La ligne est occupée.</span><span class="sxs-lookup"><span data-stu-id="346a3-277">The line is busy.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_VOICE_ANSWER"></span><span id="error_voice_answer"></span><dl> <span data-ttu-id="346a3-278"><dt><strong>ERROR_VOICE_ANSWER</strong></dt> <dt>677</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-278"><dt><strong>ERROR_VOICE_ANSWER</strong></dt> <dt>677</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-279">Une personne a répondu à la place d’un modem.</span><span class="sxs-lookup"><span data-stu-id="346a3-279">A person answered instead of a modem.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_ANSWER"></span><span id="error_no_answer"></span><dl> <span data-ttu-id="346a3-280"><dt><strong>ERROR_NO_ANSWER</strong></dt> <dt>678</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-280"><dt><strong>ERROR_NO_ANSWER</strong></dt> <dt>678</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-281">Il n’y a pas de réponse.</span><span class="sxs-lookup"><span data-stu-id="346a3-281">There is no answer.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NO_CARRIER"></span><span id="error_no_carrier"></span><dl> <span data-ttu-id="346a3-282"><dt><strong>ERROR_NO_CARRIER</strong></dt> <dt>679</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-282"><dt><strong>ERROR_NO_CARRIER</strong></dt> <dt>679</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-283">Impossible de détecter un signal d’opérateur.</span><span class="sxs-lookup"><span data-stu-id="346a3-283">Cannot detect a carrier signal.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_DIALTONE"></span><span id="error_no_dialtone"></span><dl> <span data-ttu-id="346a3-284"><dt><strong>ERROR_NO_DIALTONE</strong></dt> <dt>680</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-284"><dt><strong>ERROR_NO_DIALTONE</strong></dt> <dt>680</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-285">Il n’y a pas de tonalité.</span><span class="sxs-lookup"><span data-stu-id="346a3-285">There is no dial tone.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_IN_COMMAND"></span><span id="error_in_command"></span><dl> <span data-ttu-id="346a3-286"><dt><strong>ERROR_IN_COMMAND</strong></dt> <dt>681</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-286"><dt><strong>ERROR_IN_COMMAND</strong></dt> <dt>681</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-287">Le modem (ou un autre périphérique de connexion) a signalé une erreur générale.</span><span class="sxs-lookup"><span data-stu-id="346a3-287">The modem (or other connecting device) reported a general error.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-288">Déconseillé dans Windows Vista et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-288">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_WRITING_SECTIONNAME"></span><span id="error_writing_sectionname"></span><dl> <span data-ttu-id="346a3-289"><dt><strong>ERROR_WRITING_SECTIONNAME</strong></dt> <dt>682</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-289"><dt><strong>ERROR_WRITING_SECTIONNAME</strong></dt> <dt>682</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-290">Une erreur s’est produite lors de l’écriture du nom de la section.</span><span class="sxs-lookup"><span data-stu-id="346a3-290">There was an error in writing the section name.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_WRITING_DEVICETYPE"></span><span id="error_writing_devicetype"></span><dl> <span data-ttu-id="346a3-291"><dt><strong>ERROR_WRITING_DEVICETYPE</strong></dt> <dt>683</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-291"><dt><strong>ERROR_WRITING_DEVICETYPE</strong></dt> <dt>683</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-292">Une erreur s’est produite lors de l’écriture du type d’appareil.</span><span class="sxs-lookup"><span data-stu-id="346a3-292">There was an error in writing the device type.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_WRITING_DEVICENAME"></span><span id="error_writing_devicename"></span><dl> <span data-ttu-id="346a3-293"><dt><strong>ERROR_WRITING_DEVICENAME</strong></dt> <dt>684</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-293"><dt><strong>ERROR_WRITING_DEVICENAME</strong></dt> <dt>684</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-294">Une erreur s’est produite lors de l’écriture du nom de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="346a3-294">There was an error in writing the device name.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_WRITING_MAXCONNECTBPS"></span><span id="error_writing_maxconnectbps"></span><dl> <span data-ttu-id="346a3-295"><dt><strong>ERROR_WRITING_MAXCONNECTBPS</strong></dt> <dt>685</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-295"><dt><strong>ERROR_WRITING_MAXCONNECTBPS</strong></dt> <dt>685</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-296">Une erreur s’est produite lors de l’écriture de la vitesse de connexion maximale.</span><span class="sxs-lookup"><span data-stu-id="346a3-296">There was an error in writing the maximum connection speed.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_WRITING_MAXCARRIERBPS"></span><span id="error_writing_maxcarrierbps"></span><dl> <span data-ttu-id="346a3-297"><dt><strong>ERROR_WRITING_MAXCARRIERBPS</strong></dt> <dt>686</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-297"><dt><strong>ERROR_WRITING_MAXCARRIERBPS</strong></dt> <dt>686</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-298">Une erreur s’est produite lors de l’écriture de la vitesse maximale de l’opérateur.</span><span class="sxs-lookup"><span data-stu-id="346a3-298">There was an error in writing the maximum carrier speed.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_WRITING_USAGE"></span><span id="error_writing_usage"></span><dl> <span data-ttu-id="346a3-299"><dt><strong>ERROR_WRITING_USAGE</strong></dt> <dt>687</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-299"><dt><strong>ERROR_WRITING_USAGE</strong></dt> <dt>687</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-300">Une erreur s’est produite lors de l’écriture de l’utilisation.</span><span class="sxs-lookup"><span data-stu-id="346a3-300">There was an error in writing the usage.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_WRITING_DEFAULTOFF"></span><span id="error_writing_defaultoff"></span><dl> <span data-ttu-id="346a3-301"><dt><strong>ERROR_WRITING_DEFAULTOFF</strong></dt> <dt>688</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-301"><dt><strong>ERROR_WRITING_DEFAULTOFF</strong></dt> <dt>688</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-302">Une erreur s’est produite lors de l’écriture de la valeur par défaut OFF.</span><span class="sxs-lookup"><span data-stu-id="346a3-302">There was an error in writing the default-off.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_READING_DEFAULTOFF"></span><span id="error_reading_defaultoff"></span><dl> <span data-ttu-id="346a3-303"><dt><strong>ERROR_READING_DEFAULTOFF</strong></dt> <dt>689</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-303"><dt><strong>ERROR_READING_DEFAULTOFF</strong></dt> <dt>689</dt> </span></span></dl></td>

</tr>
<tr class="odd">
<td><span id="ERROR_EMPTY_INI_FILE"></span><span id="error_empty_ini_file"></span><dl> <span data-ttu-id="346a3-304"><dt><strong>ERROR_EMPTY_INI_FILE</strong></dt> <dt>690</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-304"><dt><strong>ERROR_EMPTY_INI_FILE</strong></dt> <dt>690</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-305">Média. Le fichier INI est vide.</span><span class="sxs-lookup"><span data-stu-id="346a3-305">The media .INI file is empty.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_AUTHENTICATION_FAILURE"></span><span id="error_authentication_failure"></span><dl> <span data-ttu-id="346a3-306"><dt><strong>ERROR_AUTHENTICATION_FAILURE</strong></dt> <dt>691</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-306"><dt><strong>ERROR_AUTHENTICATION_FAILURE</strong></dt> <dt>691</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-307">Accès refusé, car le nom d’utilisateur, le mot de passe ou les deux ne sont pas valides sur le domaine.</span><span class="sxs-lookup"><span data-stu-id="346a3-307">Access denied because the user name, password, or both is not valid on the domain.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PORT_OR_DEVICE"></span><span id="error_port_or_device"></span><dl> <span data-ttu-id="346a3-308"><dt><strong>ERROR_PORT_OR_DEVICE</strong></dt> <dt>692</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-308"><dt><strong>ERROR_PORT_OR_DEVICE</strong></dt> <dt>692</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-309">Une défaillance matérielle s’est produite dans le port ou l’appareil attaché</span><span class="sxs-lookup"><span data-stu-id="346a3-309">A hardware failure has occurred in the port or attached device</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NOT_BINARY_MACRO"></span><span id="error_not_binary_macro"></span><dl> <span data-ttu-id="346a3-310"><dt><strong>ERROR_NOT_BINARY_MACRO</strong></dt> <dt>693</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-310"><dt><strong>ERROR_NOT_BINARY_MACRO</strong></dt> <dt>693</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-311">La macro n’est pas une macro binaire.</span><span class="sxs-lookup"><span data-stu-id="346a3-311">The macro is not a binary macro.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DCB_NOT_FOUND"></span><span id="error_dcb_not_found"></span><dl> <span data-ttu-id="346a3-312"><dt><strong>ERROR_DCB_NOT_FOUND</strong></dt> <dt>694</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-312"><dt><strong>ERROR_DCB_NOT_FOUND</strong></dt> <dt>694</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-313">DCB introuvable.</span><span class="sxs-lookup"><span data-stu-id="346a3-313">DCB not found.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_STATE_MACHINES_NOT_STARTED"></span><span id="error_state_machines_not_started"></span><dl> <span data-ttu-id="346a3-314"><dt><strong>ERROR_STATE_MACHINES_NOT_STARTED</strong></dt> <dt>695</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-314"><dt><strong>ERROR_STATE_MACHINES_NOT_STARTED</strong></dt> <dt>695</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-315">Les machines d’État ne sont pas démarrées.</span><span class="sxs-lookup"><span data-stu-id="346a3-315">State machines are not started.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_STATE_MACHINES_ALREADY_STARTED"></span><span id="error_state_machines_already_started"></span><dl> <span data-ttu-id="346a3-316"><dt><strong>ERROR_STATE_MACHINES_ALREADY_STARTED</strong></dt> <dt>696</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-316"><dt><strong>ERROR_STATE_MACHINES_ALREADY_STARTED</strong></dt> <dt>696</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-317">Les machines d’État sont déjà démarrées.</span><span class="sxs-lookup"><span data-stu-id="346a3-317">State machines are already started.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PARTIAL_RESPONSE_LOOPING"></span><span id="error_partial_response_looping"></span><dl> <span data-ttu-id="346a3-318"><dt><strong>ERROR_PARTIAL_RESPONSE_LOOPING</strong></dt> <dt>697</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-318"><dt><strong>ERROR_PARTIAL_RESPONSE_LOOPING</strong></dt> <dt>697</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-319">Boucle de réponse partielle.</span><span class="sxs-lookup"><span data-stu-id="346a3-319">Partial response looping.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_UNKNOWN_RESPONSE_KEY"></span><span id="error_unknown_response_key"></span><dl> <span data-ttu-id="346a3-320"><dt><strong>ERROR_UNKNOWN_RESPONSE_KEY</strong></dt> <dt>698</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-320"><dt><strong>ERROR_UNKNOWN_RESPONSE_KEY</strong></dt> <dt>698</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-321">Nom de la clé de réponse dans l’appareil. Le fichier INF n’est pas au format attendu.</span><span class="sxs-lookup"><span data-stu-id="346a3-321">A response key name in the device .INF file is not in the expected format.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_RECV_BUF_FULL"></span><span id="error_recv_buf_full"></span><dl> <span data-ttu-id="346a3-322"><dt><strong>ERROR_RECV_BUF_FULL</strong></dt> <dt>699</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-322"><dt><strong>ERROR_RECV_BUF_FULL</strong></dt> <dt>699</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-323">La réponse de l’appareil a provoqué un dépassement de mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="346a3-323">The device response caused a buffer overflow.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_CMD_TOO_LONG"></span><span id="error_cmd_too_long"></span><dl> <span data-ttu-id="346a3-324"><dt><strong>ERROR_CMD_TOO_LONG</strong></dt> <dt>700</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-324"><dt><strong>ERROR_CMD_TOO_LONG</strong></dt> <dt>700</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-325">Commande développée dans l’appareil. Le fichier INF est trop long.</span><span class="sxs-lookup"><span data-stu-id="346a3-325">The expanded command in the device .INF file is too long.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_UNSUPPORTED_BPS"></span><span id="error_unsupported_bps"></span><dl> <span data-ttu-id="346a3-326"><dt><strong>ERROR_UNSUPPORTED_BPS</strong></dt> <dt>701</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-326"><dt><strong>ERROR_UNSUPPORTED_BPS</strong></dt> <dt>701</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-327">L’appareil a été déplacé vers une vitesse de connexion qui n’est pas prise en charge par le pilote COM.</span><span class="sxs-lookup"><span data-stu-id="346a3-327">The device moved to a connection speed that is not supported by the COM driver.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_UNEXPECTED_RESPONSE"></span><span id="error_unexpected_response"></span><dl> <span data-ttu-id="346a3-328"><dt><strong>ERROR_UNEXPECTED_RESPONSE</strong></dt> <dt>702</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-328"><dt><strong>ERROR_UNEXPECTED_RESPONSE</strong></dt> <dt>702</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-329">Réponse de l’appareil reçue quand aucune n’est attendue.</span><span class="sxs-lookup"><span data-stu-id="346a3-329">Device response received when none expected.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INTERACTIVE_MODE"></span><span id="error_interactive_mode"></span><dl> <span data-ttu-id="346a3-330"><dt><strong>ERROR_INTERACTIVE_MODE</strong></dt> <dt>703</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-330"><dt><strong>ERROR_INTERACTIVE_MODE</strong></dt> <dt>703</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-331">Une erreur s’est produite, car le mode interactif est activé.</span><span class="sxs-lookup"><span data-stu-id="346a3-331">An error occurred because the interactive mode is enabled.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_BAD_CALLBACK_NUMBER"></span><span id="error_bad_callback_number"></span><dl> <span data-ttu-id="346a3-332"><dt><strong>ERROR_BAD_CALLBACK_NUMBER</strong></dt> <dt>704</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-332"><dt><strong>ERROR_BAD_CALLBACK_NUMBER</strong></dt> <dt>704</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-333">Un numéro de rappel incorrect a été spécifié.</span><span class="sxs-lookup"><span data-stu-id="346a3-333">A bad callback number was specified.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_AUTH_STATE"></span><span id="error_invalid_auth_state"></span><dl> <span data-ttu-id="346a3-334"><dt><strong>ERROR_INVALID_AUTH_STATE</strong></dt> <dt>705</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-334"><dt><strong>ERROR_INVALID_AUTH_STATE</strong></dt> <dt>705</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-335">L’état d’authentification spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="346a3-335">The specified authentication state is not valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_WRITING_INITBPS"></span><span id="error_writing_initbps"></span><dl> <span data-ttu-id="346a3-336"><dt><strong>ERROR_WRITING_INITBPS</strong></dt> <dt>706</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-336"><dt><strong>ERROR_WRITING_INITBPS</strong></dt> <dt>706</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-337">Une erreur s’est produite lors de l’écriture de la vitesse de connexion initiale.</span><span class="sxs-lookup"><span data-stu-id="346a3-337">An error occurred when writing the initial connection speed.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-338">Déconseillé dans Windows Vista et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-338">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_X25_DIAGNOSTIC"></span><span id="error_x25_diagnostic"></span><dl> <span data-ttu-id="346a3-339"><dt><strong>ERROR_X25_DIAGNOSTIC</strong></dt> <dt>707</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-339"><dt><strong>ERROR_X25_DIAGNOSTIC</strong></dt> <dt>707</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-340">Une indication de diagnostic X. 25 a été reçue.</span><span class="sxs-lookup"><span data-stu-id="346a3-340">An X.25 diagnostic indication was received.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_ACCT_EXPIRED"></span><span id="error_acct_expired"></span><dl> <span data-ttu-id="346a3-341"><dt><strong>ERROR_ACCT_EXPIRED</strong></dt> <dt>708</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-341"><dt><strong>ERROR_ACCT_EXPIRED</strong></dt> <dt>708</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-342">Le compte spécifié a expiré.</span><span class="sxs-lookup"><span data-stu-id="346a3-342">The specified account has expired.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CHANGING_PASSWORD"></span><span id="error_changing_password"></span><dl> <span data-ttu-id="346a3-343"><dt><strong>ERROR_CHANGING_PASSWORD</strong></dt> <dt>709</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-343"><dt><strong>ERROR_CHANGING_PASSWORD</strong></dt> <dt>709</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-344">Une erreur s’est produite lors de la tentative de modification du mot de passe sur le domaine.</span><span class="sxs-lookup"><span data-stu-id="346a3-344">An error occurred while attempting to change the password on the domain.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_OVERRUN"></span><span id="error_overrun"></span><dl> <span data-ttu-id="346a3-345"><dt><strong>ERROR_OVERRUN</strong></dt> <dt>710</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-345"><dt><strong>ERROR_OVERRUN</strong></dt> <dt>710</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-346">Des erreurs de dépassement de série ont été détectées lors de la communication avec votre modem.</span><span class="sxs-lookup"><span data-stu-id="346a3-346">Serial overrun errors were detected while communicating with your modem.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_RASMAN_CANNOT_INITIALIZE"></span><span id="error_rasman_cannot_initialize"></span><dl> <span data-ttu-id="346a3-347"><dt><strong>ERROR_RASMAN_CANNOT_INITIALIZE</strong></dt> <dt>711</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-347"><dt><strong>ERROR_RASMAN_CANNOT_INITIALIZE</strong></dt> <dt>711</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-348">Échec de l’initialisation de RasMan.</span><span class="sxs-lookup"><span data-stu-id="346a3-348">RasMan initialization failure.</span></span> <span data-ttu-id="346a3-349">Vérifiez le journal des événements.</span><span class="sxs-lookup"><span data-stu-id="346a3-349">Check the event log.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_BIPLEX_PORT_NOT_AVAILABLE"></span><span id="error_biplex_port_not_available"></span><dl> <span data-ttu-id="346a3-350"><dt><strong>ERROR_BIPLEX_PORT_NOT_AVAILABLE</strong></dt> <dt>712</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-350"><dt><strong>ERROR_BIPLEX_PORT_NOT_AVAILABLE</strong></dt> <dt>712</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-351">Le port bidirectionnel est en cours d’initialisation.</span><span class="sxs-lookup"><span data-stu-id="346a3-351">The two-way port is initializing.</span></span> <span data-ttu-id="346a3-352">Patientez quelques secondes et recomposez.</span><span class="sxs-lookup"><span data-stu-id="346a3-352">Wait a few seconds and redial.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-353">Déconseillé dans Windows Vista et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-353">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NO_ACTIVE_ISDN_LINES"></span><span id="error_no_active_isdn_lines"></span><dl> <span data-ttu-id="346a3-354"><dt><strong>ERROR_NO_ACTIVE_ISDN_LINES</strong></dt> <dt>713</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-354"><dt><strong>ERROR_NO_ACTIVE_ISDN_LINES</strong></dt> <dt>713</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-355">Aucune ligne RNIS active n’est disponible.</span><span class="sxs-lookup"><span data-stu-id="346a3-355">No active ISDN lines are available.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_ISDN_CHANNELS_AVAILABLE"></span><span id="error_no_isdn_channels_available"></span><dl> <span data-ttu-id="346a3-356"><dt><strong>ERROR_NO_ISDN_CHANNELS_AVAILABLE</strong></dt> <dt>714</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-356"><dt><strong>ERROR_NO_ISDN_CHANNELS_AVAILABLE</strong></dt> <dt>714</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-357">Aucun canal RNIS n’est disponible pour effectuer l’appel.</span><span class="sxs-lookup"><span data-stu-id="346a3-357">No ISDN channels are available to make the call.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-358">Déconseillé dans Windows Vista et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-358">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_TOO_MANY_LINE_ERRORS"></span><span id="error_too_many_line_errors"></span><dl> <span data-ttu-id="346a3-359"><dt><strong>ERROR_TOO_MANY_LINE_ERRORS</strong></dt> <dt>715</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-359"><dt><strong>ERROR_TOO_MANY_LINE_ERRORS</strong></dt> <dt>715</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-360">Trop d’erreurs se sont produites en raison d’une mauvaise qualité de ligne téléphonique.</span><span class="sxs-lookup"><span data-stu-id="346a3-360">Too many errors occurred because of poor phone line quality.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-361">Déconseillé dans Windows Vista et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-361">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_IP_CONFIGURATION"></span><span id="error_ip_configuration"></span><dl> <span data-ttu-id="346a3-362"><dt><strong>ERROR_IP_CONFIGURATION</strong></dt> <dt>716</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-362"><dt><strong>ERROR_IP_CONFIGURATION</strong></dt> <dt>716</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-363">La configuration IP d’accès à distance est inutilisable.</span><span class="sxs-lookup"><span data-stu-id="346a3-363">The remote access IP configuration is unusable.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NO_IP_ADDRESSES"></span><span id="error_no_ip_addresses"></span><dl> <span data-ttu-id="346a3-364"><dt><strong>ERROR_NO_IP_ADDRESSES</strong></dt> <dt>717</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-364"><dt><strong>ERROR_NO_IP_ADDRESSES</strong></dt> <dt>717</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-365">Aucune adresse IP n’est disponible dans le pool statique d’adresses IP d’accès à distance.</span><span class="sxs-lookup"><span data-stu-id="346a3-365">No IP addresses are available in the static pool of remote access IP addresses.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PPP_TIMEOUT"></span><span id="error_ppp_timeout"></span><dl> <span data-ttu-id="346a3-366"><dt><strong>ERROR_PPP_TIMEOUT</strong></dt> <dt>718</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-366"><dt><strong>ERROR_PPP_TIMEOUT</strong></dt> <dt>718</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-367">Un délai d’attente PPP s’est produit.</span><span class="sxs-lookup"><span data-stu-id="346a3-367">A PPP timeout occurred.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PPP_REMOTE_TERMINATED"></span><span id="error_ppp_remote_terminated"></span><dl> <span data-ttu-id="346a3-368"><dt><strong>ERROR_PPP_REMOTE_TERMINATED</strong></dt> <dt>719</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-368"><dt><strong>ERROR_PPP_REMOTE_TERMINATED</strong></dt> <dt>719</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-369">La connexion a été arrêtée par l’ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="346a3-369">The connection was terminated by the remote computer.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-370">Déconseillé dans Windows Vista et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-370">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PPP_NO_PROTOCOLS_CONFIGURED"></span><span id="error_ppp_no_protocols_configured"></span><dl> <span data-ttu-id="346a3-371"><dt><strong>ERROR_PPP_NO_PROTOCOLS_CONFIGURED</strong></dt> <dt>720</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-371"><dt><strong>ERROR_PPP_NO_PROTOCOLS_CONFIGURED</strong></dt> <dt>720</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-372">Aucun protocole de contrôle PPP n’est configuré.</span><span class="sxs-lookup"><span data-stu-id="346a3-372">No PPP control protocols are configured.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PPP_NO_RESPONSE"></span><span id="error_ppp_no_response"></span><dl> <span data-ttu-id="346a3-373"><dt><strong>ERROR_PPP_NO_RESPONSE</strong></dt> <dt>721</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-373"><dt><strong>ERROR_PPP_NO_RESPONSE</strong></dt> <dt>721</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-374">L’homologue PPP distant ne répond pas.</span><span class="sxs-lookup"><span data-stu-id="346a3-374">The remote PPP peer is not responding.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PPP_INVALID_PACKET"></span><span id="error_ppp_invalid_packet"></span><dl> <span data-ttu-id="346a3-375"><dt><strong>ERROR_PPP_INVALID_PACKET</strong></dt> <dt>722</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-375"><dt><strong>ERROR_PPP_INVALID_PACKET</strong></dt> <dt>722</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-376">Le paquet PPP n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="346a3-376">The PPP packet is not valid.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PHONE_NUMBER_TOO_LONG"></span><span id="error_phone_number_too_long"></span><dl> <span data-ttu-id="346a3-377"><dt><strong>ERROR_PHONE_NUMBER_TOO_LONG</strong></dt> <dt>723</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-377"><dt><strong>ERROR_PHONE_NUMBER_TOO_LONG</strong></dt> <dt>723</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-378">Le numéro de téléphone, y compris le préfixe et le suffixe, est trop long.</span><span class="sxs-lookup"><span data-stu-id="346a3-378">The phone number, including the prefix and suffix, is too long.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_IPXCP_NO_DIALOUT_CONFIGURED"></span><span id="error_ipxcp_no_dialout_configured"></span><dl> <span data-ttu-id="346a3-379"><dt><strong>ERROR_IPXCP_NO_DIALOUT_CONFIGURED</strong></dt> <dt>724</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-379"><dt><strong>ERROR_IPXCP_NO_DIALOUT_CONFIGURED</strong></dt> <dt>724</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-380">Le protocole IPX ne peut pas effectuer de numérotation sur le modem (ou sur un autre périphérique de connexion), car cet ordinateur n’est pas configuré pour la connexion sortante (il s’agit d’un routeur IPX).</span><span class="sxs-lookup"><span data-stu-id="346a3-380">The IPX protocol cannot dial out on the modem (or other connecting device) because this computer is not configured for dialing out (it is an IPX router).</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-381">Déconseillé dans Windows Vista et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-381">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_IPXCP_NO_DIALIN_CONFIGURED"></span><span id="error_ipxcp_no_dialin_configured"></span><dl> <span data-ttu-id="346a3-382"><dt><strong>ERROR_IPXCP_NO_DIALIN_CONFIGURED</strong></dt> <dt>725</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-382"><dt><strong>ERROR_IPXCP_NO_DIALIN_CONFIGURED</strong></dt> <dt>725</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-383">Le protocole IPX ne peut pas se connecter sur le modem (ou un autre périphérique de connexion) car cet ordinateur n’est pas configuré pour la numérotation dans (le routeur IPX n’est pas installé).</span><span class="sxs-lookup"><span data-stu-id="346a3-383">The IPX protocol cannot dial in on the modem (or other connecting device) because this computer is not configured for dialing in (the IPX router is not installed).</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-384">Déconseillé dans Windows Vista et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-384">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_IPXCP_DIALOUT_ALREADY_ACTIVE"></span><span id="error_ipxcp_dialout_already_active"></span><dl> <span data-ttu-id="346a3-385"><dt><strong>ERROR_IPXCP_DIALOUT_ALREADY_ACTIVE</strong></dt> <dt>726</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-385"><dt><strong>ERROR_IPXCP_DIALOUT_ALREADY_ACTIVE</strong></dt> <dt>726</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-386">Le protocole IPX ne peut pas être utilisé pour la numérotation à distance sur plusieurs ports à la fois.</span><span class="sxs-lookup"><span data-stu-id="346a3-386">The IPX protocol cannot be used for dial-out on more than one port at a time.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_ACCESSING_TCPCFGDLL"></span><span id="error_accessing_tcpcfgdll"></span><dl> <span data-ttu-id="346a3-387"><dt><strong>ERROR_ACCESSING_TCPCFGDLL</strong></dt> <dt>727</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-387"><dt><strong>ERROR_ACCESSING_TCPCFGDLL</strong></dt> <dt>727</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-388">Impossible d’accéder à TCPCFG.DLL.</span><span class="sxs-lookup"><span data-stu-id="346a3-388">Cannot access TCPCFG.DLL.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-389">Déconseillé dans Windows Vista et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-389">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_IP_RAS_ADAPTER"></span><span id="error_no_ip_ras_adapter"></span><dl> <span data-ttu-id="346a3-390"><dt><strong>ERROR_NO_IP_RAS_ADAPTER</strong></dt> <dt>728</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-390"><dt><strong>ERROR_NO_IP_RAS_ADAPTER</strong></dt> <dt>728</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-391">Impossible de trouver une carte IP liée à l’accès à distance.</span><span class="sxs-lookup"><span data-stu-id="346a3-391">Cannot find an IP adapter bound to remote access.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SLIP_REQUIRES_IP"></span><span id="error_slip_requires_ip"></span><dl> <span data-ttu-id="346a3-392"><dt><strong>ERROR_SLIP_REQUIRES_IP</strong></dt> <dt>729</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-392"><dt><strong>ERROR_SLIP_REQUIRES_IP</strong></dt> <dt>729</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-393">SLIP ne peut pas être utilisé tant que le protocole IP n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="346a3-393">SLIP cannot be used unless the IP protocol is installed.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PROJECTION_NOT_COMPLETE"></span><span id="error_projection_not_complete"></span><dl> <span data-ttu-id="346a3-394"><dt><strong>ERROR_PROJECTION_NOT_COMPLETE</strong></dt> <dt>730</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-394"><dt><strong>ERROR_PROJECTION_NOT_COMPLETE</strong></dt> <dt>730</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-395">L’inscription de l’ordinateur n’est pas terminée.</span><span class="sxs-lookup"><span data-stu-id="346a3-395">Computer registration is not complete.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-396">Déconseillé dans Windows Vista et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-396">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PROTOCOL_NOT_CONFIGURED"></span><span id="error_protocol_not_configured"></span><dl> <span data-ttu-id="346a3-397"><dt><strong>ERROR_PROTOCOL_NOT_CONFIGURED</strong></dt> <dt>731</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-397"><dt><strong>ERROR_PROTOCOL_NOT_CONFIGURED</strong></dt> <dt>731</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-398">Le protocole spécifié n’est pas configuré.</span><span class="sxs-lookup"><span data-stu-id="346a3-398">The specified protocol is not configured.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PPP_NOT_CONVERGING"></span><span id="error_ppp_not_converging"></span><dl> <span data-ttu-id="346a3-399"><dt><strong>ERROR_PPP_NOT_CONVERGING</strong></dt> <dt>732</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-399"><dt><strong>ERROR_PPP_NOT_CONVERGING</strong></dt> <dt>732</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-400">La négociation PPP ne converge pas.</span><span class="sxs-lookup"><span data-stu-id="346a3-400">The PPP negotiation is not converging.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PPP_CP_REJECTED"></span><span id="error_ppp_cp_rejected"></span><dl> <span data-ttu-id="346a3-401"><dt><strong>ERROR_PPP_CP_REJECTED</strong></dt> <dt>733</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-401"><dt><strong>ERROR_PPP_CP_REJECTED</strong></dt> <dt>733</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-402">le protocole de contrôle PPP du protocole réseau spécifié n’est pas disponible sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="346a3-402">the PPP control protocol for the specified network protocol is not available on the server.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PPP_LCP_TERMINATED"></span><span id="error_ppp_lcp_terminated"></span><dl> <span data-ttu-id="346a3-403"><dt><strong>ERROR_PPP_LCP_TERMINATED</strong></dt> <dt>734</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-403"><dt><strong>ERROR_PPP_LCP_TERMINATED</strong></dt> <dt>734</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-404">Le protocole de contrôle de liaison PPP a été arrêté.</span><span class="sxs-lookup"><span data-stu-id="346a3-404">The PPP link control protocol was terminated.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PPP_REQUIRED_ADDRESS_REJECTED"></span><span id="error_ppp_required_address_rejected"></span><dl> <span data-ttu-id="346a3-405"><dt><strong>ERROR_PPP_REQUIRED_ADDRESS_REJECTED</strong></dt> <dt>735</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-405"><dt><strong>ERROR_PPP_REQUIRED_ADDRESS_REJECTED</strong></dt> <dt>735</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-406">L’adresse demandée a été rejetée par le serveur.</span><span class="sxs-lookup"><span data-stu-id="346a3-406">The requested address was rejected by the server.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PPP_NCP_TERMINATED"></span><span id="error_ppp_ncp_terminated"></span><dl> <span data-ttu-id="346a3-407"><dt><strong>ERROR_PPP_NCP_TERMINATED</strong></dt> <dt>736</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-407"><dt><strong>ERROR_PPP_NCP_TERMINATED</strong></dt> <dt>736</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-408">L’ordinateur distant a mis fin au protocole de contrôle.</span><span class="sxs-lookup"><span data-stu-id="346a3-408">The remote computer terminated the control protocol.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PPP_LOOPBACK_DETECTED"></span><span id="error_ppp_loopback_detected"></span><dl> <span data-ttu-id="346a3-409"><dt><strong>ERROR_PPP_LOOPBACK_DETECTED</strong></dt> <dt>737</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-409"><dt><strong>ERROR_PPP_LOOPBACK_DETECTED</strong></dt> <dt>737</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-410">Bouclage détecté.</span><span class="sxs-lookup"><span data-stu-id="346a3-410">Loopback detected.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PPP_NO_ADDRESS_ASSIGNED"></span><span id="error_ppp_no_address_assigned"></span><dl> <span data-ttu-id="346a3-411"><dt><strong>ERROR_PPP_NO_ADDRESS_ASSIGNED</strong></dt> <dt>738</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-411"><dt><strong>ERROR_PPP_NO_ADDRESS_ASSIGNED</strong></dt> <dt>738</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-412">Le serveur n’a pas attribué d’adresse.</span><span class="sxs-lookup"><span data-stu-id="346a3-412">The server did not assign an address.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CANNOT_USE_LOGON_CREDENTIALS"></span><span id="error_cannot_use_logon_credentials"></span><dl> <span data-ttu-id="346a3-413"><dt><strong>ERROR_CANNOT_USE_LOGON_CREDENTIALS</strong></dt> <dt>739</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-413"><dt><strong>ERROR_CANNOT_USE_LOGON_CREDENTIALS</strong></dt> <dt>739</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-414">Le serveur distant ne peut pas utiliser le mot de passe chiffré Windows NT.</span><span class="sxs-lookup"><span data-stu-id="346a3-414">The remote server cannot use the Windows NT encrypted password.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_TAPI_CONFIGURATION"></span><span id="error_tapi_configuration"></span><dl> <span data-ttu-id="346a3-415"><dt><strong>ERROR_TAPI_CONFIGURATION</strong></dt> <dt>740</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-415"><dt><strong>ERROR_TAPI_CONFIGURATION</strong></dt> <dt>740</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-416">Les périphériques TAPI configurés pour l’accès à distance n’ont pas pu être initialisés ou n’ont pas été installés correctement.</span><span class="sxs-lookup"><span data-stu-id="346a3-416">The TAPI devices configured for remote access failed to initialize or were not installed correctly.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NO_LOCAL_ENCRYPTION"></span><span id="error_no_local_encryption"></span><dl> <span data-ttu-id="346a3-417"><dt><strong>ERROR_NO_LOCAL_ENCRYPTION</strong></dt> <dt>741</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-417"><dt><strong>ERROR_NO_LOCAL_ENCRYPTION</strong></dt> <dt>741</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-418">L’ordinateur local ne prend pas en charge le chiffrement.</span><span class="sxs-lookup"><span data-stu-id="346a3-418">The local computer does not support encryption.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_REMOTE_ENCRYPTION"></span><span id="error_no_remote_encryption"></span><dl> <span data-ttu-id="346a3-419"><dt><strong>ERROR_NO_REMOTE_ENCRYPTION</strong></dt> <dt>742</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-419"><dt><strong>ERROR_NO_REMOTE_ENCRYPTION</strong></dt> <dt>742</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-420">Le serveur distant ne prend pas en charge le chiffrement.</span><span class="sxs-lookup"><span data-stu-id="346a3-420">The remote server does not support encryption.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_REMOTE_REQUIRES_ENCRYPTION"></span><span id="error_remote_requires_encryption"></span><dl> <span data-ttu-id="346a3-421"><dt><strong>ERROR_REMOTE_REQUIRES_ENCRYPTION</strong></dt> <dt>743</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-421"><dt><strong>ERROR_REMOTE_REQUIRES_ENCRYPTION</strong></dt> <dt>743</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-422">L’ordinateur distant requiert le chiffrement des données.</span><span class="sxs-lookup"><span data-stu-id="346a3-422">The remote computer requires data encryption.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-423">Déconseillé dans Windows Vista et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-423">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_IPXCP_NET_NUMBER_CONFLICT"></span><span id="error_ipxcp_net_number_conflict"></span><dl> <span data-ttu-id="346a3-424"><dt><strong>ERROR_IPXCP_NET_NUMBER_CONFLICT</strong></dt> <dt>744</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-424"><dt><strong>ERROR_IPXCP_NET_NUMBER_CONFLICT</strong></dt> <dt>744</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-425">Le système ne peut pas utiliser le numéro de réseau IPX attribué par l’ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="346a3-425">The system cannot use the IPX network number assigned by the remote computer.</span></span> <span data-ttu-id="346a3-426">Des informations supplémentaires sont fournies dans le journal des événements.</span><span class="sxs-lookup"><span data-stu-id="346a3-426">Additional information is provided in the event log.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-427">Déconseillé dans Windows Vista et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-427">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_SMM"></span><span id="error_invalid_smm"></span><dl> <span data-ttu-id="346a3-428"><dt><strong>ERROR_INVALID_SMM</strong></dt> <dt>745</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-428"><dt><strong>ERROR_INVALID_SMM</strong></dt> <dt>745</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-429">Le module de gestion de session (SMM) n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="346a3-429">The Session Management Module (SMM) is not valid.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-430">Déconseillé dans Windows Vista et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-430">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_SMM_UNINITIALIZED"></span><span id="error_smm_uninitialized"></span><dl> <span data-ttu-id="346a3-431"><dt><strong>ERROR_SMM_UNINITIALIZED</strong></dt> <dt>746</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-431"><dt><strong>ERROR_SMM_UNINITIALIZED</strong></dt> <dt>746</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-432">Le SMM n’est pas initialisé.</span><span class="sxs-lookup"><span data-stu-id="346a3-432">The SMM is uninitialized.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-433">Déconseillé dans Windows Vista et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-433">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NO_MAC_FOR_PORT"></span><span id="error_no_mac_for_port"></span><dl> <span data-ttu-id="346a3-434"><dt><strong>ERROR_NO_MAC_FOR_PORT</strong></dt> <dt>747</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-434"><dt><strong>ERROR_NO_MAC_FOR_PORT</strong></dt> <dt>747</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-435">Aucun MAC pour le port.</span><span class="sxs-lookup"><span data-stu-id="346a3-435">No MAC for port.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-436">Déconseillé dans Windows Vista et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-436">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_SMM_TIMEOUT"></span><span id="error_smm_timeout"></span><dl> <span data-ttu-id="346a3-437"><dt><strong>ERROR_SMM_TIMEOUT</strong></dt> <dt>748</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-437"><dt><strong>ERROR_SMM_TIMEOUT</strong></dt> <dt>748</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-438">Le SMM a dépassé le délai d’attente.</span><span class="sxs-lookup"><span data-stu-id="346a3-438">The SMM timed out.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-439">Déconseillé dans Windows Vista et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-439">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_BAD_PHONE_NUMBER"></span><span id="error_bad_phone_number"></span><dl> <span data-ttu-id="346a3-440"><dt><strong>ERROR_BAD_PHONE_NUMBER</strong></dt> <dt>749</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-440"><dt><strong>ERROR_BAD_PHONE_NUMBER</strong></dt> <dt>749</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-441">Un numéro de téléphone incorrect a été spécifié.</span><span class="sxs-lookup"><span data-stu-id="346a3-441">A bad phone number was specified.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_WRONG_MODULE"></span><span id="error_wrong_module"></span><dl> <span data-ttu-id="346a3-442"><dt><strong>ERROR_WRONG_MODULE</strong></dt> <dt>750</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-442"><dt><strong>ERROR_WRONG_MODULE</strong></dt> <dt>750</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-443">Le mauvais SMM a été spécifié.</span><span class="sxs-lookup"><span data-stu-id="346a3-443">The wrong SMM was specified.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-444">Déconseillé dans Windows Vista et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-444">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_CALLBACK_NUMBER"></span><span id="error_invalid_callback_number"></span><dl> <span data-ttu-id="346a3-445"><dt><strong>ERROR_INVALID_CALLBACK_NUMBER</strong></dt> <dt>751</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-445"><dt><strong>ERROR_INVALID_CALLBACK_NUMBER</strong></dt> <dt>751</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-446">Le numéro de rappel contient un caractère qui n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="346a3-446">The callback number contains a character that is not valid.</span></span> <span data-ttu-id="346a3-447">Seuls les 18 caractères suivants sont autorisés : de 0 à 9, T, P, W, (,),-, @ et Space.</span><span class="sxs-lookup"><span data-stu-id="346a3-447">Only the following 18 characters are allowed: 0 to 9, T, P, W, (, ), -, @, and space.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-448">Déconseillé dans Windows Vista et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-448">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_SCRIPT_SYNTAX"></span><span id="error_script_syntax"></span><dl> <span data-ttu-id="346a3-449"><dt><strong>ERROR_SCRIPT_SYNTAX</strong></dt> <dt>752</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-449"><dt><strong>ERROR_SCRIPT_SYNTAX</strong></dt> <dt>752</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-450">Une erreur de syntaxe s’est produite lors du traitement d’un script.</span><span class="sxs-lookup"><span data-stu-id="346a3-450">A syntax error was encountered while processing a script.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_HANGUP_FAILED"></span><span id="error_hangup_failed"></span><dl> <span data-ttu-id="346a3-451"><dt><strong>ERROR_HANGUP_FAILED</strong></dt> <dt>753</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-451"><dt><strong>ERROR_HANGUP_FAILED</strong></dt> <dt>753</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-452">La connexion n’a pas pu être déconnectée, car elle a été créée par le routeur multiprotocole.</span><span class="sxs-lookup"><span data-stu-id="346a3-452">The connection could not be disconnected because it was created by the multi-protocol router.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_BUNDLE_NOT_FOUND"></span><span id="error_bundle_not_found"></span><dl> <span data-ttu-id="346a3-453"><dt><strong>ERROR_BUNDLE_NOT_FOUND</strong></dt> <dt>754</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-453"><dt><strong>ERROR_BUNDLE_NOT_FOUND</strong></dt> <dt>754</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-454">Le système n’a pas pu trouver le bundle à liaisons multiples.</span><span class="sxs-lookup"><span data-stu-id="346a3-454">The system could not find the multi-link bundle.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CANNOT_DO_CUSTOMDIAL"></span><span id="error_cannot_do_customdial"></span><dl> <span data-ttu-id="346a3-455"><dt><strong>ERROR_CANNOT_DO_CUSTOMDIAL</strong></dt> <dt>755</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-455"><dt><strong>ERROR_CANNOT_DO_CUSTOMDIAL</strong></dt> <dt>755</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-456">Le système ne peut pas effectuer la numérotation automatique, car un numéroteur personnalisé a été spécifié pour cette connexion.</span><span class="sxs-lookup"><span data-stu-id="346a3-456">The system cannot perform automated dial because this connection has a custom dialer specified.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DIAL_ALREADY_IN_PROGRESS"></span><span id="error_dial_already_in_progress"></span><dl> <span data-ttu-id="346a3-457"><dt><strong>ERROR_DIAL_ALREADY_IN_PROGRESS</strong></dt> <dt>756</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-457"><dt><strong>ERROR_DIAL_ALREADY_IN_PROGRESS</strong></dt> <dt>756</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-458">Cette connexion est déjà en cours de numérotation.</span><span class="sxs-lookup"><span data-stu-id="346a3-458">This connection is already being dialed.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_RASAUTO_CANNOT_INITIALIZE"></span><span id="error_rasauto_cannot_initialize"></span><dl> <span data-ttu-id="346a3-459"><dt><strong>ERROR_RASAUTO_CANNOT_INITIALIZE</strong></dt> <dt>757</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-459"><dt><strong>ERROR_RASAUTO_CANNOT_INITIALIZE</strong></dt> <dt>757</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-460">RAS n’a pas pu être démarré automatiquement.</span><span class="sxs-lookup"><span data-stu-id="346a3-460">RAS could not be started automatically.</span></span> <span data-ttu-id="346a3-461">Des informations supplémentaires sont fournies dans le journal des événements.</span><span class="sxs-lookup"><span data-stu-id="346a3-461">Additional information is provided in the event log.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_CONNECTION_ALREADY_SHARED"></span><span id="error_connection_already_shared"></span><dl> <span data-ttu-id="346a3-462"><dt><strong>ERROR_CONNECTION_ALREADY_SHARED</strong></dt> <dt>758</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-462"><dt><strong>ERROR_CONNECTION_ALREADY_SHARED</strong></dt> <dt>758</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-463">Le partage de connexion Internet (ICS) est déjà activé sur la connexion.</span><span class="sxs-lookup"><span data-stu-id="346a3-463">Internet Connection Sharing (ICS) is already enabled on the connection.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-464">Déconseillé dans Windows Vista et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-464">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SHARING_CHANGE_FAILED"></span><span id="error_sharing_change_failed"></span><dl> <span data-ttu-id="346a3-465"><dt><strong>ERROR_SHARING_CHANGE_FAILED</strong></dt> <dt>759</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-465"><dt><strong>ERROR_SHARING_CHANGE_FAILED</strong></dt> <dt>759</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-466">Une erreur s’est produite lors de la modification des paramètres de partage de connexion Internet existants.</span><span class="sxs-lookup"><span data-stu-id="346a3-466">An error occurred while the existing Internet Connection Sharing settings were being changed.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-467">Déconseillé dans Windows Vista et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-467">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_SHARING_ROUTER_INSTALL"></span><span id="error_sharing_router_install"></span><dl> <span data-ttu-id="346a3-468"><dt><strong>ERROR_SHARING_ROUTER_INSTALL</strong></dt> <dt>760</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-468"><dt><strong>ERROR_SHARING_ROUTER_INSTALL</strong></dt> <dt>760</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-469">Une erreur s’est produite lors de l’activation des fonctionnalités de routage.</span><span class="sxs-lookup"><span data-stu-id="346a3-469">An error occurred while routing capabilities were being enabled.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-470">Déconseillé dans Windows Vista et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-470">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SHARE_CONNECTION_FAILED"></span><span id="error_share_connection_failed"></span><dl> <span data-ttu-id="346a3-471"><dt><strong>ERROR_SHARE_CONNECTION_FAILED</strong></dt> <dt>761</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-471"><dt><strong>ERROR_SHARE_CONNECTION_FAILED</strong></dt> <dt>761</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-472">Une erreur s’est produite lors de l’activation du partage de connexion Internet pour la connexion.</span><span class="sxs-lookup"><span data-stu-id="346a3-472">An error occurred while Internet Connection Sharing was being enabled for the connection.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-473">Déconseillé dans Windows Vista et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-473">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="7ERROR_SHARING_PRIVATE_INSTALL64"></span><span id="7error_sharing_private_install64"></span><dl> <span data-ttu-id="346a3-474"><dt><strong>7ERROR_SHARING_PRIVATE_INSTALL64</strong></dt> <dt>762</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-474"><dt><strong>7ERROR_SHARING_PRIVATE_INSTALL64</strong></dt> <dt>762</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-475">Une erreur s’est produite lors de la configuration du réseau local pour le partage.</span><span class="sxs-lookup"><span data-stu-id="346a3-475">An error occurred while the local network was being configured for sharing.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-476">Déconseillé dans Windows Vista et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-476">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CANNOT_SHARE_CONNECTION"></span><span id="error_cannot_share_connection"></span><dl> <span data-ttu-id="346a3-477"><dt><strong>ERROR_CANNOT_SHARE_CONNECTION</strong></dt> <dt>763</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-477"><dt><strong>ERROR_CANNOT_SHARE_CONNECTION</strong></dt> <dt>763</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-478">Impossible d’activer le partage de connexion Internet.</span><span class="sxs-lookup"><span data-stu-id="346a3-478">Internet Connection Sharing cannot be enabled.</span></span> <span data-ttu-id="346a3-479">Il y a plus d’une connexion LAN autre que la connexion à partager.</span><span class="sxs-lookup"><span data-stu-id="346a3-479">There is more than one LAN connection other than the connection to be shared.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-480">Déconseillé dans Windows Vista et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-480">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_SMART_CARD_READER"></span><span id="error_no_smart_card_reader"></span><dl> <span data-ttu-id="346a3-481"><dt><strong>ERROR_NO_SMART_CARD_READER</strong></dt> <dt>764</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-481"><dt><strong>ERROR_NO_SMART_CARD_READER</strong></dt> <dt>764</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-482">Aucun lecteur de carte à puce n’est installé.</span><span class="sxs-lookup"><span data-stu-id="346a3-482">No smart card reader is installed.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SHARING_ADDRESS_EXISTS"></span><span id="error_sharing_address_exists"></span><dl> <span data-ttu-id="346a3-483"><dt><strong>ERROR_SHARING_ADDRESS_EXISTS</strong></dt> <dt>765</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-483"><dt><strong>ERROR_SHARING_ADDRESS_EXISTS</strong></dt> <dt>765</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-484">Impossible d’activer le partage de connexion Internet.</span><span class="sxs-lookup"><span data-stu-id="346a3-484">Internet Connection Sharing cannot be enabled.</span></span> <span data-ttu-id="346a3-485">Une connexion au réseau local est déjà configurée avec l’adresse IP requise pour l’adressage IP automatique.</span><span class="sxs-lookup"><span data-stu-id="346a3-485">A LAN connection is already configured with the IP address that is required for automatic IP addressing.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_CERTIFICATE"></span><span id="error_no_certificate"></span><dl> <span data-ttu-id="346a3-486"><dt><strong>ERROR_NO_CERTIFICATE</strong></dt> <dt>766</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-486"><dt><strong>ERROR_NO_CERTIFICATE</strong></dt> <dt>766</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-487">Un certificat est introuvable.</span><span class="sxs-lookup"><span data-stu-id="346a3-487">A certificate could not be found.</span></span> <span data-ttu-id="346a3-488">Les connexions qui utilisent le protocole L2TP sur IPSec nécessitent l’installation d’un certificat d’ordinateur, également appelé certificat d’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="346a3-488">Connections that use the L2TP protocol over IPSec require the installation of a machine certificate, also known as a computer certificate.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SHARING_MULTIPLE_ADDRESSES"></span><span id="error_sharing_multiple_addresses"></span><dl> <span data-ttu-id="346a3-489"><dt><strong>ERROR_SHARING_MULTIPLE_ADDRESSES</strong></dt> <dt>767</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-489"><dt><strong>ERROR_SHARING_MULTIPLE_ADDRESSES</strong></dt> <dt>767</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-490">Impossible d’activer le partage de connexion Internet.</span><span class="sxs-lookup"><span data-stu-id="346a3-490">Internet Connection Sharing cannot be enabled.</span></span> <span data-ttu-id="346a3-491">Plus d’une adresse IP est configurée pour la connexion LAN sélectionnée en tant que réseau privé.</span><span class="sxs-lookup"><span data-stu-id="346a3-491">The LAN connection selected as the private network has more than one IP address configured.</span></span> <span data-ttu-id="346a3-492">Reconfigurez la connexion LAN avec une seule adresse IP avant d’activer le partage de connexion Internet.</span><span class="sxs-lookup"><span data-stu-id="346a3-492">Please reconfigure the LAN connection with a single IP address before enabling Internet Connection Sharing.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_FAILED_TO_ENCRYPT"></span><span id="error_failed_to_encrypt"></span><dl> <span data-ttu-id="346a3-493"><dt><strong>ERROR_FAILED_TO_ENCRYPT</strong></dt> <dt>768</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-493"><dt><strong>ERROR_FAILED_TO_ENCRYPT</strong></dt> <dt>768</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-494">La tentative de connexion a échoué en raison d’un échec de chiffrement des données.</span><span class="sxs-lookup"><span data-stu-id="346a3-494">The connection attempt failed because of failure to encrypt data.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_BAD_ADDRESS_SPECIFIED"></span><span id="error_bad_address_specified"></span><dl> <span data-ttu-id="346a3-495"><dt><strong>ERROR_BAD_ADDRESS_SPECIFIED</strong></dt> <dt>769</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-495"><dt><strong>ERROR_BAD_ADDRESS_SPECIFIED</strong></dt> <dt>769</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-496">La destination spécifiée n’est pas accessible.</span><span class="sxs-lookup"><span data-stu-id="346a3-496">The specified destination is not reachable.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_CONNECTION_REJECT"></span><span id="error_connection_reject"></span><dl> <span data-ttu-id="346a3-497"><dt><strong>ERROR_CONNECTION_REJECT</strong></dt> <dt>770</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-497"><dt><strong>ERROR_CONNECTION_REJECT</strong></dt> <dt>770</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-498">L’ordinateur distant a rejeté la tentative de connexion.</span><span class="sxs-lookup"><span data-stu-id="346a3-498">The remote computer rejected the connection attempt.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CONGESTION"></span><span id="error_congestion"></span><dl> <span data-ttu-id="346a3-499"><dt><strong>ERROR_CONGESTION</strong></dt> <dt>771</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-499"><dt><strong>ERROR_CONGESTION</strong></dt> <dt>771</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-500">La tentative de connexion a échoué car le réseau est occupé.</span><span class="sxs-lookup"><span data-stu-id="346a3-500">The connection attempt failed because the network is busy.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INCOMPATIBLE"></span><span id="error_incompatible"></span><dl> <span data-ttu-id="346a3-501"><dt><strong>ERROR_INCOMPATIBLE</strong></dt> <dt>772</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-501"><dt><strong>ERROR_INCOMPATIBLE</strong></dt> <dt>772</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-502">Le matériel réseau de l’ordinateur distant est incompatible avec le type d’appel demandé.</span><span class="sxs-lookup"><span data-stu-id="346a3-502">The remote computer's network hardware is incompatible with the type of call requested.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NUMBERCHANGED"></span><span id="error_numberchanged"></span><dl> <span data-ttu-id="346a3-503"><dt><strong>ERROR_NUMBERCHANGED</strong></dt> <dt>773</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-503"><dt><strong>ERROR_NUMBERCHANGED</strong></dt> <dt>773</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-504">La tentative de connexion a échoué car le numéro de destination a changé.</span><span class="sxs-lookup"><span data-stu-id="346a3-504">The connection attempt failed because the destination number has changed.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_TEMPFAILURE"></span><span id="error_tempfailure"></span><dl> <span data-ttu-id="346a3-505"><dt><strong>ERROR_TEMPFAILURE</strong></dt> <dt>774</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-505"><dt><strong>ERROR_TEMPFAILURE</strong></dt> <dt>774</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-506">La tentative de connexion a échoué en raison d’une défaillance temporaire.</span><span class="sxs-lookup"><span data-stu-id="346a3-506">The connection attempt failed because of a temporary failure.</span></span> <span data-ttu-id="346a3-507">Réessayez de vous connecter.</span><span class="sxs-lookup"><span data-stu-id="346a3-507">Try connecting again.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_BLOCKED"></span><span id="error_blocked"></span><dl> <span data-ttu-id="346a3-508"><dt><strong>ERROR_BLOCKED</strong></dt> <dt>775</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-508"><dt><strong>ERROR_BLOCKED</strong></dt> <dt>775</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-509">L’appel a été bloqué par l’ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="346a3-509">The call was blocked by the remote computer.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DONOTDISTURB"></span><span id="error_donotdisturb"></span><dl> <span data-ttu-id="346a3-510"><dt><strong>ERROR_DONOTDISTURB</strong></dt> <dt>776</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-510"><dt><strong>ERROR_DONOTDISTURB</strong></dt> <dt>776</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-511">L’appel n’a pas pu être connecté, car l’ordinateur distant a appelé la fonctionnalité ne pas déranger.</span><span class="sxs-lookup"><span data-stu-id="346a3-511">The call could not be connected because the remote computer has invoked the Do Not Disturb feature.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_OUTOFORDER"></span><span id="error_outoforder"></span><dl> <span data-ttu-id="346a3-512"><dt><strong>ERROR_OUTOFORDER</strong></dt> <dt>777</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-512"><dt><strong>ERROR_OUTOFORDER</strong></dt> <dt>777</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-513">La tentative de connexion a échoué car le modem ou un autre périphérique de connexion sur l’ordinateur distant n’est pas dans le désordre.</span><span class="sxs-lookup"><span data-stu-id="346a3-513">The connection attempt failed because the modem or other connection device on the remote computer is out of order.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_UNABLE_TO_AUTHENTICATE_SERVER"></span><span id="error_unable_to_authenticate_server"></span><dl> <span data-ttu-id="346a3-514"><dt><strong>ERROR_UNABLE_TO_AUTHENTICATE_SERVER</strong></dt> <dt>778</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-514"><dt><strong>ERROR_UNABLE_TO_AUTHENTICATE_SERVER</strong></dt> <dt>778</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-515">Il n’était pas possible de vérifier l’identité du serveur.</span><span class="sxs-lookup"><span data-stu-id="346a3-515">It was not possible to verify the identity of the server.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SMART_CARD_REQUIRED"></span><span id="error_smart_card_required"></span><dl> <span data-ttu-id="346a3-516"><dt><strong>ERROR_SMART_CARD_REQUIRED</strong></dt> <dt>779</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-516"><dt><strong>ERROR_SMART_CARD_REQUIRED</strong></dt> <dt>779</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-517">Pour effectuer une numérotation à l’aide de cette connexion, vous devez utiliser une carte à puce.</span><span class="sxs-lookup"><span data-stu-id="346a3-517">To dial out using this connection you must use a smart card.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-518">Déconseillé dans Windows Vista et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-518">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INVALID_FUNCTION_FOR_ENTRY"></span><span id="error_invalid_function_for_entry"></span><dl> <span data-ttu-id="346a3-519"><dt><strong>ERROR_INVALID_FUNCTION_FOR_ENTRY</strong></dt> <dt>780</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-519"><dt><strong>ERROR_INVALID_FUNCTION_FOR_ENTRY</strong></dt> <dt>780</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-520">Une fonction tentée n’est pas valide pour cette connexion.</span><span class="sxs-lookup"><span data-stu-id="346a3-520">An attempted function is not valid for this connection.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CERT_FOR_ENCRYPTION_NOT_FOUND"></span><span id="error_cert_for_encryption_not_found"></span><dl> <span data-ttu-id="346a3-521"><dt><strong>ERROR_CERT_FOR_ENCRYPTION_NOT_FOUND</strong></dt> <dt>781</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-521"><dt><strong>ERROR_CERT_FOR_ENCRYPTION_NOT_FOUND</strong></dt> <dt>781</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-522">La tentative de chiffrement a échoué, car aucun certificat valide n’a été trouvé.</span><span class="sxs-lookup"><span data-stu-id="346a3-522">The encryption attempt failed because no valid certificate was found.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-523">Déconseillé dans Windows Vista et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-523">Deprecated in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_SHARING_RRAS_CONFLICT"></span><span id="error_sharing_rras_conflict"></span><dl> <span data-ttu-id="346a3-524"><dt><strong>ERROR_SHARING_RRAS_CONFLICT</strong></dt> <dt>782</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-524"><dt><strong>ERROR_SHARING_RRAS_CONFLICT</strong></dt> <dt>782</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-525">Le partage de connexion (NAT) est actuellement installé en tant que protocole de routage et doit être supprimé avant d’activer le partage de connexion Internet.</span><span class="sxs-lookup"><span data-stu-id="346a3-525">Connection Sharing (NAT) is currently installed as a routing protocol, and must be removed before enabling Internet Connection Sharing.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SHARING_NO_PRIVATE_LAN"></span><span id="error_sharing_no_private_lan"></span><dl> <span data-ttu-id="346a3-526"><dt><strong>ERROR_SHARING_NO_PRIVATE_LAN</strong></dt> <dt>783</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-526"><dt><strong>ERROR_SHARING_NO_PRIVATE_LAN</strong></dt> <dt>783</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-527">Impossible d’activer le partage de connexion Internet.</span><span class="sxs-lookup"><span data-stu-id="346a3-527">Internet Connection Sharing cannot be enabled.</span></span> <span data-ttu-id="346a3-528">La connexion LAN sélectionnée en tant que réseau privé n’est pas présente ou est déconnectée du réseau.</span><span class="sxs-lookup"><span data-stu-id="346a3-528">The LAN connection selected as the private network is either not present, or is disconnected from the network.</span></span> <span data-ttu-id="346a3-529">Vérifiez que la carte réseau est connectée avant d’activer le partage de connexion Internet.</span><span class="sxs-lookup"><span data-stu-id="346a3-529">Please ensure that the LAN adapter is connected before enabling Internet Connection Sharing.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_DIFF_USER_AT_LOGON"></span><span id="error_no_diff_user_at_logon"></span><dl> <span data-ttu-id="346a3-530"><dt><strong>ERROR_NO_DIFF_USER_AT_LOGON</strong></dt> <dt>784</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-530"><dt><strong>ERROR_NO_DIFF_USER_AT_LOGON</strong></dt> <dt>784</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-531">Vous ne pouvez pas établir une connexion à l’aide de cette connexion au moment de la connexion, car elle est configurée pour utiliser un nom d’utilisateur différent de celui de la carte à puce.</span><span class="sxs-lookup"><span data-stu-id="346a3-531">You cannot dial using this connection at login time because it is configured to use a user name different than the one on the smart card.</span></span> <span data-ttu-id="346a3-532">Si vous souhaitez utiliser cette connexion au moment de la connexion, vous devez la configurer pour qu’elle utilise le nom d’utilisateur sur la carte à puce.</span><span class="sxs-lookup"><span data-stu-id="346a3-532">If you want to use this connection at login time, you must configure it to use the user name on the smart card.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NO_REG_CERT_AT_LOGON"></span><span id="error_no_reg_cert_at_logon"></span><dl> <span data-ttu-id="346a3-533"><dt><strong>ERROR_NO_REG_CERT_AT_LOGON</strong></dt> <dt>785</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-533"><dt><strong>ERROR_NO_REG_CERT_AT_LOGON</strong></dt> <dt>785</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-534">Vous ne pouvez pas établir une connexion à l’aide de cette connexion au moment de la connexion, car elle n’est pas configurée pour utiliser une carte à puce.</span><span class="sxs-lookup"><span data-stu-id="346a3-534">You cannot dial using this connection at login time because it is not configured to use a smart card.</span></span> <span data-ttu-id="346a3-535">Si vous souhaitez l’utiliser au moment de la connexion, vous devez modifier les propriétés de cette connexion pour qu’elle utilise une carte à puce.</span><span class="sxs-lookup"><span data-stu-id="346a3-535">If you want to use it at login time, you must edit the properties of this connection so that it uses a smart card.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_OAKLEY_NO_CERT"></span><span id="error_oakley_no_cert"></span><dl> <span data-ttu-id="346a3-536"><dt><strong>ERROR_OAKLEY_NO_CERT</strong></dt> <dt>786</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-536"><dt><strong>ERROR_OAKLEY_NO_CERT</strong></dt> <dt>786</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-537">La tentative de connexion L2TP a échoué, car il n’existe aucun certificat d’ordinateur valide sur votre ordinateur pour l’authentification de sécurité.</span><span class="sxs-lookup"><span data-stu-id="346a3-537">The L2TP connection attempt failed because there is no valid machine certificate on your computer for security authentication.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_OAKLEY_AUTH_FAIL"></span><span id="error_oakley_auth_fail"></span><dl> <span data-ttu-id="346a3-538"><dt><strong>ERROR_OAKLEY_AUTH_FAIL</strong></dt> <dt>787</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-538"><dt><strong>ERROR_OAKLEY_AUTH_FAIL</strong></dt> <dt>787</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-539">La tentative de connexion L2TP a échoué car la couche de sécurité n’a pas pu authentifier l’ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="346a3-539">The L2TP connection attempt failed because the security layer could not authenticate the remote computer.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_OAKLEY_ATTRIB_FAIL"></span><span id="error_oakley_attrib_fail"></span><dl> <span data-ttu-id="346a3-540"><dt><strong>ERROR_OAKLEY_ATTRIB_FAIL</strong></dt> <dt>788</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-540"><dt><strong>ERROR_OAKLEY_ATTRIB_FAIL</strong></dt> <dt>788</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-541">La tentative de connexion L2TP a échoué car la couche de sécurité n’a pas pu négocier de paramètres compatibles avec l’ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="346a3-541">The L2TP connection attempt failed because the security layer could not negotiate compatible parameters with the remote computer.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_OAKLEY_GENERAL_PROCESSING"></span><span id="error_oakley_general_processing"></span><dl> <span data-ttu-id="346a3-542"><dt><strong>ERROR_OAKLEY_GENERAL_PROCESSING</strong></dt> <dt>789</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-542"><dt><strong>ERROR_OAKLEY_GENERAL_PROCESSING</strong></dt> <dt>789</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-543">La tentative de connexion L2TP a échoué car la couche de sécurité a rencontré une erreur de traitement lors des négociations initiales avec l’ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="346a3-543">The L2TP connection attempt failed because the security layer encountered a processing error during initial negotiations with the remote computer.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_OAKLEY_NO_PEER_CERT"></span><span id="error_oakley_no_peer_cert"></span><dl> <span data-ttu-id="346a3-544"><dt><strong>ERROR_OAKLEY_NO_PEER_CERT</strong></dt> <dt>790</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-544"><dt><strong>ERROR_OAKLEY_NO_PEER_CERT</strong></dt> <dt>790</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-545">Échec de la tentative de connexion L2TP en raison de l’échec de la validation du certificat sur l’ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="346a3-545">The L2TP connection attempt failed because certificate validation on the remote computer failed.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_OAKLEY_NO_POLICY"></span><span id="error_oakley_no_policy"></span><dl> <span data-ttu-id="346a3-546"><dt><strong>ERROR_OAKLEY_NO_POLICY</strong></dt> <dt>791</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-546"><dt><strong>ERROR_OAKLEY_NO_POLICY</strong></dt> <dt>791</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-547">La tentative de connexion L2TP a échoué car la stratégie de sécurité pour la connexion est introuvable.</span><span class="sxs-lookup"><span data-stu-id="346a3-547">The L2TP connection attempt failed because security policy for the connection was not found.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_OAKLEY_TIMED_OUT"></span><span id="error_oakley_timed_out"></span><dl> <span data-ttu-id="346a3-548"><dt><strong>ERROR_OAKLEY_TIMED_OUT</strong></dt> <dt>792</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-548"><dt><strong>ERROR_OAKLEY_TIMED_OUT</strong></dt> <dt>792</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-549">La tentative de connexion L2TP a échoué car la négociation de sécurité a expiré.</span><span class="sxs-lookup"><span data-stu-id="346a3-549">The L2TP connection attempt failed because security negotiation timed out.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_OAKLEY_ERROR"></span><span id="error_oakley_error"></span><dl> <span data-ttu-id="346a3-550"><dt><strong>ERROR_OAKLEY_ERROR</strong></dt> <dt>793</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-550"><dt><strong>ERROR_OAKLEY_ERROR</strong></dt> <dt>793</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-551">La tentative de connexion L2TP a échoué car une erreur s’est produite lors de la négociation de la sécurité.</span><span class="sxs-lookup"><span data-stu-id="346a3-551">The L2TP connection attempt failed because an error occurred while negotiating security.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_UNKNOWN_FRAMED_PROTOCOL"></span><span id="error_unknown_framed_protocol"></span><dl> <span data-ttu-id="346a3-552"><dt><strong>ERROR_UNKNOWN_FRAMED_PROTOCOL</strong></dt> <dt>794</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-552"><dt><strong>ERROR_UNKNOWN_FRAMED_PROTOCOL</strong></dt> <dt>794</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-553">L’attribut RADIUS du protocole encadré pour cet utilisateur n’est pas PPP.</span><span class="sxs-lookup"><span data-stu-id="346a3-553">The Framed Protocol RADIUS attribute for this user is not PPP.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_WRONG_TUNNEL_TYPE"></span><span id="error_wrong_tunnel_type"></span><dl> <span data-ttu-id="346a3-554"><dt><strong>ERROR_WRONG_TUNNEL_TYPE</strong></dt> <dt>795</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-554"><dt><strong>ERROR_WRONG_TUNNEL_TYPE</strong></dt> <dt>795</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-555">L’attribut RADIUS du type de tunnel pour cet utilisateur n’est pas correct.</span><span class="sxs-lookup"><span data-stu-id="346a3-555">The Tunnel Type RADIUS attribute for this user is not correct.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_UNKNOWN_SERVICE_TYPE"></span><span id="error_unknown_service_type"></span><dl> <span data-ttu-id="346a3-556"><dt><strong>ERROR_UNKNOWN_SERVICE_TYPE</strong></dt> <dt>796</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-556"><dt><strong>ERROR_UNKNOWN_SERVICE_TYPE</strong></dt> <dt>796</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-557">L’attribut RADIUS du type de service pour cet utilisateur n’est ni encadré, ni rappelé.</span><span class="sxs-lookup"><span data-stu-id="346a3-557">The Service Type RADIUS attribute for this user is neither Framed nor Callback Framed.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CONNECTING_DEVICE_NOT_FOUND"></span><span id="error_connecting_device_not_found"></span><dl> <span data-ttu-id="346a3-558"><dt><strong>ERROR_CONNECTING_DEVICE_NOT_FOUND</strong></dt> <dt>797</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-558"><dt><strong>ERROR_CONNECTING_DEVICE_NOT_FOUND</strong></dt> <dt>797</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-559">Impossible d’établir une connexion à l’ordinateur distant, car le modem est introuvable ou était occupé.</span><span class="sxs-lookup"><span data-stu-id="346a3-559">A connection to the remote computer could not be established because the modem was not found or was busy.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_EAPTLS_CERTIFICATE"></span><span id="error_no_eaptls_certificate"></span><dl> <span data-ttu-id="346a3-560"><dt><strong>ERROR_NO_EAPTLS_CERTIFICATE</strong></dt> <dt>798</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-560"><dt><strong>ERROR_NO_EAPTLS_CERTIFICATE</strong></dt> <dt>798</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-561">Impossible de trouver un certificat pouvant être utilisé avec le protocole EAP (Extensible Authentication Protocol).</span><span class="sxs-lookup"><span data-stu-id="346a3-561">A certificate could not be found that can be used with the Extensible Authentication Protocol (EAP).</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SHARING_HOST_ADDRESS_CONFLICT"></span><span id="error_sharing_host_address_conflict"></span><dl> <span data-ttu-id="346a3-562"><dt><strong>ERROR_SHARING_HOST_ADDRESS_CONFLICT</strong></dt> <dt>799</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-562"><dt><strong>ERROR_SHARING_HOST_ADDRESS_CONFLICT</strong></dt> <dt>799</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-563">Le partage de connexion Internet (ICS) ne peut pas être activé en raison d’un conflit d’adresse IP sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="346a3-563">Internet Connection Sharing (ICS) cannot be enabled due to an IP address conflict on the network.</span></span> <span data-ttu-id="346a3-564">ICS nécessite que l’hôte soit configuré pour utiliser <strong>192.168.0.1</strong>.</span><span class="sxs-lookup"><span data-stu-id="346a3-564">ICS requires the host be configured to use <strong>192.168.0.1</strong>.</span></span> <span data-ttu-id="346a3-565">Assurez-vous qu’aucun autre client sur le réseau n’est configuré pour utiliser <strong>192.168.0.1</strong>.</span><span class="sxs-lookup"><span data-stu-id="346a3-565">Ensure that no other client on the network is configured to use <strong>192.168.0.1</strong>.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-566">Pris en charge dans Windows XP et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-566">Supported in Windows XP and later versions of Windows.</span></span>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-567">Windows 7 et versions ultérieures : l’ordinateur hôte doit être configuré pour utiliser <strong>192.168.137.1</strong>
</span><span class="sxs-lookup"><span data-stu-id="346a3-567">Windows 7 and later: The host must be configured to use <strong>192.168.137.1</strong>
</span></span></blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_AUTOMATIC_VPN_FAILED"></span><span id="error_automatic_vpn_failed"></span><dl> <span data-ttu-id="346a3-568"><dt><strong>ERROR_AUTOMATIC_VPN_FAILED</strong></dt> <dt>800</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-568"><dt><strong>ERROR_AUTOMATIC_VPN_FAILED</strong></dt> <dt>800</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-569">Impossible d’établir la connexion VPN.</span><span class="sxs-lookup"><span data-stu-id="346a3-569">Unable to establish the VPN connection.</span></span> <span data-ttu-id="346a3-570">Le serveur VPN est peut-être inaccessible ou les paramètres de sécurité ne sont peut-être pas configurés correctement pour cette connexion.</span><span class="sxs-lookup"><span data-stu-id="346a3-570">The VPN server may be unreachable, or security parameters may not be configured properly for this connection.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-571">Pris en charge dans Windows XP et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-571">Supported in Windows XP and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_VALIDATING_SERVER_CERT"></span><span id="error_validating_server_cert"></span><dl> <span data-ttu-id="346a3-572"><dt><strong>ERROR_VALIDATING_SERVER_CERT</strong></dt> <dt>801</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-572"><dt><strong>ERROR_VALIDATING_SERVER_CERT</strong></dt> <dt>801</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-573">Cette connexion est configurée pour valider l’identité du serveur d’accès, mais Windows ne peut pas vérifier le certificat numérique envoyé par le serveur.</span><span class="sxs-lookup"><span data-stu-id="346a3-573">This connection is configured to validate the identity of the access server, but Windows cannot verify the digital certificate sent by the server.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-574">Pris en charge dans Windows XP et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-574">Supported in Windows XP and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_READING_SCARD"></span><span id="error_reading_scard"></span><dl> <span data-ttu-id="346a3-575"><dt><strong>ERROR_READING_SCARD</strong></dt> <dt>802</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-575"><dt><strong>ERROR_READING_SCARD</strong></dt> <dt>802</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-576">La carte fournie n’a pas été reconnue.</span><span class="sxs-lookup"><span data-stu-id="346a3-576">The card supplied was not recognized.</span></span> <span data-ttu-id="346a3-577">Vérifiez que la carte est insérée correctement et qu’elle s’adapte en toute sécurité.</span><span class="sxs-lookup"><span data-stu-id="346a3-577">Please check that the card is inserted correctly, and fits securely.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-578">Pris en charge dans Windows XP avec SP1 et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-578">Supported in Windows XP with SP1 and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_PEAP_COOKIE_CONFIG"></span><span id="error_invalid_peap_cookie_config"></span><dl> <span data-ttu-id="346a3-579"><dt><strong>ERROR_INVALID_PEAP_COOKIE_CONFIG</strong></dt> <dt>803</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-579"><dt><strong>ERROR_INVALID_PEAP_COOKIE_CONFIG</strong></dt> <dt>803</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-580">La configuration PEAP stockée dans le cookie de session ne correspond pas à la configuration de la session active.</span><span class="sxs-lookup"><span data-stu-id="346a3-580">The PEAP configuration stored in the session cookie does not match the current session configuration.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-581">Pris en charge dans Windows XP avec SP1 et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-581">Supported in Windows XP with SP1 and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INVALID_PEAP_COOKIE_USER"></span><span id="error_invalid_peap_cookie_user"></span><dl> <span data-ttu-id="346a3-582"><dt><strong>ERROR_INVALID_PEAP_COOKIE_USER</strong></dt> <dt>804</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-582"><dt><strong>ERROR_INVALID_PEAP_COOKIE_USER</strong></dt> <dt>804</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-583">L’identité PEAP stockée dans le cookie de session ne correspond pas à l’identité actuelle.</span><span class="sxs-lookup"><span data-stu-id="346a3-583">The PEAP identity stored in the session cookie does not match the current identity.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-584">Pris en charge dans Windows XP avec SP1 et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-584">Supported in Windows XP with SP1 and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_MSCHAPV2_CONFIG"></span><span id="error_invalid_mschapv2_config"></span><dl> <span data-ttu-id="346a3-585"><dt><strong>ERROR_INVALID_MSCHAPV2_CONFIG</strong></dt> <dt>805</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-585"><dt><strong>ERROR_INVALID_MSCHAPV2_CONFIG</strong></dt> <dt>805</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-586">Vous ne pouvez pas établir une connexion à l’aide de cette connexion au moment de la connexion, car elle est configurée pour utiliser les informations d’identification de l’utilisateur actuellement connecté.</span><span class="sxs-lookup"><span data-stu-id="346a3-586">You cannot dial using this connection at login time because it is configured to use the currently-logged-in user's credentials.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-587">Pris en charge dans Windows XP avec SP1 et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-587">Supported in Windows XP with SP1 and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_VPN_GRE_BLOCKED"></span><span id="error_vpn_gre_blocked"></span><dl> <span data-ttu-id="346a3-588"><dt><strong>ERROR_VPN_GRE_BLOCKED</strong></dt> <dt>806</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-588"><dt><strong>ERROR_VPN_GRE_BLOCKED</strong></dt> <dt>806</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-589">Une connexion entre votre ordinateur et le serveur VPN a été démarrée, mais la connexion VPN ne peut pas être effectuée.</span><span class="sxs-lookup"><span data-stu-id="346a3-589">A connection between your computer and the VPN server has been started, but the VPN connection cannot be completed.</span></span> <span data-ttu-id="346a3-590">La cause la plus courante est qu’au moins un périphérique Internet (par exemple, un pare-feu ou un routeur) entre votre ordinateur et le serveur VPN n’est pas configuré pour autoriser les paquets de protocole GRE (Generic Routing Encapsulation).</span><span class="sxs-lookup"><span data-stu-id="346a3-590">The most common cause for this is that at least one Internet device (for example, a firewall or a router) between your computer and the VPN server is not configured to allow Generic Routing Encapsulation (GRE) protocol packets.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-591">Pris en charge dans Windows Vista et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-591">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_VPN_DISCONNECT"></span><span id="error_vpn_disconnect"></span><dl> <span data-ttu-id="346a3-592"><dt><strong>ERROR_VPN_DISCONNECT</strong></dt> <dt>807</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-592"><dt><strong>ERROR_VPN_DISCONNECT</strong></dt> <dt>807</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-593">La connexion réseau entre votre ordinateur et le serveur VPN a été interrompue.</span><span class="sxs-lookup"><span data-stu-id="346a3-593">The network connection between your computer and the VPN server was interrupted.</span></span> <span data-ttu-id="346a3-594">Cela peut être dû à un problème dans la transmission VPN et est généralement le résultat de la latence Internet ou simplement que votre serveur VPN a atteint sa capacité maximale.</span><span class="sxs-lookup"><span data-stu-id="346a3-594">This can be caused by a problem in the VPN transmission and is commonly the result of internet latency or simply that your VPN server has reached capacity.</span></span> <span data-ttu-id="346a3-595">Essayez de vous reconnecter au serveur VPN.</span><span class="sxs-lookup"><span data-stu-id="346a3-595">Try to reconnect to the VPN server.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-596">Pris en charge dans Windows Vista et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-596">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_VPN_REFUSED"></span><span id="error_vpn_refused"></span><dl> <span data-ttu-id="346a3-597"><dt><strong>ERROR_VPN_REFUSED</strong></dt> <dt>808</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-597"><dt><strong>ERROR_VPN_REFUSED</strong></dt> <dt>808</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-598">La connexion réseau entre votre ordinateur et le serveur VPN n’a pas pu être établie car le serveur distant a refusé la connexion.</span><span class="sxs-lookup"><span data-stu-id="346a3-598">The network connection between your computer and the VPN server could not be established because the remote server refused the connection.</span></span> <span data-ttu-id="346a3-599">Cela est généralement dû à une incompatibilité entre la configuration du serveur et vos paramètres de connexion.</span><span class="sxs-lookup"><span data-stu-id="346a3-599">This is typically caused by a mismatch between the server's configuration and your connection settings.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-600">Pris en charge dans Windows Vista et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-600">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_VPN_TIMEOUT"></span><span id="error_vpn_timeout"></span><dl> <span data-ttu-id="346a3-601"><dt><strong>ERROR_VPN_TIMEOUT</strong></dt> <dt>809</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-601"><dt><strong>ERROR_VPN_TIMEOUT</strong></dt> <dt>809</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-602">La connexion réseau entre votre ordinateur et le serveur VPN n’a pas pu être établie car le serveur distant ne répond pas.</span><span class="sxs-lookup"><span data-stu-id="346a3-602">The network connection between your computer and the VPN server could not be established because the remote server is not responding.</span></span> <span data-ttu-id="346a3-603">Cela peut être dû au fait que l’un des périphériques réseau (par exemple, pare-feu, NAT, routeurs) entre votre ordinateur et le serveur distant n’est pas configuré pour autoriser les connexions VPN.</span><span class="sxs-lookup"><span data-stu-id="346a3-603">This could be because one of the network devices (for example, firewalls, NAT, routers) between your computer and the remote server is not configured to allow VPN connections.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-604">Pris en charge dans Windows Vista et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-604">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_VPN_BAD_CERT"></span><span id="error_vpn_bad_cert"></span><dl> <span data-ttu-id="346a3-605"><dt><strong>ERROR_VPN_BAD_CERT</strong></dt> <dt>810</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-605"><dt><strong>ERROR_VPN_BAD_CERT</strong></dt> <dt>810</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-606">Une connexion réseau entre votre ordinateur et le serveur VPN a été démarrée, mais la connexion VPN n’est pas terminée.</span><span class="sxs-lookup"><span data-stu-id="346a3-606">A network connection between your computer and the VPN server was started, but the VPN connection was not completed.</span></span> <span data-ttu-id="346a3-607">Cela est généralement dû à l’utilisation d’un certificat incorrect ou arrivé à expiration pour l’authentification entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="346a3-607">This is typically caused by the use of an incorrect or expired certificate for authentication between the client and the server.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-608">Pris en charge dans Windows Vista et les versions ultérieures de Windows</span><span class="sxs-lookup"><span data-stu-id="346a3-608">Supported in Windows Vista and later versions of Windows</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_VPN_BAD_PSK"></span><span id="error_vpn_bad_psk"></span><dl> <span data-ttu-id="346a3-609"><dt><strong>ERROR_VPN_BAD_PSK</strong></dt> <dt>811</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-609"><dt><strong>ERROR_VPN_BAD_PSK</strong></dt> <dt>811</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-610">La connexion réseau entre votre ordinateur et le serveur VPN n’a pas pu être établie car le serveur distant ne répond pas.</span><span class="sxs-lookup"><span data-stu-id="346a3-610">The network connection between your computer and the VPN server could not be established because the remote server is not responding.</span></span> <span data-ttu-id="346a3-611">Cela est généralement dû à un problème de clé pré-partagée entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="346a3-611">This is typically caused by a pre-shared key problem between the client and server.</span></span> <span data-ttu-id="346a3-612">Une clé prépartagée est utilisée pour vous assurer que vous êtes bien celui que vous déclarez dans un cycle de communication de sécurité IP (IPSec).</span><span class="sxs-lookup"><span data-stu-id="346a3-612">A pre-shared key is used to guarantee you are who you say you are in an IP Security (IPSec) communication cycle.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-613">Pris en charge dans Windows Vista et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-613">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_SERVER_POLICY"></span><span id="error_server_policy"></span><dl> <span data-ttu-id="346a3-614"><dt><strong>ERROR_SERVER_POLICY</strong></dt> <dt>812</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-614"><dt><strong>ERROR_SERVER_POLICY</strong></dt> <dt>812</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-615">la connexion a été empêchée en raison d’une stratégie configurée sur votre serveur RAS/VPN.</span><span class="sxs-lookup"><span data-stu-id="346a3-615">The connection was prevented because of a policy configured on your RAS/VPN server.</span></span> <span data-ttu-id="346a3-616">Plus précisément, la méthode d’authentification utilisée par le serveur pour vérifier votre nom d’utilisateur et votre mot de passe peut ne pas correspondre à la méthode d’authentification configurée dans votre profil de connexion.</span><span class="sxs-lookup"><span data-stu-id="346a3-616">Specifically, the authentication method used by the server to verify your username and password may not match the authentication method configured in your connection profile.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-617">Pris en charge dans Windows Vista et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-617">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_BROADBAND_ACTIVE"></span><span id="error_broadband_active"></span><dl> <span data-ttu-id="346a3-618"><dt><strong>ERROR_BROADBAND_ACTIVE</strong></dt> <dt>813</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-618"><dt><strong>ERROR_BROADBAND_ACTIVE</strong></dt> <dt>813</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-619">Vous avez tenté d’établir une deuxième connexion large bande alors qu’une connexion haut débit précédente est déjà établie à l’aide du même périphérique ou du même port.</span><span class="sxs-lookup"><span data-stu-id="346a3-619">You have attempted to establish a second broadband connection while a previous broadband connection is already established using the same device or port.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-620">Pris en charge dans Windows Vista et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-620">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_BROADBAND_NO_NIC"></span><span id="error_broadband_no_nic"></span><dl> <span data-ttu-id="346a3-621"><dt><strong>ERROR_BROADBAND_NO_NIC</strong></dt> <dt>814</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-621"><dt><strong>ERROR_BROADBAND_NO_NIC</strong></dt> <dt>814</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-622">La connectivité Ethernet sous-jacente requise pour la connexion large bande est introuvable.</span><span class="sxs-lookup"><span data-stu-id="346a3-622">The underlying Ethernet connectivity required for the broadband connection was not found.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-623">Pris en charge dans Windows Vista et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-623">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_BROADBAND_TIMEOUT"></span><span id="error_broadband_timeout"></span><dl> <span data-ttu-id="346a3-624"><dt><strong>ERROR_BROADBAND_TIMEOUT</strong></dt> <dt>815</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-624"><dt><strong>ERROR_BROADBAND_TIMEOUT</strong></dt> <dt>815</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-625">Impossible d’établir la connexion au réseau haut débit sur votre ordinateur, car le serveur distant ne répond pas.</span><span class="sxs-lookup"><span data-stu-id="346a3-625">The broadband network connection could not be established on your computer because the remote server is not responding.</span></span> <span data-ttu-id="346a3-626">Cela peut être dû à une valeur qui n’est pas valide pour le champ « nom du service » pour cette connexion.</span><span class="sxs-lookup"><span data-stu-id="346a3-626">This could be caused by a value that is not valid for the 'Service Name' field for this connection.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-627">Pris en charge dans Windows Vista et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-627">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_FEATURE_DEPRECATED"></span><span id="error_feature_deprecated"></span><dl> <span data-ttu-id="346a3-628"><dt><strong>ERROR_FEATURE_DEPRECATED</strong></dt> <dt>816</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-628"><dt><strong>ERROR_FEATURE_DEPRECATED</strong></dt> <dt>816</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-629">Une fonctionnalité ou un paramètre que vous avez essayé d’activer n’est plus pris en charge par le service d’accès à distance.</span><span class="sxs-lookup"><span data-stu-id="346a3-629">A feature or setting you have tried to enable is no longer supported by the remote access service.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-630">Pris en charge dans Windows Vista et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-630">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CANNOT_DELETE"></span><span id="error_cannot_delete"></span><dl> <span data-ttu-id="346a3-631"><dt><strong>ERROR_CANNOT_DELETE</strong></dt> <dt>817</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-631"><dt><strong>ERROR_CANNOT_DELETE</strong></dt> <dt>817</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-632">Impossible de supprimer une connexion pendant qu’elle est connectée.</span><span class="sxs-lookup"><span data-stu-id="346a3-632">Cannot delete a connection while it is connected.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-633">Pris en charge dans Windows Vista et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-633">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_RASQEC_RESOURCE_CREATION_FAILED"></span><span id="error_rasqec_resource_creation_failed"></span><dl> <span data-ttu-id="346a3-634"><dt><strong>ERROR_RASQEC_RESOURCE_CREATION_FAILED</strong></dt> <dt>818</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-634"><dt><strong>ERROR_RASQEC_RESOURCE_CREATION_FAILED</strong></dt> <dt>818</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-635">Le client de contrainte de mise en conformité NAP n’a pas pu créer de ressources système pour les connexions d’accès à distance.</span><span class="sxs-lookup"><span data-stu-id="346a3-635">The Network Access Protection (NAP) enforcement client could not create system resources for remote access connections.</span></span> <span data-ttu-id="346a3-636">Certains services ou ressources réseau peuvent ne pas être disponibles.</span><span class="sxs-lookup"><span data-stu-id="346a3-636">Some network services or resources might not be available.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-637">Pris en charge dans Windows Vista et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-637">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_RASQEC_NAPAGENT_NOT_ENABLED"></span><span id="error_rasqec_napagent_not_enabled"></span><dl> <span data-ttu-id="346a3-638"><dt><strong>ERROR_RASQEC_NAPAGENT_NOT_ENABLED</strong></dt> <dt>819</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-638"><dt><strong>ERROR_RASQEC_NAPAGENT_NOT_ENABLED</strong></dt> <dt>819</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-639">Le service agent de protection d’accès réseau (agent NAP) a été désactivé ou n’est pas installé sur cet ordinateur.</span><span class="sxs-lookup"><span data-stu-id="346a3-639">The Network Access Protection Agent (NAP Agent) service has been disabled or is not installed on this computer.</span></span> <span data-ttu-id="346a3-640">Certains services ou ressources réseau peuvent ne pas être disponibles.</span><span class="sxs-lookup"><span data-stu-id="346a3-640">Some network services or resources might not be available.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-641">Pris en charge dans Windows Vista et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-641">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_RASQEC_NAPAGENT_NOT_CONNECTED"></span><span id="error_rasqec_napagent_not_connected"></span><dl> <span data-ttu-id="346a3-642"><dt><strong>ERROR_RASQEC_NAPAGENT_NOT_CONNECTED</strong></dt> <dt>820</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-642"><dt><strong>ERROR_RASQEC_NAPAGENT_NOT_CONNECTED</strong></dt> <dt>820</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-643">Le client de contrainte de mise en conformité de la protection d’accès réseau (NAP) n’a pas pu s’inscrire auprès du service agent de protection d’accès réseau (agent NAP).</span><span class="sxs-lookup"><span data-stu-id="346a3-643">The Network Access Protection (NAP) enforcement client failed to register with the Network Access Protection Agent (NAP Agent) service.</span></span> <span data-ttu-id="346a3-644">Certains services ou ressources réseau peuvent ne pas être disponibles.</span><span class="sxs-lookup"><span data-stu-id="346a3-644">Some network services or resources might not be available.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-645">Pris en charge dans Windows Vista et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-645">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_RASQEC_CONN_DOESNOTEXIST"></span><span id="error_rasqec_conn_doesnotexist"></span><dl> <span data-ttu-id="346a3-646"><dt><strong>ERROR_RASQEC_CONN_DOESNOTEXIST</strong></dt> <dt>821</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-646"><dt><strong>ERROR_RASQEC_CONN_DOESNOTEXIST</strong></dt> <dt>821</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-647">Le client de contrainte de mise en conformité NAP n’a pas pu traiter la demande, car la connexion d’accès à distance n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="346a3-647">The Network Access Protection (NAP) enforcement client was unable to process the request because the remote access connection does not exist.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-648">Pris en charge dans Windows Vista et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-648">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_RASQEC_TIMEOUT"></span><span id="error_rasqec_timeout"></span><dl> <span data-ttu-id="346a3-649"><dt><strong>ERROR_RASQEC_TIMEOUT</strong></dt> <dt>822</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-649"><dt><strong>ERROR_RASQEC_TIMEOUT</strong></dt> <dt>822</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-650">Le client de contrainte de mise en conformité NAP n’a pas répondu.</span><span class="sxs-lookup"><span data-stu-id="346a3-650">The Network Access Protection (NAP) enforcement client did not respond.</span></span> <span data-ttu-id="346a3-651">Certains services ou ressources réseau peuvent ne pas être disponibles.</span><span class="sxs-lookup"><span data-stu-id="346a3-651">Some network services or resources might not be available.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-652">Pris en charge dans Windows Vista et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-652">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PEAP_CRYPTOBINDING_INVALID"></span><span id="error_peap_cryptobinding_invalid"></span><dl> <span data-ttu-id="346a3-653"><dt><strong>ERROR_PEAP_CRYPTOBINDING_INVALID</strong></dt> <dt>823</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-653"><dt><strong>ERROR_PEAP_CRYPTOBINDING_INVALID</strong></dt> <dt>823</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-654">Le Crypto-Binding type-length-value (TLV) reçu n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="346a3-654">The Crypto-Binding type-length-value (TLV) received is not valid.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-655">Pris en charge dans Windows Vista et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-655">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PEAP_CRYPTOBINDING_NOTRECEIVED"></span><span id="error_peap_cryptobinding_notreceived"></span><dl> <span data-ttu-id="346a3-656"><dt><strong>ERROR_PEAP_CRYPTOBINDING_NOTRECEIVED</strong></dt> <dt>824</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-656"><dt><strong>ERROR_PEAP_CRYPTOBINDING_NOTRECEIVED</strong></dt> <dt>824</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-657">Crypto-Binding TLV n’a pas été reçu.</span><span class="sxs-lookup"><span data-stu-id="346a3-657">Crypto-Binding TLV was not received.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-658">Pris en charge dans Windows Vista et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-658">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_VPNSTRATEGY"></span><span id="error_invalid_vpnstrategy"></span><dl> <span data-ttu-id="346a3-659"><dt><strong>ERROR_INVALID_VPNSTRATEGY</strong></dt> <dt>825</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-659"><dt><strong>ERROR_INVALID_VPNSTRATEGY</strong></dt> <dt>825</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-660">Le protocole PPTP (point-to-Point Tunneling Protocol) n’est pas compatible avec IPv6.</span><span class="sxs-lookup"><span data-stu-id="346a3-660">Point-to-Point Tunneling Protocol (PPTP) is incompatible with IPv6.</span></span> <span data-ttu-id="346a3-661">Modifiez le type de réseau privé virtuel en protocole L2TP (Layer Two Tunneling Protocol).</span><span class="sxs-lookup"><span data-stu-id="346a3-661">Change the type of virtual private network to Layer Two Tunneling Protocol (L2TP).</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-662">Pris en charge dans Windows Vista et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-662">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_EAPTLS_CACHE_CREDENTIALS_INVALID"></span><span id="error_eaptls_cache_credentials_invalid"></span><dl> <span data-ttu-id="346a3-663"><dt><strong>ERROR_EAPTLS_CACHE_CREDENTIALS_INVALID</strong></dt> <dt>826</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-663"><dt><strong>ERROR_EAPTLS_CACHE_CREDENTIALS_INVALID</strong></dt> <dt>826</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-664">Échec de la validation EAPTLS des informations d’identification mises en cache.</span><span class="sxs-lookup"><span data-stu-id="346a3-664">EAPTLS validation of the cached credentials failed.</span></span> <span data-ttu-id="346a3-665">Supprimer les informations d’identification mises en cache.</span><span class="sxs-lookup"><span data-stu-id="346a3-665">Discard cached credentials.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-666">Pris en charge dans Windows Vista et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-666">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_IPSEC_SERVICE_STOPPED"></span><span id="error_ipsec_service_stopped"></span><dl> <span data-ttu-id="346a3-667"><dt><strong>ERROR_IPSEC_SERVICE_STOPPED</strong></dt> <dt>827</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-667"><dt><strong>ERROR_IPSEC_SERVICE_STOPPED</strong></dt> <dt>827</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-668">La connexion L2TP/IPsec ne peut pas être effectuée car le service des modules de génération de clé IPSec IKE et AuthIP et/ou le service de moteur de filtrage de base ne sont pas en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="346a3-668">The L2TP/IPsec connection cannot be completed because the IKE and AuthIP IPSec Keying Modules service and/or the Base Filtering Engine service is not running.</span></span> <span data-ttu-id="346a3-669">Ces services sont requis pour établir une connexion L2TP/IPSec.</span><span class="sxs-lookup"><span data-stu-id="346a3-669">These services are required to establish an L2TP/IPSec connection.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-670">Pris en charge dans Windows Vista et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-670">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_IDLE_TIMEOUT"></span><span id="error_idle_timeout"></span><dl> <span data-ttu-id="346a3-671"><dt><strong>ERROR_IDLE_TIMEOUT</strong></dt> <dt>828</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-671"><dt><strong>ERROR_IDLE_TIMEOUT</strong></dt> <dt>828</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-672">La connexion a été arrêtée en raison d’un délai d’inactivité.</span><span class="sxs-lookup"><span data-stu-id="346a3-672">The connection was terminated because of idle timeout.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-673">Pris en charge dans Windows Vista et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-673">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_LINK_FAILURE"></span><span id="error_link_failure"></span><dl> <span data-ttu-id="346a3-674"><dt><strong>ERROR_LINK_FAILURE</strong></dt> <dt>829</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-674"><dt><strong>ERROR_LINK_FAILURE</strong></dt> <dt>829</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-675">Le modem (ou un autre périphérique de connexion) a été déconnecté en raison d’une erreur de liaison.</span><span class="sxs-lookup"><span data-stu-id="346a3-675">The modem (or other connecting device) was disconnected due to link failure.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-676">Pris en charge dans Windows Vista et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-676">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_USER_LOGOFF"></span><span id="error_user_logoff"></span><dl> <span data-ttu-id="346a3-677"><dt><strong>ERROR_USER_LOGOFF</strong></dt> <dt>830</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-677"><dt><strong>ERROR_USER_LOGOFF</strong></dt> <dt>830</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-678">La connexion a été interrompue, car l’utilisateur s’est déconnecté.</span><span class="sxs-lookup"><span data-stu-id="346a3-678">The connection was terminated because user logged off.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-679">Pris en charge dans Windows Vista et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-679">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_FAST_USER_SWITCH"></span><span id="error_fast_user_switch"></span><dl> <span data-ttu-id="346a3-680"><dt><strong>ERROR_FAST_USER_SWITCH</strong></dt> <dt>831</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-680"><dt><strong>ERROR_FAST_USER_SWITCH</strong></dt> <dt>831</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-681">La connexion a été interrompue car le changement d’utilisateur s’est produit.</span><span class="sxs-lookup"><span data-stu-id="346a3-681">The connection was terminated because user switch happened.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-682">Pris en charge dans Windows Vista et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-682">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_HIBERNATION"></span><span id="error_hibernation"></span><dl> <span data-ttu-id="346a3-683"><dt><strong>ERROR_HIBERNATION</strong></dt> <dt>832</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-683"><dt><strong>ERROR_HIBERNATION</strong></dt> <dt>832</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-684">La connexion a été interrompue en raison de la mise en veille prolongée.</span><span class="sxs-lookup"><span data-stu-id="346a3-684">The connection was terminated because of hibernation.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-685">Pris en charge dans Windows Vista et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-685">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SYSTEM_SUSPENDED"></span><span id="error_system_suspended"></span><dl> <span data-ttu-id="346a3-686"><dt><strong>ERROR_SYSTEM_SUSPENDED</strong></dt> <dt>833</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-686"><dt><strong>ERROR_SYSTEM_SUSPENDED</strong></dt> <dt>833</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-687">La connexion a été interrompue car le système a été suspendu.</span><span class="sxs-lookup"><span data-stu-id="346a3-687">The connection was terminated because the system got suspended.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-688">Pris en charge dans Windows Vista et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-688">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_RASMAN_SERVICE_STOPPED"></span><span id="error_rasman_service_stopped"></span><dl> <span data-ttu-id="346a3-689"><dt><strong>ERROR_RASMAN_SERVICE_STOPPED</strong></dt> <dt>834</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-689"><dt><strong>ERROR_RASMAN_SERVICE_STOPPED</strong></dt> <dt>834</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-690">La connexion a été interrompue car le gestionnaire de connexions d’accès à distance s’est arrêté.</span><span class="sxs-lookup"><span data-stu-id="346a3-690">The connection was terminated because Remote Access Connection manager stopped.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-691">Pris en charge dans Windows Vista et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-691">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_SERVER_CERT"></span><span id="error_invalid_server_cert"></span><dl> <span data-ttu-id="346a3-692"><dt><strong>ERROR_INVALID_SERVER_CERT</strong></dt> <dt>835</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-692"><dt><strong>ERROR_INVALID_SERVER_CERT</strong></dt> <dt>835</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-693">La tentative de connexion L2TP a échoué car la couche de sécurité n’a pas pu authentifier l’ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="346a3-693">The L2TP connection attempt failed because the security layer could not authenticate the remote computer.</span></span> <span data-ttu-id="346a3-694">Cela peut être dû au fait qu’un ou plusieurs champs du certificat présenté par le serveur distant n’ont pas pu être validés comme appartenant à la destination cible.</span><span class="sxs-lookup"><span data-stu-id="346a3-694">This could be because one or more fields of the certificate presented by the remote server could not be validated as belonging to the target destination.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-695">Pris en charge dans Windows Vista et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-695">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NOT_NAP_CAPABLE"></span><span id="error_not_nap_capable"></span><dl> <span data-ttu-id="346a3-696"><dt><strong>ERROR_NOT_NAP_CAPABLE</strong></dt> <dt>836</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-696"><dt><strong>ERROR_NOT_NAP_CAPABLE</strong></dt> <dt>836</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-697">La machine ne prend pas en charge la protection d’accès réseau.</span><span class="sxs-lookup"><span data-stu-id="346a3-697">The machine is not NAP capable.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-698">Pris en charge dans Windows Vista et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-698">Supported in Windows Vista and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_TUNNELID"></span><span id="error_invalid_tunnelid"></span><dl> <span data-ttu-id="346a3-699"><dt><strong>ERROR_INVALID_TUNNELID</strong></dt> <dt>837</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-699"><dt><strong>ERROR_INVALID_TUNNELID</strong></dt> <dt>837</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-700">ID de tunnel non valide.</span><span class="sxs-lookup"><span data-stu-id="346a3-700">Invalid Tunnel ID.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-701">Pris en charge dans Windows 7 et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-701">Supported in Windows 7 and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_UPDATECONNECTION_REQUEST_IN_PROCESS"></span><span id="error_updateconnection_request_in_process"></span><dl> <span data-ttu-id="346a3-702"><dt><strong>ERROR_UPDATECONNECTION_REQUEST_IN_PROCESS</strong></dt> <dt>838</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-702"><dt><strong>ERROR_UPDATECONNECTION_REQUEST_IN_PROCESS</strong></dt> <dt>838</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-703">Une autre demande de mise à jour de la connexion est en cours.</span><span class="sxs-lookup"><span data-stu-id="346a3-703">Another update connection request is in progress.</span></span> <span data-ttu-id="346a3-704">RAS n’autorise qu’une seule demande de mise à jour de la connexion à la fois.</span><span class="sxs-lookup"><span data-stu-id="346a3-704">RAS allows only one update connection request at a time.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-705">Pris en charge dans Windows 7 et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-705">Supported in Windows 7 and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PROTOCOL_ENGINE_DISABLED"></span><span id="error_protocol_engine_disabled"></span><dl> <span data-ttu-id="346a3-706"><dt><strong>ERROR_PROTOCOL_ENGINE_DISABLED</strong></dt> <dt>839</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-706"><dt><strong>ERROR_PROTOCOL_ENGINE_DISABLED</strong></dt> <dt>839</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-707">La négociation à l’aide du protocole configuré est désactivée.</span><span class="sxs-lookup"><span data-stu-id="346a3-707">Negotiating using configured protocol is disable.</span></span> <span data-ttu-id="346a3-708">Modifiez les propriétés de connexion et sélectionnez un protocole différent pour la négociation, puis réessayez.</span><span class="sxs-lookup"><span data-stu-id="346a3-708">Edit connection properties and select different protocol for negotiation and try again.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-709">Pris en charge dans Windows 7 et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-709">Supported in Windows 7 and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INTERNAL_ADDRESS_FAILURE"></span><span id="error_internal_address_failure"></span><dl> <span data-ttu-id="346a3-710"><dt><strong>ERROR_INTERNAL_ADDRESS_FAILURE</strong></dt> <dt>840</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-710"><dt><strong>ERROR_INTERNAL_ADDRESS_FAILURE</strong></dt> <dt>840</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-711">Échec de la négociation d’adresse interne.</span><span class="sxs-lookup"><span data-stu-id="346a3-711">Internal address negotiation failed.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-712">Pris en charge dans Windows 7 et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-712">Supported in Windows 7 and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_FAILED_CP_REQUIRED"></span><span id="error_failed_cp_required"></span><dl> <span data-ttu-id="346a3-713"><dt><strong>ERROR_FAILED_CP_REQUIRED</strong></dt> <dt>841</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-713"><dt><strong>ERROR_FAILED_CP_REQUIRED</strong></dt> <dt>841</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-714">Le client doit demander une adresse IPv4 ou IPv6 interne.</span><span class="sxs-lookup"><span data-stu-id="346a3-714">Client has to request an Internal IPv4 or IPv6 address.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-715">Pris en charge dans Windows 7 et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-715">Supported in Windows 7 and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_TS_UNACCEPTABLE"></span><span id="error_ts_unacceptable"></span><dl> <span data-ttu-id="346a3-716"><dt><strong>ERROR_TS_UNACCEPTABLE</strong></dt> <dt>842</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-716"><dt><strong>ERROR_TS_UNACCEPTABLE</strong></dt> <dt>842</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-717">Échec de la négociation des sélecteurs de trafic.</span><span class="sxs-lookup"><span data-stu-id="346a3-717">Traffic Selectors negotiation failed.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-718">Pris en charge dans Windows 7 et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-718">Supported in Windows 7 and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_MOBIKE_DISABLED"></span><span id="error_mobike_disabled"></span><dl> <span data-ttu-id="346a3-719"><dt><strong>ERROR_MOBIKE_DISABLED</strong></dt> <dt>843</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-719"><dt><strong>ERROR_MOBIKE_DISABLED</strong></dt> <dt>843</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-720">La mobilité est désactivée pour cette connexion.</span><span class="sxs-lookup"><span data-stu-id="346a3-720">Mobility is disabled for this connection.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-721">Pris en charge dans Windows 7 et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-721">Supported in Windows 7 and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_CANNOT_INITIATE_MOBIKE_UPDATE"></span><span id="error_cannot_initiate_mobike_update"></span><dl> <span data-ttu-id="346a3-722"><dt><strong>ERROR_CANNOT_INITIATE_MOBIKE_UPDATE</strong></dt> <dt>844</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-722"><dt><strong>ERROR_CANNOT_INITIATE_MOBIKE_UPDATE</strong></dt> <dt>844</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-723">La connexion VPN est toujours en cours de connexion ou de réauthentification en raison de la modification de l’état de mise en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="346a3-723">The VPN Connection is still connecting or re-authenticating because of Quarantine state change.</span></span> <span data-ttu-id="346a3-724">Lancer Mobile Update uniquement lorsque l’état de la connexion est « connecté ».</span><span class="sxs-lookup"><span data-stu-id="346a3-724">Initiate mobile update only when connection state is 'Connected'.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-725">Pris en charge dans Windows 7 et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-725">Supported in Windows 7 and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PEAP_SERVER_REJECTED_CLIENT_TLV"></span><span id="error_peap_server_rejected_client_tlv"></span><dl> <span data-ttu-id="346a3-726"><dt><strong>ERROR_PEAP_SERVER_REJECTED_CLIENT_TLV</strong></dt> <dt>845</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-726"><dt><strong>ERROR_PEAP_SERVER_REJECTED_CLIENT_TLV</strong></dt> <dt>845</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-727">L’authentification du client a été rejetée par le serveur en raison d’un TLV inattendu ou d’une non-concordance de valeur pour un TLV.</span><span class="sxs-lookup"><span data-stu-id="346a3-727">Server rejected client authentication, due to unexpected TLV or value mismatch for a TLV.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-728">Pris en charge dans Windows 7 et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-728">Supported in Windows 7 and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INVALID_PREFERENCES"></span><span id="error_invalid_preferences"></span><dl> <span data-ttu-id="346a3-729"><dt><strong>ERROR_INVALID_PREFERENCES</strong></dt> <dt>846</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-729"><dt><strong>ERROR_INVALID_PREFERENCES</strong></dt> <dt>846</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-730">Soit la préférence de destination VPN n’est pas sélectionnée par l’utilisateur, soit elle n’est plus valide.</span><span class="sxs-lookup"><span data-stu-id="346a3-730">Either VPN destination preference is not selected by the user or it is no longer valid.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-731">Pris en charge dans Windows 7 et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-731">Supported in Windows 7 and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EAPTLS_SCARD_CACHE_CREDENTIALS_INVALID"></span><span id="error_eaptls_scard_cache_credentials_invalid"></span><dl> <span data-ttu-id="346a3-732"><dt><strong>ERROR_EAPTLS_SCARD_CACHE_CREDENTIALS_INVALID</strong></dt> <dt>847</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-732"><dt><strong>ERROR_EAPTLS_SCARD_CACHE_CREDENTIALS_INVALID</strong></dt> <dt>847</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-733">Les informations d’identification de carte à puce mises en cache ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="346a3-733">Cached smart card credential is invalid.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-734">Pris en charge dans Windows 7 et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-734">Supported in Windows 7 and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_SSTP_COOKIE_SET_FAILURE"></span><span id="error_sstp_cookie_set_failure"></span><dl> <span data-ttu-id="346a3-735"><dt><strong>ERROR_SSTP_COOKIE_SET_FAILURE</strong></dt> <dt>848</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-735"><dt><strong>ERROR_SSTP_COOKIE_SET_FAILURE</strong></dt> <dt>848</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-736">Échec de la tentative de connexion VPN en raison d’une erreur interne lors de l’ajout de cookies au protocole SSTP (Secure Socket Tunneling Protocol).</span><span class="sxs-lookup"><span data-stu-id="346a3-736">VPN connection attempt failed due to internal error occurred while adding cookies to the Secure Socket Tunneling Protocol (SSTP).</span></span> <span data-ttu-id="346a3-737">Pour plus d’informations, consultez le journal des événements système.</span><span class="sxs-lookup"><span data-stu-id="346a3-737">Please see the System Event Log for the detailed information.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_PEAP_COOKIE_ATTRIBUTES"></span><span id="error_invalid_peap_cookie_attributes"></span><dl> <span data-ttu-id="346a3-738"><dt><strong>ERROR_INVALID_PEAP_COOKIE_ATTRIBUTES</strong></dt> <dt>849</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-738"><dt><strong>ERROR_INVALID_PEAP_COOKIE_ATTRIBUTES</strong></dt> <dt>849</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-739">Le ou les attributs de la méthode interne PEAP stockés dans le cookie sont/ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="346a3-739">The PEAP inner method attribute(s) stored in the cookie is/are invalid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_EAP_METHOD_NOT_INSTALLED"></span><span id="error_eap_method_not_installed"></span><dl> <span data-ttu-id="346a3-740"><dt><strong>ERROR_EAP_METHOD_NOT_INSTALLED</strong></dt> <dt>850</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-740"><dt><strong>ERROR_EAP_METHOD_NOT_INSTALLED</strong></dt> <dt>850</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-741">Le type de protocole d’authentification extensible requis pour l’authentification de la connexion d’accès à distance n’est pas installé sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="346a3-741">The Extensible Authentication Protocol type required for authentication of the remote access connection is not installed on your computer.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EAP_METHOD_DOES_NOT_SUPPORT_SSO"></span><span id="error_eap_method_does_not_support_sso"></span><dl> <span data-ttu-id="346a3-742"><dt><strong>ERROR_EAP_METHOD_DOES_NOT_SUPPORT_SSO</strong></dt> <dt>851</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-742"><dt><strong>ERROR_EAP_METHOD_DOES_NOT_SUPPORT_SSO</strong></dt> <dt>851</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-743">Le type de protocole EAP (Extensible Authentication Protocol) configuré sur la connexion d’accès à distance ne prend pas en charge l’authentification unique.</span><span class="sxs-lookup"><span data-stu-id="346a3-743">The Extensible Authentication Protocol type configured on the remote access connection does not support single sign-on.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_EAP_METHOD_OPERATION_NOT_SUPPORTED"></span><span id="error_eap_method_operation_not_supported"></span><dl> <span data-ttu-id="346a3-744"><dt><strong>ERROR_EAP_METHOD_OPERATION_NOT_SUPPORTED</strong></dt> <dt>852</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-744"><dt><strong>ERROR_EAP_METHOD_OPERATION_NOT_SUPPORTED</strong></dt> <dt>852</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-745">Le type de protocole EAP (Extensible Authentication Protocol) configuré sur la connexion d’accès à distance ne prend pas en charge l’opération demandée.</span><span class="sxs-lookup"><span data-stu-id="346a3-745">The Extensible Authentication Protocol type configured on the remote access connection does not support the requested operation.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EAP_USER_CERT_INVALID"></span><span id="error_eap_user_cert_invalid"></span><dl> <span data-ttu-id="346a3-746"><dt><strong>ERROR_EAP_USER_CERT_INVALID</strong></dt> <dt>853</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-746"><dt><strong>ERROR_EAP_USER_CERT_INVALID</strong></dt> <dt>853</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-747">La connexion d’accès à distance est terminée, mais l’authentification a échoué car le certificat qui authentifie le client sur le serveur n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="346a3-747">The remote access connection completed, but authentication failed because the certificate that authenticates the client to the server is not valid.</span></span> <span data-ttu-id="346a3-748">Assurez-vous que le certificat utilisé pour l’authentification est valide.</span><span class="sxs-lookup"><span data-stu-id="346a3-748">Ensure that the certificate used for authentication is valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_EAP_USER_CERT_EXPIRED"></span><span id="error_eap_user_cert_expired"></span><dl> <span data-ttu-id="346a3-749"><dt><strong>ERROR_EAP_USER_CERT_EXPIRED</strong></dt> <dt>854</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-749"><dt><strong>ERROR_EAP_USER_CERT_EXPIRED</strong></dt> <dt>854</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-750">La connexion d’accès à distance est terminée, mais l’authentification a échoué, car le certificat qui authentifie le client auprès du serveur a expiré.</span><span class="sxs-lookup"><span data-stu-id="346a3-750">The remote access connection completed, but authentication failed because the certificate that authenticates the client to the server is expired.</span></span> <span data-ttu-id="346a3-751">Renouvelez le certificat.</span><span class="sxs-lookup"><span data-stu-id="346a3-751">Renew the certificate.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EAP_USER_CERT_REVOKED"></span><span id="error_eap_user_cert_revoked"></span><dl> <span data-ttu-id="346a3-752"><dt><strong>ERROR_EAP_USER_CERT_REVOKED</strong></dt> <dt>855</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-752"><dt><strong>ERROR_EAP_USER_CERT_REVOKED</strong></dt> <dt>855</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-753">La connexion d’accès à distance est terminée, mais l’authentification a échoué car le certificat qui authentifie le client sur le serveur est révoqué.</span><span class="sxs-lookup"><span data-stu-id="346a3-753">The remote access connection completed, but authentication failed because the certificate that authenticates the client to the server is revoked.</span></span> <span data-ttu-id="346a3-754">Utilisez un certificat qui n’a pas été révoqué.</span><span class="sxs-lookup"><span data-stu-id="346a3-754">Use a certificate that has not been revoked.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_EAP_USER_CERT_OTHER_ERROR"></span><span id="error_eap_user_cert_other_error"></span><dl> <span data-ttu-id="346a3-755"><dt><strong>ERROR_EAP_USER_CERT_OTHER_ERROR</strong></dt> <dt>856</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-755"><dt><strong>ERROR_EAP_USER_CERT_OTHER_ERROR</strong></dt> <dt>856</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-756">La connexion d’accès à distance est terminée, mais l’authentification a échoué en raison d’une erreur dans le certificat qui authentifie le client auprès du serveur.</span><span class="sxs-lookup"><span data-stu-id="346a3-756">The remote access connection completed, but authentication failed because of an error in the certificate that authenticates the client to the server.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EAP_SERVER_CERT_INVALID"></span><span id="error_eap_server_cert_invalid"></span><dl> <span data-ttu-id="346a3-757"><dt><strong>ERROR_EAP_SERVER_CERT_INVALID</strong></dt> <dt>857</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-757"><dt><strong>ERROR_EAP_SERVER_CERT_INVALID</strong></dt> <dt>857</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-758">La connexion d’accès à distance est terminée, mais l’authentification a échoué, car le certificat utilisé par le client pour authentifier le serveur n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="346a3-758">The remote access connection completed, but authentication failed because the certificate that the client uses to authenticate the server is not valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_EAP_SERVER_CERT_EXPIRED"></span><span id="error_eap_server_cert_expired"></span><dl> <span data-ttu-id="346a3-759"><dt><strong>ERROR_EAP_SERVER_CERT_EXPIRED</strong></dt> <dt>858</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-759"><dt><strong>ERROR_EAP_SERVER_CERT_EXPIRED</strong></dt> <dt>858</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-760">La connexion d’accès à distance est terminée, mais l’authentification a échoué, car le certificat utilisé par le client pour authentifier le serveur a expiré.</span><span class="sxs-lookup"><span data-stu-id="346a3-760">The remote access connection completed, but authentication failed because the certificate that the client uses to authenticate the server is expired.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EAP_SERVER_CERT_REVOKED"></span><span id="error_eap_server_cert_revoked"></span><dl> <span data-ttu-id="346a3-761"><dt><strong>ERROR_EAP_SERVER_CERT_REVOKED</strong></dt> <dt>859</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-761"><dt><strong>ERROR_EAP_SERVER_CERT_REVOKED</strong></dt> <dt>859</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-762">La connexion d’accès à distance est terminée, mais l’authentification a échoué, car le certificat que le client utilise pour authentifier le serveur est révoqué.</span><span class="sxs-lookup"><span data-stu-id="346a3-762">The remote access connection completed, but authentication failed because the certificate that the client uses to authenticate the server is revoked.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_EAP_SERVER_CERT_OTHER_ERROR"></span><span id="error_eap_server_cert_other_error"></span><dl> <span data-ttu-id="346a3-763"><dt><strong>ERROR_EAP_SERVER_CERT_OTHER_ERROR</strong></dt> <dt>860</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-763"><dt><strong>ERROR_EAP_SERVER_CERT_OTHER_ERROR</strong></dt> <dt>860</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-764">La connexion d’accès à distance est terminée, mais l’authentification a échoué en raison d’une erreur dans le certificat que le client utilise pour authentifier le serveur.</span><span class="sxs-lookup"><span data-stu-id="346a3-764">The remote access connection completed, but authentication failed because of an error in the certificate that the client uses to authenticate the server.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EAP_USER_ROOT_CERT_NOT_FOUND"></span><span id="error_eap_user_root_cert_not_found"></span><dl> <span data-ttu-id="346a3-765"><dt><strong>ERROR_EAP_USER_ROOT_CERT_NOT_FOUND</strong></dt> <dt>861</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-765"><dt><strong>ERROR_EAP_USER_ROOT_CERT_NOT_FOUND</strong></dt> <dt>861</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-766">La connexion d’accès à distance est terminée, mais l’authentification a échoué, car un certificat racine approuvé qui valide le certificat de l’utilisateur est introuvable dans le magasin de certificats des autorités de certification racines de confiance.</span><span class="sxs-lookup"><span data-stu-id="346a3-766">The remote access connection completed, but authentication failed because a trusted root certificate that validates the user certificate was not found in the Trusted Root Certification Authorities certificate store.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_EAP_USER_ROOT_CERT_INVALID"></span><span id="error_eap_user_root_cert_invalid"></span><dl> <span data-ttu-id="346a3-767"><dt><strong>ERROR_EAP_USER_ROOT_CERT_INVALID</strong></dt> <dt>862</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-767"><dt><strong>ERROR_EAP_USER_ROOT_CERT_INVALID</strong></dt> <dt>862</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-768">La connexion d’accès à distance est terminée, mais l’authentification a échoué, car le certificat racine approuvé utilisé pour valider le certificat utilisateur n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="346a3-768">The remote access connection completed, but authentication failed because the trusted root certificate that is used to validate the user certificate is not valid.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EAP_USER_ROOT_CERT_EXPIRED"></span><span id="error_eap_user_root_cert_expired"></span><dl> <span data-ttu-id="346a3-769"><dt><strong>ERROR_EAP_USER_ROOT_CERT_EXPIRED</strong></dt> <dt>863</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-769"><dt><strong>ERROR_EAP_USER_ROOT_CERT_EXPIRED</strong></dt> <dt>863</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-770">La connexion d’accès à distance est terminée, mais l’authentification a échoué, car le certificat dans le magasin de certificats des autorités de certification racines de confiance qui authentifie le certificat utilisateur a expiré.</span><span class="sxs-lookup"><span data-stu-id="346a3-770">The remote access connection completed, but authentication failed because the certificate in the Trusted Root Certification Authorities certificate store that authenticates the user certificate is expired.</span></span> <span data-ttu-id="346a3-771">Renouvelez le certificat.</span><span class="sxs-lookup"><span data-stu-id="346a3-771">Renew the certificate.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_EAP_SERVER_ROOT_CERT_NOT_FOUND"></span><span id="error_eap_server_root_cert_not_found"></span><dl> <span data-ttu-id="346a3-772"><dt><strong>ERROR_EAP_SERVER_ROOT_CERT_NOT_FOUND</strong></dt> <dt>864</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-772"><dt><strong>ERROR_EAP_SERVER_ROOT_CERT_NOT_FOUND</strong></dt> <dt>864</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-773">La connexion d’accès à distance est terminée, mais l’authentification a échoué, car un certificat qui valide le certificat de serveur est introuvable dans le magasin de certificats des autorités de certification racines de confiance.</span><span class="sxs-lookup"><span data-stu-id="346a3-773">The remote access connection completed, but authentication failed because a certificate that validates the server certificate was not found in the Trusted Root Certification Authorities certificate store.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EAP_SERVER_ROOT_CERT_INVALID"></span><span id="error_eap_server_root_cert_invalid"></span><dl> <span data-ttu-id="346a3-774"><dt><strong>ERROR_EAP_SERVER_ROOT_CERT_INVALID</strong></dt> <dt>865</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-774"><dt><strong>ERROR_EAP_SERVER_ROOT_CERT_INVALID</strong></dt> <dt>865</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-775">La connexion d’accès à distance est terminée, mais l’authentification a échoué car le certificat dans le magasin de certificats des autorités de certification racines de confiance qui valide le certificat de serveur n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="346a3-775">The remote access connection completed, but authentication failed because the certificate in the Trusted Root Certification Authorities certificate store that validates the server certificate is not valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_EAP_SERVER_ROOT_CERT_NAME_REQUIRED"></span><span id="error_eap_server_root_cert_name_required"></span><dl> <span data-ttu-id="346a3-776"><dt><strong>ERROR_EAP_SERVER_ROOT_CERT_NAME_REQUIRED</strong></dt> <dt>866</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-776"><dt><strong>ERROR_EAP_SERVER_ROOT_CERT_NAME_REQUIRED</strong></dt> <dt>866</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-777">La connexion d’accès à distance est terminée, mais l’authentification a échoué, car aucun nom de serveur n’a été spécifié pour le certificat sur l’ordinateur serveur.</span><span class="sxs-lookup"><span data-stu-id="346a3-777">The remote access connection completed, but authentication failed because the certificate on the server computer does not have a server name specified.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PEAP_IDENTITY_MISMATCH"></span><span id="error_peap_identity_mismatch"></span><dl> <span data-ttu-id="346a3-778"><dt><strong>ERROR_PEAP_IDENTITY_MISMATCH</strong></dt> <dt>867</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-778"><dt><strong>ERROR_PEAP_IDENTITY_MISMATCH</strong></dt> <dt>867</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-779">L’identité externe PEAP n’est pas identique à l’identité interne lorsque la confidentialité de l’identité est désactivée.</span><span class="sxs-lookup"><span data-stu-id="346a3-779">The PEAP outer identity is not same as the inner identity when identity privacy is turned OFF.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DNSNAME_NOT_RESOLVABLE"></span><span id="error_dnsname_not_resolvable"></span><dl> <span data-ttu-id="346a3-780"><dt><strong>ERROR_DNSNAME_NOT_RESOLVABLE</strong></dt> <dt>868</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-780"><dt><strong>ERROR_DNSNAME_NOT_RESOLVABLE</strong></dt> <dt>868</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-781">La connexion à distance n’a pas été établie, car le nom du serveur d’accès à distance n’a pas été résolu.</span><span class="sxs-lookup"><span data-stu-id="346a3-781">The remote connection was not made because the name of the remote access server did not resolve.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EAPTLS_PASSWD_INVALID"></span><span id="error_eaptls_passwd_invalid"></span><dl> <span data-ttu-id="346a3-782"><dt><strong>ERROR_EAPTLS_PASSWD_INVALID</strong></dt> <dt>869</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-782"><dt><strong>ERROR_EAPTLS_PASSWD_INVALID</strong></dt> <dt>869</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-783">Le mot de passe fourni pour le certificat n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="346a3-783">The password provided for the certificate is not valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_IKEV2_PSK_INTERFACE_ALREADY_EXISTS"></span><span id="error_ikev2_psk_interface_already_exists"></span><dl> <span data-ttu-id="346a3-784"><dt><strong>ERROR_IKEV2_PSK_INTERFACE_ALREADY_EXISTS</strong></dt> <dt>870</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-784"><dt><strong>ERROR_IKEV2_PSK_INTERFACE_ALREADY_EXISTS</strong></dt> <dt>870</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-785">L’interface n’a pas pu être activée, car plusieurs interfaces ayant la même destination ont été créées avec la méthode d’authentification par clé prépartagée.</span><span class="sxs-lookup"><span data-stu-id="346a3-785">The interface could not be enabled because more than one interface with the same destination has been created with the pre-shared key authentication method.</span></span> <span data-ttu-id="346a3-786">Modifiez la méthode d’authentification/destination et activez l’interface.</span><span class="sxs-lookup"><span data-stu-id="346a3-786">Change the destination/auth method and enable the interface.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="346a3-787">Les codes d’erreur de l’API de routage et d’accès à distance (RRAS) suivants sont définis dans mprerror. h.</span><span class="sxs-lookup"><span data-stu-id="346a3-787">The following Routing and Remote Access (RRAS) API error codes are defined in mprerror.h.</span></span> <span data-ttu-id="346a3-788">Tous les codes d’erreur sont pris en charge dans Windows 2000 ou les versions ultérieures de Windows, sauf indication contraire.</span><span class="sxs-lookup"><span data-stu-id="346a3-788">All error codes are supported in Windows 2000 or later versions of Windows unless specified otherwise.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="346a3-789">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="346a3-789">Return code/value</span></span></th>
<th><span data-ttu-id="346a3-790">Description</span><span class="sxs-lookup"><span data-stu-id="346a3-790">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="ERROR_ROUTER_STOPPED"></span><span id="error_router_stopped"></span><dl> <span data-ttu-id="346a3-791"><dt><strong>ERROR_ROUTER_STOPPED</strong></dt> <dt>900</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-791"><dt><strong>ERROR_ROUTER_STOPPED</strong></dt> <dt>900</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-792">Le routeur n’est pas en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="346a3-792">The router is not running.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_ALREADY_CONNECTED"></span><span id="error_already_connected"></span><dl> <span data-ttu-id="346a3-793"><dt><strong>ERROR_ALREADY_CONNECTED</strong></dt> <dt>901</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-793"><dt><strong>ERROR_ALREADY_CONNECTED</strong></dt> <dt>901</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-794">L’interface est déjà connectée.</span><span class="sxs-lookup"><span data-stu-id="346a3-794">The interface is already connected.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_UNKNOWN_PROTOCOL_ID"></span><span id="error_unknown_protocol_id"></span><dl> <span data-ttu-id="346a3-795"><dt><strong>ERROR_UNKNOWN_PROTOCOL_ID</strong></dt> <dt>902</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-795"><dt><strong>ERROR_UNKNOWN_PROTOCOL_ID</strong></dt> <dt>902</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-796">L’identificateur de protocole spécifié n’est pas connu du routeur.</span><span class="sxs-lookup"><span data-stu-id="346a3-796">The specified protocol identifier is not known to the router.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_DDM_NOT_RUNNING"></span><span id="error_ddm_not_running"></span><dl> <span data-ttu-id="346a3-797"><dt><strong>ERROR_DDM_NOT_RUNNING</strong></dt> <dt>903</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-797"><dt><strong>ERROR_DDM_NOT_RUNNING</strong></dt> <dt>903</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-798">Le gestionnaire de l’interface de connexion à la demande (DDM) n’est pas en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="346a3-798">The Demand-dial Interface Manager (DDM) is not running.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INTERFACE_ALREADY_EXISTS"></span><span id="error_interface_already_exists"></span><dl> <span data-ttu-id="346a3-799"><dt><strong>ERROR_INTERFACE_ALREADY_EXISTS</strong></dt> <dt>904</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-799"><dt><strong>ERROR_INTERFACE_ALREADY_EXISTS</strong></dt> <dt>904</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-800">Une interface portant ce nom est déjà inscrite auprès du routeur.</span><span class="sxs-lookup"><span data-stu-id="346a3-800">An interface with this name is already registered with the router.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NO_SUCH_INTERFACE"></span><span id="error_no_such_interface"></span><dl> <span data-ttu-id="346a3-801"><dt><strong>ERROR_NO_SUCH_INTERFACE</strong></dt> <dt>905</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-801"><dt><strong>ERROR_NO_SUCH_INTERFACE</strong></dt> <dt>905</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-802">Une interface portant ce nom n’est pas inscrite auprès du routeur.</span><span class="sxs-lookup"><span data-stu-id="346a3-802">An interface with this name is not registered with the router.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INTERFACE_NOT_CONNECTED"></span><span id="error_interface_not_connected"></span><dl> <span data-ttu-id="346a3-803"><dt><strong>ERROR_INTERFACE_NOT_CONNECTED</strong></dt> <dt>906</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-803"><dt><strong>ERROR_INTERFACE_NOT_CONNECTED</strong></dt> <dt>906</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-804">L’interface n’est pas connectée.</span><span class="sxs-lookup"><span data-stu-id="346a3-804">The interface is not connected.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PROTOCOL_STOP_PENDING"></span><span id="error_protocol_stop_pending"></span><dl> <span data-ttu-id="346a3-805"><dt><strong>ERROR_PROTOCOL_STOP_PENDING</strong></dt> <dt>907</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-805"><dt><strong>ERROR_PROTOCOL_STOP_PENDING</strong></dt> <dt>907</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-806">Le protocole spécifié est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="346a3-806">The specified protocol is stopping.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INTERFACE_CONNECTED"></span><span id="error_interface_connected"></span><dl> <span data-ttu-id="346a3-807"><dt><strong>ERROR_INTERFACE_CONNECTED</strong></dt> <dt>908</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-807"><dt><strong>ERROR_INTERFACE_CONNECTED</strong></dt> <dt>908</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-808">L’interface est connectée et ne peut donc pas être supprimée.</span><span class="sxs-lookup"><span data-stu-id="346a3-808">The interface is connected and hence cannot be deleted.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NO_INTERFACE_CREDENTIALS_SET"></span><span id="error_no_interface_credentials_set"></span><dl> <span data-ttu-id="346a3-809"><dt><strong>ERROR_NO_INTERFACE_CREDENTIALS_SET</strong></dt> <dt>909</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-809"><dt><strong>ERROR_NO_INTERFACE_CREDENTIALS_SET</strong></dt> <dt>909</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-810">Les informations d’identification de l’interface n’ont pas été définies.</span><span class="sxs-lookup"><span data-stu-id="346a3-810">The interface credentials have not been set.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_ALREADY_CONNECTING"></span><span id="error_already_connecting"></span><dl> <span data-ttu-id="346a3-811"><dt><strong>ERROR_ALREADY_CONNECTING</strong></dt> <dt>910</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-811"><dt><strong>ERROR_ALREADY_CONNECTING</strong></dt> <dt>910</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-812">Cette interface est déjà en cours de connexion.</span><span class="sxs-lookup"><span data-stu-id="346a3-812">This interface is already in the process of connecting.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_UPDATE_IN_PROGRESS"></span><span id="error_update_in_progress"></span><dl> <span data-ttu-id="346a3-813"><dt><strong>ERROR_UPDATE_IN_PROGRESS</strong></dt> <dt>911</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-813"><dt><strong>ERROR_UPDATE_IN_PROGRESS</strong></dt> <dt>911</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-814">Une mise à jour des informations de routage sur cette interface est déjà en cours.</span><span class="sxs-lookup"><span data-stu-id="346a3-814">An update of routing information on this interface is already in progress.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INTERFACE_CONFIGURATION"></span><span id="error_interface_configuration"></span><dl> <span data-ttu-id="346a3-815"><dt><strong>ERROR_INTERFACE_CONFIGURATION</strong></dt> <dt>912</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-815"><dt><strong>ERROR_INTERFACE_CONFIGURATION</strong></dt> <dt>912</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-816">La validation de l’interface n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="346a3-816">The interface configration is not valid.</span></span> <span data-ttu-id="346a3-817">Une autre interface est déjà connectée à la même interface sur le routeur distant.</span><span class="sxs-lookup"><span data-stu-id="346a3-817">There is already another interface that is connected to the same interface on the remote router.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NOT_CLIENT_PORT"></span><span id="error_not_client_port"></span><dl> <span data-ttu-id="346a3-818"><dt><strong>ERROR_NOT_CLIENT_PORT</strong></dt> <dt>913</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-818"><dt><strong>ERROR_NOT_CLIENT_PORT</strong></dt> <dt>913</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-819">Un client d’accès à distance a tenté de se connecter sur un port réservé aux routeurs.</span><span class="sxs-lookup"><span data-stu-id="346a3-819">A Remote Access Client attempted to connect over a port that was reserved for routers only.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NOT_ROUTER_PORT"></span><span id="error_not_router_port"></span><dl> <span data-ttu-id="346a3-820"><dt><strong>ERROR_NOT_ROUTER_PORT</strong></dt> <dt>914</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-820"><dt><strong>ERROR_NOT_ROUTER_PORT</strong></dt> <dt>914</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-821">Un routeur de connexion à la demande a tenté de se connecter sur un port réservé aux clients d’accès à distance uniquement.</span><span class="sxs-lookup"><span data-stu-id="346a3-821">A Demand Dial Router attempted to connect over a port that was reserved for Remote Access Clients only.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CLIENT_INTERFACE_ALREADY_EXISTS"></span><span id="error_client_interface_already_exists"></span><dl> <span data-ttu-id="346a3-822"><dt><strong>ERROR_CLIENT_INTERFACE_ALREADY_EXISTS</strong></dt> <dt>915</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-822"><dt><strong>ERROR_CLIENT_INTERFACE_ALREADY_EXISTS</strong></dt> <dt>915</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-823">L’interface cliente portant ce nom existe déjà et est actuellement connectée.</span><span class="sxs-lookup"><span data-stu-id="346a3-823">The client interface with this name already exists and is currently connected.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INTERFACE_DISABLED"></span><span id="error_interface_disabled"></span><dl> <span data-ttu-id="346a3-824"><dt><strong>ERROR_INTERFACE_DISABLED</strong></dt> <dt>916</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-824"><dt><strong>ERROR_INTERFACE_DISABLED</strong></dt> <dt>916</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-825">L’interface est dans un état désactivé.</span><span class="sxs-lookup"><span data-stu-id="346a3-825">The interface is in a disabled state.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_AUTH_PROTOCOL_REJECTED"></span><span id="error_auth_protocol_rejected"></span><dl> <span data-ttu-id="346a3-826"><dt><strong>ERROR_AUTH_PROTOCOL_REJECTED</strong></dt> <dt>917</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-826"><dt><strong>ERROR_AUTH_PROTOCOL_REJECTED</strong></dt> <dt>917</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-827">Le protocole d’authentification a été rejeté par l’homologue distant.</span><span class="sxs-lookup"><span data-stu-id="346a3-827">The authentication protocol was rejected by the remote peer.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_AUTH_PROTOCOL_AVAILABLE"></span><span id="error_no_auth_protocol_available"></span><dl> <span data-ttu-id="346a3-828"><dt><strong>ERROR_NO_AUTH_PROTOCOL_AVAILABLE</strong></dt> <dt>918</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-828"><dt><strong>ERROR_NO_AUTH_PROTOCOL_AVAILABLE</strong></dt> <dt>918</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-829">Aucun protocole d’authentification n’est disponible pour l’utilisation.</span><span class="sxs-lookup"><span data-stu-id="346a3-829">There are no authentication protocols available for use.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PEER_REFUSED_AUTH"></span><span id="error_peer_refused_auth"></span><dl> <span data-ttu-id="346a3-830"><dt><strong>ERROR_PEER_REFUSED_AUTH</strong></dt> <dt>919</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-830"><dt><strong>ERROR_PEER_REFUSED_AUTH</strong></dt> <dt>919</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-831">Impossible d’établir la connexion, car le protocole d’authentification utilisé par le serveur RAS/VPN pour vérifier votre nom d’utilisateur et votre mot de passe n’a pas pu être mis en correspondance avec les paramètres de votre profil de connexion.</span><span class="sxs-lookup"><span data-stu-id="346a3-831">The connection could not be established because the authentication protocol used by the RAS/VPN server to verify your username and password could not be matched with the settings in your connection profile.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_REMOTE_NO_DIALIN_PERMISSION"></span><span id="error_remote_no_dialin_permission"></span><dl> <span data-ttu-id="346a3-832"><dt><strong>ERROR_REMOTE_NO_DIALIN_PERMISSION</strong></dt> <dt>920</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-832"><dt><strong>ERROR_REMOTE_NO_DIALIN_PERMISSION</strong></dt> <dt>920</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-833">Le compte distant ne dispose pas de l’autorisation d’accès à distance.</span><span class="sxs-lookup"><span data-stu-id="346a3-833">The remote account does not have Remote Access permission.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_REMOTE_PASSWD_EXPIRED"></span><span id="error_remote_passwd_expired"></span><dl> <span data-ttu-id="346a3-834"><dt><strong>ERROR_REMOTE_PASSWD_EXPIRED</strong></dt> <dt>921</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-834"><dt><strong>ERROR_REMOTE_PASSWD_EXPIRED</strong></dt> <dt>921</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-835">Le compte distant a expiré.</span><span class="sxs-lookup"><span data-stu-id="346a3-835">The remote account has expired.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_REMOTE_ACCT_DISABLED"></span><span id="error_remote_acct_disabled"></span><dl> <span data-ttu-id="346a3-836"><dt><strong>ERROR_REMOTE_ACCT_DISABLED</strong></dt> <dt>922</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-836"><dt><strong>ERROR_REMOTE_ACCT_DISABLED</strong></dt> <dt>922</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-837">Le compte distant est désactivé.</span><span class="sxs-lookup"><span data-stu-id="346a3-837">The remote account is disabled.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_REMOTE_RESTRICTED_LOGON_HOURS"></span><span id="error_remote_restricted_logon_hours"></span><dl> <span data-ttu-id="346a3-838"><dt><strong>ERROR_REMOTE_RESTRICTED_LOGON_HOURS</strong></dt> <dt>923</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-838"><dt><strong>ERROR_REMOTE_RESTRICTED_LOGON_HOURS</strong></dt> <dt>923</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-839">Le compte distant n’est pas autorisé à se connecter à cette heure de la journée.</span><span class="sxs-lookup"><span data-stu-id="346a3-839">The remote account is not permitted to logon at this time of day.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_REMOTE_AUTHENTICATION_FAILURE"></span><span id="error_remote_authentication_failure"></span><dl> <span data-ttu-id="346a3-840"><dt><strong>ERROR_REMOTE_AUTHENTICATION_FAILURE</strong></dt> <dt>924</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-840"><dt><strong>ERROR_REMOTE_AUTHENTICATION_FAILURE</strong></dt> <dt>924</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-841">L’accès a été refusé à l’homologue distant, car le nom d’utilisateur, le mot de passe ou les deux ne sont pas valides sur le domaine.</span><span class="sxs-lookup"><span data-stu-id="346a3-841">Access was denied to the remote peer because the user name, password, or both is not valid on the domain.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INTERFACE_HAS_NO_DEVICES"></span><span id="error_interface_has_no_devices"></span><dl> <span data-ttu-id="346a3-842"><dt><strong>ERROR_INTERFACE_HAS_NO_DEVICES</strong></dt> <dt>925</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-842"><dt><strong>ERROR_INTERFACE_HAS_NO_DEVICES</strong></dt> <dt>925</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-843">Aucun port activé pour le routage n’est disponible pour une utilisation par cette interface de connexion à la demande.</span><span class="sxs-lookup"><span data-stu-id="346a3-843">There are no routing enabled ports available for use by this demand dial interface.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_IDLE_DISCONNECTED"></span><span id="error_idle_disconnected"></span><dl> <span data-ttu-id="346a3-844"><dt><strong>ERROR_IDLE_DISCONNECTED</strong></dt> <dt>926</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-844"><dt><strong>ERROR_IDLE_DISCONNECTED</strong></dt> <dt>926</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-845">Le port a été déconnecté en raison d’une inactivité.</span><span class="sxs-lookup"><span data-stu-id="346a3-845">The port has been disconnected due to inactivity.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INTERFACE_UNREACHABLE"></span><span id="error_interface_unreachable"></span><dl> <span data-ttu-id="346a3-846"><dt><strong>ERROR_INTERFACE_UNREACHABLE</strong></dt> <dt>927</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-846"><dt><strong>ERROR_INTERFACE_UNREACHABLE</strong></dt> <dt>927</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-847">L’interface n’est pas accessible pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="346a3-847">The interface is not reachable at this time.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_SERVICE_IS_PAUSED"></span><span id="error_service_is_paused"></span><dl> <span data-ttu-id="346a3-848"><dt><strong>ERROR_SERVICE_IS_PAUSED</strong></dt> <dt>928</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-848"><dt><strong>ERROR_SERVICE_IS_PAUSED</strong></dt> <dt>928</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-849">Le service de numérotation à la demande est dans un état suspendu.</span><span class="sxs-lookup"><span data-stu-id="346a3-849">The Demand Dial service is in a paused state.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INTERFACE_DISCONNECTED"></span><span id="error_interface_disconnected"></span><dl> <span data-ttu-id="346a3-850"><dt><strong>ERROR_INTERFACE_DISCONNECTED</strong></dt> <dt>929</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-850"><dt><strong>ERROR_INTERFACE_DISCONNECTED</strong></dt> <dt>929</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-851">L’interface a été déconnectée par l’administrateur.</span><span class="sxs-lookup"><span data-stu-id="346a3-851">The interface has been disconnected by the administrator.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_AUTH_SERVER_TIMEOUT"></span><span id="error_auth_server_timeout"></span><dl> <span data-ttu-id="346a3-852"><dt><strong>ERROR_AUTH_SERVER_TIMEOUT</strong></dt> <dt>930</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-852"><dt><strong>ERROR_AUTH_SERVER_TIMEOUT</strong></dt> <dt>930</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-853">Le serveur d’authentification n’a pas répondu aux demandes d’authentification en temps opportun.</span><span class="sxs-lookup"><span data-stu-id="346a3-853">The authentication server did not respond to authentication requests in a timely fashion.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PORT_LIMIT_REACHED"></span><span id="error_port_limit_reached"></span><dl> <span data-ttu-id="346a3-854"><dt><strong>ERROR_PORT_LIMIT_REACHED</strong></dt> <dt>931</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-854"><dt><strong>ERROR_PORT_LIMIT_REACHED</strong></dt> <dt>931</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-855">Le nombre maximal de ports autorisés pour une utilisation dans la connexion à plusieurs liaisons a été atteint.</span><span class="sxs-lookup"><span data-stu-id="346a3-855">The maximum number of ports allowed for use in the multi-linked connection has been reached.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PPP_SESSION_TIMEOUT"></span><span id="error_ppp_session_timeout"></span><dl> <span data-ttu-id="346a3-856"><dt><strong>ERROR_PPP_SESSION_TIMEOUT</strong></dt> <dt>932</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-856"><dt><strong>ERROR_PPP_SESSION_TIMEOUT</strong></dt> <dt>932</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-857">Le délai de connexion de l’utilisateur a été atteint.</span><span class="sxs-lookup"><span data-stu-id="346a3-857">The connection time limit for the user has been reached.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_MAX_LAN_INTERFACE_LIMIT"></span><span id="error_max_lan_interface_limit"></span><dl> <span data-ttu-id="346a3-858"><dt><strong>ERROR_MAX_LAN_INTERFACE_LIMIT</strong></dt> <dt>933</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-858"><dt><strong>ERROR_MAX_LAN_INTERFACE_LIMIT</strong></dt> <dt>933</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-859">La limite maximale du nombre d’interfaces LAN prises en charge a été atteinte.</span><span class="sxs-lookup"><span data-stu-id="346a3-859">The maximum limit on the number of LAN interfaces supported has been reached.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_MAX_WAN_INTERFACE_LIMIT"></span><span id="error_max_wan_interface_limit"></span><dl> <span data-ttu-id="346a3-860"><dt><strong>ERROR_MAX_WAN_INTERFACE_LIMIT</strong></dt> <dt>934</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-860"><dt><strong>ERROR_MAX_WAN_INTERFACE_LIMIT</strong></dt> <dt>934</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-861">La limite maximale du nombre d’interfaces de connexion à la demande prises en charge a été atteinte.</span><span class="sxs-lookup"><span data-stu-id="346a3-861">The maximum limit on the number of Demand Dial interfaces supported has been reached.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_MAX_CLIENT_INTERFACE_LIMIT"></span><span id="error_max_client_interface_limit"></span><dl> <span data-ttu-id="346a3-862"><dt><strong>ERROR_MAX_CLIENT_INTERFACE_LIMIT</strong></dt> <dt>935</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-862"><dt><strong>ERROR_MAX_CLIENT_INTERFACE_LIMIT</strong></dt> <dt>935</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-863">La limite maximale du nombre de clients d’accès à distance pris en charge a été atteinte.</span><span class="sxs-lookup"><span data-stu-id="346a3-863">The maximum limit on the number of Remote Access Clients supported has been reached.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_BAP_DISCONNECTED"></span><span id="error_bap_disconnected"></span><dl> <span data-ttu-id="346a3-864"><dt><strong>ERROR_BAP_DISCONNECTED</strong></dt> <dt>936</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-864"><dt><strong>ERROR_BAP_DISCONNECTED</strong></dt> <dt>936</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-865">Le port a été déconnecté en raison de la stratégie du protocole BAP (Bandwidth Allocation Protocol).</span><span class="sxs-lookup"><span data-stu-id="346a3-865">The port has been disconnected due to the Bandwidth Allocation Protocol (BAP) policy.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_USER_LIMIT"></span><span id="error_user_limit"></span><dl> <span data-ttu-id="346a3-866"><dt><strong>ERROR_USER_LIMIT</strong></dt> <dt>937</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-866"><dt><strong>ERROR_USER_LIMIT</strong></dt> <dt>937</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-867">Une autre connexion de votre type étant en cours d’utilisation, la connexion entrante ne peut pas accepter votre demande de connexion.</span><span class="sxs-lookup"><span data-stu-id="346a3-867">Because another connection of your type is in use, the incoming connection cannot accept your connection request.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_RADIUS_SERVERS"></span><span id="error_no_radius_servers"></span><dl> <span data-ttu-id="346a3-868"><dt><strong>ERROR_NO_RADIUS_SERVERS</strong></dt> <dt>938</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-868"><dt><strong>ERROR_NO_RADIUS_SERVERS</strong></dt> <dt>938</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-869">Aucun serveur RADIUS n’a été trouvé sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="346a3-869">No RADIUS servers were located on the network.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_RADIUS_RESPONSE"></span><span id="error_invalid_radius_response"></span><dl> <span data-ttu-id="346a3-870"><dt><strong>ERROR_INVALID_RADIUS_RESPONSE</strong></dt> <dt>939</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-870"><dt><strong>ERROR_INVALID_RADIUS_RESPONSE</strong></dt> <dt>939</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-871">La réponse reçue du serveur d’authentification RADIUS n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="346a3-871">The response received from the RADIUS authentication server was not valid.</span></span> <span data-ttu-id="346a3-872">Assurez-vous que le mot de passe secret sensible à la casse pour le serveur RADIUS est correctement défini.</span><span class="sxs-lookup"><span data-stu-id="346a3-872">Make sure that the case sensitive secret password for the RADIUS server is set correctly.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DIALIN_HOURS_RESTRICTION"></span><span id="error_dialin_hours_restriction"></span><dl> <span data-ttu-id="346a3-873"><dt><strong>ERROR_DIALIN_HOURS_RESTRICTION</strong></dt> <dt>940</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-873"><dt><strong>ERROR_DIALIN_HOURS_RESTRICTION</strong></dt> <dt>940</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-874">Vous n’êtes pas autorisé à vous connecter pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="346a3-874">You do not have permission to connect at this time.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_ALLOWED_PORT_TYPE_RESTRICTION"></span><span id="error_allowed_port_type_restriction"></span><dl> <span data-ttu-id="346a3-875"><dt><strong>ERROR_ALLOWED_PORT_TYPE_RESTRICTION</strong></dt> <dt>941</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-875"><dt><strong>ERROR_ALLOWED_PORT_TYPE_RESTRICTION</strong></dt> <dt>941</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-876">Vous n’êtes pas autorisé à vous connecter à l’aide du type d’appareil actuel.</span><span class="sxs-lookup"><span data-stu-id="346a3-876">You do not have permission to connect using the current device type.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_AUTH_PROTOCOL_RESTRICTION"></span><span id="error_auth_protocol_restriction"></span><dl> <span data-ttu-id="346a3-877"><dt><strong>ERROR_AUTH_PROTOCOL_RESTRICTION</strong></dt> <dt>942</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-877"><dt><strong>ERROR_AUTH_PROTOCOL_RESTRICTION</strong></dt> <dt>942</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-878">La connexion n’a pas pu être établie, car la méthode d’authentification utilisée par votre profil de connexion n’est pas autorisée pour une utilisation par une stratégie d’accès configurée sur le serveur RAS/VPN.</span><span class="sxs-lookup"><span data-stu-id="346a3-878">The connection could not be established because the authentication method used by your connection profile is not permitted for use by an access policy configured on the RAS/VPN server.</span></span> <span data-ttu-id="346a3-879">Plus précisément, cela peut être dû à des différences de configuration entre la méthode d’authentification sélectionnée sur le serveur RAS/VPN et la stratégie d’accès configurée pour celle-ci.</span><span class="sxs-lookup"><span data-stu-id="346a3-879">Specifically, this could be due to configuration differences between the authentication method selected on the RAS/VPN server and the access policy configured for it.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_BAP_REQUIRED"></span><span id="error_bap_required"></span><dl> <span data-ttu-id="346a3-880"><dt><strong>ERROR_BAP_REQUIRED</strong></dt> <dt>943</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-880"><dt><strong>ERROR_BAP_REQUIRED</strong></dt> <dt>943</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-881">BAP est requis pour cet utilisateur.</span><span class="sxs-lookup"><span data-stu-id="346a3-881">BAP is required for this user.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DIALOUT_HOURS_RESTRICTION"></span><span id="error_dialout_hours_restriction"></span><dl> <span data-ttu-id="346a3-882"><dt><strong>ERROR_DIALOUT_HOURS_RESTRICTION</strong></dt> <dt>944</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-882"><dt><strong>ERROR_DIALOUT_HOURS_RESTRICTION</strong></dt> <dt>944</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-883">L’interface n’est pas autorisée à se connecter pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="346a3-883">The interface is not allowed to connect at this time.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_ROUTER_CONFIG_INCOMPATIBLE"></span><span id="error_router_config_incompatible"></span><dl> <span data-ttu-id="346a3-884"><dt><strong>ERROR_ROUTER_CONFIG_INCOMPATIBLE</strong></dt> <dt>945</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-884"><dt><strong>ERROR_ROUTER_CONFIG_INCOMPATIBLE</strong></dt> <dt>945</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-885">La configuration du routeur enregistrée n’est pas compatible avec le routeur actuel.</span><span class="sxs-lookup"><span data-stu-id="346a3-885">The saved router configuration is incompatible with the current router.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="WARNING_NO_MD5_MIGRATION"></span><span id="warning_no_md5_migration"></span><dl> <span data-ttu-id="346a3-886"><dt><strong>WARNING_NO_MD5_MIGRATION</strong></dt> <dt>946</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-886"><dt><strong>WARNING_NO_MD5_MIGRATION</strong></dt> <dt>946</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-887">L’accès à distance a détecté des comptes d’utilisateur de format plus anciens qui ne seront pas migrés automatiquement.</span><span class="sxs-lookup"><span data-stu-id="346a3-887">Remote Access has detected older format user accounts that will not be migrated automatically.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PROTOCOL_ALREADY_INSTALLED"></span><span id="error_protocol_already_installed"></span><dl> <span data-ttu-id="346a3-888"><dt><strong>ERROR_PROTOCOL_ALREADY_INSTALLED</strong></dt> <dt>948</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-888"><dt><strong>ERROR_PROTOCOL_ALREADY_INSTALLED</strong></dt> <dt>948</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-889">Le transport est déjà installé avec le routeur.</span><span class="sxs-lookup"><span data-stu-id="346a3-889">The transport is already installed with the router.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INVALID_SIGNATURE_LENGTH"></span><span id="error_invalid_signature_length"></span><dl> <span data-ttu-id="346a3-890"><dt><strong>ERROR_INVALID_SIGNATURE_LENGTH</strong></dt> <dt>949</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-890"><dt><strong>ERROR_INVALID_SIGNATURE_LENGTH</strong></dt> <dt>949</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-891">La longueur de signature reçue dans un paquet du serveur RADIUS n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="346a3-891">The signature length received in a packet from RADIUS server is not valid.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-892">Pris en charge dans Windows XP et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-892">Supported in Windows XP and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_SIGNATURE"></span><span id="error_invalid_signature"></span><dl> <span data-ttu-id="346a3-893"><dt><strong>ERROR_INVALID_SIGNATURE</strong></dt> <dt>950</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-893"><dt><strong>ERROR_INVALID_SIGNATURE</strong></dt> <dt>950</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-894">La signature reçue dans un paquet du serveur RADIUS n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="346a3-894">The signature received in a packet from RADIUS server is not valid.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-895">Pris en charge dans Windows XP et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-895">Supported in Windows XP and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_SIGNATURE"></span><span id="error_no_signature"></span><dl> <span data-ttu-id="346a3-896"><dt><strong>ERROR_NO_SIGNATURE</strong></dt> <dt>951</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-896"><dt><strong>ERROR_NO_SIGNATURE</strong></dt> <dt>951</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-897">Impossible de recevoir la signature avec EAPMessage du serveur RADIUS.</span><span class="sxs-lookup"><span data-stu-id="346a3-897">Did not receive signature along with EAPMessage from RADIUS server.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-898">Pris en charge dans Windows XP et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-898">Supported in Windows XP and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_PACKET_LENGTH_OR_ID"></span><span id="error_invalid_packet_length_or_id"></span><dl> <span data-ttu-id="346a3-899"><dt><strong>ERROR_INVALID_PACKET_LENGTH_OR_ID</strong></dt> <dt>952</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-899"><dt><strong>ERROR_INVALID_PACKET_LENGTH_OR_ID</strong></dt> <dt>952</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-900">La longueur ou l’ID reçu dans un paquet du serveur RADIUS n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="346a3-900">The length or Id received in a packet from RADIUS server is not valid.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-901">Pris en charge dans Windows XP et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-901">Supported in Windows XP and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INVALID_ATTRIBUTE_LENGTH"></span><span id="error_invalid_attribute_length"></span><dl> <span data-ttu-id="346a3-902"><dt><strong>ERROR_INVALID_ATTRIBUTE_LENGTH</strong></dt> <dt>953</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-902"><dt><strong>ERROR_INVALID_ATTRIBUTE_LENGTH</strong></dt> <dt>953</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-903">La longueur reçue dans un paquet avec un attribut du serveur RADIUS n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="346a3-903">The length received in a packet with attribute from RADIUS server is not valid.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-904">Pris en charge dans Windows XP et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-904">Supported in Windows XP and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_PACKET"></span><span id="error_invalid_packet"></span><dl> <span data-ttu-id="346a3-905"><dt><strong>ERROR_INVALID_PACKET</strong></dt> <dt>954</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-905"><dt><strong>ERROR_INVALID_PACKET</strong></dt> <dt>954</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-906">Le paquet reçu du serveur RADIUS n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="346a3-906">The packet received from RADIUS server in not valid.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-907">Pris en charge dans Windows XP et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-907">Supported in Windows XP and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_AUTHENTICATOR_MISMATCH"></span><span id="error_authenticator_mismatch"></span><dl> <span data-ttu-id="346a3-908"><dt><strong>ERROR_AUTHENTICATOR_MISMATCH</strong></dt> <dt>955</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-908"><dt><strong>ERROR_AUTHENTICATOR_MISMATCH</strong></dt> <dt>955</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-909">L’authentificateur ne correspond pas au paquet du serveur RADIUS.</span><span class="sxs-lookup"><span data-stu-id="346a3-909">Authenticator does not match in packet from RADIUS server.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-910">Pris en charge dans Windows XP et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-910">Supported in Windows XP and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_REMOTEACCESS_NOT_CONFIGURED"></span><span id="error_remoteaccess_not_configured"></span><dl> <span data-ttu-id="346a3-911"><dt><strong>ERROR_REMOTEACCESS_NOT_CONFIGURED</strong></dt> <dt>956</dt> </span><span class="sxs-lookup"><span data-stu-id="346a3-911"><dt><strong>ERROR_REMOTEACCESS_NOT_CONFIGURED</strong></dt> <dt>956</dt> </span></span></dl></td>
<td><span data-ttu-id="346a3-912">Le serveur de routage et d’accès à distance n’est pas configuré ou n’est pas en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="346a3-912">Routing and Remote access server is either not configured or not running.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="346a3-913">Pris en charge dans Windows 7 et les versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="346a3-913">Supported in Windows 7 and later versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="346a3-914">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="346a3-914">Requirements</span></span>



| <span data-ttu-id="346a3-915">Condition requise</span><span class="sxs-lookup"><span data-stu-id="346a3-915">Requirement</span></span> | <span data-ttu-id="346a3-916">Valeur</span><span class="sxs-lookup"><span data-stu-id="346a3-916">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="346a3-917">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="346a3-917">Minimum supported client</span></span><br/> | <span data-ttu-id="346a3-918">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="346a3-918">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="346a3-919">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="346a3-919">Minimum supported server</span></span><br/> | <span data-ttu-id="346a3-920">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="346a3-920">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



 

 





