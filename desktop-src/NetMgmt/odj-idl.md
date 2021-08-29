---
title: Définitions IDL de jonction de domaine hors connexion
description: Définitions IDL de jonction de domaine hors connexion
ms.assetid: d495e2f0-5174-4d05-9297-4b4b0f200f08
ms.topic: article
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: f5b58287b778aa46de1bce9e99556c8c144f22d00b3699622cc8244cb092d02d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911619"
---
# <a name="offline-domain-join-idl-definitions"></a>Définitions IDL de jonction de domaine hors connexion

## <a name="description"></a>Description

Les structures de données de jonction de domaine hors connexion (ODJ) ne sont pas définies dans un fichier d’en-tête C\C + +.  Au lieu de cela, les structures sont définies au format IDL (Interface Definition Language), une fois que la compilation est utilisée pour la sérialisation et la désérialisation. sur la plateforme Windows la sérialisation et la désérialisation de ces structures sont gérées automatiquement par les api Win32 suivantes :

<a href="/windows/win32/api/lmjoin/nf-lmjoin-netprovisioncomputeraccount">NetProvisionComputerAccount</a>

<a href="/windows/win32/api/lmjoin/nf-lmjoin-netrequestofflinedomainjoin">NetRequestOfflineDomainJoin</a>

<a href="/windows/win32/api/lmjoin/nf-lmjoin-netcreateprovisioningpackage">NetCreateProvisioningPackage</a>

<a href="/windows/win32/api/lmjoin/nf-lmjoin-netrequestprovisioningpackageinstall">NetRequestProvisioningPackageInstall</a>

dans certaines situations, par exemple l’interopérabilité avec des plateformes non Windows, il peut être nécessaire de procéder à une sérialisation et une désérialisation manuelles. Cette rubrique contient des définitions pour toutes les structures de données ODJ dans une seule unité de compilation IDL et est incluse pour convienence. Une définition de fichier de configuration d’application (ACF) correspondante est également définie. Ce contenu n’est pas fourni dans le cadre d’un kit de développement logiciel (SDK). Par conséquent, le contenu ci-dessous doit être copié dans votre code et compilé avec un compilateur IDL. Le compilateur IDL produira les fonctions stub serialization\deserialization nécessaires, qui sont ensuite liées à votre application. Pour plus d’informations sur le mode de sérialisation et de désérialisation des types, consultez <a href="/windows/win32/rpc/type-serialization">sérialisation de type</a> .

Reportez-vous aux sections de structure individuelles pour obtenir une documentation détaillée sur les membres.

Si vous utilisez le compilateur Microsoft MIDL, vous devez spécifier les indicateurs suivants pour optimiser la compatibilité :

/char unsigned

/ms_ext

/c_ext

## <a name="odj-idl-file"></a>Fichier IDL ODJ

