---
title: Erreurs d’allocation de mémoire tampon RPC
description: Étant donné que la bibliothèque Runtime RPC alloue de la mémoire pour les mémoires tampons d’envoi et de réception, la fonction doit s’attendre à des erreurs d’allocation RPC.
ms.assetid: be9105df-1183-48d6-8cea-391ca628c8b7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d68c484837f1f03bce8a8175ddb343065051e3695eec7c65d8a9de89c15fb5d1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119745009"
---
# <a name="rpc-buffer-allocation-errors"></a>Erreurs d’allocation de mémoire tampon RPC

Étant donné que la bibliothèque Runtime RPC alloue de la mémoire pour les mémoires tampons d’envoi et de réception, la fonction doit s’attendre à des erreurs d’allocation RPC. Dans le cas d’une erreur d’allocation RPC, un descripteur pouvant être repris est invalidé. Il s’agit d’une exigence, car les fonctions pouvant être reprises ne peuvent pas être rembobinées.

 

 




