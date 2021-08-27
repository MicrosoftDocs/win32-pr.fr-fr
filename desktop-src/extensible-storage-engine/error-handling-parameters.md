---
description: En savoir plus sur les paramètres de gestion des erreurs
title: Paramètres de gestion des erreurs
TOCTitle: Error Handling Parameters
ms:assetid: 014996a1-5674-40c7-9538-54cae1681fec
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269173(v=EXCHG.10)
ms:contentKeyID: 32765476
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7a0556d97a0dda0182ee4fe229599030f523accd
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474825"
---
# <a name="error-handling-parameters"></a>Paramètres de gestion des erreurs


_**S’applique à :** Windows | Windows Serveurs_

## <a name="error-handling-parameters"></a>Paramètres de gestion des erreurs

Cette rubrique contient des paramètres qui sont utilisés pour la gestion des erreurs.

*JET_paramErrorToString* 70  

Ce paramètre peut être utilisé pour convertir un [JET_ERR](./jet-err.md) en chaîne. Cette opération s’effectue à l’aide d’un appel spécial à [JetGetSystemParameter](./jetgetsystemparameter-function.md) où la mémoire tampon de sortie entière contient la valeur [JET_ERR](./jet-err.md) à convertir (en tant que paramètre d’entrée) et la mémoire tampon de sortie de chaîne retourne la chaîne d’erreur correspondante. La chaîne se présente comme suit : « JET_errSuccess, opération réussie ». La chaîne est composée du nom symbolique de la chaîne, d’une virgule, puis d’une description textuelle simple de l’erreur. La chaîne de description peut elle-même contenir des virgules. Si l’erreur n’est pas reconnue, la chaîne sera « erreur inconnue, erreur inconnue ».

**Remarque**  Ce paramètre est en lecture seule.


| | | <p>Valeur par défaut :</p> | <p>Spécial</p> | | <p>Tapez :</p> | <p>Spécial</p> | | <p>Plage valide :</p> | <p>Spécial</p> | | <p>Étendue :</p> | <p>Global</p> | | <p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>No</p> | | <p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>No</p> | | <p>Affecte la disposition physique :</p> | <p>No</p> | | <p>Affecte la fiabilité :</p> | <p>No</p> | | <p>Affecte les performances :</p> | <p>No</p> | | <p>Affecte les ressources :</p> | <p>No</p> | | <p>Disponibilité :</p> | <p>Tous</p> | 


*JET_paramExceptionAction*  
98  

Ce paramètre contrôle ce qui se produit lorsqu’une exception est levée par le moteur de base de données ou le code qui est appelé par le moteur de base de données. quand la valeur JET_ExceptionMsgBox, toute exception est levée dans le Windows filtre d’exception non géré. L’exception est alors gérée en tant qu’échec de l’application. L’objectif est d’empêcher le code d’application d’essayer à tort d’intercepter et d’ignorer une exception générée par le moteur de base de données. Cela ne peut pas être autorisé, car une base de données endommagée peut se produire. Si l’application souhaite gérer correctement ces exceptions, la protection peut être désactivée en définissant ce paramètre sur JET_ExceptionNone.


| | | <p>Valeur par défaut :</p> | <p>JET_ExceptionMsgBox</p> | | <p>Tapez :</p> | <p>Integer</p> | | <p>Plage valide :</p> | <p>JET_ExceptionMsgBox, JET_ExceptionNone</p> | | <p>Étendue :</p> | <p>Global</p> | | <p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p><strong>Windows 2000, Windows XP et Windows Server 2003 :</strong>  º</p><p><strong>Windows Vista :</strong>  Oui</p> | | <p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p><strong>Windows 2000, Windows XP et Windows Server 2003 :</strong>  º</p><p><strong>Windows Vista :</strong>  Oui</p> | | <p>Affecte la disposition physique :</p> | <p>No</p> | | <p>Affecte la fiabilité :</p> | <p>Yes</p> | | <p>Affecte les performances :</p> | <p>No</p> | | <p>Affecte les ressources :</p> | <p>No</p> | | <p>Disponibilité :</p> | <p>Tous</p> | 


### <a name="requirements"></a>Configuration requise


| | | <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | | <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 


### <a name="see-also"></a>Voir aussi

[Constantes de gestion des erreurs](./error-handling-constants.md)  
[Codes d’erreur du moteur de Stockage Extensible](./extensible-storage-engine-error-codes.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JET_ERR](./jet-err.md)  
[JetInit](./jetinit-function.md)
