---
title: État du canal
description: Sur le serveur, le compilateur MIDL crée une variable d’État qui coordonne les procédures push, pull et Alloc.
ms.assetid: 7cc59cb3-cf41-40f7-a28f-b896c319ae64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6d7ec8af1907c98b7cf2098f4979dac62ef573a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127311425"
---
# <a name="the-pipe-state"></a>État du canal

Sur le serveur, le compilateur MIDL crée une variable d' *État* qui coordonne les procédures push, pull et Alloc. Côté client, le développeur doit créer la variable d' *État* . Par conséquent, la variable d' *État* est locale des deux côtés, c’est-à-dire que le client et le serveur conservent chacun leur propre état de canal. Le code stub du serveur conserve la variable d’État sur le serveur. Vous ne devez pas essayer de modifier directement son contenu. Le client doit initialiser les champs dans la structure de contrôle du canal et conserver sa variable d' *État* . Elle utilise la variable d' *État* pour identifier où localiser ou placer des données.

La variable d' *État* du client peut être aussi simple qu’un descripteur de fichier, si vous transférez des données d’un fichier vers un autre. Il peut également s’agir d’un entier qui pointe vers un élément d’un tableau. Vous pouvez aussi définir une structure d’État assez complexe pour effectuer des tâches supplémentaires, telles que la coordination des routines push et pull sur un \[ paramètre [in](/windows/desktop/Midl/in), [out](/windows/desktop/Midl/out-idl) \] .

 

 