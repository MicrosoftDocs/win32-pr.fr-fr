---
title: Modifier la méthode de la classe MicrosoftDNS_AType
description: La méthode modify met à jour la durée de vie et l’adresse IP d’un enregistrement de ressource d’adresse d’hôte (A).
ms.assetid: fe01549d-7135-499d-a5a5-cd31ea106f53
keywords:
- Modifier la méthode DNS
- Modifier la méthode DNS, MicrosoftDNS_AType classe
- MicrosoftDNS_AType de la classe DNS, Modify, méthode
topic_type:
- apiref
api_name:
- MicrosoftDNS_AType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5d9f4740aeec92726796943e53b4d2143a6378341b061aaa7d3f3f6bf6dc7d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118163480"
---
# <a name="modify-method-of-the-microsoftdns_atype-class"></a>Modifier la méthode de la \_ classe aType MicrosoftDNS

La méthode **Modify** met à jour la durée de vie et l’adresse IP d’un enregistrement de ressource d’adresse d’hôte (a).

## <a name="syntax"></a>Syntaxe


```mof
void Modify(
  [in, optional] uint32             TTL,
  [in, optional] string             IPAddress,
  [out, ref]     MicrosoftDNS_AType &RR
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*TTL* \[ dans, facultatif\]
</dt> <dd>

Durée, en secondes, pendant laquelle l’enregistrement de ressource peut être mis en cache par un programme de résolution DNS.

</dd> <dt>

*Adresse IP* \[ dans, facultatif\]
</dt> <dd>

Chaîne représentant l’adresse IP de l’hôte.

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

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> <dt>

[**Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS aType**](microsoftdns-atype-createinstancefrompropertydata.md)
</dt> </dl>

 

 





