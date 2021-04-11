---
description: La propriété AuthenticationLevel est un entier qui définit le niveau d’authentification COM affecté à cet objet.
ms.assetid: 96c2e6a5-a91f-469d-bdd1-eaa20b176158
ms.tgt_platform: multiple
title: SWbemSecurity. AuthenticationLevel, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSecurity.AuthenticationLevel
- ISWbemSecurity.AuthenticationLevel
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 63ae9e529de010e0a0ca7b8bc1da7dc8dc4891b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318861"
---
# <a name="swbemsecurityauthenticationlevel-property"></a><span data-ttu-id="e93a5-103">SWbemSecurity. AuthenticationLevel, propriété</span><span class="sxs-lookup"><span data-stu-id="e93a5-103">SWbemSecurity.AuthenticationLevel property</span></span>

<span data-ttu-id="e93a5-104">La propriété **AuthenticationLevel** est un entier qui définit le niveau d’authentification com affecté à cet objet.</span><span class="sxs-lookup"><span data-stu-id="e93a5-104">The **AuthenticationLevel** property is an integer that defines the COM Authentication level that is assigned to this object.</span></span> <span data-ttu-id="e93a5-105">Ce paramètre détermine la façon dont vous protégez les informations envoyées à partir de WMI.</span><span class="sxs-lookup"><span data-stu-id="e93a5-105">This setting determines how you protect information sent from WMI.</span></span> <span data-ttu-id="e93a5-106">Pour plus d’informations sur les niveaux d’authentification, consultez Définition de la [ \_ sécurité des \_ processus de l’application cliente](setting-client-application-process-security.md).</span><span class="sxs-lookup"><span data-stu-id="e93a5-106">For more information about authentication levels, see [Setting Client\_Application\_Process Security](setting-client-application-process-security.md).</span></span> <span data-ttu-id="e93a5-107">En général, il n’est pas nécessaire de définir le niveau d’authentification lors de l’exécution d’appels d’API WMI.</span><span class="sxs-lookup"><span data-stu-id="e93a5-107">In general, it is not necessary to set the authentication level when making WMI API calls.</span></span> <span data-ttu-id="e93a5-108">Si vous ne définissez pas cette propriété, le niveau d’authentification COM par défaut de votre système est utilisé.</span><span class="sxs-lookup"><span data-stu-id="e93a5-108">If you do not set this property, the default COM Authentication level for your system is used.</span></span>

<span data-ttu-id="e93a5-109">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="e93a5-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="e93a5-110">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="e93a5-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e93a5-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e93a5-111">Syntax</span></span>


```VB
SWbemSecurity.AuthenticationLevel As Integer
```



## <a name="property-value"></a><span data-ttu-id="e93a5-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="e93a5-112">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="e93a5-113">Notes</span><span class="sxs-lookup"><span data-stu-id="e93a5-113">Remarks</span></span>

<span data-ttu-id="e93a5-114">Le paramètre authenticationLevel vous permet de demander le niveau d’authentification et de confidentialité DCOM à utiliser au cours d’une connexion.</span><span class="sxs-lookup"><span data-stu-id="e93a5-114">The authenticationLevel setting enables you to request the level of DCOM authentication and privacy to be used throughout a connection.</span></span> <span data-ttu-id="e93a5-115">Les paramètres sont compris entre aucune authentification et authentification chiffrée par paquet.</span><span class="sxs-lookup"><span data-stu-id="e93a5-115">Settings range from no authentication to per-packet encrypted authentication.</span></span>



