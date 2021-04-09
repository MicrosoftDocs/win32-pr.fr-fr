---
description: Lorsqu’un document ou un texte doit être protégé par un seul utilisateur ou que le document doit être partagé entre un petit groupe de personnes qui ont toutes accès au même mot de passe secret, le chiffrement/déchiffrement simple peut être effectué.
ms.assetid: 68eefd24-c924-4dd1-8cb3-cc20106f9605
title: Chiffrement et déchiffrement de données
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dd7123544fb9c8fa59291be2eae2c5bf9a120f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952626"
---
# <a name="encrypting-and-decrypting-data"></a><span data-ttu-id="54de0-103">Chiffrement et déchiffrement de données</span><span class="sxs-lookup"><span data-stu-id="54de0-103">Encrypting and Decrypting Data</span></span>

<span data-ttu-id="54de0-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="54de0-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="54de0-105">Utilisez plutôt le .NET Framework pour implémenter des fonctionnalités de sécurité.</span><span class="sxs-lookup"><span data-stu-id="54de0-105">Instead, use the .NET Framework to implement security features.</span></span> <span data-ttu-id="54de0-106">Pour plus d’informations, consultez [alternatives à l’utilisation de](alternatives-to-using-capicom.md)CAPICOM.\]</span><span class="sxs-lookup"><span data-stu-id="54de0-106">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).\]</span></span>

<span data-ttu-id="54de0-107">Lorsqu’un document ou un texte doit être protégé par un seul utilisateur ou que le document doit être partagé entre un petit groupe de personnes qui ont toutes accès au même mot de passe secret, le chiffrement/déchiffrement simple peut être effectué.</span><span class="sxs-lookup"><span data-stu-id="54de0-107">When a document or text needs to have privacy protected by a single user or when the document is to be shared among a small group of people who all have access to the same secret password, simple encryption/decryption can be done.</span></span> <span data-ttu-id="54de0-108">CAPICOM ne prend pas en charge le \# type de contenu PKCS 7 EncryptedData, mais utilise une structure ASN non standard pour EncryptedData.</span><span class="sxs-lookup"><span data-stu-id="54de0-108">CAPICOM does not support the PKCS \#7 EncryptedData content type but uses a non-standard ASN structure for EncryptedData.</span></span> <span data-ttu-id="54de0-109">Par conséquent, seul CAPICOM peut déchiffrer un objet CAPICOM EncryptedData.</span><span class="sxs-lookup"><span data-stu-id="54de0-109">Therefore, only CAPICOM can decrypt a CAPICOM EncryptedData object.</span></span>

<span data-ttu-id="54de0-110">Les sections suivantes présentent des exemples de tâches de chiffrement et de déchiffrement :</span><span class="sxs-lookup"><span data-stu-id="54de0-110">The following sections show examples for encryption and decryption tasks:</span></span>

-   [<span data-ttu-id="54de0-111">Chiffrement d’un message dans CAPICOM</span><span class="sxs-lookup"><span data-stu-id="54de0-111">Encrypting a Message in CAPICOM</span></span>](encrypting-a-message-in-capicom.md)
-   [<span data-ttu-id="54de0-112">Déchiffrement d’un message dans CAPICOM</span><span class="sxs-lookup"><span data-stu-id="54de0-112">Decrypting a Message in CAPICOM</span></span>](decrypting-a-message-in-capicom.md)

 

 



