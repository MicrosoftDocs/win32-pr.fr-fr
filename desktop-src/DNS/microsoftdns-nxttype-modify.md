---
title: Modifier la méthode de la classe MicrosoftDNS_NXTType
description: La méthode modify met à jour un enregistrement de ressource (NXT) suivant.
ms.assetid: 5a21b843-0761-4022-b00a-9dbcd6814454
keywords:
- Modifier la méthode DNS
- Modifier la méthode DNS, MicrosoftDNS_NXTType classe
- MicrosoftDNS_NXTType de la classe DNS, Modify, méthode
topic_type:
- apiref
api_name:
- MicrosoftDNS_NXTType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e43082ff829a7b8701701e9b099aa0f36d274879bfb6f281272096558f1c8bd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118163200"
---
# <a name="modify-method-of-the-microsoftdns_nxttype-class"></a>Modifier la méthode de la \_ classe NXTType MicrosoftDNS

La méthode **Modify** met à jour un enregistrement de ressource (NXT) suivant.

## <a name="syntax"></a>Syntaxe


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in]           string               NextDomainName,
  [in]           string               Types,
  [out, ref]     MicrosoftDNS_NXTType &RR
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*TTL* \[ dans, facultatif\]
</dt> <dd>

Durée, en secondes, pendant laquelle l’enregistrement de ressource peut être mis en cache par un programme de résolution DNS.

</dd> <dt>

*NextDomainName* \[ dans\]
</dt> <dd>

Nom de domaine suivant.

</dd> <dt>

*Types* \[ dans\]
</dt> <dd>

Liste séparée par des espaces des mnémoniques de type RR pour le nom de propriétaire de l’enregistrement de ressource NXT.

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

[**MicrosoftDNS \_ NXTType**](microsoftdns-nxttype.md)
</dt> <dt>

[**Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS NXTType**](microsoftdns-nxttype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





