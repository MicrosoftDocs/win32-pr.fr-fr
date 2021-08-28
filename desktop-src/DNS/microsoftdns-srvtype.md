---
title: Classe MicrosoftDNS_SRVType
description: Sous-classe de MicrosoftDNS \_ ResourceRecord qui représente un enregistrement de service (SRV).
ms.assetid: 4b36246d-4466-46d9-9267-180e43547ae6
keywords:
- MicrosoftDNS_SRVType de la classe DNS
- MicrosoftDNS_SRVType de la classe DNS, Description
topic_type:
- apiref
api_name:
- MicrosoftDNS_SRVType
- MicrosoftDNS_SRVType.CreateInstanceFromPropertyData
- MicrosoftDNS_SRVType.Modify
- MicrosoftDNS_SRVType.Priority
- MicrosoftDNS_SRVType.Weight
- MicrosoftDNS_SRVType.Port
- MicrosoftDNS_SRVType.SRVDomainName
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aaff2c570647386ecd8d53592b940cbd54477764b323b5457dbec3357cf3b98c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104009"
---
# <a name="microsoftdns_srvtype-class"></a>MicrosoftDNS \_ SRVType, classe

Sous-classe de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) qui représente un enregistrement de service (SRV).

La syntaxe suivante est simplifiée à partir du code MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
class MicrosoftDNS_SRVType : MicrosoftDNS_ResourceRecord
{
  uint16 Priority;
  uint16 Weight;
  uint16 Port;
  string SRVDomainName;
};
```

## <a name="members"></a>Membres

La classe **MicrosoftDNS \_ SRVType** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La classe **MicrosoftDNS \_ SRVType** possède ces méthodes.



| Méthode                             | Description                                                                                                                                                                                                                                                                                                                                                                      |
|:-----------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | Instancie un type SRV de RR en fonction des données contenues dans les paramètres d’entrée de la méthode : le nom du serveur DNS de l’enregistrement, le nom du conteneur, le propriétaire/nom de la cible, la classe (valeur par défaut = IN), la valeur de durée de vie et la priorité, le poids, le port et le nom de domaine de l’hôte cible. Elle retourne une référence au nouvel objet sous la forme d’un paramètre de sortie. <br/> Qualificateurs : implémentés, statiques<br/> |
| **Modify**                         | Met à jour la durée de vie, la priorité, le poids, le port et le nom de domaine selon les valeurs spécifiées comme paramètres d’entrée de cette méthode. Si une nouvelle valeur n’est pas spécifiée pour un paramètre, la valeur actuelle du paramètre n’est pas modifiée. La méthode retourne une référence à l’objet modifié sous la forme d’un paramètre de sortie. <br/> Qualificateurs : implémentés<br/>                  |



 

### <a name="properties"></a>Propriétés

La classe **MicrosoftDNS \_ SRVType** a ces propriétés.

<dl> <dt>

**Port**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Port utilisé sur l’hôte cible d’un service de protocole.

</dd> <dt>

**Priorité**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Priorité de l’hôte cible spécifiée dans le nom du propriétaire. Les nombres inférieurs impliquent des priorités plus élevées.

</dd> <dt>

**SRVDomainName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom de domaine complet de l’hôte cible. Une cible de \\ . \\ signifie que le service n’est pas disponible dans ce domaine.

</dd> <dt>

**Poids**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Poids de l’hôte cible. Cela est utile lorsque vous sélectionnez parmi les hôtes qui ont la même priorité. La probabilité d’utiliser cet hôte doit être proportionnelle à son poids.

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

[**Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS SRVType**](microsoftdns-srvtype-createinstancefrompropertydata.md)
</dt> <dt>

[**Modifier la méthode de la \_ classe SRVType MicrosoftDNS**](microsoftdns-srvtype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





