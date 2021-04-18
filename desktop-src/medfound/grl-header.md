---
description: Contient l’en-tête GRL (liste de révocation globale).
ms.assetid: 806ae550-5106-47ec-8466-f967598d3e61
title: Structure GRL_HEADER
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GRL_HEADER
api_type:
- NA
api_location: ''
ms.openlocfilehash: c20c9323ac627f9f1d6c63ae893d1633fb3cd96f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515949"
---
# <a name="grl_header-structure"></a>\_Structure d’en-tête GRL

Contient l’en-tête GRL (liste de révocation globale).

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _GRL_HEADER {
  WCHAR    wszIdentifier[6];
  WORD     wFormatMajor;
  WORD     wFormatMinor;
  FILETIME CreationTime;
  DWORD    dwSequenceNumber;
  DWORD    dwForceRebootVersion;
  DWORD    dwForceProcessRestartVersion;
  DWORD    cbRevocationSectionOffset;
  DWORD    cRevokedKernelBinaries;
  DWORD    cRevokedUserBinaries;
  DWORD    cRevokedCertificates;
  DWORD    cTrustedRoots;
  DWORD    cbExtensibleSectionOffset;
  DWORD    cExtensibleEntries;
  DWORD    cbRenewalSectionOffset;
  DWORD    cRevokedKernelBinaryRenewals;
  DWORD    cRevokedUserBinaryRenewals;
  DWORD    cRevokedCertificateRenewals;
  DWORD    cbSignatureCoreOffset;
  DWORD    cbSignatureExtOffset;
} GRL_HEADER;
```



## <a name="members"></a>Membres

<dl> <dt>

**wszIdentifier**
</dt> <dd>

Identificateur GRL. La valeur est toujours L "MSGRL".

</dd> <dt>

**wFormatMajor**
</dt> <dd>

Numéro de version principale. Actuellement, la valeur doit être 1.

</dd> <dt>

**wFormatMinor**
</dt> <dd>

Numéro de version secondaire. Actuellement, la valeur doit être égale à zéro.

</dd> <dt>

**CreationTime**
</dt> <dd>

Valeur **fileTime** qui spécifie le moment où le fichier a été créé.

</dd> <dt>

**dwSequenceNumber**
</dt> <dd>

Numéro de version de GRL. Actuellement, la valeur doit être au moins égale à 3

</dd> <dt>

**dwForceRebootVersion**
</dt> <dd>

Réservé.

</dd> <dt>

**dwForceProcessRestartVersion**
</dt> <dd>

Réservé.

</dd> <dt>

**cbRevocationSectionOffset**
</dt> <dd>

Offset, en octets, entre le début de GRL et la section principale.

</dd> <dt>

**cRevokedKernelBinaries**
</dt> <dd>

Nombre de binaires de noyau révoqués listés dans GRL.

</dd> <dt>

**cRevokedUserBinaries**
</dt> <dd>

Nombre de fichiers binaires en mode utilisateur révoqués listés dans GRL.

</dd> <dt>

**cRevokedCertificates**
</dt> <dd>

Nombre de certificats révoqués listés dans GRL.

</dd> <dt>

**cTrustedRoots**
</dt> <dd>

Nombre de racines de confiance listées dans GRL.

</dd> <dt>

**cbExtensibleSectionOffset**
</dt> <dd>

Offset, en octets, entre le début de GRL et la section extensible.

</dd> <dt>

**cExtensibleEntries**
</dt> <dd>

Nombre d’entrées dans la section extensible.

</dd> <dt>

**cbRenewalSectionOffset**
</dt> <dd>

Décalage, en octets, entre le début de GRL et la section renouvellements.

</dd> <dt>

**cRevokedKernelBinaryRenewals**
</dt> <dd>

Nombre de renouvellements binaires de noyau listés dans le GRL.

</dd> <dt>

**cRevokedUserBinaryRenewals**
</dt> <dd>

Nombre de renouvellements binaires en mode utilisateur listés dans le GRL.

</dd> <dt>

**cRevokedCertificateRenewals**
</dt> <dd>

Nombre de renouvellements de certificats listés dans le GRL.

</dd> <dt>

**cbSignatureCoreOffset**
</dt> <dd>

Offset, en octets, entre le début de GRL et la signature de la section principale.

</dd> <dt>

**cbSignatureExtOffset**
</dt> <dd>

Offset, en octets, entre le début de GRL et la signature de la section extensible.

</dd> </dl>

## <a name="remarks"></a>Notes

Tous les entiers dans GRL ont un classement des octets little-endian. Toutes les structures sont alignées sur des limites de 1 octet.

Cette structure n’est pas déclarée dans un en-tête SDK. Pour utiliser cette structure, ajoutez la déclaration indiquée ici à votre code source.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Révocation de certificat OPM](opm-certificate-revocation.md)
</dt> <dt>

[Structures OPM](opm-structures.md)
</dt> </dl>

 

 




