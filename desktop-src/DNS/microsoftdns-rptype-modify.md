---
title: Modifier la méthode de la classe MicrosoftDNS_RPType
description: La méthode modify met à jour un enregistrement de ressource de personne responsable (RP).
ms.assetid: a779b905-922c-42ff-b3d9-318b3a848230
keywords:
- Modifier la méthode DNS
- Modifier la méthode DNS, MicrosoftDNS_RPType classe
- MicrosoftDNS_RPType de la classe DNS, Modify, méthode
topic_type:
- apiref
api_name:
- MicrosoftDNS_RPType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d237879b883e21c3c6289542e4eae7b9703be64931af788f042b6cdbec2ca49
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119587489"
---
# <a name="modify-method-of-the-microsoftdns_rptype-class"></a>Modifier la méthode de la \_ classe RPType MicrosoftDNS

La méthode **Modify** met à jour un enregistrement de ressource de personne responsable (RP).

## <a name="syntax"></a>Syntaxe


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in, optional] string              RPMailbox,
  [in, optional] string              TXTDomainName,
  [out, ref]     MicrosoftDNS_RPType &RR
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*TTL* \[ dans, facultatif\]
</dt> <dd>

Durée, en secondes, pendant laquelle l’enregistrement de ressource peut être mis en cache par un programme de résolution DNS.

</dd> <dt>

*RPMailbox* \[ dans, facultatif\]
</dt> <dd>

Nom de domaine complet spécifiant la boîte aux lettres pour la personne responsable.

</dd> <dt>

*TXTDomainName* \[ dans, facultatif\]
</dt> <dd>

Nom de domaine complet pour lequel existent les enregistrements de ressource TXT.

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

[**MicrosoftDNS \_ RPType**](microsoftdns-rptype.md)
</dt> <dt>

[**Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS RPType**](microsoftdns-rptype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





