---
description: 'En savoir plus sur : JET_ERR'
title: JET_ERR
TOCTitle: JET_ERR
ms:assetid: cd9cb876-251c-458d-a015-8e9045e77fc9
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294092(v=EXCHG.10)
ms:contentKeyID: 32765707
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
ms.openlocfilehash: f341f88a192fee6de55e0077778abde83493e35e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482275"
---
# <a name="jet_err"></a>JET_ERR


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jet_err"></a>JET_ERR

le type de données **JET_ERR** contient un [code d’erreur Extensible Stockage Engine](./extensible-storage-engine-error-codes.md).

```cpp
typedef long JET_ERR;
```

### <a name="data-types"></a>Types de données

JET_ERR

Une valeur zéro (correspondant à JET_errSuccess) indique que l’appel a réussi. Une valeur positive indique qu’une condition non irrécupérable s’est produite lors d’un appel de réussite. Une valeur négative indique que l’appel a échoué.

### <a name="remarks"></a>Remarques

pour plus d’informations sur le renvoi d’erreurs en tant que hresult, consultez [erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md). Pour plus d’informations sur les indicateurs permettant de configurer la base de données afin de gérer les erreurs, consultez [paramètres de gestion des erreurs](./error-handling-parameters.md).

### <a name="requirements"></a>Configuration requise


| | | <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | | <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 



### <a name="see-also"></a>Voir aussi

[erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md)  
[Codes d’erreur du moteur de Stockage Extensible](./extensible-storage-engine-error-codes.md)  
[Paramètres de gestion des erreurs](./error-handling-parameters.md)
