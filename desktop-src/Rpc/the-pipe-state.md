---
title: État du canal
description: Sur le serveur, le compilateur MIDL crée une variable d’État qui coordonne les procédures push, pull et Alloc.
ms.assetid: 7cc59cb3-cf41-40f7-a28f-b896c319ae64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d12c5ef5549d89f3aee2833599f5930f2617478e66e16c3b78188eb63a40e7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118924069"
---
# <a name="the-pipe-state"></a>État du canal

Sur le serveur, le compilateur MIDL crée une variable d' *État* qui coordonne les procédures push, pull et Alloc. Côté client, le développeur doit créer la variable d' *État* . Par conséquent, la variable d' *État* est locale des deux côtés, c’est-à-dire que le client et le serveur conservent chacun leur propre état de canal. Le code stub du serveur conserve la variable d’État sur le serveur. Vous ne devez pas essayer de modifier directement son contenu. Le client doit initialiser les champs dans la structure de contrôle du canal et conserver sa variable d' *État* . Elle utilise la variable d' *État* pour identifier où localiser ou placer des données.

La variable d' *État* du client peut être aussi simple qu’un descripteur de fichier, si vous transférez des données d’un fichier vers un autre. Il peut également s’agir d’un entier qui pointe vers un élément d’un tableau. Vous pouvez aussi définir une structure d’État assez complexe pour effectuer des tâches supplémentaires, telles que la coordination des routines push et pull sur un \[ paramètre [in](/windows/desktop/Midl/in), [out](/windows/desktop/Midl/out-idl) \] .

 

 