---
title: Modifier la méthode de la classe MicrosoftDNS_SOAType
description: La méthode modify met à jour un enregistrement de ressource SOA (Start of Authority).
ms.assetid: 531b770d-9ac9-43da-8595-fbc175b51b23
keywords:
- Modifier la méthode DNS
- Modifier la méthode DNS, MicrosoftDNS_SOAType classe
- MicrosoftDNS_SOAType de la classe DNS, Modify, méthode
topic_type:
- apiref
api_name:
- MicrosoftDNS_SOAType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74785804ebed8266443f0dd708a5d122e350a6cf88b91f228d2ce266481dffaa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119825079"
---
# <a name="modify-method-of-the-microsoftdns_soatype-class"></a>Modifier la méthode de la \_ classe SOAType MicrosoftDNS

La méthode **Modify** met à jour un enregistrement de ressource SOA (Start of Authority).

## <a name="syntax"></a>Syntaxe


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in, optional] uint32               SerialNumber,
  [in, optional] string               PrimaryServer,
  [in, optional] string               ResponsibleParty,
  [in, optional] uint32               RefreshInterval,
  [in, optional] uint32               RetryDelay,
  [in, optional] uint32               ExpireLimit,
  [in, optional] uint32               MinimumTTL,
  [out, ref]     MicrosoftDNS_SOAType &RR
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*TTL* \[ dans, facultatif\]
</dt> <dd>

Durée, en secondes, pendant laquelle l’enregistrement de ressource peut être mis en cache par un programme de résolution DNS.

</dd> <dt>

*SerialNumber* \[ dans, facultatif\]
</dt> <dd>

Numéro de série SOA représentant le nombre de fois que la zone a été mise à jour, utilisée par les [*serveurs secondaires*](s-gly.md) pour déterminer si le transfert de zone est nécessaire.

</dd> <dt>

*PrimaryServer* \[ dans, facultatif\]
</dt> <dd>

Nom du serveur principal.

</dd> <dt>

*ResponsibleParty* \[ dans, facultatif\]
</dt> <dd>

Adresse de la boîte aux lettres du tiers responsable, sous la forme alias. Domain, par exemple xyz.microsoft.com. Notez l’utilisation d’un point plutôt que d’un symbole arobase (@).

</dd> <dt>

*RefreshInterval* \[ dans, facultatif\]
</dt> <dd>

Durée, en secondes, avant l’actualisation de la zone contenant cet enregistrement.

</dd> <dt>

*RetryDelay* \[ dans, facultatif\]
</dt> <dd>

Durée, en secondes, pendant laquelle le serveur DNS doit différer entre les tentatives de résolution de noms.

</dd> <dt>

*ExpireLimit* \[ dans, facultatif\]
</dt> <dd>

Durée, en secondes, pendant laquelle les serveurs secondaires doivent attendre une réponse du serveur principal avant d’ignorer leurs copies du fichier de zone comme étant non valides.

</dd> <dt>

*MinimumTTL* \[ dans, facultatif\]
</dt> <dd>

Durée de vie (en secondes) appliquée aux enregistrements de ressources de la zone qui ne spécifient pas leur propre durée de vie.

</dd> <dt>

*RR* \[ out, Ref\]
</dt> <dd>

Référence à l’objet modifié

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

[**MicrosoftDNS \_ SOAType**](microsoftdns-soatype.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





