---
title: Modifier la méthode de la classe MicrosoftDNS_MGType
description: La méthode modify met à jour un enregistrement de ressource de groupe de messagerie (MG).
ms.assetid: c7d42964-19fb-410d-a434-85af20754e20
keywords:
- Modifier la méthode DNS
- Modifier la méthode DNS, MicrosoftDNS_MGType classe
- MicrosoftDNS_MGType de la classe DNS, Modify, méthode
topic_type:
- apiref
api_name:
- MicrosoftDNS_MGType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 706502569687a3c035c943e0a9dcc04aa1732492
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104737"
---
# <a name="modify-method-of-the-microsoftdns_mgtype-class"></a>Modifier la méthode de la \_ classe MGType MicrosoftDNS

La méthode **Modify** met à jour un enregistrement de ressource de groupe de messagerie (mg).

## <a name="syntax"></a>Syntaxe


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in, optional] string              MGMailbox,
  [out, ref]     MicrosoftDNS_MGType &RR
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*TTL* \[ dans, facultatif\]
</dt> <dd>

Durée, en secondes, pendant laquelle l’enregistrement de ressource peut être mis en cache par un programme de résolution DNS.

</dd> <dt>

*MGMailbox* \[ dans, facultatif\]
</dt> <dd>

Nom de domaine complet spécifiant une boîte aux lettres qui est membre du groupe de messagerie spécifié par le nom du propriétaire de l’enregistrement.

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

[**MicrosoftDNS \_ MGType**](microsoftdns-mgtype.md)
</dt> <dt>

[**Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS MGType**](microsoftdns-mgtype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





