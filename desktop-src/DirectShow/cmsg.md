---
description: La classe CMsgThread fournit la prise en charge d’un thread de travail auquel les demandes peuvent être publiées de manière asynchrone au lieu d’être envoyées directement.
ms.assetid: 1cf159c9-80d0-4e3b-88d8-2ba4cd18e768
title: CMsg, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsg
api_type:
- COM
api_location: ''
ms.openlocfilehash: a57a841b9c36a21895099c931acbf18a1e01ea0f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106514089"
---
# <a name="cmsg-class"></a>CMsg, classe

La classe [**CMsgThread**](cmsgthread.md) fournit la prise en charge d’un thread de travail auquel les demandes peuvent être publiées de manière asynchrone au lieu d’être envoyées directement. La classe [**CAMThread**](camthread.md) fournit un thread de travail auquel les demandes uniques peuvent être envoyées. Un seul client peut effectuer une demande à la fois et le client se bloque jusqu’à ce que le thread de travail ait terminé la demande. En revanche, la classe **CMsgThread** fournit un thread de travail sur lequel n’importe quel nombre de demandes peut être publié. Les requêtes (sous la forme d’un `CMsg` objet) sont mises en file d’attente et exécutées dans l’ordre, de manière asynchrone. Aucune réponse ou valeur de retour n’est reçue.



| Données membres              | Description                                                                                                                                                                       |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| dwFlags                   | Paramètre d’indicateur pour le code de la requête.                                                                                                                                               |
| lpParam                   | Données requises par le thread de travail comme valeurs de paramètre ou de retour. Ces données ne doivent pas être basées sur la pile, car elles seront référencées un peu plus tard après la fin de l’opération de mise en file d’attente. |
| pEvent                    | Objet d’événement qu’un thread de travail peut signaler pour indiquer l’achèvement de l’opération.                                                                                         |
| uMsg                      | Code de requête défini par le client de la classe thread et compris par la fonction de thread de travail remplacée.                                                           |
| Fonctions de membre          | Description                                                                                                                                                                       |
| [**CMsg**](cmsg-cmsg.md) | Construit un objet [**CMsg**](cmsg-cmsg.md) .                                                                                                                                    |



 

 

 



