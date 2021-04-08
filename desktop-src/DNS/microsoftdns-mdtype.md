---
title: Classe MicrosoftDNS_MDType
description: Sous-classe de MicrosoftDNS \_ ResourceRecord qui représente un agent de messagerie pour un enregistrement de domaine (MD).
ms.assetid: 11242372-65fe-44ee-845b-2430aec59127
keywords:
- MicrosoftDNS_MDType de la classe DNS
- MicrosoftDNS_MDType de la classe DNS, Description
topic_type:
- apiref
api_name:
- MicrosoftDNS_MDType
- MicrosoftDNS_MDType.CreateInstanceFromPropertyData
- MicrosoftDNS_MDType.Modify
- MicrosoftDNS_MDType.MDHost
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7641fda7a223fed7c2dc9229c5a3449c575e84ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843537"
---
# <a name="microsoftdns_mdtype-class"></a>MicrosoftDNS \_ MDType, classe

Sous-classe de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) qui représente un agent de messagerie pour un enregistrement de domaine (MD).

La syntaxe suivante est simplifiée à partir du code MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
class MicrosoftDNS_MDType : MicrosoftDNS_ResourceRecord
{
  string MDHost;
};
```

## <a name="members"></a>Membres

La classe **MicrosoftDNS \_ MDType** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La classe **MicrosoftDNS \_ MDType** possède ces méthodes.



| Méthode                             | Description                                                                                                                                                                                                                                                                                                                                                        |
|:-----------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | Instancie un enregistrement de ressource DNS MD en fonction des données contenues dans les paramètres d’entrée de la méthode : le nom du serveur DNS de l’enregistrement, le nom du conteneur, le nom du propriétaire du domaine, la classe (valeur par défaut = IN), la valeur de durée de vie et l’hôte de l’agent de messagerie. Elle retourne une référence au nouvel objet sous la forme d’un paramètre de sortie. <br/> Qualificateurs : implémentés, statiques<br/> |
| **Modify**                         | Met à jour les hôtes TTL et MD avec les valeurs spécifiées en tant que paramètres d’entrée de cette méthode. Si une nouvelle valeur n’est pas spécifiée pour un paramètre, la valeur actuelle du paramètre n’est pas modifiée. La méthode retourne une référence à l’objet modifié sous la forme d’un paramètre de sortie. <br/> Qualificateurs : implémentés<br/>                                 |



 

### <a name="properties"></a>Propriétés

La classe **MicrosoftDNS \_ MDType** a ces propriétés.

<dl> <dt>

**MDHost**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom de domaine complet qui spécifie un hôte avec un agent de messagerie capable de transmettre des messages pour le domaine spécifié.

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

[**Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS MDType**](microsoftdns-mdtype-createinstancefrompropertydata.md)
</dt> <dt>

[**Modifier la méthode de la \_ classe MDType MicrosoftDNS**](microsoftdns-mdtype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





