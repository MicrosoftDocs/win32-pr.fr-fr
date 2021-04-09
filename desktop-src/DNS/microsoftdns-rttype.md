---
title: Classe MicrosoftDNS_RTType
description: Sous-classe de MicrosoftDNS \_ ResourceRecord qui représente un enregistrement d’itinéraire (RT).
ms.assetid: 986e2bbf-4f45-4611-906e-66079fda7f4c
keywords:
- MicrosoftDNS_RTType de la classe DNS
- MicrosoftDNS_RTType de la classe DNS, Description
topic_type:
- apiref
api_name:
- MicrosoftDNS_RTType
- MicrosoftDNS_RTType.CreateInstanceFromPropertyData
- MicrosoftDNS_RTType.Modify
- MicrosoftDNS_RTType.Preference
- MicrosoftDNS_RTType.IntermediateHost
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d867185d8ce07a54a47eb5ea7591ec8d68a11059
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942279"
---
# <a name="microsoftdns_rttype-class"></a>MicrosoftDNS \_ RTType, classe

Sous-classe de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) qui représente un enregistrement d’itinéraire (RT).

La syntaxe suivante est simplifiée à partir du code MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
class MicrosoftDNS_RTType : MicrosoftDNS_ResourceRecord
{
  uint16 Preference;
  string IntermediateHost;
};
```

## <a name="members"></a>Membres

La classe **MicrosoftDNS \_ RTType** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La classe **MicrosoftDNS \_ RTType** possède ces méthodes.



| Méthode                             | Description                                                                                                                                                                                                                                                                                                                                                      |
|:-----------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | Instancie un type RT de RR en fonction des données contenues dans les paramètres d’entrée de la méthode : le nom du serveur DNS de l’enregistrement, le nom du conteneur, le propriétaire/nom d’hôte, la classe (valeur par défaut = IN), la valeur de durée de vie, la préférence d’enregistrement et le nom d’hôte intermédiaire. Elle retourne une référence au nouvel objet sous la forme d’un paramètre de sortie. <br/> Qualificateurs : implémentés, statiques<br/> |
| **Modify**                         | Met à jour la durée de vie, la préférence et l’hôte intermédiaire sur les valeurs spécifiées comme paramètres d’entrée de cette méthode. Si une nouvelle valeur n’est pas spécifiée pour un paramètre, la valeur actuelle du paramètre n’est pas modifiée. La méthode retourne une référence à l’objet modifié sous la forme d’un paramètre de sortie. <br/> Qualificateurs : implémentés<br/>        |



 

### <a name="properties"></a>Propriétés

La classe **MicrosoftDNS \_ RTType** a ces propriétés.

<dl> <dt>

**IntermediateHost**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom de domaine complet spécifiant un hôte qui servira de intermédiaire pour atteindre l’hôte spécifié par le propriétaire.

</dd> <dt>

**Relatives**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Préférence donnée à ce RR, parmi d’autres au même propriétaire. Les valeurs les plus basses sont préférées.

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

[**Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS RTType**](microsoftdns-rttype-createinstancefrompropertydata.md)
</dt> <dt>

[**Modifier la méthode de la \_ classe RTType MicrosoftDNS**](microsoftdns-rttype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





