---
description: Explique comment générer, échanger, importer et exporter des clés de Diffie-Hellman.
ms.assetid: 623a8c9e-3f6a-470b-be30-dec13342bb90
title: Clés de Diffie-Hellman
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f00eaddd580ac74e18e26498175f87b5d81b8e20
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127123229"
---
# <a name="diffie-hellman-keys"></a>Clés de Diffie-Hellman

-   [Génération de clés de Diffie-Hellman](#generating-diffie-hellman-keys)
-   [Échange de clés de Diffie-Hellman](#exchanging-diffie-hellman-keys)
-   [Exportation d’une clé privée Diffie-Hellman](#exporting-a-diffie-hellman-private-key)
-   [Exemple de code](#example-code)

## <a name="generating-diffie-hellman-keys"></a>Génération de clés de Diffie-Hellman

Pour générer une clé de Diffie-Hellman, procédez comme suit :

1.  Appelez la fonction [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) pour obtenir un descripteur du fournisseur de services de chiffrement Microsoft Diffie-Hellman.
2.  Générez la nouvelle clé. Il existe deux façons de procéder : en demandant à CryptoAPI de générer toutes les nouvelles valeurs pour G, P et X ou en utilisant des valeurs existantes pour G et P, et en générant une nouvelle valeur pour X.

    **Pour générer la clé en générant toutes les nouvelles valeurs**

    1.  Appelez la fonction [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) , en transmettant **CALG \_ DH \_ DF** (Store et Forward) ou **CALG \_ DH \_ EPHEM** (éphémère) dans le paramètre *algid* . La clé sera générée à l’aide de nouvelles valeurs aléatoires pour G et P, une nouvelle valeur calculée pour X et sa poignée sera retournée dans le paramètre *phKey* .
    2.  La nouvelle clé est maintenant prête à être utilisée. Les valeurs de G et P doivent être envoyées au destinataire avec la clé (ou envoyées par une autre méthode) lors d’un échange de [*clés*](../secgloss/e-gly.md).

    **Pour générer la clé à l’aide de valeurs prédéfinies pour G et P**

    1.  Appelez [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) en transmettant **CALG \_ DH \_ DF** (Store et Forward) **ou \_ CALG \_ DH EPHEM** (éphémère) dans le paramètre *algid* et **crypt \_ PREGEN** pour le paramètre *dwFlags* . Un handle de clé sera généré et retourné dans le paramètre *phKey* .
    2.  Initialisez une structure d' [**\_ \_ objet blob de données**](/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)) de chiffre avec le membre **PbData** défini sur la valeur P. L' [*objet BLOB*](../secgloss/b-gly.md) ne contient pas d’informations d’en-tête et le membre **pbData** est au format [*Little endian*](../secgloss/l-gly.md) .
    3.  La valeur de P est définie en appelant la fonction [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) , en passant le handle de clé récupéré à l’étape a dans le paramètre *HKEY* , l’indicateur **KP \_ P** dans le paramètre *dwParam* et un pointeur vers la structure qui contient la valeur de p dans le paramètre *pbData* .
    4.  Initialisez une structure d' [**\_ \_ objet blob de données**](/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)) de chiffre avec le membre **PbData** défini sur la valeur G. L’objet BLOB ne contient pas d’informations d’en-tête et le membre **pbData** est au format Little endian.
    5.  La valeur de G est définie en appelant la fonction [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) , en passant le handle de clé récupéré à l’étape a dans le paramètre *HKEY* , l’indicateur **KP \_ g** dans le paramètre *dwParam* et un pointeur vers la structure qui contient la valeur de G dans le paramètre *pbData* .
    6.  La valeur de X est générée en appelant la fonction [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) , en passant le handle de clé récupéré à l’étape a dans le paramètre *HKEY* , l’indicateur **KP \_ X** dans le paramètre *DwParam* et la valeur **null** dans le paramètre *pbData* .
    7.  Si tous les appels de fonction ont réussi, la clé publique Diffie-Hellman est prête à être utilisée.

3.  Lorsque la clé n’est plus nécessaire, détruisez-la en passant le handle de clé à la fonction [**CryptDestroyKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey) .

Si **CALG \_ DH \_ DF** a été spécifié dans les procédures précédentes, les valeurs de clé sont conservées dans le stockage à chaque appel à [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam). Les valeurs G et P peuvent ensuite être récupérées à l’aide de la fonction [**CryptGetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetkeyparam) . Certains fournisseurs de services de chiffrement peuvent avoir des valeurs G et P codées en dur. Dans ce cas, une erreur **\_ FIXEDPARAMETER NPD** est retournée si **CryptSetKeyParam** est appelé avec **KP \_ G** ou **KP \_ P** spécifié dans le paramètre *dwParam* . Si **CryptDestroyKey** est appelé, le handle de la clé est détruit, mais les valeurs de clé sont conservées dans le CSP. Toutefois, si **CALG \_ DH \_ EPHEM** a été spécifié, le descripteur de la clé est détruit et toutes les valeurs sont effacées du CSP.

## <a name="exchanging-diffie-hellman-keys"></a>Échange de clés de Diffie-Hellman

L’objectif de l’algorithme Diffie-Hellman est de permettre à deux ou plusieurs parties de créer et de partager une clé de session secrète identique en partageant des informations sur un réseau qui n’est pas sécurisé. Les informations qui sont partagées sur le réseau se présente sous la forme de deux valeurs constantes et d’une Diffie-Hellman clé publique. Le processus utilisé par deux parties clés-Exchange est le suivant :

-   Les deux parties acceptent les paramètres de Diffie-Hellman qui sont un nombre premier (P) et un numéro de générateur (G).
-   Le tiers 1 envoie son Diffie-Hellman clé publique au tiers 2.
-   Le tiers 2 calcule la clé de session secrète à l’aide des informations contenues dans sa clé privée et la clé publique du tiers 1.
-   Le tiers 2 envoie son Diffie-Hellman clé publique au tiers 1.
-   Le tiers 1 calcule la clé de session secrète à l’aide des informations contenues dans sa clé privée et la clé publique du tiers 2.
-   Les deux parties ont désormais la même clé de session, qui peut être utilisée pour chiffrer et déchiffrer les données. Les étapes nécessaires sont indiquées dans la procédure suivante.

**Pour préparer une clé publique Diffie-Hellman pour la transmission**

1.  Appelez la fonction [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) pour obtenir un descripteur du fournisseur de services de chiffrement Microsoft Diffie-Hellman.
2.  Créez une clé de Diffie-Hellman en appelant la fonction [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) pour créer une nouvelle clé ou en appelant la fonction [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) pour récupérer une clé existante.
3.  Obtenir la taille nécessaire pour contenir le Diffie-Hellman BLOB de clé en appelant [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey), en transmettant la **valeur null** pour le paramètre *pbData* . La taille requise est retournée dans *pdwDataLen*.
4.  Allouez de la mémoire pour l’objet BLOB de clé.
5.  Créez un [*objet blob de clé publique*](../secgloss/p-gly.md) Diffie-Hellman en appelant la fonction [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) , en passant **publicKeyBlob** dans le paramètre *dwBlobType* et le handle à la clé Diffie-Hellman dans le paramètre *HKEY* . Cet appel de fonction provoque le calcul de la valeur de la clé publique (G ^ X) mod P.
6.  Si tous les appels de fonction précédents ont réussi, le Diffie-Hellman objet BLOB de clé publique est maintenant prêt à être encodé et transmis.

**Pour importer une clé publique Diffie-Hellman et calculer la clé de session secrète**

1.  Appelez la fonction [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) pour obtenir un descripteur du fournisseur de services de chiffrement Microsoft Diffie-Hellman.
2.  Créez une clé de Diffie-Hellman en appelant la fonction [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) pour créer une nouvelle clé ou en appelant la fonction [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) pour récupérer une clé existante.
3.  Pour importer la Diffie-Hellman clé publique dans le CSP, appelez la fonction [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) , en passant un pointeur vers l’objet blob de clé publique dans le paramètre *pbData* , la longueur de l’objet BLOB dans le paramètre *dwDataLen* et le descripteur de la clé Diffie-Hellman dans le paramètre *hPubKey* . Le calcul, (Y ^ X) mod P, est alors effectué, créant ainsi la clé secrète partagée et effectuant l’échange de [*clés*](../secgloss/e-gly.md). Cet appel de fonction retourne un handle vers la nouvelle clé secrète de session dans le paramètre *HKEY* .
4.  À ce stade, le Diffie-Hellman importé est de type **CALG \_ AGREEDKEY \_ any**. Avant de pouvoir utiliser la clé, celle-ci doit être convertie en un type de clé de session. Pour ce faire, vous devez appeler la fonction [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) avec *DwParam* défini sur **KP \_ ALGID** et avec *pbData* défini sur un pointeur vers une valeur d' [**\_ ID ALG**](alg-id.md) qui représente une clé de session, par exemple **CALG \_ RC4**. La clé doit être convertie avant d’utiliser la clé partagée dans la fonction [**CryptEncrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencrypt) ou [**CryptDecrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecrypt) . Les appels passés à l’une de ces fonctions avant la conversion du type de clé échouent.
5.  La clé de session secrète est maintenant prête à être utilisée pour le chiffrement ou le déchiffrement.
6.  Lorsque la clé n’est plus nécessaire, détruisez le handle de clé en appelant la fonction [**CryptDestroyKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey) .

## <a name="exporting-a-diffie-hellman-private-key"></a>Exportation d’une clé privée Diffie-Hellman

Pour exporter une clé privée Diffie-Hellman, procédez comme suit :

1.  Appelez la fonction [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) pour obtenir un descripteur du fournisseur de services de chiffrement Microsoft Diffie-Hellman.
2.  Créez une clé de Diffie-Hellman en appelant la fonction [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) pour créer une nouvelle clé ou en appelant la fonction [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) pour récupérer une clé existante.
3.  Créez un [*objet blob de clé privée*](../secgloss/p-gly.md) Diffie-Hellman en appelant la fonction [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) , en passant **PRIVATEKEYBLOB** dans le paramètre *dwBlobType* et le handle à la clé Diffie-Hellman dans le paramètre *HKEY* .
4.  Lorsque le descripteur de clé n’est plus nécessaire, appelez la fonction [**CryptDestroyKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey) pour détruire le handle de clé.

## <a name="example-code"></a>Exemple de code

L’exemple suivant montre comment créer, exporter, importer et utiliser une clé de Diffie-Hellman pour effectuer un échange de clés.


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



 

 
