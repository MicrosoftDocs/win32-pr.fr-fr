---
title: Modifier la méthode de la classe MicrosoftDNS_TXTType
description: La méthode modify met à jour un enregistrement de ressource texte (TXT).
ms.assetid: af61057e-95be-4290-83da-a63f01ead476
keywords:
- Modifier la méthode DNS
- Modifier la méthode DNS, MicrosoftDNS_TXTType classe
- MicrosoftDNS_TXTType de la classe DNS, Modify, méthode
topic_type:
- apiref
api_name:
- MicrosoftDNS_TXTType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e565d4c48b048b4d72b11c939b644752cb14f1993c2810f127bb14f60bec929
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957298"
---
# <a name="modify-method-of-the-microsoftdns_txttype-class"></a>Modifier la méthode de la \_ classe TXTType MicrosoftDNS

La méthode **Modify** met à jour un enregistrement de ressource texte (txt).

## <a name="syntax"></a>Syntaxe


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in]           string               DescriptiveText,
  [out, ref]     MicrosoftDNS_TXTType &RR
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*TTL* \[ dans, facultatif\]
</dt> <dd>

Durée, en secondes, pendant laquelle l’enregistrement de ressource peut être mis en cache par un programme de résolution DNS.

</dd> <dt>

*DescriptiveText* \[ dans\]
</dt> <dd>

Texte descriptif, dont la sémantique dépend du domaine propriétaire.

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

[**MicrosoftDNS \_ TXTType**](microsoftdns-txttype.md)
</dt> <dt>

[**Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS TXTType**](microsoftdns-txttype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





