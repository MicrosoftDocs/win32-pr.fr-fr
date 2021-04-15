---
description: Tâches générales requises pour décoder un message enveloppé.
ms.assetid: cb71ea3a-0edd-4d46-8088-a395fab89d2b
title: Décodage des données enveloppées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc1a0ba12e967f5a0cd56347c0839ce9fca40f02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104556305"
---
# <a name="decoding-enveloped-data"></a><span data-ttu-id="6967e-103">Décodage des données enveloppées</span><span class="sxs-lookup"><span data-stu-id="6967e-103">Decoding Enveloped Data</span></span>

<span data-ttu-id="6967e-104">Les tâches générales requises pour décoder un message enveloppé sont illustrées dans l’illustration suivante et décrites dans la liste qui suit.</span><span class="sxs-lookup"><span data-stu-id="6967e-104">The general tasks required to decode an enveloped message are depicted in the following illustration and described in the list that follows it.</span></span>

![décodage des données enveloppées](images/decemsg.png)

<span data-ttu-id="6967e-106">La séquence d’événements pour décoder les données enveloppées à l’aide de la gestion de clés de transport de clé, comme illustré dans l’illustration précédente, est la suivante :</span><span class="sxs-lookup"><span data-stu-id="6967e-106">The sequence of events for decoding enveloped data using key transport key management, as depicted in the previous illustration, is as follows:</span></span>

-   <span data-ttu-id="6967e-107">Un pointeur vers le message [*enveloppé numériquement*](../secgloss/d-gly.md) est récupéré.</span><span class="sxs-lookup"><span data-stu-id="6967e-107">A pointer to the [*digitally enveloped*](../secgloss/d-gly.md) message is retrieved.</span></span>
-   <span data-ttu-id="6967e-108">Un [*magasin de certificats*](../secgloss/c-gly.md) est ouvert.</span><span class="sxs-lookup"><span data-stu-id="6967e-108">A [*certificate store*](../secgloss/c-gly.md) is opened.</span></span>
-   <span data-ttu-id="6967e-109">À partir du message, l’ID de destinataire (mon ID) est récupéré.</span><span class="sxs-lookup"><span data-stu-id="6967e-109">From the message, the recipient ID (My ID) is retrieved.</span></span>
-   <span data-ttu-id="6967e-110">L’ID de destinataire est utilisé pour récupérer le certificat.</span><span class="sxs-lookup"><span data-stu-id="6967e-110">The recipient ID is used to retrieve the certificate.</span></span>
-   <span data-ttu-id="6967e-111">La [*clé privée*](../secgloss/p-gly.md) associée à ce certificat est récupérée.</span><span class="sxs-lookup"><span data-stu-id="6967e-111">The [*private key*](../secgloss/p-gly.md) associated with that certificate is retrieved.</span></span>
-   <span data-ttu-id="6967e-112">La clé privée est utilisée pour déchiffrer la clé [*symétrique*](../secgloss/s-gly.md) ([*session*](../secgloss/s-gly.md)).</span><span class="sxs-lookup"><span data-stu-id="6967e-112">The private key is used to decrypt the [*symmetric*](../secgloss/s-gly.md) ([*session*](../secgloss/s-gly.md)) key.</span></span>
-   <span data-ttu-id="6967e-113">L’algorithme de chiffrement est récupéré à partir du message.</span><span class="sxs-lookup"><span data-stu-id="6967e-113">The encryption algorithm is retrieved from the message.</span></span>
-   <span data-ttu-id="6967e-114">À l’aide de la clé privée et de l’algorithme de chiffrement, les données sont déchiffrées.</span><span class="sxs-lookup"><span data-stu-id="6967e-114">Using the private key and encryption algorithm, the data is decrypted.</span></span>

<span data-ttu-id="6967e-115">La procédure suivante utilise des fonctions de message de bas niveau pour accomplir les tâches que vous venez de répertorier.</span><span class="sxs-lookup"><span data-stu-id="6967e-115">The following procedure uses low-level message functions to accomplish the tasks just listed.</span></span>

<span data-ttu-id="6967e-116">**Pour décoder un message enveloppé**</span><span class="sxs-lookup"><span data-stu-id="6967e-116">**To decode an enveloped message**</span></span>

