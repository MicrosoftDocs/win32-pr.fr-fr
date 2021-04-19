---
description: Listes de révocation de certificat
ms.assetid: 146e7e4a-4281-4f5c-8346-d6c0d5f5442f
title: Listes de révocation de certificat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b51ddee9f77b147d69b8895b3335d41e041da7f2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106514908"
---
# <a name="certificate-revocation-lists"></a><span data-ttu-id="224b6-103">Listes de révocation de certificat</span><span class="sxs-lookup"><span data-stu-id="224b6-103">Certificate Revocation Lists</span></span>

<span data-ttu-id="224b6-104">Cette rubrique explique comment examiner la liste de révocation de certificats (CRL) pour les pilotes révoqués lors de l’utilisation du protocole COPP (Certified Output Protection Protocol).</span><span class="sxs-lookup"><span data-stu-id="224b6-104">This topic describes how to examine the certificate revocation list (CRL) for revoked drivers when using Certified Output Protection Protocol (COPP).</span></span>

<span data-ttu-id="224b6-105">La liste de révocation de certificats contient des résumés de certificats révoqués et peut être fournie et signée uniquement par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="224b6-105">The CRL contains digests of revoked certificates and can be provided and signed only by Microsoft.</span></span> <span data-ttu-id="224b6-106">La liste de révocation des certificats est distribuée via des licences DRM (Digital Rights Management).</span><span class="sxs-lookup"><span data-stu-id="224b6-106">The CRL is distributed through digital rights management (DRM) licenses.</span></span> <span data-ttu-id="224b6-107">La liste de révocation de certificats peut révoquer n’importe quel certificat dans la chaîne de certificats du pilote.</span><span class="sxs-lookup"><span data-stu-id="224b6-107">The CRL can revoke any certificate in the driver's certificates chain.</span></span> <span data-ttu-id="224b6-108">Si un certificat de la chaîne est révoqué, ce certificat et tous les certificats situés au-dessous de lui dans la chaîne sont également révoqués.</span><span class="sxs-lookup"><span data-stu-id="224b6-108">If any certificate in the chain is revoked, then that certificate and all of the certificates below it in the chain are also revoked.</span></span>

<span data-ttu-id="224b6-109">Pour récupérer la liste de révocation de certificats, l’application doit utiliser le kit de développement logiciel (SDK) Windows Media format, version 9 ou ultérieure, et effectuer les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="224b6-109">To get the CRL, the application must use the Windows Media Format SDK, version 9 or later, and perform the following steps:</span></span>

1.  <span data-ttu-id="224b6-110">Appelez **WMCreateReader** pour créer l’objet lecteur du kit de développement logiciel (SDK) du format Windows Media.</span><span class="sxs-lookup"><span data-stu-id="224b6-110">Call **WMCreateReader** to create the Windows Media Format SDK reader object.</span></span>
2.  <span data-ttu-id="224b6-111">Interrogez l’objet lecteur de l’interface **IWMDRMReader** .</span><span class="sxs-lookup"><span data-stu-id="224b6-111">Query the reader object for the **IWMDRMReader** interface.</span></span>
3.  <span data-ttu-id="224b6-112">Appelez **IWMDRMReader :: GetDRMProperty** avec la valeur g \_ wszWMDRMNet \_ Revocation pour obtenir la liste de révocation de certificats.</span><span class="sxs-lookup"><span data-stu-id="224b6-112">Call **IWMDRMReader::GetDRMProperty** with a value of g\_wszWMDRMNet\_Revocation to get the CRL.</span></span> <span data-ttu-id="224b6-113">Vous devez appeler cette méthode deux fois : une fois pour récupérer la taille de la mémoire tampon à allouer, et une fois pour remplir la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="224b6-113">You must call this method twice: Once to get the size of the buffer to allocate, and once to fill the buffer.</span></span> <span data-ttu-id="224b6-114">Le deuxième appel retourne une chaîne qui contient la liste de révocation de certificats.</span><span class="sxs-lookup"><span data-stu-id="224b6-114">The second call returns a string that contains the CRL.</span></span> <span data-ttu-id="224b6-115">La chaîne entière est encodée en base-64.</span><span class="sxs-lookup"><span data-stu-id="224b6-115">The entire string is base-64 encoded.</span></span>
4.  <span data-ttu-id="224b6-116">Décodez la chaîne codée en base 64.</span><span class="sxs-lookup"><span data-stu-id="224b6-116">Decode the base-64 encoded string.</span></span> <span data-ttu-id="224b6-117">Pour ce faire, vous pouvez utiliser la fonction **CryptStringToBinary** .</span><span class="sxs-lookup"><span data-stu-id="224b6-117">You can use the **CryptStringToBinary** function to do this.</span></span> <span data-ttu-id="224b6-118">Cette fonction fait partie de CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="224b6-118">This function is part of CryptoAPI.</span></span>

