---
description: Une approbation doit exister entre le destinataire d’un message signé et le signataire du message.
ms.assetid: 770e4674-8896-4062-a93a-a17bd30a9129
title: Vérification de l’approbation du certificat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b711e0a86dcc5ae9cdedea278d6a3a698dfd633
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106531729"
---
# <a name="certificate-trust-verification"></a>Vérification de l’approbation du certificat

Une approbation doit exister entre le destinataire d’un message signé et le signataire du message. Une méthode pour établir cette approbation consiste à utiliser un [*certificat*](../secgloss/c-gly.md), un document électronique qui vérifie que les entités ou les personnes sont bien celles qu’ils revendiquent. Un certificat est émis pour une entité par un tiers qui est approuvé par les deux autres parties. Ainsi, chaque destinataire d’un message signé décide si l’émetteur du certificat du signataire est digne de confiance. [*CryptoAPI*](../secgloss/c-gly.md) a implémenté une méthodologie pour permettre aux développeurs d’applications de créer des applications qui vérifient automatiquement les certificats par rapport à une liste prédéfinie de certificats ou de [*racines*](../secgloss/r-gly.md)de confiance. Cette liste d’entités approuvées (appelées sujets) est appelée liste de certificats de confiance (CTL, [*Certificate Trust List*](../secgloss/c-gly.md) ).

L’exemple suivant d’utilisation d’une liste de certificats de confiance implique un administrateur intranet (réseau intra-entreprise) qui souhaite contrôler uniquement les sources externes approuvées. Dans ce cas, l’administrateur peut créer une liste de certificats ou de racines approuvés, le signer et mettre la liste à la disposition de tous les clients sur le réseau sous la forme d’une liste CTL. Une application conçue pour utiliser cette fonctionnalité CryptoAPI accepte alors uniquement les messages signés ou les logiciels téléchargés qui ont été signés par les entités de la liste.

Pour obtenir la liste de ces fonctions, consultez [fonctions de vérification des certificats](cryptography-functions.md).

 

 
