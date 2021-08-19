---
title: Modifier la méthode de la classe MicrosoftDNS_AFSDBType
description: La méthode modify met à jour un enregistrement de ressource de serveur de base de données (AFSDB) Andrew File System.
ms.assetid: 9b98a3cf-cc2b-4497-921b-eaca4d13d6a1
keywords:
- Modifier la méthode DNS
- Modifier la méthode DNS, MicrosoftDNS_AFSDBType classe
- MicrosoftDNS_AFSDBType de la classe DNS, Modify, méthode
topic_type:
- apiref
api_name:
- MicrosoftDNS_AFSDBType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 385b80d853c3b610971803c0b1d80a81b7b7c2335186fe4585e63f60c3e3cca3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104059"
---
# <a name="modify-method-of-the-microsoftdns_afsdbtype-class"></a>Modifier la méthode de la \_ classe AFSDBType MicrosoftDNS

La méthode **Modify** met à jour un enregistrement de ressource de serveur de base de données (AFSDB) Andrew File System.

## <a name="syntax"></a>Syntaxe


```mof
void Modify(
  [in, optional] uint32                 TTL,
  [in, optional] uint16                 Subtype,
  [in, optional] string                 ServerName,
  [out, ref]     MicrosoftDNS_AFSDBType &RR
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*TTL* \[ dans, facultatif\]
</dt> <dd>

Durée, en secondes, pendant laquelle l’enregistrement de ressource peut être mis en cache par un programme de résolution DNS.

</dd> <dt>

*Sous-type* \[ dans, facultatif\]
</dt> <dd>

Sous-type du serveur AFS hôte. Pour le sous-type 1 (valeur = 1), l’hôte dispose d’un serveur d’emplacement de volume AFS version 3,0 pour la cellule AFS nommée. Dans le cas d’un sous-type 2 (valeur = 2), l’hôte dispose d’un serveur de noms authentifié contenant le nœud de répertoire racine de la cellule pour la cellule DCE/NCA nommée.

</dd> <dt>

*Nom du serveur* \[ dans, facultatif\]
</dt> <dd>

Nom de domaine complet spécifiant un hôte qui a un serveur pour la cellule AFS spécifiée dans le nom du propriétaire.

</dd> <dt>

*RR* \[ out, Ref\]
</dt> <dd>

Référence à l’objet modifié.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Tout paramètre non spécifié reste inchangé dans l’enregistrement modifié.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                              |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                   |
| Espace de noms<br/>                | \\MicrosoftDNS racine<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov. mof</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MicrosoftDNS \_ AFSDBType**](microsoftdns-afsdbtype.md)
</dt> <dt>

[**Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS AFSDBType**](microsoftdns-afsdbtype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





