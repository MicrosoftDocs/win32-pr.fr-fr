---
description: Présente les étapes permettant de déchiffrer un message chiffré.
ms.assetid: 6af7dd28-325e-431a-9cdb-109d93af6302
title: Déchiffrement de données
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 970f16862bb8c6693b2ff11f519af3f7c412024b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104321038"
---
# <a name="decrypting-data"></a><span data-ttu-id="2655c-103">Déchiffrement de données</span><span class="sxs-lookup"><span data-stu-id="2655c-103">Decrypting Data</span></span>

<span data-ttu-id="2655c-104">Cette section présente les étapes permettant de déchiffrer un message chiffré.</span><span class="sxs-lookup"><span data-stu-id="2655c-104">This section presents the steps to decrypt an encrypted message.</span></span>

<span data-ttu-id="2655c-105">**Pour déchiffrer un message chiffré**</span><span class="sxs-lookup"><span data-stu-id="2655c-105">**To decrypt an encrypted message**</span></span>

1.  <span data-ttu-id="2655c-106">Obtient un pointeur vers le message enveloppé numériquement.</span><span class="sxs-lookup"><span data-stu-id="2655c-106">Get a pointer to the digitally enveloped message.</span></span>
2.  <span data-ttu-id="2655c-107">Ouvrez un magasin de certificats.</span><span class="sxs-lookup"><span data-stu-id="2655c-107">Open a certificate store.</span></span>
3.  <span data-ttu-id="2655c-108">À partir du message, récupérez l’identificateur du destinataire (mon ID).</span><span class="sxs-lookup"><span data-stu-id="2655c-108">From the message, retrieve the recipient identifier (My ID).</span></span>
4.  <span data-ttu-id="2655c-109">Utilisez l’identificateur de destinataire pour récupérer le certificat.</span><span class="sxs-lookup"><span data-stu-id="2655c-109">Use the recipient identifier to retrieve the certificate.</span></span>
5.  <span data-ttu-id="2655c-110">Obtenir la clé privée du certificat.</span><span class="sxs-lookup"><span data-stu-id="2655c-110">Get the private key for the certificate.</span></span>
6.  <span data-ttu-id="2655c-111">Utilisez la clé privée pour déchiffrer la clé symétrique (session).</span><span class="sxs-lookup"><span data-stu-id="2655c-111">Use the private key to decrypt the symmetric (session) key.</span></span>
7.  <span data-ttu-id="2655c-112">Récupérez l’algorithme de chiffrement du message.</span><span class="sxs-lookup"><span data-stu-id="2655c-112">Retrieve the encryption algorithm from the message.</span></span>
8.  <span data-ttu-id="2655c-113">À l’aide de la clé de session déchiffrée et de l’algorithme de chiffrement, déchiffrez les données.</span><span class="sxs-lookup"><span data-stu-id="2655c-113">Using the decrypted session key and the encryption algorithm, decrypt the data.</span></span>

<span data-ttu-id="2655c-114">[**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) effectue toutes les tâches de déchiffrement d’un message. Toutefois, l’initialisation des structures et d’autres données est toujours nécessaire.</span><span class="sxs-lookup"><span data-stu-id="2655c-114">[**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) does all of the tasks for decrypting a message; however, initialization of structures and other data is still necessary.</span></span>

<span data-ttu-id="2655c-115">**Pour déchiffrer des données à l’aide de CryptDecryptMessage**</span><span class="sxs-lookup"><span data-stu-id="2655c-115">**To decrypt data using CryptDecryptMessage**</span></span>

1.  <span data-ttu-id="2655c-116">Obtient un pointeur vers l’objet BLOB chiffré.</span><span class="sxs-lookup"><span data-stu-id="2655c-116">Get a pointer to the encrypted BLOB.</span></span>
2.  <span data-ttu-id="2655c-117">Ouvrez un magasin de certificats.</span><span class="sxs-lookup"><span data-stu-id="2655c-117">Open a certificate store.</span></span>
3.  <span data-ttu-id="2655c-118">Créez un groupe de magasins de certificats.</span><span class="sxs-lookup"><span data-stu-id="2655c-118">Create a certificate store array.</span></span>
4.  <span data-ttu-id="2655c-119">Initialisez la structure de la [**\_ para- \_ message \_ de déchiffrement**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_decrypt_message_para) .</span><span class="sxs-lookup"><span data-stu-id="2655c-119">Initialize the [**CRYPT\_DECRYPT\_MESSAGE\_PARA**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_decrypt_message_para) structure.</span></span>
5.  <span data-ttu-id="2655c-120">Appelez [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) pour déchiffrer les données contenues dans le message.</span><span class="sxs-lookup"><span data-stu-id="2655c-120">Call [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) to decrypt the data contained in the message.</span></span>

<span data-ttu-id="2655c-121">[Exemple de programme C : l’utilisation de CryptEncryptMessage et de CryptDecryptMessage](example-c-program-using-cryptencryptmessage-and-cryptdecryptmessage.md) implémente la procédure qui vient d’être présentée.</span><span class="sxs-lookup"><span data-stu-id="2655c-121">[Example C Program: Using CryptEncryptMessage and CryptDecryptMessage](example-c-program-using-cryptencryptmessage-and-cryptdecryptmessage.md) implements the procedure just presented.</span></span> <span data-ttu-id="2655c-122">Les commentaires indiquent les éléments de code qui effectuent chaque étape de la procédure.</span><span class="sxs-lookup"><span data-stu-id="2655c-122">Comments show which code elements accomplish each step in the procedure.</span></span> <span data-ttu-id="2655c-123">Pour plus d’informations sur la fonction, consultez [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage)et pour plus d’informations sur la structure de données, consultez [**\_ crypt Decrypt \_ message \_ para**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_decrypt_message_para).</span><span class="sxs-lookup"><span data-stu-id="2655c-123">For details about the function, see [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage), and for details about the data structure, see [**CRYPT\_DECRYPT\_MESSAGE\_PARA**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_decrypt_message_para).</span></span>

 

 



