---
description: Décrit les étapes à suivre pour chiffrer un message avec les fonctions de chiffrement de base.
ms.assetid: 34167767-96c5-4a20-b629-07e4d036b4d1
title: Chiffrement de données
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44db44db08268241e399107d8af4088dac3c0c2e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104562523"
---
# <a name="encrypting-data"></a><span data-ttu-id="27212-103">Chiffrement de données</span><span class="sxs-lookup"><span data-stu-id="27212-103">Encrypting Data</span></span>

<span data-ttu-id="27212-104">La procédure suivante décrit les étapes à suivre pour chiffrer un message avec les fonctions de chiffrement de base.</span><span class="sxs-lookup"><span data-stu-id="27212-104">The following procedure describes steps to take to encrypt a message with the Base Cryptography Functions.</span></span> <span data-ttu-id="27212-105">Pour chiffrer les messages à l’aide des \# normes PKCS 7, consultez [fonctions de message de bas niveau](cryptography-functions.md) et [fonctions de message simplifiées](cryptography-functions.md).</span><span class="sxs-lookup"><span data-stu-id="27212-105">To encrypt messages using PKCS \#7 standards, see [Low-level Message Functions](cryptography-functions.md) and [Simplified Message Functions](cryptography-functions.md).</span></span>

<span data-ttu-id="27212-106">**Pour chiffrer un message**</span><span class="sxs-lookup"><span data-stu-id="27212-106">**To encrypt a message**</span></span>

1.  <span data-ttu-id="27212-107">Générez une clé de session à l’aide de la fonction [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) .</span><span class="sxs-lookup"><span data-stu-id="27212-107">Generate a session key by using the [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) function.</span></span>

    <span data-ttu-id="27212-108">Cet appel génère une clé aléatoire et retourne un descripteur afin que la clé puisse être utilisée pour chiffrer et déchiffrer les données.</span><span class="sxs-lookup"><span data-stu-id="27212-108">Making this call generates a random key and returns a handle so the key can be used to encrypt and decrypt data.</span></span> <span data-ttu-id="27212-109">L’algorithme de chiffrement à utiliser est également spécifié à ce stade.</span><span class="sxs-lookup"><span data-stu-id="27212-109">The encryption algorithm to use is also specified at this point.</span></span> <span data-ttu-id="27212-110">Comme CryptoAPI ne permet pas aux applications d’utiliser des algorithmes de clé publique pour chiffrer les données en bloc, spécifiez un algorithme symétrique tel que RC2 ou RC4 avec l’appel [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) .</span><span class="sxs-lookup"><span data-stu-id="27212-110">Because CryptoAPI does not permit applications to use public key algorithms to encrypt bulk data, specify a symmetric algorithm such as RC2 or RC4 with the [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) call.</span></span>

2.  <span data-ttu-id="27212-111">Vous pouvez également utiliser la fonction [**CryptDeriveKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey) pour transformer un mot de passe en une clé adaptée au chiffrement.</span><span class="sxs-lookup"><span data-stu-id="27212-111">Alternatively, use the [**CryptDeriveKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey) function to transform a password into a key suitable for encryption.</span></span>

    <span data-ttu-id="27212-112">Si une application doit chiffrer le message afin que toute personne disposant d’un mot de passe spécifié puisse déchiffrer les données, utilisez [**CryptDeriveKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey) pour transformer le mot de passe en une clé adaptée au chiffrement.</span><span class="sxs-lookup"><span data-stu-id="27212-112">If an application needs to encrypt the message so that anyone with a specified password can decrypt the data, use [**CryptDeriveKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey) to transform the password into a key suitable for encryption.</span></span>

    > [!Note]  
    > <span data-ttu-id="27212-113">Dans ce cas, cette fonction est appelée à la place de la fonction [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) et les appels [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) suivants ne sont pas nécessaires.</span><span class="sxs-lookup"><span data-stu-id="27212-113">In this case, this function is called instead of the [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) function and the subsequent [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) calls are not needed.</span></span>

     

