---
description: Fonctions NTFS (TxF) transactionnelles.
ms.assetid: fb6be33c-9d6c-48b2-a4da-31c60af8d972
title: Fonctions TxF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b59fa3c9a1323ce77c97ee36390190ea6301d71d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009814"
---
# <a name="txf-functions"></a>Fonctions TxF

NTFS transactionnel (TxF) fournit les fonctions suivantes.

## <a name="in-this-section"></a>Dans cette section



| Fonction                                                                      | Description                                                                                                                  |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [**TxfLogCreateFileReadContext**](/windows/desktop/api/TxfW32/nf-txfw32-txflogcreatefilereadcontext)<br/> | Crée un contexte à utiliser pour lire les enregistrements de réplication.<br/>                                                         |
| [**TxfLogDestroyReadContext**](/windows/desktop/api/TxfW32/nf-txfw32-txflogdestroyreadcontext)<br/>       | Ferme un contexte de lecture créé par la fonction [**TxfLogCreateFileReadContext**](/windows/desktop/api/TxfW32/nf-txfw32-txflogcreatefilereadcontext) .<br/> |
| [**TxfLogReadRecords**](/windows/desktop/api/TxfW32/nf-txfw32-txflogreadrecords)<br/>                     | Lit les enregistrements de restauration par progression dans le journal.<br/>                                                                              |



 

 

 




