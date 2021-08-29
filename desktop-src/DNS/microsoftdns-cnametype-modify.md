---
title: Modifier la méthode de la classe MicrosoftDNS_CNAMEType
description: La méthode modify met à jour un enregistrement de ressource de nom canonique (CNAMe).
ms.assetid: 7e550026-d901-44a0-86ac-520682232ccb
keywords:
- Modifier la méthode DNS
- Modifier la méthode DNS, MicrosoftDNS_CNAMEType classe
- MicrosoftDNS_CNAMEType de la classe DNS, Modify, méthode
topic_type:
- apiref
api_name:
- MicrosoftDNS_CNAMEType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac4fe65904c04ae7c7379898943f28b15e19d796e157e50694ef9146e12f372f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104039"
---
# <a name="modify-method-of-the-microsoftdns_cnametype-class"></a>Modifier la méthode de la \_ classe CNAMEType MicrosoftDNS

La méthode **Modify** met à jour un enregistrement de ressource de nom canonique (CNAME).

## <a name="syntax"></a>Syntaxe


```mof
void Modify(
  [in, optional] uint32                 TTL,
  [in, optional] string                 PrimaryName,
  [out, ref]     MicrosoftDNS_CNAMEType &RR
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*TTL* \[ dans, facultatif\]
</dt> <dd>

Durée, en secondes, pendant laquelle l’enregistrement de ressource peut être mis en cache par un programme de résolution DNS.

</dd> <dt>

*PrimaryName* \[ dans, facultatif\]
</dt> <dd>

Chaîne représentant le nom principal de l’enregistrement CNAMe.

</dd> <dt>

*RR* \[ out, Ref\]
</dt> <dd>

Référence à l’objet modifié.

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

[**MicrosoftDNS \_ CNAMEType**](microsoftdns-cnametype.md)
</dt> <dt>

[**Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS CNAMEType**](microsoftdns-cnametype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