3.  <span data-ttu-id="27212-114">Si nécessaire, définissez des propriétés de chiffrement supplémentaires de la clé à l’aide de la fonction [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam)</span><span class="sxs-lookup"><span data-stu-id="27212-114">If necessary, set extra cryptographic properties of the key by using the [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) function</span></span>

    <span data-ttu-id="27212-115">Une fois la clé générée, les propriétés de chiffrement supplémentaires de la clé peuvent être définies avec la fonction [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam).</span><span class="sxs-lookup"><span data-stu-id="27212-115">After the key has been generated, extra cryptographic properties of the key can be set with the [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam)function.</span></span> <span data-ttu-id="27212-116">Cette fonction permet aux différentes sections du fichier d’être chiffrées à l’aide de différents sels de clé et fournit un moyen de modifier le mode de chiffrement ou le vecteur d’initialisation de la clé.</span><span class="sxs-lookup"><span data-stu-id="27212-116">This function allows different sections of the file to be encrypted with different key salts and provides a way to change the cipher mode or initialization vector of the key.</span></span> <span data-ttu-id="27212-117">Ces paramètres peuvent être utilisés pour rendre le chiffrement conforme à une norme de chiffrement de données particulière.</span><span class="sxs-lookup"><span data-stu-id="27212-117">These parameters can be used to make the encryption conform with a particular data encryption standard.</span></span>

4.  <span data-ttu-id="27212-118">Chiffrez les données dans le fichier avec la fonction [**CryptEncrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencrypt) .</span><span class="sxs-lookup"><span data-stu-id="27212-118">Encrypt the data in the file with the [**CryptEncrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencrypt) function.</span></span>

    <span data-ttu-id="27212-119">La fonction [**CryptEncrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencrypt) prend la clé de session générée à l’étape précédente et chiffre une mémoire tampon de données.</span><span class="sxs-lookup"><span data-stu-id="27212-119">The [**CryptEncrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencrypt) function takes the session key that was generated in the previous step and encrypts a buffer of data.</span></span>

    > [!Note]  
    > <span data-ttu-id="27212-120">À mesure que les données sont chiffrées, les données peuvent être légèrement développées par l’algorithme de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="27212-120">As the data is encrypted, the data may be slightly expanded by the encryption algorithm.</span></span> <span data-ttu-id="27212-121">L’application est responsable de la mémorisation de la longueur des données chiffrées afin que la longueur appropriée puisse être spécifiée ultérieurement pour la fonction [**CryptDecrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecrypt) .</span><span class="sxs-lookup"><span data-stu-id="27212-121">The application is responsible for remembering the length of the encrypted data so the proper length can later be specified for the [**CryptDecrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecrypt) function.</span></span>

     

5.  <span data-ttu-id="27212-122">Si vous le souhaitez, utilisez la fonction [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) pour permettre à l’utilisateur actuel de déchiffrer les données à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="27212-122">Optionally, use the [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) function to allow the current user to decrypt the data in the future.</span></span>

    <span data-ttu-id="27212-123">Pour permettre à l’utilisateur actuel de déchiffrer les données à l’avenir, la fonction [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) est utilisée pour enregistrer la clé de déchiffrement sous une forme chiffrée (un objet blob de clé) qui peut uniquement être déchiffrée avec la clé privée de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="27212-123">To allow the current user to decrypt the data in the future, the [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) function is used to save the decryption key in an encrypted form (a key BLOB) that can only be decrypted with the user's private key.</span></span> <span data-ttu-id="27212-124">Cette fonction requiert la clé publique d’échange de clés de l’utilisateur à cet effet, qui peut être obtenue à l’aide de la fonction [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) .</span><span class="sxs-lookup"><span data-stu-id="27212-124">This function requires the user's key exchange public key for this purpose, which can be obtained by using the [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) function.</span></span> <span data-ttu-id="27212-125">La fonction **CryptExportKey** retourne un objet blob de clé qui doit être stocké par l’application pour être utilisé dans le déchiffrement du fichier</span><span class="sxs-lookup"><span data-stu-id="27212-125">The **CryptExportKey** function will return a key BLOB that must be stored by the application for use in decrypting the file</span></span>

