---
title: Méthode CreateInstanceFromTextRepresentation de la classe MicrosoftDNS_ResourceRecord
description: La méthode CreateInstanceFromTextRepresentation instancie un \_ objet ResourceRecord MicrosoftDNS.
ms.assetid: 19600a9a-f75d-40ad-98e5-f81465d10f79
keywords:
- Méthode CreateInstanceFromTextRepresentation DNS
- Méthode CreateInstanceFromTextRepresentation DNS, classe MicrosoftDNS_ResourceRecord
- MicrosoftDNS_ResourceRecord de la classe DNS, méthode CreateInstanceFromTextRepresentation
topic_type:
- apiref
api_name:
- MicrosoftDNS_ResourceRecord.CreateInstanceFromTextRepresentation
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a8ee7f92db1185fe2762b0b308b4fbafdbdd80e7417c7b615939c72333f15e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104019"
---
# <a name="createinstancefromtextrepresentation-method-of-the-microsoftdns_resourcerecord-class"></a>Méthode CreateInstanceFromTextRepresentation de la \_ classe MicrosoftDNS ResourceRecord

La méthode **CreateInstanceFromTextRepresentation** instancie un [**objet \_ ResourceRecord MicrosoftDNS**](microsoftdns-resourcerecord.md) .

## <a name="syntax"></a>Syntaxe


```mof
void CreateInstanceFromTextRepresentation(
  [in]       string                      DnsServerName,
  [in]       string                      ContainerName,
  [in]       string                      TextRepresentation,
  [out, ref] MicrosoftDNS_ResourceRecord &RR
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*DnsServerName* \[ dans\]
</dt> <dd>

Nom du serveur DNS sur lequel le RR doit être créé.

</dd> <dt>

*ContainerName* \[ dans\]
</dt> <dd>

Nom du conteneur dans lequel le nouvel enregistrement de ressource doit être placé.

</dd> <dt>

*TextRepresentation* \[ dans\]
</dt> <dd>

Représentation textuelle de l’instance de RR à créer.

</dd> <dt>

*RR* \[ out, Ref\]
</dt> <dd>

Référence à l’enregistrement de ressource instancié.

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

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> <dt>

[**Méthode GetObjectByTextRepresentation de la \_ classe MicrosoftDNS ResourceRecord**](microsoftdns-resourcerecord-getobjectbytextrepresentation.md)
</dt> </dl>

 

 





