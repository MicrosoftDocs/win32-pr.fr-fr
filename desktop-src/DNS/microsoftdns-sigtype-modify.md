---
title: Modifier la méthode de la classe MicrosoftDNS_SIGType
description: La méthode modify met à jour une ressource de signature (SIG).
ms.assetid: 6a7017da-d3f1-4aba-a53a-96f578518304
keywords:
- Modifier la méthode DNS
- Modifier la méthode DNS, MicrosoftDNS_SIGType classe
- MicrosoftDNS_SIGType de la classe DNS, Modify, méthode
topic_type:
- apiref
api_name:
- MicrosoftDNS_SIGType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80fbaa25ec3b6a52aae06f99ed02d50430745dca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464526"
---
# <a name="modify-method-of-the-microsoftdns_sigtype-class"></a>Modifier la méthode de la \_ classe SIGType MicrosoftDNS

La méthode **Modify** met à jour une ressource de signature (SIG).

## <a name="syntax"></a>Syntaxe


```mof
void Modify(
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

## <a name="remarks"></a>Notes

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

[**MicrosoftDNS \_ SIGType**](microsoftdns-sigtype.md)
</dt> <dt>

[**Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS SIGType**](microsoftdns-sigtype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





