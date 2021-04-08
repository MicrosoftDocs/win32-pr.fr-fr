---
title: Modifier la méthode de la classe MicrosoftDNS_WKSType
description: La méthode modify met à jour un enregistrement de ressource Well-Known services (WKS).
ms.assetid: 3a9100eb-dc90-45bb-9739-14026da100fd
keywords:
- Modifier la méthode DNS
- Modifier la méthode DNS, MicrosoftDNS_WKSType classe
- MicrosoftDNS_WKSType de la classe DNS, Modify, méthode
topic_type:
- apiref
api_name:
- MicrosoftDNS_WKSType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30f7cf58a231d93288a3cdc170fa857bb12687af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843861"
---
# <a name="modify-method-of-the-microsoftdns_wkstype-class"></a>Modifier la méthode de la \_ classe WKSType MicrosoftDNS

La méthode **Modify** met à jour un enregistrement de ressource Well-Known services (WKS).

## <a name="syntax"></a>Syntaxe


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in, optional] uint32               InternetAddress,
  [in, optional] uint8                IPProtocol,
  [in, optional] uint8                Services,
  [out, ref]     MicrosoftDNS_WKSType &RR
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*TTL* \[ dans, facultatif\]
</dt> <dd>

Durée, en secondes, pendant laquelle l’enregistrement de ressource peut être mis en cache par un programme de résolution DNS.

</dd> <dt>

*InternetAddress* \[ dans, facultatif\]
</dt> <dd>

Adresse IP Internet pour le propriétaire de l’enregistrement.

</dd> <dt>

*IPProtocol* \[ dans, facultatif\]
</dt> <dd>

Chaîne représentant le protocole IP pour cet enregistrement. Les valeurs valides sont UDP ou TCP.

</dd> <dt>

*Services* \[ dans, facultatif\]
</dt> <dd>

Chaîne contenant tous les services utilisés par l’enregistrement du service bien connu (WKS).

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

[**MicrosoftDNS \_ WKSType**](microsoftdns-wkstype.md)
</dt> <dt>

[**Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS WKSType**](microsoftdns-wkstype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





