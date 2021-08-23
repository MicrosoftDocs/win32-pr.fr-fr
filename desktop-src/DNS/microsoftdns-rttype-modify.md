---
title: Modifier la méthode de la classe MicrosoftDNS_RTType
description: La méthode modify met à jour un enregistrement de ressource route through (RT).
ms.assetid: 80053ae6-8ce8-4aa1-be2b-aac9daa5dae3
keywords:
- Modifier la méthode DNS
- Modifier la méthode DNS, MicrosoftDNS_RTType classe
- MicrosoftDNS_RTType de la classe DNS, Modify, méthode
topic_type:
- apiref
api_name:
- MicrosoftDNS_RTType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2003f8e2840a2684f91a7a01b0341e2e8dcdf0ca88b6bf31fcf58b3a3c6f79bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692399"
---
# <a name="modify-method-of-the-microsoftdns_rttype-class"></a>Modifier la méthode de la \_ classe RTType MicrosoftDNS

La méthode **Modify** met à jour un enregistrement de ressource route through (RT).

## <a name="syntax"></a>Syntaxe


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in, optional] uint16              Preference,
  [in, optional] string              IntermediateHost,
  [out, ref]     MicrosoftDNS_RTType &RR
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*TTL* \[ dans, facultatif\]
</dt> <dd>

Durée, en secondes, pendant laquelle l’enregistrement de ressource peut être mis en cache par un programme de résolution DNS.

</dd> <dt>

*Préférence* \[ dans, facultatif\]
</dt> <dd>

Préférence donnée à ce RR, parmi d’autres au même propriétaire. Les valeurs les plus basses sont préférées.

</dd> <dt>

*IntermediateHost* \[ dans, facultatif\]
</dt> <dd>

Nom de domaine complet spécifiant un hôte qui servira de intermédiaire pour atteindre l’hôte spécifié par le propriétaire.

</dd> <dt>

*RR* \[ out, Ref\]
</dt> <dd>

Référence au nouvel objet.

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

[**MicrosoftDNS \_ RTType**](microsoftdns-rttype.md)
</dt> <dt>

[**Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS RTType**](microsoftdns-rttype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





