---
title: Détection de la prise en charge du protocole WS-Management par un ordinateur distant
description: Vous pouvez utiliser les méthodes session. identify ou IWSManSession. identify pour déterminer si l’ordinateur distant dispose d’un service qui prend en charge le protocole WS-Management.
ms.assetid: 4d11ac02-fa8b-45d7-bceb-a18f561bc928
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af82284b38b2a101c767766d44eb975ff7e1dadc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106511429"
---
# <a name="detecting-whether-a-remote-computer-supports-ws-management-protocol"></a><span data-ttu-id="440be-103">Détection de la prise en charge du protocole WS-Management par un ordinateur distant</span><span class="sxs-lookup"><span data-stu-id="440be-103">Detecting Whether a Remote Computer Supports WS-Management Protocol</span></span>

<span data-ttu-id="440be-104">Vous pouvez utiliser les méthodes [**session. identify**](session-identify.md) ou [**IWSManSession. identify**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-identify) pour déterminer si l’ordinateur distant dispose d’un service qui prend en charge le protocole WS-Management.</span><span class="sxs-lookup"><span data-stu-id="440be-104">You can use the [**Session.Identify**](session-identify.md) or [**IWSManSession.Identify**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-identify) methods to determine if the remote computer has a service that supports the WS-Management protocol.</span></span>

<span data-ttu-id="440be-105">Si un service de protocole WS-Management est configuré sur l’ordinateur distant et est à l’écoute des demandes, le service peut détecter une demande d’identification à l’aide du code XML suivant dans l’en-tête.</span><span class="sxs-lookup"><span data-stu-id="440be-105">If a WS-Management protocol service is configured on the remote computer and is listening for requests, the service can detect an Identify request by the following XML in the header.</span></span>


```XML
xmlns:wsmid="https://schemas.dmtf.org/wbem/wsman/identity/1/wsmanidentity"
```



<span data-ttu-id="440be-106">Le service de protocole WS-Management qui reçoit la demande retourne les informations contenues dans la liste suivante, dans le corps du message :</span><span class="sxs-lookup"><span data-stu-id="440be-106">The WS-Management protocol service that receives the request returns the information, contained in the following list, in the body of the message:</span></span>

-   <span data-ttu-id="440be-107">Version du protocole WS-Management.</span><span class="sxs-lookup"><span data-stu-id="440be-107">The WS-Management protocol version.</span></span> <span data-ttu-id="440be-108">par exemple, « https://schemas.dmtf.org/wbem/wsman/1/wsman ».</span><span class="sxs-lookup"><span data-stu-id="440be-108">For example, "https://schemas.dmtf.org/wbem/wsman/1/wsman".</span></span>
-   <span data-ttu-id="440be-109">Le fournisseur du produit, par exemple, « Microsoft Corporation ».</span><span class="sxs-lookup"><span data-stu-id="440be-109">The product vendor, for example, "Microsoft Corporation".</span></span>
-   <span data-ttu-id="440be-110">Version du produit.</span><span class="sxs-lookup"><span data-stu-id="440be-110">The product version.</span></span> <span data-ttu-id="440be-111">Si la demande est envoyée avec **WSManFlagUseNoAuthentication** dans le paramètre *Flags* , aucune information sur la version du produit n’est retournée.</span><span class="sxs-lookup"><span data-stu-id="440be-111">If the request is sent with **WSManFlagUseNoAuthentication** in the *flags* parameter, then no product version information is returned.</span></span> <span data-ttu-id="440be-112">Si la demande est envoyée avec l’authentification par défaut en vigueur ou avec un autre mode d’authentification spécifié, les informations de version du produit peuvent être retournées.</span><span class="sxs-lookup"><span data-stu-id="440be-112">If the request is sent with either the default authentication in effect or with another authentication mode specified, then the product version information can be returned.</span></span>

<span data-ttu-id="440be-113">La demande pour détecter si l’ordinateur distant dispose d’un service de protocole WS-Management et à l’écoute peut être exécutée au début d’un script avec d’autres opérations.</span><span class="sxs-lookup"><span data-stu-id="440be-113">The request to detect whether the remote computer has a configured and listening WS-Management protocol service can be performed at the beginning of a script with other operations.</span></span> <span data-ttu-id="440be-114">Cela permet de vérifier que les ordinateurs cibles peuvent répondre à d’autres demandes de protocole WS-Management.</span><span class="sxs-lookup"><span data-stu-id="440be-114">This will verify that the target computer or computers can respond to further WS-Management protocol requests.</span></span> <span data-ttu-id="440be-115">La vérification peut également être effectuée dans un script distinct.</span><span class="sxs-lookup"><span data-stu-id="440be-115">The verification also can be done in a separate script.</span></span>

<span data-ttu-id="440be-116">**Pour détecter un service de protocole WS-Management**</span><span class="sxs-lookup"><span data-stu-id="440be-116">**To detect a WS-Management protocol service**</span></span>

1.  <span data-ttu-id="440be-117">Créez un objet [**WSMan**](wsman.md) .</span><span class="sxs-lookup"><span data-stu-id="440be-117">Create a [**WSMan**](wsman.md) object.</span></span>

    ```VB
    Set objWsman = CreateObject("Wsman.Automation")
    ```

    

