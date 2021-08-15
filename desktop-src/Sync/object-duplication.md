---
description: La fonction DuplicateHandle crée un handle dupliqué qui peut être utilisé par un autre processus spécifié.
ms.assetid: b79d2b8f-931e-4cab-9bbe-9ead1b102132
title: Duplication d’objets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0927f9d3b60f358623e66a067e75992e71c76ca5fe072a9749c9bbc217bfa2ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118886339"
---
# <a name="object-duplication"></a>Duplication d’objets

La fonction [**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) crée un handle dupliqué qui peut être utilisé par un autre processus spécifié. Cette méthode de partage des handles d’objets est plus complexe que l’utilisation d’objets nommés ou de l’héritage. Elle nécessite une communication entre le processus de création et le processus dans lequel le descripteur est dupliqué. Les informations nécessaires (valeur de handle et identificateur de processus) peuvent être communiquées par les méthodes de communication interprocessus, telles que les canaux nommés ou la mémoire partagée nommée.

 

 
