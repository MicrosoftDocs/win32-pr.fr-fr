---
description: En savoir plus sur les constantes de gestion des erreurs
title: Constantes de gestion des erreurs
TOCTitle: Error Handling Constants
ms:assetid: 5a1f9438-2d36-483e-9820-d0de30ee5e01
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269258(v=EXCHG.10)
ms:contentKeyID: 32765560
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
ms.openlocfilehash: 4480b54277c1586ca05d4a5db2ca6fdb9e045055
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987632"
---
# <a name="error-handling-constants"></a>Constantes de gestion des erreurs


_**S’applique à :** Windows | Windows Serveurs_

## <a name="error-handling-constants"></a>Constantes de gestion des erreurs

Les constantes suivantes sont utilisées pour définir la plage des paramètres du système de [JET_paramExceptionAction](./error-handling-parameters.md) .


| <p>Constante/valeur</p> | <p>Description</p> | 
|-----------------------|--------------------|
| <p>JET_ExceptionMsgBox<br />0x0001</p> | <p>Affiche une boîte de message lorsqu’une exception se produit.</p> | 
| <p>JET_ExceptionNone<br />0x0002</p> | <p>Ne fait rien quand une exception se produit.</p> | 



### <a name="requirements"></a>Configuration requise


| Condition requise | Valeur |
|------------|----------|
| <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | 
| <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 



### <a name="see-also"></a>Voir aussi

[Paramètres de gestion des erreurs](./error-handling-parameters.md)
