---
description: Le protocole d’enregistrement TLS (Transport Layer Security) sécurise les données d’application à l’aide des clés créées pendant le protocole de transfert.
ms.assetid: 3ad4cbd9-ce7c-4882-9c53-c935068c0ba7
title: Protocole d’enregistrement TLS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a53d41ad73dc9e1338f0cbff1bec5d6cd6a55e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534039"
---
# <a name="tls-record-protocol"></a><span data-ttu-id="41d87-103">Protocole d’enregistrement TLS</span><span class="sxs-lookup"><span data-stu-id="41d87-103">TLS Record Protocol</span></span>

<span data-ttu-id="41d87-104">Le protocole d’enregistrement TLS ( [*Transport Layer Security*](../secgloss/t-gly.md) ) sécurise les données d’application à l’aide des clés créées pendant le [protocole de transfert](tls-handshake-protocol.md).</span><span class="sxs-lookup"><span data-stu-id="41d87-104">The [*Transport Layer Security*](../secgloss/t-gly.md) (TLS) Record protocol secures application data using the keys created during the [Handshake](tls-handshake-protocol.md).</span></span> <span data-ttu-id="41d87-105">Le protocole d’enregistrement est responsable de la sécurisation des données d’application et de la vérification de leur [*intégrité*](../secgloss/i-gly.md) et de leur origine.</span><span class="sxs-lookup"><span data-stu-id="41d87-105">The Record Protocol is responsible for securing application data and verifying its [*integrity*](../secgloss/i-gly.md) and origin.</span></span> <span data-ttu-id="41d87-106">Il gère les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="41d87-106">It manages the following:</span></span>

-   <span data-ttu-id="41d87-107">Division des messages sortants en blocs gérables et réassemblage des messages entrants.</span><span class="sxs-lookup"><span data-stu-id="41d87-107">Dividing outgoing messages into manageable blocks, and reassembling incoming messages.</span></span>
-   <span data-ttu-id="41d87-108">Compression des blocs sortants et décompression des blocs entrants (facultatif).</span><span class="sxs-lookup"><span data-stu-id="41d87-108">Compressing outgoing blocks and decompressing incoming blocks (optional).</span></span>
-   <span data-ttu-id="41d87-109">Application d’un [*code d’Authentification de message*](../secgloss/m-gly.md) (Mac) aux messages sortants et vérification des messages entrants à l’aide du Mac.</span><span class="sxs-lookup"><span data-stu-id="41d87-109">Applying a [*Message Authentication Code*](../secgloss/m-gly.md) (MAC) to outgoing messages, and verifying incoming messages using the MAC.</span></span>
-   <span data-ttu-id="41d87-110">Chiffrement des messages sortants et déchiffrement des messages entrants.</span><span class="sxs-lookup"><span data-stu-id="41d87-110">Encrypting outgoing messages and decrypting incoming messages.</span></span>

<span data-ttu-id="41d87-111">Lorsque le protocole d’enregistrement est terminé, les données chiffrées sortantes sont transmises à la couche TCP (Transmission Control Protocol) pour le transport.</span><span class="sxs-lookup"><span data-stu-id="41d87-111">When the Record Protocol is complete, the outgoing encrypted data is passed down to the Transmission Control Protocol (TCP) layer for transport.</span></span>

 

 
