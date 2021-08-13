---
description: 'Le processus d’installation réussit deux phases : l’acquisition et l’exécution. En cas d’échec de l’installation, une phase de restauration peut se produire.'
ms.assetid: e9cda321-6978-4f9f-aff4-ccf609c88667
title: Mécanisme d’installation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bce4396701ab5cddb43a67dddbafd1e8310092d04d779af04ad7876681cc3bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118634217"
---
# <a name="installation-mechanism"></a>Mécanisme d’installation

Le processus d’installation réussit deux phases : l’acquisition et l’exécution. En cas d’échec de l’installation, une phase de restauration peut se produire.

## <a name="acquisition"></a>Acquisition

Au début de la phase d’acquisition, une application ou un utilisateur demande au programme d’installation d’installer une fonctionnalité ou une application. Le programme d’installation parcourt ensuite les actions spécifiées dans les tables de séquence de la base de données d’installation. Ces actions interrogent la base de données d’installation et génèrent un script qui fournit une procédure pas-à-pas pour effectuer l’installation.

## <a name="execution"></a>Exécution

Pendant la phase d’exécution, le programme d’installation transmet les informations à un processus avec des privilèges élevés et exécute le script.

## <a name="rollback"></a>Restauration

Si une installation échoue, le programme d’installation restaure l’état d’origine de l’ordinateur. Quand le programme d’installation traite le script d’installation, il génère simultanément un script de restauration. En plus du script de restauration, le programme d’installation enregistre une copie de chaque fichier qu’il supprime pendant l’installation. Ces fichiers sont conservés dans un répertoire système masqué. Une fois l’installation terminée, le script de restauration et les fichiers enregistrés sont supprimés. Pour plus d’informations, consultez [restauration de l’installation](rollback-installation.md).

 

 