| <span data-ttu-id="e93a5-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="e93a5-116">Value</span></span>        | <span data-ttu-id="e93a5-117">Description</span><span class="sxs-lookup"><span data-stu-id="e93a5-117">Description</span></span>                                                                                                                                                                                                                                                                                                            |
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e93a5-118">Aucune</span><span class="sxs-lookup"><span data-stu-id="e93a5-118">None</span></span>         | <span data-ttu-id="e93a5-119">N’utilise pas d’authentification.</span><span class="sxs-lookup"><span data-stu-id="e93a5-119">Does not use any authentication.</span></span> <span data-ttu-id="e93a5-120">Tous les paramètres de sécurité sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="e93a5-120">All security settings are ignored.</span></span><br/>                                                                                                                                                                                                                                         |
| <span data-ttu-id="e93a5-121">Default</span><span class="sxs-lookup"><span data-stu-id="e93a5-121">Default</span></span>      | <span data-ttu-id="e93a5-122">Utilise une négociation de sécurité standard pour sélectionner un niveau d’authentification.</span><span class="sxs-lookup"><span data-stu-id="e93a5-122">Uses a standard security negotiation to select an authentication level.</span></span> <span data-ttu-id="e93a5-123">Il s’agit du paramètre recommandé, car le client impliqué dans la transaction sera négocié au niveau d’authentification spécifié par le serveur.</span><span class="sxs-lookup"><span data-stu-id="e93a5-123">This is the recommended setting because the client involved in the transaction will be negotiated to the authentication level specified by the server.</span></span><br/> <span data-ttu-id="e93a5-124">DCOM ne sélectionne pas la valeur aucun au cours d’une session de négociation.</span><span class="sxs-lookup"><span data-stu-id="e93a5-124">DCOM will not select the value None during a negotiation session.</span></span><br/> |
| <span data-ttu-id="e93a5-125">Se connecter</span><span class="sxs-lookup"><span data-stu-id="e93a5-125">Connect</span></span>      | <span data-ttu-id="e93a5-126">Authentifie les informations d’identification du client uniquement lorsque le client tente de se connecter au serveur.</span><span class="sxs-lookup"><span data-stu-id="e93a5-126">Authenticates the credentials of the client only when the client tries to connect to the server.</span></span> <span data-ttu-id="e93a5-127">Une fois la connexion établie, aucune vérification d’authentification supplémentaire n’a lieu.</span><span class="sxs-lookup"><span data-stu-id="e93a5-127">After a connection has been made, no additional authentication checks take place.</span></span><br/>                                                                                                                          |
| <span data-ttu-id="e93a5-128">Appeler</span><span class="sxs-lookup"><span data-stu-id="e93a5-128">Call</span></span>         | <span data-ttu-id="e93a5-129">Authentifie les informations d’identification du client uniquement au début de chaque appel, lorsque le serveur reçoit la demande.</span><span class="sxs-lookup"><span data-stu-id="e93a5-129">Authenticates the credentials of the client only at the beginning of each call, when the server receives the request.</span></span> <span data-ttu-id="e93a5-130">Les en-têtes de paquets sont signés, mais les paquets de données échangés entre le client et le serveur ne sont ni signés ni chiffrés.</span><span class="sxs-lookup"><span data-stu-id="e93a5-130">The packet headers are signed, but the data packets exchanged between the client and the server are neither signed nor encrypted.</span></span><br/>                                                     |
| <span data-ttu-id="e93a5-131">PKT</span><span class="sxs-lookup"><span data-stu-id="e93a5-131">Pkt</span></span>          | <span data-ttu-id="e93a5-132">Authentifie que tous les paquets de données sont reçus du client attendu.</span><span class="sxs-lookup"><span data-stu-id="e93a5-132">Authenticates that all data packets are received from the expected client.</span></span> <span data-ttu-id="e93a5-133">Semblable à Call ; les en-têtes de paquets sont signés, mais pas chiffrés.</span><span class="sxs-lookup"><span data-stu-id="e93a5-133">Similar to Call; packet headers are signed but not encrypted.</span></span> <span data-ttu-id="e93a5-134">Les paquets eux-mêmes ne sont ni signés ni chiffrés.</span><span class="sxs-lookup"><span data-stu-id="e93a5-134">Packets themselves are neither signed nor encrypted.</span></span><br/>                                                                                                               |
| <span data-ttu-id="e93a5-135">PktIntegrity</span><span class="sxs-lookup"><span data-stu-id="e93a5-135">PktIntegrity</span></span> | <span data-ttu-id="e93a5-136">Authentifie et vérifie qu’aucun des paquets de données transférés entre le client et le serveur n’a été modifié.</span><span class="sxs-lookup"><span data-stu-id="e93a5-136">Authenticates and verifies that none of the data packets transferred between the client and the server have been modified.</span></span> <span data-ttu-id="e93a5-137">Chaque paquet de données est signé, ce qui garantit que les paquets n’ont pas été modifiés pendant le transit.</span><span class="sxs-lookup"><span data-stu-id="e93a5-137">Every data packet is signed, ensuring that the packets have not been modified during transit.</span></span> <span data-ttu-id="e93a5-138">Aucun des paquets de données n’est chiffré.</span><span class="sxs-lookup"><span data-stu-id="e93a5-138">None of the data packets are encrypted.</span></span><br/>                                            |
| <span data-ttu-id="e93a5-139">PktPrivacy</span><span class="sxs-lookup"><span data-stu-id="e93a5-139">PktPrivacy</span></span>   | <span data-ttu-id="e93a5-140">Authentifie tous les niveaux et signes d’emprunt d’identité précédents et chiffre chaque paquet de données.</span><span class="sxs-lookup"><span data-stu-id="e93a5-140">Authenticates all previous impersonation levels and signs and encrypts each data packet.</span></span> <span data-ttu-id="e93a5-141">Cela garantit que toutes les communications entre le client et le serveur sont confidentielles.</span><span class="sxs-lookup"><span data-stu-id="e93a5-141">This ensures that all communication between the client and the server is confidential.</span></span><br/>                                                                                                                             |



 

