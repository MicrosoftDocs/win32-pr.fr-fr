---
title: Comment signer par programmation un package d’application (C++)
description: Découvrez comment signer un package d’application à l’aide de la fonction SignerSignEx2.
ms.assetid: 1183D665-83C9-4BE7-9C8D-834484B8C57F
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a91cf2c7b7be674ff14d1ceada59be593a300d7ebf1964ddce4a7a5340ab74c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130241"
---
# <a name="how-to-programmatically-sign-an-app-package-c"></a>Comment signer par programmation un package d’application (C++)

Découvrez comment signer un package d’application à l’aide de la fonction [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2) .

si vous souhaitez créer par programmation Windows des packages d’application à l’aide de l’API de création de [package](interfaces.md), vous devez également signer les packages d’application avant de pouvoir les déployer. L’API de Packaging ne fournit pas de méthode spécialisée pour la signature des packages d’application. Utilisez plutôt les fonctions de [chiffrement](/windows/desktop/SecCrypto/cryptography-functions) standard pour signer vos packages d’application.

## <a name="what-you-need-to-know"></a>Bon à savoir

### <a name="technologies"></a>Technologies

-   [Présentation de la signature de code](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))
-   [empaquetage, déploiement et interrogation d’applications Windows](appx-portal.md)
-   [fonctions de chiffrement](/windows/desktop/SecCrypto/cryptography-functions)

### <a name="prerequisites"></a>Prérequis

-   vous devez disposer d’une application Windows empaquetée. Pour plus d’informations sur la création d’un package d’application, consultez [comment créer un package d’application](how-to-create-a-package.md).
-   Vous devez disposer d’un certificat de signature de code approprié pour signer le package d’application. Pour plus d’informations sur la création d’un certificat de signature de code de test, consultez [comment créer un certificat de signature de package d’application](how-to-create-a-package-signing-certificate.md). Chargez ce certificat de signature dans une structure de [**\_ contexte de certificat**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) . Par exemple, vous pouvez utiliser [**PFXImportCertStore**](/windows/desktop/api/wincrypt/nf-wincrypt-pfximportcertstore) et [**CertFindCertificateInStore**](/windows/desktop/api/wincrypt/nf-wincrypt-certfindcertificateinstore) pour charger un certificat de signature.
-   Windows 8 introduit la fonction [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2) . utilisez **SignerSignEx2** lorsque vous vous connectez Windows des packages d’application.

## <a name="instructions"></a>Instructions

### <a name="step-1-define-the-required-structures-for-signersignex2"></a>Étape 1 : définir les structures requises pour SignerSignEx2

Outre l’en-tête Wincrypt. h, la fonction [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2) dépend de nombreuses structures qui ne sont pas définies dans un fichier d’en-tête du kit de développement logiciel (SDK). Pour utiliser **SignerSignEx2**, vous devez définir ces structures vous-même :


