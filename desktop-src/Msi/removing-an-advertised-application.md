---
description: Pour supprimer une application qui a été installée dans l’État publié, désinstallez-la simplement à l’aide de MsiInstallProduct ou MsiConfigureProduct. Vous pouvez également supprimer une application publiée à partir de la ligne de commande. Consultez Options de ligne de commande.
ms.assetid: 979928fc-d95b-4c4e-88bd-aa16fbced736
title: Suppression d’une application publiée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 880ce7d7de7ce7a8f9c9a20511f3f9d1b48ccdf34ffd2da51a71d226d0770b54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041579"
---
# <a name="removing-an-advertised-application"></a>Suppression d’une application publiée

Pour supprimer une application qui a été installée dans l’État publié, désinstallez-la simplement à l’aide de [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) ou [**MsiConfigureProduct**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta). Vous pouvez également supprimer une application publiée à partir de la ligne de commande. Consultez [options de ligne de commande](command-line-options.md).

Notez que vous ne pouvez pas supprimer une application publiée si vous avez créé le package de façon à ce que l’exécution d’une installation soit conditionnée par l’instruction **non installée**. Une application publiée n’est pas installée sur l’ordinateur de l’utilisateur et le programme d’installation ne définit pas la propriété [**installed**](installed.md) . Le package doit être créé afin que les applications publiées puissent être désinstallées.

 

 



