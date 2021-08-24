---
title: Classe MicrosoftDNS_AFSDBType
description: Sous-classe de MicrosoftDNS \_ ResourceRecord qui représente un enregistrement de serveur de base de données du système de fichiers Andrew (AFSDB).
ms.assetid: 536f4df7-bd01-458b-b8f1-36f066e9ca04
keywords:
- MicrosoftDNS_AFSDBType de la classe DNS
- MicrosoftDNS_AFSDBType de la classe DNS, Description
topic_type:
- apiref
api_name:
- MicrosoftDNS_AFSDBType
- MicrosoftDNS_AFSDBType.CreateInstanceFromPropertyData
- MicrosoftDNS_AFSDBType.Modify
- MicrosoftDNS_AFSDBType.Subtype
- MicrosoftDNS_AFSDBType.ServerName
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74c7887d51e58b8c34374ed5ca96d0206472155872ba573b7b9f8879329910f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119815699"
---
# <a name="microsoftdns_afsdbtype-class"></a>MicrosoftDNS \_ AFSDBType, classe

Sous-classe de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) qui représente un enregistrement de serveur de base de données du système de fichiers Andrew (AFSDB).

La syntaxe suivante est simplifiée à partir du code MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
class MicrosoftDNS_AFSDBType : MicrosoftDNS_ResourceRecord
{
  uint16 Subtype;
  string ServerName;
};
```

## <a name="members"></a>Membres

La classe **MicrosoftDNS \_ AFSDBType** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La classe **MicrosoftDNS \_ AFSDBType** possède ces méthodes.



| Méthode                             | Description                                                                                                                                                                                                                                                                                                                                                   |
|:-----------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | Instancie un enregistrement de ressource AFSDB en fonction des données des paramètres d’entrée de la méthode : le nom du serveur DNS, le nom du conteneur, le nom du propriétaire/de la cellule, la classe (valeur par défaut = IN), la valeur de durée de vie et le sous-type et le nom du serveur AFS hôte. Retourne une référence au nouvel objet sous la forme d’un paramètre de sortie. <br/> Qualificateurs : implémentés, statiques<br/> |
| **Modify**                         | Cette méthode met à jour la durée de vie, le sous-type et le nom de serveur avec les valeurs spécifiées comme paramètres d’entrée de cette méthode. Si une nouvelle valeur n’est pas spécifiée pour un paramètre, la valeur actuelle du paramètre n’est pas modifiée. La méthode retourne une référence à l’objet modifié sous la forme d’un paramètre de sortie. <br/> Qualificateurs : implémentés<br/>   |



 

### <a name="properties"></a>Propriétés

La classe **MicrosoftDNS \_ AFSDBType** a ces propriétés.

<dl> <dt>

**ServerName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom de domaine complet spécifiant un hôte qui a un serveur pour la cellule AFS spécifiée dans le nom du propriétaire.

</dd> <dt>

**Sous-type**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Sous-type du serveur AFS hôte. Pour le sous-type 1 (valeur = 1), l’hôte dispose d’un serveur d’emplacement de volume AFS version 3,0 pour la cellule AFS nommée. Dans le cas d’un sous-type 2 (valeur = 2), l’hôte dispose d’un serveur de noms authentifié contenant le nœud de répertoire racine de la cellule pour la cellule DCE/NCA nommée.

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

[**Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS AFSDBType**](microsoftdns-afsdbtype-createinstancefrompropertydata.md)
</dt> <dt>

[**Modifier la méthode de la \_ classe AFSDBType MicrosoftDNS**](microsoftdns-afsdbtype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





