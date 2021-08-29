---
title: Classe MicrosoftDNS_MRType
description: Sous-classe de MicrosoftDNS \_ ResourceRecord qui représente un enregistrement de renommage de boîte aux lettres (Mr).
ms.assetid: fa5da18f-121b-477b-8876-6e337382e9b8
keywords:
- MicrosoftDNS_MRType de la classe DNS
- MicrosoftDNS_MRType de la classe DNS, Description
topic_type:
- apiref
api_name:
- MicrosoftDNS_MRType
- MicrosoftDNS_MRType.CreateInstanceFromPropertyData
- MicrosoftDNS_MRType.Modify
- MicrosoftDNS_MRType.MRMailbox
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 041b6a24a58e0d0c7ba8facd08369b37f76e7d3aab4e4e3730b326c306c43bbf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874789"
---
# <a name="microsoftdns_mrtype-class"></a>MicrosoftDNS \_ MRType, classe

Sous-classe de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) qui représente un enregistrement de renommage de boîte aux lettres (Mr).

La syntaxe suivante est simplifiée à partir du code MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
class MicrosoftDNS_MRType : MicrosoftDNS_ResourceRecord
{
  string MRMailbox;
};
```

## <a name="members"></a>Membres

La classe **MicrosoftDNS \_ MRType** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La classe **MicrosoftDNS \_ MRType** possède ces méthodes.



| Méthode                             | Description                                                                                                                                                                                                                                                                                                                                                       |
|:-----------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | Cette méthode instancie un type « MR » de RR en fonction des données des paramètres d’entrée de la méthode : le nom du serveur DNS de l’enregistrement, le nom du conteneur, le nom du propriétaire de la boîte aux lettres, la classe (valeur par défaut = IN), la valeur de durée de vie et le nom de la boîte aux lettres. Elle retourne une référence au nouvel objet sous la forme d’un paramètre de sortie. <br/> Qualificateurs : implémentés, statiques<br/> |
| **Modify**                         | Cette méthode met à jour la durée de vie et la boîte aux lettres MR avec les valeurs spécifiées en tant que paramètres d’entrée de cette méthode. Si une nouvelle valeur n’est pas spécifiée pour un paramètre, la valeur actuelle du paramètre n’est pas modifiée. La méthode retourne une référence à l’objet modifié sous la forme d’un paramètre de sortie. <br/> Qualificateurs : implémentés<br/>                 |



 

### <a name="properties"></a>Propriétés

La classe **MicrosoftDNS \_ MRType** a ces propriétés.

<dl> <dt>

**MRMailbox**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom de domaine complet spécifiant une boîte aux lettres qui est le nom correct de la boîte aux lettres spécifiée dans le nom du propriétaire de l’enregistrement.

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

[**Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS MRType**](microsoftdns-mrtype-createinstancefrompropertydata.md)
</dt> <dt>

[**Modifier la méthode de la \_ classe MRType MicrosoftDNS**](microsoftdns-mrtype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





