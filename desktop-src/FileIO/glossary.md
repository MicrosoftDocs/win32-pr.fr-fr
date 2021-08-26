---
description: Terminologie utilisée pour décrire le NTFS transactionnel (TxF).
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 44cb060c-e6a6-48d6-bbcf-d8dc1ae8ceb2
title: Glossaire TxF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06e6e296319dc1a9ccd02834fe6144c28d15d61a0fe0c1ec449a07d81f96dbe2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119900649"
---
# <a name="txf-glossary"></a>Glossaire TxF

<dl> <dt>

<span id="fs.availability"></span><span id="FS.AVAILABILITY"></span>**sa**
</dt> <dd>

La disponibilité signifie qu’un gestionnaire de ressources va abandonner les transactions même si cela rompt la cohérence afin que le système puisse continuer à effectuer de nouvelles tâches. Le gestionnaire de ressources par défaut force la disponibilité sur le volume système. Par exemple, si le journal des transactions est plein, l’espace du journal des transactions ne peut pas être ajouté, et une transaction plus ancienne qui serait abandonnée nécessite la remise d’un résultat à partir d’un gestionnaire de ressources supérieur pour qu’une transaction distribuée se termine, le gestionnaire de ressources n’attend pas le gestionnaire de transactions supérieur et abandonne cette transaction, même si cela peut entraîner une

</dd> <dt>

<span id="fs.consistency"></span><span id="FS.CONSISTENCY"></span>**cohérence**
</dt> <dd>

La cohérence signifie qu’un gestionnaire de ressources va faire échouer de nouvelles transactions s’il ne peut pas avancer. Par exemple, si le journal des transactions est plein, l’espace du journal des transactions ne peut pas être ajouté, et une transaction plus ancienne qui serait abandonnée nécessite la remise d’un résultat à partir d’un gestionnaire de ressources supérieur afin qu’une transaction distribuée se termine, le gestionnaire de ressources attendra ce résultat.

</dd> <dt>

<span id="fs.miniversion"></span><span id="FS.MINIVERSION"></span>**miniversion**
</dt> <dd>

Un miniversion est une version d’un fichier qu’un rédacteur transactionnel crée pendant une transaction. Le miniversion peut être ouvert ultérieurement dans la transaction avec un accès en lecture seule.

</dd> <dt>

<span id="fs.transacted_reader"></span><span id="FS.TRANSACTED_READER"></span>**lecteur transactionnel**
</dt> <dd>

Un lecteur transactionnel est un descripteur de fichier transactionnel ouvert avec une autorisation qui fait partie de l’accès en lecture générique, mais qui ne fait pas partie d’un accès en écriture générique.

</dd> <dt>

<span id="fs.transacted_writer"></span><span id="FS.TRANSACTED_WRITER"></span>**rédacteur transactionnel**
</dt> <dd>

Un rédacteur transactionnel est un descripteur de fichier transactionnel ouvert avec une autorisation qui ne fait pas partie d’un accès en lecture générique, mais qui fait partie d’un accès en écriture générique.

</dd> </dl>

 

 



