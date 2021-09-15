---
description: 'En savoir plus sur : constantes de handle non valides'
title: Constantes de handle non valides
TOCTitle: Invalid Handle Constants
ms:assetid: 594d7804-725f-4f72-b5f0-56f099c1c17b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269256(v=EXCHG.10)
ms:contentKeyID: 32765558
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
ms.openlocfilehash: 370cc254f001f6595cd4b4297ee002706947774c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127517860"
---
# <a name="invalid-handle-constants"></a>Constantes de handle non valides


_**S’applique à :** Windows | Windows Serveurs_

## <a name="invalid-handle-constants"></a>Constantes de handle non valides

Les constantes suivantes indiquent des handles non valides pour différents aspects de ESE.


| <p>Constante/valeur</p> | <p>Description</p> | 
|-----------------------|--------------------|
| <p>JET_instanceNil<br />(~ (JET_INSTANCE) 0)</p> | <p>Handle non valide pour une instance de base de données.<br /><strong>Windows XP :</strong> introduite dans Windows XP.</p> | 
| <p>JET_sesidNil<br />(~ (JET_SESID) 0)</p> | <p>Handle non valide pour un ID de session.</p> | 
| <p>JET_tableidNil<br />(~ (JET_TABLEID) 0)</p> | <p>Handle non valide pour un ID de table.</p> | 
| <p>JET_bitNil<br />((JET_GRBIT) 0)</p> | <p>Handle non valide pour un groupe de bits.</p> | 
| <p>JET_LSNil<br />(~ (JET_LS) 0)</p> | <p>handle non valide pour l’Stockage Local.</p> | 
| <p>JET_dbidNil<br />((JET_DBID) 0xFFFFFFFF)</p> | <p>Handle non valide pour l’ID de base de données.</p> | 



### <a name="requirements"></a>Configuration requise


| Condition requise | Valeur |
|------------|----------|
| <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | 
| <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 


