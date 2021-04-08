---
title: Modifier la méthode de la classe MicrosoftDNS_AAAAType
description: La méthode modify met à jour un enregistrement de ressource d’adresse IPv6 (AAAA).
ms.assetid: d58f8a88-8473-4b26-89f0-237d2457f00b
keywords:
- Modifier la méthode DNS
- Modifier la méthode DNS, MicrosoftDNS_AAAAType classe
- MicrosoftDNS_AAAAType de la classe DNS, Modify, méthode
topic_type:
- apiref
api_name:
- MicrosoftDNS_AAAAType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc216233fe3d41e4f1e31fe0d471e766c4dc8476
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843597"
---
# <a name="modify-method-of-the-microsoftdns_aaaatype-class"></a>Modifier la méthode de la \_ classe AAAAType MicrosoftDNS

La méthode **Modify** met à jour un enregistrement de ressource d’adresse IPv6 (aaaa).

## <a name="syntax"></a>Syntaxe


```mof
void Modify(
  [in, optional] uint32                TTL,
  [in, optional] string                IPv6Address,
  [out, ref]     MicrosoftDNS_AAAAType &RR
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*TTL* \[ dans, facultatif\]
</dt> <dd>

Durée, en secondes, pendant laquelle l’enregistrement de ressource peut être mis en cache par un programme de résolution DNS.

</dd> <dt>

*AdresseIPv6* \[ dans, facultatif\]
</dt> <dd>

Adresse IPv6 de l’hôte.

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

[**MicrosoftDNS \_ AAAAType**](microsoftdns-aaaatype.md)
</dt> <dt>

[**Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS AAAAType**](microsoftdns-aaaatype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





