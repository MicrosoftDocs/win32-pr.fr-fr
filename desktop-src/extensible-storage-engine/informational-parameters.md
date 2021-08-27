---
description: 'En savoir plus sur les paramètres suivants : informations'
title: Paramètres d’information
TOCTitle: Informational Parameters
ms:assetid: 48500fc9-6d89-45b8-92ad-afb997b729f3
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269241(v=EXCHG.10)
ms:contentKeyID: 32765543
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cd932f64956e1a00aae5925b97dbf6c35ecc2661
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987602"
---
# <a name="informational-parameters"></a>Paramètres d’information


_**S’applique à :** Windows | Windows Serveurs_

## <a name="informational-parameters"></a>Paramètres d’information

Cette rubrique contient des paramètres utilisés pour exposer des informations sur le moteur de base de données.

*JET_paramKeyMost*  
134  

Ce paramètre en lecture seule indique la longueur de clé d’index maximale autorisée qui peut être sélectionnée pour la taille de page de la base de données actuelle (telle que configurée par JET_paramDatabasePageSize).


| Étiquette | Valeur |
|--------|-------|
| <p>Valeur par défaut :</p> | <p>JET_cbKeyMost4KBytePage</p> | 
| <p>Tapez :</p> | <p>Entier</p> | 
| <p>Plage valide :</p> | <p>255 – 65535</p> | 
| <p>Étendue :</p> | <p>Global</p> | 
| <p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>N/A</p> | 
| <p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>N/A</p> | 
| <p>Affecte la disposition physique :</p> | <p>No</p> | 
| <p>Affecte la fiabilité :</p> | <p>No</p> | 
| <p>Affecte les performances :</p> | <p>No</p> | 
| <p>Affecte les ressources :</p> | <p>No</p> | 
| <p>Disponibilité :</p> | <p>à compter de Windows Server 2008 et Windows Vista</p> | 



*JET_paramMaxColtyp*  
131  

Ce paramètre en lecture seule retourne la [JET_COLTYP](./jet-coltyp.md) maximale (JET_coltypMax) pour cette version du moteur de base de données. Cette valeur peut être utilisée pour tester la prise en charge d’un [JET_COLTYP](./jet-coltyp.md)spécifique. Si un [JET_COLTYP](./jet-coltyp.md) donné est inférieur à la valeur de ce paramètre, il est pris en charge par le moteur de base de données.


| Étiquette | Valeur |
|--------|-------|
| <p>Valeur par défaut :</p> | <p>JET_coltypUnsignedShort + 1</p> | 
| <p>Tapez :</p> | <p>Entier</p> | 
| <p>Plage valide :</p> | <p>0 – 255</p> | 
| <p>Étendue :</p> | <p>Global</p> | 
| <p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>N/A</p> | 
| <p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>N/A</p> | 
| <p>Affecte la disposition physique :</p> | <p>No</p> | 
| <p>Affecte la fiabilité :</p> | <p>No</p> | 
| <p>Affecte les performances :</p> | <p>No</p> | 
| <p>Affecte les ressources :</p> | <p>No</p> | 
| <p>Disponibilité :</p> | <p>à compter de Windows Server 2008 et Windows Vista</p> | 



*JET_paramLVChunkSizeMost*  
163  

Paramètre en lecture seule qui retourne la taille de segment de valeur longue en fonction de la taille de page configurée. Si une valeur long doit être lue ou écrite avec plusieurs appels de colonne jet {set, Retrieve}, l’utilisation d’une mémoire tampon dont la taille est un multiple de la taille de segment est plus efficace.


| Étiquette | Valeur |
|--------|-------|
| <p>Valeur par défaut :</p> | <p>2 ko page = 1966 octets<br />4 ko page = 4014 octets<br />8 ko page = 8110 octets<br />16 ko page = 4050 octets<br />32KO page = 8150 octets</p> | 
| <p>Tapez :</p> | <p>Entier</p> | 
| <p>Plage valide :</p> | <p>0-10000</p> | 
| <p>Étendue :</p> | <p></p> | 
| <p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p></p> | 
| <p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p></p> | 
| <p>Affecte la disposition physique :</p> | <p></p> | 
| <p>Affecte la fiabilité :</p> | <p></p> | 
| <p>Affecte les performances :</p> | <p></p> | 
| <p>Affecte les ressources :</p> | <p></p> | 
| <p>Disponibilité :</p> | <p></p> | 



### <a name="requirements"></a>Configuration requise


| Condition requise | Valeur |
|------------|----------|
| <p><strong>Client</strong></p> | <p>requiert Windows Vista.</p> | 
| <p><strong>Serveur</strong></p> | <p>requiert Windows Server 2008.</p> | 
| <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 



### <a name="see-also"></a>Voir aussi

[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[JET_COLTYP](./jet-coltyp.md)
