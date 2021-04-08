---
description: Pour supprimer une application qui a été installée dans l’État publié, désinstallez-la simplement à l’aide de MsiInstallProduct ou MsiConfigureProduct. Vous pouvez également supprimer une application publiée à partir de la ligne de commande. Consultez Options de ligne de commande.
ms.assetid: 979928fc-d95b-4c4e-88bd-aa16fbced736
title: Suppression d’une application publiée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6e8aba31dfd1538afc5585ada41b193c642950a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866077"
---
# <a name="removing-an-advertised-application"></a>Suppression d’une application publiée

Pour supprimer une application qui a été installée dans l’État publié, désinstallez-la simplement à l’aide de [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) ou [**MsiConfigureProduct**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta). Vous pouvez également supprimer une application publiée à partir de la ligne de commande. Consultez [options de ligne de commande](command-line-options.md).

Notez que vous ne pouvez pas supprimer une application publiée si vous avez créé le package de façon à ce que l’exécution d’une installation soit conditionnée par l’instruction **non installée**. Une application publiée n’est pas installée sur l’ordinateur de l’utilisateur et le programme d’installation ne définit pas la propriété [**installed**](installed.md) . Le package doit être créé afin que les applications publiées puissent être désinstallées.

 

 



