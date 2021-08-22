---
title: Modifier la méthode de la classe MicrosoftDNS_WINSRType
description: La méthode modify met à jour un enregistrement de ressource WINSR de recherche inversée (WINSr).
ms.assetid: 28be0045-5b0d-4434-a2a9-b56191f1e213
keywords:
- Modifier la méthode DNS
- Modifier la méthode DNS, MicrosoftDNS_WINSRType classe
- MicrosoftDNS_WINSRType de la classe DNS, Modify, méthode
topic_type:
- apiref
api_name:
- MicrosoftDNS_WINSRType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9db7865110b0e79642dc91671094c06dfbd10e07cd89684dab58623a9456cca9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076663"
---
# <a name="modify-method-of-the-microsoftdns_winsrtype-class"></a>Modifier la méthode de la \_ classe WINSRType MicrosoftDNS

La méthode **Modify** met à jour un enregistrement de ressource WINSR de recherche inversée (WINSR).

## <a name="syntax"></a>Syntaxe


```mof
void Modify(
  [in, optional] uint32                 TTL,
  [in, optional] uint32                 MappingFlag,
  [in, optional] uint32                 LookupTimeout,
  [in, optional] uint32                 CacheTimeout,
  [in, optional] string                 ResultDomain,
  [out, ref]     MicrosoftDNS_WINSRType &RR
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*TTL* \[ dans, facultatif\]
</dt> <dd>

Durée, en secondes, pendant laquelle l’enregistrement de ressource peut être mis en cache par un programme de résolution DNS.

</dd> <dt>

*MappingFlag* \[ dans, facultatif\]
</dt> <dd>

Indicateur de mappage WINSr qui spécifie si l’enregistrement doit être inclus dans la réplication de zone. Elle ne peut avoir que deux valeurs : 0x80000000 et 0x00010000 correspondant respectivement aux indicateurs de réplication et de non-réplication (enregistrement local).

</dd> <dt>

*LookupTimeout* \[ dans, facultatif\]
</dt> <dd>

Délai d’attente, en secondes, pour un serveur DNS à l’aide de la recherche inversée WINS.

</dd> <dt>

*CacheTimeout* \[ dans, facultatif\]
</dt> <dd>

Durée, en secondes, pendant laquelle un serveur DNS utilisant WINS recherche peut mettre en cache la réponse du serveur WINS.

</dd> <dt>

*ResultDomain* \[ dans, facultatif\]
</dt> <dd>

Nom de domaine à ajouter aux noms NetBIOS retournés.

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

[**MicrosoftDNS \_ WINSRType**](microsoftdns-winsrtype.md)
</dt> <dt>

[**Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS WINSRType**](microsoftdns-winsrtype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





