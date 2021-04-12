---
description: Le message enveloppé est constitué du message chiffré, des certificats des destinataires prévus et de l’ensemble des clés chiffrées, une pour chaque destinataire. Le message généré est au \# format PKCS 7/CMS.
ms.assetid: 2acd0b58-1028-478d-bfa1-b02fa457d7e3
title: Création et réception de messages de données enveloppés dans CAPICOM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 672d56383ac635a295847777c0e557bbe7c40b69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318237"
---
# <a name="creating-and-receiving-enveloped-data-messages-in-capicom"></a><span data-ttu-id="3d509-104">Création et réception de messages de données enveloppés dans CAPICOM</span><span class="sxs-lookup"><span data-stu-id="3d509-104">Creating and Receiving Enveloped Data Messages in CAPICOM</span></span>

<span data-ttu-id="3d509-105">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="3d509-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="3d509-106">Utilisez plutôt le .NET Framework pour implémenter des fonctionnalités de sécurité.</span><span class="sxs-lookup"><span data-stu-id="3d509-106">Instead, use the .NET Framework to implement security features.</span></span> <span data-ttu-id="3d509-107">Pour plus d’informations, consultez [alternatives à l’utilisation de](alternatives-to-using-capicom.md)CAPICOM.\]</span><span class="sxs-lookup"><span data-stu-id="3d509-107">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).\]</span></span>

<span data-ttu-id="3d509-108">Un message enveloppé est un message chiffré pour un ensemble de destinataires.</span><span class="sxs-lookup"><span data-stu-id="3d509-108">An enveloped message is a message that is encrypted for a set of recipients.</span></span> <span data-ttu-id="3d509-109">Dans le processus d’encapsulement, une clé de chiffrement de session est générée et le message est chiffré avec cette clé.</span><span class="sxs-lookup"><span data-stu-id="3d509-109">In the envelopment process, a session encryption key is generated and the message is encrypted with that key.</span></span> <span data-ttu-id="3d509-110">La clé de chiffrement est ensuite chiffrée séparément pour chaque destinataire à l’aide des clés publiques de chaque certificat de destinataire prévu.</span><span class="sxs-lookup"><span data-stu-id="3d509-110">The encryption key itself is then encrypted separately for each recipient using the public keys from each intended recipient's certificate.</span></span> <span data-ttu-id="3d509-111">Le message enveloppé est constitué du message chiffré, des certificats des destinataires prévus et de l’ensemble des clés chiffrées, une pour chaque destinataire.</span><span class="sxs-lookup"><span data-stu-id="3d509-111">The enveloped message consists of the encrypted message, the certificates of the intended recipients, and the set of encrypted keys, one for each recipient.</span></span> <span data-ttu-id="3d509-112">Le message généré est au \# format PKCS 7/CMS.</span><span class="sxs-lookup"><span data-stu-id="3d509-112">The message generated is in PKCS \#7/CMS format.</span></span>

<span data-ttu-id="3d509-113">Les sections suivantes présentent des procédures et des exemples de tâches de messages enveloppés :</span><span class="sxs-lookup"><span data-stu-id="3d509-113">The following sections show procedures and examples for enveloped message tasks:</span></span>

-   [<span data-ttu-id="3d509-114">Envoi d’un message de données enveloppées</span><span class="sxs-lookup"><span data-stu-id="3d509-114">Sending an Enveloped Data Message</span></span>](sending-an-enveloped-data-message.md)
-   [<span data-ttu-id="3d509-115">Réception d’un message de données enveloppées</span><span class="sxs-lookup"><span data-stu-id="3d509-115">Receiving an Enveloped Data Message</span></span>](receiving-an-enveloped-data-message.md)

 

 



