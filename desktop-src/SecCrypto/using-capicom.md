---
description: Cette section comprend des scénarios qui utilisent des procédures CAPICOM.
ms.assetid: f886e04a-4ea7-4d24-a05f-3e08742fe134
title: Utilisation de CAPICOM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46f81b1a346b6186ead6544b7194259cc52ae2be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527622"
---
# <a name="using-capicom"></a><span data-ttu-id="0dc4b-103">Utilisation de CAPICOM</span><span class="sxs-lookup"><span data-stu-id="0dc4b-103">Using CAPICOM</span></span>

<span data-ttu-id="0dc4b-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="0dc4b-105">Utilisez plutôt le .NET Framework pour implémenter des fonctionnalités de sécurité.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-105">Instead, use the .NET Framework to implement security features.</span></span> <span data-ttu-id="0dc4b-106">Pour plus d’informations, consultez [alternatives à l’utilisation de](alternatives-to-using-capicom.md)CAPICOM.\]</span><span class="sxs-lookup"><span data-stu-id="0dc4b-106">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).\]</span></span>

<span data-ttu-id="0dc4b-107">Cette section comprend des scénarios qui utilisent des procédures CAPICOM.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-107">This section includes scenarios that use CAPICOM procedures.</span></span>

> [!Note]  
> <span data-ttu-id="0dc4b-108">La création de [*signatures numériques*](../secgloss/d-gly.md) et la désinscription des messages avec CAPICOM s’effectuent à l’aide du chiffrement de l’infrastructure à clé publique (PKI) et ne peut être effectuée que si le signataire ou l’utilisateur déchiffrant un message enveloppé a accès à un certificat avec une clé privée associée disponible.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-108">Creating [*digital signatures*](../secgloss/d-gly.md) and un-enveloping messages with CAPICOM is done using Public Key Infrastructure (PKI) cryptography and can only be done if the signer or user decrypting an enveloped message has access to a certificate with an available, associated private key.</span></span> <span data-ttu-id="0dc4b-109">Pour déchiffrer un message enveloppé, un certificat ayant accès à la clé privée doit figurer dans le magasin MY.</span><span class="sxs-lookup"><span data-stu-id="0dc4b-109">To decrypt an enveloped message, a certificate with access to the private key must be in the MY store.</span></span>

 

<span data-ttu-id="0dc4b-110">Les scénarios basés sur des tâches et les exemples ont été répartis dans les sections suivantes :</span><span class="sxs-lookup"><span data-stu-id="0dc4b-110">Task-based scenarios discussions and examples have been separated into the following sections:</span></span>

-   [<span data-ttu-id="0dc4b-111">Alternatives à l’utilisation de CAPICOM</span><span class="sxs-lookup"><span data-stu-id="0dc4b-111">Alternatives to Using CAPICOM</span></span>](alternatives-to-using-capicom.md)
-   [<span data-ttu-id="0dc4b-112">Préparation à l’utilisation de CAPICOM</span><span class="sxs-lookup"><span data-stu-id="0dc4b-112">Getting Ready to Use CAPICOM</span></span>](getting-ready-to-use-capicom.md)
-   [<span data-ttu-id="0dc4b-113">Chiffrement et déchiffrement de données</span><span class="sxs-lookup"><span data-stu-id="0dc4b-113">Encrypting and Decrypting Data</span></span>](encrypting-and-decrypting-data.md)
-   [<span data-ttu-id="0dc4b-114">Signature des données et vérification des signatures numériques</span><span class="sxs-lookup"><span data-stu-id="0dc4b-114">Signing Data and Verifying Digital Signatures</span></span>](signing-data-and-verifying-digital-signatures.md)
-   [<span data-ttu-id="0dc4b-115">Utilisation des magasins de certificats</span><span class="sxs-lookup"><span data-stu-id="0dc4b-115">Using Certificate Stores</span></span>](using-certificate-stores.md)
-   [<span data-ttu-id="0dc4b-116">Création et réception des messages de données enveloppés</span><span class="sxs-lookup"><span data-stu-id="0dc4b-116">Creating and Receiving Enveloped Data Messages</span></span>](creating-and-receiving-enveloped-data-messages-in-capicom.md)

 

 
