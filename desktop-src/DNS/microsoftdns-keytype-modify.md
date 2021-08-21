---
title: Modifier la méthode de la classe MicrosoftDNS_KEYType
description: La méthode modify met à jour un enregistrement de ressource clé.
ms.assetid: 0ea1e0e5-ccd1-4800-b0c3-27795c36250c
keywords:
- Modifier la méthode DNS
- Modifier la méthode DNS, MicrosoftDNS_KEYType classe
- MicrosoftDNS_KEYType de la classe DNS, Modify, méthode
topic_type:
- apiref
api_name:
- MicrosoftDNS_KEYType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff5b657e940716a7afa2113dcbdc6836ab3680c1dfe37b88a454d9bdd0c7bc28
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118163255"
---
# <a name="modify-method-of-the-microsoftdns_keytype-class"></a>Modify, méthode de la \_ classe KeyType de MicrosoftDNS

La méthode **Modify** met à jour un enregistrement de ressource clé.

## <a name="syntax"></a>Syntaxe


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in, optional] uint16               Flags,
  [in, optional] uint16               Protocol,
  [in, optional] uint16               Algorithm,
  [in, optional] string               PublicKey,
  [out, ref]     MicrosoftDNS_KEYType &RR
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*TTL* \[ dans, facultatif\]
</dt> <dd>

Durée, en secondes, pendant laquelle l’enregistrement de ressource peut être mis en cache par un programme de résolution DNS.

</dd> <dt>

*Indicateurs* \[ dans, facultatif\]
</dt> <dd>

Indicateurs utilisés pour spécifier le mappage, comme décrit dans la norme IETF RFC 2535.

</dd> <dt>

*Protocole* \[ dans, facultatif\]
</dt> <dd>

Protocole pour lequel la clé spécifiée dans le RR peut être utilisée. Les valeurs affectées sont indiquées dans le tableau suivant.



| Valeur                                                                                                    | Signification                  |
|----------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl>     | TLS<br/>           |
| <span id="2"></span><dl> <dt>**2**</dt> </dl>     | Courrier électronique<br/>        |
| <span id="3"></span><dl> <dt>**3**</dt> </dl>     | DNSSEC<br/>        |
| <span id="4"></span><dl> <dt>**4**</dt> </dl>     | IPsec<br/>         |
| <span id="255"></span><dl> <dt>**255**</dt> </dl> | Tous les protocoles<br/> |



 

</dd> <dt>

*Algorithme* \[ dans, facultatif\]
</dt> <dd>

Algorithme utilisé avec la clé spécifiée dans l’enregistrement de ressource. Les valeurs affectées sont indiquées dans le tableau suivant.



| Valeur                                                                                                | Signification                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | RSA/MD5 (RFC 2537)<br/>          |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Diffie-Hellman (RFC 2539)<br/>   |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | DSA (RFC 2536)<br/>              |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | Chiffrement à courbe elliptique<br/> |



 

</dd> <dt>

*PublicKey* \[ dans, facultatif\]
</dt> <dd>

Clé publique, représentée dans la base 64, comme décrit dans l’annexe A de la RFC 2535.

</dd> <dt>

*RR* \[ out, Ref\]
</dt> <dd>

Référence au nouvel objet.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Tout paramètre non spécifié reste inchangé dans l’enregistrement modifié.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                              |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                   |
| Espace de noms<br/>                | \\MicrosoftDNS racine<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov. mof</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MicrosoftDNS, \_ KeyType**](microsoftdns-keytype.md)
</dt> <dt>

[**Méthode CreateInstanceFromPropertyData de la \_ classe KeyType de MicrosoftDNS**](microsoftdns-keytype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





