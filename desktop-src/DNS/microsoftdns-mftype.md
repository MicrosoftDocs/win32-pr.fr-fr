---
title: Classe MicrosoftDNS_MFType
description: Sous-classe de MicrosoftDNS \_ ResourceRecord qui représente un enregistrement de l’agent de transfert du courrier pour le domaine (MF).
ms.assetid: 0ba0fddd-c316-4a5b-ad65-6344dbe949c1
keywords:
- MicrosoftDNS_MFType de la classe DNS
- MicrosoftDNS_MFType de la classe DNS, Description
topic_type:
- apiref
api_name:
- MicrosoftDNS_MFType
- MicrosoftDNS_MFType.CreateInstanceFromPropertyData
- MicrosoftDNS_MFType.Modify
- MicrosoftDNS_MFType.MFHost
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e030f695e95ee736b1c53a345201e0bd1addfe3e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104740"
---
# <a name="microsoftdns_mftype-class"></a>MicrosoftDNS \_ MFType, classe

Sous-classe de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) qui représente un enregistrement de l’agent de transfert du courrier pour le domaine (MF).

La syntaxe suivante est simplifiée à partir du code MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
class MicrosoftDNS_MFType : MicrosoftDNS_ResourceRecord
{
  string MFHost;
};
```

## <a name="members"></a>Membres

La classe **MicrosoftDNS \_ MFType** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La classe **MicrosoftDNS \_ MFType** possède ces méthodes.



| Méthode                             | Description                                                                                                                                                                                                                                                                                                                                                            |
|:-----------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | Cette méthode instancie un type MF de RR en fonction des données contenues dans les paramètres d’entrée de la méthode : le nom du serveur DNS de l’enregistrement, le nom du conteneur, le nom du propriétaire du domaine, la classe (valeur par défaut = IN), la valeur de la durée de vie et l’hôte de l’agent de messagerie. Elle retourne une référence au nouvel objet sous la forme d’un paramètre de sortie. <br/> Qualificateurs : implémentés, statiques<br/> |
| **Modify**                         | Cette méthode met à jour l’hôte TTL et MF avec les valeurs spécifiées en tant que paramètres d’entrée de cette méthode. Si une nouvelle valeur n’est pas spécifiée pour un paramètre, la valeur actuelle du paramètre n’est pas modifiée. La méthode retourne une référence à l’objet modifié sous la forme d’un paramètre de sortie. <br/> Qualificateurs : implémentés<br/>                         |



 

### <a name="properties"></a>Propriétés

La classe **MicrosoftDNS \_ MFType** a ces propriétés.

<dl> <dt>

**MFHost**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom de domaine complet spécifiant un ordinateur hôte avec un agent de messagerie qui va accepter le courrier pour le transfert vers le domaine spécifié.

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

[**Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS MFType**](microsoftdns-mftype-createinstancefrompropertydata.md)
</dt> <dt>

[**Modifier la méthode de la \_ classe MFType MicrosoftDNS**](microsoftdns-mftype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





