---
description: Contient des informations sur un fournisseur de services de chiffrement de carte à puce (CSP).
ms.assetid: b3e6722a-25dd-4137-b224-4082e846ddec
title: Structure KERB_SMARTCARD_CSP_INFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KERB_SMARTCARD_CSP_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 190c3e770a50acb7363fb10c469a7400831bc7b512d2b8158d687c83403b6df9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127339"
---
# <a name="kerb_smartcard_csp_info-structure"></a>\_Structure d' \_ informations du CSP de carte à puce KERB \_

La structure des **\_ \_ \_ informations du CSP** de carte à puce KERB contient des informations sur un [*fournisseur de services de chiffrement*](../secgloss/c-gly.md) de carte à puce (CSP).

Cette structure n’est pas déclarée dans un en-tête public.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _KERB_SMARTCARD_CSP_INFO {
  DWORD dwCspInfoLen;
  DWORD MessageType;
  union {
    PVOID   ContextInformation;
    ULONG64 SpaceHolderForWow64;
  };
  DWORD flags;
  DWORD KeySpec;
  ULONG nCardNameOffset;
  ULONG nReaderNameOffset;
  ULONG nContainerNameOffset;
  ULONG nCSPNameOffset;
  TCHAR bBuffer;
} KERB_SMARTCARD_CSP_INFO, *PKERB_SMARTCARD_CSP_INFO;
```



## <a name="members"></a>Membres

<dl> <dt>

**dwCspInfoLen**
</dt> <dd>

Taille, en octets, de cette structure, y compris les données ajoutées.

</dd> <dt>

**MessageType**
</dt> <dd>

Type de message passé. Ce membre doit avoir la valeur 1.

</dd> <dt>

**ContextInformation**
</dt> <dd>

Réservé.

</dd> <dt>

**SpaceHolderForWow64**
</dt> <dd>

Réservé.

</dd> <dt>

**flags**
</dt> <dd>

Réservé.

</dd> <dt>

**KeySpec**
</dt> <dd>

Clé privée à utiliser à partir du conteneur de clé spécifié dans la mémoire tampon **bBuffer**. La clé peut être l’une des valeurs suivantes, définie dans WinCrypt. h.



| Valeur                                                                                                                                                                                                                   | Signification                                   |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------|
| <span id="AT_KEYEXCHANGE"></span><span id="at_keyexchange"></span><dl> <dt>**À \_ KeyExchange**</dt> <dt>1</dt> </dl> | La clé est une clé d’échange de clé.<br/> |
| <span id="AT_SIGNATURE"></span><span id="at_signature"></span><dl> <dt>**À \_ SIGNATURE**</dt> <dt>2</dt> </dl>       | La clé est une clé de signature.<br/>    |



 

</dd> <dt>

**nCardNameOffset**
</dt> <dd>

Nombre de caractères dans la mémoire tampon **bBuffer** qui précèdent le nom de la carte à puce dans cette mémoire tampon.

> [!IMPORTANT]
> Si le nom de la carte à puce n’est pas fourni, la mémoire tampon doit contenir une chaîne vide.

 

</dd> <dt>

**nReaderNameOffset**
</dt> <dd>

Nombre de caractères dans la mémoire tampon **bBuffer** qui précèdent le nom du lecteur de carte à puce dans cette mémoire tampon.

> [!IMPORTANT]
> Si le nom du lecteur de carte à puce n’est pas fourni, la mémoire tampon doit contenir une chaîne vide.

 

</dd> <dt>

**nContainerNameOffset**
</dt> <dd>

Nombre de caractères dans la mémoire tampon **bBuffer** qui précèdent le nom du conteneur de clé dans cette mémoire tampon. Cette chaîne ne peut pas être vide.

</dd> <dt>

**nCSPNameOffset**
</dt> <dd>

Nombre de caractères dans la mémoire tampon **bBuffer** qui précèdent le nom du fournisseur de services de chiffrement dans cette mémoire tampon.

</dd> <dt>

**bBuffer**
</dt> <dd>

Tableau de caractères initialisé à une longueur de `sizeof(DWORD)` . Cette mémoire tampon contient les noms référencés par les membres **nCardNameOffset**, **nReaderNameOffset**, **nContainerNameOffset** et **nCSPNameOffset** , ainsi que toutes les données supplémentaires fournies par le fournisseur de services de chiffrement.

Les noms qui ne sont pas fournis doivent être représentés dans cette mémoire tampon par des chaînes vides.

</dd> </dl>

## <a name="remarks"></a>Remarques

Lorsque cette structure est sérialisée, les membres de la structure doivent être alignés sur les limites qui sont des multiples de 2 octets.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_connexion au certificat KERB \_**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-kerb_certificate_logon)
</dt> </dl>

 

 
