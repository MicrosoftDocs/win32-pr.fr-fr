---
description: Décrit les codes d’erreur 1700-3999 définis dans le fichier d’en-tête WinError. h et est destiné aux développeurs.
ms.assetid: 7e57c087-53e4-443d-9227-21d9eb3cc71f
title: Codes d’erreur système (1700-3999) (WinError. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 23b90db71a6e2e84b28f4aafc94475e9e82e3e7a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860673"
---
# <a name="system-error-codes-1700-3999"></a><span data-ttu-id="2ee13-103">Codes d’erreur système (1700-3999)</span><span class="sxs-lookup"><span data-stu-id="2ee13-103">System Error Codes (1700-3999)</span></span>

> [!NOTE]
> <span data-ttu-id="2ee13-104">Ces informations sont destinées aux développeurs qui déboguent les erreurs système.</span><span class="sxs-lookup"><span data-stu-id="2ee13-104">This information is intended for developers debugging system errors.</span></span> <span data-ttu-id="2ee13-105">Pour les autres erreurs, telles que les problèmes de Windows Update, il existe une liste de ressources dans la page [codes d’erreur](system-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="2ee13-105">For other errors, such as issues with Windows Update, there is a list of resources on the [Error codes](system-error-codes.md) page.</span></span>

<span data-ttu-id="2ee13-106">La liste suivante décrit les [codes d’erreur système](system-error-codes.md) pour les erreurs 1700 à 3999.</span><span class="sxs-lookup"><span data-stu-id="2ee13-106">The following list describes [system error codes](system-error-codes.md) for errors 1700 to 3999.</span></span> <span data-ttu-id="2ee13-107">Elles sont retournées par la fonction [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) lorsque de nombreuses fonctions échouent.</span><span class="sxs-lookup"><span data-stu-id="2ee13-107">They are returned by the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function when many functions fail.</span></span> <span data-ttu-id="2ee13-108">Pour récupérer le texte de description de l’erreur dans votre application, utilisez la fonction [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) avec le **format \_ message \_ de \_** l’indicateur système.</span><span class="sxs-lookup"><span data-stu-id="2ee13-108">To retrieve the description text for the error in your application, use the [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) function with the **FORMAT\_MESSAGE\_FROM\_SYSTEM** flag.</span></span>

<dl> <dt>

<span data-ttu-id="2ee13-109"><span id="RPC_S_INVALID_STRING_BINDING"></span><span id="rpc_s_invalid_string_binding"></span>**RPC \_ S \_ \_ liaison de chaîne non valide \_**</span><span class="sxs-lookup"><span data-stu-id="2ee13-109"><span id="RPC_S_INVALID_STRING_BINDING"></span><span id="rpc_s_invalid_string_binding"></span>**RPC\_S\_INVALID\_STRING\_BINDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-110">1700 (0x6A4)</span><span class="sxs-lookup"><span data-stu-id="2ee13-110">1700 (0x6A4)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-111">La liaison de chaîne n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="2ee13-111">The string binding is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-112"><span id="RPC_S_WRONG_KIND_OF_BINDING"></span><span id="rpc_s_wrong_kind_of_binding"></span>**le \_ \_ \_ type \_ de liaison RPC \_ est incorrect**</span><span class="sxs-lookup"><span data-stu-id="2ee13-112"><span id="RPC_S_WRONG_KIND_OF_BINDING"></span><span id="rpc_s_wrong_kind_of_binding"></span>**RPC\_S\_WRONG\_KIND\_OF\_BINDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-113">1701 (0x6A5)</span><span class="sxs-lookup"><span data-stu-id="2ee13-113">1701 (0x6A5)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-114">Le type du handle de liaison n’est pas correct.</span><span class="sxs-lookup"><span data-stu-id="2ee13-114">The binding handle is not the correct type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-115"><span id="RPC_S_INVALID_BINDING"></span><span id="rpc_s_invalid_binding"></span>**\_liaison RPC S \_ non valide \_**</span><span class="sxs-lookup"><span data-stu-id="2ee13-115"><span id="RPC_S_INVALID_BINDING"></span><span id="rpc_s_invalid_binding"></span>**RPC\_S\_INVALID\_BINDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-116">1702 (0x6A6)</span><span class="sxs-lookup"><span data-stu-id="2ee13-116">1702 (0x6A6)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-117">Le handle de liaison n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="2ee13-117">The binding handle is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-118"><span id="RPC_S_PROTSEQ_NOT_SUPPORTED"></span><span id="rpc_s_protseq_not_supported"></span>**RPC \_ S \_ PROTSEQ \_ non \_ pris en charge**</span><span class="sxs-lookup"><span data-stu-id="2ee13-118"><span id="RPC_S_PROTSEQ_NOT_SUPPORTED"></span><span id="rpc_s_protseq_not_supported"></span>**RPC\_S\_PROTSEQ\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-119">1703 (0x6A7)</span><span class="sxs-lookup"><span data-stu-id="2ee13-119">1703 (0x6A7)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-120">La séquence de protocole RPC n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="2ee13-120">The RPC protocol sequence is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-121"><span id="RPC_S_INVALID_RPC_PROTSEQ"></span><span id="rpc_s_invalid_rpc_protseq"></span>**RPC \_ S \_ PROTSEQ non valide \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2ee13-121"><span id="RPC_S_INVALID_RPC_PROTSEQ"></span><span id="rpc_s_invalid_rpc_protseq"></span>**RPC\_S\_INVALID\_RPC\_PROTSEQ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-122">1704 (0x6A8)</span><span class="sxs-lookup"><span data-stu-id="2ee13-122">1704 (0x6A8)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-123">La séquence de protocole RPC n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="2ee13-123">The RPC protocol sequence is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-124"><span id="RPC_S_INVALID_STRING_UUID"></span><span id="rpc_s_invalid_string_uuid"></span>**\_UUID de \_ chaîne non valide RPC \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2ee13-124"><span id="RPC_S_INVALID_STRING_UUID"></span><span id="rpc_s_invalid_string_uuid"></span>**RPC\_S\_INVALID\_STRING\_UUID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-125">1705 (0x6A9)</span><span class="sxs-lookup"><span data-stu-id="2ee13-125">1705 (0x6A9)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-126">L’identificateur unique universel (UUID) de la chaîne n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="2ee13-126">The string universal unique identifier (UUID) is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-127"><span id="RPC_S_INVALID_ENDPOINT_FORMAT"></span><span id="rpc_s_invalid_endpoint_format"></span>**FORMAT de point de terminaison de RPC \_ S \_ non valide \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2ee13-127"><span id="RPC_S_INVALID_ENDPOINT_FORMAT"></span><span id="rpc_s_invalid_endpoint_format"></span>**RPC\_S\_INVALID\_ENDPOINT\_FORMAT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-128">1706 (0x6AA)</span><span class="sxs-lookup"><span data-stu-id="2ee13-128">1706 (0x6AA)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-129">Le format du point de terminaison n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="2ee13-129">The endpoint format is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-130"><span id="RPC_S_INVALID_NET_ADDR"></span><span id="rpc_s_invalid_net_addr"></span>**\_ \_ \_ adresse réseau non valide \_ RPC**</span><span class="sxs-lookup"><span data-stu-id="2ee13-130"><span id="RPC_S_INVALID_NET_ADDR"></span><span id="rpc_s_invalid_net_addr"></span>**RPC\_S\_INVALID\_NET\_ADDR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-131">1707 (0x6AB)</span><span class="sxs-lookup"><span data-stu-id="2ee13-131">1707 (0x6AB)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-132">L’adresse réseau n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="2ee13-132">The network address is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-133"><span id="RPC_S_NO_ENDPOINT_FOUND"></span><span id="rpc_s_no_endpoint_found"></span>**\_ \_ aucun point de \_ terminaison RPC n' \_ a été trouvé**</span><span class="sxs-lookup"><span data-stu-id="2ee13-133"><span id="RPC_S_NO_ENDPOINT_FOUND"></span><span id="rpc_s_no_endpoint_found"></span>**RPC\_S\_NO\_ENDPOINT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-134">1708 (0x6AC)</span><span class="sxs-lookup"><span data-stu-id="2ee13-134">1708 (0x6AC)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-135">Aucun point de terminaison n’a été trouvé.</span><span class="sxs-lookup"><span data-stu-id="2ee13-135">No endpoint was found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-136"><span id="RPC_S_INVALID_TIMEOUT"></span><span id="rpc_s_invalid_timeout"></span>**\_ \_ \_ délai d’attente des S RPC non valide**</span><span class="sxs-lookup"><span data-stu-id="2ee13-136"><span id="RPC_S_INVALID_TIMEOUT"></span><span id="rpc_s_invalid_timeout"></span>**RPC\_S\_INVALID\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-137">1709 (0x6AD)</span><span class="sxs-lookup"><span data-stu-id="2ee13-137">1709 (0x6AD)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-138">La valeur du délai d’attente n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="2ee13-138">The timeout value is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-139"><span id="RPC_S_OBJECT_NOT_FOUND"></span><span id="rpc_s_object_not_found"></span>**\_objet RPC \_ S \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="2ee13-139"><span id="RPC_S_OBJECT_NOT_FOUND"></span><span id="rpc_s_object_not_found"></span>**RPC\_S\_OBJECT\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-140">1710 (0x6AE)</span><span class="sxs-lookup"><span data-stu-id="2ee13-140">1710 (0x6AE)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-141">L’identificateur unique universel (UUID) de l’objet est introuvable.</span><span class="sxs-lookup"><span data-stu-id="2ee13-141">The object universal unique identifier (UUID) was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-142"><span id="RPC_S_ALREADY_REGISTERED"></span><span id="rpc_s_already_registered"></span>**RPC \_ \_ déjà \_ inscrit**</span><span class="sxs-lookup"><span data-stu-id="2ee13-142"><span id="RPC_S_ALREADY_REGISTERED"></span><span id="rpc_s_already_registered"></span>**RPC\_S\_ALREADY\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-143">1711 (0x6AF)</span><span class="sxs-lookup"><span data-stu-id="2ee13-143">1711 (0x6AF)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-144">L’identificateur unique universel (UUID) de l’objet a déjà été inscrit.</span><span class="sxs-lookup"><span data-stu-id="2ee13-144">The object universal unique identifier (UUID) has already been registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-145"><span id="RPC_S_TYPE_ALREADY_REGISTERED"></span><span id="rpc_s_type_already_registered"></span>**\_type RPC \_ S \_ déjà \_ inscrit**</span><span class="sxs-lookup"><span data-stu-id="2ee13-145"><span id="RPC_S_TYPE_ALREADY_REGISTERED"></span><span id="rpc_s_type_already_registered"></span>**RPC\_S\_TYPE\_ALREADY\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-146">1712 (0x6B0)</span><span class="sxs-lookup"><span data-stu-id="2ee13-146">1712 (0x6B0)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-147">Le type d’identificateur unique universel (UUID) a déjà été inscrit.</span><span class="sxs-lookup"><span data-stu-id="2ee13-147">The type universal unique identifier (UUID) has already been registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-148"><span id="RPC_S_ALREADY_LISTENING"></span><span id="rpc_s_already_listening"></span>**RPC \_ déjà à l' \_ \_ écoute**</span><span class="sxs-lookup"><span data-stu-id="2ee13-148"><span id="RPC_S_ALREADY_LISTENING"></span><span id="rpc_s_already_listening"></span>**RPC\_S\_ALREADY\_LISTENING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-149">1713 (0x6B1)</span><span class="sxs-lookup"><span data-stu-id="2ee13-149">1713 (0x6B1)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-150">Le serveur RPC est déjà à l’écoute.</span><span class="sxs-lookup"><span data-stu-id="2ee13-150">The RPC server is already listening.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-151"><span id="RPC_S_NO_PROTSEQS_REGISTERED"></span><span id="rpc_s_no_protseqs_registered"></span>**RPC \_ S \_ non \_ PROTSEQS \_ inscrits**</span><span class="sxs-lookup"><span data-stu-id="2ee13-151"><span id="RPC_S_NO_PROTSEQS_REGISTERED"></span><span id="rpc_s_no_protseqs_registered"></span>**RPC\_S\_NO\_PROTSEQS\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-152">1714 (0x6B2)</span><span class="sxs-lookup"><span data-stu-id="2ee13-152">1714 (0x6B2)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-153">Aucune séquence de protocole n’a été inscrite.</span><span class="sxs-lookup"><span data-stu-id="2ee13-153">No protocol sequences have been registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-154"><span id="RPC_S_NOT_LISTENING"></span><span id="rpc_s_not_listening"></span>**RPC \_ S \_ n' \_ écoutant pas**</span><span class="sxs-lookup"><span data-stu-id="2ee13-154"><span id="RPC_S_NOT_LISTENING"></span><span id="rpc_s_not_listening"></span>**RPC\_S\_NOT\_LISTENING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-155">1715 (0x6B3)</span><span class="sxs-lookup"><span data-stu-id="2ee13-155">1715 (0x6B3)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-156">Le serveur RPC n’est pas à l’écoute.</span><span class="sxs-lookup"><span data-stu-id="2ee13-156">The RPC server is not listening.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-157"><span id="RPC_S_UNKNOWN_MGR_TYPE"></span><span id="rpc_s_unknown_mgr_type"></span>**\_type de \_ \_ Gestionnaire inconnu \_ RPC**</span><span class="sxs-lookup"><span data-stu-id="2ee13-157"><span id="RPC_S_UNKNOWN_MGR_TYPE"></span><span id="rpc_s_unknown_mgr_type"></span>**RPC\_S\_UNKNOWN\_MGR\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-158">1716 (0x6B4)</span><span class="sxs-lookup"><span data-stu-id="2ee13-158">1716 (0x6B4)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-159">Le type de gestionnaire est inconnu.</span><span class="sxs-lookup"><span data-stu-id="2ee13-159">The manager type is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-160"><span id="RPC_S_UNKNOWN_IF"></span><span id="rpc_s_unknown_if"></span>**RPC \_ S \_ inconnu \_ si**</span><span class="sxs-lookup"><span data-stu-id="2ee13-160"><span id="RPC_S_UNKNOWN_IF"></span><span id="rpc_s_unknown_if"></span>**RPC\_S\_UNKNOWN\_IF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-161">1717 (0x6B5)</span><span class="sxs-lookup"><span data-stu-id="2ee13-161">1717 (0x6B5)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-162">L’interface est inconnue.</span><span class="sxs-lookup"><span data-stu-id="2ee13-162">The interface is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-163"><span id="RPC_S_NO_BINDINGS"></span><span id="rpc_s_no_bindings"></span>**\_ \_ aucune \_ liaison RPC**</span><span class="sxs-lookup"><span data-stu-id="2ee13-163"><span id="RPC_S_NO_BINDINGS"></span><span id="rpc_s_no_bindings"></span>**RPC\_S\_NO\_BINDINGS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-164">1718 (0x6B6)</span><span class="sxs-lookup"><span data-stu-id="2ee13-164">1718 (0x6B6)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-165">Il n’y a aucune liaison.</span><span class="sxs-lookup"><span data-stu-id="2ee13-165">There are no bindings.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-166"><span id="RPC_S_NO_PROTSEQS"></span><span id="rpc_s_no_protseqs"></span>**RPC \_ S \_ non \_ PROTSEQS**</span><span class="sxs-lookup"><span data-stu-id="2ee13-166"><span id="RPC_S_NO_PROTSEQS"></span><span id="rpc_s_no_protseqs"></span>**RPC\_S\_NO\_PROTSEQS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-167">1719 (0x6B7)</span><span class="sxs-lookup"><span data-stu-id="2ee13-167">1719 (0x6B7)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-168">Il n’existe aucune séquence de protocole.</span><span class="sxs-lookup"><span data-stu-id="2ee13-168">There are no protocol sequences.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-169"><span id="RPC_S_CANT_CREATE_ENDPOINT"></span><span id="rpc_s_cant_create_endpoint"></span>**RPC \_ \_ Impossible de \_ créer un \_ point de terminaison**</span><span class="sxs-lookup"><span data-stu-id="2ee13-169"><span id="RPC_S_CANT_CREATE_ENDPOINT"></span><span id="rpc_s_cant_create_endpoint"></span>**RPC\_S\_CANT\_CREATE\_ENDPOINT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-170">1720 (0x6B8)</span><span class="sxs-lookup"><span data-stu-id="2ee13-170">1720 (0x6B8)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-171">Impossible de créer le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="2ee13-171">The endpoint cannot be created.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-172"><span id="RPC_S_OUT_OF_RESOURCES"></span><span id="rpc_s_out_of_resources"></span>**\_ressources RPC \_ insuffisantes \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2ee13-172"><span id="RPC_S_OUT_OF_RESOURCES"></span><span id="rpc_s_out_of_resources"></span>**RPC\_S\_OUT\_OF\_RESOURCES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-173">1721 (0x6B9)</span><span class="sxs-lookup"><span data-stu-id="2ee13-173">1721 (0x6B9)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-174">Les ressources disponibles sont insuffisantes pour terminer cette opération.</span><span class="sxs-lookup"><span data-stu-id="2ee13-174">Not enough resources are available to complete this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-175"><span id="RPC_S_SERVER_UNAVAILABLE"></span><span id="rpc_s_server_unavailable"></span>**\_serveur RPC \_ S \_ non disponible**</span><span class="sxs-lookup"><span data-stu-id="2ee13-175"><span id="RPC_S_SERVER_UNAVAILABLE"></span><span id="rpc_s_server_unavailable"></span>**RPC\_S\_SERVER\_UNAVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-176">1722 (0x6BA)</span><span class="sxs-lookup"><span data-stu-id="2ee13-176">1722 (0x6BA)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-177">Le serveur RPC est indisponible.</span><span class="sxs-lookup"><span data-stu-id="2ee13-177">The RPC server is unavailable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-178"><span id="RPC_S_SERVER_TOO_BUSY"></span><span id="rpc_s_server_too_busy"></span>**\_serveur RPC \_ S \_ encombré \_**</span><span class="sxs-lookup"><span data-stu-id="2ee13-178"><span id="RPC_S_SERVER_TOO_BUSY"></span><span id="rpc_s_server_too_busy"></span>**RPC\_S\_SERVER\_TOO\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-179">1723 (0x6BB)</span><span class="sxs-lookup"><span data-stu-id="2ee13-179">1723 (0x6BB)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-180">Le serveur RPC est trop occupé pour terminer cette opération.</span><span class="sxs-lookup"><span data-stu-id="2ee13-180">The RPC server is too busy to complete this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-181"><span id="RPC_S_INVALID_NETWORK_OPTIONS"></span><span id="rpc_s_invalid_network_options"></span>**\_ \_ options réseau non VALIDEs RPC \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2ee13-181"><span id="RPC_S_INVALID_NETWORK_OPTIONS"></span><span id="rpc_s_invalid_network_options"></span>**RPC\_S\_INVALID\_NETWORK\_OPTIONS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-182">1724 (0x6BC)</span><span class="sxs-lookup"><span data-stu-id="2ee13-182">1724 (0x6BC)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-183">Les options réseau ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="2ee13-183">The network options are invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-184"><span id="RPC_S_NO_CALL_ACTIVE"></span><span id="rpc_s_no_call_active"></span>**RPC \_ S \_ aucun \_ appel \_ actif**</span><span class="sxs-lookup"><span data-stu-id="2ee13-184"><span id="RPC_S_NO_CALL_ACTIVE"></span><span id="rpc_s_no_call_active"></span>**RPC\_S\_NO\_CALL\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-185">1725 (0x6BD)</span><span class="sxs-lookup"><span data-stu-id="2ee13-185">1725 (0x6BD)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-186">Aucun appel de procédure distante n’est actif sur ce thread.</span><span class="sxs-lookup"><span data-stu-id="2ee13-186">There are no remote procedure calls active on this thread.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-187"><span id="RPC_S_CALL_FAILED"></span><span id="rpc_s_call_failed"></span>**échec de l' \_ appel RPC S \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2ee13-187"><span id="RPC_S_CALL_FAILED"></span><span id="rpc_s_call_failed"></span>**RPC\_S\_CALL\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-188">1726 (0x6BE)</span><span class="sxs-lookup"><span data-stu-id="2ee13-188">1726 (0x6BE)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-189">L’appel de procédure distante a échoué.</span><span class="sxs-lookup"><span data-stu-id="2ee13-189">The remote procedure call failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-190"><span id="RPC_S_CALL_FAILED_DNE"></span><span id="rpc_s_call_failed_dne"></span>**échec de l’appel des RPC \_ S \_ \_ \_ dne**</span><span class="sxs-lookup"><span data-stu-id="2ee13-190"><span id="RPC_S_CALL_FAILED_DNE"></span><span id="rpc_s_call_failed_dne"></span>**RPC\_S\_CALL\_FAILED\_DNE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-191">1727 (0x6BF)</span><span class="sxs-lookup"><span data-stu-id="2ee13-191">1727 (0x6BF)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-192">L’appel de procédure distante a échoué et ne s’est pas exécuté.</span><span class="sxs-lookup"><span data-stu-id="2ee13-192">The remote procedure call failed and did not execute.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-193"><span id="RPC_S_PROTOCOL_ERROR"></span><span id="rpc_s_protocol_error"></span>**\_erreur de \_ protocole \_ S RPC**</span><span class="sxs-lookup"><span data-stu-id="2ee13-193"><span id="RPC_S_PROTOCOL_ERROR"></span><span id="rpc_s_protocol_error"></span>**RPC\_S\_PROTOCOL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-194">1728 (0x6C0)</span><span class="sxs-lookup"><span data-stu-id="2ee13-194">1728 (0x6C0)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-195">Une erreur de protocole d’appel de procédure distante (RPC) s’est produite.</span><span class="sxs-lookup"><span data-stu-id="2ee13-195">A remote procedure call (RPC) protocol error occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-196"><span id="RPC_S_PROXY_ACCESS_DENIED"></span><span id="rpc_s_proxy_access_denied"></span>**\_ \_ accès proxy RPC \_ \_ refusé**</span><span class="sxs-lookup"><span data-stu-id="2ee13-196"><span id="RPC_S_PROXY_ACCESS_DENIED"></span><span id="rpc_s_proxy_access_denied"></span>**RPC\_S\_PROXY\_ACCESS\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-197">1729 (0x6C1)</span><span class="sxs-lookup"><span data-stu-id="2ee13-197">1729 (0x6C1)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-198">L’accès au proxy HTTP est refusé.</span><span class="sxs-lookup"><span data-stu-id="2ee13-198">Access to the HTTP proxy is denied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-199"><span id="RPC_S_UNSUPPORTED_TRANS_SYN"></span><span id="rpc_s_unsupported_trans_syn"></span>**RPC \_ \_ non pris en charge par \_ TRANS \_ syn**</span><span class="sxs-lookup"><span data-stu-id="2ee13-199"><span id="RPC_S_UNSUPPORTED_TRANS_SYN"></span><span id="rpc_s_unsupported_trans_syn"></span>**RPC\_S\_UNSUPPORTED\_TRANS\_SYN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-200">1730 (0x6C2)</span><span class="sxs-lookup"><span data-stu-id="2ee13-200">1730 (0x6C2)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-201">La syntaxe de transfert n’est pas prise en charge par le serveur RPC.</span><span class="sxs-lookup"><span data-stu-id="2ee13-201">The transfer syntax is not supported by the RPC server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-202"><span id="RPC_S_UNSUPPORTED_TYPE"></span><span id="rpc_s_unsupported_type"></span>**\_ \_ type non pris en charge par RPC \_**</span><span class="sxs-lookup"><span data-stu-id="2ee13-202"><span id="RPC_S_UNSUPPORTED_TYPE"></span><span id="rpc_s_unsupported_type"></span>**RPC\_S\_UNSUPPORTED\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-203">1732 (0x6C4)</span><span class="sxs-lookup"><span data-stu-id="2ee13-203">1732 (0x6C4)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-204">Le type d’identificateur unique universel (UUID) n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="2ee13-204">The universal unique identifier (UUID) type is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-205"><span id="RPC_S_INVALID_TAG"></span><span id="rpc_s_invalid_tag"></span>**\_ \_ balise RPC S non valide \_**</span><span class="sxs-lookup"><span data-stu-id="2ee13-205"><span id="RPC_S_INVALID_TAG"></span><span id="rpc_s_invalid_tag"></span>**RPC\_S\_INVALID\_TAG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-206">1733 (0x6C5)</span><span class="sxs-lookup"><span data-stu-id="2ee13-206">1733 (0x6C5)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-207">La balise n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="2ee13-207">The tag is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-208"><span id="RPC_S_INVALID_BOUND"></span><span id="rpc_s_invalid_bound"></span>**\_liaison RPC \_ non valide \_**</span><span class="sxs-lookup"><span data-stu-id="2ee13-208"><span id="RPC_S_INVALID_BOUND"></span><span id="rpc_s_invalid_bound"></span>**RPC\_S\_INVALID\_BOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-209">1734 (0x6C6)</span><span class="sxs-lookup"><span data-stu-id="2ee13-209">1734 (0x6C6)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-210">Les limites du tableau ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="2ee13-210">The array bounds are invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-211"><span id="RPC_S_NO_ENTRY_NAME"></span><span id="rpc_s_no_entry_name"></span>**RPC \_ \_ sans \_ nom d’entrée \_**</span><span class="sxs-lookup"><span data-stu-id="2ee13-211"><span id="RPC_S_NO_ENTRY_NAME"></span><span id="rpc_s_no_entry_name"></span>**RPC\_S\_NO\_ENTRY\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-212">1735 (0x6C7)</span><span class="sxs-lookup"><span data-stu-id="2ee13-212">1735 (0x6C7)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-213">La liaison ne contient pas de nom d’entrée.</span><span class="sxs-lookup"><span data-stu-id="2ee13-213">The binding does not contain an entry name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-214"><span id="RPC_S_INVALID_NAME_SYNTAX"></span><span id="rpc_s_invalid_name_syntax"></span>**RPC \_ S \_ \_ syntaxe de nom non valide \_**</span><span class="sxs-lookup"><span data-stu-id="2ee13-214"><span id="RPC_S_INVALID_NAME_SYNTAX"></span><span id="rpc_s_invalid_name_syntax"></span>**RPC\_S\_INVALID\_NAME\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-215">1736 (0x6C8)</span><span class="sxs-lookup"><span data-stu-id="2ee13-215">1736 (0x6C8)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-216">La syntaxe du nom n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="2ee13-216">The name syntax is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-217"><span id="RPC_S_UNSUPPORTED_NAME_SYNTAX"></span><span id="rpc_s_unsupported_name_syntax"></span>**RPC \_ S \_ syntaxe de nom non prise en charge \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2ee13-217"><span id="RPC_S_UNSUPPORTED_NAME_SYNTAX"></span><span id="rpc_s_unsupported_name_syntax"></span>**RPC\_S\_UNSUPPORTED\_NAME\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-218">1737 (0x6C9)</span><span class="sxs-lookup"><span data-stu-id="2ee13-218">1737 (0x6C9)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-219">La syntaxe du nom n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="2ee13-219">The name syntax is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-220"><span id="RPC_S_UUID_NO_ADDRESS"></span><span id="rpc_s_uuid_no_address"></span>**\_UUID RPC \_ S \_ aucune \_ adresse**</span><span class="sxs-lookup"><span data-stu-id="2ee13-220"><span id="RPC_S_UUID_NO_ADDRESS"></span><span id="rpc_s_uuid_no_address"></span>**RPC\_S\_UUID\_NO\_ADDRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-221">1739 (0x6CB)</span><span class="sxs-lookup"><span data-stu-id="2ee13-221">1739 (0x6CB)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-222">Aucune adresse réseau ne peut être utilisée pour construire un identificateur unique universel (UUID).</span><span class="sxs-lookup"><span data-stu-id="2ee13-222">No network address is available to use to construct a universal unique identifier (UUID).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-223"><span id="RPC_S_DUPLICATE_ENDPOINT"></span><span id="rpc_s_duplicate_endpoint"></span>**\_point de terminaison RPC S \_ dupliqué \_**</span><span class="sxs-lookup"><span data-stu-id="2ee13-223"><span id="RPC_S_DUPLICATE_ENDPOINT"></span><span id="rpc_s_duplicate_endpoint"></span>**RPC\_S\_DUPLICATE\_ENDPOINT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-224">1740 (0x6CC)</span><span class="sxs-lookup"><span data-stu-id="2ee13-224">1740 (0x6CC)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-225">Le point de terminaison est un doublon.</span><span class="sxs-lookup"><span data-stu-id="2ee13-225">The endpoint is a duplicate.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-226"><span id="RPC_S_UNKNOWN_AUTHN_TYPE"></span><span id="rpc_s_unknown_authn_type"></span>**\_ \_ \_ type AUTHn inconnu RPC \_**</span><span class="sxs-lookup"><span data-stu-id="2ee13-226"><span id="RPC_S_UNKNOWN_AUTHN_TYPE"></span><span id="rpc_s_unknown_authn_type"></span>**RPC\_S\_UNKNOWN\_AUTHN\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-227">1741 (0x6CD)</span><span class="sxs-lookup"><span data-stu-id="2ee13-227">1741 (0x6CD)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-228">Le type d’authentification est inconnu.</span><span class="sxs-lookup"><span data-stu-id="2ee13-228">The authentication type is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-229"><span id="RPC_S_MAX_CALLS_TOO_SMALL"></span><span id="rpc_s_max_calls_too_small"></span>**\_ \_ nombre maximal d’appels RPC S \_ \_ trop \_ petit**</span><span class="sxs-lookup"><span data-stu-id="2ee13-229"><span id="RPC_S_MAX_CALLS_TOO_SMALL"></span><span id="rpc_s_max_calls_too_small"></span>**RPC\_S\_MAX\_CALLS\_TOO\_SMALL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-230">1742 (0x6CE)</span><span class="sxs-lookup"><span data-stu-id="2ee13-230">1742 (0x6CE)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-231">Le nombre maximal d’appels est trop petit.</span><span class="sxs-lookup"><span data-stu-id="2ee13-231">The maximum number of calls is too small.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-232"><span id="RPC_S_STRING_TOO_LONG"></span><span id="rpc_s_string_too_long"></span>**\_chaîne RPC \_ \_ trop \_ longue**</span><span class="sxs-lookup"><span data-stu-id="2ee13-232"><span id="RPC_S_STRING_TOO_LONG"></span><span id="rpc_s_string_too_long"></span>**RPC\_S\_STRING\_TOO\_LONG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-233">1743 (0x6CF)</span><span class="sxs-lookup"><span data-stu-id="2ee13-233">1743 (0x6CF)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-234">La chaîne est trop longue.</span><span class="sxs-lookup"><span data-stu-id="2ee13-234">The string is too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-235"><span id="RPC_S_PROTSEQ_NOT_FOUND"></span><span id="rpc_s_protseq_not_found"></span>**RPC \_ S \_ PROTSEQ \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="2ee13-235"><span id="RPC_S_PROTSEQ_NOT_FOUND"></span><span id="rpc_s_protseq_not_found"></span>**RPC\_S\_PROTSEQ\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-236">1744 (0x6D0)</span><span class="sxs-lookup"><span data-stu-id="2ee13-236">1744 (0x6D0)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-237">La séquence de protocole RPC est introuvable.</span><span class="sxs-lookup"><span data-stu-id="2ee13-237">The RPC protocol sequence was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-238"><span id="RPC_S_PROCNUM_OUT_OF_RANGE"></span><span id="rpc_s_procnum_out_of_range"></span>**RPC \_ S \_ PROCNUM \_ hors \_ \_ limites**</span><span class="sxs-lookup"><span data-stu-id="2ee13-238"><span id="RPC_S_PROCNUM_OUT_OF_RANGE"></span><span id="rpc_s_procnum_out_of_range"></span>**RPC\_S\_PROCNUM\_OUT\_OF\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-239">1745 (0x6D1)</span><span class="sxs-lookup"><span data-stu-id="2ee13-239">1745 (0x6D1)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-240">Le numéro de la procédure est hors limites.</span><span class="sxs-lookup"><span data-stu-id="2ee13-240">The procedure number is out of range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-241"><span id="RPC_S_BINDING_HAS_NO_AUTH"></span><span id="rpc_s_binding_has_no_auth"></span>**la \_ liaison RPC S n' \_ \_ a \_ pas d' \_ authentification**</span><span class="sxs-lookup"><span data-stu-id="2ee13-241"><span id="RPC_S_BINDING_HAS_NO_AUTH"></span><span id="rpc_s_binding_has_no_auth"></span>**RPC\_S\_BINDING\_HAS\_NO\_AUTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-242">1746 (0x6D2)</span><span class="sxs-lookup"><span data-stu-id="2ee13-242">1746 (0x6D2)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-243">La liaison ne contient pas d’informations d’authentification.</span><span class="sxs-lookup"><span data-stu-id="2ee13-243">The binding does not contain any authentication information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-244"><span id="RPC_S_UNKNOWN_AUTHN_SERVICE"></span><span id="rpc_s_unknown_authn_service"></span>**RPC \_ S \_ \_ service d’authentification inconnu \_**</span><span class="sxs-lookup"><span data-stu-id="2ee13-244"><span id="RPC_S_UNKNOWN_AUTHN_SERVICE"></span><span id="rpc_s_unknown_authn_service"></span>**RPC\_S\_UNKNOWN\_AUTHN\_SERVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-245">1747 (0x6D3)</span><span class="sxs-lookup"><span data-stu-id="2ee13-245">1747 (0x6D3)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-246">Le service d’authentification est inconnu.</span><span class="sxs-lookup"><span data-stu-id="2ee13-246">The authentication service is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-247"><span id="RPC_S_UNKNOWN_AUTHN_LEVEL"></span><span id="rpc_s_unknown_authn_level"></span>**\_niveau d' \_ authentification inconnue RPC S \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2ee13-247"><span id="RPC_S_UNKNOWN_AUTHN_LEVEL"></span><span id="rpc_s_unknown_authn_level"></span>**RPC\_S\_UNKNOWN\_AUTHN\_LEVEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-248">1748 (0x6D4)</span><span class="sxs-lookup"><span data-stu-id="2ee13-248">1748 (0x6D4)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-249">Le niveau d’authentification est inconnu.</span><span class="sxs-lookup"><span data-stu-id="2ee13-249">The authentication level is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-250"><span id="RPC_S_INVALID_AUTH_IDENTITY"></span><span id="rpc_s_invalid_auth_identity"></span>**\_identité d’authentification RPC S \_ non valide \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2ee13-250"><span id="RPC_S_INVALID_AUTH_IDENTITY"></span><span id="rpc_s_invalid_auth_identity"></span>**RPC\_S\_INVALID\_AUTH\_IDENTITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-251">1749 (0x6D5)</span><span class="sxs-lookup"><span data-stu-id="2ee13-251">1749 (0x6D5)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-252">Le contexte de sécurité n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="2ee13-252">The security context is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-253"><span id="RPC_S_UNKNOWN_AUTHZ_SERVICE"></span><span id="rpc_s_unknown_authz_service"></span>**RPC \_ S \_ service d’autorisation inconnu \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2ee13-253"><span id="RPC_S_UNKNOWN_AUTHZ_SERVICE"></span><span id="rpc_s_unknown_authz_service"></span>**RPC\_S\_UNKNOWN\_AUTHZ\_SERVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-254">1750 (0x6D6)</span><span class="sxs-lookup"><span data-stu-id="2ee13-254">1750 (0x6D6)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-255">Le service d’autorisation est inconnu.</span><span class="sxs-lookup"><span data-stu-id="2ee13-255">The authorization service is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-256"><span id="EPT_S_INVALID_ENTRY"></span><span id="ept_s_invalid_entry"></span>**\_entrée EPT S \_ non valide \_**</span><span class="sxs-lookup"><span data-stu-id="2ee13-256"><span id="EPT_S_INVALID_ENTRY"></span><span id="ept_s_invalid_entry"></span>**EPT\_S\_INVALID\_ENTRY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-257">1751 (0x6D7)</span><span class="sxs-lookup"><span data-stu-id="2ee13-257">1751 (0x6D7)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-258">L’entrée n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="2ee13-258">The entry is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-259"><span id="EPT_S_CANT_PERFORM_OP"></span><span id="ept_s_cant_perform_op"></span>**EPT \_ S ne pas \_ effectuer d' \_ \_ opérations**</span><span class="sxs-lookup"><span data-stu-id="2ee13-259"><span id="EPT_S_CANT_PERFORM_OP"></span><span id="ept_s_cant_perform_op"></span>**EPT\_S\_CANT\_PERFORM\_OP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-260">1752 (0x6D8)</span><span class="sxs-lookup"><span data-stu-id="2ee13-260">1752 (0x6D8)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-261">Le point de terminaison de serveur ne peut pas effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="2ee13-261">The server endpoint cannot perform the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-262"><span id="EPT_S_NOT_REGISTERED"></span><span id="ept_s_not_registered"></span>**EPT \_ S \_ non \_ inscrit**</span><span class="sxs-lookup"><span data-stu-id="2ee13-262"><span id="EPT_S_NOT_REGISTERED"></span><span id="ept_s_not_registered"></span>**EPT\_S\_NOT\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-263">1753 (0x6D9)</span><span class="sxs-lookup"><span data-stu-id="2ee13-263">1753 (0x6D9)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-264">il n’y a plus de points de terminaison disponibles auprès du mappeur de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="2ee13-264">There are no more endpoints available from the endpoint mapper.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-265"><span id="RPC_S_NOTHING_TO_EXPORT"></span><span id="rpc_s_nothing_to_export"></span>**RPC \_ S \_ rien \_ à \_ Exporter**</span><span class="sxs-lookup"><span data-stu-id="2ee13-265"><span id="RPC_S_NOTHING_TO_EXPORT"></span><span id="rpc_s_nothing_to_export"></span>**RPC\_S\_NOTHING\_TO\_EXPORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-266">1754 (0x6DA)</span><span class="sxs-lookup"><span data-stu-id="2ee13-266">1754 (0x6DA)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-267">Aucune interface n’a été exportée.</span><span class="sxs-lookup"><span data-stu-id="2ee13-267">No interfaces have been exported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-268"><span id="RPC_S_INCOMPLETE_NAME"></span><span id="rpc_s_incomplete_name"></span>**\_ \_ nom incomplet RPC S \_**</span><span class="sxs-lookup"><span data-stu-id="2ee13-268"><span id="RPC_S_INCOMPLETE_NAME"></span><span id="rpc_s_incomplete_name"></span>**RPC\_S\_INCOMPLETE\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-269">1755 (0x6DB)</span><span class="sxs-lookup"><span data-stu-id="2ee13-269">1755 (0x6DB)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-270">Le nom de l’entrée est incomplet.</span><span class="sxs-lookup"><span data-stu-id="2ee13-270">The entry name is incomplete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-271"><span id="RPC_S_INVALID_VERS_OPTION"></span><span id="rpc_s_invalid_vers_option"></span>**\_option RPC S \_ non valide \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2ee13-271"><span id="RPC_S_INVALID_VERS_OPTION"></span><span id="rpc_s_invalid_vers_option"></span>**RPC\_S\_INVALID\_VERS\_OPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-272">1756 (0x6DC)</span><span class="sxs-lookup"><span data-stu-id="2ee13-272">1756 (0x6DC)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-273">L’option version n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="2ee13-273">The version option is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-274"><span id="RPC_S_NO_MORE_MEMBERS"></span><span id="rpc_s_no_more_members"></span>**RPC \_ \_ ne pas \_ plus de \_ membres**</span><span class="sxs-lookup"><span data-stu-id="2ee13-274"><span id="RPC_S_NO_MORE_MEMBERS"></span><span id="rpc_s_no_more_members"></span>**RPC\_S\_NO\_MORE\_MEMBERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-275">1757 (0x6DD)</span><span class="sxs-lookup"><span data-stu-id="2ee13-275">1757 (0x6DD)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-276">Il n’y a plus de membres.</span><span class="sxs-lookup"><span data-stu-id="2ee13-276">There are no more members.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-277"><span id="RPC_S_NOT_ALL_OBJS_UNEXPORTED"></span><span id="rpc_s_not_all_objs_unexported"></span>**RPC \_ \_ non \_ tous les \_ ne comportaient non \_ exportés**</span><span class="sxs-lookup"><span data-stu-id="2ee13-277"><span id="RPC_S_NOT_ALL_OBJS_UNEXPORTED"></span><span id="rpc_s_not_all_objs_unexported"></span>**RPC\_S\_NOT\_ALL\_OBJS\_UNEXPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-278">1758 (0x6DE)</span><span class="sxs-lookup"><span data-stu-id="2ee13-278">1758 (0x6DE)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-279">Il n’y a rien à désexporter.</span><span class="sxs-lookup"><span data-stu-id="2ee13-279">There is nothing to unexport.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-280"><span id="RPC_S_INTERFACE_NOT_FOUND"></span><span id="rpc_s_interface_not_found"></span>**\_interface RPC \_ S \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="2ee13-280"><span id="RPC_S_INTERFACE_NOT_FOUND"></span><span id="rpc_s_interface_not_found"></span>**RPC\_S\_INTERFACE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-281">1759 (0x6DF)</span><span class="sxs-lookup"><span data-stu-id="2ee13-281">1759 (0x6DF)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-282">L’interface est introuvable.</span><span class="sxs-lookup"><span data-stu-id="2ee13-282">The interface was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-283"><span id="RPC_S_ENTRY_ALREADY_EXISTS"></span><span id="rpc_s_entry_already_exists"></span>**l' \_ entrée RPC S \_ \_ \_ existe déjà**</span><span class="sxs-lookup"><span data-stu-id="2ee13-283"><span id="RPC_S_ENTRY_ALREADY_EXISTS"></span><span id="rpc_s_entry_already_exists"></span>**RPC\_S\_ENTRY\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-284">1760 (0x6E0)</span><span class="sxs-lookup"><span data-stu-id="2ee13-284">1760 (0x6E0)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-285">L’entrée existe déjà.</span><span class="sxs-lookup"><span data-stu-id="2ee13-285">The entry already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-286"><span id="RPC_S_ENTRY_NOT_FOUND"></span><span id="rpc_s_entry_not_found"></span>**\_entrée RPC \_ S \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="2ee13-286"><span id="RPC_S_ENTRY_NOT_FOUND"></span><span id="rpc_s_entry_not_found"></span>**RPC\_S\_ENTRY\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-287">1761 (0x6E1)</span><span class="sxs-lookup"><span data-stu-id="2ee13-287">1761 (0x6E1)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-288">L’entrée est introuvable.</span><span class="sxs-lookup"><span data-stu-id="2ee13-288">The entry is not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-289"><span id="RPC_S_NAME_SERVICE_UNAVAILABLE"></span><span id="rpc_s_name_service_unavailable"></span>**\_service de \_ noms \_ RPC \_ non disponible**</span><span class="sxs-lookup"><span data-stu-id="2ee13-289"><span id="RPC_S_NAME_SERVICE_UNAVAILABLE"></span><span id="rpc_s_name_service_unavailable"></span>**RPC\_S\_NAME\_SERVICE\_UNAVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-290">1762 (0x6E2)</span><span class="sxs-lookup"><span data-stu-id="2ee13-290">1762 (0x6E2)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-291">Le service de noms n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="2ee13-291">The name service is unavailable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-292"><span id="RPC_S_INVALID_NAF_ID"></span><span id="rpc_s_invalid_naf_id"></span>**\_ \_ \_ ID NAF non valide \_ de RPC**</span><span class="sxs-lookup"><span data-stu-id="2ee13-292"><span id="RPC_S_INVALID_NAF_ID"></span><span id="rpc_s_invalid_naf_id"></span>**RPC\_S\_INVALID\_NAF\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-293">1763 (0x6E3)</span><span class="sxs-lookup"><span data-stu-id="2ee13-293">1763 (0x6E3)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-294">La famille d’adresses réseau n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="2ee13-294">The network address family is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-295"><span id="RPC_S_CANNOT_SUPPORT"></span><span id="rpc_s_cannot_support"></span>**RPC \_ \_ ne peut pas \_ prendre en charge**</span><span class="sxs-lookup"><span data-stu-id="2ee13-295"><span id="RPC_S_CANNOT_SUPPORT"></span><span id="rpc_s_cannot_support"></span>**RPC\_S\_CANNOT\_SUPPORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-296">1764 (0x6E4)</span><span class="sxs-lookup"><span data-stu-id="2ee13-296">1764 (0x6E4)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-297">L'opération demandée n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="2ee13-297">The requested operation is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-298"><span id="RPC_S_NO_CONTEXT_AVAILABLE"></span><span id="rpc_s_no_context_available"></span>**RPC \_ \_ sans \_ contexte \_ disponible**</span><span class="sxs-lookup"><span data-stu-id="2ee13-298"><span id="RPC_S_NO_CONTEXT_AVAILABLE"></span><span id="rpc_s_no_context_available"></span>**RPC\_S\_NO\_CONTEXT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-299">1765 (0x6E5)</span><span class="sxs-lookup"><span data-stu-id="2ee13-299">1765 (0x6E5)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-300">Aucun contexte de sécurité n’est disponible pour autoriser l’emprunt d’identité.</span><span class="sxs-lookup"><span data-stu-id="2ee13-300">No security context is available to allow impersonation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-301"><span id="RPC_S_INTERNAL_ERROR"></span><span id="rpc_s_internal_error"></span>**\_ \_ erreur interne RPC \_ S**</span><span class="sxs-lookup"><span data-stu-id="2ee13-301"><span id="RPC_S_INTERNAL_ERROR"></span><span id="rpc_s_internal_error"></span>**RPC\_S\_INTERNAL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-302">1766 (0x6E6)</span><span class="sxs-lookup"><span data-stu-id="2ee13-302">1766 (0x6E6)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-303">Une erreur interne s’est produite dans un appel de procédure distante (RPC).</span><span class="sxs-lookup"><span data-stu-id="2ee13-303">An internal error occurred in a remote procedure call (RPC).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-304"><span id="RPC_S_ZERO_DIVIDE"></span><span id="rpc_s_zero_divide"></span>**\_ \_ Division zéro du \_ RPC**</span><span class="sxs-lookup"><span data-stu-id="2ee13-304"><span id="RPC_S_ZERO_DIVIDE"></span><span id="rpc_s_zero_divide"></span>**RPC\_S\_ZERO\_DIVIDE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-305">1767 (0x6E7)</span><span class="sxs-lookup"><span data-stu-id="2ee13-305">1767 (0x6E7)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-306">Le serveur RPC a tenté une division d’entier par zéro.</span><span class="sxs-lookup"><span data-stu-id="2ee13-306">The RPC server attempted an integer division by zero.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-307"><span id="RPC_S_ADDRESS_ERROR"></span><span id="rpc_s_address_error"></span>**\_erreur d' \_ adresse RPC S \_**</span><span class="sxs-lookup"><span data-stu-id="2ee13-307"><span id="RPC_S_ADDRESS_ERROR"></span><span id="rpc_s_address_error"></span>**RPC\_S\_ADDRESS\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-308">1768 (0x6E8)</span><span class="sxs-lookup"><span data-stu-id="2ee13-308">1768 (0x6E8)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-309">Une erreur d’adressage s’est produite sur le serveur RPC.</span><span class="sxs-lookup"><span data-stu-id="2ee13-309">An addressing error occurred in the RPC server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-310"><span id="RPC_S_FP_DIV_ZERO"></span><span id="rpc_s_fp_div_zero"></span>**\_ \_ \_ valeur zéro div FP \_ de RPC**</span><span class="sxs-lookup"><span data-stu-id="2ee13-310"><span id="RPC_S_FP_DIV_ZERO"></span><span id="rpc_s_fp_div_zero"></span>**RPC\_S\_FP\_DIV\_ZERO**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-311">1769 (0x6E9)</span><span class="sxs-lookup"><span data-stu-id="2ee13-311">1769 (0x6E9)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-312">Une opération à virgule flottante au niveau du serveur RPC a provoqué une division par zéro.</span><span class="sxs-lookup"><span data-stu-id="2ee13-312">A floating-point operation at the RPC server caused a division by zero.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-313"><span id="RPC_S_FP_UNDERFLOW"></span><span id="rpc_s_fp_underflow"></span>**dépassement de capacité négatif RPC \_ S \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2ee13-313"><span id="RPC_S_FP_UNDERFLOW"></span><span id="rpc_s_fp_underflow"></span>**RPC\_S\_FP\_UNDERFLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-314">1770 (0x6EA)</span><span class="sxs-lookup"><span data-stu-id="2ee13-314">1770 (0x6EA)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-315">Un dépassement de capacité négatif à virgule flottante s’est produit au niveau du serveur RPC.</span><span class="sxs-lookup"><span data-stu-id="2ee13-315">A floating-point underflow occurred at the RPC server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-316"><span id="RPC_S_FP_OVERFLOW"></span><span id="rpc_s_fp_overflow"></span>**\_dépassement de \_ capacité du FP RPC S \_**</span><span class="sxs-lookup"><span data-stu-id="2ee13-316"><span id="RPC_S_FP_OVERFLOW"></span><span id="rpc_s_fp_overflow"></span>**RPC\_S\_FP\_OVERFLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-317">1771 (0x6EB)</span><span class="sxs-lookup"><span data-stu-id="2ee13-317">1771 (0x6EB)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-318">Un dépassement de capacité à virgule flottante s’est produit au niveau du serveur RPC.</span><span class="sxs-lookup"><span data-stu-id="2ee13-318">A floating-point overflow occurred at the RPC server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-319"><span id="RPC_X_NO_MORE_ENTRIES"></span><span id="rpc_x_no_more_entries"></span>**RPC \_ X \_ \_ plus d' \_ entrées**</span><span class="sxs-lookup"><span data-stu-id="2ee13-319"><span id="RPC_X_NO_MORE_ENTRIES"></span><span id="rpc_x_no_more_entries"></span>**RPC\_X\_NO\_MORE\_ENTRIES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-320">1772 (0x6EC)</span><span class="sxs-lookup"><span data-stu-id="2ee13-320">1772 (0x6EC)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-321">La liste des serveurs RPC disponibles pour la liaison des handles automatiques est épuisée.</span><span class="sxs-lookup"><span data-stu-id="2ee13-321">The list of RPC servers available for the binding of auto handles has been exhausted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-322"><span id="RPC_X_SS_CHAR_TRANS_OPEN_FAIL"></span><span id="rpc_x_ss_char_trans_open_fail"></span>**\_échec d' \_ \_ ouverture de \_ TRANS \_ . RPC X SS \_**</span><span class="sxs-lookup"><span data-stu-id="2ee13-322"><span id="RPC_X_SS_CHAR_TRANS_OPEN_FAIL"></span><span id="rpc_x_ss_char_trans_open_fail"></span>**RPC\_X\_SS\_CHAR\_TRANS\_OPEN\_FAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-323">1773 (0x6ED)</span><span class="sxs-lookup"><span data-stu-id="2ee13-323">1773 (0x6ED)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-324">Impossible d’ouvrir le fichier de table de traduction des caractères.</span><span class="sxs-lookup"><span data-stu-id="2ee13-324">Unable to open the character translation table file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-325"><span id="RPC_X_SS_CHAR_TRANS_SHORT_FILE"></span><span id="rpc_x_ss_char_trans_short_file"></span>**\_fichier de \_ \_ type \_ short de \_ transaction \_ RPC X SS**</span><span class="sxs-lookup"><span data-stu-id="2ee13-325"><span id="RPC_X_SS_CHAR_TRANS_SHORT_FILE"></span><span id="rpc_x_ss_char_trans_short_file"></span>**RPC\_X\_SS\_CHAR\_TRANS\_SHORT\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-326">1774 (0x6EE)</span><span class="sxs-lookup"><span data-stu-id="2ee13-326">1774 (0x6EE)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-327">Le fichier contenant la table de traduction de caractères a moins de 512 octets.</span><span class="sxs-lookup"><span data-stu-id="2ee13-327">The file containing the character translation table has fewer than 512 bytes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-328"><span id="RPC_X_SS_IN_NULL_CONTEXT"></span><span id="rpc_x_ss_in_null_context"></span>**RPC \_ X \_ SS \_ dans \_ le \_ contexte null**</span><span class="sxs-lookup"><span data-stu-id="2ee13-328"><span id="RPC_X_SS_IN_NULL_CONTEXT"></span><span id="rpc_x_ss_in_null_context"></span>**RPC\_X\_SS\_IN\_NULL\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-329">1775 (0x6EF)</span><span class="sxs-lookup"><span data-stu-id="2ee13-329">1775 (0x6EF)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-330">Un handle de contexte null a été passé du client à l’hôte pendant un appel de procédure distante.</span><span class="sxs-lookup"><span data-stu-id="2ee13-330">A null context handle was passed from the client to the host during a remote procedure call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-331"><span id="RPC_X_SS_CONTEXT_DAMAGED"></span><span id="rpc_x_ss_context_damaged"></span>**\_ \_ contexte SS RPC \_ X \_ endommagé**</span><span class="sxs-lookup"><span data-stu-id="2ee13-331"><span id="RPC_X_SS_CONTEXT_DAMAGED"></span><span id="rpc_x_ss_context_damaged"></span>**RPC\_X\_SS\_CONTEXT\_DAMAGED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-332">1777 (0x6F1)</span><span class="sxs-lookup"><span data-stu-id="2ee13-332">1777 (0x6F1)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-333">Le handle de contexte a changé pendant un appel de procédure distante.</span><span class="sxs-lookup"><span data-stu-id="2ee13-333">The context handle changed during a remote procedure call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-334"><span id="RPC_X_SS_HANDLES_MISMATCH"></span><span id="rpc_x_ss_handles_mismatch"></span>**non \_ - \_ \_ concordance des handles RPC X SS \_**</span><span class="sxs-lookup"><span data-stu-id="2ee13-334"><span id="RPC_X_SS_HANDLES_MISMATCH"></span><span id="rpc_x_ss_handles_mismatch"></span>**RPC\_X\_SS\_HANDLES\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-335">1778 (0x6F2)</span><span class="sxs-lookup"><span data-stu-id="2ee13-335">1778 (0x6F2)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-336">Les handles de liaison passés à un appel de procédure distante ne correspondent pas.</span><span class="sxs-lookup"><span data-stu-id="2ee13-336">The binding handles passed to a remote procedure call do not match.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-337"><span id="RPC_X_SS_CANNOT_GET_CALL_HANDLE"></span><span id="rpc_x_ss_cannot_get_call_handle"></span>**RPC \_ X \_ SS \_ ne peut pas \_ recevoir le \_ handle d’appel \_**</span><span class="sxs-lookup"><span data-stu-id="2ee13-337"><span id="RPC_X_SS_CANNOT_GET_CALL_HANDLE"></span><span id="rpc_x_ss_cannot_get_call_handle"></span>**RPC\_X\_SS\_CANNOT\_GET\_CALL\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-338">1779 (0x6F3)</span><span class="sxs-lookup"><span data-stu-id="2ee13-338">1779 (0x6F3)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-339">Le stub ne peut pas recevoir le descripteur d’appel de procédure distante.</span><span class="sxs-lookup"><span data-stu-id="2ee13-339">The stub is unable to get the remote procedure call handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-340"><span id="RPC_X_NULL_REF_POINTER"></span><span id="rpc_x_null_ref_pointer"></span>**\_ \_ \_ pointeur Ref null RPC \_ X**</span><span class="sxs-lookup"><span data-stu-id="2ee13-340"><span id="RPC_X_NULL_REF_POINTER"></span><span id="rpc_x_null_ref_pointer"></span>**RPC\_X\_NULL\_REF\_POINTER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-341">1780 (0x6F4)</span><span class="sxs-lookup"><span data-stu-id="2ee13-341">1780 (0x6F4)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-342">Un pointeur de référence null a été passé au stub.</span><span class="sxs-lookup"><span data-stu-id="2ee13-342">A null reference pointer was passed to the stub.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-343"><span id="RPC_X_ENUM_VALUE_OUT_OF_RANGE"></span><span id="rpc_x_enum_value_out_of_range"></span>**\_ \_ valeur enum RPC \_ X \_ hors \_ \_ limites**</span><span class="sxs-lookup"><span data-stu-id="2ee13-343"><span id="RPC_X_ENUM_VALUE_OUT_OF_RANGE"></span><span id="rpc_x_enum_value_out_of_range"></span>**RPC\_X\_ENUM\_VALUE\_OUT\_OF\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-344">1781 (0x6F5)</span><span class="sxs-lookup"><span data-stu-id="2ee13-344">1781 (0x6F5)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-345">La valeur d'énumération est hors limites.</span><span class="sxs-lookup"><span data-stu-id="2ee13-345">The enumeration value is out of range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-346"><span id="RPC_X_BYTE_COUNT_TOO_SMALL"></span><span id="rpc_x_byte_count_too_small"></span>**le \_ nombre d’octets RPC X est \_ \_ \_ trop \_ petit**</span><span class="sxs-lookup"><span data-stu-id="2ee13-346"><span id="RPC_X_BYTE_COUNT_TOO_SMALL"></span><span id="rpc_x_byte_count_too_small"></span>**RPC\_X\_BYTE\_COUNT\_TOO\_SMALL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-347">1782 (0x6F6)</span><span class="sxs-lookup"><span data-stu-id="2ee13-347">1782 (0x6F6)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-348">Le nombre d’octets est trop petit.</span><span class="sxs-lookup"><span data-stu-id="2ee13-348">The byte count is too small.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-349"><span id="RPC_X_BAD_STUB_DATA"></span><span id="rpc_x_bad_stub_data"></span>**RPC \_ X \_ \_ données de stub incorrectes \_**</span><span class="sxs-lookup"><span data-stu-id="2ee13-349"><span id="RPC_X_BAD_STUB_DATA"></span><span id="rpc_x_bad_stub_data"></span>**RPC\_X\_BAD\_STUB\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-350">1783 (0x6F7)</span><span class="sxs-lookup"><span data-stu-id="2ee13-350">1783 (0x6F7)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-351">Le stub a reçu des données incorrectes.</span><span class="sxs-lookup"><span data-stu-id="2ee13-351">The stub received bad data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-352"><span id="ERROR_INVALID_USER_BUFFER"></span><span id="error_invalid_user_buffer"></span>**ERREUR \_ de \_ mémoire tampon utilisateur non valide \_**</span><span class="sxs-lookup"><span data-stu-id="2ee13-352"><span id="ERROR_INVALID_USER_BUFFER"></span><span id="error_invalid_user_buffer"></span>**ERROR\_INVALID\_USER\_BUFFER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-353">1784 (0x6F8)</span><span class="sxs-lookup"><span data-stu-id="2ee13-353">1784 (0x6F8)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-354">La mémoire tampon de l’utilisateur fournie n’est pas valide pour l’opération demandée.</span><span class="sxs-lookup"><span data-stu-id="2ee13-354">The supplied user buffer is not valid for the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-355"><span id="ERROR_UNRECOGNIZED_MEDIA"></span><span id="error_unrecognized_media"></span>**ERREUR de \_ média non reconnu \_**</span><span class="sxs-lookup"><span data-stu-id="2ee13-355"><span id="ERROR_UNRECOGNIZED_MEDIA"></span><span id="error_unrecognized_media"></span>**ERROR\_UNRECOGNIZED\_MEDIA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-356">1785 (0x6F9)</span><span class="sxs-lookup"><span data-stu-id="2ee13-356">1785 (0x6F9)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-357">Le support de disque n’est pas reconnu.</span><span class="sxs-lookup"><span data-stu-id="2ee13-357">The disk media is not recognized.</span></span> <span data-ttu-id="2ee13-358">Elle n’est peut-être pas mise en forme.</span><span class="sxs-lookup"><span data-stu-id="2ee13-358">It may not be formatted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-359"><span id="ERROR_NO_TRUST_LSA_SECRET"></span><span id="error_no_trust_lsa_secret"></span>**ERREUR de \_ non- \_ \_ \_ secret LSA secret**</span><span class="sxs-lookup"><span data-stu-id="2ee13-359"><span id="ERROR_NO_TRUST_LSA_SECRET"></span><span id="error_no_trust_lsa_secret"></span>**ERROR\_NO\_TRUST\_LSA\_SECRET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-360">1786 (0x6FA)</span><span class="sxs-lookup"><span data-stu-id="2ee13-360">1786 (0x6FA)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-361">La station de travail n’a pas de secret de confiance.</span><span class="sxs-lookup"><span data-stu-id="2ee13-361">The workstation does not have a trust secret.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-362"><span id="ERROR_NO_TRUST_SAM_ACCOUNT"></span><span id="error_no_trust_sam_account"></span>**ERREUR \_ aucun \_ \_ compte Sam d’approbation \_**</span><span class="sxs-lookup"><span data-stu-id="2ee13-362"><span id="ERROR_NO_TRUST_SAM_ACCOUNT"></span><span id="error_no_trust_sam_account"></span>**ERROR\_NO\_TRUST\_SAM\_ACCOUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-363">1787 (0x6FB)</span><span class="sxs-lookup"><span data-stu-id="2ee13-363">1787 (0x6FB)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-364">La base de données de sécurité sur le serveur ne dispose pas d’un compte d’ordinateur pour cette relation d’approbation de station de travail.</span><span class="sxs-lookup"><span data-stu-id="2ee13-364">The security database on the server does not have a computer account for this workstation trust relationship.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-365"><span id="ERROR_TRUSTED_DOMAIN_FAILURE"></span><span id="error_trusted_domain_failure"></span>**erreur \_ de \_ domaine approuvé d’erreur \_**</span><span class="sxs-lookup"><span data-stu-id="2ee13-365"><span id="ERROR_TRUSTED_DOMAIN_FAILURE"></span><span id="error_trusted_domain_failure"></span>**ERROR\_TRUSTED\_DOMAIN\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-366">1788 (0x6FC)</span><span class="sxs-lookup"><span data-stu-id="2ee13-366">1788 (0x6FC)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-367">La relation d’approbation entre le domaine principal et le domaine approuvé a échoué.</span><span class="sxs-lookup"><span data-stu-id="2ee13-367">The trust relationship between the primary domain and the trusted domain failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-368"><span id="ERROR_TRUSTED_RELATIONSHIP_FAILURE"></span><span id="error_trusted_relationship_failure"></span>**échec de la \_ relation approuvée d’erreur \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2ee13-368"><span id="ERROR_TRUSTED_RELATIONSHIP_FAILURE"></span><span id="error_trusted_relationship_failure"></span>**ERROR\_TRUSTED\_RELATIONSHIP\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-369">1789 (0x6FD)</span><span class="sxs-lookup"><span data-stu-id="2ee13-369">1789 (0x6FD)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-370">La relation d'approbation entre cette station de travail et le domaine principal a échoué.</span><span class="sxs-lookup"><span data-stu-id="2ee13-370">The trust relationship between this workstation and the primary domain failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-371"><span id="ERROR_TRUST_FAILURE"></span><span id="error_trust_failure"></span>**échec de l’approbation d’erreur \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2ee13-371"><span id="ERROR_TRUST_FAILURE"></span><span id="error_trust_failure"></span>**ERROR\_TRUST\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-372">1790 (0x6FE)</span><span class="sxs-lookup"><span data-stu-id="2ee13-372">1790 (0x6FE)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-373">Échec de l’ouverture de session réseau.</span><span class="sxs-lookup"><span data-stu-id="2ee13-373">The network logon failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-374"><span id="RPC_S_CALL_IN_PROGRESS"></span><span id="rpc_s_call_in_progress"></span>**\_appel RPC \_ S \_ en \_ cours**</span><span class="sxs-lookup"><span data-stu-id="2ee13-374"><span id="RPC_S_CALL_IN_PROGRESS"></span><span id="rpc_s_call_in_progress"></span>**RPC\_S\_CALL\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-375">1791 (0x6FF)</span><span class="sxs-lookup"><span data-stu-id="2ee13-375">1791 (0x6FF)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-376">Un appel de procédure distante est déjà en cours pour ce thread.</span><span class="sxs-lookup"><span data-stu-id="2ee13-376">A remote procedure call is already in progress for this thread.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-377"><span id="ERROR_NETLOGON_NOT_STARTED"></span><span id="error_netlogon_not_started"></span>**ERREUR \_ Netlogon \_ non \_ démarrée**</span><span class="sxs-lookup"><span data-stu-id="2ee13-377"><span id="ERROR_NETLOGON_NOT_STARTED"></span><span id="error_netlogon_not_started"></span>**ERROR\_NETLOGON\_NOT\_STARTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-378">1792 (0X700)</span><span class="sxs-lookup"><span data-stu-id="2ee13-378">1792 (0x700)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-379">Une tentative de connexion a été effectuée, mais le service d’ouverture de session réseau n’a pas été démarré.</span><span class="sxs-lookup"><span data-stu-id="2ee13-379">An attempt was made to logon, but the network logon service was not started.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-380"><span id="ERROR_ACCOUNT_EXPIRED"></span><span id="error_account_expired"></span>**compte d’erreur \_ \_ expiré**</span><span class="sxs-lookup"><span data-stu-id="2ee13-380"><span id="ERROR_ACCOUNT_EXPIRED"></span><span id="error_account_expired"></span>**ERROR\_ACCOUNT\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-381">1793 (0x701)</span><span class="sxs-lookup"><span data-stu-id="2ee13-381">1793 (0x701)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-382">Le compte de l’utilisateur a expiré.</span><span class="sxs-lookup"><span data-stu-id="2ee13-382">The user's account has expired.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-383"><span id="ERROR_REDIRECTOR_HAS_OPEN_HANDLES"></span><span id="error_redirector_has_open_handles"></span>**le \_ REdirecteur d’erreurs \_ a des \_ \_ Handles ouverts**</span><span class="sxs-lookup"><span data-stu-id="2ee13-383"><span id="ERROR_REDIRECTOR_HAS_OPEN_HANDLES"></span><span id="error_redirector_has_open_handles"></span>**ERROR\_REDIRECTOR\_HAS\_OPEN\_HANDLES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-384">1794 (0x702)</span><span class="sxs-lookup"><span data-stu-id="2ee13-384">1794 (0x702)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-385">Le redirecteur est en cours d’utilisation et ne peut pas être déchargé.</span><span class="sxs-lookup"><span data-stu-id="2ee13-385">The redirector is in use and cannot be unloaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-386"><span id="ERROR_PRINTER_DRIVER_ALREADY_INSTALLED"></span><span id="error_printer_driver_already_installed"></span>**ERREUR le \_ pilote d’imprimante est \_ \_ déjà \_ installé**</span><span class="sxs-lookup"><span data-stu-id="2ee13-386"><span id="ERROR_PRINTER_DRIVER_ALREADY_INSTALLED"></span><span id="error_printer_driver_already_installed"></span>**ERROR\_PRINTER\_DRIVER\_ALREADY\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-387">1795 (0x703)</span><span class="sxs-lookup"><span data-stu-id="2ee13-387">1795 (0x703)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-388">Le pilote d’imprimante spécifié est déjà installé.</span><span class="sxs-lookup"><span data-stu-id="2ee13-388">The specified printer driver is already installed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-389"><span id="ERROR_UNKNOWN_PORT"></span><span id="error_unknown_port"></span>**ERREUR \_ \_ port inconnu**</span><span class="sxs-lookup"><span data-stu-id="2ee13-389"><span id="ERROR_UNKNOWN_PORT"></span><span id="error_unknown_port"></span>**ERROR\_UNKNOWN\_PORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-390">1796 (0x704)</span><span class="sxs-lookup"><span data-stu-id="2ee13-390">1796 (0x704)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-391">Le port spécifié est inconnu.</span><span class="sxs-lookup"><span data-stu-id="2ee13-391">The specified port is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-392"><span id="ERROR_UNKNOWN_PRINTER_DRIVER"></span><span id="error_unknown_printer_driver"></span>**ERREUR \_ de \_ pilote d’imprimante inconnu \_**</span><span class="sxs-lookup"><span data-stu-id="2ee13-392"><span id="ERROR_UNKNOWN_PRINTER_DRIVER"></span><span id="error_unknown_printer_driver"></span>**ERROR\_UNKNOWN\_PRINTER\_DRIVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-393">1797 (0x705)</span><span class="sxs-lookup"><span data-stu-id="2ee13-393">1797 (0x705)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-394">Le pilote d’imprimante est inconnu.</span><span class="sxs-lookup"><span data-stu-id="2ee13-394">The printer driver is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-395"><span id="ERROR_UNKNOWN_PRINTPROCESSOR"></span><span id="error_unknown_printprocessor"></span>**ERREUR \_ inconnue \_ PRINTPROCESSOR**</span><span class="sxs-lookup"><span data-stu-id="2ee13-395"><span id="ERROR_UNKNOWN_PRINTPROCESSOR"></span><span id="error_unknown_printprocessor"></span>**ERROR\_UNKNOWN\_PRINTPROCESSOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-396">1798 (0x706)</span><span class="sxs-lookup"><span data-stu-id="2ee13-396">1798 (0x706)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-397">Le processeur d’impression est inconnu.</span><span class="sxs-lookup"><span data-stu-id="2ee13-397">The print processor is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-398"><span id="ERROR_INVALID_SEPARATOR_FILE"></span><span id="error_invalid_separator_file"></span>**ERREUR \_ \_ fichier séparateur non valide \_**</span><span class="sxs-lookup"><span data-stu-id="2ee13-398"><span id="ERROR_INVALID_SEPARATOR_FILE"></span><span id="error_invalid_separator_file"></span>**ERROR\_INVALID\_SEPARATOR\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-399">1799 (0x707)</span><span class="sxs-lookup"><span data-stu-id="2ee13-399">1799 (0x707)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-400">Le fichier séparateur spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="2ee13-400">The specified separator file is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-401"><span id="ERROR_INVALID_PRIORITY"></span><span id="error_invalid_priority"></span>**priorité d’erreur \_ non valide \_**</span><span class="sxs-lookup"><span data-stu-id="2ee13-401"><span id="ERROR_INVALID_PRIORITY"></span><span id="error_invalid_priority"></span>**ERROR\_INVALID\_PRIORITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-402">1800 (0x708)</span><span class="sxs-lookup"><span data-stu-id="2ee13-402">1800 (0x708)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-403">La priorité spécifiée n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="2ee13-403">The specified priority is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-404"><span id="ERROR_INVALID_PRINTER_NAME"></span><span id="error_invalid_printer_name"></span>**ERREUR \_ de \_ nom d’imprimante non valide \_**</span><span class="sxs-lookup"><span data-stu-id="2ee13-404"><span id="ERROR_INVALID_PRINTER_NAME"></span><span id="error_invalid_printer_name"></span>**ERROR\_INVALID\_PRINTER\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-405">1801 (0x709)</span><span class="sxs-lookup"><span data-stu-id="2ee13-405">1801 (0x709)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-406">Le nom de l’imprimante n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="2ee13-406">The printer name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-407"><span id="ERROR_PRINTER_ALREADY_EXISTS"></span><span id="error_printer_already_exists"></span>**une erreur d' \_ imprimante \_ \_ existe déjà**</span><span class="sxs-lookup"><span data-stu-id="2ee13-407"><span id="ERROR_PRINTER_ALREADY_EXISTS"></span><span id="error_printer_already_exists"></span>**ERROR\_PRINTER\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-408">1802 (0x70A)</span><span class="sxs-lookup"><span data-stu-id="2ee13-408">1802 (0x70A)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-409">L’imprimante existe déjà.</span><span class="sxs-lookup"><span data-stu-id="2ee13-409">The printer already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-410"><span id="ERROR_INVALID_PRINTER_COMMAND"></span><span id="error_invalid_printer_command"></span>**ERREUR \_ de \_ commande d’imprimante non valide \_**</span><span class="sxs-lookup"><span data-stu-id="2ee13-410"><span id="ERROR_INVALID_PRINTER_COMMAND"></span><span id="error_invalid_printer_command"></span>**ERROR\_INVALID\_PRINTER\_COMMAND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-411">1803 (0x70B)</span><span class="sxs-lookup"><span data-stu-id="2ee13-411">1803 (0x70B)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-412">La commande d’imprimante n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="2ee13-412">The printer command is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-413"><span id="ERROR_INVALID_DATATYPE"></span><span id="error_invalid_datatype"></span>**ERREUR \_ de \_ type de données non valide**</span><span class="sxs-lookup"><span data-stu-id="2ee13-413"><span id="ERROR_INVALID_DATATYPE"></span><span id="error_invalid_datatype"></span>**ERROR\_INVALID\_DATATYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-414">1804 (0x70C)</span><span class="sxs-lookup"><span data-stu-id="2ee13-414">1804 (0x70C)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-415">Le type de données spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="2ee13-415">The specified datatype is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-416"><span id="ERROR_INVALID_ENVIRONMENT"></span><span id="error_invalid_environment"></span>**ERREUR \_ d' \_ environnement non valide**</span><span class="sxs-lookup"><span data-stu-id="2ee13-416"><span id="ERROR_INVALID_ENVIRONMENT"></span><span id="error_invalid_environment"></span>**ERROR\_INVALID\_ENVIRONMENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-417">1805 (0x70D)</span><span class="sxs-lookup"><span data-stu-id="2ee13-417">1805 (0x70D)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-418">L’environnement spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="2ee13-418">The environment specified is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-419"><span id="RPC_S_NO_MORE_BINDINGS"></span><span id="rpc_s_no_more_bindings"></span>**RPC \_ \_ ne pas \_ plus de \_ liaisons**</span><span class="sxs-lookup"><span data-stu-id="2ee13-419"><span id="RPC_S_NO_MORE_BINDINGS"></span><span id="rpc_s_no_more_bindings"></span>**RPC\_S\_NO\_MORE\_BINDINGS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-420">1806 (0x70E)</span><span class="sxs-lookup"><span data-stu-id="2ee13-420">1806 (0x70E)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-421">Il n’y a plus de liaisons.</span><span class="sxs-lookup"><span data-stu-id="2ee13-421">There are no more bindings.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-422"><span id="ERROR_NOLOGON_INTERDOMAIN_TRUST_ACCOUNT"></span><span id="error_nologon_interdomain_trust_account"></span>**ERREUR \_ NOlogo- \_ compte de \_ confiance interdomaine \_**</span><span class="sxs-lookup"><span data-stu-id="2ee13-422"><span id="ERROR_NOLOGON_INTERDOMAIN_TRUST_ACCOUNT"></span><span id="error_nologon_interdomain_trust_account"></span>**ERROR\_NOLOGON\_INTERDOMAIN\_TRUST\_ACCOUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-423">1807 (0x70F)</span><span class="sxs-lookup"><span data-stu-id="2ee13-423">1807 (0x70F)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-424">Le compte utilisé est un compte de confiance interdomaine.</span><span class="sxs-lookup"><span data-stu-id="2ee13-424">The account used is an interdomain trust account.</span></span> <span data-ttu-id="2ee13-425">Utilisez votre compte d’utilisateur global ou votre compte d’utilisateur local pour accéder à ce serveur.</span><span class="sxs-lookup"><span data-stu-id="2ee13-425">Use your global user account or local user account to access this server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-426"><span id="ERROR_NOLOGON_WORKSTATION_TRUST_ACCOUNT"></span><span id="error_nologon_workstation_trust_account"></span>**ERREUR \_ NOlogos \_ \_ compte de confiance de station de travail \_**</span><span class="sxs-lookup"><span data-stu-id="2ee13-426"><span id="ERROR_NOLOGON_WORKSTATION_TRUST_ACCOUNT"></span><span id="error_nologon_workstation_trust_account"></span>**ERROR\_NOLOGON\_WORKSTATION\_TRUST\_ACCOUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-427">1808 (0x710)</span><span class="sxs-lookup"><span data-stu-id="2ee13-427">1808 (0x710)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-428">Le compte utilisé est un compte d’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="2ee13-428">The account used is a computer account.</span></span> <span data-ttu-id="2ee13-429">Utilisez votre compte d’utilisateur global ou votre compte d’utilisateur local pour accéder à ce serveur.</span><span class="sxs-lookup"><span data-stu-id="2ee13-429">Use your global user account or local user account to access this server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-430"><span id="ERROR_NOLOGON_SERVER_TRUST_ACCOUNT"></span><span id="error_nologon_server_trust_account"></span>**ERREUR \_ NOlogos \_ \_ compte de confiance du serveur \_**</span><span class="sxs-lookup"><span data-stu-id="2ee13-430"><span id="ERROR_NOLOGON_SERVER_TRUST_ACCOUNT"></span><span id="error_nologon_server_trust_account"></span>**ERROR\_NOLOGON\_SERVER\_TRUST\_ACCOUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-431">1809 (0x711)</span><span class="sxs-lookup"><span data-stu-id="2ee13-431">1809 (0x711)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-432">Le compte utilisé est un compte de confiance de serveur.</span><span class="sxs-lookup"><span data-stu-id="2ee13-432">The account used is a server trust account.</span></span> <span data-ttu-id="2ee13-433">Utilisez votre compte d’utilisateur global ou votre compte d’utilisateur local pour accéder à ce serveur.</span><span class="sxs-lookup"><span data-stu-id="2ee13-433">Use your global user account or local user account to access this server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-434"><span id="ERROR_DOMAIN_TRUST_INCONSISTENT"></span><span id="error_domain_trust_inconsistent"></span>**approbation de domaine d’erreur \_ \_ \_ incohérente**</span><span class="sxs-lookup"><span data-stu-id="2ee13-434"><span id="ERROR_DOMAIN_TRUST_INCONSISTENT"></span><span id="error_domain_trust_inconsistent"></span>**ERROR\_DOMAIN\_TRUST\_INCONSISTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-435">1810 (0x712)</span><span class="sxs-lookup"><span data-stu-id="2ee13-435">1810 (0x712)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-436">Le nom ou l’ID de sécurité (SID) du domaine spécifié est incohérent avec les informations d’approbation pour ce domaine.</span><span class="sxs-lookup"><span data-stu-id="2ee13-436">The name or security ID (SID) of the domain specified is inconsistent with the trust information for that domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-437"><span id="ERROR_SERVER_HAS_OPEN_HANDLES"></span><span id="error_server_has_open_handles"></span>**le \_ serveur d’erreurs \_ a des \_ \_ Handles ouverts**</span><span class="sxs-lookup"><span data-stu-id="2ee13-437"><span id="ERROR_SERVER_HAS_OPEN_HANDLES"></span><span id="error_server_has_open_handles"></span>**ERROR\_SERVER\_HAS\_OPEN\_HANDLES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-438">1811 (0x713)</span><span class="sxs-lookup"><span data-stu-id="2ee13-438">1811 (0x713)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-439">Le serveur est en cours d’utilisation et ne peut pas être déchargé.</span><span class="sxs-lookup"><span data-stu-id="2ee13-439">The server is in use and cannot be unloaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-440"><span id="ERROR_RESOURCE_DATA_NOT_FOUND"></span><span id="error_resource_data_not_found"></span>**données de ressource d’erreur \_ \_ \_ \_ introuvables**</span><span class="sxs-lookup"><span data-stu-id="2ee13-440"><span id="ERROR_RESOURCE_DATA_NOT_FOUND"></span><span id="error_resource_data_not_found"></span>**ERROR\_RESOURCE\_DATA\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-441">1812 (0x714)</span><span class="sxs-lookup"><span data-stu-id="2ee13-441">1812 (0x714)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-442">Le fichier image spécifié ne contenait pas de section de ressource.</span><span class="sxs-lookup"><span data-stu-id="2ee13-442">The specified image file did not contain a resource section.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-443"><span id="ERROR_RESOURCE_TYPE_NOT_FOUND"></span><span id="error_resource_type_not_found"></span>**TYPE de ressource d’erreur \_ \_ \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="2ee13-443"><span id="ERROR_RESOURCE_TYPE_NOT_FOUND"></span><span id="error_resource_type_not_found"></span>**ERROR\_RESOURCE\_TYPE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-444">1813 (0x715)</span><span class="sxs-lookup"><span data-stu-id="2ee13-444">1813 (0x715)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-445">Le type de ressource spécifié est introuvable dans le fichier image.</span><span class="sxs-lookup"><span data-stu-id="2ee13-445">The specified resource type cannot be found in the image file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-446"><span id="ERROR_RESOURCE_NAME_NOT_FOUND"></span><span id="error_resource_name_not_found"></span>**ERREUR \_ de \_ nom de ressource \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="2ee13-446"><span id="ERROR_RESOURCE_NAME_NOT_FOUND"></span><span id="error_resource_name_not_found"></span>**ERROR\_RESOURCE\_NAME\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-447">1814 (0x716)</span><span class="sxs-lookup"><span data-stu-id="2ee13-447">1814 (0x716)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-448">Le nom de ressource spécifié est introuvable dans le fichier image.</span><span class="sxs-lookup"><span data-stu-id="2ee13-448">The specified resource name cannot be found in the image file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-449"><span id="ERROR_RESOURCE_LANG_NOT_FOUND"></span><span id="error_resource_lang_not_found"></span>**ERREUR \_ de \_ ressource \_ lang \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="2ee13-449"><span id="ERROR_RESOURCE_LANG_NOT_FOUND"></span><span id="error_resource_lang_not_found"></span>**ERROR\_RESOURCE\_LANG\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-450">1815 (0x717)</span><span class="sxs-lookup"><span data-stu-id="2ee13-450">1815 (0x717)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-451">L’ID de langue de ressource spécifié est introuvable dans le fichier image.</span><span class="sxs-lookup"><span data-stu-id="2ee13-451">The specified resource language ID cannot be found in the image file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-452"><span id="ERROR_NOT_ENOUGH_QUOTA"></span><span id="error_not_enough_quota"></span>**QUOTA d’erreur \_ \_ insuffisante \_**</span><span class="sxs-lookup"><span data-stu-id="2ee13-452"><span id="ERROR_NOT_ENOUGH_QUOTA"></span><span id="error_not_enough_quota"></span>**ERROR\_NOT\_ENOUGH\_QUOTA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-453">1816 (0x718)</span><span class="sxs-lookup"><span data-stu-id="2ee13-453">1816 (0x718)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-454">Quota insuffisant pour traiter cette commande.</span><span class="sxs-lookup"><span data-stu-id="2ee13-454">Not enough quota is available to process this command.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-455"><span id="RPC_S_NO_INTERFACES"></span><span id="rpc_s_no_interfaces"></span>**\_interfaces RPC \_ sans \_ interface**</span><span class="sxs-lookup"><span data-stu-id="2ee13-455"><span id="RPC_S_NO_INTERFACES"></span><span id="rpc_s_no_interfaces"></span>**RPC\_S\_NO\_INTERFACES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-456">1817 (0x719)</span><span class="sxs-lookup"><span data-stu-id="2ee13-456">1817 (0x719)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-457">Aucune interface n’a été inscrite.</span><span class="sxs-lookup"><span data-stu-id="2ee13-457">No interfaces have been registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-458"><span id="RPC_S_CALL_CANCELLED"></span><span id="rpc_s_call_cancelled"></span>**\_appel RPC \_ S \_ annulé**</span><span class="sxs-lookup"><span data-stu-id="2ee13-458"><span id="RPC_S_CALL_CANCELLED"></span><span id="rpc_s_call_cancelled"></span>**RPC\_S\_CALL\_CANCELLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-459">1818 (0x71A)</span><span class="sxs-lookup"><span data-stu-id="2ee13-459">1818 (0x71A)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-460">L’appel de procédure distante a été annulé.</span><span class="sxs-lookup"><span data-stu-id="2ee13-460">The remote procedure call was cancelled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-461"><span id="RPC_S_BINDING_INCOMPLETE"></span><span id="rpc_s_binding_incomplete"></span>**\_liaison RPC \_ S \_ incomplète**</span><span class="sxs-lookup"><span data-stu-id="2ee13-461"><span id="RPC_S_BINDING_INCOMPLETE"></span><span id="rpc_s_binding_incomplete"></span>**RPC\_S\_BINDING\_INCOMPLETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-462">1819 (0x71B)</span><span class="sxs-lookup"><span data-stu-id="2ee13-462">1819 (0x71B)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-463">Le handle de liaison ne contient pas toutes les informations requises.</span><span class="sxs-lookup"><span data-stu-id="2ee13-463">The binding handle does not contain all required information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-464"><span id="RPC_S_COMM_FAILURE"></span><span id="rpc_s_comm_failure"></span>**\_échec de \_ communication RPC S \_**</span><span class="sxs-lookup"><span data-stu-id="2ee13-464"><span id="RPC_S_COMM_FAILURE"></span><span id="rpc_s_comm_failure"></span>**RPC\_S\_COMM\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-465">1820 (0x71C)</span><span class="sxs-lookup"><span data-stu-id="2ee13-465">1820 (0x71C)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-466">Un échec de communication s’est produit lors d’un appel de procédure distante.</span><span class="sxs-lookup"><span data-stu-id="2ee13-466">A communications failure occurred during a remote procedure call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-467"><span id="RPC_S_UNSUPPORTED_AUTHN_LEVEL"></span><span id="rpc_s_unsupported_authn_level"></span>**RPC \_ S \_ niveau non pris en charge par \_ Authn \_**</span><span class="sxs-lookup"><span data-stu-id="2ee13-467"><span id="RPC_S_UNSUPPORTED_AUTHN_LEVEL"></span><span id="rpc_s_unsupported_authn_level"></span>**RPC\_S\_UNSUPPORTED\_AUTHN\_LEVEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-468">1821 (0x71D)</span><span class="sxs-lookup"><span data-stu-id="2ee13-468">1821 (0x71D)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-469">Le niveau d’authentification demandé n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="2ee13-469">The requested authentication level is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-470"><span id="RPC_S_NO_PRINC_NAME"></span><span id="rpc_s_no_princ_name"></span>**RPC \_ \_ n’a pas de \_ nom de princ \_**</span><span class="sxs-lookup"><span data-stu-id="2ee13-470"><span id="RPC_S_NO_PRINC_NAME"></span><span id="rpc_s_no_princ_name"></span>**RPC\_S\_NO\_PRINC\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-471">1822 (0x71E)</span><span class="sxs-lookup"><span data-stu-id="2ee13-471">1822 (0x71E)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-472">Aucun nom principal n’est inscrit.</span><span class="sxs-lookup"><span data-stu-id="2ee13-472">No principal name registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-473"><span id="RPC_S_NOT_RPC_ERROR"></span><span id="rpc_s_not_rpc_error"></span>**RPC \_ S \_ non \_ \_ erreur RPC**</span><span class="sxs-lookup"><span data-stu-id="2ee13-473"><span id="RPC_S_NOT_RPC_ERROR"></span><span id="rpc_s_not_rpc_error"></span>**RPC\_S\_NOT\_RPC\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-474">1823 (0x71F)</span><span class="sxs-lookup"><span data-stu-id="2ee13-474">1823 (0x71F)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-475">L’erreur spécifiée n’est pas un code d’erreur RPC Windows valide.</span><span class="sxs-lookup"><span data-stu-id="2ee13-475">The error specified is not a valid Windows RPC error code.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-476"><span id="RPC_S_UUID_LOCAL_ONLY"></span><span id="rpc_s_uuid_local_only"></span>**\_UUID RPC \_ \_ uniquement local \_**</span><span class="sxs-lookup"><span data-stu-id="2ee13-476"><span id="RPC_S_UUID_LOCAL_ONLY"></span><span id="rpc_s_uuid_local_only"></span>**RPC\_S\_UUID\_LOCAL\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-477">1824 (0x720)</span><span class="sxs-lookup"><span data-stu-id="2ee13-477">1824 (0x720)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-478">Un UUID qui est valide uniquement sur cet ordinateur a été alloué.</span><span class="sxs-lookup"><span data-stu-id="2ee13-478">A UUID that is valid only on this computer has been allocated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-479"><span id="RPC_S_SEC_PKG_ERROR"></span><span id="rpc_s_sec_pkg_error"></span>**erreur du s de la \_ \_ seconde RPC \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2ee13-479"><span id="RPC_S_SEC_PKG_ERROR"></span><span id="rpc_s_sec_pkg_error"></span>**RPC\_S\_SEC\_PKG\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-480">1825 (0x721)</span><span class="sxs-lookup"><span data-stu-id="2ee13-480">1825 (0x721)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-481">Une erreur spécifique au package de sécurité s’est produite.</span><span class="sxs-lookup"><span data-stu-id="2ee13-481">A security package specific error occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-482"><span id="RPC_S_NOT_CANCELLED"></span><span id="rpc_s_not_cancelled"></span>**RPC \_ S \_ non \_ annulés**</span><span class="sxs-lookup"><span data-stu-id="2ee13-482"><span id="RPC_S_NOT_CANCELLED"></span><span id="rpc_s_not_cancelled"></span>**RPC\_S\_NOT\_CANCELLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-483">1826 (0x722)</span><span class="sxs-lookup"><span data-stu-id="2ee13-483">1826 (0x722)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-484">Le thread n’est pas annulé.</span><span class="sxs-lookup"><span data-stu-id="2ee13-484">Thread is not canceled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-485"><span id="RPC_X_INVALID_ES_ACTION"></span><span id="rpc_x_invalid_es_action"></span>**\_ \_ action es non valides RPC X \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2ee13-485"><span id="RPC_X_INVALID_ES_ACTION"></span><span id="rpc_x_invalid_es_action"></span>**RPC\_X\_INVALID\_ES\_ACTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-486">1827 (0x723)</span><span class="sxs-lookup"><span data-stu-id="2ee13-486">1827 (0x723)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-487">Opération non valide sur le handle d’encodage/décodage.</span><span class="sxs-lookup"><span data-stu-id="2ee13-487">Invalid operation on the encoding/decoding handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-488"><span id="RPC_X_WRONG_ES_VERSION"></span><span id="rpc_x_wrong_es_version"></span>**RPC \_ X \_ mauvaise \_ \_ version es**</span><span class="sxs-lookup"><span data-stu-id="2ee13-488"><span id="RPC_X_WRONG_ES_VERSION"></span><span id="rpc_x_wrong_es_version"></span>**RPC\_X\_WRONG\_ES\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-489">1828 (0x724)</span><span class="sxs-lookup"><span data-stu-id="2ee13-489">1828 (0x724)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-490">Version incompatible du package de sérialisation.</span><span class="sxs-lookup"><span data-stu-id="2ee13-490">Incompatible version of the serializing package.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-491"><span id="RPC_X_WRONG_STUB_VERSION"></span><span id="rpc_x_wrong_stub_version"></span>**\_version de stub RPC X \_ incorrecte \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2ee13-491"><span id="RPC_X_WRONG_STUB_VERSION"></span><span id="rpc_x_wrong_stub_version"></span>**RPC\_X\_WRONG\_STUB\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-492">1829 (0x725)</span><span class="sxs-lookup"><span data-stu-id="2ee13-492">1829 (0x725)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-493">Version incompatible du stub RPC.</span><span class="sxs-lookup"><span data-stu-id="2ee13-493">Incompatible version of the RPC stub.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-494"><span id="RPC_X_INVALID_PIPE_OBJECT"></span><span id="rpc_x_invalid_pipe_object"></span>**\_ \_ objet canal non valide RPC X \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2ee13-494"><span id="RPC_X_INVALID_PIPE_OBJECT"></span><span id="rpc_x_invalid_pipe_object"></span>**RPC\_X\_INVALID\_PIPE\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-495">1830 (0x726)</span><span class="sxs-lookup"><span data-stu-id="2ee13-495">1830 (0x726)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-496">L’objet du canal RPC n’est pas valide ou est endommagé.</span><span class="sxs-lookup"><span data-stu-id="2ee13-496">The RPC pipe object is invalid or corrupted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-497"><span id="RPC_X_WRONG_PIPE_ORDER"></span><span id="rpc_x_wrong_pipe_order"></span>**\_ \_ mauvais ordre des \_ canaux RPC X \_**</span><span class="sxs-lookup"><span data-stu-id="2ee13-497"><span id="RPC_X_WRONG_PIPE_ORDER"></span><span id="rpc_x_wrong_pipe_order"></span>**RPC\_X\_WRONG\_PIPE\_ORDER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-498">1831 (0x727)</span><span class="sxs-lookup"><span data-stu-id="2ee13-498">1831 (0x727)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-499">Une opération non valide a été tentée sur un objet canal RPC.</span><span class="sxs-lookup"><span data-stu-id="2ee13-499">An invalid operation was attempted on an RPC pipe object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-500"><span id="RPC_X_WRONG_PIPE_VERSION"></span><span id="rpc_x_wrong_pipe_version"></span>**\_version du canal RPC X \_ incorrect \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2ee13-500"><span id="RPC_X_WRONG_PIPE_VERSION"></span><span id="rpc_x_wrong_pipe_version"></span>**RPC\_X\_WRONG\_PIPE\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-501">1832 (0x728)</span><span class="sxs-lookup"><span data-stu-id="2ee13-501">1832 (0x728)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-502">Version du canal RPC non prise en charge.</span><span class="sxs-lookup"><span data-stu-id="2ee13-502">Unsupported RPC pipe version.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-503"><span id="RPC_S_COOKIE_AUTH_FAILED"></span><span id="rpc_s_cookie_auth_failed"></span>**échec de l’authentification des cookies RPC \_ S \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2ee13-503"><span id="RPC_S_COOKIE_AUTH_FAILED"></span><span id="rpc_s_cookie_auth_failed"></span>**RPC\_S\_COOKIE\_AUTH\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-504">1833 (0x729)</span><span class="sxs-lookup"><span data-stu-id="2ee13-504">1833 (0x729)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-505">Le serveur proxy HTTP a rejeté la connexion en raison de l’échec de l’authentification du cookie.</span><span class="sxs-lookup"><span data-stu-id="2ee13-505">HTTP proxy server rejected the connection because the cookie authentication failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-506"><span id="RPC_S_GROUP_MEMBER_NOT_FOUND"></span><span id="rpc_s_group_member_not_found"></span>**\_membre du groupe RPC S \_ \_ \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="2ee13-506"><span id="RPC_S_GROUP_MEMBER_NOT_FOUND"></span><span id="rpc_s_group_member_not_found"></span>**RPC\_S\_GROUP\_MEMBER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-507">1898 (0x76A)</span><span class="sxs-lookup"><span data-stu-id="2ee13-507">1898 (0x76A)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-508">Le membre du groupe est introuvable.</span><span class="sxs-lookup"><span data-stu-id="2ee13-508">The group member was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-509"><span id="EPT_S_CANT_CREATE"></span><span id="ept_s_cant_create"></span>**EPT \_ S \_ impossible à \_ créer**</span><span class="sxs-lookup"><span data-stu-id="2ee13-509"><span id="EPT_S_CANT_CREATE"></span><span id="ept_s_cant_create"></span>**EPT\_S\_CANT\_CREATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-510">1899 (0x76B)</span><span class="sxs-lookup"><span data-stu-id="2ee13-510">1899 (0x76B)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-511">Impossible de créer l’entrée de la base de données du mappeur du point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="2ee13-511">The endpoint mapper database entry could not be created.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-512"><span id="RPC_S_INVALID_OBJECT"></span><span id="rpc_s_invalid_object"></span>**\_objet RPC S \_ non valide \_**</span><span class="sxs-lookup"><span data-stu-id="2ee13-512"><span id="RPC_S_INVALID_OBJECT"></span><span id="rpc_s_invalid_object"></span>**RPC\_S\_INVALID\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-513">1900 (0x76C)</span><span class="sxs-lookup"><span data-stu-id="2ee13-513">1900 (0x76C)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-514">L’identificateur unique universel (UUID) de l’objet est l’UUID Nil.</span><span class="sxs-lookup"><span data-stu-id="2ee13-514">The object universal unique identifier (UUID) is the nil UUID.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-515"><span id="ERROR_INVALID_TIME"></span><span id="error_invalid_time"></span>**\_heure non valide de l’erreur \_**</span><span class="sxs-lookup"><span data-stu-id="2ee13-515"><span id="ERROR_INVALID_TIME"></span><span id="error_invalid_time"></span>**ERROR\_INVALID\_TIME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-516">1901 (0x76D)</span><span class="sxs-lookup"><span data-stu-id="2ee13-516">1901 (0x76D)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-517">L’heure spécifiée n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="2ee13-517">The specified time is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-518"><span id="ERROR_INVALID_FORM_NAME"></span><span id="error_invalid_form_name"></span>**ERREUR \_ de \_ nom de formulaire non valide \_**</span><span class="sxs-lookup"><span data-stu-id="2ee13-518"><span id="ERROR_INVALID_FORM_NAME"></span><span id="error_invalid_form_name"></span>**ERROR\_INVALID\_FORM\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-519">1902 (0x76E)</span><span class="sxs-lookup"><span data-stu-id="2ee13-519">1902 (0x76E)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-520">Le nom de formulaire spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="2ee13-520">The specified form name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-521"><span id="ERROR_INVALID_FORM_SIZE"></span><span id="error_invalid_form_size"></span>**ERREUR \_ de \_ taille de formulaire non valide \_**</span><span class="sxs-lookup"><span data-stu-id="2ee13-521"><span id="ERROR_INVALID_FORM_SIZE"></span><span id="error_invalid_form_size"></span>**ERROR\_INVALID\_FORM\_SIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-522">1903 (0x76F)</span><span class="sxs-lookup"><span data-stu-id="2ee13-522">1903 (0x76F)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-523">La taille de formulaire spécifiée n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="2ee13-523">The specified form size is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-524"><span id="ERROR_ALREADY_WAITING"></span><span id="error_already_waiting"></span>**ERREUR \_ déjà en \_ attente**</span><span class="sxs-lookup"><span data-stu-id="2ee13-524"><span id="ERROR_ALREADY_WAITING"></span><span id="error_already_waiting"></span>**ERROR\_ALREADY\_WAITING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-525">1904 (0x770)</span><span class="sxs-lookup"><span data-stu-id="2ee13-525">1904 (0x770)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-526">Le handle d’imprimante spécifié est déjà attendu.</span><span class="sxs-lookup"><span data-stu-id="2ee13-526">The specified printer handle is already being waited on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-527"><span id="ERROR_PRINTER_DELETED"></span><span id="error_printer_deleted"></span>**ERREUR d' \_ imprimante \_ supprimée**</span><span class="sxs-lookup"><span data-stu-id="2ee13-527"><span id="ERROR_PRINTER_DELETED"></span><span id="error_printer_deleted"></span>**ERROR\_PRINTER\_DELETED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-528">1905 (0x771)</span><span class="sxs-lookup"><span data-stu-id="2ee13-528">1905 (0x771)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-529">L’imprimante spécifiée a été supprimée.</span><span class="sxs-lookup"><span data-stu-id="2ee13-529">The specified printer has been deleted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-530"><span id="ERROR_INVALID_PRINTER_STATE"></span><span id="error_invalid_printer_state"></span>**ERREUR de l’état de l' \_ imprimante non valide \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2ee13-530"><span id="ERROR_INVALID_PRINTER_STATE"></span><span id="error_invalid_printer_state"></span>**ERROR\_INVALID\_PRINTER\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-531">1906 (0x772)</span><span class="sxs-lookup"><span data-stu-id="2ee13-531">1906 (0x772)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-532">L’état de l’imprimante n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="2ee13-532">The state of the printer is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-533"><span id="ERROR_PASSWORD_MUST_CHANGE"></span><span id="error_password_must_change"></span>**le \_ mot de passe d’erreur \_ doit \_ changer**</span><span class="sxs-lookup"><span data-stu-id="2ee13-533"><span id="ERROR_PASSWORD_MUST_CHANGE"></span><span id="error_password_must_change"></span>**ERROR\_PASSWORD\_MUST\_CHANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-534">1907 (0x773)</span><span class="sxs-lookup"><span data-stu-id="2ee13-534">1907 (0x773)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-535">Le mot de passe de l’utilisateur doit être modifié avant la connexion.</span><span class="sxs-lookup"><span data-stu-id="2ee13-535">The user's password must be changed before signing in.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-536"><span id="ERROR_DOMAIN_CONTROLLER_NOT_FOUND"></span><span id="error_domain_controller_not_found"></span>**contrôleur de domaine d’erreur \_ \_ \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="2ee13-536"><span id="ERROR_DOMAIN_CONTROLLER_NOT_FOUND"></span><span id="error_domain_controller_not_found"></span>**ERROR\_DOMAIN\_CONTROLLER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-537">1908 (0x774)</span><span class="sxs-lookup"><span data-stu-id="2ee13-537">1908 (0x774)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-538">Impossible de trouver le contrôleur de domaine pour ce domaine.</span><span class="sxs-lookup"><span data-stu-id="2ee13-538">Could not find the domain controller for this domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-539"><span id="ERROR_ACCOUNT_LOCKED_OUT"></span><span id="error_account_locked_out"></span>**compte d’erreur \_ \_ verrouillé \_**</span><span class="sxs-lookup"><span data-stu-id="2ee13-539"><span id="ERROR_ACCOUNT_LOCKED_OUT"></span><span id="error_account_locked_out"></span>**ERROR\_ACCOUNT\_LOCKED\_OUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-540">1909 (0x775)</span><span class="sxs-lookup"><span data-stu-id="2ee13-540">1909 (0x775)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-541">Le compte référencé est actuellement verrouillé et n’est peut-être pas connecté à.</span><span class="sxs-lookup"><span data-stu-id="2ee13-541">The referenced account is currently locked out and may not be logged on to.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-542"><span id="OR_INVALID_OXID"></span><span id="or_invalid_oxid"></span>**OU \_ Oxid non valide \_**</span><span class="sxs-lookup"><span data-stu-id="2ee13-542"><span id="OR_INVALID_OXID"></span><span id="or_invalid_oxid"></span>**OR\_INVALID\_OXID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-543">1910 (0x776)</span><span class="sxs-lookup"><span data-stu-id="2ee13-543">1910 (0x776)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-544">L’exportateur d’objets spécifié est introuvable.</span><span class="sxs-lookup"><span data-stu-id="2ee13-544">The object exporter specified was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-545"><span id="OR_INVALID_OID"></span><span id="or_invalid_oid"></span>**OU \_ OID non valide \_**</span><span class="sxs-lookup"><span data-stu-id="2ee13-545"><span id="OR_INVALID_OID"></span><span id="or_invalid_oid"></span>**OR\_INVALID\_OID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-546">1911 (0x777)</span><span class="sxs-lookup"><span data-stu-id="2ee13-546">1911 (0x777)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-547">L’objet spécifié est introuvable.</span><span class="sxs-lookup"><span data-stu-id="2ee13-547">The object specified was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-548"><span id="OR_INVALID_SET"></span><span id="or_invalid_set"></span>**OU \_ jeu non valide \_**</span><span class="sxs-lookup"><span data-stu-id="2ee13-548"><span id="OR_INVALID_SET"></span><span id="or_invalid_set"></span>**OR\_INVALID\_SET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-549">1912 (0x778)</span><span class="sxs-lookup"><span data-stu-id="2ee13-549">1912 (0x778)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-550">Le programme de résolution d’objets spécifié n’a pas été trouvé.</span><span class="sxs-lookup"><span data-stu-id="2ee13-550">The object resolver set specified was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-551"><span id="RPC_S_SEND_INCOMPLETE"></span><span id="rpc_s_send_incomplete"></span>**RPC \_ S \_ envoyés \_ incomplets**</span><span class="sxs-lookup"><span data-stu-id="2ee13-551"><span id="RPC_S_SEND_INCOMPLETE"></span><span id="rpc_s_send_incomplete"></span>**RPC\_S\_SEND\_INCOMPLETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-552">1913 (0x779)</span><span class="sxs-lookup"><span data-stu-id="2ee13-552">1913 (0x779)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-553">Certaines données restent à envoyer dans la mémoire tampon de la demande.</span><span class="sxs-lookup"><span data-stu-id="2ee13-553">Some data remains to be sent in the request buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-554"><span id="RPC_S_INVALID_ASYNC_HANDLE"></span><span id="rpc_s_invalid_async_handle"></span>**RPC \_ S \_ \_ handle asynchrone non valide \_**</span><span class="sxs-lookup"><span data-stu-id="2ee13-554"><span id="RPC_S_INVALID_ASYNC_HANDLE"></span><span id="rpc_s_invalid_async_handle"></span>**RPC\_S\_INVALID\_ASYNC\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-555">1914 (0x77A)</span><span class="sxs-lookup"><span data-stu-id="2ee13-555">1914 (0x77A)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-556">Handle d’appel de procédure distante asynchrone non valide.</span><span class="sxs-lookup"><span data-stu-id="2ee13-556">Invalid asynchronous remote procedure call handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-557"><span id="RPC_S_INVALID_ASYNC_CALL"></span><span id="rpc_s_invalid_async_call"></span>**RPC \_ S \_ \_ appel asynchrone non valide \_**</span><span class="sxs-lookup"><span data-stu-id="2ee13-557"><span id="RPC_S_INVALID_ASYNC_CALL"></span><span id="rpc_s_invalid_async_call"></span>**RPC\_S\_INVALID\_ASYNC\_CALL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-558">1915 (0x77B)</span><span class="sxs-lookup"><span data-stu-id="2ee13-558">1915 (0x77B)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-559">Handle d’appel RPC asynchrone non valide pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="2ee13-559">Invalid asynchronous RPC call handle for this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-560"><span id="RPC_X_PIPE_CLOSED"></span><span id="rpc_x_pipe_closed"></span>**\_canal RPC \_ X \_ fermé**</span><span class="sxs-lookup"><span data-stu-id="2ee13-560"><span id="RPC_X_PIPE_CLOSED"></span><span id="rpc_x_pipe_closed"></span>**RPC\_X\_PIPE\_CLOSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-561">1916 (0x77C)</span><span class="sxs-lookup"><span data-stu-id="2ee13-561">1916 (0x77C)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-562">L’objet canal RPC a déjà été fermé.</span><span class="sxs-lookup"><span data-stu-id="2ee13-562">The RPC pipe object has already been closed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-563"><span id="RPC_X_PIPE_DISCIPLINE_ERROR"></span><span id="rpc_x_pipe_discipline_error"></span>**\_erreur de \_ discipline de canal RPC X \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2ee13-563"><span id="RPC_X_PIPE_DISCIPLINE_ERROR"></span><span id="rpc_x_pipe_discipline_error"></span>**RPC\_X\_PIPE\_DISCIPLINE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-564">1917 (0x77D)</span><span class="sxs-lookup"><span data-stu-id="2ee13-564">1917 (0x77D)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-565">L’appel RPC est terminé avant le traitement de tous les canaux.</span><span class="sxs-lookup"><span data-stu-id="2ee13-565">The RPC call completed before all pipes were processed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-566"><span id="RPC_X_PIPE_EMPTY"></span><span id="rpc_x_pipe_empty"></span>**\_canal RPC \_ X \_ vide**</span><span class="sxs-lookup"><span data-stu-id="2ee13-566"><span id="RPC_X_PIPE_EMPTY"></span><span id="rpc_x_pipe_empty"></span>**RPC\_X\_PIPE\_EMPTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-567">1918 (0x77E)</span><span class="sxs-lookup"><span data-stu-id="2ee13-567">1918 (0x77E)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-568">Aucune donnée n’est disponible à partir du canal RPC.</span><span class="sxs-lookup"><span data-stu-id="2ee13-568">No more data is available from the RPC pipe.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-569"><span id="ERROR_NO_SITENAME"></span><span id="error_no_sitename"></span>**ERREUR \_ non \_ SiteName**</span><span class="sxs-lookup"><span data-stu-id="2ee13-569"><span id="ERROR_NO_SITENAME"></span><span id="error_no_sitename"></span>**ERROR\_NO\_SITENAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-570">1919 (0x77F)</span><span class="sxs-lookup"><span data-stu-id="2ee13-570">1919 (0x77F)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-571">Aucun nom de site n’est disponible pour cet ordinateur.</span><span class="sxs-lookup"><span data-stu-id="2ee13-571">No site name is available for this machine.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-572"><span id="ERROR_CANT_ACCESS_FILE"></span><span id="error_cant_access_file"></span>**ERREUR \_ Impossible d' \_ accéder au \_ fichier**</span><span class="sxs-lookup"><span data-stu-id="2ee13-572"><span id="ERROR_CANT_ACCESS_FILE"></span><span id="error_cant_access_file"></span>**ERROR\_CANT\_ACCESS\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-573">1920 (0x780)</span><span class="sxs-lookup"><span data-stu-id="2ee13-573">1920 (0x780)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-574">Le système ne peut pas accéder au fichier.</span><span class="sxs-lookup"><span data-stu-id="2ee13-574">The file cannot be accessed by the system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-575"><span id="ERROR_CANT_RESOLVE_FILENAME"></span><span id="error_cant_resolve_filename"></span>**ERREUR \_ Impossible de \_ résoudre le nom de \_ fichier**</span><span class="sxs-lookup"><span data-stu-id="2ee13-575"><span id="ERROR_CANT_RESOLVE_FILENAME"></span><span id="error_cant_resolve_filename"></span>**ERROR\_CANT\_RESOLVE\_FILENAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-576">1921 (0x781)</span><span class="sxs-lookup"><span data-stu-id="2ee13-576">1921 (0x781)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-577">Le nom du fichier ne peut pas être résolu par le système.</span><span class="sxs-lookup"><span data-stu-id="2ee13-577">The name of the file cannot be resolved by the system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-578"><span id="RPC_S_ENTRY_TYPE_MISMATCH"></span><span id="rpc_s_entry_type_mismatch"></span>**incompatibilité de type d’entrée RPC \_ S \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2ee13-578"><span id="RPC_S_ENTRY_TYPE_MISMATCH"></span><span id="rpc_s_entry_type_mismatch"></span>**RPC\_S\_ENTRY\_TYPE\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-579">1922 (0x782)</span><span class="sxs-lookup"><span data-stu-id="2ee13-579">1922 (0x782)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-580">L’entrée n’est pas du type attendu.</span><span class="sxs-lookup"><span data-stu-id="2ee13-580">The entry is not of the expected type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-581"><span id="RPC_S_NOT_ALL_OBJS_EXPORTED"></span><span id="rpc_s_not_all_objs_exported"></span>**RPC \_ S \_ \_ tous les \_ ne comportaient \_ exportés**</span><span class="sxs-lookup"><span data-stu-id="2ee13-581"><span id="RPC_S_NOT_ALL_OBJS_EXPORTED"></span><span id="rpc_s_not_all_objs_exported"></span>**RPC\_S\_NOT\_ALL\_OBJS\_EXPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-582">1923 (0x783)</span><span class="sxs-lookup"><span data-stu-id="2ee13-582">1923 (0x783)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-583">Tous les UUID d’objet n’ont pas pu être exportés vers l’entrée spécifiée.</span><span class="sxs-lookup"><span data-stu-id="2ee13-583">Not all object UUIDs could be exported to the specified entry.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-584"><span id="RPC_S_INTERFACE_NOT_EXPORTED"></span><span id="rpc_s_interface_not_exported"></span>**\_interface RPC \_ S \_ non \_ exportée**</span><span class="sxs-lookup"><span data-stu-id="2ee13-584"><span id="RPC_S_INTERFACE_NOT_EXPORTED"></span><span id="rpc_s_interface_not_exported"></span>**RPC\_S\_INTERFACE\_NOT\_EXPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-585">1924 (0x784)</span><span class="sxs-lookup"><span data-stu-id="2ee13-585">1924 (0x784)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-586">L’interface n’a pas pu être exportée vers l’entrée spécifiée.</span><span class="sxs-lookup"><span data-stu-id="2ee13-586">Interface could not be exported to the specified entry.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-587"><span id="RPC_S_PROFILE_NOT_ADDED"></span><span id="rpc_s_profile_not_added"></span>**\_Profil RPC \_ S \_ non \_ ajouté**</span><span class="sxs-lookup"><span data-stu-id="2ee13-587"><span id="RPC_S_PROFILE_NOT_ADDED"></span><span id="rpc_s_profile_not_added"></span>**RPC\_S\_PROFILE\_NOT\_ADDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-588">1925 (0x785)</span><span class="sxs-lookup"><span data-stu-id="2ee13-588">1925 (0x785)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-589">Impossible d’ajouter l’entrée de profil spécifiée.</span><span class="sxs-lookup"><span data-stu-id="2ee13-589">The specified profile entry could not be added.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-590"><span id="RPC_S_PRF_ELT_NOT_ADDED"></span><span id="rpc_s_prf_elt_not_added"></span>**le \_ PRF du PRF RPC S \_ \_ n’a \_ pas \_ été ajouté**</span><span class="sxs-lookup"><span data-stu-id="2ee13-590"><span id="RPC_S_PRF_ELT_NOT_ADDED"></span><span id="rpc_s_prf_elt_not_added"></span>**RPC\_S\_PRF\_ELT\_NOT\_ADDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-591">1926 (0x786)</span><span class="sxs-lookup"><span data-stu-id="2ee13-591">1926 (0x786)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-592">Impossible d’ajouter l’élément de profil spécifié.</span><span class="sxs-lookup"><span data-stu-id="2ee13-592">The specified profile element could not be added.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-593"><span id="RPC_S_PRF_ELT_NOT_REMOVED"></span><span id="rpc_s_prf_elt_not_removed"></span>**le PRF de la RPC \_ S \_ \_ ELT \_ n’a pas \_ été supprimé**</span><span class="sxs-lookup"><span data-stu-id="2ee13-593"><span id="RPC_S_PRF_ELT_NOT_REMOVED"></span><span id="rpc_s_prf_elt_not_removed"></span>**RPC\_S\_PRF\_ELT\_NOT\_REMOVED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-594">1927 (0x787)</span><span class="sxs-lookup"><span data-stu-id="2ee13-594">1927 (0x787)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-595">Impossible de supprimer l’élément de profil spécifié.</span><span class="sxs-lookup"><span data-stu-id="2ee13-595">The specified profile element could not be removed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-596"><span id="RPC_S_GRP_ELT_NOT_ADDED"></span><span id="rpc_s_grp_elt_not_added"></span>**la GRP de l’appel de procédure de \_ \_ GRP est \_ \_ non \_ ajoutée**</span><span class="sxs-lookup"><span data-stu-id="2ee13-596"><span id="RPC_S_GRP_ELT_NOT_ADDED"></span><span id="rpc_s_grp_elt_not_added"></span>**RPC\_S\_GRP\_ELT\_NOT\_ADDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-597">1928 (0x788)</span><span class="sxs-lookup"><span data-stu-id="2ee13-597">1928 (0x788)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-598">Impossible d’ajouter l’élément de groupe.</span><span class="sxs-lookup"><span data-stu-id="2ee13-598">The group element could not be added.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-599"><span id="RPC_S_GRP_ELT_NOT_REMOVED"></span><span id="rpc_s_grp_elt_not_removed"></span>**la GRP des appels RPC \_ \_ \_ ELT \_ n’a pas \_ été supprimée**</span><span class="sxs-lookup"><span data-stu-id="2ee13-599"><span id="RPC_S_GRP_ELT_NOT_REMOVED"></span><span id="rpc_s_grp_elt_not_removed"></span>**RPC\_S\_GRP\_ELT\_NOT\_REMOVED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-600">1929 (0x789)</span><span class="sxs-lookup"><span data-stu-id="2ee13-600">1929 (0x789)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-601">Impossible de supprimer l’élément de groupe.</span><span class="sxs-lookup"><span data-stu-id="2ee13-601">The group element could not be removed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-602"><span id="ERROR_KM_DRIVER_BLOCKED"></span><span id="error_km_driver_blocked"></span>**ERREUR \_ de \_ pilote km \_ bloqué**</span><span class="sxs-lookup"><span data-stu-id="2ee13-602"><span id="ERROR_KM_DRIVER_BLOCKED"></span><span id="error_km_driver_blocked"></span>**ERROR\_KM\_DRIVER\_BLOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-603">1930 (0x78A)</span><span class="sxs-lookup"><span data-stu-id="2ee13-603">1930 (0x78A)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-604">Le pilote d’imprimante n’est pas compatible avec une stratégie activée sur votre ordinateur qui bloque les pilotes NT 4,0.</span><span class="sxs-lookup"><span data-stu-id="2ee13-604">The printer driver is not compatible with a policy enabled on your computer that blocks NT 4.0 drivers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-605"><span id="ERROR_CONTEXT_EXPIRED"></span><span id="error_context_expired"></span>**contexte d’erreur \_ \_ expiré**</span><span class="sxs-lookup"><span data-stu-id="2ee13-605"><span id="ERROR_CONTEXT_EXPIRED"></span><span id="error_context_expired"></span>**ERROR\_CONTEXT\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-606">1931 (0x78B)</span><span class="sxs-lookup"><span data-stu-id="2ee13-606">1931 (0x78B)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-607">Le contexte a expiré et ne peut plus être utilisé.</span><span class="sxs-lookup"><span data-stu-id="2ee13-607">The context has expired and can no longer be used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-608"><span id="ERROR_PER_USER_TRUST_QUOTA_EXCEEDED"></span><span id="error_per_user_trust_quota_exceeded"></span>**ERREUR \_ par \_ quota de confiance de l’utilisateur \_ \_ \_ dépassé**</span><span class="sxs-lookup"><span data-stu-id="2ee13-608"><span id="ERROR_PER_USER_TRUST_QUOTA_EXCEEDED"></span><span id="error_per_user_trust_quota_exceeded"></span>**ERROR\_PER\_USER\_TRUST\_QUOTA\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-609">1932 (0x78C)</span><span class="sxs-lookup"><span data-stu-id="2ee13-609">1932 (0x78C)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-610">Le quota de création d’approbation déléguée de l’utilisateur actuel a été dépassé.</span><span class="sxs-lookup"><span data-stu-id="2ee13-610">The current user's delegated trust creation quota has been exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-611"><span id="ERROR_ALL_USER_TRUST_QUOTA_EXCEEDED"></span><span id="error_all_user_trust_quota_exceeded"></span>**ERREUR l’intégralité du quota de confiance de l' \_ utilisateur est \_ \_ \_ \_ dépassée**</span><span class="sxs-lookup"><span data-stu-id="2ee13-611"><span id="ERROR_ALL_USER_TRUST_QUOTA_EXCEEDED"></span><span id="error_all_user_trust_quota_exceeded"></span>**ERROR\_ALL\_USER\_TRUST\_QUOTA\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-612">1933 (0x78D)</span><span class="sxs-lookup"><span data-stu-id="2ee13-612">1933 (0x78D)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-613">Le quota de création d’approbation déléguée totale a été dépassé.</span><span class="sxs-lookup"><span data-stu-id="2ee13-613">The total delegated trust creation quota has been exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-614"><span id="ERROR_USER_DELETE_TRUST_QUOTA_EXCEEDED"></span><span id="error_user_delete_trust_quota_exceeded"></span>**ERREUR la suppression du quota de confiance par l' \_ utilisateur est \_ \_ \_ \_ dépassée**</span><span class="sxs-lookup"><span data-stu-id="2ee13-614"><span id="ERROR_USER_DELETE_TRUST_QUOTA_EXCEEDED"></span><span id="error_user_delete_trust_quota_exceeded"></span>**ERROR\_USER\_DELETE\_TRUST\_QUOTA\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-615">1934 (0x78E)</span><span class="sxs-lookup"><span data-stu-id="2ee13-615">1934 (0x78E)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-616">Le quota de suppression d’approbation déléguée de l’utilisateur actuel a été dépassé.</span><span class="sxs-lookup"><span data-stu-id="2ee13-616">The current user's delegated trust deletion quota has been exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-617"><span id="ERROR_AUTHENTICATION_FIREWALL_FAILED"></span><span id="error_authentication_firewall_failed"></span>**ERREUR \_ de \_ pare-feu d’authentification \_**</span><span class="sxs-lookup"><span data-stu-id="2ee13-617"><span id="ERROR_AUTHENTICATION_FIREWALL_FAILED"></span><span id="error_authentication_firewall_failed"></span>**ERROR\_AUTHENTICATION\_FIREWALL\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-618">1935 (0x78F)</span><span class="sxs-lookup"><span data-stu-id="2ee13-618">1935 (0x78F)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-619">L’ordinateur avec lequel vous vous connectez est protégé par un pare-feu d’authentification.</span><span class="sxs-lookup"><span data-stu-id="2ee13-619">The computer you are signing into is protected by an authentication firewall.</span></span> <span data-ttu-id="2ee13-620">Le compte spécifié n’est pas autorisé à s’authentifier sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="2ee13-620">The specified account is not allowed to authenticate to the computer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-621"><span id="ERROR_REMOTE_PRINT_CONNECTIONS_BLOCKED"></span><span id="error_remote_print_connections_blocked"></span>**ERREUR \_ de \_ connexions d’impression à distance \_ \_ bloquées**</span><span class="sxs-lookup"><span data-stu-id="2ee13-621"><span id="ERROR_REMOTE_PRINT_CONNECTIONS_BLOCKED"></span><span id="error_remote_print_connections_blocked"></span>**ERROR\_REMOTE\_PRINT\_CONNECTIONS\_BLOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-622">1936 (0x790)</span><span class="sxs-lookup"><span data-stu-id="2ee13-622">1936 (0x790)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-623">Les connexions à distance au spouleur d’impression sont bloquées par une stratégie définie sur votre machine.</span><span class="sxs-lookup"><span data-stu-id="2ee13-623">Remote connections to the Print Spooler are blocked by a policy set on your machine.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-624"><span id="ERROR_NTLM_BLOCKED"></span><span id="error_ntlm_blocked"></span>**ERREUR \_ NTLM \_ bloquée**</span><span class="sxs-lookup"><span data-stu-id="2ee13-624"><span id="ERROR_NTLM_BLOCKED"></span><span id="error_ntlm_blocked"></span>**ERROR\_NTLM\_BLOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-625">1937 (0x791)</span><span class="sxs-lookup"><span data-stu-id="2ee13-625">1937 (0x791)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-626">L’authentification a échoué car l’authentification NTLM a été désactivée.</span><span class="sxs-lookup"><span data-stu-id="2ee13-626">Authentication failed because NTLM authentication has been disabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-627"><span id="ERROR_PASSWORD_CHANGE_REQUIRED"></span><span id="error_password_change_required"></span>**\_modification du mot de passe d’erreur \_ \_ obligatoire**</span><span class="sxs-lookup"><span data-stu-id="2ee13-627"><span id="ERROR_PASSWORD_CHANGE_REQUIRED"></span><span id="error_password_change_required"></span>**ERROR\_PASSWORD\_CHANGE\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-628">1938 (0x792)</span><span class="sxs-lookup"><span data-stu-id="2ee13-628">1938 (0x792)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-629">Échec de l’ouverture de session : la stratégie EAS exige que l’utilisateur modifie son mot de passe avant que cette opération puisse être effectuée.</span><span class="sxs-lookup"><span data-stu-id="2ee13-629">Logon Failure: EAS policy requires that the user change their password before this operation can be performed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-630"><span id="ERROR_INVALID_PIXEL_FORMAT"></span><span id="error_invalid_pixel_format"></span>**ERREUR \_ \_ au format de pixel non valide \_**</span><span class="sxs-lookup"><span data-stu-id="2ee13-630"><span id="ERROR_INVALID_PIXEL_FORMAT"></span><span id="error_invalid_pixel_format"></span>**ERROR\_INVALID\_PIXEL\_FORMAT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-631">2000 (0x7D0)</span><span class="sxs-lookup"><span data-stu-id="2ee13-631">2000 (0x7D0)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-632">Le format de pixel n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="2ee13-632">The pixel format is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-633"><span id="ERROR_BAD_DRIVER"></span><span id="error_bad_driver"></span>**ERREUR \_ de \_ pilote incorrect**</span><span class="sxs-lookup"><span data-stu-id="2ee13-633"><span id="ERROR_BAD_DRIVER"></span><span id="error_bad_driver"></span>**ERROR\_BAD\_DRIVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-634">2001 (0x7D1)</span><span class="sxs-lookup"><span data-stu-id="2ee13-634">2001 (0x7D1)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-635">Le pilote spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="2ee13-635">The specified driver is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-636"><span id="ERROR_INVALID_WINDOW_STYLE"></span><span id="error_invalid_window_style"></span>**ERREUR \_ de \_ style de fenêtre non valide \_**</span><span class="sxs-lookup"><span data-stu-id="2ee13-636"><span id="ERROR_INVALID_WINDOW_STYLE"></span><span id="error_invalid_window_style"></span>**ERROR\_INVALID\_WINDOW\_STYLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-637">2002 (0x7D2)</span><span class="sxs-lookup"><span data-stu-id="2ee13-637">2002 (0x7D2)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-638">Le style de fenêtre ou l’attribut de classe n’est pas valide pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="2ee13-638">The window style or class attribute is invalid for this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-639"><span id="ERROR_METAFILE_NOT_SUPPORTED"></span><span id="error_metafile_not_supported"></span>**métafichier d’erreur \_ \_ non \_ pris en charge**</span><span class="sxs-lookup"><span data-stu-id="2ee13-639"><span id="ERROR_METAFILE_NOT_SUPPORTED"></span><span id="error_metafile_not_supported"></span>**ERROR\_METAFILE\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-640">2003 (0x7D3)</span><span class="sxs-lookup"><span data-stu-id="2ee13-640">2003 (0x7D3)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-641">L’opération de métafichier demandée n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="2ee13-641">The requested metafile operation is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-642"><span id="ERROR_TRANSFORM_NOT_SUPPORTED"></span><span id="error_transform_not_supported"></span>**transformation d’erreur \_ \_ non \_ prise en charge**</span><span class="sxs-lookup"><span data-stu-id="2ee13-642"><span id="ERROR_TRANSFORM_NOT_SUPPORTED"></span><span id="error_transform_not_supported"></span>**ERROR\_TRANSFORM\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-643">2004 (0x7D4)</span><span class="sxs-lookup"><span data-stu-id="2ee13-643">2004 (0x7D4)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-644">L’opération de transformation demandée n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="2ee13-644">The requested transformation operation is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-645"><span id="ERROR_CLIPPING_NOT_SUPPORTED"></span><span id="error_clipping_not_supported"></span>**découpage des erreurs \_ \_ non \_ pris en charge**</span><span class="sxs-lookup"><span data-stu-id="2ee13-645"><span id="ERROR_CLIPPING_NOT_SUPPORTED"></span><span id="error_clipping_not_supported"></span>**ERROR\_CLIPPING\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-646">2005 (0x7D5)</span><span class="sxs-lookup"><span data-stu-id="2ee13-646">2005 (0x7D5)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-647">L’opération de découpage demandée n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="2ee13-647">The requested clipping operation is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-648"><span id="ERROR_INVALID_CMM"></span><span id="error_invalid_cmm"></span>**ERREUR \_ CMM non valide \_**</span><span class="sxs-lookup"><span data-stu-id="2ee13-648"><span id="ERROR_INVALID_CMM"></span><span id="error_invalid_cmm"></span>**ERROR\_INVALID\_CMM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-649">2010 (0x7DA)</span><span class="sxs-lookup"><span data-stu-id="2ee13-649">2010 (0x7DA)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-650">Le module de gestion des couleurs spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="2ee13-650">The specified color management module is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-651"><span id="ERROR_INVALID_PROFILE"></span><span id="error_invalid_profile"></span>**ERREUR \_ de \_ Profil non valide**</span><span class="sxs-lookup"><span data-stu-id="2ee13-651"><span id="ERROR_INVALID_PROFILE"></span><span id="error_invalid_profile"></span>**ERROR\_INVALID\_PROFILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-652">2011 (0x7DB)</span><span class="sxs-lookup"><span data-stu-id="2ee13-652">2011 (0x7DB)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-653">Le profil de couleurs spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="2ee13-653">The specified color profile is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-654"><span id="ERROR_TAG_NOT_FOUND"></span><span id="error_tag_not_found"></span>**\_balise d’erreur \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="2ee13-654"><span id="ERROR_TAG_NOT_FOUND"></span><span id="error_tag_not_found"></span>**ERROR\_TAG\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-655">2012 (0x7DC)</span><span class="sxs-lookup"><span data-stu-id="2ee13-655">2012 (0x7DC)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-656">La balise spécifiée est introuvable.</span><span class="sxs-lookup"><span data-stu-id="2ee13-656">The specified tag was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-657"><span id="ERROR_TAG_NOT_PRESENT"></span><span id="error_tag_not_present"></span>**\_balise d’erreur \_ \_ absente**</span><span class="sxs-lookup"><span data-stu-id="2ee13-657"><span id="ERROR_TAG_NOT_PRESENT"></span><span id="error_tag_not_present"></span>**ERROR\_TAG\_NOT\_PRESENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-658">2013 (0x7DD)</span><span class="sxs-lookup"><span data-stu-id="2ee13-658">2013 (0x7DD)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-659">Une balise requise n’est pas présente.</span><span class="sxs-lookup"><span data-stu-id="2ee13-659">A required tag is not present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-660"><span id="ERROR_DUPLICATE_TAG"></span><span id="error_duplicate_tag"></span>**\_balise d’erreur dupliquée \_**</span><span class="sxs-lookup"><span data-stu-id="2ee13-660"><span id="ERROR_DUPLICATE_TAG"></span><span id="error_duplicate_tag"></span>**ERROR\_DUPLICATE\_TAG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-661">2014 (0x7DE)</span><span class="sxs-lookup"><span data-stu-id="2ee13-661">2014 (0x7DE)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-662">La balise spécifiée est déjà présente.</span><span class="sxs-lookup"><span data-stu-id="2ee13-662">The specified tag is already present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-663"><span id="ERROR_PROFILE_NOT_ASSOCIATED_WITH_DEVICE"></span><span id="error_profile_not_associated_with_device"></span>**\_profil \_ d’erreur non \_ associé à l' \_ \_ appareil**</span><span class="sxs-lookup"><span data-stu-id="2ee13-663"><span id="ERROR_PROFILE_NOT_ASSOCIATED_WITH_DEVICE"></span><span id="error_profile_not_associated_with_device"></span>**ERROR\_PROFILE\_NOT\_ASSOCIATED\_WITH\_DEVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-664">2015 (0x7DF)</span><span class="sxs-lookup"><span data-stu-id="2ee13-664">2015 (0x7DF)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-665">Le profil de couleurs spécifié n’est pas associé à l’appareil spécifié.</span><span class="sxs-lookup"><span data-stu-id="2ee13-665">The specified color profile is not associated with the specified device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-666"><span id="ERROR_PROFILE_NOT_FOUND"></span><span id="error_profile_not_found"></span>**\_profil d' \_ erreur \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="2ee13-666"><span id="ERROR_PROFILE_NOT_FOUND"></span><span id="error_profile_not_found"></span>**ERROR\_PROFILE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-667">2016 (0x7E0)</span><span class="sxs-lookup"><span data-stu-id="2ee13-667">2016 (0x7E0)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-668">Le profil de couleurs spécifié est introuvable.</span><span class="sxs-lookup"><span data-stu-id="2ee13-668">The specified color profile was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-669"><span id="ERROR_INVALID_COLORSPACE"></span><span id="error_invalid_colorspace"></span>**ERREUR \_ COLORSPACE non valide \_**</span><span class="sxs-lookup"><span data-stu-id="2ee13-669"><span id="ERROR_INVALID_COLORSPACE"></span><span id="error_invalid_colorspace"></span>**ERROR\_INVALID\_COLORSPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-670">2017 (0x7E1)</span><span class="sxs-lookup"><span data-stu-id="2ee13-670">2017 (0x7E1)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-671">L’espace de couleurs spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="2ee13-671">The specified color space is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-672"><span id="ERROR_ICM_NOT_ENABLED"></span><span id="error_icm_not_enabled"></span>**ERREUR \_ ICM \_ non \_ activée**</span><span class="sxs-lookup"><span data-stu-id="2ee13-672"><span id="ERROR_ICM_NOT_ENABLED"></span><span id="error_icm_not_enabled"></span>**ERROR\_ICM\_NOT\_ENABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-673">2018 (0x7E2)</span><span class="sxs-lookup"><span data-stu-id="2ee13-673">2018 (0x7E2)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-674">La gestion des couleurs des images n’est pas activée.</span><span class="sxs-lookup"><span data-stu-id="2ee13-674">Image Color Management is not enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-675"><span id="ERROR_DELETING_ICM_XFORM"></span><span id="error_deleting_icm_xform"></span>**ERREUR lors de \_ la suppression du \_ \_ XForm CCI**</span><span class="sxs-lookup"><span data-stu-id="2ee13-675"><span id="ERROR_DELETING_ICM_XFORM"></span><span id="error_deleting_icm_xform"></span>**ERROR\_DELETING\_ICM\_XFORM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-676">2019 (0x7E3)</span><span class="sxs-lookup"><span data-stu-id="2ee13-676">2019 (0x7E3)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-677">Une erreur s’est produite lors de la suppression de la transformation de couleur.</span><span class="sxs-lookup"><span data-stu-id="2ee13-677">There was an error while deleting the color transform.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-678"><span id="ERROR_INVALID_TRANSFORM"></span><span id="error_invalid_transform"></span>**ERREUR \_ de \_ transformation non valide**</span><span class="sxs-lookup"><span data-stu-id="2ee13-678"><span id="ERROR_INVALID_TRANSFORM"></span><span id="error_invalid_transform"></span>**ERROR\_INVALID\_TRANSFORM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-679">2020 (0x7E4)</span><span class="sxs-lookup"><span data-stu-id="2ee13-679">2020 (0x7E4)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-680">La transformation de couleur spécifiée n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="2ee13-680">The specified color transform is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-681"><span id="ERROR_COLORSPACE_MISMATCH"></span><span id="error_colorspace_mismatch"></span>**ERREUR \_ d' \_ incompatibilité COLORSPACE**</span><span class="sxs-lookup"><span data-stu-id="2ee13-681"><span id="ERROR_COLORSPACE_MISMATCH"></span><span id="error_colorspace_mismatch"></span>**ERROR\_COLORSPACE\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-682">2021 (0x7E5)</span><span class="sxs-lookup"><span data-stu-id="2ee13-682">2021 (0x7E5)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-683">La transformation spécifiée ne correspond pas à l’espace de couleurs de la bitmap.</span><span class="sxs-lookup"><span data-stu-id="2ee13-683">The specified transform does not match the bitmap's color space.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-684"><span id="ERROR_INVALID_COLORINDEX"></span><span id="error_invalid_colorindex"></span>**ERREUR \_ ColorIndex non valide \_**</span><span class="sxs-lookup"><span data-stu-id="2ee13-684"><span id="ERROR_INVALID_COLORINDEX"></span><span id="error_invalid_colorindex"></span>**ERROR\_INVALID\_COLORINDEX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-685">2022 (0x7E6)</span><span class="sxs-lookup"><span data-stu-id="2ee13-685">2022 (0x7E6)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-686">L’index de couleur nommé spécifié n’est pas présent dans le profil.</span><span class="sxs-lookup"><span data-stu-id="2ee13-686">The specified named color index is not present in the profile.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-687"><span id="ERROR_PROFILE_DOES_NOT_MATCH_DEVICE"></span><span id="error_profile_does_not_match_device"></span>**le \_ profil d’erreur \_ ne \_ \_ correspond pas au \_ périphérique**</span><span class="sxs-lookup"><span data-stu-id="2ee13-687"><span id="ERROR_PROFILE_DOES_NOT_MATCH_DEVICE"></span><span id="error_profile_does_not_match_device"></span>**ERROR\_PROFILE\_DOES\_NOT\_MATCH\_DEVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-688">2023 (0x7E7)</span><span class="sxs-lookup"><span data-stu-id="2ee13-688">2023 (0x7E7)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-689">Le profil spécifié est destiné à un périphérique d’un type différent de celui du périphérique spécifié.</span><span class="sxs-lookup"><span data-stu-id="2ee13-689">The specified profile is intended for a device of a different type than the specified device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-690"><span id="ERROR_CONNECTED_OTHER_PASSWORD"></span><span id="error_connected_other_password"></span>**ERREUR lors de la connexion d’un \_ \_ autre \_ mot de passe**</span><span class="sxs-lookup"><span data-stu-id="2ee13-690"><span id="ERROR_CONNECTED_OTHER_PASSWORD"></span><span id="error_connected_other_password"></span>**ERROR\_CONNECTED\_OTHER\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-691">2108 (0x83C)</span><span class="sxs-lookup"><span data-stu-id="2ee13-691">2108 (0x83C)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-692">La connexion réseau a été établie avec succès, mais l’utilisateur devait être invité à entrer un mot de passe différent de celui spécifié à l’origine.</span><span class="sxs-lookup"><span data-stu-id="2ee13-692">The network connection was made successfully, but the user had to be prompted for a password other than the one originally specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-693"><span id="ERROR_CONNECTED_OTHER_PASSWORD_DEFAULT"></span><span id="error_connected_other_password_default"></span>**ERREUR \_ liée à un \_ autre \_ mot de passe \_ par défaut**</span><span class="sxs-lookup"><span data-stu-id="2ee13-693"><span id="ERROR_CONNECTED_OTHER_PASSWORD_DEFAULT"></span><span id="error_connected_other_password_default"></span>**ERROR\_CONNECTED\_OTHER\_PASSWORD\_DEFAULT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-694">2109 (0x83D)</span><span class="sxs-lookup"><span data-stu-id="2ee13-694">2109 (0x83D)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-695">La connexion réseau a été établie avec succès à l’aide des informations d’identification par défaut.</span><span class="sxs-lookup"><span data-stu-id="2ee13-695">The network connection was made successfully using default credentials.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-696"><span id="ERROR_BAD_USERNAME"></span><span id="error_bad_username"></span>**ERREUR \_ \_ nom d’utilisateur incorrect**</span><span class="sxs-lookup"><span data-stu-id="2ee13-696"><span id="ERROR_BAD_USERNAME"></span><span id="error_bad_username"></span>**ERROR\_BAD\_USERNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-697">2202 (0x89A)</span><span class="sxs-lookup"><span data-stu-id="2ee13-697">2202 (0x89A)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-698">Le nom d’utilisateur spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="2ee13-698">The specified username is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-699"><span id="ERROR_NOT_CONNECTED"></span><span id="error_not_connected"></span>**ERREUR \_ non \_ connectée**</span><span class="sxs-lookup"><span data-stu-id="2ee13-699"><span id="ERROR_NOT_CONNECTED"></span><span id="error_not_connected"></span>**ERROR\_NOT\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-700">2250 (0x8CA)</span><span class="sxs-lookup"><span data-stu-id="2ee13-700">2250 (0x8CA)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-701">Cette connexion réseau n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="2ee13-701">This network connection does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-702"><span id="ERROR_OPEN_FILES"></span><span id="error_open_files"></span>**ERREUR lors de l' \_ ouverture des \_ fichiers**</span><span class="sxs-lookup"><span data-stu-id="2ee13-702"><span id="ERROR_OPEN_FILES"></span><span id="error_open_files"></span>**ERROR\_OPEN\_FILES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-703">2401 (0x961)</span><span class="sxs-lookup"><span data-stu-id="2ee13-703">2401 (0x961)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-704">Cette connexion réseau a des fichiers ouverts ou des demandes en attente.</span><span class="sxs-lookup"><span data-stu-id="2ee13-704">This network connection has files open or requests pending.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-705"><span id="ERROR_ACTIVE_CONNECTIONS"></span><span id="error_active_connections"></span>**\_connexions actives d’erreur \_**</span><span class="sxs-lookup"><span data-stu-id="2ee13-705"><span id="ERROR_ACTIVE_CONNECTIONS"></span><span id="error_active_connections"></span>**ERROR\_ACTIVE\_CONNECTIONS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-706">2402 (0x962)</span><span class="sxs-lookup"><span data-stu-id="2ee13-706">2402 (0x962)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-707">Les connexions actives existent toujours.</span><span class="sxs-lookup"><span data-stu-id="2ee13-707">Active connections still exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-708"><span id="ERROR_DEVICE_IN_USE"></span><span id="error_device_in_use"></span>**\_périphérique \_ d’erreur en cours d' \_ utilisation**</span><span class="sxs-lookup"><span data-stu-id="2ee13-708"><span id="ERROR_DEVICE_IN_USE"></span><span id="error_device_in_use"></span>**ERROR\_DEVICE\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-709">2404 (0x964)</span><span class="sxs-lookup"><span data-stu-id="2ee13-709">2404 (0x964)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-710">L’appareil est en cours d’utilisation par un processus actif et ne peut pas être déconnecté.</span><span class="sxs-lookup"><span data-stu-id="2ee13-710">The device is in use by an active process and cannot be disconnected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-711"><span id="ERROR_UNKNOWN_PRINT_MONITOR"></span><span id="error_unknown_print_monitor"></span>**ERREUR \_ de \_ moniteur d’impression inconnu \_**</span><span class="sxs-lookup"><span data-stu-id="2ee13-711"><span id="ERROR_UNKNOWN_PRINT_MONITOR"></span><span id="error_unknown_print_monitor"></span>**ERROR\_UNKNOWN\_PRINT\_MONITOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-712">3000 (0xBB8)</span><span class="sxs-lookup"><span data-stu-id="2ee13-712">3000 (0xBB8)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-713">Le moniteur d’impression spécifié est inconnu.</span><span class="sxs-lookup"><span data-stu-id="2ee13-713">The specified print monitor is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-714"><span id="ERROR_PRINTER_DRIVER_IN_USE"></span><span id="error_printer_driver_in_use"></span>**ERREUR \_ \_ de pilote \_ d’imprimante en cours d' \_ utilisation**</span><span class="sxs-lookup"><span data-stu-id="2ee13-714"><span id="ERROR_PRINTER_DRIVER_IN_USE"></span><span id="error_printer_driver_in_use"></span>**ERROR\_PRINTER\_DRIVER\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-715">3001 (0xBB9)</span><span class="sxs-lookup"><span data-stu-id="2ee13-715">3001 (0xBB9)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-716">Le pilote d’imprimante spécifié est en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="2ee13-716">The specified printer driver is currently in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-717"><span id="ERROR_SPOOL_FILE_NOT_FOUND"></span><span id="error_spool_file_not_found"></span>**fichier de mise en file d’attente d’erreurs \_ \_ \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="2ee13-717"><span id="ERROR_SPOOL_FILE_NOT_FOUND"></span><span id="error_spool_file_not_found"></span>**ERROR\_SPOOL\_FILE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-718">3002 (0xBBA)</span><span class="sxs-lookup"><span data-stu-id="2ee13-718">3002 (0xBBA)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-719">Le fichier de mise en file d’attente est introuvable.</span><span class="sxs-lookup"><span data-stu-id="2ee13-719">The spool file was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-720"><span id="ERROR_SPL_NO_STARTDOC"></span><span id="error_spl_no_startdoc"></span>**ERREUR \_ SPL \_ non \_ STARTDOC**</span><span class="sxs-lookup"><span data-stu-id="2ee13-720"><span id="ERROR_SPL_NO_STARTDOC"></span><span id="error_spl_no_startdoc"></span>**ERROR\_SPL\_NO\_STARTDOC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-721">3003 (0xBBB)</span><span class="sxs-lookup"><span data-stu-id="2ee13-721">3003 (0xBBB)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-722">Un appel StartDocPrinter n’a pas été émis.</span><span class="sxs-lookup"><span data-stu-id="2ee13-722">A StartDocPrinter call was not issued.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-723"><span id="ERROR_SPL_NO_ADDJOB"></span><span id="error_spl_no_addjob"></span>**ERREUR \_ SPL \_ non \_ ADDJOB**</span><span class="sxs-lookup"><span data-stu-id="2ee13-723"><span id="ERROR_SPL_NO_ADDJOB"></span><span id="error_spl_no_addjob"></span>**ERROR\_SPL\_NO\_ADDJOB**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-724">3004 (0xBBC)</span><span class="sxs-lookup"><span data-stu-id="2ee13-724">3004 (0xBBC)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-725">Un appel AddJob n’a pas été émis.</span><span class="sxs-lookup"><span data-stu-id="2ee13-725">An AddJob call was not issued.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-726"><span id="ERROR_PRINT_PROCESSOR_ALREADY_INSTALLED"></span><span id="error_print_processor_already_installed"></span>**le processeur d’impression des erreurs est \_ \_ \_ déjà \_ installé**</span><span class="sxs-lookup"><span data-stu-id="2ee13-726"><span id="ERROR_PRINT_PROCESSOR_ALREADY_INSTALLED"></span><span id="error_print_processor_already_installed"></span>**ERROR\_PRINT\_PROCESSOR\_ALREADY\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-727">3005 (0xBBD)</span><span class="sxs-lookup"><span data-stu-id="2ee13-727">3005 (0xBBD)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-728">Le processeur d’impression spécifié a déjà été installé.</span><span class="sxs-lookup"><span data-stu-id="2ee13-728">The specified print processor has already been installed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-729"><span id="ERROR_PRINT_MONITOR_ALREADY_INSTALLED"></span><span id="error_print_monitor_already_installed"></span>**ERREUR \_ de \_ moniteur d’impression \_ déjà \_ installée**</span><span class="sxs-lookup"><span data-stu-id="2ee13-729"><span id="ERROR_PRINT_MONITOR_ALREADY_INSTALLED"></span><span id="error_print_monitor_already_installed"></span>**ERROR\_PRINT\_MONITOR\_ALREADY\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-730">3006 (0xBBE)</span><span class="sxs-lookup"><span data-stu-id="2ee13-730">3006 (0xBBE)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-731">Le moniteur d’impression spécifié a déjà été installé.</span><span class="sxs-lookup"><span data-stu-id="2ee13-731">The specified print monitor has already been installed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-732"><span id="ERROR_INVALID_PRINT_MONITOR"></span><span id="error_invalid_print_monitor"></span>**ERREUR \_ de \_ moniteur d’impression non valide \_**</span><span class="sxs-lookup"><span data-stu-id="2ee13-732"><span id="ERROR_INVALID_PRINT_MONITOR"></span><span id="error_invalid_print_monitor"></span>**ERROR\_INVALID\_PRINT\_MONITOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-733">3007 (0xBBF)</span><span class="sxs-lookup"><span data-stu-id="2ee13-733">3007 (0xBBF)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-734">Le moniteur d’impression spécifié ne dispose pas des fonctions requises.</span><span class="sxs-lookup"><span data-stu-id="2ee13-734">The specified print monitor does not have the required functions.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-735"><span id="ERROR_PRINT_MONITOR_IN_USE"></span><span id="error_print_monitor_in_use"></span>**ERREUR \_ \_ \_ de l’analyseur d’impression en cours d' \_ utilisation**</span><span class="sxs-lookup"><span data-stu-id="2ee13-735"><span id="ERROR_PRINT_MONITOR_IN_USE"></span><span id="error_print_monitor_in_use"></span>**ERROR\_PRINT\_MONITOR\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-736">3008 (0xBC0)</span><span class="sxs-lookup"><span data-stu-id="2ee13-736">3008 (0xBC0)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-737">Le moniteur d’impression spécifié est en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="2ee13-737">The specified print monitor is currently in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-738"><span id="ERROR_PRINTER_HAS_JOBS_QUEUED"></span><span id="error_printer_has_jobs_queued"></span>**l' \_ imprimante Error \_ a des travaux en \_ \_ file d’attente**</span><span class="sxs-lookup"><span data-stu-id="2ee13-738"><span id="ERROR_PRINTER_HAS_JOBS_QUEUED"></span><span id="error_printer_has_jobs_queued"></span>**ERROR\_PRINTER\_HAS\_JOBS\_QUEUED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-739">3009 (0xBC1)</span><span class="sxs-lookup"><span data-stu-id="2ee13-739">3009 (0xBC1)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-740">L’opération demandée n’est pas autorisée lorsque des travaux sont en file d’attente sur l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="2ee13-740">The requested operation is not allowed when there are jobs queued to the printer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-741"><span id="ERROR_SUCCESS_REBOOT_REQUIRED"></span><span id="error_success_reboot_required"></span>**ERREUR \_ de \_ redémarrage de la réussite \_ obligatoire**</span><span class="sxs-lookup"><span data-stu-id="2ee13-741"><span id="ERROR_SUCCESS_REBOOT_REQUIRED"></span><span id="error_success_reboot_required"></span>**ERROR\_SUCCESS\_REBOOT\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-742">3010 (0xBC2)</span><span class="sxs-lookup"><span data-stu-id="2ee13-742">3010 (0xBC2)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-743">L’opération demandée est réussie.</span><span class="sxs-lookup"><span data-stu-id="2ee13-743">The requested operation is successful.</span></span> <span data-ttu-id="2ee13-744">Les modifications ne seront effectives qu’après le redémarrage du système.</span><span class="sxs-lookup"><span data-stu-id="2ee13-744">Changes will not be effective until the system is rebooted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-745"><span id="ERROR_SUCCESS_RESTART_REQUIRED"></span><span id="error_success_restart_required"></span>**ERREUR \_ de \_ redémarrage de la réussite \_ requise**</span><span class="sxs-lookup"><span data-stu-id="2ee13-745"><span id="ERROR_SUCCESS_RESTART_REQUIRED"></span><span id="error_success_restart_required"></span>**ERROR\_SUCCESS\_RESTART\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-746">3011 (0xBC3)</span><span class="sxs-lookup"><span data-stu-id="2ee13-746">3011 (0xBC3)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-747">L’opération demandée est réussie.</span><span class="sxs-lookup"><span data-stu-id="2ee13-747">The requested operation is successful.</span></span> <span data-ttu-id="2ee13-748">Les modifications ne sont pas effectives tant que le service n’est pas redémarré.</span><span class="sxs-lookup"><span data-stu-id="2ee13-748">Changes will not be effective until the service is restarted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-749"><span id="ERROR_PRINTER_NOT_FOUND"></span><span id="error_printer_not_found"></span>**ERREUR \_ imprimante \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="2ee13-749"><span id="ERROR_PRINTER_NOT_FOUND"></span><span id="error_printer_not_found"></span>**ERROR\_PRINTER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-750">3012 (0xBC4)</span><span class="sxs-lookup"><span data-stu-id="2ee13-750">3012 (0xBC4)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-751">Aucune imprimante n’a été trouvée.</span><span class="sxs-lookup"><span data-stu-id="2ee13-751">No printers were found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-752"><span id="ERROR_PRINTER_DRIVER_WARNED"></span><span id="error_printer_driver_warned"></span>**ERREUR \_ de \_ pilote d’imprimante \_**</span><span class="sxs-lookup"><span data-stu-id="2ee13-752"><span id="ERROR_PRINTER_DRIVER_WARNED"></span><span id="error_printer_driver_warned"></span>**ERROR\_PRINTER\_DRIVER\_WARNED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-753">3013 (0xBC5)</span><span class="sxs-lookup"><span data-stu-id="2ee13-753">3013 (0xBC5)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-754">Le pilote d’imprimante est réputé non fiable.</span><span class="sxs-lookup"><span data-stu-id="2ee13-754">The printer driver is known to be unreliable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-755"><span id="ERROR_PRINTER_DRIVER_BLOCKED"></span><span id="error_printer_driver_blocked"></span>**ERREUR \_ de \_ pilote d’imprimante \_ bloquée**</span><span class="sxs-lookup"><span data-stu-id="2ee13-755"><span id="ERROR_PRINTER_DRIVER_BLOCKED"></span><span id="error_printer_driver_blocked"></span>**ERROR\_PRINTER\_DRIVER\_BLOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-756">3014 (0xBC6)</span><span class="sxs-lookup"><span data-stu-id="2ee13-756">3014 (0xBC6)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-757">Le pilote d’imprimante est connu pour endommager le système.</span><span class="sxs-lookup"><span data-stu-id="2ee13-757">The printer driver is known to harm the system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-758"><span id="ERROR_PRINTER_DRIVER_PACKAGE_IN_USE"></span><span id="error_printer_driver_package_in_use"></span>**ERREUR \_ \_ \_ \_ de package de pilotes d’imprimante en cours d' \_ utilisation**</span><span class="sxs-lookup"><span data-stu-id="2ee13-758"><span id="ERROR_PRINTER_DRIVER_PACKAGE_IN_USE"></span><span id="error_printer_driver_package_in_use"></span>**ERROR\_PRINTER\_DRIVER\_PACKAGE\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-759">3015 (0xBC7)</span><span class="sxs-lookup"><span data-stu-id="2ee13-759">3015 (0xBC7)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-760">Le package de pilotes d’imprimante spécifié est en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="2ee13-760">The specified printer driver package is currently in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-761"><span id="ERROR_CORE_DRIVER_PACKAGE_NOT_FOUND"></span><span id="error_core_driver_package_not_found"></span>**PACKAGE de pilotes d’erreur \_ Core \_ \_ \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="2ee13-761"><span id="ERROR_CORE_DRIVER_PACKAGE_NOT_FOUND"></span><span id="error_core_driver_package_not_found"></span>**ERROR\_CORE\_DRIVER\_PACKAGE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-762">3016 (0xBC8)</span><span class="sxs-lookup"><span data-stu-id="2ee13-762">3016 (0xBC8)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-763">Impossible de trouver un package de pilotes principal requis par le package de pilotes d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="2ee13-763">Unable to find a core driver package that is required by the printer driver package.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-764"><span id="ERROR_FAIL_REBOOT_REQUIRED"></span><span id="error_fail_reboot_required"></span>**ERREUR d' \_ échec de \_ redémarrage \_ requis**</span><span class="sxs-lookup"><span data-stu-id="2ee13-764"><span id="ERROR_FAIL_REBOOT_REQUIRED"></span><span id="error_fail_reboot_required"></span>**ERROR\_FAIL\_REBOOT\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-765">3017 (0xBC9)</span><span class="sxs-lookup"><span data-stu-id="2ee13-765">3017 (0xBC9)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-766">L'opération demandée a échoué.</span><span class="sxs-lookup"><span data-stu-id="2ee13-766">The requested operation failed.</span></span> <span data-ttu-id="2ee13-767">Un redémarrage système est nécessaire pour restaurer les modifications apportées.</span><span class="sxs-lookup"><span data-stu-id="2ee13-767">A system reboot is required to roll back changes made.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-768"><span id="ERROR_FAIL_REBOOT_INITIATED"></span><span id="error_fail_reboot_initiated"></span>**ERREUR lors de l' \_ échec du \_ redémarrage \_**</span><span class="sxs-lookup"><span data-stu-id="2ee13-768"><span id="ERROR_FAIL_REBOOT_INITIATED"></span><span id="error_fail_reboot_initiated"></span>**ERROR\_FAIL\_REBOOT\_INITIATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-769">3018 (0xBCA)</span><span class="sxs-lookup"><span data-stu-id="2ee13-769">3018 (0xBCA)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-770">L'opération demandée a échoué.</span><span class="sxs-lookup"><span data-stu-id="2ee13-770">The requested operation failed.</span></span> <span data-ttu-id="2ee13-771">Un redémarrage système a été initié pour restaurer les modifications apportées.</span><span class="sxs-lookup"><span data-stu-id="2ee13-771">A system reboot has been initiated to roll back changes made.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-772"><span id="ERROR_PRINTER_DRIVER_DOWNLOAD_NEEDED"></span><span id="error_printer_driver_download_needed"></span>**ERREUR lors du téléchargement du pilote d' \_ imprimante \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2ee13-772"><span id="ERROR_PRINTER_DRIVER_DOWNLOAD_NEEDED"></span><span id="error_printer_driver_download_needed"></span>**ERROR\_PRINTER\_DRIVER\_DOWNLOAD\_NEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-773">3019 (0xBCB)</span><span class="sxs-lookup"><span data-stu-id="2ee13-773">3019 (0xBCB)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-774">Le pilote d’imprimante spécifié est introuvable sur le système et doit être téléchargé.</span><span class="sxs-lookup"><span data-stu-id="2ee13-774">The specified printer driver was not found on the system and needs to be downloaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-775"><span id="ERROR_PRINT_JOB_RESTART_REQUIRED"></span><span id="error_print_job_restart_required"></span>**ERREUR \_ de \_ redémarrage du travail d’impression \_ \_ requis**</span><span class="sxs-lookup"><span data-stu-id="2ee13-775"><span id="ERROR_PRINT_JOB_RESTART_REQUIRED"></span><span id="error_print_job_restart_required"></span>**ERROR\_PRINT\_JOB\_RESTART\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-776">3020 (0xBCC)</span><span class="sxs-lookup"><span data-stu-id="2ee13-776">3020 (0xBCC)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-777">L’impression du travail d’impression demandé a échoué.</span><span class="sxs-lookup"><span data-stu-id="2ee13-777">The requested print job has failed to print.</span></span> <span data-ttu-id="2ee13-778">Une mise à jour du système d’impression exige que le travail soit renvoyé.</span><span class="sxs-lookup"><span data-stu-id="2ee13-778">A print system update requires the job to be resubmitted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-779"><span id="ERROR_INVALID_PRINTER_DRIVER_MANIFEST"></span><span id="error_invalid_printer_driver_manifest"></span>**ERREUR \_ du \_ \_ manifeste du pilote d’imprimante non valide \_**</span><span class="sxs-lookup"><span data-stu-id="2ee13-779"><span id="ERROR_INVALID_PRINTER_DRIVER_MANIFEST"></span><span id="error_invalid_printer_driver_manifest"></span>**ERROR\_INVALID\_PRINTER\_DRIVER\_MANIFEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-780">3021 (0xBCD)</span><span class="sxs-lookup"><span data-stu-id="2ee13-780">3021 (0xBCD)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-781">Le pilote d’imprimante ne contient pas de manifeste valide ou contient un trop grand nombre de manifestes.</span><span class="sxs-lookup"><span data-stu-id="2ee13-781">The printer driver does not contain a valid manifest, or contains too many manifests.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-782"><span id="ERROR_PRINTER_NOT_SHAREABLE"></span><span id="error_printer_not_shareable"></span>**ERREUR de partage de l' \_ imprimante \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2ee13-782"><span id="ERROR_PRINTER_NOT_SHAREABLE"></span><span id="error_printer_not_shareable"></span>**ERROR\_PRINTER\_NOT\_SHAREABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-783">3022 (0xBCE)</span><span class="sxs-lookup"><span data-stu-id="2ee13-783">3022 (0xBCE)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-784">Impossible de partager l’imprimante spécifiée.</span><span class="sxs-lookup"><span data-stu-id="2ee13-784">The specified printer cannot be shared.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-785"><span id="ERROR_REQUEST_PAUSED"></span><span id="error_request_paused"></span>**demande d’erreur \_ \_ suspendue**</span><span class="sxs-lookup"><span data-stu-id="2ee13-785"><span id="ERROR_REQUEST_PAUSED"></span><span id="error_request_paused"></span>**ERROR\_REQUEST\_PAUSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-786">3050 (0xBEA)</span><span class="sxs-lookup"><span data-stu-id="2ee13-786">3050 (0xBEA)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-787">L’opération a été suspendue.</span><span class="sxs-lookup"><span data-stu-id="2ee13-787">The operation was paused.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2ee13-788"><span id="ERROR_IO_REISSUE_AS_CACHED"></span><span id="error_io_reissue_as_cached"></span>**ERREUR \_ de RÉémission d’e/s \_ \_ \_ mise en cache**</span><span class="sxs-lookup"><span data-stu-id="2ee13-788"><span id="ERROR_IO_REISSUE_AS_CACHED"></span><span id="error_io_reissue_as_cached"></span>**ERROR\_IO\_REISSUE\_AS\_CACHED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ee13-789">3950 (0xF6E)</span><span class="sxs-lookup"><span data-stu-id="2ee13-789">3950 (0xF6E)</span></span>
</dt> <dt>



<span data-ttu-id="2ee13-790">Réémettez l’opération donnée en tant qu’opération d’e/s mise en cache.</span><span class="sxs-lookup"><span data-stu-id="2ee13-790">Reissue the given operation as a cached IO operation.</span></span>


</dt> </dl> </dd> </dl>


## <a name="requirements"></a><span data-ttu-id="2ee13-791">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2ee13-791">Requirements</span></span>



| <span data-ttu-id="2ee13-792">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2ee13-792">Requirement</span></span> | <span data-ttu-id="2ee13-793">Valeur</span><span class="sxs-lookup"><span data-stu-id="2ee13-793">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2ee13-794">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2ee13-794">Minimum supported client</span></span><br/> | <span data-ttu-id="2ee13-795">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2ee13-795">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="2ee13-796">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2ee13-796">Minimum supported server</span></span><br/> | <span data-ttu-id="2ee13-797">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2ee13-797">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2ee13-798">En-tête</span><span class="sxs-lookup"><span data-stu-id="2ee13-798">Header</span></span><br/>                   | <dl> <span data-ttu-id="2ee13-799"><dt>WinError. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ee13-799"><dt>WinError.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ee13-800">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2ee13-800">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ee13-801">Codes d’erreur système</span><span class="sxs-lookup"><span data-stu-id="2ee13-801">System Error Codes</span></span>](system-error-codes.md)
</dt> </dl>

 

 




