---
title: Interfaces du fournisseur protocole RDP (Remote Desktop Protocol)
description: Interfaces prises en charge par l’API du fournisseur protocole RDP (Remote Desktop Protocol).
ms.assetid: 180c29d4-a305-45ac-8989-6226dccb75d5
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85494e26c391095fbf97e8e408ee6b6181756c03
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939552"
---
# <a name="remote-desktop-protocol-provider-interfaces"></a>Interfaces du fournisseur protocole RDP (Remote Desktop Protocol)

Les interfaces suivantes sont prises en charge par l’API du fournisseur protocole RDP (Remote Desktop Protocol).

## <a name="in-this-section"></a>Dans cette section

<dl> <dt>

[**IWRdsProtocolConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnection)
</dt> <dd>

Expose les méthodes appelées par le service Services Bureau à distance pour configurer une connexion cliente.

</dd> <dt>

[**IWRdsProtocolConnectionCallback**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnectioncallback)
</dt> <dd>

Expose des méthodes qui fournissent des informations sur l’état d’une connexion cliente et qui effectuent des actions pour le client. Cette interface est implémentée par le service Services Bureau à distance et appelée par le protocole.

</dd> <dt>

[**IWRdsProtocolLicenseConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollicenseconnection)
</dt> <dd>

Expose les méthodes utilisées par le service Services Bureau à distance pour exécuter le protocole de transfert de licences pendant une séquence de connexion.

</dd> <dt>

[**IWRdsProtocolListener**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistener)
</dt> <dd>

Expose des méthodes qui demandent que le protocole démarre et cesse d’écouter les demandes de connexion clientes.

</dd> <dt>

[**IWRdsProtocolListenerCallback**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistenercallback)
</dt> <dd>

Expose des méthodes qui informent le service Services Bureau à distance qu’un client s’est connecté.

</dd> <dt>

[**IWRdsProtocolLogonErrorRedirector**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollogonerrorredirector)
</dt> <dd>

Expose les méthodes appelées par le service Services Bureau à distance pour mettre à jour l’état de l’ouverture de session et déterminer comment diriger les messages d’erreur d’ouverture de session.

</dd> <dt>

[**IWRdsProtocolManager**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolmanager)
</dt> <dd>

Expose les méthodes que le service Services Bureau à distance utilise pour communiquer avec le fournisseur de protocole.

</dd> <dt>

[**IWRdsProtocolSettings**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolsettings)
</dt> <dd>

Expose des méthodes pour récupérer et ajouter des paramètres liés à la stratégie.

</dd> <dt>

[**IWRdsProtocolShadowCallback**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolshadowcallback)
</dt> <dd>

Expose les méthodes appelées par le protocole pour notifier au service Services Bureau à distance de démarrer ou d’arrêter le côté cible d’une ombre.

</dd> <dt>

[**IWRdsProtocolShadowConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolshadowconnection)
</dt> <dd>

Expose des méthodes qui informent le fournisseur de protocole de l’état de l’occultation de session.

</dd> <dt>

[**IWRdsRemoteFXGraphicsConnection**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsremotefxgraphicsconnection)
</dt> <dd>

Expose des méthodes relatives à la manipulation et à la compréhension des graphiques sur la connexion cliente.

</dd> <dt>

[Interfaces du fournisseur de protocole Desktop déconseillées](deprecated-desktop-protocol-provider-interfaces.md)
</dt> <dd>

Les interfaces suivantes sont déconseillées et ne doivent plus être utilisées. Pour les nouveaux projets, utilisez à la place les interfaces des interfaces du fournisseur protocole RDP (Remote Desktop Protocol).

</dd> </dl>

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence du fournisseur protocole RDP (Remote Desktop Protocol)](custom-remote-protocol-reference.md)
</dt> <dt>

[Énumérations du fournisseur protocole RDP (Remote Desktop Protocol)](custom-remote-protocol-enumerations.md)
</dt> <dt>

[Structures du fournisseur protocole RDP (Remote Desktop Protocol)](custom-remote-protocol-structures.md)
</dt> <dt>

[Unions de fournisseurs protocole RDP (Remote Desktop Protocol)](custom-remote-protocol-unions.md)
</dt> </dl>

 

 