```C++
include "dsgetdc.h";

interface ODJ
{
    typedef struct _ODJ_BLOB
    {
        ULONG ulODJFormat;
        ULONG cbBlob;
        [size_is(cbBlob)] PBYTE pBlob;
    } ODJ_BLOB, *PODJ_BLOB;

    typedef struct _ODJ_PROVISION_DATA
    {
        ULONG ulVersion;
        ULONG ulcBlobs;
        [size_is(ulcBlobs)] PODJ_BLOB pBlobs;
    } ODJ_PROVISION_DATA;

    typedef ODJ_PROVISION_DATA *PODJ_PROVISION_DATA;

    typedef struct _OP_BLOB
    {
        ULONG                       cbBlob;
        [size_is(cbBlob)]   PBYTE   pBlob;

    } OP_BLOB, *POP_BLOB;

    typedef struct _OP_PACKAGE_PART
    {
        GUID    PartType;
        ULONG   ulFlags;
        OP_BLOB Part;
        OP_BLOB Extension;
    } OP_PACKAGE_PART, *POP_PACKAGE_PART;

    typedef struct _OP_PACKAGE_PART_COLLECTION
    {
        ULONG                                 cParts;
        [size_is(cParts)]   POP_PACKAGE_PART  pParts;
        OP_BLOB                               Extension;
    } OP_PACKAGE_PART_COLLECTION, *POP_PACKAGE_PART_COLLECTION;

    typedef struct _OP_PACKAGE
    {
        GUID    EncryptionType;
        OP_BLOB EncryptionContext;
        OP_BLOB WrappedPartCollection;
        ULONG   cbDecryptedPartCollection;
        OP_BLOB Extension;
    } OP_PACKAGE, *POP_PACKAGE;

    typedef struct _SID_IDENTIFIER_AUTHORITY
    {
        UCHAR Value[6];
    } SID_IDENTIFIER_AUTHORITY, *PSID_IDENTIFIER_AUTHORITY;

    typedef struct _ODJ_SID
    {
        UCHAR Revision;
        UCHAR SubAuthorityCount;
        SID_IDENTIFIER_AUTHORITY IdentifierAuthority;
        [size_is(SubAuthorityCount)] ULONG SubAuthority[*];
    }   ODJ_SID, *PODJ_SID;

    typedef struct _ODJ_UNICODE_STRING
    {
        USHORT Length;
        USHORT MaximumLength;
        [size_is(MaximumLength/2), length_is(Length/2)] PWSTR Buffer;
    } ODJ_UNICODE_STRING, *PODJ_UNICODE_STRING;

    typedef struct _ODJ_POLICY_DNS_DOMAIN_INFO
    {
        ODJ_UNICODE_STRING Name;
        ODJ_UNICODE_STRING DnsDomainName;
        ODJ_UNICODE_STRING DnsForestName;
        GUID DomainGuid;
        PODJ_SID Sid;
    }   ODJ_POLICY_DNS_DOMAIN_INFO;

    typedef struct _ODJ_WIN7BLOB
    {
        [string] wchar_t *lpDomain;
        [string] wchar_t *lpMachineName;
        [string] wchar_t *lpMachinePassword;
        ODJ_POLICY_DNS_DOMAIN_INFO  DnsDomainInfo;
        DOMAIN_CONTROLLER_INFOW DcInfo;
        DWORD Options;
    } ODJ_WIN7BLOB;

    typedef ODJ_WIN7BLOB *PODJ_WIN7BLOB;

    cpp_quote("#define OP_JP2_FLAG_PERSISTENTSITE    0x00000001")

    typedef struct _OP_JOINPROV2_PART
    {
        DWORD     dwFlags;
        [string] wchar_t *lpNetbiosName;
        [string] wchar_t *lpSiteName;
        [string] wchar_t *lpPrimaryDNSDomain;

        DWORD             dwReserved;
        [string] wchar_t *lpReserved;
    } OP_JOINPROV2_PART, *POP_JOINPROV2_PART;

    typedef struct _OP_JOINPROV3_PART
    {
        DWORD Rid;
        [string] wchar_t *lpSid;
    } OP_JOINPROV3_PART, *POP_JOINPROV3_PART;

    typedef struct _OP_POLICY_ELEMENT
    {
        [string] wchar_t                *pKeyPath;
        [string] wchar_t                *pValueName;
        ULONG                           ulValueType;
        ULONG                           cbValueData;
        [size_is(cbValueData)]  PBYTE   pValueData;
    } OP_POLICY_ELEMENT, *POP_POLICY_ELEMENT;

    typedef struct _OP_POLICY_ELEMENT_LIST
    {
        [string] wchar_t                            *pSource;
        ULONG                                       ulRootKeyId;
        ULONG                                       cElements;
        [size_is(cElements)]    POP_POLICY_ELEMENT  pElements;
    } OP_POLICY_ELEMENT_LIST, *POP_POLICY_ELEMENT_LIST;

    typedef struct _OP_POLICY_PART
    {
        ULONG                                       cElementLists;
        [size_is(cElementLists)]
                            POP_POLICY_ELEMENT_LIST pElementLists;
        OP_BLOB                                     Extension;
    } OP_POLICY_PART, *POP_POLICY_PART;

    typedef struct _OP_CERT_PFX_STORE
    {
        [string] wchar_t            *pTemplateName;
        ULONG                       ulPrivateKeyExportPolicy;
        [string] wchar_t            *pPolicyServerUrl;
        ULONG                       ulPolicyServerUrlFlags;
        [string] wchar_t            *pPolicyServerId;
        ULONG                       cbPfx;
        [size_is(cbPfx)]    PBYTE   pPfx;
    } OP_CERT_PFX_STORE, *POP_CERT_PFX_STORE;

    typedef struct _OP_CERT_SST_STORE
    {
        ULONG                       StoreLocation;
        [string] wchar_t            *pStoreName;
        ULONG                       cbSst;
        [size_is(cbSst)]    PBYTE   pSst;
    } OP_CERT_SST_STORE, *POP_CERT_SST_STORE;

    typedef struct _OP_CERT_PART
    {
        ULONG                                       cPfxStores;
        [size_is(cPfxStores)]   POP_CERT_PFX_STORE  pPfxStores;
        ULONG                                       cSstStores;
        [size_is(cSstStores)]   POP_CERT_SST_STORE  pSstStores;
        OP_BLOB                                     Extension;
    } OP_CERT_PART, *POP_CERT_PART;
}
```

## <a name="odj-acf-file"></a>Fichier ODJ ACF

```C++
[
    // If necessary for your application, see MIDL documentation for alternatives to explicit_handle
    explicit_handle
]
interface ODJ
{
    typedef [encode, decode] PODJ_WIN7BLOB;
    typedef [encode, decode] POP_JOINPROV2_PART;
    typedef [encode, decode] POP_JOINPROV3_PART;
    typedef [encode, decode] PODJ_PROVISION_DATA;
    typedef [encode, decode] POP_PACKAGE_PART;
    typedef [encode, decode] POP_PACKAGE_PART_COLLECTION;
    typedef [encode, decode] POP_PACKAGE;
    typedef [encode, decode] POP_POLICY_PART;
    typedef [encode, decode] POP_CERT_PART;
}
```

## <a name="see-also"></a>Voir aussi

<a href="/windows/win32/midl/midl-start-page">Microsoft Interface Definition Language</a>

<a href="/windows/win32/midl/midl-command-line-reference">Référence de Command-Line MIDL</a>

<a href="/windows/win32/rpc/serialization-services">Services de sérialisation</a>

<a href="/windows/win32/rpc/type-serialization">Sérialisation de type</a>

<a href="/windows/win32/api/lmjoin/nf-lmjoin-netprovisioncomputeraccount">NetProvisionComputerAccount</a>

<a href="/windows/win32/api/lmjoin/nf-lmjoin-netrequestofflinedomainjoin">NetRequestOfflineDomainJoin</a>

<a href="/windows/win32/api/lmjoin/nf-lmjoin-netcreateprovisioningpackage">NetCreateProvisioningPackage</a>

<a href="/windows/win32/api/lmjoin/nf-lmjoin-netrequestprovisioningpackageinstall">NetRequestProvisioningPackageInstall</a>