> [!Note]  
> <span data-ttu-id="224b6-119">Pour utiliser l’interface **IWMDRMReader** , vous devez obtenir une bibliothèque DRM statique auprès de Microsoft et lier votre application à ce fichier de bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="224b6-119">To use the **IWMDRMReader** interface, you must obtain a static DRM library from Microsoft and link your application to this library file.</span></span> <span data-ttu-id="224b6-120">Pour plus d’informations, consultez la rubrique « obtention de la bibliothèque DRM requise » dans la documentation du kit de développement logiciel (SDK) Windows Media format.</span><span class="sxs-lookup"><span data-stu-id="224b6-120">For more information, see the topic "Obtaining the Required DRM Library" in the Windows Media Format SDK documentation.</span></span>

 

<span data-ttu-id="224b6-121">Si la liste de révocation de certificats n’est pas présente sur l’ordinateur de l’utilisateur, la méthode **GetDRMProperty** retourne la \_ propriété NS E DRM non \_ \_ prise en charge \_ .</span><span class="sxs-lookup"><span data-stu-id="224b6-121">If the CRL is not present on the user's computer, the **GetDRMProperty** method returns NS\_E\_DRM\_UNSUPPORTED\_PROPERTY.</span></span> <span data-ttu-id="224b6-122">Actuellement, la seule façon d’obtenir la liste de révocation de certificats consiste à acquérir une licence DRM.</span><span class="sxs-lookup"><span data-stu-id="224b6-122">Currently, the only way to obtain the CRL is to acquire a DRM license.</span></span>

<span data-ttu-id="224b6-123">Le code suivant illustre une fonction qui retourne la liste de révocation de certificats :</span><span class="sxs-lookup"><span data-stu-id="224b6-123">The following code shows a function that returns the CRL:</span></span>