```C++
typedef struct _SIGNER_FILE_INFO
{
    DWORD cbSize;
    LPCWSTR pwszFileName;
    HANDLE hFile;
}SIGNER_FILE_INFO, *PSIGNER_FILE_INFO;
 
typedef struct _SIGNER_BLOB_INFO
{
    DWORD cbSize;
    GUID *pGuidSubject;
    DWORD cbBlob;
    BYTE *pbBlob;
    LPCWSTR pwszDisplayName;
}SIGNER_BLOB_INFO, *PSIGNER_BLOB_INFO;
 
typedef struct _SIGNER_SUBJECT_INFO
{
    DWORD cbSize;
    DWORD *pdwIndex;
    DWORD dwSubjectChoice;
    union
    {
        SIGNER_FILE_INFO *pSignerFileInfo;
        SIGNER_BLOB_INFO *pSignerBlobInfo;
    };
}SIGNER_SUBJECT_INFO, *PSIGNER_SUBJECT_INFO;
 
// dwSubjectChoice should be one of the following:
#define SIGNER_SUBJECT_FILE    0x01
#define SIGNER_SUBJECT_BLOB    0x02
 
typedef struct _SIGNER_ATTR_AUTHCODE
{
    DWORD cbSize;
    BOOL fCommercial;
    BOOL fIndividual;
    LPCWSTR pwszName;
    LPCWSTR pwszInfo;
}SIGNER_ATTR_AUTHCODE, *PSIGNER_ATTR_AUTHCODE;
 
typedef struct _SIGNER_SIGNATURE_INFO
{
    DWORD cbSize;
    ALG_ID algidHash;
    DWORD dwAttrChoice;
    union
    {
        SIGNER_ATTR_AUTHCODE *pAttrAuthcode;
    };
    PCRYPT_ATTRIBUTES psAuthenticated;
    PCRYPT_ATTRIBUTES psUnauthenticated;
}SIGNER_SIGNATURE_INFO, *PSIGNER_SIGNATURE_INFO;
 
// dwAttrChoice should be one of the following:
#define SIGNER_NO_ATTR          0x00
#define SIGNER_AUTHCODE_ATTR    0x01
 
typedef struct _SIGNER_PROVIDER_INFO
{
    DWORD cbSize;
    LPCWSTR pwszProviderName;
    DWORD dwProviderType;
    DWORD dwKeySpec;
    DWORD dwPvkChoice;
    union
    {
        LPWSTR pwszPvkFileName;
        LPWSTR pwszKeyContainer;
    };
}SIGNER_PROVIDER_INFO, *PSIGNER_PROVIDER_INFO;
 
//dwPvkChoice should be one of the following:
#define PVK_TYPE_FILE_NAME       0x01
#define PVK_TYPE_KEYCONTAINER    0x02
 
typedef struct _SIGNER_SPC_CHAIN_INFO
{
    DWORD cbSize;
    LPCWSTR pwszSpcFile;
    DWORD dwCertPolicy; 
    HCERTSTORE hCertStore;
}SIGNER_SPC_CHAIN_INFO, *PSIGNER_SPC_CHAIN_INFO;
 
typedef struct _SIGNER_CERT_STORE_INFO
{
    DWORD cbSize;
    PCCERT_CONTEXT pSigningCert;
    DWORD dwCertPolicy;
    HCERTSTORE hCertStore;
}SIGNER_CERT_STORE_INFO, *PSIGNER_CERT_STORE_INFO;
 
//dwCertPolicy can be a combination of the following flags:
#define SIGNER_CERT_POLICY_STORE            0x01
#define SIGNER_CERT_POLICY_CHAIN            0x02
#define SIGNER_CERT_POLICY_SPC              0x04
#define SIGNER_CERT_POLICY_CHAIN_NO_ROOT    0x08
 
typedef struct _SIGNER_CERT
{
    DWORD cbSize;
    DWORD dwCertChoice;
    union
    {
        LPCWSTR pwszSpcFile;
        SIGNER_CERT_STORE_INFO *pCertStoreInfo;
        SIGNER_SPC_CHAIN_INFO *pSpcChainInfo;
    };
    HWND hwnd;
}SIGNER_CERT, *PSIGNER_CERT;
 
//dwCertChoice should be one of the following
#define SIGNER_CERT_SPC_FILE     0x01
#define SIGNER_CERT_STORE        0x02
#define SIGNER_CERT_SPC_CHAIN    0x03
 
typedef struct _SIGNER_CONTEXT
{
    DWORD cbSize;
    DWORD cbBlob;
    BYTE *pbBlob;
}SIGNER_CONTEXT, *PSIGNER_CONTEXT;
 
typedef struct _SIGNER_SIGN_EX2_PARAMS
{
    DWORD dwFlags;
    PSIGNER_SUBJECT_INFO pSubjectInfo;
    PSIGNER_CERT pSigningCert;
    PSIGNER_SIGNATURE_INFO pSignatureInfo;
    PSIGNER_PROVIDER_INFO pProviderInfo;
    DWORD dwTimestampFlags;
    PCSTR pszAlgorithmOid;
    PCWSTR pwszTimestampURL;
    PCRYPT_ATTRIBUTES pCryptAttrs;
    PVOID pSipData;
    PSIGNER_CONTEXT *pSignerContext;
    PVOID pCryptoPolicy;
    PVOID pReserved;
} SIGNER_SIGN_EX2_PARAMS, *PSIGNER_SIGN_EX2_PARAMS;
 
typedef struct _APPX_SIP_CLIENT_DATA
{
    PSIGNER_SIGN_EX2_PARAMS pSignerParams;
    IUnknown* pAppxSipState;
} APPX_SIP_CLIENT_DATA, *PAPPX_SIP_CLIENT_DATA;
```



