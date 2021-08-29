---
title: Modifier la méthode de la classe MicrosoftDNS_MFType
description: La méthode modify met à jour un enregistrement de ressource de l’agent de transfert de messagerie pour le domaine (MF).
ms.assetid: b4bc43a5-6f43-487d-ad6c-3e01d5b2b6b8
keywords:
- Modifier la méthode DNS
- Modifier la méthode DNS, MicrosoftDNS_MFType classe
- MicrosoftDNS_MFType de la classe DNS, Modify, méthode
topic_type:
- apiref
api_name:
- MicrosoftDNS_MFType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa387e067678299c14f3925299d1bdb658ec010458f81ecac3727bf8bf9aa3c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874919"
---
# <a name="modify-method-of-the-microsoftdns_mftype-class"></a>Modifier la méthode de la \_ classe MFType MicrosoftDNS

La méthode **Modify** met à jour un enregistrement de ressource de l’agent de transfert de messagerie pour le domaine (MF).

## <a name="syntax"></a>Syntaxe


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in, optional] string              MFHost,
  [out, ref]     MicrosoftDNS_MFType &RR
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*TTL* \[ dans, facultatif\]
</dt> <dd>

Durée, en secondes, pendant laquelle l’enregistrement de ressource peut être mis en cache par un programme de résolution DNS.

</dd> <dt>

*MFHost* \[ dans, facultatif\]
</dt> <dd>

Nom de l’hôte qui fournit l’agent de transfert du courrier.

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

[**MicrosoftDNS \_ MFType**](microsoftdns-mftype.md)
</dt> <dt>

[**Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS MFType**](microsoftdns-mftype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





