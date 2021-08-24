---
title: Méthode CreateInstanceFromPropertyData de la classe MicrosoftDNS_TXTType
description: La méthode CreateInstanceFromPropertyData instancie un enregistrement de ressource texte (TXT).
ms.assetid: f518bb07-e64f-4240-a7b8-9363374b83d6
keywords:
- Méthode CreateInstanceFromPropertyData DNS
- Méthode CreateInstanceFromPropertyData DNS, classe MicrosoftDNS_TXTType
- MicrosoftDNS_TXTType de la classe DNS, méthode CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_TXTType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb0d1282f5a9bedac25d808455907ac3faa8e001da58447506123b4b5f5b78a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119655299"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_txttype-class"></a>Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS TXTType

La méthode **CreateInstanceFromPropertyData** instancie un enregistrement de ressource texte (txt).

## <a name="syntax"></a>Syntaxe


```mof
void CreateInstanceFromPropertyData(
  [in]           string               DnsServerName,
  [in]           string               ContainerName,
  [in]           string               OwnerName,
  [in, optional] uint32               RecordClass = 1,
  [in, optional] uint32               TTL,
  [in]           string               DescriptiveText,
  [out, ref]     MicrosoftDNS_TXTType &RR
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*DnsServerName* \[ dans\]
</dt> <dd>

Nom de domaine complet ou adresse IP du serveur DNS qui contient ce RR.

</dd> <dt>

*ContainerName* \[ dans\]
</dt> <dd>

Nom du conteneur de la zone, du cache ou de l’instance RootHints qui contient ce RR.

</dd> <dt>

*OwnerName* \[ dans\]
</dt> <dd>

Nom du propriétaire de l’enregistrement de ressource.

</dd> <dt>

*RecordClass* \[ dans, facultatif\]
</dt> <dd>

Classe de l’enregistrement de ressource. La valeur par défaut est 1. Les valeurs suivantes sont valides.



| Valeur                                                                                                | Signification                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | DANS (Internet)<br/> |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | CS (CSNET)<br/>    |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | CH (CHAOS)<br/>    |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | HS (Hesiod)<br/>   |



 

</dd> <dt>

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

[**Modifier la méthode de la \_ classe TXTType MicrosoftDNS**](microsoftdns-txttype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