1.  <span data-ttu-id="6967e-117">Obtient un pointeur vers l’objet BLOB encodé.</span><span class="sxs-lookup"><span data-stu-id="6967e-117">Get a pointer to the encoded BLOB.</span></span>
2.  <span data-ttu-id="6967e-118">Appelez [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode), en passant les arguments nécessaires.</span><span class="sxs-lookup"><span data-stu-id="6967e-118">Call [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode), passing the necessary arguments.</span></span>
3.  <span data-ttu-id="6967e-119">Appelez [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) une fois, en passant le handle récupéré à l’étape 2 et un pointeur vers les données qui doivent être décodées.</span><span class="sxs-lookup"><span data-stu-id="6967e-119">Call [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) once, passing in the handle retrieved in step 2 and a pointer to the data that is to be decoded.</span></span> <span data-ttu-id="6967e-120">Cela entraîne le suivi des actions appropriées sur le message, en fonction du type de message.</span><span class="sxs-lookup"><span data-stu-id="6967e-120">This causes the appropriate actions to be taken on the message, depending on the message type.</span></span>
4.  <span data-ttu-id="6967e-121">Appelez [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), en passant le handle récupéré à l’étape 2 et \_ le \_ paramètre de type CMSG pour vérifier que le message est du type de données enveloppé.</span><span class="sxs-lookup"><span data-stu-id="6967e-121">Call [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), passing in the handle retrieved in step 2 and CMSG\_TYPE\_PARAM to verify that the message is of the enveloped data type.</span></span>
5.  <span data-ttu-id="6967e-122">Appelez à nouveau [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), en passant \_ \_ le paramètre de type de contenu interne CMSG \_ \_ pour récupérer le type de données du [*contenu interne*](../secgloss/i-gly.md).</span><span class="sxs-lookup"><span data-stu-id="6967e-122">Again call [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), passing in CMSG\_INNER\_CONTENT\_TYPE\_PARAM to get the data type of the [*inner content*](../secgloss/i-gly.md).</span></span>
6.  <span data-ttu-id="6967e-123">Si le type de données de contenu interne est **Data**, effectuez le déchiffrement et le décodage du contenu.</span><span class="sxs-lookup"><span data-stu-id="6967e-123">If the inner content data type is **data**, proceed to decrypt and decode the content.</span></span> <span data-ttu-id="6967e-124">Sinon, exécutez une procédure de décodage appropriée pour le type de données de contenu.</span><span class="sxs-lookup"><span data-stu-id="6967e-124">Otherwise, run a decoding procedure appropriate for the content data type.</span></span>
7.  <span data-ttu-id="6967e-125">En supposant que le type de contenu interne est « Data », initialisez la structure de données [**CMSG \_ CTRL \_ decrypte \_ para**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_ctrl_decrypt_para) , puis appelez [**CryptMsgControl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol), en passant CMSG \_ CTRL \_ et l’adresse de la structure.</span><span class="sxs-lookup"><span data-stu-id="6967e-125">Assuming the inner content type is "data", initialize the [**CMSG\_CTRL\_DECRYPT\_PARA**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_ctrl_decrypt_para) data structure, and call [**CryptMsgControl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol), passing in CMSG\_CTRL\_DECRYPT and the address of the structure.</span></span> <span data-ttu-id="6967e-126">Le contenu sera déchiffré.</span><span class="sxs-lookup"><span data-stu-id="6967e-126">The content will be decrypted.</span></span>
8.  <span data-ttu-id="6967e-127">Appelez [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), en passant \_ le paramètre de contenu CMSG \_ pour obtenir un pointeur vers l’objet blob de données décodées (chaîne d'**octets** ).</span><span class="sxs-lookup"><span data-stu-id="6967e-127">Call [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam), passing in CMSG\_CONTENT\_PARAM to get a pointer to the decoded content data BLOB (**BYTE** string).</span></span>
9.  <span data-ttu-id="6967e-128">Appelez [**CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose) pour fermer le message.</span><span class="sxs-lookup"><span data-stu-id="6967e-128">Call [**CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose) to close the message.</span></span>

<span data-ttu-id="6967e-129">Le résultat de cette procédure est que le message est décodé et déchiffré et qu’un pointeur est récupéré dans l’objet BLOB de données de contenu.</span><span class="sxs-lookup"><span data-stu-id="6967e-129">The result of this procedure is that the message is decoded and decrypted and a pointer is retrieved to the content data BLOB.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6967e-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6967e-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6967e-131">Exemple de programme C : encodage d’un message signé et enveloppé</span><span class="sxs-lookup"><span data-stu-id="6967e-131">Example C Program: Encoding an Enveloped, Signed Message</span></span>](example-c-program-encoding-an-enveloped-signed-message.md)
</dt> </dl>

 

 
