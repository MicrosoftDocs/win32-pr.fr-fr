---
title: Méthode CreateInstanceFromPropertyData de la classe MicrosoftDNS_SIGType
description: La méthode CreateInstanceFromPropertyData instancie un enregistrement de ressource signature (SIG).
ms.assetid: 8e83e56f-d2b3-4b71-be70-7d2640d49845
keywords:
- Méthode CreateInstanceFromPropertyData DNS
- Méthode CreateInstanceFromPropertyData DNS, classe MicrosoftDNS_SIGType
- MicrosoftDNS_SIGType de la classe DNS, méthode CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_SIGType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c21660572d9557e6425b459c5694a7eeee4722cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032481"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_sigtype-class"></a>Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS SIGType

La méthode **CreateInstanceFromPropertyData** instancie un enregistrement de ressource signature (SIG).

## <a name="syntax"></a>Syntaxe


```mof
void CreateInstanceFromPropertyData(
  [in]           string               DnsServerName,
  [in]           string               ContainerName,
  [in]           string               OwnerName,
  [in, optional] uint32               RecordClass = 1,
  [in, optional] uint32               TTL,
  [in]           uint16               TypeCovered,
  [in]           uint16               Algorithm,
  [in]           uint16               Labels,
  [in]           uint32               OriginalTTL,
  [in]           uint32               SignatureExpiration,
  [in]           uint32               SignatureInception,
  [in]           uint16               KeyTag,
  [in]           string               SignerName,
  [in]           string               Signature,
  [out, ref]     MicrosoftDNS_SIGType &RR
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*DnsServerName* \[ dans\]
</dt> <dd>

Nom de domaine complet ou adresse IP du serveur DNS qui contient ce RR.

</dd> <dt>

*ContainerName* \[ dans\]
</dt> <dd>

Nom du conteneur de la zone, du cache ou de l’instance RootHints qui contient ce RR.

</dd> <dt>

*OwnerName* \[ dans\]
</dt> <dd>

Nom du propriétaire de l’enregistrement de ressource.

</dd> <dt>

*RecordClass* \[ dans, facultatif\]
</dt> <dd>

Classe de l’enregistrement de ressource. La valeur par défaut est 1. Les valeurs suivantes sont valides.



| Valeur                                                                                                | Signification                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | DANS (Internet)<br/> |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | CS (CSNET)<br/>    |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | CH (CHAOS)<br/>    |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | HS (Hesiod)<br/>   |



 

</dd> <dt>

*TTL* \[ dans, facultatif\]
</dt> <dd>

Durée, en secondes, pendant laquelle l’enregistrement de ressource peut être mis en cache par un programme de résolution DNS.

</dd> <dt>

*TypeCovered* \[ dans\]
</dt> <dd>

Type d’enregistrement de ressource couvert par ce SIG.

</dd> <dt>

*Algorithme* \[ dans\]
</dt> <dd>

Algorithme utilisé avec la clé spécifiée dans l’enregistrement de ressource. Les valeurs affectées sont indiquées dans le tableau suivant.



| Valeur                                                                                                | Signification                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | RSA/MD5 (RFC 2537)<br/>          |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Diffie-Hellman (RFC 2539)<br/>   |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | DSA (RFC 2536)<br/>              |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | Chiffrement à courbe elliptique<br/> |



 

</dd> <dt>

*Étiquettes* \[ dans\]
</dt> <dd>

Nombre non signé d’étiquettes dans le nom du propriétaire du RR SIG d’origine. Le nombre n’inclut pas l’étiquette NULL pour la racine, ni les caractères génériques initiaux.

</dd> <dt>

*OriginalTTL* \[ dans\]
</dt> <dd>

TTL de l’ensemble de RR signé par SIG.

</dd> <dt>

*SignatureExpiration* \[ dans\]
</dt> <dd>

Date d’expiration de la signature, exprimée en secondes depuis le 1er janvier 1970, heure de Greenwich (GMT), à l’exception des secondes bissextiles.

</dd> <dt>

*SignatureInception* \[ dans\]
</dt> <dd>

Date et heure auxquelles la signature devient valide, exprimée en secondes depuis le 1er janvier 1970, heure de Greenwich (GMT), à l’exception des secondes bissextiles.

</dd> <dt>

*KeyTag* \[ dans\]
</dt> <dd>

Méthode utilisée pour choisir une clé qui vérifie un SIG. Consultez RFC 2535, annexe C, pour connaître la méthode utilisée pour calculer un KeyTag.

</dd> <dt>

*SignerName* \[ dans\]
</dt> <dd>

Nom de domaine du signataire qui a généré le RR SIG.

</dd> <dt>

*Signature* \[ dans\]
</dt> <dd>

Signature, représentée dans la base 64, mise en forme comme défini dans la RFC 2535, annexe A.

</dd> <dt>

*RR* \[ out, Ref\]
</dt> <dd>

Référence au nouvel objet.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                              |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                   |
| Espace de noms<br/>                | \\MicrosoftDNS racine<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov. mof</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MicrosoftDNS \_ SIGType**](microsoftdns-sigtype.md)
</dt> <dt>

[**Modifier la méthode de la \_ classe SIGType MicrosoftDNS**](microsoftdns-sigtype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





