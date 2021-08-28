---
title: Classe MicrosoftDNS_RPType
description: Sous-classe de MicrosoftDNS \_ ResourceRecord qui représente un enregistrement de personne responsable (RP).
ms.assetid: 2b1c1bbc-a69f-4480-a7f2-6420240d4ad8
keywords:
- MicrosoftDNS_RPType de la classe DNS
- MicrosoftDNS_RPType de la classe DNS, Description
topic_type:
- apiref
api_name:
- MicrosoftDNS_RPType
- MicrosoftDNS_RPType.CreateInstanceFromPropertyData
- MicrosoftDNS_RPType.Modify
- MicrosoftDNS_RPType.RPMailbox
- MicrosoftDNS_RPType.TXTDomainName
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2088420acc7a8d0e58cfa23ed95458c797dbe9f930651bc02f083fcc81f5342d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119655369"
---
# <a name="microsoftdns_rptype-class"></a>MicrosoftDNS \_ RPType, classe

Sous-classe de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) qui représente un enregistrement de personne responsable (RP).

La syntaxe suivante est simplifiée à partir du code MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
class MicrosoftDNS_RPType : MicrosoftDNS_ResourceRecord
{
  string RPMailbox;
  string TXTDomainName;
};
```

## <a name="members"></a>Membres

La classe **MicrosoftDNS \_ RPType** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La classe **MicrosoftDNS \_ RPType** possède ces méthodes.



| Méthode                             | Description                                                                                                                                                                                                                                                                                                                                                                                         |
|:-----------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | Instancie un type de ressource RP en fonction des données contenues dans les paramètres d’entrée de la méthode : le nom du serveur DNS, le nom du conteneur, le nom du propriétaire/de la personne responsable, la classe (valeur par défaut = IN), la valeur de durée de vie et les noms de domaine pour la boîte aux lettres et les emplacements des RR TXT de la personne. Elle retourne une référence au nouvel objet sous la forme d’un paramètre de sortie. <br/> Qualificateurs : implémentés, statiques<br/> |
| **Modify**                         | Cette méthode met à jour les noms de domaine TTL, RP et TXT sur les valeurs spécifiées comme paramètres d’entrée de cette méthode. Si une nouvelle valeur n’est pas spécifiée pour un paramètre, la valeur actuelle du paramètre n’est pas modifiée. La méthode retourne une référence à l’objet modifié sous la forme d’un paramètre de sortie. <br/> Qualificateurs : implémentés<br/>                                  |



 

### <a name="properties"></a>Propriétés

La classe **MicrosoftDNS \_ RPType** a ces propriétés.

<dl> <dt>

**RPMailbox**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom de domaine complet spécifiant la boîte aux lettres pour la personne responsable.

</dd> <dt>

**TXTDomainName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom de domaine complet pour lequel existent les enregistrements de ressource TXT.

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

[**Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS RPType**](microsoftdns-rptype-createinstancefrompropertydata.md)
</dt> <dt>

[**Modifier la méthode de la \_ classe RPType MicrosoftDNS**](microsoftdns-rptype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