2.  <span data-ttu-id="440be-118">Déterminez si la demande doit être envoyée ou non authentifiée et définissez le paramètre *Flags* en conséquence dans l’appel à [**WSMan. CreateSession**](wsman-createsession.md).</span><span class="sxs-lookup"><span data-stu-id="440be-118">Determine whether the request should be sent authenticated or unauthenticated and set the *flags* parameter accordingly in the call to [**WSMan.CreateSession**](wsman-createsession.md).</span></span>

    ```VB
    set objSession = objWsman.CreateSession("Remote1", _
       objWsman.SessionFlagUseNoAuthentication)
    ```

    

3.  <span data-ttu-id="440be-119">Appelez [**session. identifier**](session-identify.md).</span><span class="sxs-lookup"><span data-stu-id="440be-119">Call [**Session.Identify**](session-identify.md).</span></span>

    ```VB
    objSession.Identify
    ```

    

## <a name="examples"></a><span data-ttu-id="440be-120">Exemples</span><span class="sxs-lookup"><span data-stu-id="440be-120">Examples</span></span>

<span data-ttu-id="440be-121">L’exemple de code VBScript suivant envoie une demande d’identification non authentifiée à l’ordinateur distant nommé « remote1 » dans le même domaine.</span><span class="sxs-lookup"><span data-stu-id="440be-121">The following VBScript code example sends an unauthenticated Identify request to the remote computer named "Remote1" in the same domain.</span></span>


```VB
set objWsman = CreateObject("Wsman.Automation")
set objSession = objWsman.CreateSession("Remote1", _
  objWsman.SessionFlagUseNoAuthentication)
WScript.Echo objSession.Identify
```



<span data-ttu-id="440be-122">La réponse suivante affiche le code XML renvoyé par l’ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="440be-122">The following response shows the XML returned by the remote computer.</span></span> <span data-ttu-id="440be-123">La version de protocole WS-Management (« https://schemas.dmtf.org/wbem/wsman/1/wsman.xsd ») et le fournisseur de système d’exploitation (« Microsoft Corporation ») sont spécifiés dans le code XML renvoyé.</span><span class="sxs-lookup"><span data-stu-id="440be-123">The WS-Management protocol version ("https://schemas.dmtf.org/wbem/wsman/1/wsman.xsd") and the operating system vendor ("Microsoft Corporation") are specified in the returned XML.</span></span> <span data-ttu-id="440be-124">Étant donné que le message est envoyé sans être authentifié, la version du produit n’est pas retournée par le service Windows Remote Management.</span><span class="sxs-lookup"><span data-stu-id="440be-124">Because the message is sent unauthenticated, the product version is not returned by the Windows Remote Management service.</span></span>


```XML
<wsmid:IdentifyResponse xmlns:wsmid=
    "https://schemas.dmtf.org/wbem/wsman/identity/1/wsmanidentity.xsd">
<wsmid:ProtocolVersion>https://schemas.dmtf.org/wbem/wsman/1/wsman.xsd
    </wsmid:ProtocolVersion>
<wsmid:ProductVendor>Microsoft Corporation</wsmid:ProductVendor>
<wsmid:ProductVersion>OS: 0.0.0 SP: 0.0 Stack:1.0</wsmid:ProductVersion>
</wsmid:IdentifyResponse>
```



<span data-ttu-id="440be-125">L’exemple de code VBScript suivant envoie une demande d’identification authentifiée à l’ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="440be-125">The following VBScript code example sends an authenticated Identify request to the remote computer.</span></span>


```VB
set ObjWSMan = CreateObject("Wsman.Automation")
set objSession = WSMan.CreateSession("Remote1", _
  objWSMan.SessionFlagUseKerberos)
WScript.Echo objSession.Identify
```



<span data-ttu-id="440be-126">Étant donné que la demande a été envoyée avec l’authentification, les informations de version sont retournées.</span><span class="sxs-lookup"><span data-stu-id="440be-126">Because the request was sent with authentication, the version information is returned.</span></span>


```XML
<wsmid:IdentifyResponse xmlns:wsmid=
    "https://schemas.dmtf.org/wbem/wsman/identity/1/wsmanidentity.xsd">
<wsmid:ProtocolVersion>https://schemas.dmtf.org/wbem/wsman/1/wsman.xsd
    </wsmid:ProtocolVersion>
<wsmid:ProductVendor>Microsoft Corporation</wsmid:ProductVendor>
<wsmid:ProductVersion>OS: 6.0.5384 SP: 0.0 Stack:1.0</wsmid:ProductVersion>
</wsmid:IdentifyResponse>
```



## <a name="related-topics"></a><span data-ttu-id="440be-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="440be-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="440be-128">À propos de Windows Remote Management</span><span class="sxs-lookup"><span data-stu-id="440be-128">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="440be-129">Utilisation de Windows Remote Management</span><span class="sxs-lookup"><span data-stu-id="440be-129">Using Windows Remote Management</span></span>](using-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="440be-130">Référence Windows Remote Management</span><span class="sxs-lookup"><span data-stu-id="440be-130">Windows Remote Management Reference</span></span>](windows-remote-management-reference.md)
</dt> </dl>

 

 




