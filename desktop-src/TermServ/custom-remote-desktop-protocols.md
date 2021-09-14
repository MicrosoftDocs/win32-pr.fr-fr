---
title: API du fournisseur protocole RDP (Remote Desktop Protocol)
description: Vous utilisez l’API du fournisseur protocole RDP (Remote Desktop Protocol) pour créer un protocole pour assurer la communication entre le service Services Bureau à distance et plusieurs clients.
ms.assetid: dd14c569-195e-460e-a1c3-2a74d0f49ff5
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95aed1c6866f3078c3761ad8ec631ef23b43a9ae
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013366"
---
# <a name="remote-desktop-protocol-provider-api"></a>API du fournisseur protocole RDP (Remote Desktop Protocol)

Vous utilisez l’API du fournisseur protocole RDP (Remote Desktop Protocol) pour créer un protocole pour assurer la communication entre le service Services Bureau à distance et plusieurs clients.

lors du chargement d’Windows serveur, le service Services Bureau à distance (également appelé gestionnaire de connexion à distance (RCM)) démarre. Le service démarre également les objets d’écouteur pour les fournisseurs de protocole RDP (Remote Desktop Protocol) qui, à leur tour, écoutent les connexions clientes. Le service et les fournisseurs de protocole sont des objets en mode utilisateur qui communiquent à l’aide des API abordées dans cette documentation. Les fournisseurs de protocole peuvent communiquer avec les pilotes en mode noyau en utilisant des contrôles d’entrée/sortie (IOCTL). L'illustration ci-dessous décrit cela.

![architecture de l’API de protocole personnalisé](images/protocol-architecture.png)

Microsoft a implémenté le protocole RDP (Remote Desktop Protocol) (RDP) pour assurer la communication entre le service Services Bureau à distance et les connexions clientes. Vous pouvez créer votre propre protocole à l’aide des interfaces, structures, unions et types d’énumération qui composent l’API du fournisseur protocole RDP (Remote Desktop Protocol). Pour plus d’informations, voir les rubriques suivantes :

<dl> <dt>

[Création d’un fournisseur de protocole RDP (Remote Desktop Protocol)](creating-a-custom-remote-protocol.md)
</dt> <dd>

Informations sur la création d’un fournisseur de protocole RDP (Remote Desktop Protocol). Le gestionnaire de protocole est implémenté en tant que serveur COM et enregistré dans un emplacement où le service Services Bureau à distance démarre.

</dd> <dt>

[Référence du fournisseur protocole RDP (Remote Desktop Protocol)](custom-remote-protocol-reference.md)
</dt> <dd>

Contient des interfaces, des structures, des unions et des types énumération qui vous permettent de créer un protocole RDP (Remote Desktop Protocol) personnalisé (RDP).

</dd> </dl>

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos de Services Bureau à distance](about-terminal-services.md)
</dt> </dl>

 

 




