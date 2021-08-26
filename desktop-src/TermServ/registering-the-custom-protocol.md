---
title: Inscription du gestionnaire de protocole
description: Vous devez créer au moins une entrée de valeur de Registre pour votre gestionnaire de protocole afin que le service Services Bureau à distance puisse l’instancier.
ms.assetid: 4cc7197b-88f3-4906-9b59-66587f970e2a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f851fe74d7e22a068eccd0d901cab14d754b6b2364611bfdda2aecd68dcf224d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119988789"
---
# <a name="registering-the-protocol-manager"></a>Inscription du gestionnaire de protocole

Vous devez créer au moins une entrée de valeur de Registre pour votre gestionnaire de protocole afin que le service Services Bureau à distance puisse l’instancier.

## <a name="registry-location"></a>Emplacement du registre

Créez une clé de Registre à l’emplacement suivant pour chaque écouteur ([**IWRdsProtocolListener**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistener)) que votre protocole utilise. Dans cet exemple, les nouvelles clés d’écouteur sont appelées *MyListener1* et *MyListener2*.

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

Pour référence, vous pouvez afficher les entrées de valeur sous la clé de l’écouteur **RDP-TCP** par défaut à cet emplacement.

## <a name="registry-value-entries"></a>Entrées de la valeur de Registre

La clé de l’écouteur pour le protocole doit avoir une entrée de valeur nommée **\_ objet LoadableProtocol**<dl> <dt>

Type de données
</dt> <dd>REG_SZ</dd> Interface </dl> of type **REG\_SZ** that contains the CLSID of the protocol manager for that listener. (The protocol manager is a COM server that implements the <a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolmanager">**IWRdsProtocolManager**</a> .) Le service Services Bureau à distance utilise ce CLSID pour instancier le gestionnaire de protocole de cet écouteur après avoir trouvé l’écouteur dans le registre.

Si votre fournisseur de protocole utilise plus d’un écouteur, le service Services Bureau à distance crée une seule instance du gestionnaire de protocole et l’utilise pour appeler [**createListener**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-createlistener) une fois pour chaque écouteur.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Création d’un fournisseur de protocole RDP (Remote Desktop Protocol)](creating-a-custom-remote-protocol.md)
</dt> <dt>

[Séquence d’appel de méthode](method-call-sequence.md)
</dt> </dl>

 

 




