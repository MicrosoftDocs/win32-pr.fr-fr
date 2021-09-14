---
title: Utilisation de Services Bureau à distance canaux virtuels
description: Pour implémenter un canal virtuel, vous fournissez les modules serveur et client de l’application d’un canal virtuel.
ms.assetid: 3b378071-ebd6-47b0-8a9c-3e671505011a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 539eafca38c19855fdb057ceeb6e79cb4613773a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127217385"
---
# <a name="using-remote-desktop-services-virtual-channels"></a>Utilisation de Services Bureau à distance canaux virtuels

Pour implémenter un canal virtuel, vous fournissez les modules serveur et client de l’application d’un canal virtuel. Le module de serveur peut être une application en mode utilisateur ou un pilote en mode noyau. Le module client doit être une DLL.

Pour obtenir une description de ces modules, consultez les rubriques suivantes.

## <a name="in-this-section"></a>Dans cette section

<dl> <dt>

[Application de serveur de canal virtuel](virtual-channel-server-application.md)
</dt> <dd>

Le module de serveur d’une application qui utilise des canaux virtuels doit être une application en mode utilisateur s’exécutant dans une session cliente sur le serveur hôte de session Bureau à distance (hôte de session Bureau à distance). Notez que vous devez fournir une méthode pour démarrer l’application serveur.

</dd> <dt>

[DLL du client du canal virtuel](virtual-channel-client-dll.md)
</dt> <dd>

Le client d’une application de canaux virtuels est une DLL qui est chargée pendant l’initialisation Services Bureau à distance sur l’ordinateur client. La DLL doit être inscrite sur l’ordinateur client.

</dd> <dt>

[Inscription du client du canal virtuel](virtual-channel-client-registration.md)
</dt> <dd>

Vous devez stocker le nom de la DLL cliente dans le registre.

</dd> <dt>

[Canaux virtuels persistants de contrôle à distance](remote-control-persistent-virtual-channels.md)
</dt> <dd>

Un canal virtuel persistant de contrôle à distance n’est pas fermé lorsqu’un contrôle à distance se connecte ou se déconnecte pour la session connectée au client. Les données continueront à être transmises et reçues via ce canal.

</dd> <dt>

[Canaux virtuels dynamiques](dynamic-virtual-channels.md)
</dt> <dd>

Les API de canal virtuel dynamique (DVC) étendent les API de canal virtuel existantes pour Services Bureau à distance, appelées API de canal virtuel statique (SVC).

</dd> </dl>

si vous avez activé l’application d’un canal virtuel dans votre déploiement Services Bureau à distance, vous pouvez également mettre l’application à la disposition des ordinateurs clients qui accèdent au serveur hôte de Session bureau à distance à l’aide du contrôle Bureau à distance ActiveX. pour plus d’informations, consultez [utilisation du contrôle Bureau à distance ActiveX avec des canaux virtuels](using-the-remote-desktop-activex-control-with-virtual-channels.md).

 

 




