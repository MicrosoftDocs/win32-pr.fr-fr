---
description: Processus de décodage des données signées.
ms.assetid: 803220d0-7963-4fc4-8451-a979e54a9cc3
title: Décodage des données signées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdfd327746c5d0ba8e7089e1c273817b76c16370
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106512950"
---
# <a name="decoding-signed-data"></a><span data-ttu-id="ea15c-103">Décodage des données signées</span><span class="sxs-lookup"><span data-stu-id="ea15c-103">Decoding Signed Data</span></span>

<span data-ttu-id="ea15c-104">Le processus général suivant décode un type de [*données signé*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="ea15c-104">The following general process decodes a [*signed data*](../secgloss/s-gly.md) type.</span></span>

<span data-ttu-id="ea15c-105">**Pour décoder un message signé**</span><span class="sxs-lookup"><span data-stu-id="ea15c-105">**To decode a signed message**</span></span>

1.  <span data-ttu-id="ea15c-106">Obtient un pointeur vers l’objet BLOB encodé.</span><span class="sxs-lookup"><span data-stu-id="ea15c-106">Get a pointer to the encoded BLOB.</span></span>
2.  <span data-ttu-id="ea15c-107">Appelez [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode), en passant les arguments nécessaires.</span><span class="sxs-lookup"><span data-stu-id="ea15c-107">Call [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode), passing the necessary arguments.</span></span>
3.  <span data-ttu-id="ea15c-108">Appelez [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) une fois, en passant le handle récupéré à l’étape 2 et un pointeur vers les données qui doivent être décodées.</span><span class="sxs-lookup"><span data-stu-id="ea15c-108">Call [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) once, passing in the handle retrieved in step 2 and a pointer to the data that is to be decoded.</span></span> <span data-ttu-id="ea15c-109">Cela entraîne le suivi des actions appropriées sur le message, en fonction du type de message.</span><span class="sxs-lookup"><span data-stu-id="ea15c-109">This causes the appropriate actions to be taken on the message, depending on the message type.</span></span>
4.  <span data-ttu-id="ea15c-110">Appelez [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), en passant le handle récupéré à l’étape 2 et les types de paramètres appropriés pour accéder aux données décodées.</span><span class="sxs-lookup"><span data-stu-id="ea15c-110">Call [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), passing in the handle retrieved in step 2 and the appropriate parameter types to access the decoded data.</span></span> <span data-ttu-id="ea15c-111">Par exemple, transmettez \_ le paramètre de contenu CMSG \_ pour obtenir un pointeur vers le contenu décodé.</span><span class="sxs-lookup"><span data-stu-id="ea15c-111">For example, pass in CMSG\_CONTENT\_PARAM to get a pointer to the decoded content.</span></span>

<span data-ttu-id="ea15c-112">Le processus général suivant vérifie la signature d’un message décodé et signé.</span><span class="sxs-lookup"><span data-stu-id="ea15c-112">The following general process verifies the signature of a decoded, signed message.</span></span>

<span data-ttu-id="ea15c-113">**Pour vérifier la signature d’un message décodé, signé**</span><span class="sxs-lookup"><span data-stu-id="ea15c-113">**To verify the signature of a decoded, signed message**</span></span>

1.  <span data-ttu-id="ea15c-114">Appelez [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), en transmettant la valeur du paramètre handle du message et CMSG du \_ signataire du signataire \_ \_ \_ pour récupérer [**les \_ informations du certificat**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) du signataire à partir du message.</span><span class="sxs-lookup"><span data-stu-id="ea15c-114">Call [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), passing in the message handle and CMSG\_SIGNER\_CERT\_INFO\_PARAM to get the signer's [**CERT\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) from the message.</span></span>
2.  <span data-ttu-id="ea15c-115">Appelez [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) pour ouvrir un magasin temporaire qui est initialisé avec les certificats du message.</span><span class="sxs-lookup"><span data-stu-id="ea15c-115">Call [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) to open a temporary store that is initialized with the certificates from the message.</span></span>
3.  <span data-ttu-id="ea15c-116">Appelez [**CertGetSubjectCertificateFromStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetsubjectcertificatefromstore) pour récupérer les [**\_ informations de certificat**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) du signataire à partir des certificats inclus dans le message.</span><span class="sxs-lookup"><span data-stu-id="ea15c-116">Call [**CertGetSubjectCertificateFromStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetsubjectcertificatefromstore) to get the signer's [**CERT\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) from the certificates included in the message.</span></span>
4.  <span data-ttu-id="ea15c-117">Appelez [**CryptMsgControl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol), en transmettant CMSG \_ CTRL \_ verify \_ signature pour vérifier les signatures.</span><span class="sxs-lookup"><span data-stu-id="ea15c-117">Call [**CryptMsgControl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol), passing in CMSG\_CTRL\_VERIFY\_SIGNATURE to verify the signatures.</span></span>
5.  <span data-ttu-id="ea15c-118">Appelez [**CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose) pour fermer le message.</span><span class="sxs-lookup"><span data-stu-id="ea15c-118">Call [**CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose) to close the message.</span></span>

<span data-ttu-id="ea15c-119">Le résultat de ces procédures est que la signature est vérifiée et qu’un pointeur est récupéré dans le contenu du message décodé obtenu à l’étape 4 de la procédure de décodage d’un message signé.</span><span class="sxs-lookup"><span data-stu-id="ea15c-119">The result of these procedures is that the signature is verified and a pointer is retrieved to the decoded message content obtained in step 4 of the procedure for decoding a signed message.</span></span>

<span data-ttu-id="ea15c-120">Pour plus d’informations sur le codage C, consultez [exemple de programme c : signature, encodage, décodage et vérification d’un message](example-c-program-signing-encoding-decoding-and-verifying-a-message.md).</span><span class="sxs-lookup"><span data-stu-id="ea15c-120">For C coding details, see [Example C Program: Signing, Encoding, Decoding, and Verifying a Message](example-c-program-signing-encoding-decoding-and-verifying-a-message.md).</span></span>

 

 
