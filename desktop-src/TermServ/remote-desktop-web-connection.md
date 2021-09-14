---
title: Connexion Bureau à distance par le Web
description: Connexion Bureau à distance par le Web est une application Web composée d’un contrôle ActiveX et d’un exemple de page de connexion.
ms.assetid: f9d252b0-205a-47df-9eca-d5744c09e079
ms.tgt_platform: multiple
keywords:
- Connexion Bureau à distance par le Web Services Bureau à distance
- Services Bureau à distance protocole RDP (Remote Desktop Protocol) (RDP), Connexion Bureau à distance par le Web vue d’ensemble
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41bb1e8f562e3e5c47c6050f550fe3c7090446be
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127324625"
---
# <a name="remote-desktop-web-connection"></a>Connexion Bureau à distance par le Web

Connexion Bureau à distance par le Web est une application Web composée d’un contrôle ActiveX et d’un exemple de page de connexion. Lorsque vous déployez des Connexion Bureau à distance par le Web sur un serveur Web, vous pouvez fournir une connectivité client aux serveurs Bureau à distance hôte de session (hôte de session Bureau à distance) et à d’autres ordinateurs à l’aide d’Internet Explorer et de TCP/IP.

## <a name="in-this-section"></a>Dans cette section

<dl> <dt>

[Configuration requise pour Connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md)
</dt> <dd>

Répertorie la configuration requise pour un Connexion Bureau à distance par le Web.

</dd> <dt>

[Canaux virtuels scriptables](scriptable-virtual-channels.md)
</dt> <dd>

Décrit les modifications apportées au modèle de programmation pour l’implémentation d’applications de canal virtuel fournies par les services Terminal Server client avancé (TSAC).

</dd> </dl>

La documentation de référence de Connexion Bureau à distance par le Web est incluse dans la section [référence de connexion Bureau à distance par le Web](remote-desktop-web-connection-reference.md) .

Pour plus d’informations, consultez les rubriques suivantes :

-   [Implémentation de canaux virtuels scriptables à l’aide de Connexion Bureau à distance par le Web](implementing-scriptable-virtual-channels-using-remote-desktop-web-connection.md)
-   [incorporation du contrôle Bureau à distance ActiveX dans une page web](embedding-the-remote-desktop-activex-control-in-a-web-page.md)
-   [téléchargement et utilisation du contrôle Bureau à distance ActiveX](/previous-versions//aa380808(v=vs.85))
-   [utilisation du contrôle Bureau à distance ActiveX avec des canaux virtuels](using-the-remote-desktop-activex-control-with-virtual-channels.md)
-   [Fournir la sécurité du client RDP](providing-for-rdp-client-security.md)
-   [Désactivation des fonctionnalités de Services Bureau à distance](disabling-terminal-services-features.md)

## <a name="installing-remote-desktop-web-connection"></a>Installation de Connexion Bureau à distance par le Web

les étapes suivantes installent les Bureau à distance ActiveX contrôle et l’exemple de page web dans le répertoire% systemroot% \\ Web \\ Tsweb. Ils partagent la page Web dans le répertoire TSWeb sur votre serveur, par exemple, sur https://*MyServer*/TSWeb. Le contrôle (msrdp. ocx) et le code Connexion Bureau à distance par le Web se trouvent dans Msrdp.cab.

**Pour installer Connexion Bureau à distance par le Web**

1.  dans l’élément ajout/suppression de programmes du panneau de configuration, sous ajout/suppression de Windows composants, installez Microsoft Internet Information Services (IIS).
2.  Installez le sous-composant World Wide Web service d’IIS.
3.  Installez le sous-composant Connexion Bureau à distance par le Web du service World Wide Web.

pour obtenir une description de la page web qui est incluse dans l’installation de Connexion Bureau à distance par le Web, consultez [exemple de page web inclus avec le contrôle ActiveX Bureau à distance](sample-web-page-included-with-the-remote-desktop-activex-control.md).

 

 