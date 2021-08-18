---
title: Modifier la méthode de la classe MicrosoftDNS_MXType
description: La méthode modify met à jour un enregistrement de ressource de serveur de messagerie (MR).
ms.assetid: 40267ac9-0392-4e08-a5d2-145ee9639c39
keywords:
- Modifier la méthode DNS
- Modifier la méthode DNS, MicrosoftDNS_MXType classe
- MicrosoftDNS_MXType de la classe DNS, Modify, méthode
topic_type:
- apiref
api_name:
- MicrosoftDNS_MXType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74fb31da6bf0861c94c54163fa9c771ac592fca105a5459214e17031c3b8e6a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076783"
---
# <a name="modify-method-of-the-microsoftdns_mxtype-class"></a>Modifier la méthode de la \_ classe MXType MicrosoftDNS

La méthode **Modify** met à jour un enregistrement de ressource de serveur de messagerie (Mr).

## <a name="syntax"></a>Syntaxe


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in, optional] uint16              Preference,
  [in, optional] string              MailExchange,
  [out, ref]     MicrosoftDNS_MXType &RR
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*TTL* \[ dans, facultatif\]
</dt> <dd>

Durée, en secondes, pendant laquelle l’enregistrement de ressource peut être mis en cache par un programme de résolution DNS.

</dd> <dt>

*Préférence* \[ dans, facultatif\]
</dt> <dd>

Préférence donnée à ce RR, parmi d’autres au même propriétaire. Les valeurs les plus basses sont préférées.

</dd> <dt>

*MailExchange* \[ dans, facultatif\]
</dt> <dd>

Nom de domaine complet spécifiant un ordinateur hôte prêt à agir comme échange de messagerie pour le nom du propriétaire.

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

[**MicrosoftDNS \_ MXType**](microsoftdns-mxtype.md)
</dt> <dt>

[**Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS MXType**](microsoftdns-mxtype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