```C++
////////////////////////////////////////////////////////////////////////
//  Name: GetCRL
//  Description: Gets the certificate revocation list (CRL).
//
//  ppBuffer: Receives a pointer to the buffer that contains the CRL.
//  pcbBuffer: Receives the size of the buffer returned in ppBuffer.
//
//  The caller must free the returned buffer by calling CoTaskMemFree.
////////////////////////////////////////////////////////////////////////
HRESULT GetCRL(BYTE **ppBuffer, DWORD *pcbBuffer)
{
    IWMReader *pReader = NULL;
    IWMDRMReader *pDrmReader = NULL;
    HRESULT hr = S_OK;

    // DRM attribute data.
    WORD cbAttributeLength = 0;
    BYTE *pDataBase64 = NULL;
    WMT_ATTR_DATATYPE type;

    // Buffer for base-64 decoded CRL.
    BYTE *pCRL = NULL;
    DWORD cbCRL = 0;

    // Create the WMReader object.
    hr = WMCreateReader(NULL, 0, &pReader);

    // Query for the IWMDRMReader interface.
    if (SUCCEEDED(hr))
    {
        hr = pReader->QueryInterface(
            IID_IWMDRMReader, (void**)&pDrmReader);
    }

    // Call GetDRMProperty once to find the size of the buffer.
    if (SUCCEEDED(hr))
    {
        hr = pDrmReader->GetDRMProperty(
            g_wszWMDRMNET_Revocation,
            &type,
            NULL,
            &cbAttributeLength
            );
    }

    // Allocate a buffer.
    if (SUCCEEDED(hr))
    {
        pDataBase64 = (BYTE*)CoTaskMemAlloc(cbAttributeLength);
        if (pDataBase64 == NULL)
        {
            hr = E_OUTOFMEMORY;
        }
    }

    // Call GetDRMProperty again to get the property.
    if (SUCCEEDED(hr))
    {
        hr = pDrmReader->GetDRMProperty(
            g_wszWMDRMNET_Revocation,
            &type,
            pDataBase64,
            &cbAttributeLength
            );
    }

    // Find the size of the buffer for the base-64 decoding.
    if (SUCCEEDED(hr))
    {
        BOOL bResult = CryptStringToBinary(
            (WCHAR*)pDataBase64,    // Base-64 encoded string.
            0,                      // Null-terminated.
            CRYPT_STRING_BASE64,    
            NULL,                   // Buffer (NULL).
            &cbCRL,                 // Receives the size of the buffer. 
            NULL, NULL              // Optional.
            );
        if (!bResult)
        {
            hr = __HRESULT_FROM_WIN32(GetLastError());
        }
    }

    // Allocate a buffer for the CRL.
    if (SUCCEEDED(hr))
    {
        pCRL = (BYTE*)CoTaskMemAlloc(cbCRL);
        if (pCRL == NULL)
        {
            hr = E_OUTOFMEMORY;
        }
    }

    // Base-64 decode to get the CRL.
    if (SUCCEEDED(hr))
    {
        BOOL bResult = CryptStringToBinary(
            (WCHAR*)pDataBase64,    // Base-64 encoded string.
            0,                      // Null-terminated.
            CRYPT_STRING_BASE64,    
            pCRL,                   // Buffer.
            &cbCRL,                 // Receives the size of the buffer. 
            NULL, NULL              // Optional.
            );
        if (!bResult)
        {
            hr = __HRESULT_FROM_WIN32(GetLastError());
        }
    }

    // Return the buffer to the caller. Caller must free the buffer.
    if (SUCCEEDED(hr))
    {
        *ppBuffer = pCRL;
        *pcbBuffer = cbCRL;
    }
    else
    {
        CoTaskMemFree(pCRL);
    }

    CoTaskMemFree(pDataBase64);
    SAFE_RELEASE(pReader);
    SAFE_RELEASE(pDrmReader);
    return hr;
}
```



<span data-ttu-id="224b6-124">Ensuite, l’application doit vérifier que la liste de révocation de certificats est valide.</span><span class="sxs-lookup"><span data-stu-id="224b6-124">Next, the application must verify that the CRL is valid.</span></span> <span data-ttu-id="224b6-125">Pour ce faire, vérifiez que le certificat de liste de révocation de certificats, qui fait partie de la liste de révocation de certificats, est directement signé par le certificat racine Microsoft et que la valeur de l’élément SignCRL est définie sur 1.</span><span class="sxs-lookup"><span data-stu-id="224b6-125">To do so, verify that the CRL certificate, which is part of the CRL, is directly signed by the Microsoft Root Certificate and has the SignCRL element value set to 1.</span></span> <span data-ttu-id="224b6-126">Vérifiez également la signature de la liste de révocation de certificats.</span><span class="sxs-lookup"><span data-stu-id="224b6-126">Also, verify the signature of the CRL.</span></span>

<span data-ttu-id="224b6-127">Une fois la liste de révocation de certificats vérifiée, l’application peut la stocker.</span><span class="sxs-lookup"><span data-stu-id="224b6-127">After the CRL is verified, the application can store it.</span></span> <span data-ttu-id="224b6-128">Le numéro de version de la liste de révocation de certificats doit également être vérifié avant le stockage, afin que l’application stocke toujours la version la plus récente.</span><span class="sxs-lookup"><span data-stu-id="224b6-128">The CRL version number should also be checked before storing so that the application always stores the newest version.</span></span>

<span data-ttu-id="224b6-129">La liste de révocation de certificats a le format suivant.</span><span class="sxs-lookup"><span data-stu-id="224b6-129">The CRL has the following format.</span></span>



