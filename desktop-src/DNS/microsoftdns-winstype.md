---
title: Classe MicrosoftDNS_WINSType
description: sous-classe de MicrosoftDNS \_ ResourceRecord qui représente un enregistrement WINS (Windows Internet Name Service).
ms.assetid: 8f891d80-ee4d-4641-8a6c-159c78e5cf86
keywords:
- MicrosoftDNS_WINSType de la classe DNS
- MicrosoftDNS_WINSType de la classe DNS, Description
topic_type:
- apiref
api_name:
- MicrosoftDNS_WINSType
- MicrosoftDNS_WINSType.CreateInstanceFromPropertyData
- MicrosoftDNS_WINSType.Modify
- MicrosoftDNS_WINSType.MappingFlag
- MicrosoftDNS_WINSType.LookupTimeout
- MicrosoftDNS_WINSType.CacheTimeout
- MicrosoftDNS_WINSType.WinsServers
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 089faa6fa3cda6780b600dbf6c296fd1ce71f902428e6c2abe16f92dada1e219
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118162839"
---
# <a name="microsoftdns_winstype-class"></a>MicrosoftDNS \_ WINSType, classe

sous-classe de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) qui représente un enregistrement WINS (Windows Internet Name Service).

La syntaxe suivante est simplifiée à partir du code MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
class MicrosoftDNS_WINSType : MicrosoftDNS_ResourceRecord
{
  uint32 MappingFlag;
  uint32 LookupTimeout;
  uint32 CacheTimeout;
  string WinsServers;
};
```

## <a name="members"></a>Membres

La classe **MicrosoftDNS \_ WINSType** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La classe **MicrosoftDNS \_ WINSType** possède ces méthodes.



| Méthode                             | Description                                                                                                                                                                                                                                                                                                                                                                                                  |
|:-----------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | Instancie un type WINS de RR en fonction des données contenues dans les paramètres d’entrée de la méthode : le nom du serveur DNS, le nom du conteneur, le nom du propriétaire, la classe (valeur par défaut = IN), la valeur de durée de vie et l’indicateur de mappage WINS, le délai d’attente de la recherche, le délai d’expiration du cache et la liste Elle retourne une référence au nouvel objet sous la forme d’un paramètre de sortie. <br/> Qualificateurs : implémentés, statiques<br/> |
| **Modify**                         | Met à jour les valeurs spécifiées en tant que paramètres d’entrée de cette méthode pour la durée de vie, l’indicateur de mappage, le délai d’attente de recherche, le délai d’attente du cache et les serveurs WINS. Si une nouvelle valeur n’est pas spécifiée pour un paramètre, la valeur actuelle du paramètre n’est pas modifiée. La méthode retourne une référence à l’objet modifié sous la forme d’un paramètre de sortie. <br/> Qualificateurs : implémentés<br/>                      |



 

### <a name="properties"></a>Propriétés

La classe **MicrosoftDNS \_ WINSType** a ces propriétés.

<dl> <dt>

**CacheTimeout**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Durée, en secondes, pendant laquelle un serveur DNS qui utilise WINS peut mettre en cache la réponse du serveur WINS.

</dd> <dt>

**LookupTimeout**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Durée, en secondes, pendant laquelle un serveur DNS tente de résoudre à l’aide de la recherche WINS.

</dd> <dt>

**MappingFlag**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indicateur de mappage WINS qui spécifie si l’enregistrement doit être inclus dans la réplication de zone. Elle ne peut avoir que deux valeurs : 0x80000000 et 0x00010000 correspondant respectivement aux indicateurs de réplication et de non-réplication (enregistrement local). Les valeurs suivantes sont valides.



| Valeur                                                                                                                                               | Signification                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="0x80000000"></span><span id="0X80000000"></span><dl> <dt>**0x80000000**</dt> </dl> | Indicateur de réplication<br/>                   |
| <span id="0x00010000"></span><span id="0X00010000"></span><dl> <dt>**0x00010000**</dt> </dl> | Indicateur de non-réplication (enregistrement local)<br/> |



 

</dd> <dt>

**WinsServers**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Liste des adresses IP séparées par des virgules des serveurs WINS utilisés dans les recherches WINS.

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

[**Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS WINSType**](microsoftdns-winstype-createinstancefrompropertydata.md)
</dt> <dt>

[**Modifier la méthode de la \_ classe WINSType MicrosoftDNS**](microsoftdns-winstype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





