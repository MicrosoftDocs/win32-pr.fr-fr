---
description: 'En savoir plus sur : JET_SNT'
title: JET_SNT
TOCTitle: JET_SNT
ms:assetid: 74ac5142-8102-4dd3-8f2a-786a7a2ac78f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269294(v=EXCHG.10)
ms:contentKeyID: 32765586
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
ms.openlocfilehash: 250ad992ec26b218bab21691f26c0938b6be6921
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481385"
---
# <a name="jet_snt"></a>JET_SNT


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jet_snt"></a>JET_SNT

Le [JET_SNT]() groupe de constantes décrit les points de la progression d’une opération sur laquelle les informations sont demandées dans un appel à la fonction de rappel [JET_PFNSTATUS](./jet-pfnstatus-callback-function.md) .


| <p>Constante/valeur</p> | <p>Description</p> | 
|-----------------------|--------------------|
| <p>JET_sntBegin<br />5</p> | <p>Début d’une opération</p> | 
| <p>JET_sntRequirements<br />7</p> | <p>Non pris en charge.</p><p><strong>Windows serveur 2000 :</strong>  L’opération est démarrée. Dans ce cas, le dernier paramètre de la fonction de rappel doit être un pointeur valide vers une structure de <a href="gg269328(v=exchg.10).md">JET_SNPROG</a> qui indique le nombre total d’unités à exécuter.</p> | 
| <p>JET_sntProgress<br />0</p> | <p>Nombre d’unités terminées et nombre d’unités encore à effectuer. Ces informations sont retournées dans les membres d’une structure <a href="gg269328(v=exchg.10).md">JET_SNPROG</a> .</p> | 
| <p>JET_sntComplete<br />6</p> | <p>Achèvement d’une opération.</p> | 
| <p>JET_sntFail<br />3</p> | <p>L’échec d’une opération.</p> | 
| <p>JET_sntRecoveryStep<br />8</p> | <p>Contrôle de récupération d’une opération.</p><div class="alert">&gt; [!NOTE]&gt; <P>cette valeur ne s’applique pas aux versions du système d’exploitation Windows à partir de Windows 8.</P></div> | 



### <a name="requirements"></a>Configuration requise


| | | <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | | <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 



### <a name="see-also"></a>Voir aussi

[JET_PFNSTATUS](./jet-pfnstatus-callback-function.md)  
[JET_SNP](./jet-snp.md)  
[JET_SNPROG](./jet-snprog-structure.md)
