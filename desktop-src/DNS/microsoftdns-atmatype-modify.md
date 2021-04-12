---
title: Modifier la méthode de la classe MicrosoftDNS_ATMAType
description: La méthode modify met à jour un enregistrement de ressource d’adresse ATM en nom (ATMA).
ms.assetid: 202fc38d-fb8f-4044-bb7d-9e041cbde8ec
keywords:
- Modifier la méthode DNS
- Modifier la méthode DNS, MicrosoftDNS_ATMAType classe
- MicrosoftDNS_ATMAType de la classe DNS, Modify, méthode
topic_type:
- apiref
api_name:
- MicrosoftDNS_ATMAType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48d784e9421641dc53d64bb39a2e97b0d9ef257b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032872"
---
# <a name="modify-method-of-the-microsoftdns_atmatype-class"></a>Modifier la méthode de la \_ classe ATMAType MicrosoftDNS

La méthode **Modify** met à jour un enregistrement de ressource d’adresse ATM en nom (ATMA).

## <a name="syntax"></a>Syntaxe


```mof
void Modify(
  [in, optional] uint32                TTL,
  [in, optional] uint16                Format,
  [in, optional] string                ATMAddress,
  [out, ref]     MicrosoftDNS_ATMAType &RR
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*TTL* \[ dans, facultatif\]
</dt> <dd>

Durée, en secondes, pendant laquelle l’enregistrement de ressource peut être mis en cache par un programme de résolution DNS.

</dd> <dt>

*Format* \[ dans, facultatif\]
</dt> <dd>

Format d’adresse ATM. Deux valeurs possibles pour FORMAT sont : 0 indiquant le format AESA (ATM End System Address) et 1 indiquant le format E. 164.

</dd> <dt>

*ATMAddress* \[ dans, facultatif\]
</dt> <dd>

Chaîne de longueur variable d’octets contenant l’adresse ATM du nœud/propriétaire auquel appartient ce RR. Les quatre premiers octets du tableau sont utilisés pour stocker la taille de la chaîne d’octets. L’octet le plus significatif est stocké à l’octet 0.

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

[**MicrosoftDNS \_ ATMAType**](microsoftdns-atmatype.md)
</dt> <dt>

[**Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS ATMAType**](microsoftdns-atmatype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





