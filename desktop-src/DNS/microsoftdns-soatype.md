---
title: Classe MicrosoftDNS_SOAType
description: Sous-classe de MicrosoftDNS \_ ResourceRecord qui représente un enregistrement SOA (Start of Authority).
ms.assetid: a5e6b6d3-7f5d-42e2-b3ed-2786f7aafb14
keywords:
- MicrosoftDNS_SOAType de la classe DNS
- MicrosoftDNS_SOAType de la classe DNS, Description
topic_type:
- apiref
api_name:
- MicrosoftDNS_SOAType
- MicrosoftDNS_SOAType.Modify
- MicrosoftDNS_SOAType.SerialNumber
- MicrosoftDNS_SOAType.PrimaryServer
- MicrosoftDNS_SOAType.ResponsibleParty
- MicrosoftDNS_SOAType.RefreshInterval
- MicrosoftDNS_SOAType.RetryDelay
- MicrosoftDNS_SOAType.ExpireLimit
- MicrosoftDNS_SOAType.MinimumTTL
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad2a9b0317c6e842558f771dcd10ec7707602e17510ffc20c3a9684fc94bf7d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118163143"
---
# <a name="microsoftdns_soatype-class"></a>MicrosoftDNS \_ SOAType, classe

Sous-classe de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) qui représente un enregistrement SOA (Start of Authority).

La syntaxe suivante est simplifiée à partir du code MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
class MicrosoftDNS_SOAType : MicrosoftDNS_ResourceRecord
{
  uint32 SerialNumber;
  string PrimaryServer;
  string ResponsibleParty;
  uint32 RefreshInterval;
  uint32 RetryDelay;
  uint32 ExpireLimit;
  uint32 MinimumTTL;
};
```

## <a name="members"></a>Membres

La classe **MicrosoftDNS \_ SOAType** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La classe **MicrosoftDNS \_ SOAType** possède ces méthodes.



| Méthode     | Description                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|:-----------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Modify** | Met à jour la durée de vie, le numéro de série SOA, le serveur principal, le tiers responsable, l’intervalle d’actualisation, le délai avant nouvelle tentative, la limite d’expiration et la durée de vie minimale (pour la zone) aux valeurs spécifiées comme paramètres d’entrée de cette méthode. Si une nouvelle valeur n’est pas spécifiée pour un paramètre, la valeur actuelle du paramètre n’est pas modifiée. La méthode retourne une référence à l’objet modifié sous la forme d’un paramètre de sortie. <br/> Qualificateurs : implémentés<br/> |



 

### <a name="properties"></a>Propriétés

La classe **MicrosoftDNS \_ SOAType** a ces propriétés.

<dl> <dt>

**ExpireLimit**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Durée, en secondes, avant qu’une zone qui ne réponde ne soit plus faisant autorité.

</dd> <dt>

**MinimumTTL**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Limite inférieure de la durée, en secondes, pendant laquelle un serveur DNS ou un programme de résolution de mise en cache est autorisé à mettre en cache un enregistrement de ressource de la zone à laquelle cet enregistrement appartient.

</dd> <dt>

**PrimaryServer**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Serveur DNS faisant autorité pour la zone à laquelle l’enregistrement appartient.

</dd> <dt>

**RefreshInterval**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Durée, en secondes, avant l’actualisation de la zone contenant cet enregistrement.

</dd> <dt>

**ResponsibleParty**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom du tiers responsable de la zone à laquelle l’enregistrement appartient.

</dd> <dt>

**RetryDelay**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Durée, en secondes, avant la nouvelle tentative d’actualisation de la zone à laquelle cet enregistrement appartient.

</dd> <dt>

**SerialNumber**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Numéro de série de l’enregistrement SOA.

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

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> <dt>

[**Modifier la méthode de la \_ classe SOAType MicrosoftDNS**](microsoftdns-soatype-modify.md)
</dt> </dl>

 

 





