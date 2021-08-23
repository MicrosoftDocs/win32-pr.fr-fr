---
title: Classe MicrosoftDNS_MBType
description: Sous-classe de MicrosoftDNS \_ ResourceRecord qui représente un enregistrement de ressource de boîte aux lettres (MB).
ms.assetid: b8f3b106-58f4-44b8-b2db-b00f1a495641
keywords:
- MicrosoftDNS_MBType de la classe DNS
- MicrosoftDNS_MBType de la classe DNS, Description
topic_type:
- apiref
api_name:
- MicrosoftDNS_MBType
- MicrosoftDNS_MBType.CreateInstanceFromPropertyData
- MicrosoftDNS_MBType.Modify
- MicrosoftDNS_MBType.MBHost
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccea0cc9c30fb8a46debedaa2aeb0811ed63b08005919c7f189d771fd7daed2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118163263"
---
# <a name="microsoftdns_mbtype-class"></a>MicrosoftDNS \_ MBType, classe

Sous-classe de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) qui représente un enregistrement de ressource de boîte aux lettres (MB).

La syntaxe suivante est simplifiée à partir du code MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
class MicrosoftDNS_MBType : MicrosoftDNS_ResourceRecord
{
  string MBHost;
};
```

## <a name="members"></a>Membres

La classe **MicrosoftDNS \_ MBType** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La classe **MicrosoftDNS \_ MBType** possède ces méthodes.



| Méthode                             | Description                                                                                                                                                                                                                                                                                                                               |
|:-----------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | Instancie un RR MB basé sur les données des paramètres d’entrée de la méthode : le nom du serveur DNS de l’enregistrement, le nom du conteneur, le nom du propriétaire de la boîte aux lettres, la classe (valeur par défaut = IN), la valeur de durée de vie et l’hôte de la boîte aux lettres. Elle retourne une référence au nouvel objet sous la forme d’un paramètre de sortie. <br/> Qualificateurs : implémentés, statiques<br/> |
| **Modify**                         | Met à jour l’hôte TTL et MB avec les valeurs spécifiées en tant que paramètres d’entrée de cette méthode. Si une nouvelle valeur n’est pas spécifiée pour un paramètre, la valeur actuelle du paramètre n’est pas modifiée. La méthode retourne une référence à l’objet modifié sous la forme d’un paramètre de sortie. <br/> Qualificateurs : implémentés<br/>        |



 

### <a name="properties"></a>Propriétés

La classe **MicrosoftDNS \_ MBType** a ces propriétés.

<dl> <dt>

**MBHost**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom de domaine complet qui spécifie un hôte de la boîte aux lettres spécifiée dans le nom du propriétaire de l’enregistrement.

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

[**Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS MBType**](microsoftdns-mbtype-createinstancefrompropertydata.md)
</dt> <dt>

[**Modifier la méthode de la \_ classe MBType MicrosoftDNS**](microsoftdns-mbtype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





