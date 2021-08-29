---
title: Classe MicrosoftDNS_Statistic
description: La \_ classe statistique MicrosoftDNS représente une statistique de serveur DNS unique.
ms.assetid: 49ee79d6-b93f-4a9b-8054-1ad290d092d6
keywords:
- MicrosoftDNS_Statistic de la classe DNS
- MicrosoftDNS_Statistic de la classe DNS, Description
topic_type:
- apiref
api_name:
- MicrosoftDNS_Statistic
- MicrosoftDNS_Statistic.DnsServerName
- MicrosoftDNS_Statistic.CollectionName
- MicrosoftDNS_Statistic.CollectionId
- MicrosoftDNS_Statistic.Name
- MicrosoftDNS_Statistic.Value
- MicrosoftDNS_Statistic.StringValue
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a489f8a4d9e3d442d4157243594c187a799d20a1d07b3ccc68135e73ddce288
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119815659"
---
# <a name="microsoftdns_statistic-class"></a>\_Classe de statistiques MicrosoftDNS

La **classe \_ statistique MicrosoftDNS** représente une statistique de serveur DNS unique.

La syntaxe suivante est simplifiée à partir du code MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
class MicrosoftDNS_Statistic
{
  string DnsServerName;
  string CollectionName;
  uint32 CollectionId;
  string Name;
  uint32 Value;
  string StringValue;
};
```

## <a name="members"></a>Membres

La **classe \_ statistique MicrosoftDNS** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La **classe \_ statistique MicrosoftDNS** possède ces propriétés.

<dl> <dt>

**CollectionId**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Représentation numérique de **CollectionName**.

</dd> <dt>

**CollectionName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom de la collection à laquelle la statistique appartient.

</dd> <dt>

**DnsServerName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique le nom de domaine complet ou l’adresse IP du serveur DNS qui contient la statistique.

</dd> <dt>

**Nom**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom de la statistique.

</dd> <dt>

**StringValue**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Valeur de chaîne de la statistique, utilisée uniquement lorsque la valeur de statistique n’est pas représentée comme une valeur DWORD.

</dd> <dt>

**Valeur**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Valeur numérique de la statistique, représentée sous la forme d’un DWORD.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                              |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                   |
| Espace de noms<br/>                | \\MicrosoftDNS racine<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov. mof</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[MicrosoftDNS \_ StatisticCollection](microsoftdns-statisticcollection.md)
</dt> </dl>

 

 





