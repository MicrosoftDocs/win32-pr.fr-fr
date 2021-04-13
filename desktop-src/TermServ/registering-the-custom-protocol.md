---
title: Inscription du gestionnaire de protocole
description: Vous devez créer au moins une entrée de valeur de Registre pour votre gestionnaire de protocole afin que le service Services Bureau à distance puisse l’instancier.
ms.assetid: 4cc7197b-88f3-4906-9b59-66587f970e2a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0193440414c1b95b741b6e1f0257d8d1aa3e00b9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379762"
---
# <a name="registering-the-protocol-manager"></a><span data-ttu-id="1ba9f-103">Inscription du gestionnaire de protocole</span><span class="sxs-lookup"><span data-stu-id="1ba9f-103">Registering the Protocol Manager</span></span>

<span data-ttu-id="1ba9f-104">Vous devez créer au moins une entrée de valeur de Registre pour votre gestionnaire de protocole afin que le service Services Bureau à distance puisse l’instancier.</span><span class="sxs-lookup"><span data-stu-id="1ba9f-104">You must create at least one registry value entry for your protocol manager so that the Remote Desktop Services service can instantiate it.</span></span>

## <a name="registry-location"></a><span data-ttu-id="1ba9f-105">Emplacement du registre</span><span class="sxs-lookup"><span data-stu-id="1ba9f-105">Registry Location</span></span>

<span data-ttu-id="1ba9f-106">Créez une clé de Registre à l’emplacement suivant pour chaque écouteur ([**IWRdsProtocolListener**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistener)) que votre protocole utilise.</span><span class="sxs-lookup"><span data-stu-id="1ba9f-106">Create a registry key in the following location for each listener ([**IWRdsProtocolListener**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistener)) that your protocol uses.</span></span> <span data-ttu-id="1ba9f-107">Dans cet exemple, les nouvelles clés d’écouteur sont appelées *MyListener1* et *MyListener2*.</span><span class="sxs-lookup"><span data-stu-id="1ba9f-107">In this example, the new listener keys are called *MyListener1* and *MyListener2*.</span></span>

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Control
            Terminal Server
               WinStations
                  RDP-Tcp
                  MyListener1
                  MyListener2
```

<span data-ttu-id="1ba9f-108">Pour référence, vous pouvez afficher les entrées de valeur sous la clé de l’écouteur **RDP-TCP** par défaut à cet emplacement.</span><span class="sxs-lookup"><span data-stu-id="1ba9f-108">For reference, you can view the value entries under the default **RDP-Tcp** listener key in this location.</span></span>

## <a name="registry-value-entries"></a><span data-ttu-id="1ba9f-109">Entrées de la valeur de Registre</span><span class="sxs-lookup"><span data-stu-id="1ba9f-109">Registry Value Entries</span></span>

<span data-ttu-id="1ba9f-110">La clé de l’écouteur pour le protocole doit avoir une entrée de valeur nommée **\_ objet LoadableProtocol**</span><span class="sxs-lookup"><span data-stu-id="1ba9f-110">The listener key for the protocol must have a value entry called **LoadableProtocol\_Object**</span></span><dl> <dt>

<span data-ttu-id="1ba9f-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="1ba9f-111">Data type</span></span>
</dt> <dd><span data-ttu-id="1ba9f-112">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="1ba9f-112">REG_SZ</span></span></dd> <span data-ttu-id="1ba9f-113">Interface </dl> of type **REG\_SZ** that contains the CLSID of the protocol manager for that listener. (The protocol manager is a COM server that implements the <a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolmanager">**IWRdsProtocolManager**</a> .) Le service Services Bureau à distance utilise ce CLSID pour instancier le gestionnaire de protocole de cet écouteur après avoir trouvé l’écouteur dans le registre.</span><span class="sxs-lookup"><span data-stu-id="1ba9f-113"></dl> of type **REG\_SZ** that contains the CLSID of the protocol manager for that listener. (The protocol manager is a COM server that implements the <a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolmanager">**IWRdsProtocolManager**</a> interface.) The Remote Desktop Services service uses this CLSID to instantiate the protocol manager for this listener after it finds the listener in the registry.</span></span>

<span data-ttu-id="1ba9f-114">Si votre fournisseur de protocole utilise plus d’un écouteur, le service Services Bureau à distance crée une seule instance du gestionnaire de protocole et l’utilise pour appeler [**createListener**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-createlistener) une fois pour chaque écouteur.</span><span class="sxs-lookup"><span data-stu-id="1ba9f-114">If your protocol provider uses more than one listener, the Remote Desktop Services service only creates one instance of the protocol manager, and uses it to call [**CreateListener**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-createlistener) once for each listener.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1ba9f-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1ba9f-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1ba9f-116">Création d’un fournisseur de protocole RDP (Remote Desktop Protocol)</span><span class="sxs-lookup"><span data-stu-id="1ba9f-116">Creating a Remote Desktop Protocol Provider</span></span>](creating-a-custom-remote-protocol.md)
</dt> <dt>

[<span data-ttu-id="1ba9f-117">Séquence d’appel de méthode</span><span class="sxs-lookup"><span data-stu-id="1ba9f-117">Method Call Sequence</span></span>](method-call-sequence.md)
</dt> </dl>

 

 




