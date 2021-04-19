---
description: Un message enveloppé est un message chiffré pour un destinataire ou un ensemble de destinataires.
ms.assetid: caf86ec8-48b6-4017-95ad-7a21fcaed4cf
title: Création et réception des messages de données enveloppés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81d973ded4656966d1b61ac0ae9779acf35eb578
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515005"
---
# <a name="creating-and-receiving-enveloped-data-messages"></a><span data-ttu-id="e1410-103">Création et réception des messages de données enveloppés</span><span class="sxs-lookup"><span data-stu-id="e1410-103">Creating and Receiving Enveloped Data Messages</span></span>

<span data-ttu-id="e1410-104">Un message enveloppé est un message chiffré pour un ensemble de destinataires.</span><span class="sxs-lookup"><span data-stu-id="e1410-104">An enveloped message is a message that is encrypted for a set of recipients.</span></span> <span data-ttu-id="e1410-105">Dans le processus d’encapsulement, une clé de chiffrement de session est générée et le message est chiffré avec cette clé.</span><span class="sxs-lookup"><span data-stu-id="e1410-105">In the envelopment process, a session encryption key is generated and the message is encrypted with that key.</span></span> <span data-ttu-id="e1410-106">La clé de chiffrement est ensuite chiffrée séparément pour chaque destinataire à l’aide des clés publiques de chaque certificat de destinataire prévu.</span><span class="sxs-lookup"><span data-stu-id="e1410-106">The encryption key itself is then encrypted separately for each recipient using the public keys from each intended recipient's certificate.</span></span> <span data-ttu-id="e1410-107">Le message enveloppé est constitué du message chiffré, des certificats des destinataires prévus et de l’ensemble des clés chiffrées, une pour chaque destinataire.</span><span class="sxs-lookup"><span data-stu-id="e1410-107">The enveloped message consists of the encrypted message, the certificates of the intended recipients, and the set of encrypted keys, one for each recipient.</span></span> <span data-ttu-id="e1410-108">Le message généré est au format [*PKCS \# 7*](../secgloss/p-gly.md)/CMS.</span><span class="sxs-lookup"><span data-stu-id="e1410-108">The message generated is in [*PKCS \#7*](../secgloss/p-gly.md)/CMS format.</span></span>

<span data-ttu-id="e1410-109">Les sections suivantes présentent des procédures et des exemples de tâches de messages enveloppés :</span><span class="sxs-lookup"><span data-stu-id="e1410-109">The following sections show procedures and examples for enveloped message tasks:</span></span>

-   [<span data-ttu-id="e1410-110">Encodage de données enveloppées</span><span class="sxs-lookup"><span data-stu-id="e1410-110">Encoding Enveloped Data</span></span>](encoding-enveloped-data.md)
-   [<span data-ttu-id="e1410-111">Décodage des données enveloppées</span><span class="sxs-lookup"><span data-stu-id="e1410-111">Decoding Enveloped Data</span></span>](decoding-enveloped-data.md)
-   [<span data-ttu-id="e1410-112">Autre code pour l’encodage d’un message enveloppé</span><span class="sxs-lookup"><span data-stu-id="e1410-112">Alternate Code for Encoding an Enveloped Message</span></span>](alternate-code-for-encoding-an-enveloped-message.md)
-   [<span data-ttu-id="e1410-113">Exemple de programme C : encodage d’un message signé et enveloppé</span><span class="sxs-lookup"><span data-stu-id="e1410-113">Example C Program: Encoding an Enveloped, Signed Message</span></span>](example-c-program-encoding-an-enveloped-signed-message.md)

 

 
