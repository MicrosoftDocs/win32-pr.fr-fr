---
title: DCOMSCMRemoteCallFlags
description: Contrôle le comportement des appels du gestionnaire de contrôle des services DCOM local (DCOMSCM) à un DCOMSCM distant.
ms.assetid: fb306da7-4b9a-4386-8525-7f78bd6bf728
keywords:
- Valeur de Registre DCOMSCMRemoteCallFlags COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fda58975e40ac6ac1633db8aa78f2c7636f9103
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104031912"
---
# <a name="dcomscmremotecallflags"></a><span data-ttu-id="b8aca-104">DCOMSCMRemoteCallFlags</span><span class="sxs-lookup"><span data-stu-id="b8aca-104">DCOMSCMRemoteCallFlags</span></span>

<span data-ttu-id="b8aca-105">Contrôle le comportement des appels du gestionnaire de contrôle des services DCOM local (DCOMSCM) à un DCOMSCM distant.</span><span class="sxs-lookup"><span data-stu-id="b8aca-105">Controls the behavior of calls from the local DCOM Service Control Manager (DCOMSCM) to a remote DCOMSCM.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="b8aca-106">Entrée de Registre</span><span class="sxs-lookup"><span data-stu-id="b8aca-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   DCOMSCMRemoteCallFlags = value
```

## <a name="remarks"></a><span data-ttu-id="b8aca-107">Notes</span><span class="sxs-lookup"><span data-stu-id="b8aca-107">Remarks</span></span>

<span data-ttu-id="b8aca-108">Il s’agit d’une valeur de **Registre \_ DWORD** .</span><span class="sxs-lookup"><span data-stu-id="b8aca-108">This is a **REG\_DWORD** value.</span></span>



| <span data-ttu-id="b8aca-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="b8aca-109">Value</span></span> | <span data-ttu-id="b8aca-110">Description</span><span class="sxs-lookup"><span data-stu-id="b8aca-110">Description</span></span>                                       |
|-------|---------------------------------------------------|
| <span data-ttu-id="b8aca-111">0x1</span><span class="sxs-lookup"><span data-stu-id="b8aca-111">0x1</span></span>   | <span data-ttu-id="b8aca-112">**DCOMSCM \_ Activation \_ utiliser \_ tous les \_ AUTHNSERVICES**</span><span class="sxs-lookup"><span data-stu-id="b8aca-112">**DCOMSCM\_ACTIVATION\_USE\_ALL\_AUTHNSERVICES**</span></span>  |
| <span data-ttu-id="b8aca-113">0x2</span><span class="sxs-lookup"><span data-stu-id="b8aca-113">0x2</span></span>   | <span data-ttu-id="b8aca-114">**DCOMSCM \_ Activation \_ interdire un \_ appel non sécurisé \_**</span><span class="sxs-lookup"><span data-stu-id="b8aca-114">**DCOMSCM\_ACTIVATION\_DISALLOW\_UNSECURE\_CALL**</span></span> |
| <span data-ttu-id="b8aca-115">0x4</span><span class="sxs-lookup"><span data-stu-id="b8aca-115">0x4</span></span>   | <span data-ttu-id="b8aca-116">**DCOMSCM \_ résoudre \_ utiliser \_ tous les \_ AUTHNSERVICES**</span><span class="sxs-lookup"><span data-stu-id="b8aca-116">**DCOMSCM\_RESOLVE\_USE\_ALL\_AUTHNSERVICES**</span></span>     |
| <span data-ttu-id="b8aca-117">0x8</span><span class="sxs-lookup"><span data-stu-id="b8aca-117">0x8</span></span>   | <span data-ttu-id="b8aca-118">**DCOMSCM \_ résoudre \_ interdire un \_ appel non sécurisé \_**</span><span class="sxs-lookup"><span data-stu-id="b8aca-118">**DCOMSCM\_RESOLVE\_DISALLOW\_UNSECURE\_CALL**</span></span>    |
| <span data-ttu-id="b8aca-119">0x10</span><span class="sxs-lookup"><span data-stu-id="b8aca-119">0x10</span></span>  | <span data-ttu-id="b8aca-120">**DCOMSCM \_ ping \_ utiliser \_ Mid \_ AUTHNSERVICE**</span><span class="sxs-lookup"><span data-stu-id="b8aca-120">**DCOMSCM\_PING\_USE\_MID\_AUTHNSERVICE**</span></span>         |



 

## <a name="dcomscm_activation_use_all_authnservices-description"></a><span data-ttu-id="b8aca-121">DCOMSCM \_ Activation \_ utiliser \_ toutes les \_ AUTHNSERVICES Description</span><span class="sxs-lookup"><span data-stu-id="b8aca-121">DCOMSCM\_ACTIVATION\_USE\_ALL\_AUTHNSERVICES Description</span></span>

<span data-ttu-id="b8aca-122">Lorsque le client émet une demande d’activation qui utilise les paramètres de sécurité par défaut, le DCOMSCM local utilise le service d’authentification Negotiate lors de l’appel RPC d’activation au DCOMSCM distant.</span><span class="sxs-lookup"><span data-stu-id="b8aca-122">When the client issues an activation request that uses the default security settings, the local DCOMSCM uses the Negotiate authentication service when making the activation RPC call to the remote DCOMSCM.</span></span> <span data-ttu-id="b8aca-123">Si l’appel échoue, le DCOMSCM local effectue l’appel RPC d’activation en l’absence de sécurité.</span><span class="sxs-lookup"><span data-stu-id="b8aca-123">If the call fails, the local DCOMSCM makes the activation RPC call using no security.</span></span>

<span data-ttu-id="b8aca-124">**Windows Server 2003 et Windows XP/2000 :** Si l’appel RPC d’activation qui utilise le service Negotiate Authentication échoue, le DCOMSCM local effectue l’appel RPC d’activation à l’aide de Kerberos, NTLM ou d’autres fournisseurs de sécurité configurés.</span><span class="sxs-lookup"><span data-stu-id="b8aca-124">**Windows Server 2003 and Windows XP/2000:** If the activation RPC call that uses the Negotiate authentication service fails, the local DCOMSCM makes the activation RPC call using Kerberos, NTLM, or other configured security providers.</span></span> <span data-ttu-id="b8aca-125">Si aucun fournisseur de sécurité ne fonctionne, le DCOMSCM local effectue l’appel RPC d’activation en l’absence de sécurité.</span><span class="sxs-lookup"><span data-stu-id="b8aca-125">If no security providers work, the local DCOMSCM makes the activation RPC call using no security.</span></span>

<span data-ttu-id="b8aca-126">En définissant cet indicateur, les DCOMSCM locaux sur Windows Vista ou version ultérieure peuvent être configurés pour se comporter comme des systèmes antérieurs à Vista.</span><span class="sxs-lookup"><span data-stu-id="b8aca-126">By setting this flag, the local DCOMSCM on Windows Vista or higher can be made to behave like pre-Vista systems.</span></span> <span data-ttu-id="b8aca-127">Il n’est pas recommandé de définir cet indicateur, sauf s’il est requis pour des raisons de compatibilité.</span><span class="sxs-lookup"><span data-stu-id="b8aca-127">It is not recommended to set this flag unless required for compatibility reasons.</span></span>

## <a name="dcomscm_activation_disallow_unsecure_call-description"></a><span data-ttu-id="b8aca-128">DCOMSCM \_ Activation \_ interdire la description de l' \_ appel non sécurisé \_</span><span class="sxs-lookup"><span data-stu-id="b8aca-128">DCOMSCM\_ACTIVATION\_DISALLOW\_UNSECURE\_CALL Description</span></span>

<span data-ttu-id="b8aca-129">Si la valeur de l’indicateur d' **\_ \_ \_ \_ appel non sécurisé** de l’activation de DCOMSCM est définie, le DCOMSCM local n’effectue pas d’appel RPC d’activation non sécurisé.</span><span class="sxs-lookup"><span data-stu-id="b8aca-129">If the **DCOMSCM\_ACTIVATION\_DISALLOW\_UNSECURE\_CALL** flag is set, the local DCOMSCM does not make an unsecure activation RPC call.</span></span> <span data-ttu-id="b8aca-130">Pour permettre aux clients d’effectuer des demandes d’activation avec des paramètres de sécurité autres que ceux par défaut, spécifiez la structure [**COAUTHINFO**](/windows/desktop/api/wtypesbase/ns-wtypesbase-coauthinfo) lors de la demande d’activation.</span><span class="sxs-lookup"><span data-stu-id="b8aca-130">To enable clients to make activation requests with non-default security settings, specify the [**COAUTHINFO**](/windows/desktop/api/wtypesbase/ns-wtypesbase-coauthinfo) structure when making the activation request.</span></span> <span data-ttu-id="b8aca-131">Dans ce cas, l' **activation de DCOMSCM \_ \_ utilise \_ tous les \_** indicateurs d' **\_ Activation \_ \_ non sécurisés \_** AUTHNSERVICES et DCOMSCM sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="b8aca-131">In this case, the **DCOMSCM\_ACTIVATION\_USE\_ALL\_AUTHNSERVICES** and **DCOMSCM\_ACTIVATION\_DISALLOW\_UNSECURE\_CALL** flags are ignored.</span></span>

<span data-ttu-id="b8aca-132">Il n’est pas recommandé de définir cet indicateur, sauf si tous les clients et serveurs du réseau sont entièrement authentifiés.</span><span class="sxs-lookup"><span data-stu-id="b8aca-132">It is not recommended to set this flag unless all the clients and servers in the network are fully authenticated.</span></span>

## <a name="dcomscm_resolve_use_all_authnservices-description"></a><span data-ttu-id="b8aca-133">DCOMSCM \_ résoudre \_ utiliser \_ toutes les \_ AUTHNSERVICES Description</span><span class="sxs-lookup"><span data-stu-id="b8aca-133">DCOMSCM\_RESOLVE\_USE\_ALL\_AUTHNSERVICES Description</span></span>

<span data-ttu-id="b8aca-134">Lorsque le client démarshale une référence d’objet, le DCOMSCM local utilise le service d’authentification Negotiate lors de l’appel RPC de résolution OXID au DCOMSCM distant.</span><span class="sxs-lookup"><span data-stu-id="b8aca-134">When the client unmarshals an object reference, the local DCOMSCM uses the Negotiate authentication service when making the OXID Resolution RPC call to the remote DCOMSCM.</span></span> <span data-ttu-id="b8aca-135">Si l’appel échoue, le DCOMSCM local effectue l’appel RPC de résolution OXID à l’aide d’aucune sécurité.</span><span class="sxs-lookup"><span data-stu-id="b8aca-135">If the call fails, the local DCOMSCM makes the OXID Resolution RPC call using no security.</span></span>

<span data-ttu-id="b8aca-136">**Windows Server 2003 et Windows XP/2000 :** Si l’appel RPC de résolution OXID à l’aide du service d’authentification Negotiate échoue, le DCOMSCM local effectue l’appel RPC de résolution OXID à l’aide de Kerberos, NTLM ou d’autres fournisseurs de sécurité configurés.</span><span class="sxs-lookup"><span data-stu-id="b8aca-136">**Windows Server 2003 and Windows XP/2000:** If the OXID Resolution RPC call using the Negotiate authentication service fails, the local DCOMSCM makes the OXID Resolution RPC call by using Kerberos, NTLM, or other configured security providers.</span></span> <span data-ttu-id="b8aca-137">Si aucun fournisseur de sécurité ne fonctionne, le DCOMSCM local effectue l’appel RPC de résolution OXID à l’aide d’aucune sécurité.</span><span class="sxs-lookup"><span data-stu-id="b8aca-137">If no security providers work, then the local DCOMSCM makes the OXID Resolution RPC call using no security.</span></span>

<span data-ttu-id="b8aca-138">En définissant cet indicateur, les DCOMSCM locaux sur Windows Vista ou version ultérieure peuvent être configurés pour se comporter comme des systèmes antérieurs à Vista.</span><span class="sxs-lookup"><span data-stu-id="b8aca-138">By setting this flag, the local DCOMSCM on Windows Vista or higher can be made to behave like pre-Vista systems.</span></span> <span data-ttu-id="b8aca-139">Il n’est pas recommandé de définir cet indicateur, sauf s’il est requis pour des raisons de compatibilité.</span><span class="sxs-lookup"><span data-stu-id="b8aca-139">It is not recommended to set this flag unless required for compatibility reasons.</span></span>

## <a name="dcomscm_resolve_disallow_unsecure_call-description"></a><span data-ttu-id="b8aca-140">DCOMSCM \_ résoudre \_ interdire la description de l' \_ appel non sécurisé \_</span><span class="sxs-lookup"><span data-stu-id="b8aca-140">DCOMSCM\_RESOLVE\_DISALLOW\_UNSECURE\_CALL Description</span></span>

<span data-ttu-id="b8aca-141">Si l’indicateur **DCOMSCM \_ résoudre l’interdiction d' \_ \_ \_ appel non sécurisé** est défini, le DCOMSCM local n’effectue pas d’appel RPC de résolution de Oxid non sécurisé.</span><span class="sxs-lookup"><span data-stu-id="b8aca-141">If the **DCOMSCM\_RESOLVE\_DISALLOW\_UNSECURE\_CALL** flag is set, the local DCOMSCM does not make an unsecure OXID Resolution RPC call.</span></span> <span data-ttu-id="b8aca-142">En outre, le DCOMSCM local n’effectue pas un appel RPC garbage collection ping non sécurisé.</span><span class="sxs-lookup"><span data-stu-id="b8aca-142">In addition, the local DCOMSCM does not make an unsecure garbage collection Ping RPC call.</span></span> <span data-ttu-id="b8aca-143">Il n’est pas recommandé de définir cet indicateur, sauf si tous les clients et serveurs du réseau sont entièrement authentifiés.</span><span class="sxs-lookup"><span data-stu-id="b8aca-143">It is not recommended to set this flag unless all the clients and servers in the network are fully authenticated.</span></span>

## <a name="dcomscm_ping_use_mid_authnservice-description"></a><span data-ttu-id="b8aca-144">DCOMSCM \_ ping \_ use \_ Mid \_ AUTHNSERVICE Description</span><span class="sxs-lookup"><span data-stu-id="b8aca-144">DCOMSCM\_PING\_USE\_MID\_AUTHNSERVICE Description</span></span>

<span data-ttu-id="b8aca-145">Le DCOMSCM local utilise le service d’authentification Negotiate lors du test ping de l’appel RPC de garbage collection vers le DCOMSCM distant.</span><span class="sxs-lookup"><span data-stu-id="b8aca-145">The local DCOMSCM uses the Negotiate authentication service when making the garbage-collection Ping RPC call to the remote DCOMSCM.</span></span> <span data-ttu-id="b8aca-146">En cas d’échec de l’appel, le DCOMSCM local effectue l’appel RPC ping de garbage collection sans sécurité.</span><span class="sxs-lookup"><span data-stu-id="b8aca-146">If the call fails, the local DCOMSCM makes the garbage-collection Ping RPC call using no security.</span></span>

<span data-ttu-id="b8aca-147">**Windows Server 2003 et Windows XP/2000 :** En cas d’échec de l’appel RPC ping de garbage collection à l’aide du service Negotiate Authentication, le DCOMSCM local effectue l’appel RPC ping garbage collection à l’aide de Kerberos, NTLM et d’autres fournisseurs de sécurité configurés.</span><span class="sxs-lookup"><span data-stu-id="b8aca-147">**Windows Server 2003 and Windows XP/2000:** If the garbage-collection Ping RPC call using the Negotiate authentication service fails, the local DCOMSCM makes the garbage collection Ping RPC call by using Kerberos, NTLM, and other configured security providers.</span></span> <span data-ttu-id="b8aca-148">Si aucun fournisseur de sécurité ne fonctionne, le DCOMSCM local effectue l’appel RPC ping garbage collection à l’aide d’aucune sécurité.</span><span class="sxs-lookup"><span data-stu-id="b8aca-148">If no security providers work, then the local DCOMSCM makes the garbage collection Ping RPC call using no security.</span></span>

<span data-ttu-id="b8aca-149">En définissant cet indicateur, les DCOMSCM locaux sur Windows Vista ou version ultérieure peuvent être configurés pour se comporter comme des systèmes antérieurs à Vista.</span><span class="sxs-lookup"><span data-stu-id="b8aca-149">By setting this flag, the local DCOMSCM on Windows Vista or above can be made to behave like pre-Vista systems.</span></span> <span data-ttu-id="b8aca-150">Il n’est pas recommandé de définir l’indicateur **\_ ping DCOMSCM \_ use \_ Mid \_ AUTHNSERVICE** , sauf s’il est requis pour des raisons de compatibilité.</span><span class="sxs-lookup"><span data-stu-id="b8aca-150">It is not recommended to set the **DCOMSCM\_PING\_USE\_MID\_AUTHNSERVICE** flag unless required for compatibility reasons.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b8aca-151">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b8aca-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b8aca-152">Authentification des connexions à distance</span><span class="sxs-lookup"><span data-stu-id="b8aca-152">Authentication for Remote Connections</span></span>](/windows/desktop/WinRM/authentication-for-remote-connections)
</dt> <dt>

[<span data-ttu-id="b8aca-153">EnableDCOM</span><span class="sxs-lookup"><span data-stu-id="b8aca-153">EnableDCOM</span></span>](enabledcom.md)
</dt> <dt>

[<span data-ttu-id="b8aca-154">Inscription des serveurs COM</span><span class="sxs-lookup"><span data-stu-id="b8aca-154">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> <dt>

[<span data-ttu-id="b8aca-155">Sécurité dans COM</span><span class="sxs-lookup"><span data-stu-id="b8aca-155">Security in COM</span></span>](security-in-com.md)
</dt> </dl>

 

 