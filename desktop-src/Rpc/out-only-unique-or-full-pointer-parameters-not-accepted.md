---
title: Out-Only paramètres de pointeur unique ou complet non acceptés
description: Les pointeurs uniques ou complets qui ne sont pas acceptés par le compilateur MIDL ne sont pas acceptés. De telles spécifications provoquent la génération d’un message d’erreur par le compilateur MIDL.
ms.assetid: 0477980e-d76e-452f-9ab1-71a8ed8642d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b9511c21045892eb7a5b3230d8f0180578b489b06b5b5402fb0b11f6a3ff31a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118927568"
---
# <a name="out-only-unique-or-full-pointer-parameters-not-accepted"></a>Out-Only paramètres de pointeur unique ou complet non acceptés

Les pointeurs uniques ou complets qui sont en \[ [dehors](/windows/desktop/Midl/out-idl) \] de ne sont pas acceptés par le compilateur MIDL. De telles spécifications provoquent la génération d’un message d’erreur par le compilateur MIDL.

Le stub serveur généré automatiquement doit allouer de la mémoire pour le référent du pointeur afin que l’application serveur puisse stocker des données dans cette zone mémoire. En fonction de la définition d’un paramètre en **\[ sortie \]** seule, aucune information sur le paramètre n’est transmise du client au serveur. Dans le cas d’un pointeur unique, qui peut prendre la valeur null, le stub du serveur ne dispose pas de suffisamment d’informations pour dupliquer correctement le pointeur unique dans l’espace d’adressage du serveur, et le stub ne peut pas non plus indiquer si le pointeur doit pointer vers une adresse valide ou s’il doit avoir la valeur null. Par conséquent, cette combinaison n’est pas autorisée.

Plutôt que de \[ **sortir**, [uniques](/windows/desktop/Midl/unique) \] ou \[ **sortants** des pointeurs [ptr](/windows/desktop/Midl/ptr) \] , utilisez \[ **des** pointeurs in, **out**, **unique** \] ou \[ **in**, **out**, **ptr** \] , ou utilisez un autre niveau d’indirection, tel qu’un pointeur de référence qui pointe vers le pointeur unique ou complet valide.

 

 