| <span data-ttu-id="224b6-130">Section</span><span class="sxs-lookup"><span data-stu-id="224b6-130">Section</span></span>            | <span data-ttu-id="224b6-131">Contents</span><span class="sxs-lookup"><span data-stu-id="224b6-131">Contents</span></span>                                                             |
|--------------------|----------------------------------------------------------------------|
| <span data-ttu-id="224b6-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="224b6-132">Header</span></span>             | <span data-ttu-id="224b6-133">version32 : nombre d’entrées de la liste de révocation de certificats 32 bits</span><span class="sxs-lookup"><span data-stu-id="224b6-133">32-bit CRL version32-bit number of entries</span></span>                           |
| <span data-ttu-id="224b6-134">Entrées de révocation</span><span class="sxs-lookup"><span data-stu-id="224b6-134">Revocation Entries</span></span> | <span data-ttu-id="224b6-135">Plusieurs entrées de révocation de 160 bits</span><span class="sxs-lookup"><span data-stu-id="224b6-135">Multiple 160-bit revocation entries</span></span>                                  |
| <span data-ttu-id="224b6-136">Certificat</span><span class="sxs-lookup"><span data-stu-id="224b6-136">Certificate</span></span>        | <span data-ttu-id="224b6-137">certificat lengthVariable-longueur de certificat 32</span><span class="sxs-lookup"><span data-stu-id="224b6-137">32-bit certificate lengthVariable-length certificate</span></span>                 |
| <span data-ttu-id="224b6-138">Signature</span><span class="sxs-lookup"><span data-stu-id="224b6-138">Signature</span></span>          | <span data-ttu-id="224b6-139">signature 8 bits type16-bit signature lengthVariable-length signature</span><span class="sxs-lookup"><span data-stu-id="224b6-139">8-bit signature type16-bit signature lengthVariable-length signature</span></span> |



 

> [!Note]  
> <span data-ttu-id="224b6-140">Toutes les valeurs entières sont non signées et sont représentées par une notation Big-endian (ordre d’octet réseau).</span><span class="sxs-lookup"><span data-stu-id="224b6-140">All integer values are unsigned and are represented in big-endian (network byte order) notation.</span></span>

 

<span data-ttu-id="224b6-141">Descriptions des sections CRL</span><span class="sxs-lookup"><span data-stu-id="224b6-141">CRL Section Descriptions</span></span>

<dl> <dt>

<span data-ttu-id="224b6-142"><span id="Header"></span><span id="header"></span><span id="HEADER"></span>Titre</span><span class="sxs-lookup"><span data-stu-id="224b6-142"><span id="Header"></span><span id="header"></span><span id="HEADER"></span>Header</span></span>
</dt> <dd>

<span data-ttu-id="224b6-143">L’en-tête contient le numéro de version de la liste de révocation de certificats et le nombre d’entrées de révocation dans la liste de révocation de certificats.</span><span class="sxs-lookup"><span data-stu-id="224b6-143">The header contains the version number of the CRL and the number of revocation entries in the CRL.</span></span> <span data-ttu-id="224b6-144">Une liste de révocation de certificats peut contenir zéro ou plusieurs entrées.</span><span class="sxs-lookup"><span data-stu-id="224b6-144">A CRL can contain zero or more entries.</span></span>

</dd> <dt>

<span data-ttu-id="224b6-145"><span id="Revocation_entries"></span><span id="revocation_entries"></span><span id="REVOCATION_ENTRIES"></span>Entrées de révocation</span><span class="sxs-lookup"><span data-stu-id="224b6-145"><span id="Revocation_entries"></span><span id="revocation_entries"></span><span id="REVOCATION_ENTRIES"></span>Revocation entries</span></span>
</dt> <dd>

<span data-ttu-id="224b6-146">Chaque entrée de révocation est le condensé 160 bits d’un certificat révoqué.</span><span class="sxs-lookup"><span data-stu-id="224b6-146">Each revocation entry is the 160-bit digest of a revoked certificate.</span></span> <span data-ttu-id="224b6-147">Comparez ce condensé avec l’élément DigestValue dans le certificat.</span><span class="sxs-lookup"><span data-stu-id="224b6-147">Compare this digest with the DigestValue element within the certificate.</span></span>

</dd> <dt>

<span data-ttu-id="224b6-148"><span id="Certificate"></span><span id="certificate"></span><span id="CERTIFICATE"></span>Certificat</span><span class="sxs-lookup"><span data-stu-id="224b6-148"><span id="Certificate"></span><span id="certificate"></span><span id="CERTIFICATE"></span>Certificate</span></span>
</dt> <dd>

