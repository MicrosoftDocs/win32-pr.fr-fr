---
description: Arrêt d’une connexion Schannel
ms.assetid: 7081ba1f-df3c-41b4-96da-24d44e74d714
title: Arrêt d’une connexion Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc61b67083ceee65da714069c2b30ba1bfd5c89b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127193839"
---
# <a name="shutting-down-an-schannel-connection"></a>Arrêt d’une connexion Schannel

Lorsqu’un client ou un serveur se termine avec une connexion, il doit l’arrêter. L’autre partie doit, à son tour, reconnaître l’arrêt et supprimer la connexion.

**Pour arrêter une connexion Schannel**

1.  Appelez la fonction [**ApplyControlToken**](/windows/desktop/api/Sspi/nf-sspi-applycontroltoken) , en spécifiant le \_ jeton de contrôle d’arrêt Schannel.
2.  Après avoir reçu une \_ \_ valeur de retour s E OK de [**ApplyControlToken**](/windows/desktop/api/Sspi/nf-sspi-applycontroltoken), appelez la fonction [**InitializeSecurityContext (SChannel)**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) (clients) ou [**AcceptSecurityContext (SChannel)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) (serveurs), en passant dans des mémoires tampons vides.
3.  Procédez comme si votre application était en train de créer une nouvelle connexion jusqu’à ce que la fonction retourne SEC \_ I \_ Context \_ expiré ou sec \_ e \_ OK pour indiquer que la connexion est arrêtée.
4.  Envoyer les informations de sortie finales, le cas échéant, au tiers distant.
5.  Appelez [**DeleteSecurityContext**](/windows/desktop/api/Sspi/nf-sspi-deletesecuritycontext) pour libérer les ressources détenues par la connexion.

## <a name="recognizing-a-shutdown"></a>Reconnaissance d’un arrêt

La fonction [**DecryptMessage (SChannel)**](/windows/win32/api/sspi/nf-sspi-decryptmessage) retourne le \_ contexte sec I \_ \_ expiré lorsque l’expéditeur du message a arrêté la connexion. Après avoir reçu cette valeur de retour, suivez la procédure pour arrêter une connexion Schannel, plus haut dans cette rubrique.

 

 