<span data-ttu-id="e93a5-142">Vous pouvez définir le niveau d’authentification des objets [**SWbemServices**](swbemservices.md), [**SWbemObject**](swbemobject.md), [**SWbemObjectSet**](swbemobjectset.md), [**SWbemObjectPath**](swbemobjectpath.md)et [**SwbemLocator**](swbemlocator.md) en affectant à la propriété **AuthenticationLevel** la valeur souhaitée.</span><span class="sxs-lookup"><span data-stu-id="e93a5-142">You can set the authentication level of the [**SWbemServices**](swbemservices.md), [**SWbemObject**](swbemobject.md), [**SWbemObjectSet**](swbemobjectset.md), [**SWbemObjectPath**](swbemobjectpath.md), and [**SwbemLocator**](swbemlocator.md) objects by setting the **AuthenticationLevel** property to the desired value.</span></span>

<span data-ttu-id="e93a5-143">L’exemple suivant montre comment définir le niveau d’authentification pour un objet **SwbemObject** .</span><span class="sxs-lookup"><span data-stu-id="e93a5-143">The following example shows how to set the authentication level for an **SwbemObject** object.</span></span>


```VB
objinstance.Security_.AuthenticationLevel = wbemAuthenticationLevelPkt
```



<span data-ttu-id="e93a5-144">Vous pouvez également spécifier des niveaux d’authentification dans le cadre d’un moniker.</span><span class="sxs-lookup"><span data-stu-id="e93a5-144">You can also specify authentication levels as part of a moniker.</span></span> <span data-ttu-id="e93a5-145">L’exemple suivant définit le niveau d’authentification et le niveau d’emprunt d’identité, et récupère une instance [**de \_ disque logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk).</span><span class="sxs-lookup"><span data-stu-id="e93a5-145">The following example sets the authentication level and the impersonation level, and retrieves an instance of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk).</span></span>


```VB
Set objinst = GetObject("WinMgmts:{impersonationLevel=impersonate,authenticationLevel=pktPrivacy}!root/cimv2:Win32_LogicalDisk='c:'")
```



## <a name="requirements"></a><span data-ttu-id="e93a5-146">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e93a5-146">Requirements</span></span>



| <span data-ttu-id="e93a5-147">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e93a5-147">Requirement</span></span> | <span data-ttu-id="e93a5-148">Valeur</span><span class="sxs-lookup"><span data-stu-id="e93a5-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e93a5-149">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e93a5-149">Minimum supported client</span></span><br/> | <span data-ttu-id="e93a5-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e93a5-150">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e93a5-151">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e93a5-151">Minimum supported server</span></span><br/> | <span data-ttu-id="e93a5-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e93a5-152">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e93a5-153">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="e93a5-153">Type library</span></span><br/>             | <dl> <span data-ttu-id="e93a5-154"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e93a5-154"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e93a5-155">DLL</span><span class="sxs-lookup"><span data-stu-id="e93a5-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e93a5-156"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e93a5-156"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="e93a5-157">CLSID</span><span class="sxs-lookup"><span data-stu-id="e93a5-157">CLSID</span></span><br/>                    | <span data-ttu-id="e93a5-158">CLSID \_ SWbemSecurity</span><span class="sxs-lookup"><span data-stu-id="e93a5-158">CLSID\_SWbemSecurity</span></span><br/>                                                         |
| <span data-ttu-id="e93a5-159">IID</span><span class="sxs-lookup"><span data-stu-id="e93a5-159">IID</span></span><br/>                      | <span data-ttu-id="e93a5-160">IID \_ ISWbemSecurity</span><span class="sxs-lookup"><span data-stu-id="e93a5-160">IID\_ISWbemSecurity</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="e93a5-161">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e93a5-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e93a5-162">Définition de la sécurité des processus d' \_ application cliente \_</span><span class="sxs-lookup"><span data-stu-id="e93a5-162">Setting Client\_Application\_Process Security</span></span>](setting-client-application-process-security.md)
</dt> <dt>

[<span data-ttu-id="e93a5-163">**WbemAuthenticationLevelEnum**</span><span class="sxs-lookup"><span data-stu-id="e93a5-163">**WbemAuthenticationLevelEnum**</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)
</dt> <dt>

[<span data-ttu-id="e93a5-164">**SWbemSecurity**</span><span class="sxs-lookup"><span data-stu-id="e93a5-164">**SWbemSecurity**</span></span>](swbemsecurity.md)
</dt> </dl>

 

