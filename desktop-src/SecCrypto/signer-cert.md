---
description: Spécifie un certificat utilisé pour signer un document. Le certificat peut être stocké dans un fichier SPC (Software Publisher Certificate) ou dans un magasin de certificats.
ms.assetid: 9a99ce98-237d-4223-ab3d-0576041038e3
title: Structure SIGNER_CERT
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_CERT
api_type:
- NA
api_location: ''
ms.openlocfilehash: a14f955749e98ca34cda0be2c57a3d5c546afc41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104209867"
---
# <a name="signer_cert-structure"></a>Structure du \_ certificat du signataire

La structure du certificat du **signataire \_** spécifie un [*certificat*](../secgloss/c-gly.md) utilisé pour signer un document. Le certificat peut être stocké dans un fichier SPC ( [*Software Publisher Certificate*](../secgloss/s-gly.md) ) ou dans un [*magasin de certificats*](../secgloss/c-gly.md).

> [!Note]  
> Cette structure n’est définie dans aucun fichier d’en-tête. Pour utiliser cette structure, vous devez la définir vous-même comme indiqué dans cette rubrique.

 

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _SIGNER_CERT {
  DWORD cbSize;
  DWORD dwCertChoice;
  union {
    LPCWSTR                pwszSpcFile;
    SIGNER_CERT_STORE_INFO *pCertStoreInfo;
    SIGNER_SPC_CHAIN_INFO  *pSpcChainInfo;
  };
  HWND  hwnd;
} SIGNER_CERT, *PSIGNER_CERT;
```



## <a name="members"></a>Membres

<dl> <dt>

**cbSize**
</dt> <dd>

Taille, en octets, de la structure.

</dd> <dt>

**dwCertChoice**
</dt> <dd>

Spécifie comment le certificat est stocké. Ce membre peut être une ou plusieurs des valeurs suivantes.



| Valeur                                                                                                                                                                                                                                          | Signification                                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SIGNER_CERT_SPC_FILE"></span><span id="signer_cert_spc_file"></span><dl> <dt>**Signataire \_ \_ \_ Fichier CPS du certificat**</dt> <dt>1</dt> </dl>    | Le certificat est stocké dans un fichier SPC. Le membre **pwszSpcFile** contient le chemin d’accès et le nom de fichier du fichier SPC.<br/>                                                                                                                                                  |
| <span id="SIGNER_CERT_STORE"></span><span id="signer_cert_store"></span><dl> <dt>**Signataire \_ \_Magasin de certificats**</dt> <dt>2</dt> </dl>              | Le certificat est stocké dans un magasin de certificats. Le membre **pCertStoreInfo** contient un pointeur vers une structure d' [**\_ \_ \_ informations du magasin**](signer-cert-store-info.md) du certificat du signataire qui spécifie le magasin de certificats dans lequel le certificat est stocké.<br/>                 |
| <span id="SIGNER_CERT_SPC_CHAIN"></span><span id="signer_cert_spc_chain"></span><dl> <dt>**Signataire \_ CERTIFICAT \_ SPC \_ chaîne**</dt> <dt>3</dt> </dl> | Le certificat est stocké dans un fichier SPC et est associé à une chaîne de certificats. Le membre **pSpcChainInfo** contient un pointeur vers une structure d' [**\_ \_ \_ informations de chaîne SPC du signataire**](signer-spc-chain-info.md) qui contient les informations de chaîne du certificat.<br/> |



 

</dd> <dt>

**pwszSpcFile**
</dt> <dd>

Pointeur vers une chaîne Unicode terminée par le caractère null qui contient le chemin d’accès et le nom de fichier du fichier SPC dans lequel le certificat est stocké. Ce membre est utilisé uniquement si le membre **dwCertChoice** contient le **\_ \_ \_ fichier SPC du certificat du signataire**.

</dd> <dt>

**pCertStoreInfo**
</dt> <dd>

Pointeur vers une structure d' [**\_ \_ \_ informations du magasin**](signer-cert-store-info.md) du certificat du signataire qui spécifie le magasin de certificats dans lequel le certificat est stocké. Ce membre est utilisé uniquement si le membre **dwCertChoice** contient le **\_ \_ magasin de certificats de signataire**.

</dd> <dt>

**pSpcChainInfo**
</dt> <dd>

Pointeur vers une structure d' [**\_ \_ \_ informations de chaîne SPC du signataire**](signer-spc-chain-info.md) qui contient les informations de chaîne du certificat. Ce membre est utilisé uniquement si le membre **dwCertChoice** contient le **certificat du signataire du \_ certificat \_ SPC \_**.

</dd> <dt>

**HWND**
</dt> <dd>

Handle de la fenêtre à utiliser comme propriétaire de toutes les boîtes de dialogue affichées. Ce membre n’est pas actuellement utilisé et est ignoré.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SignerSign**](signersign.md)
</dt> <dt>

[**SignerSignEx**](signersignex.md)
</dt> </dl>

 

 
