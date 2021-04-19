---
description: Utilisez la procédure suivante pour déboguer les experts écrits en Microsoft Visual C++.
ms.assetid: 7356fcae-3cfe-4a5b-86dd-bebee859fa19
title: Débogage d’un expert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e1a7e6b3998eb18d3ea9c5ef25600a6fc08f1eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523278"
---
# <a name="debugging-an-expert"></a>Débogage d’un expert

Utilisez la procédure suivante pour déboguer les experts écrits en Microsoft Visual C++.

**Débogage d’un expert**

1.  Installez l’expert (fichier DLL) et le fichier de base de données du programme (. pdb) générés lorsque vous avez compilé l’expert à l’emplacement approprié. Pour plus d’informations, consultez [installation d’un expert sur Moniteur réseau 2,1](installing-an-expert-to-network-monitor-2-1.md).
2.  Démarrez Microsoft Visual C++.
3.  Dans le menu **fichier** , cliquez sur **ouvrir** , puis sélectionnez le nom de votre dll d’expert.
4.  Après le chargement de Microsoft Visual C++, cliquez sur le menu **projet** , puis sur **paramètres**.
5.  Cliquez sur **Déboguer**. Sous **exécutable pour session de débogage**, tapez le chemin d’accès complet de Netmon.exe, par exemple :

    ``` syntax
    C:\Program files\Netmon2\Netmon.exe
    ```

6.  Définissez les points d’arrêt dans votre code.

 

 



