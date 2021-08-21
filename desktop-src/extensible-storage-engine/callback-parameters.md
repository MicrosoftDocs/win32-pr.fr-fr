---
description: 'En savoir plus sur : paramètres de rappel'
title: Paramètres de rappel
TOCTitle: Callback Parameters
ms:assetid: 7f3cdc13-ffbd-4e5a-b650-1c6388e784dc
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269310(v=EXCHG.10)
ms:contentKeyID: 32765600
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
ms.openlocfilehash: a7b904c090852ea3990ac78e37a7ca851e152968
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465216"
---
# <a name="callback-parameters"></a>Paramètres de rappel


_**S’applique à :** Windows | Windows Serveurs_

## <a name="callback-parameters"></a>Paramètres de rappel

Cette rubrique contient des paramètres qui sont utilisés pour les rappels.

*JET_paramDisableCallbacks*  
65  

Ce paramètre désactive tous les rappels du moteur de base de données pour les fonctions fournies par l’application. Elle est principalement destinée à prendre en charge les utilitaires du moteur de base de données et n’est pas destinée à être utilisée dans votre application.


| | | <p>Valeur par défaut :</p> | <p>Faux</p> | | <p>Tapez :</p> | <p>Boolean</p> | | <p>Plage valide :</p> | <p>False, True</p> | | <p>Étendue :</p> | <p>Instance</p> | | <p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Yes</p> | | <p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>No</p> | | <p>Affecte la disposition physique :</p> | <p>No</p> | | <p>Affecte la fiabilité :</p> | <p>No</p> | | <p>Affecte les performances :</p> | <p>No</p> | | <p>Affecte les ressources :</p> | <p>No</p> | | <p>Disponibilité :</p> | <p>Windows XP et versions ultérieures</p> | 



*JET_paramEnablePersistedCallbacks*  
156  

Ce paramètre permet l’utilisation de rappels persistants dans la base de données. dans les versions antérieures à Windows Vista, l’utilisation de rappels persistants était activée par défaut. Les applications doivent maintenant activer explicitement l’utilisation de rappels persistants au moment de l’exécution à l’aide de ce paramètre. Si ce paramètre n’est pas défini, toute opération de base de données qui requiert l’appel d’un rappel échouera avec JET_errCallbackFailed. Ce paramètre n’affecte pas les rappels spécifiés au moment de l’exécution avec les mécanismes suivants : JET_paramRuntimeCallback, [JetRegisterCallback](./jetregistercallback-function.md)ou un paramètre de rappel explicite à une API jet. Il est toujours possible de créer des éléments de schéma qui contiennent des rappels persistants, même si l’utilisation de ces rappels persistants est interdite. Quand ce paramètre est défini sur false, il remplace JET_paramDisableCallbacks.


| | | <p>Valeur par défaut :</p> | <p>Faux</p> | | <p>Tapez :</p> | <p>Boolean</p> | | <p>Plage valide :</p> | <p>False, True</p> | | <p>Étendue :</p> | <p>Instance</p> | | <p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Yes</p> | | <p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>No</p> | | <p>Affecte la disposition physique :</p> | <p>No</p> | | <p>Affecte la fiabilité :</p> | <p>No</p> | | <p>Affecte les performances :</p> | <p>No</p> | | <p>Affecte les ressources :</p> | <p>No</p> | | <p>Disponibilité :</p> | <p>Windows Versions Vista et ultérieures</p> | 



*JET_paramRuntimeCallback*  
73  

Ce paramètre configure le moteur à l’aide d’une fonction de rappel d’exécution qui implémente l’interface [JET_CALLBACK](./jet-callback-callback-function.md) . Ce rappel peut être appelé pour les raisons suivantes : [JET_cbtypFreeCursorLS](./jet-cbtyp.md), [JET_cbtypFreeTableLS](./jet-cbtyp.md)ou [JET_cbtypNull](./jet-cbtyp.md). Pour plus d’informations, consultez [JetSetLS](./jetsetls-function.md) .


| | | <p>Valeur par défaut :</p> | <p>NULL</p> | | <p>Tapez :</p> | <p>Pointeur de fonction (JET_API_PTR)</p> | | <p>Plage valide :</p> | <p>NULL, <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>*</p> | | <p>Étendue :</p> | <p>Instance</p> | | <p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Yes</p> | | <p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>No</p> | | <p>Affecte la disposition physique :</p> | <p>No</p> | | <p>Affecte la fiabilité :</p> | <p>No</p> | | <p>Affecte les performances :</p> | <p>No</p> | | <p>Affecte les ressources :</p> | <p>No</p> | | <p>Disponibilité :</p> | <p>Windows XP et versions ultérieures</p> | 



### <a name="requirements"></a>Configuration requise


| | | <p><strong>Client</strong></p> | <p>requiert Windows Vista ou Windows XP.</p> | | <p><strong>Serveur</strong></p> | <p>requiert Windows server 2008 ou Windows server 2003.</p> | | <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 



### <a name="see-also"></a>Voir aussi

[JET_API_PTR](./jet-api-ptr.md)  
[JET_CALLBACK](./jet-callback-callback-function.md)  
[JET_CBTYP](./jet-cbtyp.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[JetSetLS](./jetsetls-function.md)
