---
description: 'En savoir plus sur : JET_SNP'
title: JET_SNP
TOCTitle: JET_SNP
ms:assetid: 7f3d1cc5-7b27-454d-8dd1-584ab4b60ab0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269311(v=EXCHG.10)
ms:contentKeyID: 32765601
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
ms.openlocfilehash: ee83dc86aa6faf5fab0b45596a586c657e4c6e2a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474125"
---
# <a name="jet_snp"></a>JET_SNP


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jet_snp"></a>JET_SNP

Le **JET_SNP** groupe de constantes décrit le type de l’opération pour laquelle des informations de progression doivent être obtenues. Ces constantes sont utilisées comme paramètre *SNP* de la fonction de rappel [JET_PFNSTATUS](./jet-pfnstatus-callback-function.md) .


| <p>Constante/valeur</p> | <p>Description</p> | 
|-----------------------|--------------------|
| <p>JET_snpRepair<br />2</p> | <p>Le rappel est destiné à une opération de réparation.</p> | 
| <p>JET_snpCompact<br />4</p> | <p>Le rappel est destiné à la défragmentation de la base de données.</p> | 
| <p>JET_snpRestore<br />8</p> | <p>Le rappel est destiné à une opération de restauration.</p> | 
| <p>JET_snpBackup<br />9</p> | <p>Le rappel est destiné à une opération de sauvegarde.</p> | 
| <p>JET_snpUpgrade<br />10</p> | <p>Non pris en charge.</p><p><strong>Windows 2000 :</strong>  Le rappel est destiné à l’opération de mise à niveau du format de base de données.</p> | 
| <p>JET_snpScrub<br />11</p> | <p>Le rappel est destiné à une opération de mise à zéro de base de données (c’est-à-dire de nettoyage).</p><p><strong>Windows server 2003 et Windows 2000 server :</strong>  Non pris en charge.</p> | 
| <p>JET_snpUpgradeRecordFormat<br />12</p> | <p>Le rappel est destiné au processus de mise à niveau du format d’enregistrement de toutes les pages de la base de données.</p><p><strong>Windows server 2003 et Windows 2000 server :</strong>  Non pris en charge.</p> | 



### <a name="requirements"></a>Configuration requise


| | | <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | | <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 



### <a name="see-also"></a>Voir aussi

[JET_PFNSTATUS](./jet-pfnstatus-callback-function.md)  
[JET_SNPROG](./jet-snprog-structure.md)  
[JET_SNT](./jet-snt.md)