<span data-ttu-id="224b6-149">La section certificat contient une valeur 32 bits indiquant la longueur (en octets) du certificat XML et de sa chaîne de certificats, ainsi qu’un tableau d’octets contenant à la fois le certificat XML de l’autorité de certification et la chaîne de certificats qui contient Microsoft comme racine.</span><span class="sxs-lookup"><span data-stu-id="224b6-149">The certificate section contains a 32-bit value indicating the length (in bytes) of the XML certificate and its certificate chain, along with a byte array that contains both the XML certificate of the Certificate Authority (CA) and the certificate chain that has Microsoft as the Root.</span></span> <span data-ttu-id="224b6-150">Le certificat doit être signé par une autorité de certification habilitée à émettre des listes de révocation de certificats.</span><span class="sxs-lookup"><span data-stu-id="224b6-150">The certificate must be signed by a CA that has the authority to issue CRLs.</span></span>

> [!Note]  
> <span data-ttu-id="224b6-151">Le certificat ne doit pas se terminer par un caractère null.</span><span class="sxs-lookup"><span data-stu-id="224b6-151">The certificate must not be null-terminated.</span></span>

 

</dd> <dt>

<span data-ttu-id="224b6-152"><span id="Signature"></span><span id="signature"></span><span id="SIGNATURE"></span>Signature</span><span class="sxs-lookup"><span data-stu-id="224b6-152"><span id="Signature"></span><span id="signature"></span><span id="SIGNATURE"></span>Signature</span></span>
</dt> <dd>

<span data-ttu-id="224b6-153">La section signature contient le type et la longueur de la signature, ainsi que la signature numérique elle-même.</span><span class="sxs-lookup"><span data-stu-id="224b6-153">The signature section contains the signature type and length, and the digital signature itself.</span></span> <span data-ttu-id="224b6-154">Le type 8 bits a la valeur 2 pour indiquer qu’il utilise SHA-1 avec le chiffrement RSA 1024 bits.</span><span class="sxs-lookup"><span data-stu-id="224b6-154">The 8-bit type is set to 2 to indicate that it uses SHA-1 with 1024-bit RSA encryption.</span></span> <span data-ttu-id="224b6-155">La longueur est une valeur de 16 bits contenant la longueur de la signature numérique, en octets.</span><span class="sxs-lookup"><span data-stu-id="224b6-155">The length is a 16-bit value containing the length of the digital signature in bytes.</span></span> <span data-ttu-id="224b6-156">La signature numérique est calculée sur toutes les sections précédentes de la liste de révocation de certificats.</span><span class="sxs-lookup"><span data-stu-id="224b6-156">The digital signature is calculated over all prior sections of the CRL.</span></span>

<span data-ttu-id="224b6-157">La signature est calculée à l’aide du schéma de signature numérique RSASSA-PSS défini dans PKCS \# 1 (version 2,1).</span><span class="sxs-lookup"><span data-stu-id="224b6-157">The signature is calculated using the RSASSA-PSS digital signature scheme that is defined in PKCS \#1 (version 2.1).</span></span> <span data-ttu-id="224b6-158">La fonction de hachage est SHA-1, qui est définie dans normes FIPS (Federal Information Processing Standard) (FIPS) 180-2, et la fonction de génération de masque est MGF1, qui est définie dans la section B. 2.1 dans PKCS \# 1 (version 2,1).</span><span class="sxs-lookup"><span data-stu-id="224b6-158">The hash function is SHA-1, which is defined in Federal Information Processing Standard (FIPS) 180-2, and the mask generation function is MGF1, which is defined in section B.2.1 in PKCS \#1 (version 2.1).</span></span> <span data-ttu-id="224b6-159">Les opérations RSASP1 et RSAVP1 utilisent RSA avec un module 1024 bits avec un exposant de vérification de 65537.</span><span class="sxs-lookup"><span data-stu-id="224b6-159">The RSASP1 and RSAVP1 operations use RSA with a 1024-bit modulus with a verification exponent of 65537.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="224b6-160">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="224b6-160">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="224b6-161">Utilisation du protocole COPP (Certified Output Protection Protocol)</span><span class="sxs-lookup"><span data-stu-id="224b6-161">Using Certified Output Protection Protocol (COPP)</span></span>](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