### <a name="step-2-call-signersignex2-to-sign-the-app-package"></a>Étape 2 : appeler SignerSignEx2 pour signer le package d’application

Une fois que vous avez défini les structures requises spécifiées à l’étape précédente, vous pouvez utiliser l’une des options disponibles dans la fonction [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2) pour signer un package d’application. lorsque vous utilisez **SignerSignEx2** avec des packages d’application Windows, ces restrictions s’appliquent :

-   Vous devez fournir un pointeur vers une structure de **\_ \_ \_ données de client SIP AppX** en tant que paramètre *pSipData* lorsque vous signez un package d’application. Vous devez remplir le membre **pSignerParams** des **\_ \_ \_ données du client SIP AppX** avec les mêmes paramètres que ceux que vous utilisez pour signer le package d’application. Pour ce faire, définissez les paramètres souhaités sur la structure de signature **\_ \_ EX2 \_ params** , assignez l’adresse de cette structure à **pSignerParams**, puis référencez directement les membres de la structure également lorsque vous appelez [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2).
-   Après avoir appelé [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2), vous devez libérer le **pAppxSipState** sur *pSipData* en appelant [**IUnknown :: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sur **pAppxSipState** si ce n’est pas **null**.
-   Le membre **algidHash** de la structure d' **\_ \_ informations sur la signature du signataire** doit être le même algorithme de hachage que celui utilisé pour créer le package d’application. Pour plus d’informations sur la façon de déterminer l’algorithme de hachage à partir du package d’application, consultez [Comment signer un package d’application à l’aide de SignTool](how-to-sign-a-package-using-signtool.md). l’algorithme Windows 8 par défaut utilisé par [MakeAppx](make-appx-package--makeappx-exe-.md) et Visual Studio pour créer des packages d’application est « algidHash = CALG \_ SHA \_ 256 ».
-   Si vous voulez également horodater la signature sur le package d’application, vous devez le faire pendant l’appel à [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2) en fournissant les paramètres d’horodatage facultatifs de **SignerSignEx2**(*dwTimestampFlags*, *pszTimestampAlgorithmOid*, *pwszHttpTimeStamp*, *psRequest*). L’appel de [**SignerTimeStampEx3**](/windows/desktop/SecCrypto/signertimestampex3) ou de ses variantes sur un package d’application déjà signé n’est pas pris en charge.

Voici un exemple de code qui montre comment appeler [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2):


```C++
HRESULT SignAppxPackage(
    _In_ PCCERT_CONTEXT signingCertContext,
    _In_ LPCWSTR packageFilePath)
{
    HRESULT hr = S_OK;
 
    // Initialize the parameters for SignerSignEx2
    DWORD signerIndex = 0;
 
    SIGNER_FILE_INFO fileInfo = {};
    fileInfo.cbSize = sizeof(SIGNER_FILE_INFO);
    fileInfo.pwszFileName = packageFilePath;
 
    SIGNER_SUBJECT_INFO subjectInfo = {};
    subjectInfo.cbSize = sizeof(SIGNER_SUBJECT_INFO);
    subjectInfo.pdwIndex = &signerIndex;
    subjectInfo.dwSubjectChoice = SIGNER_SUBJECT_FILE;
    subjectInfo.pSignerFileInfo = &fileInfo;
 
    SIGNER_CERT_STORE_INFO certStoreInfo = {};
    certStoreInfo.cbSize = sizeof(SIGNER_CERT_STORE_INFO);
    certStoreInfo.dwCertPolicy = SIGNER_CERT_POLICY_CHAIN_NO_ROOT;
    certStoreInfo.pSigningCert = signingCertContext;
 
    SIGNER_CERT cert = {};
    cert.cbSize = sizeof(SIGNER_CERT);
    cert.dwCertChoice = SIGNER_CERT_STORE;
    cert.pCertStoreInfo = &certStoreInfo;
 
    // The algidHash of the signature to be created must match the
    // hash algorithm used to create the app package
    SIGNER_SIGNATURE_INFO signatureInfo = {};
    signatureInfo.cbSize = sizeof(SIGNER_SIGNATURE_INFO);
    signatureInfo.algidHash = CALG_SHA_256; 
    signatureInfo.dwAttrChoice = SIGNER_NO_ATTR;
 
    SIGNER_SIGN_EX2_PARAMS signerParams = {};
    signerParams.pSubjectInfo = &subjectInfo;
    signerParams.pSigningCert = &cert;
    signerParams.pSignatureInfo = &signatureInfo;
 
    APPX_SIP_CLIENT_DATA sipClientData = {};
    sipClientData.pSignerParams = &signerParams;
    signerParams.pSipData = &sipClientData;
 
    // Type definition for invoking SignerSignEx2 via GetProcAddress
    typedef HRESULT (WINAPI *SignerSignEx2Function)(
        DWORD,
        PSIGNER_SUBJECT_INFO,
        PSIGNER_CERT,
        PSIGNER_SIGNATURE_INFO,
        PSIGNER_PROVIDER_INFO,
        DWORD,
        PCSTR,
        PCWSTR,
        PCRYPT_ATTRIBUTES,
        PVOID,
        PSIGNER_CONTEXT *,
        PVOID,
        PVOID); 
 
    // Load the SignerSignEx2 function from MSSign32.dll
    HMODULE msSignModule = LoadLibraryEx(
        L"MSSign32.dll", 
        NULL, 
        LOAD_LIBRARY_SEARCH_SYSTEM32);

    if (msSignModule)
    {
        SignerSignEx2Function SignerSignEx2 = reinterpret_cast<SignerSignEx2Function>(
            GetProcAddress(msSignModule, "SignerSignEx2"));
        if (SignerSignEx2)
        {
            hr = SignerSignEx2(
                signerParams.dwFlags,
                signerParams.pSubjectInfo,
                signerParams.pSigningCert,
                signerParams.pSignatureInfo,
                signerParams.pProviderInfo,
                signerParams.dwTimestampFlags,
                signerParams.pszAlgorithmOid,
                signerParams.pwszTimestampURL,
                signerParams.pCryptAttrs,
                signerParams.pSipData,
                signerParams.pSignerContext,
                signerParams.pCryptoPolicy,
                signerParams.pReserved);
        }
        else
        {
            DWORD lastError = GetLastError();
            hr = HRESULT_FROM_WIN32(lastError);
        }
 
        FreeLibrary(msSignModule);
    }
    else
    {
        DWORD lastError = GetLastError();
        hr = HRESULT_FROM_WIN32(lastError);
    }
 
    // Free any state used during app package signing
    if (sipClientData.pAppxSipState)
    {
        sipClientData.pAppxSipState->Release();
    }
 
    return hr;
}
```



## <a name="remarks"></a>Remarques

Une fois que vous avez signé le package d’application, vous pouvez également essayer de valider la signature par programmation à l’aide de la fonction [**WinVerifyTrust**](/windows/desktop/api/wintrust/nf-wintrust-winverifytrust) avec l' **\_ action WINTRUST \_ générique \_ verify \_ v2**. il n’existe pas de considérations particulières dans ce cas pour utiliser **WinVerifyTrust** avec des packages d’application Windows.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Présentation de la signature de code](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))
</dt> <dt>

[API d’empaquetage](interfaces.md)
</dt> <dt>

[fonctions de chiffrement](/windows/desktop/SecCrypto/cryptography-functions)
</dt> </dl>

 

 