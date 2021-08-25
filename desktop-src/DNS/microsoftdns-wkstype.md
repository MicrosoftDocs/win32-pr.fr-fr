---
title: Classe MicrosoftDNS_WKSType
description: Sous-classe de MicrosoftDNS \_ ResourceRecord qui représente un enregistrement Well-Known services (WKS).
ms.assetid: 7bbfd518-d473-4127-949b-9133a43ac7a7
keywords:
- MicrosoftDNS_WKSType de la classe DNS
- MicrosoftDNS_WKSType de la classe DNS, Description
topic_type:
- apiref
api_name:
- MicrosoftDNS_WKSType
- MicrosoftDNS_WKSType.CreateInstanceFromPropertyData
- MicrosoftDNS_WKSType.Modify
- MicrosoftDNS_WKSType.InternetAddress
- MicrosoftDNS_WKSType.IPProtocol
- MicrosoftDNS_WKSType.Services
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f82a6621e3dedacd5520c00b71c66bf0091c31135b70f27486ba43da63f393da
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874759"
---
# <a name="microsoftdns_wkstype-class"></a>MicrosoftDNS \_ WKSType, classe

Sous-classe de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) qui représente un enregistrement Well-Known services (WKS).

La syntaxe suivante est simplifiée à partir du code MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
class MicrosoftDNS_WKSType : MicrosoftDNS_ResourceRecord
{
  string InternetAddress;
  string IPProtocol;
  string Services;
};
```

## <a name="members"></a>Membres

La classe **MicrosoftDNS \_ WKSType** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La classe **MicrosoftDNS \_ WKSType** possède ces méthodes.



| Méthode                             | Description                                                                                                                                                                                                                                                                                                                                                                     |
|:-----------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | Instancie un type WKS de RR en fonction des données contenues dans les paramètres d’entrée de la méthode : le nom du serveur DNS de l’enregistrement, le nom du conteneur, le nom du propriétaire, la classe (valeur par défaut = IN), la valeur de la durée de vie et l’adresse Internet du propriétaire, le protocole IP et le masque de bits du port. Elle retourne une référence au nouvel objet sous la forme d’un paramètre de sortie. <br/> Qualificateurs : implémentés, statiques<br/>  |
| **Modify**                         | Cette méthode met à jour la durée de vie, l’adresse Internet, le protocole IP et les services avec les valeurs spécifiées en tant que paramètres d’entrée de cette méthode. Si une nouvelle valeur n’est pas spécifiée pour un paramètre, la valeur actuelle du paramètre n’est pas modifiée. La méthode retourne une référence à l’objet modifié sous la forme d’un paramètre de sortie. <br/> Qualificateurs : implémentés<br/> |



 

### <a name="properties"></a>Propriétés

La classe **MicrosoftDNS \_ WKSType** a ces propriétés.

<dl> <dt>

**InternetAddress**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Adresse IP Internet pour le propriétaire de l’enregistrement.

</dd> <dt>

**IPProtocol**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Chaîne représentant le protocole IP pour cet enregistrement. Les valeurs valides sont UDP ou TCP.

</dd> <dt>

**Services**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Chaîne contenant tous les services utilisés par l’enregistrement du service bien connu (WKS).

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

[**Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS WKSType**](microsoftdns-wkstype-createinstancefrompropertydata.md)
</dt> <dt>

[**Modifier la méthode de la \_ classe WKSType MicrosoftDNS**](microsoftdns-wkstype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





