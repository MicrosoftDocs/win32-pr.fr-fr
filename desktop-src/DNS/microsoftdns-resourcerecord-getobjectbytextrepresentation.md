---
title: Méthode GetObjectByTextRepresentation de la classe MicrosoftDNS_ResourceRecord
description: La méthode GetObjectByTextRepresentation récupère une instance existante de la classe MicrosoftDNS \_ ResourceRecord.
ms.assetid: d25e10de-81fa-4220-b2b8-d9a65298b629
keywords:
- Méthode GetObjectByTextRepresentation DNS
- Méthode GetObjectByTextRepresentation DNS, classe MicrosoftDNS_ResourceRecord
- MicrosoftDNS_ResourceRecord de la classe DNS, méthode GetObjectByTextRepresentation
topic_type:
- apiref
api_name:
- MicrosoftDNS_ResourceRecord.GetObjectByTextRepresentation
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2aea2588a70ff4bdab89eae58b65715152d6c7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465682"
---
# <a name="getobjectbytextrepresentation-method-of-the-microsoftdns_resourcerecord-class"></a>Méthode GetObjectByTextRepresentation de la \_ classe MicrosoftDNS ResourceRecord

La méthode **GetObjectByTextRepresentation** récupère une instance existante de la classe [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) .

## <a name="syntax"></a>Syntaxe


```mof
void GetObjectByTextRepresentation(
  [in]  string                      DnsServerName,
  [in]  string                      ContainerName,
  [in]  string                      TextRepresentation,
  [out] MicrosoftDns_ResourceRecord RR
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*DnsServerName* \[ dans\]
</dt> <dd>

Nom du serveur DNS à partir duquel le RR doit être récupéré.

</dd> <dt>

*ContainerName* \[ dans\]
</dt> <dd>

Nom du conteneur à partir duquel l’enregistrement de ressource doit être obtenu.

</dd> <dt>

*TextRepresentation* \[ dans\]
</dt> <dd>

Représentation textuelle du RR à récupérer.

</dd> <dt>

*RR* \[ à\]
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

[**Méthode CreateInstanceFromTextRepresentation de la \_ classe MicrosoftDNS ResourceRecord**](microsoftdns-resourcerecord-createinstancefromtextrepresentation.md)
</dt> </dl>

 

 





