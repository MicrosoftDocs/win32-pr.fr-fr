---
title: Classe MicrosoftDNS_CNAMEType
description: Sous-classe de MicrosoftDNS \_ ResourceRecord qui représente un enregistrement de nom canonique (CNAME).
ms.assetid: 93a972e3-abb1-425f-beb7-32abe7d0b485
keywords:
- MicrosoftDNS_CNAMEType de la classe DNS
- MicrosoftDNS_CNAMEType de la classe DNS, Description
topic_type:
- apiref
api_name:
- MicrosoftDNS_CNAMEType
- MicrosoftDNS_CNAMEType.CreateInstanceFromPropertyData
- MicrosoftDNS_CNAMEType.Modify
- MicrosoftDNS_CNAMEType.PrimaryName
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e819380726fb311d3e892ff3ae1610890f87330cc3d15ac7e9459985aa775354
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076843"
---
# <a name="microsoftdns_cnametype-class"></a>MicrosoftDNS \_ CNAMEType, classe

Sous-classe de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) qui représente un enregistrement de nom canonique (CNAME).

La syntaxe suivante est simplifiée à partir du code MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
class MicrosoftDNS_CNAMEType : MicrosoftDNS_ResourceRecord
{
  string PrimaryName;
};
```

## <a name="members"></a>Membres

La classe **MicrosoftDNS \_ CNAMEType** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La classe **MicrosoftDNS \_ CNAMEType** possède ces méthodes.



| Méthode                             | Description                                                                                                                                                                                                                                                                                                                                                    |
|:-----------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | Instancie un enregistrement de ressource CNAMe en fonction des données contenues dans les paramètres d’entrée de la méthode : le nom du serveur DNS, le nom du conteneur, le nom du propriétaire, la classe (valeur par défaut = IN), la valeur de la durée de vie et le nom principal de l’enregistrement CNAMe. Elle retourne une référence au nouvel objet sous la forme d’un paramètre de sortie. <br/> Qualificateurs : implémentés, statiques<br/> |
| **Modify**                         | Met à jour la durée de vie et le nom principal avec les valeurs spécifiées en tant que paramètres d’entrée de cette méthode. Si une nouvelle valeur n’est pas spécifiée pour un paramètre, la valeur actuelle du paramètre n’est pas modifiée. La méthode retourne une référence à l’objet modifié sous la forme d’un paramètre de sortie. <br/> Qualificateurs : implémentés<br/>                        |



 

### <a name="properties"></a>Propriétés

La classe **MicrosoftDNS \_ CNAMEType** a ces propriétés.

<dl> <dt>

**PrimaryName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom canonique ou nom principal du propriétaire de l’enregistrement CNAMe.

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

[**Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS CNAMEType**](microsoftdns-cnametype-createinstancefrompropertydata.md)
</dt> <dt>

[**Modifier la méthode de la \_ classe CNAMEType MicrosoftDNS**](microsoftdns-cnametype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





