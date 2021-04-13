---
title: Modifier la méthode de la classe MicrosoftDNS_MRType
description: La méthode modify met à jour un enregistrement de ressource de changement de nom de boîte aux lettres (MR).
ms.assetid: eb833735-d485-4603-9976-305244537acd
keywords:
- Modifier la méthode DNS
- Modifier la méthode DNS, MicrosoftDNS_MRType classe
- MicrosoftDNS_MRType de la classe DNS, Modify, méthode
topic_type:
- apiref
api_name:
- MicrosoftDNS_MRType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 996692301e8446b3fd67e20eca036cd085e83b03
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465226"
---
# <a name="modify-method-of-the-microsoftdns_mrtype-class"></a>Modifier la méthode de la \_ classe MRType MicrosoftDNS

La méthode **Modify** met à jour un enregistrement de ressource de changement de nom de boîte aux lettres (Mr).

## <a name="syntax"></a>Syntaxe


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in]           string              MRMailbox,
  [out, ref]     MicrosoftDNS_MRType &RR
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*TTL* \[ dans, facultatif\]
</dt> <dd>

Durée, en secondes, pendant laquelle l’enregistrement de ressource peut être mis en cache par un programme de résolution DNS.

</dd> <dt>

*MRMailbox* \[ dans\]
</dt> <dd>

Nom de domaine complet spécifiant une boîte aux lettres qui est le nom correct de la boîte aux lettres spécifiée dans le nom du propriétaire de l’enregistrement.

</dd> <dt>

*RR* \[ out, Ref\]
</dt> <dd>

Référence à l’objet modifié.

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

[**MicrosoftDNS \_ MRType**](microsoftdns-mrtype.md)
</dt> <dt>

[**Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS MRType**](microsoftdns-mrtype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