> [!Note]  
> <span data-ttu-id="27212-126">Si l’application possède des certificats (ou des clés publiques) pour d’autres utilisateurs, elle peut permettre à d’autres utilisateurs de déchiffrer le fichier en effectuant des appels [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) pour chaque utilisateur qui doit recevoir l’accès.</span><span class="sxs-lookup"><span data-stu-id="27212-126">If the application has certificates (or public keys) for other users, it can permit other users to decrypt the file by performing [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) calls for each user who should receive access.</span></span> <span data-ttu-id="27212-127">Les objets BLOB de clé retournés doivent être stockés par l’application, comme à l’étape 5.</span><span class="sxs-lookup"><span data-stu-id="27212-127">The returned key BLOBs must be stored by the application, as in step 5.</span></span>

 

## <a name="creating-an-encrypted-message"></a><span data-ttu-id="27212-128">Création d’un message chiffré</span><span class="sxs-lookup"><span data-stu-id="27212-128">Creating an Encrypted Message</span></span>

<span data-ttu-id="27212-129">Les fonctions de message simplifiées facilitent le chiffrement et le déchiffrement des données.</span><span class="sxs-lookup"><span data-stu-id="27212-129">The simplified message functions make it easier to encrypt and decrypt data.</span></span> <span data-ttu-id="27212-130">L’illustration suivante représente les tâches individuelles qui doivent être accomplies pour chiffrer un message.</span><span class="sxs-lookup"><span data-stu-id="27212-130">The following illustration depicts the individual tasks that must be accomplished to encrypt a message.</span></span> <span data-ttu-id="27212-131">Les étapes sont décrites dans la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="27212-131">The steps are described in the following list.</span></span>

![chiffrement d’un message](images/encmsg.png)

<span data-ttu-id="27212-133">**Pour chiffrer un message**</span><span class="sxs-lookup"><span data-stu-id="27212-133">**To encrypt a message**</span></span>

1.  <span data-ttu-id="27212-134">Obtient un pointeur vers le message de texte en clair.</span><span class="sxs-lookup"><span data-stu-id="27212-134">Get a pointer to the plaintext message.</span></span>
2.  <span data-ttu-id="27212-135">Générez une clé symétrique (session).</span><span class="sxs-lookup"><span data-stu-id="27212-135">Generate a symmetric (session) key.</span></span>
3.  <span data-ttu-id="27212-136">À l’aide de la clé symétrique et de l’algorithme de chiffrement spécifié, chiffrez les données du message.</span><span class="sxs-lookup"><span data-stu-id="27212-136">Using the symmetric key and specified encryption algorithm, encrypt the message data.</span></span>
4.  <span data-ttu-id="27212-137">Ouvrez un magasin de certificats.</span><span class="sxs-lookup"><span data-stu-id="27212-137">Open a certificate store.</span></span>
5.  <span data-ttu-id="27212-138">Obtient le certificat du destinataire.</span><span class="sxs-lookup"><span data-stu-id="27212-138">Get the recipient's certificate.</span></span>
6.  <span data-ttu-id="27212-139">Récupération de la clé publique à partir du certificat du destinataire.</span><span class="sxs-lookup"><span data-stu-id="27212-139">Get the public key from the recipient's certificate.</span></span>
7.  <span data-ttu-id="27212-140">À l’aide de la clé publique du destinataire, chiffrez la clé symétrique.</span><span class="sxs-lookup"><span data-stu-id="27212-140">Using the recipient's public key, encrypt the symmetric key.</span></span>
8.  <span data-ttu-id="27212-141">Obtient l’identificateur du destinataire à partir du certificat du destinataire.</span><span class="sxs-lookup"><span data-stu-id="27212-141">Get the recipient's identifier from the recipient's certificate.</span></span>
9.  <span data-ttu-id="27212-142">Incluez ce qui suit dans le message enveloppé numériquement : l’algorithme de chiffrement des données, les données chiffrées, la clé symétrique chiffrée et l’identificateur du destinataire.</span><span class="sxs-lookup"><span data-stu-id="27212-142">Include the following in the digitally enveloped message: the data encryption algorithm, the encrypted data, the encrypted symmetric key, and the recipient identifier.</span></span>

 

 



