---
description: Dans une infrastructure à clé publique Microsoft, les demandes de certificat sont envoyées à partir d’ordinateurs clients vers des autorités de certification en tant que chaîne binaire qui contient une séquence de structures de données encodées.
ms.assetid: 0b9fa1bc-b67e-4b50-abd5-cbc3663ff219
title: Encodage de demande de certificat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cd9dfedede4c7b10d4968242b1d27ad11e2b6f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756544"
---
# <a name="certificate-request-encoding"></a><span data-ttu-id="193c9-103">Encodage de demande de certificat</span><span class="sxs-lookup"><span data-stu-id="193c9-103">Certificate Request Encoding</span></span>

<span data-ttu-id="193c9-104">Dans une infrastructure à clé publique Microsoft, les demandes de certificat sont envoyées à partir d’ordinateurs clients vers des autorités de certification en tant que chaîne binaire qui contient une séquence de structures de données encodées.</span><span class="sxs-lookup"><span data-stu-id="193c9-104">In a Microsoft PKI, certificate requests are sent from client computers to certification authorities (CAs) as a binary string that contains a sequence of encoded data structures.</span></span> <span data-ttu-id="193c9-105">L’API d’inscription de certificats utilise le ASN. 1 (Abstract Syntax Notation One) pour décrire et encoder ces structures.</span><span class="sxs-lookup"><span data-stu-id="193c9-105">The Certificate Enrollment API uses Abstract Syntax Notation One (ASN.1) to describe and encode these structures.</span></span> <span data-ttu-id="193c9-106">Dans le cadre de cette documentation, ASN. 1 peut être divisé de manière conceptuelle en règles syntaxiques (ISO 8824) qui décrivent les structures de données et les règles d’encodage (ISO 8825) qui spécifient la façon dont les données doivent être encodées pour la transmission réseau.</span><span class="sxs-lookup"><span data-stu-id="193c9-106">For the purposes of this documentation, ASN.1 can be conceptually divided into the syntax rules (ISO 8824) that describe the data structures and the encoding rules (ISO 8825) that specify how the data is to be encoded for network transmission.</span></span> <span data-ttu-id="193c9-107">Pour plus d'informations, voir les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="193c9-107">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="193c9-108">Présentation de la syntaxe et de l’encodage ASN. 1</span><span class="sxs-lookup"><span data-stu-id="193c9-108">Introduction to ASN.1 Syntax and Encoding</span></span>](about-introduction-to-asn-1-syntax-and-encoding.md)
-   [<span data-ttu-id="193c9-109">Système de type ASN. 1</span><span class="sxs-lookup"><span data-stu-id="193c9-109">ASN.1 Type System</span></span>](about-asn-1-type-system.md)
-   [<span data-ttu-id="193c9-110">Distinguished Encoding Rules</span><span class="sxs-lookup"><span data-stu-id="193c9-110">Distinguished Encoding Rules</span></span>](distinguished-encoding-rules.md)

## <a name="related-topics"></a><span data-ttu-id="193c9-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="193c9-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="193c9-112">À propos de l’API d’inscription de certificats</span><span class="sxs-lookup"><span data-stu-id="193c9-112">About the Certificate Enrollment API</span></span>](about-the-certificate-enrollment-api.md)
</dt> </dl>

 

 



