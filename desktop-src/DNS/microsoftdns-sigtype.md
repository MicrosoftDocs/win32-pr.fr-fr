---
title: Classe MicrosoftDNS_SIGType
description: Sous-classe de MicrosoftDNS \_ ResourceRecord qui représente un enregistrement de ressource de signature (SIG).
ms.assetid: ef3729ad-448b-449e-ae59-34888925128a
keywords:
- MicrosoftDNS_SIGType de la classe DNS
- MicrosoftDNS_SIGType de la classe DNS, Description
topic_type:
- apiref
api_name:
- MicrosoftDNS_SIGType
- MicrosoftDNS_SIGType.CreateInstanceFromPropertyData
- MicrosoftDNS_SIGType.Modify
- MicrosoftDNS_SIGType.TypeCovered
- MicrosoftDNS_SIGType.Algorithm
- MicrosoftDNS_SIGType.Labels
- MicrosoftDNS_SIGType.OriginalTTL
- MicrosoftDNS_SIGType.SignatureExpiration
- MicrosoftDNS_SIGType.SignatureInception
- MicrosoftDNS_SIGType.KeyTag
- MicrosoftDNS_SIGType.SignerName
- MicrosoftDNS_SIGType.Signature
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e17009bf6458bd51b1d7a41b31f33ad0695e0da1a41c77aa72f56ee01573a529
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118163170"
---
# <a name="microsoftdns_sigtype-class"></a>MicrosoftDNS \_ SIGType, classe

Sous-classe de [**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md) qui représente un enregistrement de ressource de signature (SIG).

La syntaxe suivante est simplifiée à partir du code MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
class MicrosoftDNS_SIGType : MicrosoftDNS_ResourceRecord
{
  uint16 TypeCovered;
  uint16 Algorithm;
  uint16 Labels;
  uint32 OriginalTTL;
  uint32 SignatureExpiration;
  uint32 SignatureInception;
  uint16 KeyTag;
  string SignerName;
  string Signature;
};
```

## <a name="members"></a>Membres

La classe **MicrosoftDNS \_ SIGType** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La classe **MicrosoftDNS \_ SIGType** possède ces méthodes.



| Méthode                             | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|:-----------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | Instancie un RR SIG basé sur les données des paramètres d’entrée de la méthode : le nom du serveur DNS de l’enregistrement, le nom du conteneur, le nom du propriétaire, la classe (valeur par défaut = IN), la valeur de durée de vie et l’indicateur de mappage WINS, le délai de recherche inverse, le délai d’expiration du cache WINS et le nom de domaine à ajouter Elle retourne une référence au nouvel objet sous la forme d’un paramètre de sortie. <br/> Qualificateurs : implémentés, statiques<br/>                                                                                                                                                                                                                                                       |
| **Modify**                         | Met à jour la durée de vie, l’indicateur de mappage, le délai d’attente de recherche, le délai d’attente du cache et le domaine de résultat sur les valeurs spécifiées comme paramètres d’entrée de cette méthode. Si une nouvelle valeur n’est pas spécifiée pour un paramètre, la valeur actuelle du paramètre n’est pas modifiée. La méthode retourne une référence à l’objet modifié sous la forme d’un paramètre de sortie. <br/> Qualificateurs : implémentés<br/> **Windows Server 2003 :** Cette méthode met également à jour l’TypeCovered, l’algorithme, les étiquettes, OriginalTTL, SignatureExpiration, SignatureInception, KeyTag, SignerName et la signature avec les valeurs spécifiées comme paramètres d’entrée de cette méthode.<br/> <br/> |



 

### <a name="properties"></a>Propriétés

La classe **MicrosoftDNS \_ SIGType** a ces propriétés.

<dl> <dt>

**Algorithme**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Algorithme utilisé avec la clé spécifiée dans l’enregistrement de ressource. Les valeurs affectées sont indiquées dans le tableau suivant.



| Valeur                                                                                                | Signification                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | RSA/MD5 (RFC 2537)<br/>          |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Diffie-Hellman (RFC 2539)<br/>   |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | DSA (RFC 2536)<br/>              |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | Chiffrement à courbe elliptique<br/> |



 

</dd> <dt>

**KeyTag**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Méthode utilisée pour choisir une clé qui vérifie un SIG. Consultez RFC 2535, annexe C, pour connaître la méthode utilisée pour calculer un KeyTag.

</dd> <dt>

**Étiquettes**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nombre non signé d’étiquettes dans le nom du propriétaire du RR SIG d’origine. Le nombre n’inclut pas l’étiquette NULL pour la racine, ni les caractères génériques initiaux.

</dd> <dt>

**OriginalTTL**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

TTL de l’ensemble de RR signé par SIG.

</dd> <dt>

**Signature**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Signature, représentée dans la base 64, mise en forme comme défini dans la RFC 2535, annexe A.

</dd> <dt>

**SignatureExpiration**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Date d’expiration de la signature, exprimée en secondes depuis le 1er janvier 1970, heure de Greenwich (GMT), à l’exception des secondes bissextiles.

</dd> <dt>

**SignatureInception**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Date et heure auxquelles la signature devient valide, exprimée en secondes depuis le 1er janvier 1970, heure de Greenwich (GMT), à l’exception des secondes bissextiles.

</dd> <dt>

**SignerName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom de domaine du signataire qui a généré le RR SIG.

</dd> <dt>

**TypeCovered**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Type d’enregistrement de ressource couvert par ce SIG.

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

[**Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS SIGType**](microsoftdns-sigtype-createinstancefrompropertydata.md)
</dt> <dt>

[**Modifier la méthode de la \_ classe SIGType MicrosoftDNS**](microsoftdns-sigtype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





