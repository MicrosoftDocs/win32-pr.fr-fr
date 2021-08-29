---
title: Classe MicrosoftDNS_ATMAType
description: Sous-classe de MicrosoftDNS \_ ResourceRecord qui représente un enregistrement d’adresse ATM dans le nom (ATMA).
ms.assetid: 3e9e4032-08a0-4a2e-bcff-f461b69a44d4
keywords:
- MicrosoftDNS_ATMAType de la classe DNS
- MicrosoftDNS_ATMAType de la classe DNS, Description
topic_type:
- apiref
api_name:
- MicrosoftDNS_ATMAType
- MicrosoftDNS_ATMAType.CreateInstanceFromPropertyData
- MicrosoftDNS_ATMAType.Modify
- MicrosoftDNS_ATMAType.Format
- MicrosoftDNS_ATMAType.ATMAddress
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 441fdfb8e07ad7206d21a1979381089cf03bfa875251f084eddbd45fba0f4e16
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119795643"
---
# <a name="microsoftdns_atmatype-class"></a>MicrosoftDNS \_ ATMAType, classe

Sous-classe de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) qui représente un enregistrement d’adresse ATM dans le nom (ATMA).

La syntaxe suivante est simplifiée à partir du code MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
class MicrosoftDNS_ATMAType : MicrosoftDNS_ResourceRecord
{
  uint16 Format;
  string ATMAddress;
};
```

## <a name="members"></a>Membres

La classe **MicrosoftDNS \_ ATMAType** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La classe **MicrosoftDNS \_ ATMAType** possède ces méthodes.



| Méthode                             | Description                                                                                                                                                                                                                                                                                                                                        |
|:-----------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | Instancie un enregistrement de ressource ATMA en fonction des données contenues dans les paramètres d’entrée de la méthode : le nom du serveur DNS, le nom du conteneur, le nom du propriétaire/nœud, la classe (valeur par défaut = IN), la valeur de durée de vie et le format et l’adresse ATM. Retourne une référence au nouvel objet sous la forme d’un paramètre de sortie. <br/> Qualificateurs : implémentés, statiques<br/> |
| **Modify**                         | Met à jour l’adresse TTL, format et ATMA avec les valeurs spécifiées en tant que paramètres d’entrée de cette méthode. Si une nouvelle valeur n’est pas spécifiée pour un paramètre, la valeur actuelle du paramètre n’est pas modifiée. La méthode retourne une référence à l’objet modifié sous la forme d’un paramètre de sortie. <br/> Qualificateurs : implémentés<br/>         |



 

### <a name="properties"></a>Propriétés

La classe **MicrosoftDNS \_ ATMAType** a ces propriétés.

<dl> <dt>

**ATMAddress**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Chaîne de longueur variable d’octets contenant l’adresse ATM du nœud/propriétaire auquel appartient ce RR. Les 4 premiers octets du tableau sont utilisés pour stocker la taille de la chaîne d’octets. L’octet le plus significatif est stocké à l’octet 0.

</dd> <dt>

**Format**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Format d’adresse ATM. Les valeurs valides sont : 0 indiquant le format AESA (ATM End System Address) et 1 indiquant le format E. 164.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                              |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                   |
| Espace de noms<br/>                | \\MicrosoftDNS racine<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov. mof</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS ATMAType**](microsoftdns-atmatype-createinstancefrompropertydata.md)
</dt> <dt>

[**Modifier la méthode de la \_ classe ATMAType MicrosoftDNS**](microsoftdns-atmatype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





