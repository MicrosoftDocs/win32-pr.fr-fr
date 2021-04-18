---
title: Classe MicrosoftDNS_X25Type
description: Sous-classe de MicrosoftDNS \_ ResourceRecord qui représente un enregistrement X. 25 (X25).
ms.assetid: 1213dfd7-30b3-413e-b723-f4284fa0b416
keywords:
- MicrosoftDNS_X25Type de la classe DNS
- MicrosoftDNS_X25Type de la classe DNS, Description
topic_type:
- apiref
api_name:
- MicrosoftDNS_X25Type
- MicrosoftDNS_X25Type.CreateInstanceFromPropertyData
- MicrosoftDNS_X25Type.Modify
- MicrosoftDNS_X25Type.PSDNAddress
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e584119dbd45d5d6c7fae347c506c42fcda4fff7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106529081"
---
# <a name="microsoftdns_x25type-class"></a>MicrosoftDNS \_ X25Type, classe

Sous-classe de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) qui représente un enregistrement X. 25 (X25).

La syntaxe suivante est simplifiée à partir du code MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
class MicrosoftDNS_X25Type : MicrosoftDNS_ResourceRecord
{
  string PSDNAddress;
};
```

## <a name="members"></a>Membres

La classe **MicrosoftDNS \_ X25Type** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La classe **MicrosoftDNS \_ X25Type** possède ces méthodes.



| Méthode                             | Description                                                                                                                                                                                                                                                                                                                                         |
|:-----------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | Instancie un type « X25 » de RR en fonction des données des paramètres d’entrée de la méthode : le nom du serveur DNS de l’enregistrement, le nom du conteneur, le nom du propriétaire, la classe (valeur par défaut = IN), la valeur de la durée de vie et l’adresse PSDN. Elle retourne une référence au nouvel objet sous la forme d’un paramètre de sortie. <br/> Qualificateurs : implémentés, statiques<br/>              |
| **Modify**                         | Cette méthode met à jour les adresses TTL et PSDN avec les valeurs spécifiées en tant que paramètres d’entrée de cette méthode. Si une nouvelle valeur n’est pas spécifiée pour un paramètre, la valeur actuelle du paramètre n’est pas modifiée. La méthode retourne une référence à l’objet modifié sous la forme d’un paramètre de sortie. <br/> Qualificateurs : implémentés<br/> |



 

### <a name="properties"></a>Propriétés

La classe **MicrosoftDNS \_ X25Type** a ces propriétés.

<dl> <dt>

**PSDNAddress**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Adresse PSDN du propriétaire de l’enregistrement de ressource.

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

[**Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS X25Type**](microsoftdns-x25type-createinstancefrompropertydata.md)
</dt> <dt>

[**Modifier la méthode de la \_ classe X25Type MicrosoftDNS**](microsoftdns-x25type-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





