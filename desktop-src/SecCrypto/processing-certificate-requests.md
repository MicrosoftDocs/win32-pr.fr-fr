---
description: Explique comment les services de certificats traitent les demandes de certificat.
ms.assetid: 40641167-12de-4008-80e4-2fb758146421
title: Traitement des demandes de certificat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5be2c8e8acacbb001803cf3ce8d7e1263e920673eb912a04105ec8bb2772953a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117977402"
---
# <a name="processing-certificate-requests"></a>Traitement des demandes de certificat

Les services de certificats effectuent les étapes suivantes lors du traitement d’une [*demande de certificat*](../secgloss/c-gly.md):

1.  Réception de la demande.

    La [*demande de certificat*](../secgloss/c-gly.md) est envoyée par le client à une application intermédiaire, qui la formate dans une \# demande de format PKCS 10 et l’envoie au moteur serveur.

2.  Approbation de la demande.

    Le moteur de serveur appelle le [module de stratégie](policy-modules.md), qui interroge les propriétés de demande, détermine si la demande est autorisée ou non, et définit les propriétés de certificat facultatives.

3.  La formation des certificats.

    Si la demande est approuvée, le moteur de serveur prend la demande, ainsi que toutes les propriétés demandées par le module de stratégie, et crée un certificat complet.

4.  Publication du certificat.

    Le moteur du serveur stocke le certificat terminé dans la base de données des services de certificats et notifie l’application intermédiaire de l’état de la demande. Si le [module de sortie](exit-modules.md) l’a demandé, le moteur du serveur l’avertit d’un événement d’émission de certificat. Cela permet au module de sortie d’effectuer d’autres opérations, telles que la publication du certificat sur un référentiel de certificats externe (par exemple, un service d’annuaire). Pendant ce temps, l’intermédiaire récupère le certificat publié auprès des services de certificats et le transmet au client.

L’illustration suivante montre comment une [*demande de certificat*](../secgloss/c-gly.md) est traitée par les services de certificats.

![traitement d’une demande de certificat](images/certflow.png)

 

 
