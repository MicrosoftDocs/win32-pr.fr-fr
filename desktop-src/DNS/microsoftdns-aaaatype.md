---
title: Classe MicrosoftDNS_AAAAType
description: Sous-classe de MicrosoftDNS \_ ResourceRecord qui représente un enregistrement d’adresse IPv6 (aaaa). L’enregistrement AAAA est généralement prononcé \ 0034 ; enregistrement Quad-a \ 0034 ;.
ms.assetid: e16a7a69-18df-43dc-add9-700a702724ce
keywords:
- MicrosoftDNS_AAAAType de la classe DNS
- MicrosoftDNS_AAAAType de la classe DNS, Description
topic_type:
- apiref
api_name:
- MicrosoftDNS_AAAAType
- MicrosoftDNS_AAAAType.CreateInstanceFromPropertyData
- MicrosoftDNS_AAAAType.Modify
- MicrosoftDNS_AAAAType.IPv6Address
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0131177c342730c08868946c29356554cbfb9cab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509321"
---
# <a name="microsoftdns_aaaatype-class"></a>MicrosoftDNS \_ AAAAType, classe

Sous-classe de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) qui représente un enregistrement d’adresse IPv6 (aaaa). L’enregistrement AAAA est couramment dit « enregistrement Quad-a ».

La syntaxe suivante est simplifiée à partir du code MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
class MicrosoftDNS_AAAAType : MicrosoftDNS_ResourceRecord
{
  string IPv6Address;
};
```

## <a name="members"></a>Membres

La classe **MicrosoftDNS \_ AAAAType** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La classe **MicrosoftDNS \_ AAAAType** possède ces méthodes.



| Méthode                             | Description                                                                                                                                                                                                                                                                                                                                  |
|:-----------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | Instancie un type « AAAA » de RR en fonction des données des paramètres d’entrée de la méthode : le nom du serveur DNS, le nom du conteneur, le propriétaire/nom d’hôte, la classe (valeur par défaut = IN), la valeur de durée de vie et l’adresse IPv6. Elle retourne une référence au nouvel objet sous la forme d’un paramètre de sortie. <br/> Qualificateurs : implémentés, statiques<br/> |
| **Modify**                         | Met à jour l’adresse TTL et IPv6 avec les valeurs spécifiées en tant que paramètres d’entrée de cette méthode. Si une nouvelle valeur n’est pas spécifiée pour un paramètre, la valeur actuelle du paramètre n’est pas modifiée. La méthode retourne une référence à l’objet modifié sous la forme d’un paramètre de sortie. <br/> Qualificateurs : implémentés<br/>      |



 

### <a name="properties"></a>Propriétés

La classe **MicrosoftDNS \_ AAAAType** a ces propriétés.

<dl> <dt>

**IPv6Address**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Adresse IPv6 de l’hôte.

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

[**Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS AAAAType**](microsoftdns-aaaatype-createinstancefrompropertydata.md)
</dt> <dt>

[**Modifier la méthode de la \_ classe AAAAType MicrosoftDNS**](microsoftdns-aaaatype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





