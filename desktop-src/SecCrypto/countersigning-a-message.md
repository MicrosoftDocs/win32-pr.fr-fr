---
description: Explique comment contre-signer un message à l’aide de CryptMsgCountersign.
ms.assetid: e1969b43-f50e-4c7d-a7e5-b22db4e05be2
title: Contre-signature d’un message
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02091d25e7ee22f986a26b8f07abff68ebb8c11c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523275"
---
# <a name="countersigning-a-message"></a><span data-ttu-id="7aa03-103">Contre-signature d’un message</span><span class="sxs-lookup"><span data-stu-id="7aa03-103">Countersigning a Message</span></span>

<span data-ttu-id="7aa03-104">**Pour contre-signer un message signé à l’aide de CryptMsgCountersign**</span><span class="sxs-lookup"><span data-stu-id="7aa03-104">**To countersign a signed message by using CryptMsgCountersign**</span></span>

1.  <span data-ttu-id="7aa03-105">Appelez [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode) pour obtenir un descripteur du message signé.</span><span class="sxs-lookup"><span data-stu-id="7aa03-105">Call [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode) to get a handle to the signed message.</span></span>
2.  <span data-ttu-id="7aa03-106">Initialisez une structure d' [**\_ informations de \_ codage \_ CMSG**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) pour le signataire.</span><span class="sxs-lookup"><span data-stu-id="7aa03-106">Initialize a [**CMSG\_SIGNER\_ENCODE\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) structure for the countersigner.</span></span>
3.  <span data-ttu-id="7aa03-107">Ajoutez la structure d’informations de codage du signataire CMSG à un tableau de contre- [**\_ signataires \_ \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) (un seul contresigné est actuellement pris en charge).</span><span class="sxs-lookup"><span data-stu-id="7aa03-107">Add the [**CMSG\_SIGNER\_ENCODE\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) structure to an array of countersigners (only one countersigner is currently supported).</span></span>
4.  <span data-ttu-id="7aa03-108">Appelez [**CryptMsgCountersign**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcountersign) pour ajouter la contre-signature ou les contre-signatures.</span><span class="sxs-lookup"><span data-stu-id="7aa03-108">Call [**CryptMsgCountersign**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcountersign) to add the countersignature or countersignatures.</span></span>

<span data-ttu-id="7aa03-109">Si tous les appels de fonction ont été exécutés correctement, le message d’origine a désormais une contre- [*signature*](../secgloss/c-gly.md) incluse comme attribut non authentifié.</span><span class="sxs-lookup"><span data-stu-id="7aa03-109">If all of the function calls succeed, the original message now has a [*countersignature*](../secgloss/c-gly.md) included as an unauthenticated attribute.</span></span>

<span data-ttu-id="7aa03-110">**Pour contre-signer un message signé à l’aide de CryptMsgCountersignEncoded**</span><span class="sxs-lookup"><span data-stu-id="7aa03-110">**To countersign a signed message by using CryptMsgCountersignEncoded**</span></span>

1.  <span data-ttu-id="7aa03-111">Appelez [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode) pour obtenir un descripteur du message signé.</span><span class="sxs-lookup"><span data-stu-id="7aa03-111">Call [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode) to get a handle to the signed message.</span></span>
2.  <span data-ttu-id="7aa03-112">Appelez [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) pour récupérer les informations de signataire encodées du message signé.</span><span class="sxs-lookup"><span data-stu-id="7aa03-112">Call [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) to retrieve the encoded signer information of the signed message.</span></span>
3.  <span data-ttu-id="7aa03-113">Initialisez une structure d' [**\_ informations de \_ codage \_ CMSG**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) pour le signataire.</span><span class="sxs-lookup"><span data-stu-id="7aa03-113">Initialize a [**CMSG\_SIGNER\_ENCODE\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) structure for the countersigner.</span></span>
4.  <span data-ttu-id="7aa03-114">Ajoutez la structure d’informations de codage du signataire CMSG à un tableau de contre- [**\_ signataires \_ \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) (un seul contresigné est actuellement pris en charge).</span><span class="sxs-lookup"><span data-stu-id="7aa03-114">Add the [**CMSG\_SIGNER\_ENCODE\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_encode_info) structure to an array of countersigners (only one countersigner is currently supported).</span></span>
5.  <span data-ttu-id="7aa03-115">Appelez [**CryptMsgCountersignEncoded**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcountersignencoded) pour créer l’attribut de contre-signature encodé.</span><span class="sxs-lookup"><span data-stu-id="7aa03-115">Call [**CryptMsgCountersignEncoded**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcountersignencoded) to create the encoded countersignature attribute.</span></span>
6.  <span data-ttu-id="7aa03-116">Appelez [**CryptMsgControl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol) pour ajouter l’attribut contre-signature au message d’origine en tant qu’attribut non authentifié.</span><span class="sxs-lookup"><span data-stu-id="7aa03-116">Call [**CryptMsgControl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol) to add the countersignature attribute to the original message as an unauthenticated attribute.</span></span>

<span data-ttu-id="7aa03-117">Si tous les appels de fonction ont échoué, un attribut contre- [*signature*](../secgloss/c-gly.md) est ajouté au message d’origine.</span><span class="sxs-lookup"><span data-stu-id="7aa03-117">If all of the function calls succeed, a [*countersignature*](../secgloss/c-gly.md) attribute is added to the original message.</span></span>

 

 
