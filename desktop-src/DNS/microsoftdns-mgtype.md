---
title: Classe MicrosoftDNS_MGType
description: Sous-classe de MicrosoftDNS \_ ResourceRecord qui représente un enregistrement de groupe de messagerie (mg).
ms.assetid: ce5795d1-e575-46ef-ad82-62b329e261d6
keywords:
- MicrosoftDNS_MGType de la classe DNS
- MicrosoftDNS_MGType de la classe DNS, Description
topic_type:
- apiref
api_name:
- MicrosoftDNS_MGType
- MicrosoftDNS_MGType.CreateInstanceFromPropertyData
- MicrosoftDNS_MGType.Modify
- MicrosoftDNS_MGType.MGMailbox
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4772f8841977fbeae1f0bf609a65a9511bc704a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509370"
---
# <a name="microsoftdns_mgtype-class"></a>MicrosoftDNS \_ MGType, classe

Sous-classe de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) qui représente un enregistrement de groupe de messagerie (mg).

La syntaxe suivante est simplifiée à partir du code MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
class MicrosoftDNS_MGType : MicrosoftDNS_ResourceRecord
{
  string MGMailbox;
};
```

## <a name="members"></a>Membres

La classe **MicrosoftDNS \_ MGType** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La classe **MicrosoftDNS \_ MGType** possède ces méthodes.



| Méthode                             | Description                                                                                                                                                                                                                                                                                                                                                      |
|:-----------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | Cette méthode instancie un type de RR MG basé sur les données contenues dans les paramètres d’entrée de la méthode : le nom du serveur DNS de l’enregistrement, le nom du conteneur, le nom du propriétaire du groupe de messagerie, la classe (valeur par défaut = IN), la valeur de durée de vie et le nom de la boîte aux lettres. Elle retourne une référence au nouvel objet sous la forme d’un paramètre de sortie. <br/> Qualificateurs : implémentés, statiques<br/> |
| **Modify**                         | Cette méthode met à jour la boîte aux lettres TTL et MG avec les valeurs spécifiées comme paramètres d’entrée de cette méthode. Si une nouvelle valeur n’est pas spécifiée pour un paramètre, la valeur actuelle du paramètre n’est pas modifiée. La méthode retourne une référence à l’objet modifié sous la forme d’un paramètre de sortie. <br/> Qualificateurs : implémentés<br/>                |



 

### <a name="properties"></a>Propriétés

La classe **MicrosoftDNS \_ MGType** a ces propriétés.

<dl> <dt>

**MGMailbox**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom de domaine complet spécifiant une boîte aux lettres qui est membre du groupe de messagerie spécifié par le nom du propriétaire de l’enregistrement.

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

[**Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS MGType**](microsoftdns-mgtype-createinstancefrompropertydata.md)
</dt> <dt>

[**Modifier la méthode de la \_ classe MGType MicrosoftDNS**](microsoftdns-mgtype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





