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
# <a name="detecting-whether-a-remote-computer-supports-ws-management-protocol"></a>Détection de la prise en charge du protocole WS-Management par un ordinateur distant

Vous pouvez utiliser les méthodes [**session. identify**](session-identify.md) ou [**IWSManSession. identify**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-identify) pour déterminer si l’ordinateur distant dispose d’un service qui prend en charge le protocole WS-Management.

Si un service de protocole WS-Management est configuré sur l’ordinateur distant et est à l’écoute des demandes, le service peut détecter une demande d’identification à l’aide du code XML suivant dans l’en-tête.


```XML
xmlns:wsmid="https://schemas.dmtf.org/wbem/wsman/identity/1/wsmanidentity"
```



Le service de protocole WS-Management qui reçoit la demande retourne les informations contenues dans la liste suivante, dans le corps du message :

-   Version du protocole WS-Management. par exemple, « https://schemas.dmtf.org/wbem/wsman/1/wsman ».
-   Le fournisseur du produit, par exemple, « Microsoft Corporation ».
-   Version du produit. Si la demande est envoyée avec **WSManFlagUseNoAuthentication** dans le paramètre *Flags* , aucune information sur la version du produit n’est retournée. Si la demande est envoyée avec l’authentification par défaut en vigueur ou avec un autre mode d’authentification spécifié, les informations de version du produit peuvent être retournées.

La demande pour détecter si l’ordinateur distant dispose d’un service de protocole WS-Management et à l’écoute peut être exécutée au début d’un script avec d’autres opérations. Cela permet de vérifier que les ordinateurs cibles peuvent répondre à d’autres demandes de protocole WS-Management. La vérification peut également être effectuée dans un script distinct.

**Pour détecter un service de protocole WS-Management**

1.  Créez un objet [**WSMan**](wsman.md) .

    ```VB
    Set objWsman = CreateObject("Wsman.Automation")
    ```

    

2.  Déterminez si la demande doit être envoyée ou non authentifiée et définissez le paramètre *Flags* en conséquence dans l’appel à [**WSMan. CreateSession**](wsman-createsession.md).

    ```VB
    set objSession = objWsman.CreateSession("Remote1", _
       objWsman.SessionFlagUseNoAuthentication)
    ```

    

3.  Appelez [**session. identifier**](session-identify.md).

    ```VB
    objSession.Identify
    ```

    

## <a name="examples"></a>Exemples

L’exemple de code VBScript suivant envoie une demande d’identification non authentifiée à l’ordinateur distant nommé « remote1 » dans le même domaine.


```VB
set objWsman = CreateObject("Wsman.Automation")
set objSession = objWsman.CreateSession("Remote1", _
  objWsman.SessionFlagUseNoAuthentication)
WScript.Echo objSession.Identify
```



La réponse suivante affiche le code XML renvoyé par l’ordinateur distant. La version de protocole WS-Management (« https://schemas.dmtf.org/wbem/wsman/1/wsman.xsd ») et le fournisseur de système d’exploitation (« Microsoft Corporation ») sont spécifiés dans le code XML renvoyé. Étant donné que le message est envoyé sans être authentifié, la version du produit n’est pas retournée par le service Windows Remote Management.


```XML
<wsmid:IdentifyResponse xmlns:wsmid=
    "https://schemas.dmtf.org/wbem/wsman/identity/1/wsmanidentity.xsd">
<wsmid:ProtocolVersion>https://schemas.dmtf.org/wbem/wsman/1/wsman.xsd
    </wsmid:ProtocolVersion>
<wsmid:ProductVendor>Microsoft Corporation</wsmid:ProductVendor>
<wsmid:ProductVersion>OS: 0.0.0 SP: 0.0 Stack:1.0</wsmid:ProductVersion>
</wsmid:IdentifyResponse>
```



L’exemple de code VBScript suivant envoie une demande d’identification authentifiée à l’ordinateur distant.


```VB
set ObjWSMan = CreateObject("Wsman.Automation")
set objSession = WSMan.CreateSession("Remote1", _
  objWSMan.SessionFlagUseKerberos)
WScript.Echo objSession.Identify
```



Étant donné que la demande a été envoyée avec l’authentification, les informations de version sont retournées.


```XML
<wsmid:IdentifyResponse xmlns:wsmid=
    "https://schemas.dmtf.org/wbem/wsman/identity/1/wsmanidentity.xsd">
<wsmid:ProtocolVersion>https://schemas.dmtf.org/wbem/wsman/1/wsman.xsd
    </wsmid:ProtocolVersion>
<wsmid:ProductVendor>Microsoft Corporation</wsmid:ProductVendor>
<wsmid:ProductVersion>OS: 6.0.5384 SP: 0.0 Stack:1.0</wsmid:ProductVersion>
</wsmid:IdentifyResponse>
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos de Windows Remote Management](about-windows-remote-management.md)
</dt> <dt>

[Utilisation de Windows Remote Management](using-windows-remote-management.md)
</dt> <dt>

[Référence Windows Remote Management](windows-remote-management-reference.md)
</dt> </dl>

 

 




