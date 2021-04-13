---
description: Explique comment générer, échanger, importer et exporter des clés de Diffie-Hellman.
ms.assetid: 623a8c9e-3f6a-470b-be30-dec13342bb90
title: Clés de Diffie-Hellman
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f00eaddd580ac74e18e26498175f87b5d81b8e20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104321034"
---
# <a name="diffie-hellman-keys"></a><span data-ttu-id="e2122-103">Clés de Diffie-Hellman</span><span class="sxs-lookup"><span data-stu-id="e2122-103">Diffie-Hellman Keys</span></span>

-   [<span data-ttu-id="e2122-104">Génération de clés de Diffie-Hellman</span><span class="sxs-lookup"><span data-stu-id="e2122-104">Generating Diffie-Hellman Keys</span></span>](#generating-diffie-hellman-keys)
-   [<span data-ttu-id="e2122-105">Échange de clés de Diffie-Hellman</span><span class="sxs-lookup"><span data-stu-id="e2122-105">Exchanging Diffie-Hellman Keys</span></span>](#exchanging-diffie-hellman-keys)
-   [<span data-ttu-id="e2122-106">Exportation d’une clé privée Diffie-Hellman</span><span class="sxs-lookup"><span data-stu-id="e2122-106">Exporting a Diffie-Hellman Private Key</span></span>](#exporting-a-diffie-hellman-private-key)
-   [<span data-ttu-id="e2122-107">Exemple de code</span><span class="sxs-lookup"><span data-stu-id="e2122-107">Example Code</span></span>](#example-code)

## <a name="generating-diffie-hellman-keys"></a><span data-ttu-id="e2122-108">Génération de clés de Diffie-Hellman</span><span class="sxs-lookup"><span data-stu-id="e2122-108">Generating Diffie-Hellman Keys</span></span>

<span data-ttu-id="e2122-109">Pour générer une clé de Diffie-Hellman, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="e2122-109">To generate a Diffie-Hellman key, perform the following steps:</span></span>

1.  <span data-ttu-id="e2122-110">Appelez la fonction [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) pour obtenir un descripteur du fournisseur de services de chiffrement Microsoft Diffie-Hellman.</span><span class="sxs-lookup"><span data-stu-id="e2122-110">Call the [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) function to get a handle to the Microsoft Diffie-Hellman Cryptographic Provider.</span></span>
2.  <span data-ttu-id="e2122-111">Générez la nouvelle clé.</span><span class="sxs-lookup"><span data-stu-id="e2122-111">Generate the new key.</span></span> <span data-ttu-id="e2122-112">Il existe deux façons de procéder : en demandant à CryptoAPI de générer toutes les nouvelles valeurs pour G, P et X ou en utilisant des valeurs existantes pour G et P, et en générant une nouvelle valeur pour X.</span><span class="sxs-lookup"><span data-stu-id="e2122-112">There are two ways to accomplish this—by having CryptoAPI generate all new values for G, P, and X or by using existing values for G and P, and generating a new value for X.</span></span>

    <span data-ttu-id="e2122-113">**Pour générer la clé en générant toutes les nouvelles valeurs**</span><span class="sxs-lookup"><span data-stu-id="e2122-113">**To generate the key by generating all new values**</span></span>

    1.  <span data-ttu-id="e2122-114">Appelez la fonction [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) , en transmettant **CALG \_ DH \_ DF** (Store et Forward) ou **CALG \_ DH \_ EPHEM** (éphémère) dans le paramètre *algid* .</span><span class="sxs-lookup"><span data-stu-id="e2122-114">Call the [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) function, passing either **CALG\_DH\_SF** (store and forward) or **CALG\_DH\_EPHEM** (ephemeral) in the *Algid* parameter.</span></span> <span data-ttu-id="e2122-115">La clé sera générée à l’aide de nouvelles valeurs aléatoires pour G et P, une nouvelle valeur calculée pour X et sa poignée sera retournée dans le paramètre *phKey* .</span><span class="sxs-lookup"><span data-stu-id="e2122-115">The key will be generated using new, random values for G and P, a newly calculated value for X, and its handle will be returned in the *phKey* parameter.</span></span>
    2.  <span data-ttu-id="e2122-116">La nouvelle clé est maintenant prête à être utilisée.</span><span class="sxs-lookup"><span data-stu-id="e2122-116">The new key is now ready for use.</span></span> <span data-ttu-id="e2122-117">Les valeurs de G et P doivent être envoyées au destinataire avec la clé (ou envoyées par une autre méthode) lors d’un échange de [*clés*](../secgloss/e-gly.md).</span><span class="sxs-lookup"><span data-stu-id="e2122-117">The values of G and P must be sent to the recipient along with the key (or sent by some other method) when doing a [*key exchange*](../secgloss/e-gly.md).</span></span>

    <span data-ttu-id="e2122-118">**Pour générer la clé à l’aide de valeurs prédéfinies pour G et P**</span><span class="sxs-lookup"><span data-stu-id="e2122-118">**To generate the key by using predefined values for G and P**</span></span>

    1.  <span data-ttu-id="e2122-119">Appelez [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) en transmettant **CALG \_ DH \_ DF** (Store et Forward) **ou \_ CALG \_ DH EPHEM** (éphémère) dans le paramètre *algid* et **crypt \_ PREGEN** pour le paramètre *dwFlags* .</span><span class="sxs-lookup"><span data-stu-id="e2122-119">Call [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) passing either **CALG\_DH\_SF** (store and forward) or **CALG\_DH\_EPHEM** (ephemeral) in the *Algid* parameter and **CRYPT\_PREGEN** for the *dwFlags* parameter.</span></span> <span data-ttu-id="e2122-120">Un handle de clé sera généré et retourné dans le paramètre *phKey* .</span><span class="sxs-lookup"><span data-stu-id="e2122-120">A key handle will be generated and returned in the *phKey* parameter.</span></span>
    2.  <span data-ttu-id="e2122-121">Initialisez une structure d' [**\_ \_ objet blob de données**](/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)) de chiffre avec le membre **PbData** défini sur la valeur P.</span><span class="sxs-lookup"><span data-stu-id="e2122-121">Initialize a [**CRYPT\_DATA\_BLOB**](/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)) structure with the **pbData** member set to the P value.</span></span> <span data-ttu-id="e2122-122">L' [*objet BLOB*](../secgloss/b-gly.md) ne contient pas d’informations d’en-tête et le membre **pbData** est au format [*Little endian*](../secgloss/l-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="e2122-122">The [*BLOB*](../secgloss/b-gly.md) contains no header information and the **pbData** member is in [*little-endian*](../secgloss/l-gly.md) format.</span></span>
    3.  <span data-ttu-id="e2122-123">La valeur de P est définie en appelant la fonction [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) , en passant le handle de clé récupéré à l’étape a dans le paramètre *HKEY* , l’indicateur **KP \_ P** dans le paramètre *dwParam* et un pointeur vers la structure qui contient la valeur de p dans le paramètre *pbData* .</span><span class="sxs-lookup"><span data-stu-id="e2122-123">The value of P is set by calling the [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) function, passing the key handle retrieved in step a in the *hKey* parameter, the **KP\_P** flag in the *dwParam* parameter, and a pointer to the structure that contains the value of P in the *pbData* parameter.</span></span>
    4.  <span data-ttu-id="e2122-124">Initialisez une structure d' [**\_ \_ objet blob de données**](/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)) de chiffre avec le membre **PbData** défini sur la valeur G.</span><span class="sxs-lookup"><span data-stu-id="e2122-124">Initialize a [**CRYPT\_DATA\_BLOB**](/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)) structure with the **pbData** member set to the G value.</span></span> <span data-ttu-id="e2122-125">L’objet BLOB ne contient pas d’informations d’en-tête et le membre **pbData** est au format Little endian.</span><span class="sxs-lookup"><span data-stu-id="e2122-125">The BLOB contains no header information and the **pbData** member is in little-endian format.</span></span>
    5.  <span data-ttu-id="e2122-126">La valeur de G est définie en appelant la fonction [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) , en passant le handle de clé récupéré à l’étape a dans le paramètre *HKEY* , l’indicateur **KP \_ g** dans le paramètre *dwParam* et un pointeur vers la structure qui contient la valeur de G dans le paramètre *pbData* .</span><span class="sxs-lookup"><span data-stu-id="e2122-126">The value of G is set by calling the [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) function, passing the key handle retrieved in step a in the *hKey* parameter, the **KP\_G** flag in the *dwParam* parameter, and a pointer to the structure that contains the value of G in the *pbData* parameter.</span></span>
    6.  <span data-ttu-id="e2122-127">La valeur de X est générée en appelant la fonction [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) , en passant le handle de clé récupéré à l’étape a dans le paramètre *HKEY* , l’indicateur **KP \_ X** dans le paramètre *DwParam* et la valeur **null** dans le paramètre *pbData* .</span><span class="sxs-lookup"><span data-stu-id="e2122-127">The value of X is generated by calling the [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) function, passing the key handle retrieved in step a in the *hKey* parameter, the **KP\_X** flag in the *dwParam* parameter, and **NULL** in the *pbData* parameter.</span></span>
    7.  <span data-ttu-id="e2122-128">Si tous les appels de fonction ont réussi, la clé publique Diffie-Hellman est prête à être utilisée.</span><span class="sxs-lookup"><span data-stu-id="e2122-128">If all the function calls succeeded, the Diffie-Hellman public key is ready for use.</span></span>

3.  <span data-ttu-id="e2122-129">Lorsque la clé n’est plus nécessaire, détruisez-la en passant le handle de clé à la fonction [**CryptDestroyKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey) .</span><span class="sxs-lookup"><span data-stu-id="e2122-129">When the key is no longer needed, destroy it by passing the key handle to the [**CryptDestroyKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey) function.</span></span>

<span data-ttu-id="e2122-130">Si **CALG \_ DH \_ DF** a été spécifié dans les procédures précédentes, les valeurs de clé sont conservées dans le stockage à chaque appel à [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam).</span><span class="sxs-lookup"><span data-stu-id="e2122-130">If **CALG\_DH\_SF** was specified in the previous procedures, the key values are persisted to storage with each call to [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam).</span></span> <span data-ttu-id="e2122-131">Les valeurs G et P peuvent ensuite être récupérées à l’aide de la fonction [**CryptGetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetkeyparam) .</span><span class="sxs-lookup"><span data-stu-id="e2122-131">The G and P values can then be retrieved by using the [**CryptGetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetkeyparam) function.</span></span> <span data-ttu-id="e2122-132">Certains fournisseurs de services de chiffrement peuvent avoir des valeurs G et P codées en dur.</span><span class="sxs-lookup"><span data-stu-id="e2122-132">Some CSPs may have hard-coded G and P values.</span></span> <span data-ttu-id="e2122-133">Dans ce cas, une erreur **\_ FIXEDPARAMETER NPD** est retournée si **CryptSetKeyParam** est appelé avec **KP \_ G** ou **KP \_ P** spécifié dans le paramètre *dwParam* .</span><span class="sxs-lookup"><span data-stu-id="e2122-133">In this case a **NTE\_FIXEDPARAMETER** error will be returned if **CryptSetKeyParam** is called with **KP\_G** or **KP\_P** specified in the *dwParam* parameter.</span></span> <span data-ttu-id="e2122-134">Si **CryptDestroyKey** est appelé, le handle de la clé est détruit, mais les valeurs de clé sont conservées dans le CSP.</span><span class="sxs-lookup"><span data-stu-id="e2122-134">If **CryptDestroyKey** is called, the handle to the key is destroyed, but the key values are retained in the CSP.</span></span> <span data-ttu-id="e2122-135">Toutefois, si **CALG \_ DH \_ EPHEM** a été spécifié, le descripteur de la clé est détruit et toutes les valeurs sont effacées du CSP.</span><span class="sxs-lookup"><span data-stu-id="e2122-135">However, if **CALG\_DH\_EPHEM** was specified, the handle to the key is destroyed, and all values are cleared from the CSP.</span></span>

## <a name="exchanging-diffie-hellman-keys"></a><span data-ttu-id="e2122-136">Échange de clés de Diffie-Hellman</span><span class="sxs-lookup"><span data-stu-id="e2122-136">Exchanging Diffie-Hellman Keys</span></span>

<span data-ttu-id="e2122-137">L’objectif de l’algorithme Diffie-Hellman est de permettre à deux ou plusieurs parties de créer et de partager une clé de session secrète identique en partageant des informations sur un réseau qui n’est pas sécurisé.</span><span class="sxs-lookup"><span data-stu-id="e2122-137">The purpose of the Diffie-Hellman algorithm is to make it possible for two or more parties to create and share an identical, secret session key by sharing information over a network that is not secure.</span></span> <span data-ttu-id="e2122-138">Les informations qui sont partagées sur le réseau se présente sous la forme de deux valeurs constantes et d’une Diffie-Hellman clé publique.</span><span class="sxs-lookup"><span data-stu-id="e2122-138">The information that gets shared over the network is in the form of a couple of constant values and a Diffie-Hellman public key.</span></span> <span data-ttu-id="e2122-139">Le processus utilisé par deux parties clés-Exchange est le suivant :</span><span class="sxs-lookup"><span data-stu-id="e2122-139">The process used by two key-exchange parties is as follows:</span></span>

-   <span data-ttu-id="e2122-140">Les deux parties acceptent les paramètres de Diffie-Hellman qui sont un nombre premier (P) et un numéro de générateur (G).</span><span class="sxs-lookup"><span data-stu-id="e2122-140">Both parties agree to the Diffie-Hellman parameters which are a prime number (P) and a generator number (G).</span></span>
-   <span data-ttu-id="e2122-141">Le tiers 1 envoie son Diffie-Hellman clé publique au tiers 2.</span><span class="sxs-lookup"><span data-stu-id="e2122-141">Party 1 sends its Diffie-Hellman public key to party 2.</span></span>
-   <span data-ttu-id="e2122-142">Le tiers 2 calcule la clé de session secrète à l’aide des informations contenues dans sa clé privée et la clé publique du tiers 1.</span><span class="sxs-lookup"><span data-stu-id="e2122-142">Party 2 computes the secret session key by using the information contained in its private key and party 1's public key.</span></span>
-   <span data-ttu-id="e2122-143">Le tiers 2 envoie son Diffie-Hellman clé publique au tiers 1.</span><span class="sxs-lookup"><span data-stu-id="e2122-143">Party 2 sends its Diffie-Hellman public key to party 1.</span></span>
-   <span data-ttu-id="e2122-144">Le tiers 1 calcule la clé de session secrète à l’aide des informations contenues dans sa clé privée et la clé publique du tiers 2.</span><span class="sxs-lookup"><span data-stu-id="e2122-144">Party 1 computes the secret session key by using the information contained in its private key and party 2's public key.</span></span>
-   <span data-ttu-id="e2122-145">Les deux parties ont désormais la même clé de session, qui peut être utilisée pour chiffrer et déchiffrer les données.</span><span class="sxs-lookup"><span data-stu-id="e2122-145">Both parties now have the same session key, which can be used for encrypting and decrypting data.</span></span> <span data-ttu-id="e2122-146">Les étapes nécessaires sont indiquées dans la procédure suivante.</span><span class="sxs-lookup"><span data-stu-id="e2122-146">The steps necessary for this are shown in the following procedure.</span></span>

<span data-ttu-id="e2122-147">**Pour préparer une clé publique Diffie-Hellman pour la transmission**</span><span class="sxs-lookup"><span data-stu-id="e2122-147">**To prepare a Diffie-Hellman public key for transmission**</span></span>

1.  <span data-ttu-id="e2122-148">Appelez la fonction [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) pour obtenir un descripteur du fournisseur de services de chiffrement Microsoft Diffie-Hellman.</span><span class="sxs-lookup"><span data-stu-id="e2122-148">Call the [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) function to get a handle to the Microsoft Diffie-Hellman Cryptographic Provider.</span></span>
2.  <span data-ttu-id="e2122-149">Créez une clé de Diffie-Hellman en appelant la fonction [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) pour créer une nouvelle clé ou en appelant la fonction [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) pour récupérer une clé existante.</span><span class="sxs-lookup"><span data-stu-id="e2122-149">Create a Diffie-Hellman key by calling the [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) function to create a new key, or by calling the [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) function to retrieve an existing key.</span></span>
3.  <span data-ttu-id="e2122-150">Obtenir la taille nécessaire pour contenir le Diffie-Hellman BLOB de clé en appelant [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey), en transmettant la **valeur null** pour le paramètre *pbData* .</span><span class="sxs-lookup"><span data-stu-id="e2122-150">Get the size needed to hold the Diffie-Hellman key BLOB by calling the [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey), passing **NULL** for the *pbData* parameter.</span></span> <span data-ttu-id="e2122-151">La taille requise est retournée dans *pdwDataLen*.</span><span class="sxs-lookup"><span data-stu-id="e2122-151">The required size will be returned in *pdwDataLen*.</span></span>
4.  <span data-ttu-id="e2122-152">Allouez de la mémoire pour l’objet BLOB de clé.</span><span class="sxs-lookup"><span data-stu-id="e2122-152">Allocate memory for the key BLOB.</span></span>
5.  <span data-ttu-id="e2122-153">Créez un [*objet blob de clé publique*](../secgloss/p-gly.md) Diffie-Hellman en appelant la fonction [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) , en passant **publicKeyBlob** dans le paramètre *dwBlobType* et le handle à la clé Diffie-Hellman dans le paramètre *HKEY* .</span><span class="sxs-lookup"><span data-stu-id="e2122-153">Create a Diffie-Hellman [*public key BLOB*](../secgloss/p-gly.md) by calling the [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) function, passing **PUBLICKEYBLOB** in the *dwBlobType* parameter and the handle to the Diffie-Hellman key in the *hKey* parameter.</span></span> <span data-ttu-id="e2122-154">Cet appel de fonction provoque le calcul de la valeur de la clé publique (G ^ X) mod P.</span><span class="sxs-lookup"><span data-stu-id="e2122-154">This function call causes the calculation of the public key value, (G^X) mod P.</span></span>
6.  <span data-ttu-id="e2122-155">Si tous les appels de fonction précédents ont réussi, le Diffie-Hellman objet BLOB de clé publique est maintenant prêt à être encodé et transmis.</span><span class="sxs-lookup"><span data-stu-id="e2122-155">If all the preceding function calls were successful, the Diffie-Hellman public key BLOB is now ready to be encoded and transmitted.</span></span>

<span data-ttu-id="e2122-156">**Pour importer une clé publique Diffie-Hellman et calculer la clé de session secrète**</span><span class="sxs-lookup"><span data-stu-id="e2122-156">**To import a Diffie-Hellman public key and calculate the secret session key**</span></span>

1.  <span data-ttu-id="e2122-157">Appelez la fonction [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) pour obtenir un descripteur du fournisseur de services de chiffrement Microsoft Diffie-Hellman.</span><span class="sxs-lookup"><span data-stu-id="e2122-157">Call the [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) function to get a handle to the Microsoft Diffie-Hellman Cryptographic Provider.</span></span>
2.  <span data-ttu-id="e2122-158">Créez une clé de Diffie-Hellman en appelant la fonction [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) pour créer une nouvelle clé ou en appelant la fonction [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) pour récupérer une clé existante.</span><span class="sxs-lookup"><span data-stu-id="e2122-158">Create a Diffie-Hellman key by calling the [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) function to create a new key, or by calling the [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) function to retrieve an existing key.</span></span>
3.  <span data-ttu-id="e2122-159">Pour importer la Diffie-Hellman clé publique dans le CSP, appelez la fonction [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) , en passant un pointeur vers l’objet blob de clé publique dans le paramètre *pbData* , la longueur de l’objet BLOB dans le paramètre *dwDataLen* et le descripteur de la clé Diffie-Hellman dans le paramètre *hPubKey* .</span><span class="sxs-lookup"><span data-stu-id="e2122-159">To import the Diffie-Hellman public key into the CSP, call the [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) function, passing a pointer to the public key BLOB in the *pbData* parameter, the length of the BLOB in the *dwDataLen* parameter, and the handle to the Diffie-Hellman key in the *hPubKey* parameter.</span></span> <span data-ttu-id="e2122-160">Le calcul, (Y ^ X) mod P, est alors effectué, créant ainsi la clé secrète partagée et effectuant l’échange de [*clés*](../secgloss/e-gly.md).</span><span class="sxs-lookup"><span data-stu-id="e2122-160">This causes the calculation, (Y^X) mod P, to be performed, thus creating the shared, secret key and completing the [*key exchange*](../secgloss/e-gly.md).</span></span> <span data-ttu-id="e2122-161">Cet appel de fonction retourne un handle vers la nouvelle clé secrète de session dans le paramètre *HKEY* .</span><span class="sxs-lookup"><span data-stu-id="e2122-161">This function call returns a handle to the new, secret, session key in the *hKey* parameter.</span></span>
4.  <span data-ttu-id="e2122-162">À ce stade, le Diffie-Hellman importé est de type **CALG \_ AGREEDKEY \_ any**.</span><span class="sxs-lookup"><span data-stu-id="e2122-162">At this point, the imported Diffie-Hellman is of type **CALG\_AGREEDKEY\_ANY**.</span></span> <span data-ttu-id="e2122-163">Avant de pouvoir utiliser la clé, celle-ci doit être convertie en un type de clé de session.</span><span class="sxs-lookup"><span data-stu-id="e2122-163">Before the key can be used, it must be converted into a session key type.</span></span> <span data-ttu-id="e2122-164">Pour ce faire, vous devez appeler la fonction [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) avec *DwParam* défini sur **KP \_ ALGID** et avec *pbData* défini sur un pointeur vers une valeur d' [**\_ ID ALG**](alg-id.md) qui représente une clé de session, par exemple **CALG \_ RC4**.</span><span class="sxs-lookup"><span data-stu-id="e2122-164">This is accomplished by calling the [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) function with *dwParam* set to **KP\_ALGID** and with *pbData* set to a pointer to a [**ALG\_ID**](alg-id.md) value that represents a session key, such as **CALG\_RC4**.</span></span> <span data-ttu-id="e2122-165">La clé doit être convertie avant d’utiliser la clé partagée dans la fonction [**CryptEncrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencrypt) ou [**CryptDecrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecrypt) .</span><span class="sxs-lookup"><span data-stu-id="e2122-165">The key must be converted before using the shared key in the [**CryptEncrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencrypt) or [**CryptDecrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecrypt) function.</span></span> <span data-ttu-id="e2122-166">Les appels passés à l’une de ces fonctions avant la conversion du type de clé échouent.</span><span class="sxs-lookup"><span data-stu-id="e2122-166">Calls made to either of these functions prior to converting the key type will fail.</span></span>
5.  <span data-ttu-id="e2122-167">La clé de session secrète est maintenant prête à être utilisée pour le chiffrement ou le déchiffrement.</span><span class="sxs-lookup"><span data-stu-id="e2122-167">The secret session key is now ready to be used for encryption or decryption.</span></span>
6.  <span data-ttu-id="e2122-168">Lorsque la clé n’est plus nécessaire, détruisez le handle de clé en appelant la fonction [**CryptDestroyKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey) .</span><span class="sxs-lookup"><span data-stu-id="e2122-168">When the key is no longer needed, destroy the key handle by calling the [**CryptDestroyKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey) function.</span></span>

## <a name="exporting-a-diffie-hellman-private-key"></a><span data-ttu-id="e2122-169">Exportation d’une clé privée Diffie-Hellman</span><span class="sxs-lookup"><span data-stu-id="e2122-169">Exporting a Diffie-Hellman Private Key</span></span>

<span data-ttu-id="e2122-170">Pour exporter une clé privée Diffie-Hellman, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="e2122-170">To export a Diffie-Hellman private key, perform the following steps:</span></span>

1.  <span data-ttu-id="e2122-171">Appelez la fonction [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) pour obtenir un descripteur du fournisseur de services de chiffrement Microsoft Diffie-Hellman.</span><span class="sxs-lookup"><span data-stu-id="e2122-171">Call the [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) function to get a handle to the Microsoft Diffie-Hellman Cryptographic Provider.</span></span>
2.  <span data-ttu-id="e2122-172">Créez une clé de Diffie-Hellman en appelant la fonction [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) pour créer une nouvelle clé ou en appelant la fonction [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) pour récupérer une clé existante.</span><span class="sxs-lookup"><span data-stu-id="e2122-172">Create a Diffie-Hellman key by calling the [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) function to create a new key, or by calling the [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) function to retrieve an existing key.</span></span>
3.  <span data-ttu-id="e2122-173">Créez un [*objet blob de clé privée*](../secgloss/p-gly.md) Diffie-Hellman en appelant la fonction [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) , en passant **PRIVATEKEYBLOB** dans le paramètre *dwBlobType* et le handle à la clé Diffie-Hellman dans le paramètre *HKEY* .</span><span class="sxs-lookup"><span data-stu-id="e2122-173">Create a Diffie-Hellman [*private key BLOB*](../secgloss/p-gly.md) by calling the [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) function, passing **PRIVATEKEYBLOB** in the *dwBlobType* parameter and the handle to the Diffie-Hellman key in the *hKey* parameter.</span></span>
4.  <span data-ttu-id="e2122-174">Lorsque le descripteur de clé n’est plus nécessaire, appelez la fonction [**CryptDestroyKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey) pour détruire le handle de clé.</span><span class="sxs-lookup"><span data-stu-id="e2122-174">When the key handle is no longer needed, call the [**CryptDestroyKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey) function to destroy the key handle.</span></span>

## <a name="example-code"></a><span data-ttu-id="e2122-175">Exemple de code</span><span class="sxs-lookup"><span data-stu-id="e2122-175">Example Code</span></span>

<span data-ttu-id="e2122-176">L’exemple suivant montre comment créer, exporter, importer et utiliser une clé de Diffie-Hellman pour effectuer un échange de clés.</span><span class="sxs-lookup"><span data-stu-id="e2122-176">The following example shows how to create, export, import, and use a Diffie-Hellman key to perform a key exchange.</span></span>


```C++
#include <tchar.h>
#include <windows.h>
#include <wincrypt.h>
#pragma comment(lib, "crypt32.lib")

// The key size, in bits.
#define DHKEYSIZE 512

// Prime in little-endian format.
static const BYTE g_rgbPrime[] = 
{
    0x91, 0x02, 0xc8, 0x31, 0xee, 0x36, 0x07, 0xec, 
    0xc2, 0x24, 0x37, 0xf8, 0xfb, 0x3d, 0x69, 0x49, 
    0xac, 0x7a, 0xab, 0x32, 0xac, 0xad, 0xe9, 0xc2, 
    0xaf, 0x0e, 0x21, 0xb7, 0xc5, 0x2f, 0x76, 0xd0, 
    0xe5, 0x82, 0x78, 0x0d, 0x4f, 0x32, 0xb8, 0xcb,
    0xf7, 0x0c, 0x8d, 0xfb, 0x3a, 0xd8, 0xc0, 0xea, 
    0xcb, 0x69, 0x68, 0xb0, 0x9b, 0x75, 0x25, 0x3d,
    0xaa, 0x76, 0x22, 0x49, 0x94, 0xa4, 0xf2, 0x8d 
};

// Generator in little-endian format.
static BYTE g_rgbGenerator[] = 
{
    0x02, 0x88, 0xd7, 0xe6, 0x53, 0xaf, 0x72, 0xc5,
    0x8c, 0x08, 0x4b, 0x46, 0x6f, 0x9f, 0x2e, 0xc4,
    0x9c, 0x5c, 0x92, 0x21, 0x95, 0xb7, 0xe5, 0x58, 
    0xbf, 0xba, 0x24, 0xfa, 0xe5, 0x9d, 0xcb, 0x71, 
    0x2e, 0x2c, 0xce, 0x99, 0xf3, 0x10, 0xff, 0x3b,
    0xcb, 0xef, 0x6c, 0x95, 0x22, 0x55, 0x9d, 0x29,
    0x00, 0xb5, 0x4c, 0x5b, 0xa5, 0x63, 0x31, 0x41,
    0x13, 0x0a, 0xea, 0x39, 0x78, 0x02, 0x6d, 0x62
};

BYTE g_rgbData[] = {0x01, 0x02, 0x03, 0x04,    0x05, 0x06, 0x07, 0x08};

int _tmain(int argc, _TCHAR* argv[])
{
    UNREFERENCED_PARAMETER(argc);
    UNREFERENCED_PARAMETER(argv);
    
    BOOL fReturn;
    HCRYPTPROV hProvParty1 = NULL; 
    HCRYPTPROV hProvParty2 = NULL; 
    DATA_BLOB P;
    DATA_BLOB G;
    HCRYPTKEY hPrivateKey1 = NULL;
    HCRYPTKEY hPrivateKey2 = NULL;
    PBYTE pbKeyBlob1 = NULL;
    PBYTE pbKeyBlob2 = NULL;
    HCRYPTKEY hSessionKey1 = NULL;
    HCRYPTKEY hSessionKey2 = NULL;
    PBYTE pbData = NULL;

    /************************
    Construct data BLOBs for the prime and generator. The P and G 
    values, represented by the g_rgbPrime and g_rgbGenerator arrays 
    respectively, are shared values that have been agreed to by both 
    parties.
    ************************/
    P.cbData = DHKEYSIZE/8;
    P.pbData = (BYTE*)(g_rgbPrime);

    G.cbData = DHKEYSIZE/8;
    G.pbData = (BYTE*)(g_rgbGenerator);

    /************************
    Create the private Diffie-Hellman key for party 1. 
    ************************/
    // Acquire a provider handle for party 1.
    fReturn = CryptAcquireContext(
        &hProvParty1, 
        NULL,
        MS_ENH_DSS_DH_PROV,
        PROV_DSS_DH, 
        CRYPT_VERIFYCONTEXT);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Create an ephemeral private key for party 1.
    fReturn = CryptGenKey(
        hProvParty1, 
        CALG_DH_EPHEM, 
        DHKEYSIZE << 16 | CRYPT_EXPORTABLE | CRYPT_PREGEN,
        &hPrivateKey1);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Set the prime for party 1's private key.
    fReturn = CryptSetKeyParam(
        hPrivateKey1,
        KP_P,
        (PBYTE)&P,
        0);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Set the generator for party 1's private key.
    fReturn = CryptSetKeyParam(
        hPrivateKey1,
        KP_G,
        (PBYTE)&G,
        0);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Generate the secret values for party 1's private key.
    fReturn = CryptSetKeyParam(
        hPrivateKey1,
        KP_X,
        NULL,
        0);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    /************************
    Create the private Diffie-Hellman key for party 2. 
    ************************/
    // Acquire a provider handle for party 2.
    fReturn = CryptAcquireContext(
        &hProvParty2, 
        NULL,
        MS_ENH_DSS_DH_PROV,
        PROV_DSS_DH, 
        CRYPT_VERIFYCONTEXT);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Create an ephemeral private key for party 2.
    fReturn = CryptGenKey(
        hProvParty2, 
        CALG_DH_EPHEM, 
        DHKEYSIZE << 16 | CRYPT_EXPORTABLE | CRYPT_PREGEN,
        &hPrivateKey2);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Set the prime for party 2's private key.
    fReturn = CryptSetKeyParam(
        hPrivateKey2,
        KP_P,
        (PBYTE)&P,
        0);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Set the generator for party 2's private key.
    fReturn = CryptSetKeyParam(
        hPrivateKey2,
        KP_G,
        (PBYTE)&G,
        0);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Generate the secret values for party 2's private key.
    fReturn = CryptSetKeyParam(
        hPrivateKey2,
        KP_X,
        NULL,
        0);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    /************************
    Export Party 1's public key.
    ************************/
    // Public key value, (G^X) mod P is calculated.
    DWORD dwDataLen1;

    // Get the size for the key BLOB.
    fReturn = CryptExportKey(
        hPrivateKey1,
        NULL,
        PUBLICKEYBLOB,
        0,
        NULL,
        &dwDataLen1);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Allocate the memory for the key BLOB.
    if(!(pbKeyBlob1 = (PBYTE)malloc(dwDataLen1)))
    { 
        goto ErrorExit;
    }

    // Get the key BLOB.
    fReturn = CryptExportKey(
        hPrivateKey1,
        0,
        PUBLICKEYBLOB,
        0,
        pbKeyBlob1,
        &dwDataLen1);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    /************************
    Export Party 2's public key.
    ************************/
    // Public key value, (G^X) mod P is calculated.
    DWORD dwDataLen2;

    // Get the size for the key BLOB.
    fReturn = CryptExportKey(
        hPrivateKey2,
        NULL,
        PUBLICKEYBLOB,
        0,
        NULL,
        &dwDataLen2);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Allocate the memory for the key BLOB.
    if(!(pbKeyBlob2 = (PBYTE)malloc(dwDataLen2)))
    { 
        goto ErrorExit;
    }

    // Get the key BLOB.
    fReturn = CryptExportKey(
        hPrivateKey2,
        0,
        PUBLICKEYBLOB,
        0,
        pbKeyBlob2,
        &dwDataLen2);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    /************************
    Party 1 imports party 2's public key.
    The imported key will contain the new shared secret 
    key (Y^X) mod P. 
    ************************/
    fReturn = CryptImportKey(
        hProvParty1,
        pbKeyBlob2,
        dwDataLen2,
        hPrivateKey1,
        0,
        &hSessionKey2);
    if(!fReturn)
    {
        goto ErrorExit;
    }
    
    /************************
    Party 2 imports party 1's public key.
    The imported key will contain the new shared secret 
    key (Y^X) mod P. 
    ************************/
    fReturn = CryptImportKey(
        hProvParty2,
        pbKeyBlob1,
        dwDataLen1,
        hPrivateKey2,
        0,
        &hSessionKey1);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    /************************
    Convert the agreed keys to symmetric keys. They are currently of 
    the form CALG_AGREEDKEY_ANY. Convert them to CALG_RC4.
    ************************/
    ALG_ID Algid = CALG_RC4;

    // Enable the party 1 public session key for use by setting the 
    // ALGID.
    fReturn = CryptSetKeyParam(
        hSessionKey1,
        KP_ALGID,
        (PBYTE)&Algid,
        0);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Enable the party 2 public session key for use by setting the 
    // ALGID.
    fReturn = CryptSetKeyParam(
        hSessionKey2,
        KP_ALGID,
        (PBYTE)&Algid,
        0);
    if(!fReturn)
    {
        goto ErrorExit;
    }

    /************************
    Encrypt some data with party 1's session key. 
    ************************/
    // Get the size.
    DWORD dwLength = sizeof(g_rgbData);
    fReturn = CryptEncrypt(
        hSessionKey1, 
        0, 
        TRUE,
        0, 
        NULL, 
        &dwLength,
        sizeof(g_rgbData));
    if(!fReturn)
    {
        goto ErrorExit;
    }

    // Allocate a buffer to hold the encrypted data.
    pbData = (PBYTE)malloc(dwLength);
    if(!pbData)
    {
        goto ErrorExit;
    }

    // Copy the unencrypted data to the buffer. The data will be 
    // encrypted in place.
    memcpy(pbData, g_rgbData, sizeof(g_rgbData)); 

    // Encrypt the data.
    dwLength = sizeof(g_rgbData);
    fReturn = CryptEncrypt(
        hSessionKey1, 
        0, 
        TRUE,
        0, 
        pbData, 
        &dwLength,
        sizeof(g_rgbData));
    if(!fReturn)
    {
        goto ErrorExit;
    }
  
    /************************
    Decrypt the data with party 2's session key. 
    ************************/
    dwLength = sizeof(g_rgbData);
    fReturn = CryptDecrypt(
        hSessionKey2,
        0,
        TRUE,
        0,
        pbData,
        &dwLength);
    if(!fReturn)
    {
        goto ErrorExit;
    }


ErrorExit:
    if(pbData)
    {
        free(pbData);
        pbData = NULL;
    }

    if(hSessionKey2)
    {
        CryptDestroyKey(hSessionKey2);
        hSessionKey2 = NULL;
    }

    if(hSessionKey1)
    {
        CryptDestroyKey(hSessionKey1);
        hSessionKey1 = NULL;
    }

    if(pbKeyBlob2)
    {
        free(pbKeyBlob2);
        pbKeyBlob2 = NULL;
    }

    if(pbKeyBlob1)
    {
        free(pbKeyBlob1);
        pbKeyBlob1 = NULL;
    }

    if(hPrivateKey2)
    {
        CryptDestroyKey(hPrivateKey2);
        hPrivateKey2 = NULL;
    }

    if(hPrivateKey1)
    {
        CryptDestroyKey(hPrivateKey1);
        hPrivateKey1 = NULL;
    }

    if(hProvParty2)
    {
        CryptReleaseContext(hProvParty2, 0);
        hProvParty2 = NULL;
    }

    if(hProvParty1)
    {
        CryptReleaseContext(hProvParty1, 0);
        hProvParty1 = NULL;
    }

    return 0;
}
```



 

 
