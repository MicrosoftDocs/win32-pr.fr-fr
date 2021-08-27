---
description: En savoir plus sur les constantes de journalisation des événements
title: Constantes de journalisation des événements
TOCTitle: Event Logging Constants
ms:assetid: d24603a9-a9be-4700-bc20-4e3f0661e741
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294101(v=EXCHG.10)
ms:contentKeyID: 32765716
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
ms.openlocfilehash: fa04ffe87ca25be127919c705ea5c7d6c3411485
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987040"
---
# <a name="event-logging-constants"></a>Constantes de journalisation des événements


_**S’applique à :** Windows | Windows Serveurs_

## <a name="event-logging-constants"></a>Constantes de journalisation des événements

Les constantes suivantes indiquent le niveau de détail des messages du journal des événements pour le paramètre système [JET_ParamEventLoggingLevel](./event-log-parameters.md) .


| <p>Constante/valeur</p> | <p>Description</p> | 
|-----------------------|--------------------|
| <p>JET_EventLoggingDisable<br />0</p> | <p>Désactive la journalisation des événements.</p> | 
| <p>JET_EventLoggingLevelMax<br />100</p> | <p>Définit le niveau maximal à utiliser pour les journaux des événements, qui est actuellement de 100 caractères.</p> | 



### <a name="requirements"></a>Configuration requise


| Condition requise | Valeur |
|------------|----------|
| <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | 
| <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 



### <a name="see-also"></a>Voir aussi

[Paramètres du journal des événements](./event-log-parameters.md)
